PROJECT( antigrain )

# additional are modified Find routines
SET ( CMAKE_MODULE_PATH "${antigrain_SOURCE_DIR}/bin" )

CMAKE_MINIMUM_REQUIRED( VERSION 3.0 )

SET(AGG_MAJOR_VERSION 0 )
SET(AGG_MINOR_VERSION 1 )
SET(AGG_BUILD_VERSION 1 )

SET( AGG_FLAGS "" )
SET( AGG_INCLUDE_DIRS "" )
SET( AGG_LIBRARY_DIRS "" )
SET( AGG_LIBRARIES "" )

SET (LIBRARY_OUTPUT_PATH ${antigrain_BINARY_DIR}/lib/ CACHE PATH "Single output directory for building all libraries." FORCE )
SET( AGG_LIBRARY_DIRS  lib )
#SET (EXECUTABLE_OUTPUT_PATH ${antigrain_BINARY_DIR}/exe/ CACHE PATH "Single output directory for building all executables.")
#MARK_AS_ADVANCED(LIBRARY_OUTPUT_PATH EXECUTABLE_OUTPUT_PATH)

LINK_DIRECTORIES(  ${antigrain_BINARY_DIR}/lib )

OPTION( agg_USE_GPC "Use Gpc Boolean library" OFF)
OPTION( agg_USE_FREETYPE "Use Freetype library" OFF)
OPTION( agg_USE_EXPAT "Use Expat library" OFF)
OPTION( agg_USE_SDL_PLATFORM "Use SDL as platform" OFF)
OPTION( agg_USE_PACK "Package Agg" OFF)
OPTION( agg_USE_AGG2D "Agg 2D graphical context" OFF)
OPTION( agg_USE_DEBUG "For debug version" OFF)
OPTION( agg_BUILD_EXAMPLES "Build the AGG examples" ON)
OPTION( agg_BUILD_DEMO "Build the AGG demo" ON)
OPTION( agg_BUILD_PLATFORM "Build the AGG platform helper" ON)
OPTION( agg_BUILD_CONTROLS "Build the AGG controls" ON)

IF( agg_BUILD_DEMO OR agg_BUILD_EXAMPLES )
    MESSAGE(STATUS "Force enable the platform and controls helper due to Demo / Example being build.")
    SET( agg_BUILD_PLATFORM ON CACHE BOOL "Build the AGG platform helper" FORCE)
    SET( agg_BUILD_CONTROLS ON CACHE BOOL "Build the AGG controls" FORCE)
ENDIF( agg_BUILD_DEMO OR agg_BUILD_EXAMPLES )

IF( agg_USE_DEBUG )
    #SET( PFDEBUG "d" )
    SET( CMAKE_DEBUG_POSTFIX "d" )
ENDIF( agg_USE_DEBUG )

# for the moment this decides the platform code.
IF(WIN32)
    ADD_DEFINITIONS( -D_MSWVC_ -D_CRT_SECURE_NO_WARNINGS -D_CRT_SECURE_NO_DEPRECATE )
    SET( WIN32GUI WIN32 )    
    INCLUDE_DIRECTORIES( ${antigrain_SOURCE_DIR}/font_win32_tt )
    SET( AGG_INCLUDE_DIRS ${AGG_INCLUDE_DIRS} font_win32_tt )    
ENDIF(WIN32)

IF(UNIX)
    ADD_DEFINITIONS( -D__UNIX__  )
    SET( WIN32GUI "" )

    FIND_PACKAGE(X11)
    IF(X11_FOUND)  
        INCLUDE_DIRECTORIES(${X11_INCLUDE_DIRS})
        LINK_LIBRARIES(${X11_LIBRARIES})
    ENDIF(X11_FOUND)

ENDIF(UNIX)

# more specific set platform code part to use for different compilers/tool sets
IF ( ${CMAKE_GENERATOR} STREQUAL "MSYS Makefiles" )
	SET (CMAKE_CXX_FLAGS_RELEASE "-DNDEBUG" CACHE STRING
		"Flags used by the compiler during release builds" FORCE)
	SET (CMAKE_CX_FLAGS_RELEASE "-DNDEBUG" CACHE STRING
		"Flags used by the compiler during release builds" FORCE)		
ENDIF ( ${CMAKE_GENERATOR} STREQUAL "MSYS Makefiles" )

IF ( ${CMAKE_GENERATOR} STREQUAL "MinGW Makefiles" )
	
ENDIF ( ${CMAKE_GENERATOR} STREQUAL "MinGW Makefiles" )

IF ( ${CMAKE_GENERATOR} STREQUAL "Unix Makefiles" )
    IF( CYGWIN OR MINGW )
		SET (CMAKE_CXX_FLAGS_RELEASE "-DNDEBUG" CACHE STRING
			"Flags used by the compiler during release builds" FORCE)
		SET (CMAKE_C_FLAGS_RELEASE "-DNDEBUG" CACHE STRING
			"Flags used by the compiler during release builds" FORCE)
    ENDIF( CYGWIN OR MINGW )	
ENDIF ( ${CMAKE_GENERATOR} STREQUAL "Unix Makefiles" )

IF ( ${CMAKE_GENERATOR} MATCHES "Visual Studio.*" )
	
ENDIF ( ${CMAKE_GENERATOR} MATCHES "Visual Studio.*" )

IF ( ${CMAKE_GENERATOR} MATCHES "Borland Makefiles" )

ENDIF ( ${CMAKE_GENERATOR} MATCHES "Borland Makefiles" )


ADD_SUBDIRECTORY( src )

IF ( agg_BUILD_EXAMPLES )
    ADD_SUBDIRECTORY( examples )
ENDIF( agg_BUILD_EXAMPLES )

CONFIGURE_FILE( ${antigrain_SOURCE_DIR}/bin/AggConfig.cmake.in
                ${antigrain_BINARY_DIR}/bin/AggConfig.cmake
                @ONLY IMMEDIATE )

CONFIGURE_FILE( ${antigrain_SOURCE_DIR}/bin/AggConfigOutBuild.cmake.in
                ${antigrain_BINARY_DIR}/bin/AggConfigOutBuild.cmake
                @ONLY IMMEDIATE )
                
CONFIGURE_FILE( ${antigrain_SOURCE_DIR}/bin/FindAgg.cmake
                ${antigrain_BINARY_DIR}/myapp/FindAgg.cmake
                @ONLY IMMEDIATE )

CONFIGURE_FILE( ${antigrain_SOURCE_DIR}/bin/UseAgg.cmake.in
                ${antigrain_BINARY_DIR}/bin/UseAgg.cmake
                @ONLY IMMEDIATE )

IF ( agg_BUILD_DEMO )
    ADD_SUBDIRECTORY( myapp )
ENDIF ( agg_BUILD_DEMO )

INSTALL( FILES ${antigrain_BINARY_DIR}/bin/AggConfigOutBuild.cmake DESTINATION "bin" RENAME AggConfig.cmake )
INSTALL( FILES ${antigrain_BINARY_DIR}/bin/AggConfig.cmake DESTINATION "bin" )
INSTALL( FILES ${antigrain_BINARY_DIR}/bin/UseAgg.cmake DESTINATION "bin" )

#-------------------------------------------------------------------
# Build a CPack installer if CPack is available and this is a build 
IF ( agg_USE_PACK )    
    IF(EXISTS "${CMAKE_ROOT}/Modules/CPack.cmake")
        SET(CPACK_PACKAGE_DESCRIPTION_SUMMARY "Agg - Vector Graphics")
        SET(CPACK_PACKAGE_VENDOR "Agg")
        SET(CPACK_PACKAGE_DESCRIPTION_FILE "${CMAKE_CURRENT_SOURCE_DIR}/copying")
        SET(CPACK_RESOURCE_FILE_LICENSE "${CMAKE_CURRENT_SOURCE_DIR}/copying")
        SET(CPACK_PACKAGE_VERSION_MAJOR "${AGG_MAJOR_VERSION}")
        SET(CPACK_PACKAGE_VERSION_MINOR "${AGG_MINOR_VERSION}")
        SET(CPACK_PACKAGE_VERSION_PATCH "${AGG_BUILD_VERSION}")
        SET(CPACK_PACKAGE_INSTALL_DIRECTORY "AGG_${CPACK_PACKAGE_VERSION_MAJOR}.${CPACK_PACKAGE_VERSION_MINOR}")
        SET(CPACK_SOURCE_PACKAGE_FILE_NAME "agg-${CPACK_PACKAGE_VERSION_MAJOR}.${CPACK_PACKAGE_VERSION_MINOR}.${CPACK_PACKAGE_VERSION_PATCH}")
        SET(CPACK_PACKAGE_EXECUTABLES
        "agg" "AGG"
        )
        SET(CPACK_SOURCE_STRIP_FILES "")
        SET(CPACK_STRIP_FILES "bin/ccmake;bin/cmake;bin/cpack;bin/ctest")
 

        IF(WIN32)
            SET(CPACK_NSIS_DISPLAY_NAME "${CPACK_PACKAGE_INSTALL_DIRECTORY}")
            SET(CPACK_NSIS_HELP_LINK "http://agg.sourceforge.net")
            SET(CPACK_NSIS_URL_INFO_ABOUT "http://agg.sourceforge.net")
            SET(CPACK_NSIS_CONTACT "http://agg.sourceforge.net")
        ENDIF(WIN32)

        INCLUDE(CPack)
    ENDIF(EXISTS "${CMAKE_ROOT}/Modules/CPack.cmake")   
ENDIF ( agg_USE_PACK )

INCLUDE( myapp/myproject.cmake )
