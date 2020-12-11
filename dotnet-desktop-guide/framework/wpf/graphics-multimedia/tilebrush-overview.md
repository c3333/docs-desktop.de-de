---
title: Übersicht über TileBrush
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TileBrush [WPF]
- brushes [WPF], TileBrush
ms.assetid: aa4a7b7e-d09d-44c2-8d61-310c50e08d68
ms.openlocfilehash: 99bcc8695206030a381d71df2dda495867d3e9c7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976840"
---
# <a name="tilebrush-overview"></a>Übersicht über TileBrush
<xref:System.Windows.Media.TileBrush> -Objekte bieten Ihnen sehr viel Kontrolle über die Art und Weise, wie ein Bereich mit einem Bild, oder gezeichnet wird <xref:System.Windows.Media.Drawing> <xref:System.Windows.Media.Visual> . In diesem Thema wird beschrieben, wie Sie mithilfe <xref:System.Windows.Media.TileBrush> von-Funktionen mehr Kontrolle darüber erhalten, wie ein <xref:System.Windows.Media.ImageBrush> , <xref:System.Windows.Media.DrawingBrush> oder <xref:System.Windows.Media.VisualBrush> einen Bereich zeichnet.  

<a name="prerequisite"></a>
## <a name="prerequisites"></a>Voraussetzungen  
 Um dieses Thema zu verstehen, ist es hilfreich zu verstehen, wie die grundlegenden Funktionen der-,-oder-Klasse verwendet werden <xref:System.Windows.Media.ImageBrush> <xref:System.Windows.Media.DrawingBrush> <xref:System.Windows.Media.VisualBrush> . Eine Einführung zu diesen Typen finden Sie unterzeichnen [mit Bildern, Zeichnungen und visuellen](painting-with-images-drawings-and-visuals.md)Elementen.  
  
<a name="tilebrush"></a>
## <a name="painting-an-area-with-tiles"></a>Zeichnen eines Bereichs mit Kacheln  
 <xref:System.Windows.Media.ImageBrush>, <xref:System.Windows.Media.DrawingBrush> , sind <xref:System.Windows.Media.VisualBrush> Typen von- <xref:System.Windows.Media.TileBrush> Objekten. Kacheleffekte bieten Ihnen gute Steuerungsmöglichkeiten für das Malen eines Bilds, einer Zeichnung oder eines visuellen Objekts in einem Bereich. Sie können beispielsweise zum Zeichnen eines Bereichs anstelle eines einzelnen gestreckten Bilds eine Reihe von Bildkacheln verwenden, die ein Muster ergeben.  
  
 Beim Zeichnen eines Bereichs mit einem Kacheleffekt spielen drei Komponenten eine Rolle: Inhalt, Basiskachel und Ausgabebereich.  
  
 ![TileBrush-Komponenten](./media/wcpsdk-mmgraphics-defaultcontentprojection2.png "wcpsdk_mmgraphics_defaultcontentprojection2")  
Komponenten eines TileBrush mit einer einzelnen Kachel  
  
 ![Komponenten eines gekachelten TileBrush-Elements](./media/graphicsmm-tiledprojection.png "graphicsmm_tiledprojection")  
Komponenten eines TileBrush mit einer TileMode-Kachel  
  
 Der Ausgabebereich ist der Bereich, der gezeichnet wird, z <xref:System.Windows.Shapes.Shape.Fill%2A> . b <xref:System.Windows.Shapes.Ellipse> . der eines oder eines <xref:System.Windows.Controls.Control.Background%2A> <xref:System.Windows.Controls.Button> . In den nächsten Abschnitten werden die anderen beiden Komponenten von beschrieben <xref:System.Windows.Media.TileBrush> .  
  
<a name="brushcontent"></a>
## <a name="brush-content"></a>Pinselinhalt  
 Es gibt drei verschiedene Typen von <xref:System.Windows.Media.TileBrush> und jeder Paint mit einem anderen Inhaltstyp.  
  
- Wenn der Pinsel ein ist <xref:System.Windows.Media.ImageBrush> , handelt es sich bei diesem Inhalt um ein Bild, bei dem die- <xref:System.Windows.Media.ImageBrush.ImageSource%2A> Eigenschaft den Inhalt der angibt <xref:System.Windows.Media.ImageBrush> .  
  
- Wenn der Pinsel eine ist <xref:System.Windows.Media.DrawingBrush> , ist dieser Inhalt eine Zeichnung. Die- <xref:System.Windows.Media.DrawingBrush.Drawing%2A> Eigenschaft gibt den Inhalt des an <xref:System.Windows.Media.DrawingBrush> .  
  
- Wenn der Pinsel ein ist <xref:System.Windows.Media.VisualBrush> , ist dieser Inhalt ein visuelles Element. Die- <xref:System.Windows.Media.VisualBrush.Visual%2A> Eigenschaft gibt den Inhalt des an <xref:System.Windows.Media.VisualBrush> .  
  
 Sie können die Position und die Dimensionen des <xref:System.Windows.Media.TileBrush> Inhalts mithilfe der- <xref:System.Windows.Media.TileBrush.Viewbox%2A> Eigenschaft angeben, obwohl es üblich ist, den <xref:System.Windows.Media.TileBrush.Viewbox%2A> Standardwert von festgelegt zu lassen. Standardmäßig <xref:System.Windows.Media.TileBrush.Viewbox%2A> ist so konfiguriert, dass der Inhalt des Pinsels vollständig enthalten ist. Weitere Informationen zum Konfigurieren von finden Sie auf <xref:System.Windows.Controls.Viewbox> der <xref:System.Windows.Controls.Viewbox> Eigenschaften Seite.  
  
<a name="thebasetile"></a>
## <a name="the-base-tile"></a>Basiskachel  
 Ein <xref:System.Windows.Media.TileBrush> projiziert seinen Inhalt auf eine Basis Kachel. Die- <xref:System.Windows.Media.TileBrush.Stretch%2A> Eigenschaft steuert <xref:System.Windows.Media.TileBrush> , wie Inhalt gestreckt wird, um die Basis Kachel auszufüllen. Die- <xref:System.Windows.Media.TileBrush.Stretch%2A> Eigenschaft akzeptiert die folgenden Werte, die durch die- <xref:System.Windows.Media.Stretch> Enumeration definiert werden:  
  
- <xref:System.Windows.Media.Stretch.None>: Der Inhalt des Pinsels wird nicht gestreckt, um die Kachel auszufüllen.  
  
- <xref:System.Windows.Media.Stretch.Fill>: Der Inhalt des Pinsels wird so skaliert, dass er der Kachel entspricht. Da Höhe und Breite des Inhalts unabhängig voneinander skaliert werden, wird das ursprüngliche Seitenverhältnis des Inhalts möglicherweise nicht beibehalten. Der Inhalt des Pinsels wird möglicherweise verzerrt, um die Ausgabekachel vollständig auszufüllen.  
  
- <xref:System.Windows.Media.Stretch.Uniform>: Der Inhalt des Pinsels wird so skaliert, dass er vollständig innerhalb der Kachel passt. Das Seitenverhältnis des Inhalts wird beibehalten.  
  
- <xref:System.Windows.Media.Stretch.UniformToFill>: Der Inhalt des Pinsels wird so skaliert, dass er den Ausgabebereich vollständig ausfüllt, während das ursprüngliche Seitenverhältnis des Inhalts beibehalten wird.  
  
 In der folgenden Abbildung werden die verschiedenen <xref:System.Windows.Media.TileBrush.Stretch%2A> Einstellungen veranschaulicht.  
  
 ![Unterschiedliche TileBrush-Dehneinstellungen](./media/img-mmgraphics-stretchenum.jpg "img_mmgraphics_stretchenum")  
  
 Im folgenden Beispiel wird der Inhalt eines <xref:System.Windows.Media.ImageBrush> so festgelegt, dass er nicht gestreckt wird, um den Ausgabebereich auszufüllen.  
  
 [!code-xaml[BrushOverviewExamples_snip#GraphicsMMNoStretchExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/StretchExample.xaml#graphicsmmnostretchexample)]  
  
 [!code-csharp[BrushOverviewExamples_procedural_snip#GraphicsMMNoStretchExample](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/CSharp/StretchExample.cs#graphicsmmnostretchexample)]
 [!code-vb[BrushOverviewExamples_procedural_snip#GraphicsMMNoStretchExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/visualbasic/stretchexample.vb#graphicsmmnostretchexample)]  
  
 Standardmäßig generiert eine <xref:System.Windows.Media.TileBrush> einzelne Kachel (die Basis Kachel) und dehnt diese Kachel aus, um den Ausgabebereich vollständig auszufüllen. Sie können die Größe und Position der Basis Kachel ändern, indem Sie die <xref:System.Windows.Media.TileBrush.Viewport%2A> -Eigenschaft und die-Eigenschaft festlegen <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> .  
  
<a name="basetilesize"></a>
### <a name="base-tile-size"></a>Größe der Basiskachel  
 Die <xref:System.Windows.Media.TileBrush.Viewport%2A> -Eigenschaft bestimmt die Größe und Position der Basis Kachel, und die- <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> Eigenschaft bestimmt, ob der <xref:System.Windows.Media.TileBrush.Viewport%2A> mithilfe absoluter oder relativer Koordinaten angegeben wird. Wenn die Koordinaten relativ sind, sind sie relativ zur Größe des Ausgabebereichs. Der Punkt (0,0) stellt die obere linke Ecke des Ausgabebereichs und (1,1) stellt die untere rechte Ecke des Ausgabebereichs dar. Legen Sie die-Eigenschaft auf fest, um anzugeben, dass die- <xref:System.Windows.Media.TileBrush.Viewport%2A> Eigenschaft absolute Koordinaten verwendet <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> <xref:System.Windows.Media.BrushMappingMode.Absolute> .  
  
 In der folgenden Abbildung wird der Unterschied in der Ausgabe zwischen einem-Paar <xref:System.Windows.Media.TileBrush> und relativer und absoluter Darstellung veranschaulicht <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> . Beachten Sie, dass in den Abbildungen ein Kachelmuster angezeigt wird. Im nächsten Abschnitt wird beschrieben, wie Kachelmuster angegeben werden.  
  
 ![Absolute und relative Viewport-Einheiten](./media/absolute-and-relative-viewports.png "absolute_and_relative_viewports")  
  
 Im folgenden Beispiel wird ein Bild verwendet, um eine Kachel zu erstellen, deren Breite und Höhe 50% ist. Die Basiskachel befindet sich bei (0,0) des Ausgabebereichs.  
  
 [!code-xaml[BrushOverviewExamples_snip#GraphicsMMRelativeViewportUnitsExample1](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TileSizeExample.xaml#graphicsmmrelativeviewportunitsexample1)]  
  
 [!code-csharp[BrushOverviewExamples_procedural_snip#GraphicsMMRelativeViewportUnitsExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/CSharp/TileSizeExample.cs#graphicsmmrelativeviewportunitsexample1)]
 [!code-vb[BrushOverviewExamples_procedural_snip#GraphicsMMRelativeViewportUnitsExample1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/visualbasic/tilesizeexample.vb#graphicsmmrelativeviewportunitsexample1)]  
  
 Im nächsten Beispiel werden die Kacheln eines <xref:System.Windows.Media.ImageBrush> auf 25 geräteunabhängige Pixel festgelegt. Da <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> absolut ist, sind die <xref:System.Windows.Media.ImageBrush> Kacheln immer 25 x 25 Pixel, unabhängig von der Größe des gezeichneten Bereichs.  
  
 [!code-xaml[BrushOverviewExamples_snip#GraphicsMMAbsoluteViewportUnitsExample1](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TileSizeExample.xaml#graphicsmmabsoluteviewportunitsexample1)]  
  
 [!code-csharp[BrushOverviewExamples_procedural_snip#GraphicsMMAbsoluteViewportUnitsExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/CSharp/TileSizeExample.cs#graphicsmmabsoluteviewportunitsexample1)]
 [!code-vb[BrushOverviewExamples_procedural_snip#GraphicsMMAbsoluteViewportUnitsExample1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/visualbasic/tilesizeexample.vb#graphicsmmabsoluteviewportunitsexample1)]  
  
<a name="tilingbehavior"></a>
### <a name="tiling-behavior"></a>Kachelverhalten  
 Ein <xref:System.Windows.Media.TileBrush> erzeugt ein gekacheltes Muster, wenn die Basis Kachel den Ausgabebereich nicht vollständig ausgefüllt und ein anderer tichmodus <xref:System.Windows.Media.TileMode.None> angegeben wird. Wenn die Kachel eines Kachel Pinsels den Ausgabebereich nicht vollständig ausgefüllt hat, gibt die- <xref:System.Windows.Media.TileBrush.TileMode%2A> Eigenschaft an, ob die Basis Kachel dupliziert werden soll, um den Ausgabebereich auszufüllen, und wenn dies der Fall ist, wie die Basis Kachel dupliziert werden soll. Die- <xref:System.Windows.Media.TileBrush.TileMode%2A> Eigenschaft akzeptiert die folgenden Werte, die durch die- <xref:System.Windows.Media.TileMode> Enumeration definiert werden:  
  
- <xref:System.Windows.Media.TileMode.None>: Nur die Basis Kachel wird gezeichnet.  
  
- <xref:System.Windows.Media.TileMode.Tile>: Die Basis Kachel wird gezeichnet, und der verbleibende Bereich wird durch Wiederholen der Basis Kachel aufgefüllt, sodass der Rechte Rand einer Kachel an den linken Rand der nächsten Kachel und auf ähnliche Weise am unteren und oberen Rand liegt.  
  
- <xref:System.Windows.Media.TileMode.FlipX>: Identisch <xref:System.Windows.Media.TileMode.Tile> mit, aber alternative Spalten von Kacheln werden horizontal gekippt.  
  
- <xref:System.Windows.Media.TileMode.FlipY>: Identisch <xref:System.Windows.Media.TileMode.Tile> mit, aber alternative Zeilen von Kacheln werden vertikal gekippt.  
  
- <xref:System.Windows.Media.TileMode.FlipXY>: Eine Kombination aus <xref:System.Windows.Media.TileMode.FlipX> und <xref:System.Windows.Media.TileMode.FlipY> .  
  
 Die folgende Abbildung zeigt die unterschiedlichen Kachelmodi.  
  
 ![Unterschiedliche TileBrush-TileMode-Einstellungen](./media/img-mmgraphics-tilemodes.gif "img_mmgraphics_tilemodes")  
  
 Im folgenden Beispiel wird ein Bild verwendet, um ein Rechteck zu zeichnen, das 100 Pixel breit und 100 Pixel hoch ist. Wenn der Pinsel <xref:System.Windows.Media.TileBrush.Viewport%2A> auf 0, 0, 0,25, 0,25 festgelegt wurde, wird die Basis Kachel des Pinsels auf 1/4 des Ausgabe Bereichs festgelegt. Der Pinsel <xref:System.Windows.Media.TileBrush.TileMode%2A> ist auf festgelegt <xref:System.Windows.Media.TileMode.FlipXY> . sodass er das Rechteck mit Kachelreihen ausfüllt.  
  
 [!code-xaml[BrushOverviewExamples_snip#GraphicsMMFlipXYExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TilingExample.xaml#graphicsmmflipxyexample)]  
  
 [!code-csharp[BrushOverviewExamples_procedural_snip#GraphicsMMFlipXYExample](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/CSharp/TilingExample.cs#graphicsmmflipxyexample)]
 [!code-vb[BrushOverviewExamples_procedural_snip#GraphicsMMFlipXYExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/visualbasic/tilingexample.vb#graphicsmmflipxyexample)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.ImageBrush>
- <xref:System.Windows.Media.DrawingBrush>
- <xref:System.Windows.Media.VisualBrush>
- <xref:System.Windows.Media.TileBrush>
- [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](painting-with-images-drawings-and-visuals.md)
- [Artikel zu Vorgehensweisen](brushes-how-to-topics.md)
- [Übersicht über Freezable-Objekte](../advanced/freezable-objects-overview.md)
- [Beispiel zu ImageBrush](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ImageBrush)
- [VisualBrush-Beispiel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/VisualBrush)
