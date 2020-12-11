---
title: 'Gewusst wie: Animieren der Farbe oder der Durchlässigkeit von SolidColorBrush'
ms.date: 03/30/2017
helpviewer_keywords:
- SolidColorBrush [WPF], animating color of
- colors [WPF], animating
- opacity [WPF], animating
- animation [WPF], color of SolidColorBrush
- animation [WPF], opacity of SolidColorBrush
- SolidColorBrush [WPF], animating opacity of
ms.assetid: d9154354-843f-4713-bad1-35bb0ba6eaeb
ms.openlocfilehash: 08b85935e0cb1ababd1fb63b9d02518ea3fcfa17
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975410"
---
# <a name="how-to-animate-the-color-or-opacity-of-a-solidcolorbrush"></a>Gewusst wie: Animieren der Farbe oder der Durchlässigkeit von SolidColorBrush
In diesem Beispiel wird gezeigt, wie die <xref:System.Windows.Media.SolidColorBrush.Color%2A> und eines animiert werden <xref:System.Windows.Media.Brush.Opacity%2A> <xref:System.Windows.Media.SolidColorBrush> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden drei Animationen zum Animieren der <xref:System.Windows.Media.SolidColorBrush.Color%2A> und <xref:System.Windows.Media.Brush.Opacity%2A> einer verwendet <xref:System.Windows.Media.SolidColorBrush> .  
  
- Die erste Animation, a <xref:System.Windows.Media.Animation.ColorAnimation> , ändert die Farbe des Pinsels in, <xref:System.Windows.Media.Colors.Gray%2A> Wenn die Maus in das Rechteck eintritt.  
  
- Die nächste Animation, eine andere <xref:System.Windows.Media.Animation.ColorAnimation> , ändert die Farbe des Pinsels in, <xref:System.Windows.Media.Colors.Orange%2A> Wenn der Mauszeiger das Rechteck verlässt.  
  
- Die letzte Animation, a <xref:System.Windows.Media.Animation.DoubleAnimation> , ändert die Deckkraft des Pinsels in 0,0, wenn die linke Maustaste gedrückt wird.  
  
 [!code-csharp[brushanimations_snip#SolidColorBrushAnimationExample](~/samples/snippets/csharp/VS_Snippets_Wpf/brushanimations_snip/CSharp/SolidColorBrushExample.cs#solidcolorbrushanimationexample)]  
  
 Ein ausführeres Beispiel, das zeigt, wie Sie verschiedene Arten von Pinseln animieren, finden Sie im [Beispiel Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes). Weitere Informationen zur Animation finden Sie unter [Übersicht über Animationen](animation-overview.md).  
  
 Aus Gründen der Konsistenz mit anderen Animations Beispielen wird in den Code Versionen dieses Beispiels ein-Objekt verwendet, <xref:System.Windows.Media.Animation.Storyboard> um Ihre Animationen anzuwenden. Beim Anwenden einer einzelnen Animation im Code ist es jedoch einfacher, die-Methode zu verwenden, <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> anstatt eine zu verwenden <xref:System.Windows.Media.Animation.Storyboard> . Ein Beispiel finden Sie unter [Animieren einer Eigenschaft ohne Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Animationen](animation-overview.md)
- [Übersicht über Storyboards](storyboards-overview.md)
- [Beispiel für Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes)
