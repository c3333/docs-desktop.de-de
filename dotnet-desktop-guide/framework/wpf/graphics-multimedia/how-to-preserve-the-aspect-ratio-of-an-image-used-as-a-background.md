---
title: 'Gewusst wie: Beibehalten des Seitenverhältnisses bei einem als Hintergrund verwendeten Bild'
ms.date: 03/30/2017
helpviewer_keywords:
- aspect ratios of background images [WPF], preserving
- brushes [WPF], preserving aspect ratios of background images
- background images [WPF], preserving aspect ratios
ms.assetid: 28c39478-13d7-4011-80a3-8b9cc3e54478
ms.openlocfilehash: b467fcd353994faef19b5a997e03d6582789eac1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975312"
---
# <a name="how-to-preserve-the-aspect-ratio-of-an-image-used-as-a-background"></a>Gewusst wie: Beibehalten des Seitenverhältnisses bei einem als Hintergrund verwendeten Bild
In diesem Beispiel wird gezeigt, wie die-Eigenschaft eines verwendet wird, um <xref:System.Windows.Media.TileBrush.Stretch%2A> <xref:System.Windows.Media.ImageBrush> das Seitenverhältnis des Bilds beizubehalten.  
  
 Wenn Sie einen Bereich mit einem <xref:System.Windows.Media.ImageBrush> zeichnen, wird der Inhalt standardmäßig gestreckt, um den Ausgabebereich vollständig auszufüllen. Wenn der Ausgabebereich und das Bild unterschiedliche Seitenverhältnisse aufweisen, wird das Bild durch dieses Strecken verzerrt.  
  
 Wenn Sie <xref:System.Windows.Media.ImageBrush> das Seitenverhältnis des Bilds beibehalten möchten, legen Sie die- <xref:System.Windows.Media.TileBrush.Stretch%2A> Eigenschaft auf <xref:System.Windows.Media.Stretch.Uniform> oder fest <xref:System.Windows.Media.Stretch.UniformToFill> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden zwei- <xref:System.Windows.Media.ImageBrush> Objekte verwendet, um zwei Rechtecke zu zeichnen. Jedes Rechteck ist 300 x 150 Pixel groß und enthält jeweils ein 300 x 300 Pixel großes Bild. Die <xref:System.Windows.Media.TileBrush.Stretch%2A> -Eigenschaft des ersten Pinsels ist auf festgelegt <xref:System.Windows.Media.Stretch.Uniform> , und die- <xref:System.Windows.Media.TileBrush.Stretch%2A> Eigenschaft des zweiten Pinsels ist auf festgelegt <xref:System.Windows.Media.Stretch.UniformToFill> .  
  
 [!code-csharp[UsingImageBrush_snip#ImageBrushStretchModesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/StretchModes.cs#imagebrushstretchmodesexamplewholepage)]  
  
 Die folgende Abbildung zeigt die Ausgabe des ersten Pinsels mit der <xref:System.Windows.Media.TileBrush.Stretch%2A> Einstellung <xref:System.Windows.Media.Stretch.Uniform> .  
  
 ![ImageBrush mit Uniform-Dehnung](./media/graphicsmm-imagebrushuniformstretch.jpg "graphicsmm_ImageBrushUniformStretch")  
  
 Die nächste Abbildung zeigt die Ausgabe des zweiten Pinsels mit der <xref:System.Windows.Media.TileBrush.Stretch%2A> Einstellung <xref:System.Windows.Media.Stretch.UniformToFill> .  
  
 ![ImageBrush mit UniformToFill-Dehnung](./media/graphicsmm-imagebrushuniformtofillstretch.jpg "graphicsmm_ImageBrushUniformToFillStretch")  
  
 Beachten Sie, dass sich die <xref:System.Windows.Media.TileBrush.Stretch%2A> -Eigenschaft identisch mit den anderen <xref:System.Windows.Media.TileBrush> -Objekten verhält, <xref:System.Windows.Media.DrawingBrush> d <xref:System.Windows.Media.VisualBrush> . h. für und. Weitere Informationen zu <xref:System.Windows.Media.ImageBrush> und anderen <xref:System.Windows.Media.TileBrush> Objekten finden Sie unterzeichnen [mit Bildern, Zeichnungen und visuellen](painting-with-images-drawings-and-visuals.md)Elementen.  
  
 Beachten Sie auch, dass die-Eigenschaft, obwohl die- <xref:System.Windows.Media.TileBrush.Stretch%2A> Eigenschaft anscheinend angibt, wie der <xref:System.Windows.Media.TileBrush> Inhalt an den Ausgabebereich angepasst wird, tatsächlich angibt, wie der Inhalt gestreckt wird, um die zugehörige <xref:System.Windows.Media.TileBrush> Basis Kachel auszufüllen. Weitere Informationen finden Sie unter <xref:System.Windows.Media.TileBrush>.  
  
 Dieses Codebeispiel ist Teil eines größeren Beispiels, das für die-Klasse bereitgestellt wird <xref:System.Windows.Media.ImageBrush> . Das komplette Beispiel finden Sie unter [ImageBrush Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ImageBrush).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.TileBrush>
- [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](painting-with-images-drawings-and-visuals.md)
