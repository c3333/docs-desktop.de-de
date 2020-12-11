---
title: 'Gewusst wie: Festlegen von FillBehavior für ein Timeline-Objekt, das das Ende des aktiven Zeitraums erreicht hat'
ms.date: 03/30/2017
helpviewer_keywords:
- FillBehavior property for inactive timelines [WPF]
- Timelines [WPF], FillBehavior property
ms.assetid: db805f59-d513-4dac-af15-47005dae3199
ms.openlocfilehash: 1f54f2c1bb49bb7a0301f112a109194ab1a8658e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976844"
---
# <a name="how-to-specify-the-fillbehavior-for-a-timeline-that-has-reached-the-end-of-its-active-period"></a>Gewusst wie: Festlegen von FillBehavior für ein Timeline-Objekt, das das Ende des aktiven Zeitraums erreicht hat
In diesem Beispiel wird gezeigt, wie das- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> Objekt für die inaktive einer <xref:System.Windows.Media.Animation.Timeline> animierten Eigenschaft angegeben wird.  
  
## <a name="example"></a>Beispiel  
 Die- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> Eigenschaft eines <xref:System.Windows.Media.Animation.Timeline> bestimmt, was mit dem Wert einer animierten Eigenschaft geschieht, wenn es nicht animiert wird, d. h., wenn das inaktiv ist, das übergeordnete Element jedoch <xref:System.Windows.Media.Animation.Timeline> <xref:System.Windows.Media.Animation.Timeline> innerhalb des aktiven oder des beibehaltenen Zeitraums liegt. Wenn z. b. eine animierte Eigenschaft an Ihrem Endwert verbleibt, nachdem die Animation beendet wurde, oder wird Sie auf den Wert zurückgesetzt, den Sie vor dem Start der Animation hatte?  
  
 Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.DoubleAnimation> , um die <xref:System.Windows.FrameworkElement.Width%2A> von zwei Rechtecke zu animieren. Jedes Rechteck verwendet ein anderes- <xref:System.Windows.Media.Animation.Timeline> Objekt.  
  
 Eine <xref:System.Windows.Media.Animation.Timeline> verfügt über einen, der <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> auf festgelegt ist <xref:System.Windows.Media.Animation.FillBehavior.Stop> , was bewirkt, dass die Breite des Rechtecks auf seinen nicht animierten Wert zurückgesetzt wird, wenn <xref:System.Windows.Media.Animation.Timeline> beendet wird. Der andere <xref:System.Windows.Media.Animation.Timeline> verfügt über <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> einen <xref:System.Windows.Media.Animation.FillBehavior.HoldEnd> von, der bewirkt, dass die Breite beim Ende des am Endwert verbleibt <xref:System.Windows.Media.Animation.Timeline> .  
  
 [!code-xaml[timingbehaviors_snip#FillBehaviorWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/FillBehaviorExample.xaml#fillbehaviorwholepage)]  
  
 Das komplette Beispiel finden Sie unter [Animation Example Gallery](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/AnimationExamples).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.DoubleAnimation>
- <xref:System.Windows.FrameworkElement.Width%2A>
- <xref:System.Windows.Media.Animation.Timeline>
- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A>
- <xref:System.Windows.Media.Animation.FillBehavior.Stop>
- <xref:System.Windows.Media.Animation.FillBehavior.HoldEnd>
- [Übersicht über Animationen](animation-overview.md)
- [Gewusst-wie-Themen zu Animation und Zeitsteuerung](animation-and-timing-how-to-topics.md)
