
SET( antigrain_HEADERS
    ${antigrain_SOURCE_DIR}/include/agg_alpha_mask_u8.h
    ${antigrain_SOURCE_DIR}/include/agg_arc.h
    ${antigrain_SOURCE_DIR}/include/agg_array.h
    ${antigrain_SOURCE_DIR}/include/agg_arrowhead.h
    ${antigrain_SOURCE_DIR}/include/agg_basics.h
    ${antigrain_SOURCE_DIR}/include/agg_bezier_arc.h
    ${antigrain_SOURCE_DIR}/include/agg_bitset_iterator.h
    ${antigrain_SOURCE_DIR}/include/agg_blur.h
    ${antigrain_SOURCE_DIR}/include/agg_bounding_rect.h
    ${antigrain_SOURCE_DIR}/include/agg_bspline.h
    ${antigrain_SOURCE_DIR}/include/agg_clip_liang_barsky.h
    ${antigrain_SOURCE_DIR}/include/agg_color_gray.h
    ${antigrain_SOURCE_DIR}/include/agg_color_rgba.h
    ${antigrain_SOURCE_DIR}/include/agg_config.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_adaptor_vcgen.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_adaptor_vpgen.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_bspline.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_clip_polygon.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_clip_polyline.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_close_polygon.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_concat.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_contour.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_curve.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_dash.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_gpc.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_marker.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_marker_adaptor.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_segmentator.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_shorten_path.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_smooth_poly1.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_stroke.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_transform.h
    ${antigrain_SOURCE_DIR}/include/agg_conv_unclose_polygon.h
    ${antigrain_SOURCE_DIR}/include/agg_curves.h
    ${antigrain_SOURCE_DIR}/include/agg_dda_line.h
    ${antigrain_SOURCE_DIR}/include/agg_ellipse.h
    ${antigrain_SOURCE_DIR}/include/agg_ellipse_bresenham.h
    ${antigrain_SOURCE_DIR}/include/agg_embedded_raster_fonts.h
    ${antigrain_SOURCE_DIR}/include/agg_font_cache_manager.h
    ${antigrain_SOURCE_DIR}/include/agg_gamma_functions.h
    ${antigrain_SOURCE_DIR}/include/agg_gamma_lut.h
    ${antigrain_SOURCE_DIR}/include/agg_glyph_raster_bin.h
    ${antigrain_SOURCE_DIR}/include/agg_gradient_lut.h
    ${antigrain_SOURCE_DIR}/include/agg_gsv_text.h
    ${antigrain_SOURCE_DIR}/include/agg_image_accessors.h
    ${antigrain_SOURCE_DIR}/include/agg_image_filters.h
    ${antigrain_SOURCE_DIR}/include/agg_line_aa_basics.h
    ${antigrain_SOURCE_DIR}/include/agg_math.h
    ${antigrain_SOURCE_DIR}/include/agg_math_stroke.h
    ${antigrain_SOURCE_DIR}/include/agg_path_length.h
    ${antigrain_SOURCE_DIR}/include/agg_path_storage.h
    ${antigrain_SOURCE_DIR}/include/agg_path_storage_integer.h
    ${antigrain_SOURCE_DIR}/include/agg_pattern_filters_rgba.h
    ${antigrain_SOURCE_DIR}/include/agg_pixfmt_amask_adaptor.h
    ${antigrain_SOURCE_DIR}/include/agg_pixfmt_gray.h
    ${antigrain_SOURCE_DIR}/include/agg_pixfmt_rgb.h
    ${antigrain_SOURCE_DIR}/include/agg_pixfmt_rgb_packed.h
    ${antigrain_SOURCE_DIR}/include/agg_pixfmt_rgba.h
    ${antigrain_SOURCE_DIR}/include/agg_pixfmt_transposer.h
    ${antigrain_SOURCE_DIR}/include/agg_rasterizer_cells_aa.h
    ${antigrain_SOURCE_DIR}/include/agg_rasterizer_compound_aa.h
    ${antigrain_SOURCE_DIR}/include/agg_rasterizer_outline.h
    ${antigrain_SOURCE_DIR}/include/agg_rasterizer_outline_aa.h
    ${antigrain_SOURCE_DIR}/include/agg_rasterizer_scanline_aa.h
    ${antigrain_SOURCE_DIR}/include/agg_rasterizer_sl_clip.h
    ${antigrain_SOURCE_DIR}/include/agg_renderer_base.h
    ${antigrain_SOURCE_DIR}/include/agg_renderer_markers.h
    ${antigrain_SOURCE_DIR}/include/agg_renderer_mclip.h
    ${antigrain_SOURCE_DIR}/include/agg_renderer_outline_aa.h
    ${antigrain_SOURCE_DIR}/include/agg_renderer_outline_image.h
    ${antigrain_SOURCE_DIR}/include/agg_renderer_primitives.h
    ${antigrain_SOURCE_DIR}/include/agg_renderer_raster_text.h
    ${antigrain_SOURCE_DIR}/include/agg_renderer_scanline.h
    ${antigrain_SOURCE_DIR}/include/agg_rendering_buffer.h
    ${antigrain_SOURCE_DIR}/include/agg_rendering_buffer_dynarow.h
    ${antigrain_SOURCE_DIR}/include/agg_rounded_rect.h
    ${antigrain_SOURCE_DIR}/include/agg_scanline_bin.h
    ${antigrain_SOURCE_DIR}/include/agg_scanline_boolean_algebra.h
    ${antigrain_SOURCE_DIR}/include/agg_scanline_p.h
    ${antigrain_SOURCE_DIR}/include/agg_scanline_storage_aa.h
    ${antigrain_SOURCE_DIR}/include/agg_scanline_storage_bin.h
    ${antigrain_SOURCE_DIR}/include/agg_scanline_u.h
    ${antigrain_SOURCE_DIR}/include/agg_shorten_path.h
    ${antigrain_SOURCE_DIR}/include/agg_simul_eq.h
    ${antigrain_SOURCE_DIR}/include/agg_span_allocator.h
    ${antigrain_SOURCE_DIR}/include/agg_span_converter.h
    ${antigrain_SOURCE_DIR}/include/agg_span_gouraud.h
    ${antigrain_SOURCE_DIR}/include/agg_span_gouraud_gray.h
    ${antigrain_SOURCE_DIR}/include/agg_span_gouraud_rgba.h
    ${antigrain_SOURCE_DIR}/include/agg_span_gradient.h
    ${antigrain_SOURCE_DIR}/include/agg_span_gradient_alpha.h
    ${antigrain_SOURCE_DIR}/include/agg_span_image_filter.h
    ${antigrain_SOURCE_DIR}/include/agg_span_image_filter_gray.h
    ${antigrain_SOURCE_DIR}/include/agg_span_image_filter_rgb.h
    ${antigrain_SOURCE_DIR}/include/agg_span_image_filter_rgba.h
    ${antigrain_SOURCE_DIR}/include/agg_span_interpolator_adaptor.h
    ${antigrain_SOURCE_DIR}/include/agg_span_interpolator_linear.h
    ${antigrain_SOURCE_DIR}/include/agg_span_interpolator_persp.h
    ${antigrain_SOURCE_DIR}/include/agg_span_interpolator_trans.h
    ${antigrain_SOURCE_DIR}/include/agg_span_pattern_gray.h
    ${antigrain_SOURCE_DIR}/include/agg_span_pattern_rgb.h
    ${antigrain_SOURCE_DIR}/include/agg_span_pattern_rgba.h
    ${antigrain_SOURCE_DIR}/include/agg_span_solid.h
    ${antigrain_SOURCE_DIR}/include/agg_span_subdiv_adaptor.h
    ${antigrain_SOURCE_DIR}/include/agg_trans_affine.h
    ${antigrain_SOURCE_DIR}/include/agg_trans_bilinear.h
    ${antigrain_SOURCE_DIR}/include/agg_trans_double_path.h
    ${antigrain_SOURCE_DIR}/include/agg_trans_perspective.h
    ${antigrain_SOURCE_DIR}/include/agg_trans_single_path.h
    ${antigrain_SOURCE_DIR}/include/agg_trans_viewport.h
    ${antigrain_SOURCE_DIR}/include/agg_trans_warp_magnifier.h
    ${antigrain_SOURCE_DIR}/include/agg_vcgen_bspline.h
    ${antigrain_SOURCE_DIR}/include/agg_vcgen_contour.h
    ${antigrain_SOURCE_DIR}/include/agg_vcgen_dash.h
    ${antigrain_SOURCE_DIR}/include/agg_vcgen_markers_term.h
    ${antigrain_SOURCE_DIR}/include/agg_vcgen_smooth_poly1.h
    ${antigrain_SOURCE_DIR}/include/agg_vcgen_stroke.h
    ${antigrain_SOURCE_DIR}/include/agg_vcgen_vertex_sequence.h
    ${antigrain_SOURCE_DIR}/include/agg_vertex_sequence.h
    ${antigrain_SOURCE_DIR}/include/agg_vpgen_clip_polygon.h
    ${antigrain_SOURCE_DIR}/include/agg_vpgen_clip_polyline.h
    ${antigrain_SOURCE_DIR}/include/agg_vpgen_segmentator.h

    ${antigrain_SOURCE_DIR}/include/agg_span_gradient_contour.h
    ${antigrain_SOURCE_DIR}/include/agg_span_gradient_image.h
)

ADD_LIBRARY( antigrain

    agg_arc.cpp
    agg_arrowhead.cpp
    agg_bezier_arc.cpp
    agg_bspline.cpp
    agg_curves.cpp
    agg_embedded_raster_fonts.cpp
    agg_gsv_text.cpp
    agg_image_filters.cpp
    agg_line_aa_basics.cpp
    agg_line_profile_aa.cpp
    agg_rounded_rect.cpp
    agg_sqrt_tables.cpp
    agg_trans_affine.cpp
    agg_trans_double_path.cpp
    agg_trans_single_path.cpp
    agg_trans_warp_magnifier.cpp
    agg_vcgen_bspline.cpp
    agg_vcgen_contour.cpp
    agg_vcgen_dash.cpp
    agg_vcgen_markers_term.cpp
    agg_vcgen_smooth_poly1.cpp
    agg_vcgen_stroke.cpp
    agg_vpgen_clip_polygon.cpp
    agg_vpgen_segmentator.cpp

    ${antigrain_HEADERS}
)

#controls code for interactive modifying samples
IF( agg_BUILD_CONTROLS )
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

    ADD_LIBRARY( controls
	ctrl/agg_spline_ctrl.cpp
	ctrl/agg_slider_ctrl.cpp
	ctrl/agg_scale_ctrl.cpp
	ctrl/agg_rbox_ctrl.cpp
	ctrl/agg_polygon_ctrl.cpp
	ctrl/agg_gamma_spline.cpp
	ctrl/agg_gamma_ctrl.cpp
	ctrl/agg_cbox_ctrl.cpp
	ctrl/agg_bezier_ctrl.cpp

	${controls_HEADERS}
    )
    TARGET_INCLUDE_DIRECTORIES( controls PRIVATE ${antigrain_SOURCE_DIR}/include )
    TARGET_INCLUDE_DIRECTORIES( controls PUBLIC ${antigrain_SOURCE_DIR}/include/ctrl )
    TARGET_LINK_LIBRARIES( antigrain PUBLIC controls )

ENDIF( agg_BUILD_CONTROLS )

# the main include dir of Agg
TARGET_INCLUDE_DIRECTORIES( antigrain PUBLIC ${antigrain_SOURCE_DIR}/include )
SET( AGG_INCLUDE_DIRS ${AGG_INCLUDE_DIRS} include )

##################################################
# Set all includes, flags, libraries, related to expat
##################################################

IF( agg_USE_EXPAT )

    FIND_PACKAGE( EXPAT )

    IF(EXPAT_FOUND)
        TARGET_INCLUDE_DIRECTORIES( antigrain PUBLIC ${EXPAT_INCLUDE_DIRS})
	TARGET_LINK_LIBRARIES( antigrain PUBLIC ${EXPAT_LIBRARIES})
    ELSE(EXPAT_FOUND)
        MESSAGE(SEND_ERROR "expat not found")
    ENDIF(EXPAT_FOUND)
ENDIF( agg_USE_EXPAT )





##################################################
# Set all includes, flags, libraries, related to freetype
##################################################

IF ( agg_USE_FREETYPE )
    FIND_PACKAGE( Freetype )
    IF( FREETYPE_FOUND )

        ADD_LIBRARY( freetypefont
	    ../font_freetype/agg_font_freetype.h
	    ../font_freetype/agg_font_freetype.cpp
	)
        TARGET_INCLUDE_DIRECTORIES( freetypefont PUBLIC ${FREETYPE_INCLUDE_DIRS} )
	TARGET_LINK_LIBRARIES( freetypefont PUBLIC ${FREETYPE_LIBRARIES} )
	TARGET_LINK_DIRECTORIES( freetypefont PUBLIC ${FREETYPE_LINK_DIR} )
	SET( AGG_INCLUDE_DIRS ${AGG_INCLUDE_DIRS} font_freetype )
	TARGET_COMPILE_DEFINITIONS( freetypefont PUBLIC -DAGG_USE_FREETYPE )
	SET( AGG_FLAGS ${AGG_FLAGS} -DAGG_USE_FREETYPE )
	TARGET_LINK_DIRECTORIES( antigrain PUBLIC freetypefont )
	SET( AGG_LIBRARIES ${AGG_LIBRARIES} aggfontfreetype${PFDEBUG} )
	TARGET_INCLUDE_DIRECTORIES( freetypefont PUBLIC ${antigrain_SOURCE_DIR}/font_freetype )
	SET_TARGET_PROPERTIES( freetypefont  PROPERTIES OUTPUT_NAME aggfontfreetype${PFDEBUG} )

	INSTALL( TARGETS freetypefont DESTINATION lib )
	    INSTALL( FILES ../font_freetype/agg_font_freetype.h DESTINATION agg/font_freetype )
    ELSE( FREETYPE_FOUND )
        MESSAGE(SEND_ERROR "freetype not found")
    ENDIF( FREETYPE_FOUND )
ENDIF ( agg_USE_FREETYPE )

#platform stuff to ease sample use
IF( agg_BUILD_PLATFORM )
    SET( platform_HEADERS
	${antigrain_SOURCE_DIR}/include/platform/agg_platform_support.h
    )

    IF(WIN32)

	ADD_LIBRARY( platform
	    ../src/platform/win32/agg_win32_bmp.cpp
	    ../src/platform/win32/agg_platform_support.cpp
	    ../font_win32_tt/agg_font_win32_tt.cpp

	            ${platform_HEADERS}
	)
        TARGET_INCLUDE_DIRECTORIES( platform PRIVATE ${antigrain_SOURCE_DIR}/include )
	TARGET_INCLUDE_DIRECTORIES( platform PUBLIC ${antigrain_SOURCE_DIR}/font_win32_tt )
            INSTALL( FILES ../font_win32_tt/agg_font_win32_tt.h DESTINATION agg/font_win32_tt )
    ENDIF(WIN32)
    IF(UNIX)
        ADD_LIBRARY( platform
	    ../src/platform/X11/agg_platform_support.cpp

	            ${platform_HEADERS}
	)
    ENDIF(UNIX)
    IF(APPLE)
        ADD_LIBRARY( platform
	    ../src/platform/mac/agg_mac_pmap.cpp
	    ../src/platform/mac/agg_platform_support.cpp

	            ${platform_HEADERS}
	)
    ENDIF(APPLE)

    ##################################################
    # Set all includes, flags, libraries, related to SDL
    ##################################################
    FIND_PACKAGE( SDL QUIET )
    IF( SDL_FOUND )
        IF ( agg_USE_SDL_PLATFORM )
	    SET( AGG_LIBRARIES ${AGG_LIBRARIES} aggctrl${PFDEBUG} aggsdlplatform${PFDEBUG} agg${PFDEBUG} )

	    ADD_LIBRARY( sdlplatform
		../src/platform/sdl/agg_platform_support.cpp

		        ${platform_HEADERS}
	    )
	    TARGET_INCLUDE_DIRECTORIES( sdlplatform PUBLIC ${SDL_INCLUDE_DIR})
	    TARGET_LINK_LIBRARIES( sdlplatform PUBLIC ${SDL_LIBRARY})
	    TARGET_LINK_LIBRARIES( antigrain PUBLIC sdlplatform)
	    INSTALL( TARGETS sdlplatform DESTINATION lib )
	    SET_TARGET_PROPERTIES( sdlplatform  PROPERTIES OUTPUT_NAME aggsdlplatform${PFDEBUG} )
	ENDIF ( agg_USE_SDL_PLATFORM )
    ELSE( SDL_FOUND )
        IF ( agg_USE_SDL_PLATFORM )
	    MESSAGE( "SDL libray was not found, disable agg_USE_SDL_PLATFORM please" )
	ENDIF ( agg_USE_SDL_PLATFORM )

	TARGET_LINK_LIBRARIES( antigrain PUBLIC platform)
	SET( AGG_LIBRARIES ${AGG_LIBRARIES} aggctrl${PFDEBUG} aggplatform${PFDEBUG} agg${PFDEBUG} )
    ENDIF( SDL_FOUND )

ENDIF( agg_BUILD_PLATFORM )

# boolean operations library GPC

IF ( agg_USE_GPC )

    ADD_LIBRARY( gpcbool
        ../gpc/gpc.c
        ../gpc/gpc.h
    )
    TARGET_INCLUDE_DIRECTORIES( gpcbool PUBLIC ${antigrain_SOURCE_DIR}/gpc )
    SET( AGG_INCLUDE_DIRS ${AGG_INCLUDE_DIRS} gpc )
    TARGET_COMPILE_DEFINITIONS( gpcbool PUBLIC -DAGG_USE_GPC )
    SET( AGG_FLAGS ${AGG_FLAGS} -DAGG_USE_GPC )
    TARGET_LINK_LIBRARIES( antigrain PUBLIC gpcbool )
    SET( AGG_LIBRARIES ${AGG_LIBRARIES} gpc${PFDEBUG} )


    INSTALL( TARGETS gpcbool DESTINATION lib )
	INSTALL( FILES ../gpc/gpc.h DESTINATION agg/gpc )	
    SET_TARGET_PROPERTIES( gpcbool   PROPERTIES OUTPUT_NAME gpc${PFDEBUG} )
ENDIF ( agg_USE_GPC )

IF ( agg_USE_AGG2D )

    ADD_LIBRARY( agg2d
        ../agg2d/agg2d.cpp
        ../agg2d/agg2d.h
    )
    TARGET_INCLUDE_DIRECTORIES( agg2d PUBLIC ${antigrain_SOURCE_DIR}/agg2d )
    SET( AGG_INCLUDE_DIRS ${AGG_INCLUDE_DIRS} agg2d )
    TARGET_COMPILE_DEFINITIONS( agg2d PUBLIC -DAGG_USE_AGG2D )
    OPTION( agg_USE_AGG2D_FREETYPE "Agg 2D graphical context uses freetype" OFF)
    SET( AGG_FLAGS ${AGG_FLAGS} -DAGG_USE_AGG2D )
    TARGET_LINK_LIBRARIES( antigrain PUBLIC agg2d )
    SET( AGG_LIBRARIES ${AGG_LIBRARIES} agg2d${PFDEBUG} )

    INSTALL( TARGETS agg2d DESTINATION lib )
	INSTALL( FILES ../agg2d/agg2d.h DESTINATION agg/agg2d )	
    SET_TARGET_PROPERTIES( agg2d  PROPERTIES OUTPUT_NAME agg2d${PFDEBUG} )
ENDIF ( agg_USE_AGG2D )

IF ( agg_USE_AGG2D_FREETYPE )
    ADD_DEFINITIONS( -DAGG2D_USE_FREETYPE )
    SET( AGG_FLAGS ${AGG_FLAGS} -DAGG2D_USE_FREETYPE )
ENDIF ( agg_USE_AGG2D_FREETYPE )

SET_TARGET_PROPERTIES( antigrain PROPERTIES OUTPUT_NAME agg${PFDEBUG} )
INSTALL( FILES ${antigrain_HEADERS} DESTINATION agg/include )
INSTALL( TARGETS antigrain DESTINATION lib )
IF( agg_BUILD_PLATFORM )
    SET_TARGET_PROPERTIES( platform  PROPERTIES OUTPUT_NAME aggplatform${PFDEBUG} )
    INSTALL( FILES ${platform_HEADERS} DESTINATION agg/include/platform )
    INSTALL( TARGETS platform DESTINATION lib )
ENDIF( agg_BUILD_PLATFORM )
IF( agg_BUILD_CONTROLS )
    SET_TARGET_PROPERTIES( controls  PROPERTIES OUTPUT_NAME aggctrl${PFDEBUG} )
    INSTALL( FILES ${controls_HEADERS} DESTINATION agg/include/ctrl )
    INSTALL( TARGETS controls DESTINATION lib )
ENDIF( agg_BUILD_CONTROLS )


SET( AGG_FLAGS ${AGG_FLAGS} CACHE STRING "Agg package flags" FORCE )
SET( AGG_INCLUDE_DIRS ${AGG_INCLUDE_DIRS} CACHE STRING "Agg package libs include paths" FORCE )
SET( AGG_LIBRARY_DIRS ${AGG_LIBRARY_DIRS} CACHE STRING "Agg package libs directory paths" FORCE )
SET( AGG_LIBRARIES ${AGG_LIBRARIES} CACHE STRING "Agg package libraries" FORCE )
