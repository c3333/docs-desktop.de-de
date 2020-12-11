---
title: 'Gewusst wie: Behandeln eines geladenen Ereignisses'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- XAML [WPF], Loaded events
- events [WPF], Loaded
- Loaded events [WPF]
ms.assetid: 0cf8d003-8441-4df4-807a-6db09347e829
ms.openlocfilehash: 7ca95e195792f8fb4789c481e84dda51f2910434
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976286"
---
# <a name="how-to-handle-a-loaded-event"></a><span data-ttu-id="ff962-102">Gewusst wie: Behandeln eines geladenen Ereignisses</span><span class="sxs-lookup"><span data-stu-id="ff962-102">How to: Handle a Loaded Event</span></span>
<span data-ttu-id="ff962-103">Dieses Beispiel zeigt, wie das <xref:System.Windows.FrameworkElement.Loaded?displayProperty=nameWithType> -Ereignis und ein entsprechendes Szenario für die Behandlung dieses Ereignisses behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="ff962-103">This example shows how to handle the <xref:System.Windows.FrameworkElement.Loaded?displayProperty=nameWithType> event, and an appropriate scenario for handling that event.</span></span> <span data-ttu-id="ff962-104">Der Handler erstellt eine, <xref:System.Windows.Controls.Button> Wenn die Seite geladen wird.</span><span class="sxs-lookup"><span data-stu-id="ff962-104">The handler  creates a <xref:System.Windows.Controls.Button> when the page loads.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ff962-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ff962-105">Example</span></span>  
 <span data-ttu-id="ff962-106">Im folgenden Beispiel wird [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] in Verbindung mit einer Code Behind-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff962-106">The following example uses [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] together with a code-behind file.</span></span>  
  
 [!code-xaml[FELoaded#XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FELoaded/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[FELoaded#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/FELoaded/CSharp/default.xaml.cs#handler)]
 [!code-vb[FELoaded#Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FELoaded/VisualBasic/default.xaml.vb#handler)]  
  
## <a name="see-also"></a><span data-ttu-id="ff962-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff962-107">See also</span></span>

- <xref:System.Windows.FrameworkElement>
- [<span data-ttu-id="ff962-108">Objektlebensdauer-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ff962-108">Object Lifetime Events</span></span>](object-lifetime-events.md)
- [<span data-ttu-id="ff962-109">Übersicht über Routingereignisse</span><span class="sxs-lookup"><span data-stu-id="ff962-109">Routed Events Overview</span></span>](routed-events-overview.md)
- [<span data-ttu-id="ff962-110">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="ff962-110">How-to Topics</span></span>](base-elements-how-to-topics.md)
