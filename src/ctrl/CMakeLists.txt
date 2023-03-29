PROJECT( aggctrl )

CMAKE_MINIMUM_REQUIRED( VERSION 3.13 )

SET( controls_HEADERS
    ${antigrain_SOURCE_DIR}/include/ctrl/agg_slider_ctrl.h
    ${antigrain_SOURCE_DIR}/include/ctrl/agg_spline_ctrl.h
    ${antigrain_SOURCE_DIR}/include/ctrl/agg_scale_ctrl.h
    ${antigrain_SOURCE_DIR}/include/ctrl/agg_rbox_ctrl.h
    ${antigrain_SOURCE_DIR}/include/ctrl/agg_polygon_ctrl.h
    ${antigrain_SOURCE_DIR}/include/ctrl/agg_gamma_spline.h
    ${antigrain_SOURCE_DIR}/include/ctrl/agg_gamma_ctrl.h
    ${antigrain_SOURCE_DIR}/include/ctrl/agg_ctrl.h
    ${antigrain_SOURCE_DIR}/include/ctrl/agg_cbox_ctrl.h
    ${antigrain_SOURCE_DIR}/include/ctrl/agg_bezier_ctrl.h
)

ADD_LIBRARY( ${PROJECT_NAME} STATIC
    agg_spline_ctrl.cpp
    agg_slider_ctrl.cpp
    agg_scale_ctrl.cpp
    agg_rbox_ctrl.cpp
    agg_polygon_ctrl.cpp
    agg_gamma_spline.cpp
    agg_gamma_ctrl.cpp
    agg_cbox_ctrl.cpp
    agg_bezier_ctrl.cpp
    ${controls_HEADERS}
)

TARGET_LINK_LIBRARIES( ${PROJECT_NAME} PUBLIC agg )

ADD_LIBRARY( agg::controls ALIAS ${PROJECT_NAME} )
TARGET_LINK_LIBRARIES( agg_internal INTERFACE agg::controls )

SET_TARGET_PROPERTIES(
    ${PROJECT_NAME}
    PROPERTIES
    PUBLIC_HEADER "${controls_HEADERS}"
    VERSION ${agg_VERSION}
    SOVERSION 0.${agg_VERSION}
)

INSTALL(TARGETS ${PROJECT_NAME}
    EXPORT aggTargets DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR} COMPONENT runtime
    ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR} COMPONENT devel
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/agg/ctrl COMPONENT devel
)
