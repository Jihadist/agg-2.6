
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
    ${antigrain_SOURCE_DIR}/include/agg_pixfmt_base.h
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
    ${antigrain_SOURCE_DIR}/include/agg_rasterizer_scanline_aa_nogamma.h
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

ADD_LIBRARY( agg STATIC

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

ADD_LIBRARY ( agg_internal INTERFACE )
ADD_LIBRARY( agg::agg ALIAS agg_internal )
TARGET_LINK_LIBRARIES( agg_internal INTERFACE agg )
#controls code for interactive modifying samples
IF ( agg_BUILD_CONTROLS )

    ADD_SUBDIRECTORY( ctrl )

ENDIF ( agg_BUILD_CONTROLS )

# the main include dir of Agg
TARGET_INCLUDE_DIRECTORIES( agg PUBLIC
    $<BUILD_INTERFACE:${antigrain_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include/agg>)


#platform stuff to ease sample use
IF( agg_BUILD_PLATFORM )

    ADD_SUBDIRECTORY( platform )

ENDIF( agg_BUILD_PLATFORM )

SET_TARGET_PROPERTIES(
    agg
    PROPERTIES
    PUBLIC_HEADER "${antigrain_HEADERS}"
    VERSION ${agg_VERSION}
    SOVERSION 0.${agg_VERSION}
)

INSTALL(TARGETS agg
    EXPORT aggTargets DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR} COMPONENT runtime
    ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR} COMPONENT devel
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/agg COMPONENT devel
)

INSTALL(EXPORT aggTargets
    DESTINATION ${CMAKE_INSTALL_LIBDIR}/cmake/agg/
    FILE aggTargets.cmake
    NAMESPACE ${PROJECT_NAME}::
    COMPONENT devel
)
