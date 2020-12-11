---
title: 'Gewusst wie: Angeben des Übergabeverhaltens zwischen Storyboard-Animationen'
ms.date: 03/30/2017
helpviewer_keywords:
- Storyboards [WPF], handoff behavior between animations
- animation [WPF], handoff behavior between
ms.assetid: 97bd6842-929b-49d9-813e-46553ae46472
ms.openlocfilehash: d7129d6a48bdf31dc4953bb450267ad3b38fdd17
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975470"
---
# <a name="how-to-specify-handoffbehavior-between-storyboard-animations"></a>Gewusst wie: Angeben des Übergabeverhaltens zwischen Storyboard-Animationen
In diesem Beispiel wird gezeigt, wie das Übergabe Verhalten zwischen Storyboard-Animationen angegeben wird. Die- <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> Eigenschaft von <xref:System.Windows.Media.Animation.BeginStoryboard> gibt an, wie neue Animationen mit vorhandenen Animationen interagieren, die bereits auf eine Eigenschaft angewendet wurden.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden zwei Schaltflächen erstellt, die vergrößert werden, wenn der Mauszeiger darüber bewegt wird und kleiner wird, wenn sich der Cursor weg bewegt. Wenn Sie mit der Maus auf eine Schaltfläche klicken und dann schnell den Cursor entfernen, wird die zweite Animation angewendet, bevor der erste Vorgang abgeschlossen ist. Wenn sich zwei Animationen wie diese überlappen, sehen Sie den Unterschied zwischen den <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> Werten von <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> und <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace> . Ein Wert von <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> kombiniert die überlappenden Animationen, was zu einem reibungsloseren Übergang zwischen Animationen führt, während der Wert <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace> bewirkt, dass die neue Animation die frühere überlappende Animation sofort ersetzt.  
  
 [!code-xaml[timingbehaviors_snip#HandoffBehaviorWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/HandoffBehaviorExample.xaml#handoffbehaviorwholepage)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.BeginStoryboard>
- <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A>
- [Übersicht über Animationen](animation-overview.md)
- [Gewusst-wie-Themen zu Animation und Zeitsteuerung](animation-and-timing-how-to-topics.md)
