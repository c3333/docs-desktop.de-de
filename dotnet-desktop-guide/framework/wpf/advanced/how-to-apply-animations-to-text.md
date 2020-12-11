---
title: 'Gewusst wie: Anwenden von Animationen auf Text'
ms.date: 03/30/2017
helpviewer_keywords:
- typography [WPF], animations
- animation [WPF], text
ms.assetid: eec3d26c-0a21-420f-8012-671621c47089
ms.openlocfilehash: ed2f3beb904f724ac93e2c4033aa6b2eb3fa1290
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976387"
---
# <a name="how-to-apply-animations-to-text"></a>Gewusst wie: Anwenden von Animationen auf Text
Animationen können die Anzeige und die Darstellung von Text in Ihrer Anwendung ändern. In den folgenden Beispielen werden verschiedene Animations Typen verwendet, um die Anzeige von Text in einem-Steuerelement zu beeinflussen <xref:System.Windows.Controls.TextBlock> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.DoubleAnimation> , um die Breite des Textblocks zu animieren. Der Breitenwert ändert sich innerhalb von 10 Sekunden von der Breite des Textblocks auf 0. Anschließend werden die Breitenwerte umgekehrt und es wird fortgefahren. Dieser Animationstyp erstellt einen Wipe-Effekt.  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample1)]  
  
 Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.DoubleAnimation> , um die Deckkraft des Textblocks zu animieren. Der Deckkraftwert wird über einen Zeitraum von 5 Sekunden von 1,0 auf 0 geändert. Anschließend werden die Deckkraftwerte umgekehrt und es wird fortgefahren.  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample2)]  
  
 Im folgenden Diagramm wird dargestellt, wie sich das- <xref:System.Windows.Controls.TextBlock> Steuerelement `1.00` `0.00` im Rahmen des 5-Sekunden-Intervalls, das von definiert wird, durch die Deckkraft ändern <xref:System.Windows.Media.Animation.Timeline.Duration%2A> .  
  
 ![Text, der die Deckkraft von 1,00 auf 0,00 ändert.](./media/how-to-apply-animations-to-text/faded-text-opacity-change.png)  

 Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.ColorAnimation> , um die Vordergrundfarbe des Textblocks zu animieren. Der Wert für die Vordergrundfarbe ändert sich im Verlauf von 5 Sekunden von einer Farbe in eine zweite Farbe. Anschließend werden die Farbwerte umgekehrt und es wird fortgefahren.  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample3](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample3)]  
  
 Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.DoubleAnimation> , um den TextBlock zu drehen. Der Textblock führt eine vollständige Drehung über einen Zeitraum von 20 Sekunden aus, und anschließend wird die Drehung wiederholt.  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample4](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample4)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Animationen](../graphics-multimedia/animation-overview.md)
