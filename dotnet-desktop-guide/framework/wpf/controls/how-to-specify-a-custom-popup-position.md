---
title: 'Gewusst wie: Angeben einer benutzerdefinierten Popup-Position'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Popup control [WPF], specifying custom position
ms.assetid: 28c24f39-d3aa-4ee2-b950-384b4a5dab92
ms.openlocfilehash: b48dedc044b418062642af5c5bb40afab78a3c97
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977526"
---
# <a name="how-to-specify-a-custom-popup-position"></a><span data-ttu-id="02b9e-102">Gewusst wie: Angeben einer benutzerdefinierten Popup-Position</span><span class="sxs-lookup"><span data-stu-id="02b9e-102">How to: Specify a Custom Popup Position</span></span>
<span data-ttu-id="02b9e-103">In diesem Beispiel wird gezeigt, wie eine benutzerdefinierte Position für ein Steuerelement angegeben <xref:System.Windows.Controls.Primitives.Popup> wird, wenn die- <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> Eigenschaft auf festgelegt ist <xref:System.Windows.Controls.Primitives.PlacementMode.Custom> .</span><span class="sxs-lookup"><span data-stu-id="02b9e-103">This example shows how to specify a custom position for a <xref:System.Windows.Controls.Primitives.Popup> control when the <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> property is set to <xref:System.Windows.Controls.Primitives.PlacementMode.Custom>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="02b9e-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="02b9e-104">Example</span></span>  
 <span data-ttu-id="02b9e-105">Wenn die- <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> Eigenschaft auf festgelegt ist <xref:System.Windows.Controls.Primitives.PlacementMode.Custom> , <xref:System.Windows.Controls.Primitives.Popup> Ruft die eine definierte Instanz des Delegaten auf <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> .</span><span class="sxs-lookup"><span data-stu-id="02b9e-105">When the <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> property is set to <xref:System.Windows.Controls.Primitives.PlacementMode.Custom>, the <xref:System.Windows.Controls.Primitives.Popup> calls a defined instance of the <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> delegate.</span></span> <span data-ttu-id="02b9e-106">Dieser Delegat gibt eine Reihe möglicher Punkte zurück, die relativ zur linken oberen Ecke des Zielbereichs und der linken oberen Ecke von sind <xref:System.Windows.Controls.Primitives.Popup> .</span><span class="sxs-lookup"><span data-stu-id="02b9e-106">This delegate returns a set of possible points that are relative to the top-left corner of the target area and the top-left corner of the <xref:System.Windows.Controls.Primitives.Popup>.</span></span> <span data-ttu-id="02b9e-107">Die <xref:System.Windows.Controls.Primitives.Popup> Platzierung erfolgt an dem Punkt, an dem die beste Sichtbarkeit bereit steht.</span><span class="sxs-lookup"><span data-stu-id="02b9e-107">The <xref:System.Windows.Controls.Primitives.Popup> placement occurs at the point that provides the best visibility.</span></span>  
  
 <span data-ttu-id="02b9e-108">Im folgenden Beispiel wird gezeigt, wie die Position eines definiert <xref:System.Windows.Controls.Primitives.Popup> wird, indem die-Eigenschaft auf festgelegt wird <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> <xref:System.Windows.Controls.Primitives.PlacementMode.Custom> .</span><span class="sxs-lookup"><span data-stu-id="02b9e-108">The following example shows how to define the position of a <xref:System.Windows.Controls.Primitives.Popup> by setting the <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> property to <xref:System.Windows.Controls.Primitives.PlacementMode.Custom>.</span></span> <span data-ttu-id="02b9e-109">Außerdem wird gezeigt, wie ein Delegat erstellt und zugewiesen wird <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> , um die zu positionieren <xref:System.Windows.Controls.Primitives.Popup> .</span><span class="sxs-lookup"><span data-stu-id="02b9e-109">It also shows how to create and assign a <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> delegate in order to position the <xref:System.Windows.Controls.Primitives.Popup>.</span></span>  <span data-ttu-id="02b9e-110">Der Rückruf Delegat gibt zwei- <xref:System.Windows.Controls.Primitives.CustomPopupPlacement> Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="02b9e-110">The callback delegate returns two <xref:System.Windows.Controls.Primitives.CustomPopupPlacement> objects.</span></span>  <span data-ttu-id="02b9e-111">Wenn die <xref:System.Windows.Controls.Primitives.Popup> von einem Bildschirmrand an der ersten Position ausgeblendet wird, <xref:System.Windows.Controls.Primitives.Popup> wird der an der zweiten Position platziert.</span><span class="sxs-lookup"><span data-stu-id="02b9e-111">If the <xref:System.Windows.Controls.Primitives.Popup> is hidden by a screen edge at the first position, the <xref:System.Windows.Controls.Primitives.Popup> is placed at the second position.</span></span>  
  
 [!code-xaml[PopupCustomPlacement#CustomPlacement](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupCustomPlacement/CSharp/Window1.xaml#customplacement)]  
  
 [!code-csharp[PopupCustomPlacement#DelegateInstance](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupCustomPlacement/CSharp/Window1.xaml.cs#delegateinstance)]
 [!code-vb[PopupCustomPlacement#DelegateInstance](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PopupCustomPlacement/visualbasic/window1.xaml.vb#delegateinstance)]  
  
 [!code-csharp[PopupCustomPlacement#DelegateDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupCustomPlacement/CSharp/Window1.xaml.cs#delegatedefinition)]
 [!code-vb[PopupCustomPlacement#DelegateDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PopupCustomPlacement/visualbasic/window1.xaml.vb#delegatedefinition)]  
  
 <span data-ttu-id="02b9e-112">Das komplette Beispiel finden Sie unter [Beispiel für eine Popup Platzierung](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/PopupPositionSnippet/CS).</span><span class="sxs-lookup"><span data-stu-id="02b9e-112">For the complete sample, see [Popup Placement Sample](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/PopupPositionSnippet/CS).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="02b9e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02b9e-113">See also</span></span>

- <xref:System.Windows.Controls.Primitives.Popup>
- [<span data-ttu-id="02b9e-114">Übersicht über Popup</span><span class="sxs-lookup"><span data-stu-id="02b9e-114">Popup overview</span></span>](popup-overview.md)
- [<span data-ttu-id="02b9e-115">Gewusst-wie-Artikel</span><span class="sxs-lookup"><span data-stu-id="02b9e-115">How-to articles</span></span>](popup-how-to-topics.md)
