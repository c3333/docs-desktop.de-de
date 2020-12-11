---
title: Übersicht über Pinseltransformationen
ms.date: 03/30/2017
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- brushes [WPF], transformation properties
- properties [WPF], transformation
- transformation properties of brushes [WPF]
ms.assetid: 8b9bfc09-12fd-4cd5-b445-99949f27bc39
ms.openlocfilehash: 7616e1620c0bd342e3c8bb776e8d72c038bd3cc6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976902"
---
# <a name="brush-transformation-overview"></a>Übersicht über Pinseltransformationen
Die Brush-Klasse stellt zwei Transformations Eigenschaften bereit: <xref:System.Windows.Media.Brush.Transform%2A> und <xref:System.Windows.Media.Brush.RelativeTransform%2A> . Diese Eigenschaften ermöglichen Ihnen den Inhalt eines Pinsels zu drehen, zu skalieren, zu neigen und zu übersetzen. Dieses Thema beschreibt die  Unterschiede zwischen diesen beiden Eigenschaften sowie Beispiele für deren Verwendung.  
  
<a name="prerequisites"></a>
## <a name="prerequisites"></a>Voraussetzungen  
 Um dieses Thema zu verstehen, sollten Sie die Features des Pinsels kennen, den Sie transformieren. Informationen zu <xref:System.Windows.Media.LinearGradientBrush> und <xref:System.Windows.Media.RadialGradientBrush> finden Sie unter [Übersicht über das Zeichnen mit voll Tonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md). Informationen zu, oder finden Sie unterzeichnen <xref:System.Windows.Media.ImageBrush> <xref:System.Windows.Media.DrawingBrush> <xref:System.Windows.Media.VisualBrush>  [mit Bildern, Zeichnungen und visuellen](painting-with-images-drawings-and-visuals.md)Elementen. Sie sollten auch mit den 2D- Transformationen, die unter  [Übersicht über Transformationen](transforms-overview.md) beschrieben werden, vertraut sein.  
  
<a name="transformversusrelativetransform"></a>
## <a name="differences-between-the-transform-and-relativetransform-properties"></a>Unterschiede zwischen den Eigenschaften Transform und RelativeTransform  
 Wenn Sie eine Transformation auf die-Eigenschaft eines Pinsels anwenden <xref:System.Windows.Media.Brush.Transform%2A> , müssen Sie die Größe des gezeichneten Bereichs kennen, wenn Sie den Pinsel Inhalt über seinen Mittelpunkt transformieren möchten. Angenommen, der gezeichnete Bereich ist 200 geräteunabhängige Pixel breit und 150 hoch.  Wenn Sie einen verwendet <xref:System.Windows.Media.RotateTransform> haben, um die Ausgabe des Pinsels um 45 Grad um seinen Mittelpunkt zu drehen, geben Sie das <xref:System.Windows.Media.RotateTransform> a <xref:System.Windows.Media.RotateTransform.CenterX%2A> von 100 und einen <xref:System.Windows.Media.RotateTransform.CenterY%2A> von 75 an.  
  
 Wenn Sie eine Transformation auf die-Eigenschaft eines Pinsels anwenden <xref:System.Windows.Media.Brush.RelativeTransform%2A> , wird diese Transformation auf den Pinsel angewendet, bevor die Ausgabe dem gezeichneten Bereich zugeordnet wird. Die folgende Liste beschreibt die Reihenfolge, in welcher der Inhalt eines Pinsels verarbeitet und transformiert wird.  
  
1. Verarbeiten Sie den Inhalt des Pinsels. Bei einem <xref:System.Windows.Media.GradientBrush> bedeutet dies, dass der Farbverlaufs Bereich bestimmt wird. Bei einem <xref:System.Windows.Media.TileBrush> wird der <xref:System.Windows.Media.TileBrush.Viewbox%2A> zugeordnet <xref:System.Windows.Media.TileBrush.Viewport%2A> . Dies ergibt die Ausgabe des Pinsels.  
  
2. Projizieren Sie die Ausgabe des Pinsels auf das 1 x 1-Transformationsrechteck.  
  
3. Wenden Sie den Pinsel an <xref:System.Windows.Media.Brush.RelativeTransform%2A> , wenn dieser über einen verfügt.  
  
4. Projizieren Sie die transformierte Ausgabe auf den zu zeichnenden Bereich.  
  
5. Wenden Sie den Pinsel an <xref:System.Windows.Media.Transform> , wenn dieser über einen verfügt.  
  
 Da der <xref:System.Windows.Media.Brush.RelativeTransform%2A> angewendet wird, während die Ausgabe des Pinsels einem 1 x 1-Rechteck zugeordnet ist, scheinen die Werte für Transform Center und Offset relativ zu sein. Wenn Sie z. b. einen <xref:System.Windows.Media.RotateTransform> zum Drehen der Ausgabe des Pinsels von 45 Grad um den Mittelpunkt verwendet haben, geben Sie das <xref:System.Windows.Media.RotateTransform> a <xref:System.Windows.Media.RotateTransform.CenterX%2A> von 0,5 und einen <xref:System.Windows.Media.RotateTransform.CenterY%2A> von 0,5 an.  
  
 Die folgende Abbildung zeigt die Ausgabe mehrerer Pinsel, die um 45 Grad gedreht wurden, mithilfe der <xref:System.Windows.Media.Brush.RelativeTransform%2A> -Eigenschaft und der-Eigenschaft <xref:System.Windows.Media.Brush.Transform%2A> .  
  
 ![RelativeTransform- und Transformieren-Eigenschaften](./media/graphicsmm-brushrelativetransform-transform-small.png "graphicsmm_brushrelativetransform_transform_small")  
  
<a name="relativetransformandtilebrush"></a>
## <a name="using-relativetransform-with-a-tilebrush"></a>Verwenden von RelativeTransform mit einem TileBrush-Objekt  
 Da Kachel Pinsel komplexer als andere Pinsel sind, kann das Anwenden einer <xref:System.Windows.Media.Brush.RelativeTransform%2A> auf eine unerwartete Ergebnisse verursachen. Ziehen Sie z.B. die folgende Abbildung heran.  
  
 ![Das Quellbild](./media/graphicsmm-reltransform-1-original-image.jpg "graphicsmm_reltransform_1_original_image")  
  
 Im folgenden Beispiel wird verwendet <xref:System.Windows.Media.ImageBrush> , um einen rechteckigen Bereich mit dem vorangehenden Bild zu zeichnen. Es wendet einen <xref:System.Windows.Media.RotateTransform> auf die <xref:System.Windows.Media.ImageBrush> -Eigenschaft des-Objekts an <xref:System.Windows.Media.Brush.RelativeTransform%2A> und legt seine- <xref:System.Windows.Media.TileBrush.Stretch%2A> Eigenschaft auf fest <xref:System.Windows.Media.Stretch.UniformToFill> . dabei sollte das Seitenverhältnis des Bilds beibehalten werden, wenn es gestreckt wird, um das Rechteck vollständig auszufüllen.  
  
 [!code-xaml[BrushOverviewExamples_snip#GraphicsMMRelativeTransformExample2Inline](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/RelativeTransformIllustration.xaml#graphicsmmrelativetransformexample2inline)]  
  
 Dieses Beispiel erzeugt die folgende Ausgabe:  
  
 ![Die transformierte Ausgabe](./media/graphicsmm-reltransform-6-output.png "graphicsmm_reltransform_6_output")  
  
 Beachten Sie, dass das Bild verzerrt ist, obwohl der Pinsel <xref:System.Windows.Media.TileBrush.Stretch%2A> auf festgelegt wurde <xref:System.Windows.Media.Stretch.UniformToFill> . Das liegt daran, dass die relative Transformation angewendet wird, nachdem der Pinsel der zugeordnet wurde <xref:System.Windows.Media.TileBrush.Viewbox%2A> <xref:System.Windows.Media.TileBrush.Viewport%2A> . In der folgenden Liste werden die einzelnen Schritte des Prozesses beschrieben:  
  
1. Projizieren Sie den Inhalt des Pinsels ( <xref:System.Windows.Media.TileBrush.Viewbox%2A> ) <xref:System.Windows.Media.TileBrush.Viewport%2A> mithilfe der Pinsel Einstellung auf seine Basis Kachel () <xref:System.Windows.Media.TileBrush.Stretch%2A> .  
  
     ![Dehnen Sie die Viewbox, um den Viewport einzupassen](./media/graphicsmm-reltransform-2-viewbox-to-viewport.png "graphicsmm_reltransform_2_viewbox_to_viewport")  
  
2. Projizieren Sie die Basiskachel auf das 1 x 1-Transformationsrechteck.  
  
     ![Ordnen Sie den Viewport dem Transformationsrechteck zu](./media/graphicsmm-reltransform-3-output-to-transform.png "graphicsmm_reltransform_3_output_to_transform")  
  
3. Anwenden von <xref:System.Windows.Media.RotateTransform> .  
  
     ![Wenden Sie die relative Transformation an](./media/graphicsmm-reltransform-4-transform-rotate.png "graphicsmm_reltransform_4_transform_rotate")  
  
4. Projizieren Sie die transformierte Basiskachel auf den zu zeichnenden Bereich.  
  
     ![Projizieren Sie den transformierten Pinsel auf den Ausgabebereich](./media/graphicsmm-reltransform-5-transform-to-output.png "graphicsmm_reltransform_5_transform_to_output")  
  
<a name="rotateexample"></a>
## <a name="example-rotate-an-imagebrush-45-degrees"></a>Beispiel: Drehen eines ImageBrush um 45 Grad  
 Im folgenden Beispiel wird ein <xref:System.Windows.Media.RotateTransform> auf die- <xref:System.Windows.Media.Brush.RelativeTransform%2A> Eigenschaft eines angewendet <xref:System.Windows.Media.ImageBrush> . Die-Eigenschaft und die-Eigenschaft des- <xref:System.Windows.Media.RotateTransform> Objekts <xref:System.Windows.Media.RotateTransform.CenterX%2A> <xref:System.Windows.Media.RotateTransform.CenterY%2A> sind auf 0,5 und die relativen Koordinaten des Mittelpunkts des Inhalts festgelegt. Als Folge, wird der Inhalt des Pinsels wird um seinen Mittelpunkt gedreht.  
  
 [!code-csharp[BrushesIntroduction_snip#ImageBrushRelativeTransformExample](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/BrushTransformExample.cs#imagebrushrelativetransformexample)]
 [!code-vb[BrushesIntroduction_snip#ImageBrushRelativeTransformExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/brushtransformexample.vb#imagebrushrelativetransformexample)]
 [!code-xaml[BrushesIntroduction_snip#ImageBrushRelativeTransformExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/BrushTransformExample.xaml#imagebrushrelativetransformexample)]  
  
 Im nächsten Beispiel wird auch ein <xref:System.Windows.Media.RotateTransform> auf eine angewendet <xref:System.Windows.Media.ImageBrush> , aber die- <xref:System.Windows.Media.Brush.Transform%2A> Eigenschaft anstelle der- <xref:System.Windows.Media.Brush.RelativeTransform%2A> Eigenschaft verwendet. Um den Pinsel um seinen Mittelpunkt zu drehen, <xref:System.Windows.Media.RotateTransform> muss das-Objekt und das-Objekt <xref:System.Windows.Media.RotateTransform.CenterX%2A> <xref:System.Windows.Media.RotateTransform.CenterY%2A> auf absolute Koordinaten festgelegt werden. Da das vom Pinsel gezeichnete Rechteck 175 mal 90 Pixel beträgt, liegt sein Mittelpunkt bei (87,5, 45).  
  
 [!code-csharp[BrushesIntroduction_snip#ImageBrushTransformExample](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/BrushTransformExample.cs#imagebrushtransformexample)]
 [!code-vb[BrushesIntroduction_snip#ImageBrushTransformExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/brushtransformexample.vb#imagebrushtransformexample)]
 [!code-xaml[BrushesIntroduction_snip#ImageBrushTransformExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/BrushTransformExample.xaml#imagebrushtransformexample)]  
  
 Die folgende Abbildung zeigt den Pinsel ohne Transformation, wobei die Transformation auf die <xref:System.Windows.Media.Brush.RelativeTransform%2A> -Eigenschaft angewendet wird und die Transformation auf die-Eigenschaft angewendet wird <xref:System.Windows.Media.Brush.Transform%2A> .  
  
 ![RelativeTransform- und Transform-Pinseleinstellungen](./media/wcpsdk-graphicsmm-transformandrelativetransform.png "wcpsdk_graphicsmm_transformandrelativetransform")  
  
 Dieses Beispiel ist Teil eines umfangreicheren Beispiels. Das vollständige Beispiel finden Sie unter der [Beispiel für Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes). Weitere Informationen zu Pinseln, finden Sie unter der [Übersicht über WPF-Pinsel](wpf-brushes-overview.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Brush.Transform%2A>
- <xref:System.Windows.Media.Brush.RelativeTransform%2A>
- <xref:System.Windows.Media.Transform>
- <xref:System.Windows.Media.Brush>
- [Übersicht über das Zeichnen mit Volltonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md)
- [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](painting-with-images-drawings-and-visuals.md)
- [Übersicht über Transformationen](transforms-overview.md)
