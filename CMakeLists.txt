set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(qcustomplot STATIC
    src/colorgradient.h src/colorgradient.cpp
    src/core.h src/core.cpp
    src/global.h
    src/item.h src/item.cpp
    src/layer.h src/layer.cpp
    src/layout.h src/layout.cpp
    src/lineending.h src/lineending.cpp
    src/paintbuffer.h src/paintbuffer.cpp
    src/painter.h src/painter.cpp
    src/plottable.h src/plottable.cpp
    src/scatterstyle.h src/scatterstyle.cpp
    src/selection.h src/selection.cpp
    src/selectiondecorator-bracket.h src/selectiondecorator-bracket.cpp
    src/selectionrect.h src/selectionrect.cpp
    src/vector2d.h src/vector2d.cpp

    src/axis/axis.h src/axis/axis.cpp
    src/axis/axisticker.h src/axis/axisticker.cpp
    src/axis/axistickerdatetime.h src/axis/axistickerdatetime.cpp
    src/axis/axistickerfixed.h src/axis/axistickerfixed.cpp
    src/axis/axistickerlog.h src/axis/axistickerlog.cpp
    src/axis/axistickerpi.h src/axis/axistickerpi.cpp
    src/axis/axistickertext.h src/axis/axistickertext.cpp
    src/axis/axistickertime.h src/axis/axistickertime.cpp
    src/axis/labelpainter.h src/axis/labelpainter.cpp
    src/axis/range.h src/axis/range.cpp

    src/items/item-bracket.h src/items/item-bracket.cpp
    src/items/item-curve.h src/items/item-curve.cpp
    src/items/item-ellipse.h src/items/item-ellipse.cpp
    src/items/item-line.h src/items/item-line.cpp
    src/items/item-pixmap.h src/items/item-pixmap.cpp
    src/items/item-rect.h src/items/item-rect.cpp
    src/items/item-straightline.h src/items/item-straightline.cpp
    src/items/item-text.h src/items/item-text.cpp
    src/items/item-tracer.h src/items/item-tracer.cpp

    src/layoutelements/layoutelement-axisrect.h src/layoutelements/layoutelement-axisrect.cpp
    src/layoutelements/layoutelement-colorscale.h src/layoutelements/layoutelement-colorscale.cpp
    src/layoutelements/layoutelement-legend.h src/layoutelements/layoutelement-legend.cpp
    src/layoutelements/layoutelement-textelement.h src/layoutelements/layoutelement-textelement.cpp

    src/plottables/plottable-bars.h src/plottables/plottable-bars.cpp
    src/plottables/plottable-colormap.h src/plottables/plottable-colormap.cpp
    src/plottables/plottable-curve.h src/plottables/plottable-curve.cpp
    src/plottables/plottable-errorbar.h src/plottables/plottable-errorbar.cpp
    src/plottables/plottable-financial.h src/plottables/plottable-financial.cpp
    src/plottables/plottable-graph.h src/plottables/plottable-graph.cpp
    src/plottables/plottable-statisticalbox.h src/plottables/plottable-statisticalbox.cpp

    src/polar/layoutelement-angularaxis.h src/polar/layoutelement-angularaxis.cpp
    src/polar/polargraph.h src/polar/polargraph.cpp
    src/polar/polargrid.h src/polar/polargrid.cpp
    src/polar/radialaxis.h src/polar/radialaxis.cpp
)

target_link_libraries(qcustomplot PRIVATE
    Qt::Widgets
    Qt::PrintSupport
)

target_include_directories(qcustomplot PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/src
)

target_include_directories(qcustomplot INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}/..
)
