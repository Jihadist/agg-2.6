
##################################################
# Set all includes, flags, libraries, related to expat
##################################################

IF( agg_USE_EXPAT )

    FIND_PACKAGE( EXPAT CONFIG REQUIRED )

ENDIF( agg_USE_EXPAT )

ADD_EXECUTABLE( aa_demo ${WIN32GUI}
    aa_demo.cpp
)

TARGET_LINK_LIBRARIES( aa_demo agg::agg )

ADD_EXECUTABLE( aa_test ${WIN32GUI}
    aa_test.cpp
)

TARGET_LINK_LIBRARIES( aa_test agg::agg )

ADD_EXECUTABLE( alpha_gradient ${WIN32GUI}
    alpha_gradient.cpp
)

TARGET_LINK_LIBRARIES( alpha_gradient agg::agg )

ADD_EXECUTABLE( alpha_mask ${WIN32GUI}
    alpha_mask.cpp
    parse_lion.cpp
)

TARGET_LINK_LIBRARIES( alpha_mask agg::agg )

ADD_EXECUTABLE( alpha_mask2 ${WIN32GUI}
    alpha_mask.cpp
    parse_lion.cpp
)

TARGET_LINK_LIBRARIES( alpha_mask2 agg::agg )

ADD_EXECUTABLE( alpha_mask3 ${WIN32GUI}
    alpha_mask.cpp
    make_arrows.cpp
    make_gb_poly.cpp
    parse_lion.cpp
)

TARGET_LINK_LIBRARIES( alpha_mask3 agg::agg )

ADD_EXECUTABLE( bezier_div ${WIN32GUI}
    bezier_div.cpp
    interactive_polygon.cpp
)

TARGET_LINK_LIBRARIES( bezier_div agg::agg )

ADD_EXECUTABLE( blend_color ${WIN32GUI}
    blend_color.cpp
)

TARGET_LINK_LIBRARIES( blend_color agg::agg )

ADD_EXECUTABLE( blur ${WIN32GUI}
    blur.cpp
)

TARGET_LINK_LIBRARIES( blur agg::agg )

ADD_EXECUTABLE( bspline ${WIN32GUI}
    bspline.cpp
    interactive_polygon.cpp
)

TARGET_LINK_LIBRARIES( bspline agg::agg )

ADD_EXECUTABLE( circles ${WIN32GUI}
    circles.cpp
)

TARGET_LINK_LIBRARIES( circles agg::agg )

ADD_EXECUTABLE( component_rendering ${WIN32GUI}
    component_rendering.cpp
)

TARGET_LINK_LIBRARIES( component_rendering agg::agg )

ADD_EXECUTABLE( compositing ${WIN32GUI}
    compositing.cpp
)

TARGET_LINK_LIBRARIES( compositing agg::agg )

ADD_EXECUTABLE( compositing2 ${WIN32GUI}
    compositing2.cpp
)

TARGET_LINK_LIBRARIES( compositing2 agg::agg )

ADD_EXECUTABLE( conv_contour ${WIN32GUI}
    conv_contour.cpp
)

TARGET_LINK_LIBRARIES( conv_contour agg::agg )

ADD_EXECUTABLE( conv_dash_marker ${WIN32GUI}
    conv_dash_marker.cpp
)

TARGET_LINK_LIBRARIES( conv_dash_marker agg::agg )

ADD_EXECUTABLE( conv_stroke ${WIN32GUI}
    conv_stroke.cpp
)

TARGET_LINK_LIBRARIES( conv_stroke agg::agg )

ADD_EXECUTABLE( distortions ${WIN32GUI}
    distortions.cpp
)

TARGET_LINK_LIBRARIES( distortions agg::agg )

ADD_EXECUTABLE( flash_rasterizer ${WIN32GUI}
    flash_rasterizer.cpp
)

TARGET_LINK_LIBRARIES( flash_rasterizer agg::agg )

ADD_EXECUTABLE( flash_rasterizer2 ${WIN32GUI}
    flash_rasterizer2.cpp
)

TARGET_LINK_LIBRARIES( flash_rasterizer2 agg::agg )

IF ( agg_USE_FREETYPE )
    ADD_EXECUTABLE( freetype_test ${WIN32GUI}
        freetype_test.cpp
        make_arrows.cpp
        make_gb_poly.cpp
    )

    TARGET_LINK_LIBRARIES( freetype_test agg::agg )

ENDIF ( agg_USE_FREETYPE )

ADD_EXECUTABLE( gamma_correction ${WIN32GUI}
    gamma_correction.cpp
)

TARGET_LINK_LIBRARIES( gamma_correction agg::agg )

ADD_EXECUTABLE( gamma_ctrl ${WIN32GUI}
    gamma_ctrl.cpp
)

TARGET_LINK_LIBRARIES( gamma_ctrl agg::agg )

ADD_EXECUTABLE( gamma_tuner ${WIN32GUI}
    gamma_tuner.cpp
)

TARGET_LINK_LIBRARIES( gamma_tuner agg::agg )

ADD_EXECUTABLE( gouraud ${WIN32GUI}
    gouraud.cpp
)

TARGET_LINK_LIBRARIES( gouraud agg::agg )

ADD_EXECUTABLE( gouraud_mesh ${WIN32GUI}
    gouraud_mesh.cpp
)

TARGET_LINK_LIBRARIES( gouraud_mesh agg::agg )

IF ( agg_USE_GPC )
    ADD_EXECUTABLE( gpc_test ${WIN32GUI}
        gpc_test.cpp
        make_arrows.cpp
        make_gb_poly.cpp
        )

    TARGET_LINK_LIBRARIES( gpc_test agg::agg )

ENDIF ( agg_USE_GPC )

ADD_EXECUTABLE( gradients ${WIN32GUI}
    gradients.cpp
)

TARGET_LINK_LIBRARIES( gradients agg::agg )

ADD_EXECUTABLE( gradient_focal ${WIN32GUI}
    gradient_focal.cpp
)

TARGET_LINK_LIBRARIES( gradient_focal agg::agg )

ADD_EXECUTABLE( gradients_contour ${WIN32GUI}
    gradients_contour.cpp
    make_arrows.cpp
    make_gb_poly.cpp
    parse_lion.cpp
)

TARGET_LINK_LIBRARIES( gradients_contour agg::agg )

ADD_EXECUTABLE( graph_test ${WIN32GUI}
    graph_test.cpp
)

TARGET_LINK_LIBRARIES( graph_test agg::agg )

ADD_EXECUTABLE( idea ${WIN32GUI}
    idea.cpp
)

TARGET_LINK_LIBRARIES( idea agg::agg )

ADD_EXECUTABLE( image1 ${WIN32GUI}
    image1.cpp
)

TARGET_LINK_LIBRARIES( image1 agg::agg )

ADD_EXECUTABLE( image_alpha ${WIN32GUI}
    image_alpha.cpp
)

TARGET_LINK_LIBRARIES( image_alpha agg::agg )

ADD_EXECUTABLE( image_filters ${WIN32GUI}
    image_filters.cpp
)

TARGET_LINK_LIBRARIES( image_filters agg::agg )

ADD_EXECUTABLE( image_filters2 ${WIN32GUI}
    image_filters2.cpp
)

TARGET_LINK_LIBRARIES( image_filters2 agg::agg )

ADD_EXECUTABLE( image_fltr_graph ${WIN32GUI}
    image_fltr_graph.cpp
)

TARGET_LINK_LIBRARIES( image_fltr_graph agg::agg )

ADD_EXECUTABLE( image_perspective ${WIN32GUI}
    image_perspective.cpp
    interactive_polygon.cpp
)

TARGET_LINK_LIBRARIES( image_perspective agg::agg )

ADD_EXECUTABLE( image_resample ${WIN32GUI}
    image_resample.cpp
    interactive_polygon.cpp
)

TARGET_LINK_LIBRARIES( image_resample agg::agg )

ADD_EXECUTABLE( image_transforms ${WIN32GUI}
    image_transforms.cpp
)

TARGET_LINK_LIBRARIES( image_transforms agg::agg )

ADD_EXECUTABLE( line_patterns ${WIN32GUI}
    line_patterns.cpp
)

TARGET_LINK_LIBRARIES( line_patterns agg::agg )

ADD_EXECUTABLE( line_patterns_clip ${WIN32GUI}
    line_patterns_clip.cpp
)

TARGET_LINK_LIBRARIES( line_patterns_clip agg::agg )

ADD_EXECUTABLE( lion ${WIN32GUI}
    lion.cpp
    parse_lion.cpp
)

TARGET_LINK_LIBRARIES( lion agg::agg )

ADD_EXECUTABLE( lion_lens ${WIN32GUI}
    lion_lens.cpp
    parse_lion.cpp
)

TARGET_LINK_LIBRARIES( lion_lens agg::agg )

ADD_EXECUTABLE( lion_outline ${WIN32GUI}
    lion_outline.cpp
    parse_lion.cpp
)

TARGET_LINK_LIBRARIES( lion_outline agg::agg )

ADD_EXECUTABLE( mol_view ${WIN32GUI}
    mol_view.cpp
)

TARGET_LINK_LIBRARIES( mol_view agg::agg )

ADD_EXECUTABLE( multi_clip ${WIN32GUI}
    multi_clip.cpp
    parse_lion.cpp
)

TARGET_LINK_LIBRARIES( multi_clip agg::agg )

ADD_EXECUTABLE( pattern_fill ${WIN32GUI}
    pattern_fill.cpp
)

TARGET_LINK_LIBRARIES( pattern_fill agg::agg )

ADD_EXECUTABLE( pattern_perspective ${WIN32GUI}
    pattern_perspective.cpp
    interactive_polygon.cpp
)

TARGET_LINK_LIBRARIES( pattern_perspective agg::agg )

ADD_EXECUTABLE( pattern_resample ${WIN32GUI}
    pattern_resample.cpp
    interactive_polygon.cpp
)

TARGET_LINK_LIBRARIES( pattern_resample agg::agg )

ADD_EXECUTABLE( perspective ${WIN32GUI}
    perspective.cpp
    interactive_polygon.cpp
    parse_lion.cpp
)

TARGET_LINK_LIBRARIES( perspective agg::agg )

ADD_EXECUTABLE( polymorphic_renderer ${WIN32GUI}
    polymorphic_renderer.cpp
)

TARGET_LINK_LIBRARIES( polymorphic_renderer agg::agg )

ADD_EXECUTABLE( rasterizers ${WIN32GUI}
    rasterizers.cpp
)

TARGET_LINK_LIBRARIES( rasterizers agg::agg )

ADD_EXECUTABLE( rasterizers2 ${WIN32GUI}
    rasterizers2.cpp
)

TARGET_LINK_LIBRARIES( rasterizers2 agg::agg )

ADD_EXECUTABLE( rasterizer_compound ${WIN32GUI}
    rasterizer_compound.cpp
)

TARGET_LINK_LIBRARIES( rasterizer_compound agg::agg )

ADD_EXECUTABLE( raster_text ${WIN32GUI}
    raster_text.cpp
)

TARGET_LINK_LIBRARIES( raster_text agg::agg )

ADD_EXECUTABLE( rounded_rect ${WIN32GUI}
    rounded_rect.cpp
)

TARGET_LINK_LIBRARIES( rounded_rect agg::agg )

ADD_EXECUTABLE( scanline_boolean ${WIN32GUI}
    scanline_boolean.cpp
    interactive_polygon.cpp
)

TARGET_LINK_LIBRARIES( scanline_boolean agg::agg )

ADD_EXECUTABLE( scanline_boolean2 ${WIN32GUI}
    scanline_boolean2.cpp
    make_arrows.cpp
    make_gb_poly.cpp
)

TARGET_LINK_LIBRARIES( scanline_boolean2 agg::agg )

ADD_EXECUTABLE( simple_blur ${WIN32GUI}
    simple_blur.cpp
    parse_lion.cpp
)

TARGET_LINK_LIBRARIES( simple_blur agg::agg )

IF(WIN32)

    ADD_EXECUTABLE( trans_curve1 ${WIN32GUI}
        trans_curve1.cpp
        interactive_polygon.cpp
    )

    TARGET_LINK_LIBRARIES( trans_curve1 agg::agg )

    ADD_EXECUTABLE( trans_curve2 ${WIN32GUI}
        trans_curve2.cpp
        interactive_polygon.cpp
    )

    TARGET_LINK_LIBRARIES( trans_curve2 agg::agg )

    ADD_EXECUTABLE( truetype_test ${WIN32GUI}
        truetype_test.cpp
    )

    TARGET_LINK_LIBRARIES( truetype_test agg::agg )

ENDIF(WIN32)

ADD_EXECUTABLE( trans_polar ${WIN32GUI}
    trans_polar.cpp
)

TARGET_LINK_LIBRARIES( trans_polar agg::agg )

IF ( agg_USE_EXPAT )
    ADD_EXECUTABLE( svg_test ${WIN32GUI}
        ./svg_viewer/svg_test.cpp
        ./svg_viewer/agg_svg_exception.h
        ./svg_viewer/agg_svg_parser.cpp
        ./svg_viewer/agg_svg_parser.h
        ./svg_viewer/agg_svg_path_renderer.cpp
        ./svg_viewer/agg_svg_path_renderer.h
        ./svg_viewer/agg_svg_path_tokenizer.cpp
        ./svg_viewer/agg_svg_path_tokenizer.h
        )

    TARGET_LINK_LIBRARIES( svg_test agg::agg expat::expat )

ENDIF ( agg_USE_EXPAT )

IF(WIN32)
    ADD_EXECUTABLE( pure_api ${WIN32GUI}
        ./win32_api/pure_api/pure_api.h
        ./win32_api/pure_api/pure_api.cpp
        ./win32_api/pure_api/resource.h
        ./win32_api/pure_api/StdAfx.h
        ./win32_api/pure_api/StdAfx.cpp
        ./win32_api/pure_api/pure_api.rc
        parse_lion.cpp
            
    )

    TARGET_LINK_LIBRARIES( pure_api agg::agg )

ENDIF(WIN32)

IF( agg_USE_AGG2D )
    ADD_EXECUTABLE( agg2_demo ${WIN32GUI}
        agg2d_demo.cpp
    )

    TARGET_LINK_LIBRARIES( agg2_demo agg::agg )

ENDIF( agg_USE_AGG2D )
