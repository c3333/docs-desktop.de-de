---
title: 'Gewusst wie: Sicherstellen, dass ein GridSplitter sichtbar ist'
ms.date: 03/30/2017
helpviewer_keywords:
- GridSplitter control [WPF], ensuring visibility of
ms.assetid: 0a62a964-89c8-48f0-9023-5df721a8cf47
ms.openlocfilehash: 2085ac5cec206d8692a1267acf132688f0aa9082
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978165"
---
# <a name="how-to-make-sure-that-a-gridsplitter-is-visible"></a><span data-ttu-id="06791-102">Gewusst wie: Sicherstellen, dass ein GridSplitter sichtbar ist</span><span class="sxs-lookup"><span data-stu-id="06791-102">How to: Make Sure That a GridSplitter Is Visible</span></span>
<span data-ttu-id="06791-103">In diesem Beispiel wird gezeigt, wie sichergestellt wird, dass ein <xref:System.Windows.Controls.GridSplitter> Steuerelement nicht von den anderen Steuerelementen in einer ausgeblendet wird <xref:System.Windows.Controls.Grid> .</span><span class="sxs-lookup"><span data-stu-id="06791-103">This example shows how to make sure a <xref:System.Windows.Controls.GridSplitter> control is not hidden by the other controls in a <xref:System.Windows.Controls.Grid>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="06791-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="06791-104">Example</span></span>  
 <span data-ttu-id="06791-105">Der <xref:System.Windows.Controls.Panel.Children%2A> eines <xref:System.Windows.Controls.Grid> Steuer Elements wird in der Reihenfolge gerendert, in der Sie in Markup oder Code definiert sind.</span><span class="sxs-lookup"><span data-stu-id="06791-105">The <xref:System.Windows.Controls.Panel.Children%2A> of a <xref:System.Windows.Controls.Grid> control are rendered in the order that they are defined in markup or code.</span></span> <span data-ttu-id="06791-106"><xref:System.Windows.Controls.GridSplitter> Steuerelemente können von anderen Steuerelementen ausgeblendet werden, wenn Sie Sie nicht als die letzten Elemente in der Auflistung definieren, <xref:System.Windows.Controls.Panel.Children%2A> oder wenn Sie andere Steuerelemente eine höhere Version angeben <xref:System.Windows.Controls.Panel.ZIndexProperty> .</span><span class="sxs-lookup"><span data-stu-id="06791-106"><xref:System.Windows.Controls.GridSplitter> controls can be hidden by other controls if you do not define them as the last elements in the <xref:System.Windows.Controls.Panel.Children%2A> collection or if you give other controls a higher <xref:System.Windows.Controls.Panel.ZIndexProperty>.</span></span>  
  
 <span data-ttu-id="06791-107"><xref:System.Windows.Controls.GridSplitter>Führen Sie einen der folgenden Schritte aus, um verborgene Steuerelemente zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="06791-107">To prevent hidden <xref:System.Windows.Controls.GridSplitter> controls, do one of the following.</span></span>  
  
- <span data-ttu-id="06791-108">Stellen Sie sicher, dass die-Steuer <xref:System.Windows.Controls.GridSplitter> Elemente der zuletzt <xref:System.Windows.Controls.Panel.Children%2A> hinzugefügt wurden <xref:System.Windows.Controls.Grid> .</span><span class="sxs-lookup"><span data-stu-id="06791-108">Make sure that <xref:System.Windows.Controls.GridSplitter> controls are the last <xref:System.Windows.Controls.Panel.Children%2A> added to the <xref:System.Windows.Controls.Grid>.</span></span> <span data-ttu-id="06791-109">Das folgende Beispiel zeigt <xref:System.Windows.Controls.GridSplitter> als letztes Element in der-Auflistung <xref:System.Windows.Controls.Panel.Children%2A> von <xref:System.Windows.Controls.Grid> .</span><span class="sxs-lookup"><span data-stu-id="06791-109">The following example shows the <xref:System.Windows.Controls.GridSplitter> as the last element in the <xref:System.Windows.Controls.Panel.Children%2A> collection of the <xref:System.Windows.Controls.Grid>.</span></span>  
  
 [!code-xaml[GridSplitterSnips#GridSplitterLastChild](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplitterlastchild)]  
  
- <span data-ttu-id="06791-110">Legen <xref:System.Windows.Controls.Panel.ZIndexProperty> Sie auf fest <xref:System.Windows.Controls.GridSplitter> , damit es höher ist als ein Steuerelement, das es andernfalls ausblenden würde.</span><span class="sxs-lookup"><span data-stu-id="06791-110">Set the <xref:System.Windows.Controls.Panel.ZIndexProperty> on the <xref:System.Windows.Controls.GridSplitter> to be higher than a control that would otherwise hide it.</span></span> <span data-ttu-id="06791-111">Im folgenden Beispiel wird das- <xref:System.Windows.Controls.GridSplitter> Steuerelement höher <xref:System.Windows.Controls.Panel.ZIndexProperty> als das-Steuerelement <xref:System.Windows.Controls.Button> .</span><span class="sxs-lookup"><span data-stu-id="06791-111">The following example gives the <xref:System.Windows.Controls.GridSplitter> control a higher <xref:System.Windows.Controls.Panel.ZIndexProperty> than the <xref:System.Windows.Controls.Button> control.</span></span>  
  
 [!code-xaml[GridSplitterSnips#GridSplitterZIndex](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplitterzindex)]  
  
- <span data-ttu-id="06791-112">Legen Sie Ränder für das-Steuerelement fest, die andernfalls ausblenden, <xref:System.Windows.Controls.GridSplitter> sodass der verfügbar gemacht <xref:System.Windows.Controls.GridSplitter> wird.</span><span class="sxs-lookup"><span data-stu-id="06791-112">Set margins on the control that would otherwise hide the <xref:System.Windows.Controls.GridSplitter> so that the <xref:System.Windows.Controls.GridSplitter> is exposed.</span></span> <span data-ttu-id="06791-113">Im folgenden Beispiel werden die Ränder eines-Steuer Elements festgelegt, das andernfalls überlagern und ausblenden würde <xref:System.Windows.Controls.GridSplitter> .</span><span class="sxs-lookup"><span data-stu-id="06791-113">The following example sets margins on a control that would otherwise overlay and hide the <xref:System.Windows.Controls.GridSplitter>.</span></span>  
  
 [!code-xaml[GridSplitterSnips#GridSplitterMargin](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplittermargin)]  
  
## <a name="see-also"></a><span data-ttu-id="06791-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06791-114">See also</span></span>

- <xref:System.Windows.Controls.GridSplitter>
- [<span data-ttu-id="06791-115">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="06791-115">How-to Topics</span></span>](gridsplitter-how-to-topics.md)
