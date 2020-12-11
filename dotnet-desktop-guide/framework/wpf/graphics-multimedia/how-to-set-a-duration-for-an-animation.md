---
title: 'Gewusst wie: Festlegen der Dauer einer Animation'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], duration
- Timelines [WPF], description
- duration of animations [WPF]
ms.assetid: 155034ef-7d00-4416-a73c-b1713992d2eb
ms.openlocfilehash: bdae1689ffeb8c54d756b9debbd26d57a052892d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977939"
---
# <a name="how-to-set-a-duration-for-an-animation"></a>Gewusst wie: Festlegen der Dauer einer Animation
Ein <xref:System.Windows.Media.Animation.Timeline> stellt einen Zeitabschnitt dar, und die Länge dieses Segments wird durch die der Zeitachse bestimmt <xref:System.Windows.Duration> . Wenn ein <xref:System.Windows.Media.Animation.Timeline> das Ende seiner Dauer erreicht, wird die Wiedergabe beendet. Wenn das untergeordnete Zeit <xref:System.Windows.Media.Animation.Timeline> Achsen hat, wird die Wiedergabe ebenfalls beendet. Im Fall einer Animation gibt das an, <xref:System.Windows.Duration> wie lange die Animation für den Übergang vom Startwert zum Endwert benötigt.  
  
 Sie können einen <xref:System.Windows.Duration> mit einer bestimmten, begrenzten Uhrzeit oder den speziellen Werten <xref:System.Windows.Duration.Automatic%2A> oder angeben <xref:System.Windows.Duration.Forever%2A> . Die Dauer einer Animation muss immer ein Uhrzeitwert sein, da eine Animation immer eine definierte, begrenzte Länge haben muss – andernfalls weiß die Animation nicht, wie Sie zwischen den Zielwerten wechseln kann. Containertimelines ( <xref:System.Windows.Media.Animation.TimelineGroup> -Objekte), wie z. b. <xref:System.Windows.Media.Animation.Storyboard> und <xref:System.Windows.Media.Animation.ParallelTimeline> , haben eine Standarddauer von. dies <xref:System.Windows.Duration.Automatic%2A> bedeutet, dass Sie automatisch enden, wenn das letzte untergeordnete Element beendet wird.  
  
 Im folgenden Beispiel wird die Breite, die Höhe und die Füllfarbe eines <xref:System.Windows.Shapes.Rectangle> animiert. Dauer werden für Animations-und Container Zeitachse festgelegt, was zu Animationseffekten führt, einschließlich der Steuerung der erkannten Geschwindigkeit einer Animation und Überschreiben der Dauer von untergeordneten Zeitachsen mit der Dauer einer Container Zeitachse.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[timingbehaviors_snip#DurationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/DurationExample.xaml#durationexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Duration>
- [Übersicht über Animationen](animation-overview.md)
