PROJECT( MyAggApp )


CMAKE_MINIMUM_REQUIRED( VERSION 3.13 )


ADD_EXECUTABLE( my_demo ${WIN32GUI}
    my_demo.cpp
)

TARGET_LINK_LIBRARIES ( my_demo antigrain::antigrain )

IF( agg_USE_AGG2D )
    ADD_EXECUTABLE( agg2d_demo ${WIN32GUI}
        agg2d_demo.cpp
    )
    TARGET_LINK_LIBRARIES ( agg2d_demo antigrain::antigrain )
ENDIF( agg_USE_AGG2D )

# for the moment this decides the platform code.
IF(WIN32)
    ADD_DEFINITIONS( -D_CRT_SECURE_NO_WARNINGS -D_CRT_SECURE_NO_DEPRECATE )
    SET( WIN32GUI WIN32 )
ENDIF(WIN32)

IF(UNIX)
    SET( WIN32GUI "" )

ENDIF(UNIX)
