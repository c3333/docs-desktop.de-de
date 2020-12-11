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
# <a name="how-to-specify-handoffbehavior-between-storyboard-animations"></a><span data-ttu-id="d19db-102">Gewusst wie: Angeben des Übergabeverhaltens zwischen Storyboard-Animationen</span><span class="sxs-lookup"><span data-stu-id="d19db-102">How to: Specify HandoffBehavior Between Storyboard Animations</span></span>
<span data-ttu-id="d19db-103">In diesem Beispiel wird gezeigt, wie das Übergabe Verhalten zwischen Storyboard-Animationen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d19db-103">This example shows how to specify handoff behavior between storyboard animations.</span></span> <span data-ttu-id="d19db-104">Die- <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> Eigenschaft von <xref:System.Windows.Media.Animation.BeginStoryboard> gibt an, wie neue Animationen mit vorhandenen Animationen interagieren, die bereits auf eine Eigenschaft angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d19db-104">The <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> property of <xref:System.Windows.Media.Animation.BeginStoryboard> specifies how new animations interact with any existing ones that are already applied to a property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d19db-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d19db-105">Example</span></span>  
 <span data-ttu-id="d19db-106">Im folgenden Beispiel werden zwei Schaltflächen erstellt, die vergrößert werden, wenn der Mauszeiger darüber bewegt wird und kleiner wird, wenn sich der Cursor weg bewegt.</span><span class="sxs-lookup"><span data-stu-id="d19db-106">The following example creates two buttons that enlarge when the mouse cursor moves over them and become smaller when the cursor moves away.</span></span> <span data-ttu-id="d19db-107">Wenn Sie mit der Maus auf eine Schaltfläche klicken und dann schnell den Cursor entfernen, wird die zweite Animation angewendet, bevor der erste Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d19db-107">If you mouse over a button and then quickly remove the cursor, the second animation will be applied before the first one is finished.</span></span> <span data-ttu-id="d19db-108">Wenn sich zwei Animationen wie diese überlappen, sehen Sie den Unterschied zwischen den <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> Werten von <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> und <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace> .</span><span class="sxs-lookup"><span data-stu-id="d19db-108">It is when two animations overlap like this that you can see the difference between the <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> values of <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> and <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace>.</span></span> <span data-ttu-id="d19db-109">Ein Wert von <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> kombiniert die überlappenden Animationen, was zu einem reibungsloseren Übergang zwischen Animationen führt, während der Wert <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace> bewirkt, dass die neue Animation die frühere überlappende Animation sofort ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d19db-109">A value of <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> combines the overlapping animations causing a smoother transition between animations while a value of <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace> causes the new animation to immediately replace the earlier overlapping animation.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#HandoffBehaviorWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/HandoffBehaviorExample.xaml#handoffbehaviorwholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="d19db-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d19db-110">See also</span></span>

- <xref:System.Windows.Media.Animation.BeginStoryboard>
- <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A>
- [<span data-ttu-id="d19db-111">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="d19db-111">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="d19db-112">Gewusst-wie-Themen zu Animation und Zeitsteuerung</span><span class="sxs-lookup"><span data-stu-id="d19db-112">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
