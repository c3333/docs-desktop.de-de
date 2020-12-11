---
title: 'Gewusst wie: Wiederholen einer Animation'
ms.date: 03/30/2017
helpviewer_keywords:
- RepeatBehavior property of timelines [WPF]
- repeating animating [WPF]
- Timelines RepeatBehavior property [WPF]
- animation [WPF], repeating
ms.assetid: e6f3b068-eeeb-47fd-8d40-8848c31f1e1e
ms.openlocfilehash: 1512c49a658c80f3ab6af652839c3562af3dd205
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978016"
---
# <a name="how-to-repeat-an-animation"></a>Gewusst wie: Wiederholen einer Animation
In diesem Beispiel wird gezeigt, wie die-Eigenschaft eines verwendet wird, um <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> <xref:System.Windows.Media.Animation.Timeline> das Wiederholungs Verhalten einer Animation zu steuern.  
  
## <a name="example"></a>Beispiel  
 Die- <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> Eigenschaft eines <xref:System.Windows.Media.Animation.Timeline> steuert, wie oft eine Animation ihre einfache Dauer wiederholt. Mithilfe von <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> können Sie angeben, dass eine <xref:System.Windows.Media.Animation.Timeline> für eine bestimmte Anzahl von vorkommen (eine Iterations Anzahl) oder für einen angegebenen Zeitraum wiederholt werden soll. In beiden Fällen durchläuft die Animation so viele End-to-End-Ausführungen, die Sie benötigen, um die angeforderte Anzahl oder Dauer auszufüllen.  
  
 Standardmäßig haben Zeitachsen eine Wiederholungs Anzahl von 1,0. Dies bedeutet, dass Sie einmalig wiedergegeben werden und nicht wiederholt werden. Wenn Sie jedoch die- <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> Eigenschaft eines auf festlegen <xref:System.Windows.Media.Animation.Timeline> <xref:System.Windows.Media.Animation.RepeatBehavior.Forever%2A> , wird die Zeitachse unbegrenzt wiederholt.  
  
 Im folgenden Beispiel wird gezeigt, wie die-Eigenschaft verwendet wird <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> , um das Wiederholungs Verhalten einer Animation zu steuern. Im Beispiel wird die- <xref:System.Windows.FrameworkElement.Width%2A> Eigenschaft von fünf Rechtecke mit den einzelnen Rechtecks mit einem anderen Typ von Wiederholungs Verhalten animiert.  
  
 [!code-xaml[timingbehaviors_snip#RepeatBehaviorWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/RepeatBehaviorExample.xaml#repeatbehaviorwholepage)]  
  
 Das komplette Beispiel finden Sie unter [Beispiel für Animations Zeitverhalten](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/AnimationTiming).  
  
## <a name="see-also"></a>Siehe auch

- [Sammeln von Animationen während Wiederholungszyklen](how-to-accumulate-animation-values-during-repeat-cycles.md)
- [Festlegen, ob eine Zeitachse automatisch umgekehrt wird](how-to-specify-whether-a-timeline-automatically-reverses.md)
- [Gewusst-wie-Themen zu Animation und Zeitsteuerung](animation-and-timing-how-to-topics.md)
- [Übersicht über Animationen](animation-overview.md)
- [Beispiel zum Verhalten der Animationszeitsteuerung](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/AnimationTiming)
