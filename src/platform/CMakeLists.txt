PROJECT( platform )

CMAKE_MINIMUM_REQUIRED( VERSION 3.13 )

SET( platform_HEADERS
    ${antigrain_SOURCE_DIR}/include/platform/agg_platform_support.h
)

IF(WIN32)

    ADD_SUBDIRECTORY( win32 )

ENDIF(WIN32)
IF(UNIX)

    ADD_SUBDIRECTORY( X11 )

ENDIF(UNIX)
IF(APPLE)

    ADD_SUBDIRECTORY( mac )

ENDIF(APPLE)

##################################################
# Set all includes, flags, libraries, related to SDL
##################################################
## Does not work with SDL2
IF ( agg_USE_SDL_PLATFORM )

    ADD_SUBDIRECTORY( sdl )

ENDIF ( agg_USE_SDL_PLATFORM )



