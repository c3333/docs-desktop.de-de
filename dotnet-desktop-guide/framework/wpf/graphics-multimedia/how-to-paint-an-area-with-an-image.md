---
title: 'Gewusst wie: Zeichnen eines Bereichs mit einem Bild'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [WPF], painting with
- painting [WPF], with images
- brushes [WPF], painting with images
ms.assetid: 3432c533-1fc7-492d-94ee-0b13d60125ae
ms.openlocfilehash: 92969778c04c6ac634a2964c402d6c3439b96b49
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976186"
---
# <a name="how-to-paint-an-area-with-an-image"></a>Gewusst wie: Zeichnen eines Bereichs mit einem Bild
In diesem Beispiel wird gezeigt, wie die-Klasse verwendet wird <xref:System.Windows.Media.ImageBrush> , um einen Bereich mit einem Bild zu zeichnen. Ein <xref:System.Windows.Media.ImageBrush> zeigt ein einzelnes Bild an, das durch die- <xref:System.Windows.Media.ImageBrush.ImageSource%2A> Eigenschaft angegeben wird.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird der einer <xref:System.Windows.Controls.Control.Background%2A> Schaltfläche mithilfe eines gezeichnet <xref:System.Windows.Media.ImageBrush> .  
  
 [!code-csharp[UsingImageBrush_snip#ImageBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/PaintingWithImagesExample.cs#imagebrushexamplewholepage)]  
  
 Standardmäßig wird <xref:System.Windows.Media.ImageBrush> das Bild von einem gestreckt, um den zu Zeichnungs enden Bereich vollständig auszufüllen. Im vorhergehenden Beispiel wird das Bild zum Ausfüllen der Schaltfläche gestreckt, wobei das Bild möglicherweise verzerrt wird. Sie können dieses Verhalten steuern, indem Sie die- <xref:System.Windows.Media.TileBrush.Stretch%2A> Eigenschaft von <xref:System.Windows.Media.TileBrush> auf <xref:System.Windows.Media.Stretch.Uniform> oder festlegen <xref:System.Windows.Media.Stretch.UniformToFill> , wodurch der Pinsel das Seitenverhältnis des Bilds beibehält.  
  
 Wenn Sie die-Eigenschaft und die-Eigenschaft eines festgelegt <xref:System.Windows.Media.TileBrush.Viewport%2A> <xref:System.Windows.Media.TileBrush.TileMode%2A> <xref:System.Windows.Media.ImageBrush> haben, können Sie ein sich wiederholendes Muster erstellen. Im folgenden Beispiel wird eine Schaltfläche mithilfe eines Musters gezeichnet, das auf Basis eines Bilds erstellt wird.  
  
 [!code-csharp[UsingImageBrush_snip#TiledImageBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TiledImageBrushExample.cs#tiledimagebrushexamplewholepage)]
 [!code-vb[UsingImageBrush_snip#TiledImageBrushExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/UsingImageBrush_snip/VisualBasic/TiledImageBrushExample.vb#tiledimagebrushexamplewholepage)]  
  
 Weitere Informationen zur <xref:System.Windows.Media.ImageBrush> -Klasse finden Sie unterzeichnen [mit Bildern, Zeichnungen und visuellen](painting-with-images-drawings-and-visuals.md)Elementen.  
  
 Dieses Codebeispiel ist Teil eines größeren Beispiels, das für die-Klasse bereitgestellt wird <xref:System.Windows.Media.ImageBrush> . Das komplette Beispiel finden Sie unter [ImageBrush Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/ImageBrush).  
  
## <a name="see-also"></a>Siehe auch

- [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](painting-with-images-drawings-and-visuals.md)
