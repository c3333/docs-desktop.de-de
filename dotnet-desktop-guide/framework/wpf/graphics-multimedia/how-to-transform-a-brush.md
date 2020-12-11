---
title: 'Gewusst wie: Transformieren eines Pinsels'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- brushes [WPF], rotating contents
- brushes [WPF], Transform property
- rotating contents of brushes [WPF]
ms.assetid: ebada2f9-f01f-4863-9ea2-c2e4e51610f1
ms.openlocfilehash: b4484e2fc1ae3e969b02b1d8f3ae4ab2a035558e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976862"
---
# <a name="how-to-transform-a-brush"></a>Gewusst wie: Transformieren eines Pinsels
Dieses Beispiel zeigt, wie <xref:System.Windows.Media.Brush> Sie-Objekte mithilfe ihrer beiden Transformations Eigenschaften transformieren können: <xref:System.Windows.Media.Brush.RelativeTransform%2A> und <xref:System.Windows.Media.Brush.Transform%2A> .  
  
 In den folgenden Beispielen wird ein verwendet <xref:System.Windows.Media.RotateTransform> , um den Inhalt von <xref:System.Windows.Media.ImageBrush> um um 45 Grad zu drehen.  
  
 In der folgenden Abbildung wird der <xref:System.Windows.Media.ImageBrush> ohne einen dargestellt <xref:System.Windows.Media.RotateTransform> , wobei <xref:System.Windows.Media.RotateTransform> auf die <xref:System.Windows.Media.Brush.RelativeTransform%2A> -Eigenschaft angewendet wird und der <xref:System.Windows.Media.RotateTransform> auf die-Eigenschaft angewendet wird <xref:System.Windows.Media.Brush.Transform%2A> .  
  
 ![RelativeTransform- und Transform-Pinseleinstellungen](./media/wcpsdk-graphicsmm-transformandrelativetransform.png "wcpsdk_graphicsmm_transformandrelativetransform")  
  
## <a name="example"></a>Beispiel  
 Im ersten Beispiel wird ein <xref:System.Windows.Media.RotateTransform> auf die- <xref:System.Windows.Media.Brush.RelativeTransform%2A> Eigenschaft eines-Objekts angewendet <xref:System.Windows.Media.ImageBrush> . Die <xref:System.Windows.Media.RotateTransform.CenterX%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.RotateTransform.CenterY%2A> eines- <xref:System.Windows.Media.RotateTransform> Objekts sind auf 0,5 festgelegt. Dies ist die relative Koordinate des Mittelpunkts dieses Inhalts. Folglich dreht sich der <xref:System.Windows.Media.ImageBrush> Inhalt um seinen Mittelpunkt.  
  
 [!code-csharp[BrushesIntroduction_snip#ImageBrushRelativeTransformExample](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/BrushTransformExample.cs#imagebrushrelativetransformexample)]
 [!code-vb[BrushesIntroduction_snip#ImageBrushRelativeTransformExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/brushtransformexample.vb#imagebrushrelativetransformexample)]
 [!code-xaml[BrushesIntroduction_snip#ImageBrushRelativeTransformExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/BrushTransformExample.xaml#imagebrushrelativetransformexample)]  
  
 Im zweiten Beispiel wird auch ein <xref:System.Windows.Media.RotateTransform> auf einen angewendet <xref:System.Windows.Media.ImageBrush> . Allerdings wird in diesem Beispiel die- <xref:System.Windows.Media.Brush.Transform%2A> Eigenschaft anstelle der- <xref:System.Windows.Media.Brush.RelativeTransform%2A> Eigenschaft verwendet.  
  
 Um den Pinsel um seinen Mittelpunkt zu drehen, werden im Beispiel die <xref:System.Windows.Media.RotateTransform.CenterX%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.RotateTransform.CenterY%2A> des- <xref:System.Windows.Media.RotateTransform> Objekts auf absolute Koordinaten festgelegt. Da der Pinsel ein Rechteck mit der Größe 175 mal 90 Pixel zeichnet, liegt der Mittelpunkt des Rechtecks bei (87,5/45).  
  
 [!code-csharp[BrushesIntroduction_snip#ImageBrushTransformExample](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/BrushTransformExample.cs#imagebrushtransformexample)]
 [!code-vb[BrushesIntroduction_snip#ImageBrushTransformExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/brushtransformexample.vb#imagebrushtransformexample)]
 [!code-xaml[BrushesIntroduction_snip#ImageBrushTransformExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/BrushTransformExample.xaml#imagebrushtransformexample)]  
  
 Eine Beschreibung der Funktionsweise der <xref:System.Windows.Media.Brush.RelativeTransform%2A> -und- <xref:System.Windows.Media.Brush.Transform%2A> Eigenschaften finden Sie in der [Übersicht über die Pinsel Transformation](brush-transformation-overview.md).  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes). Weitere Informationen über Pinsel finden Sie unter [Übersicht über das Zeichnen mit Volltonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md).  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Pinseltransformationen](brush-transformation-overview.md)
- [Übersicht über das Zeichnen mit Volltonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md)
- [Übersicht über Transformationen](transforms-overview.md)
