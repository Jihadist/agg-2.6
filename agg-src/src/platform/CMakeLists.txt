PROJECT( platform )

CMAKE_MINIMUM_REQUIRED( VERSION 3.0 )
SET( platform_HEADERS
    ${antigrain_SOURCE_DIR}/include/platform/agg_platform_support.h
)

IF(WIN32)
    ADD_LIBRARY( ${PROJECT_NAME} STATIC
        win32/agg_win32_bmp.cpp
        win32/agg_platform_support.cpp
        ${platform_HEADERS}
    )

ENDIF(WIN32)
IF(UNIX)
    ADD_LIBRARY( ${PROJECT_NAME} STATIC
        X11/agg_platform_support.cpp
        ${platform_HEADERS}
    )
ENDIF(UNIX)
IF(APPLE)
    ADD_LIBRARY( ${PROJECT_NAME} STATIC
        mac/agg_mac_pmap.cpp
        mac/agg_platform_support.cpp
        ${platform_HEADERS}
    )
ENDIF(APPLE)

##################################################
# Set all includes, flags, libraries, related to SDL
##################################################
## Does not work with SDL2
IF ( agg_USE_SDL_PLATFORM )
    FIND_PACKAGE( SDL REQUIRED )

    ADD_LIBRARY( sdlplatform STATIC
        sdl/agg_platform_support.cpp
        ${platform_HEADERS}
    )
    TARGET_INCLUDE_DIRECTORIES( sdlplatform PUBLIC ${SDL_INCLUDE_DIR})
    TARGET_LINK_LIBRARIES( sdlplatform PUBLIC ${SDL_LIBRARY})
    TARGET_LINK_LIBRARIES( sdlplatform PUBLIC antigrain)

    ADD_LIBRARY(antigrain::sdlplatform ALIAS sdlplatform)
    TARGET_LINK_LIBRARIES( antigrain_internal INTERFACE antigrain::sdlplatform )

    INSTALL( TARGETS sdlplatform DESTINATION lib )
ENDIF( SDL_FOUND )

TARGET_LINK_LIBRARIES( ${PROJECT_NAME} PUBLIC antigrain )

ADD_LIBRARY( antigrain::platform ALIAS ${PROJECT_NAME})
TARGET_LINK_LIBRARIES( antigrain_internal INTERFACE antigrain::platform )


INSTALL( FILES ${platform_HEADERS} DESTINATION agg/include/platform )
INSTALL( TARGETS ${PROJECT_NAME} DESTINATION lib )
