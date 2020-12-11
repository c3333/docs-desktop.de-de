---
title: 'Gewusst wie: Angeben, ob die Wiedergaberichtung einer Zeitachse automatisch umgekehrt wird'
ms.date: 03/30/2017
helpviewer_keywords:
- AutoReverse property of timelines [WPF]
- Timelines [WPF], AutoReverse property
ms.assetid: 1648dd90-1bee-409a-ac69-ac729867f557
ms.openlocfilehash: 0fe2d337d8afa5197475e5b9ee40950226596e8b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975466"
---
# <a name="how-to-specify-whether-a-timeline-automatically-reverses"></a>Gewusst wie: Angeben, ob die Wiedergaberichtung einer Zeitachse automatisch umgekehrt wird
Die-Eigenschaft einer Zeitachse <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> bestimmt, ob Sie nach Abschluss einer Forward-Iterations Anweisung in umgekehrter Reihenfolge abgespielt Das folgende Beispiel zeigt mehrere Animationen mit identischen Duration-und Zielwerten, aber mit anderen <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> Einstellungen. Um zu veranschaulichen, wie sich die- <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> Eigenschaft mit anderen <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> Einstellungen verhält, werden einige Animationen für die Wiederholung festgelegt. Die letzte Animation zeigt, wie die-Eigenschaft für die Verwendung von in der-Tabelle vorlag <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> .  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[timingbehaviors_snip#AutoReverseAndRepeatBehaviorExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AutoReverseExample.xaml#autoreverseandrepeatbehaviorexamplewholepage)]
