---
title: 'Gewusst wie: Animieren der Position oder Farbe eines Farbverlaufunterbrechungspunkts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- position [WPF], animating
- animation [WPF], position of GradientStop objects
- GradientStop objects [WPF], animating color of
- colors [WPF], animating
- animation [WPF], color of GradientStop objects
- GradientStop objects [WPF], animating position of
ms.assetid: 6f5b8b47-6c32-4b8e-98ee-fdf6515ec843
ms.openlocfilehash: aeae33f5f3c8016808988f58d61969e9b6f05039
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975330"
---
# <a name="how-to-animate-the-position-or-color-of-a-gradient-stop"></a>Gewusst wie: Animieren der Position oder Farbe eines Farbverlaufunterbrechungspunkts
Dieses Beispiel zeigt, wie das <xref:System.Windows.Media.GradientStop.Color%2A> -Objekt und das-Objekt animiert werden <xref:System.Windows.Media.GradientStop.Offset%2A> <xref:System.Windows.Media.GradientStop> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden drei Farbverlaufs Stopps in einem animiert <xref:System.Windows.Media.LinearGradientBrush> . In diesem Beispiel werden drei Animationen verwendet, von denen jede einen anderen Farbverlaufs-halte Vorgang animiert:  
  
- Die erste Animation, a <xref:System.Windows.Media.Animation.DoubleAnimation> , animiert den ersten Farbverlaufs anzuhalten <xref:System.Windows.Media.GradientStop.Offset%2A> von 0,0 bis 1,0 und dann zurück zu 0,0. Folglich verschiebt sich die erste Farbe im Farbverlauf von der linken zum rechten Rand des Rechtecks und dann zurück zur linken Seite.  
  
- Die zweite Animation, a <xref:System.Windows.Media.Animation.ColorAnimation> , animiert die zweite Farbverlaufs Stopps <xref:System.Windows.Media.GradientStop.Color%2A> von <xref:System.Windows.Media.Colors.Purple%2A> auf <xref:System.Windows.Media.Colors.Yellow%2A> und dann zurück zu <xref:System.Windows.Media.Colors.Purple%2A> . Folglich wechselt die Mittel Farbe im Farbverlauf von lila in gelb und zurück zu Lila.  
  
- Die dritte Animation, eine andere <xref:System.Windows.Media.Animation.ColorAnimation> , animiert die Deckkraft des dritten Farbverlaufs Stopps <xref:System.Windows.Media.GradientStop.Color%2A> durch-1 und dann zurück. Folglich wird die dritte Farbe im Farbverlauf ausgeblendet und dann wieder transparent.  
  
 [!code-csharp[BrushesIntroduction_snip#GraphicsMMGradientAnimationExamplesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/GradientStopAnimationExample.cs#graphicsmmgradientanimationexampleswholepage)]
 [!code-vb[BrushesIntroduction_snip#GraphicsMMGradientAnimationExamplesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/gradientstopanimationexample.vb#graphicsmmgradientanimationexampleswholepage)]
 [!code-xaml[BrushesIntroduction_snip#GraphicsMMGradientAnimationExamplesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/GradientStopAnimationExample.xaml#graphicsmmgradientanimationexampleswholepage)]  
  
 Obwohl in diesem Beispiel ein verwendet <xref:System.Windows.Media.LinearGradientBrush> wird, ist der Prozess für das Animieren von <xref:System.Windows.Media.GradientStop> Objekten in einer identisch <xref:System.Windows.Media.RadialGradientBrush> .  
  
 Weitere Beispiele finden Sie im [Beispiel Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.GradientStop>
- [Übersicht über Animationen](animation-overview.md)
- [Übersicht über Storyboards](storyboards-overview.md)
