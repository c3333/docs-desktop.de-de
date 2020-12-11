---
title: 'Gewusst wie: Zeichnen eines Bereichs mit einem linearen Farbverlauf'
ms.date: 03/30/2017
helpviewer_keywords:
- linear gradients [WPF], painting with
- brushes [WPF], painting with linear gradients
- painting [WPF], with linear gradients
ms.assetid: 00e0cd04-48c0-4ec5-850e-d321beb37a34
ms.openlocfilehash: 76c491632911c48db34d932ba3895278591378a5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976542"
---
# <a name="how-to-paint-an-area-with-a-linear-gradient"></a>Gewusst wie: Zeichnen eines Bereichs mit einem linearen Farbverlauf
In diesem Beispiel wird gezeigt, wie die-Klasse verwendet wird <xref:System.Windows.Media.LinearGradientBrush> , um einen Bereich mit einem linearen Farbverlauf zu zeichnen. Im folgenden Beispiel <xref:System.Windows.Shapes.Shape.Fill%2A> wird der eines <xref:System.Windows.Shapes.Rectangle> mit einem diagonalen linearen Farbverlauf gezeichnet, der von gelb zu rot zu blau in Kalk grün übergeht.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[GradientBrushExamples_snip#DiagonalGradient1XAML](~/samples/snippets/xaml/VS_Snippets_Wpf/GradientBrushExamples_snip/XAML/LinearGradientBrushExample.xaml#diagonalgradient1xaml)]  
  
 [!code-csharp[GradientBrushExamples_snip#DiagonalGradient1CSharp](~/samples/snippets/csharp/VS_Snippets_Wpf/GradientBrushExamples_snip/CSharp/LinearGradientBrushExample.cs#diagonalgradient1csharp)]  
  
 Die folgende Abbildung zeigt den im vorherigen Beispiel erstellten Farbverlauf.  
  
 ![Diagonaler, linearer Farbverlauf](./media/graphicsmm-diagonallgb.jpg "graphicsmm_DiagonalLGB")  
  
 Um einen horizontalen linearen Farbverlauf zu erstellen, <xref:System.Windows.Media.LinearGradientBrush.StartPoint%2A> ändern <xref:System.Windows.Media.LinearGradientBrush.EndPoint%2A> Sie und von <xref:System.Windows.Media.LinearGradientBrush> in (0,0) und (1, 0,5). Im folgenden Beispiel <xref:System.Windows.Shapes.Rectangle> wird ein mit einem horizontalen linearen Farbverlauf gezeichnet.  
  
 [!code-xaml[GradientBrushExamples_snip#HorizontalGradient1XAML](~/samples/snippets/xaml/VS_Snippets_Wpf/GradientBrushExamples_snip/XAML/LinearGradientBrushExample.xaml#horizontalgradient1xaml)]  
  
 [!code-csharp[GradientBrushExamples_snip#HorizontalGradient1CSharp](~/samples/snippets/csharp/VS_Snippets_Wpf/GradientBrushExamples_snip/CSharp/LinearGradientBrushExample.cs#horizontalgradient1csharp)]  
  
 Die folgende Abbildung zeigt den im vorherigen Beispiel erstellten Farbverlauf.  
  
 ![Ein horizontaler, linearer Farbverlauf](./media/graphicsmm-horizontallgb.jpg "graphicsmm_HorizontalLGB")  
  
 Um einen vertikalen linearen Farbverlauf zu erstellen, <xref:System.Windows.Media.LinearGradientBrush.StartPoint%2A> ändern <xref:System.Windows.Media.LinearGradientBrush.EndPoint%2A> Sie und von <xref:System.Windows.Media.LinearGradientBrush> in (0,5, 0) und (0,5, 1). Im folgenden Beispiel <xref:System.Windows.Shapes.Rectangle> wird ein mit einem vertikalen linearen Farbverlauf gezeichnet.  
  
 [!code-xaml[GradientBrushExamples_snip#VerticalGradient1XAML](~/samples/snippets/xaml/VS_Snippets_Wpf/GradientBrushExamples_snip/XAML/LinearGradientBrushExample.xaml#verticalgradient1xaml)]  
  
 [!code-csharp[GradientBrushExamples_snip#VerticalGradient1CSharp](~/samples/snippets/csharp/VS_Snippets_Wpf/GradientBrushExamples_snip/CSharp/LinearGradientBrushExample.cs#verticalgradient1csharp)]  
  
 Die folgende Abbildung zeigt den im vorherigen Beispiel erstellten Farbverlauf.  
  
 ![Vertikaler, linearer Farbverlauf](./media/graphicsmm-verticallgb.jpg "graphicsmm_VerticalLGB")  
  
> [!NOTE]
> In den Beispielen in diesem Thema wird das Standard Koordinatensystem zum Festlegen von Startpunkten und Endpunkten verwendet. Das Standard Koordinatensystem ist relativ zu einem umgebenden Feld: 0 gibt 0 Prozent des umgebenden Felds an, und 1 gibt 100 Prozent des umgebenden Felds an. Sie können dieses Koordinatensystem ändern, indem Sie die- <xref:System.Windows.Media.GradientBrush.MappingMode%2A> Eigenschaft auf den Wert festlegen <xref:System.Windows.Media.BrushMappingMode.Absolute?displayProperty=nameWithType> . Ein absolutes Koordinatensystem ist nicht relativ zu einem umgebenden Feld. Werte werden direkt im lokalen Raum interpretiert.  
  
 Weitere Beispiele finden Sie unter [Beispiel für Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes). Weitere Informationen zu Farbverläufen und anderen Pinseltypen finden Sie unter Übersicht über das Zeichnen [mit voll Tonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md).
