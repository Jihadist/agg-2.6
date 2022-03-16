PROJECT( MyAggApp )


# additional are modified Find routines
SET ( CMAKE_MODULE_PATH "${MyAggApp_BINARY_DIR}" )

CMAKE_MINIMUM_REQUIRED( VERSION 3.0 )



##################################################
# Set all includes, flags, libraries, related to Agg
##################################################

FIND_PACKAGE( Agg )
IF( AGG_FOUND )
    #normally the next is needed, but since this very file is in Agg its source, all is already in place
    #INCLUDE(${AGG_USE_FILE})
ELSE( AGG_FOUND )
    MESSAGE( "AGG library was not found" )
ENDIF( AGG_FOUND )


ADD_EXECUTABLE( my_demo ${WIN32GUI}
    my_demo.cpp
)

TARGET_LINK_LIBRARIES ( my_demo antigrain)

IF( agg_USE_AGG2D )
    ADD_EXECUTABLE( agg2d_demo ${WIN32GUI}
        agg2d_demo.cpp
    )
    TARGET_LINK_LIBRARIES ( agg2d_demo antigrain)
ENDIF( agg_USE_AGG2D )

# for the moment this decides the platform code.
IF(WIN32)
    ADD_DEFINITIONS( -D_CRT_SECURE_NO_WARNINGS -D_CRT_SECURE_NO_DEPRECATE )
    SET( WIN32GUI WIN32 )
ENDIF(WIN32)

IF(UNIX)
    ADD_DEFINITIONS( -D__UNIX__  )
    SET( WIN32GUI "" )

    FIND_PACKAGE(X11)
    IF(X11_FOUND)
        TARGET_INCLUDE_DIRECTORIES( agg2d_demo ${X11_INCLUDE_DIRS})
	TARGET_LINK_LIBRARIES( agg2d_demo ${X11_LIBRARIES})
	TARGET_INCLUDE_DIRECTORIES( my_demo ${X11_INCLUDE_DIRS})
	TARGET_LINK_LIBRARIES( my_demo ${X11_LIBRARIES})
    ENDIF(X11_FOUND)

ENDIF(UNIX)
