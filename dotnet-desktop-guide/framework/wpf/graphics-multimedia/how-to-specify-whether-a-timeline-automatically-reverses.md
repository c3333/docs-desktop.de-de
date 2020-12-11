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
# <a name="how-to-specify-whether-a-timeline-automatically-reverses"></a><span data-ttu-id="1c657-102">Gewusst wie: Angeben, ob die Wiedergaberichtung einer Zeitachse automatisch umgekehrt wird</span><span class="sxs-lookup"><span data-stu-id="1c657-102">How to: Specify Whether a Timeline Automatically Reverses</span></span>
<span data-ttu-id="1c657-103">Die-Eigenschaft einer Zeitachse <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> bestimmt, ob Sie nach Abschluss einer Forward-Iterations Anweisung in umgekehrter Reihenfolge abgespielt</span><span class="sxs-lookup"><span data-stu-id="1c657-103">A timeline's <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> property determines whether it plays in reverse after it completes a forward iteration.</span></span> <span data-ttu-id="1c657-104">Das folgende Beispiel zeigt mehrere Animationen mit identischen Duration-und Zielwerten, aber mit anderen <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="1c657-104">The following example shows several animations with identical duration and target values, but with different <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> settings.</span></span> <span data-ttu-id="1c657-105">Um zu veranschaulichen, wie sich die- <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> Eigenschaft mit anderen <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> Einstellungen verhält, werden einige Animationen für die Wiederholung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c657-105">To demonstrate how the <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> property behaves with different <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> settings, some animations are set to repeat.</span></span> <span data-ttu-id="1c657-106">Die letzte Animation zeigt, wie die-Eigenschaft für die Verwendung von in der-Tabelle vorlag <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> .</span><span class="sxs-lookup"><span data-stu-id="1c657-106">The last animation shows how the <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> property works on nested timelines.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1c657-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1c657-107">Example</span></span>  
 [!code-xaml[timingbehaviors_snip#AutoReverseAndRepeatBehaviorExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AutoReverseExample.xaml#autoreverseandrepeatbehaviorexamplewholepage)]
