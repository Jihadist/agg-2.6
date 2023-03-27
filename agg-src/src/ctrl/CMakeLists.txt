PROJECT( controls )

CMAKE_MINIMUM_REQUIRED( VERSION 3.0 )


SET( controls_HEADERS
    ${CMAKE_CURRENT_SOURCE_DIR}/../../include/ctrl/agg_slider_ctrl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/../../include/ctrl/agg_spline_ctrl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/../../include/ctrl/agg_scale_ctrl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/../../include/ctrl/agg_rbox_ctrl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/../../include/ctrl/agg_polygon_ctrl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/../../include/ctrl/agg_gamma_spline.h
    ${CMAKE_CURRENT_SOURCE_DIR}/../../include/ctrl/agg_gamma_ctrl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/../../include/ctrl/agg_ctrl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/../../include/ctrl/agg_cbox_ctrl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/../../include/ctrl/agg_bezier_ctrl.h
)

ADD_LIBRARY( controls
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
TARGET_INCLUDE_DIRECTORIES( controls PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} )
TARGET_LINK_LIBRARIES( controls PRIVATE antigrain )
TARGET_LINK_LIBRARIES( antigrain INTERFACE controls )

INSTALL( FILES ${controls_HEADERS} DESTINATION agg/include/ctrl )
INSTALL( TARGETS controls DESTINATION lib )
