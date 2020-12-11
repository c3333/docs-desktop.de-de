---
title: 'Vorgehensweise: Hinzufügen von Suchfunktionen zu einem ListView-Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- lists [Windows Forms], enabling searching
- list views [Windows Forms], enabling searching
- ListView control [Windows Forms], adding search capabilities
- searching [Windows Forms], adding search capabilities to ListView control
ms.assetid: 557782d9-b705-4bab-b496-9938afddac82
ms.openlocfilehash: d5d4dae55fc9f0613ab6535b2fe57e262d0ef141
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976246"
---
# <a name="how-to-add-search-capabilities-to-a-listview-control"></a><span data-ttu-id="d91ed-102">Vorgehensweise: Hinzufügen von Suchfunktionen zu einem ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d91ed-102">How to: Add Search Capabilities to a ListView Control</span></span>
<span data-ttu-id="d91ed-103">Oft, wenn Sie mit einer großen Liste von Elementen in einem Steuerelement arbeiten <xref:System.Windows.Forms.ListView> , möchten Sie dem Benutzer Suchfunktionen anbieten.</span><span class="sxs-lookup"><span data-stu-id="d91ed-103">Oftentimes when working with a large list of items in a <xref:System.Windows.Forms.ListView> control, you want to offer search capabilities to the user.</span></span> <span data-ttu-id="d91ed-104">Das <xref:System.Windows.Forms.ListView> -Steuerelement bietet diese Funktion auf zwei verschiedene Arten: Text Übereinstimmung und Suche nach Orten.</span><span class="sxs-lookup"><span data-stu-id="d91ed-104">The <xref:System.Windows.Forms.ListView> control offers this capability in two different ways: text matching and location searching.</span></span>  
  
 <span data-ttu-id="d91ed-105">Mit der <xref:System.Windows.Forms.ListView.FindItemWithText%2A> -Methode können Sie eine Text Suche für eine <xref:System.Windows.Forms.ListView> in der Listen-oder Detailansicht ausführen, wenn eine Such Zeichenfolge und ein optionaler Start-und endIndex angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d91ed-105">The <xref:System.Windows.Forms.ListView.FindItemWithText%2A> method allows you to perform a text search on a <xref:System.Windows.Forms.ListView> in list or details view, given a search string and an optional starting and ending index.</span></span> <span data-ttu-id="d91ed-106">Im Gegensatz dazu ermöglicht die- <xref:System.Windows.Forms.ListView.FindNearestItem%2A> Methode das Auffinden eines Elements in einem <xref:System.Windows.Forms.ListView> in-Symbol oder einer Kachel Ansicht, wenn ein Satz von x-und y-Koordinaten und eine zu durchsuchende Richtung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d91ed-106">In contrast, the <xref:System.Windows.Forms.ListView.FindNearestItem%2A> method allows you to find an item in a <xref:System.Windows.Forms.ListView> in icon or tile view, given a set of x- and y-coordinates and a direction to search.</span></span>  
  
### <a name="to-find-an-item-using-text"></a><span data-ttu-id="d91ed-107">So suchen Sie ein Element mithilfe von Text</span><span class="sxs-lookup"><span data-stu-id="d91ed-107">To find an item using text</span></span>  
  
1. <span data-ttu-id="d91ed-108">Erstellen <xref:System.Windows.Forms.ListView> Sie ein-Objekt, bei dem die- <xref:System.Windows.Forms.ListView.View%2A> Eigenschaft auf oder festgelegt <xref:System.Windows.Forms.View.Details> <xref:System.Windows.Forms.View.List> ist, und füllen Sie dann <xref:System.Windows.Forms.ListView> mit Elementen.</span><span class="sxs-lookup"><span data-stu-id="d91ed-108">Create a <xref:System.Windows.Forms.ListView> with the <xref:System.Windows.Forms.ListView.View%2A> property set to <xref:System.Windows.Forms.View.Details> or <xref:System.Windows.Forms.View.List>, and then populate the <xref:System.Windows.Forms.ListView> with items.</span></span>  
  
2. <span data-ttu-id="d91ed-109">Wenden Sie die- <xref:System.Windows.Forms.ListView.FindItemWithText%2A> Methode an, und übergeben Sie den Text des Elements, das Sie suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="d91ed-109">Call the <xref:System.Windows.Forms.ListView.FindItemWithText%2A> method, passing the text of the item you would like to find.</span></span>  
  
3. <span data-ttu-id="d91ed-110">Im folgenden Codebeispiel wird veranschaulicht, wie ein einfaches erstellt <xref:System.Windows.Forms.ListView> , mit Elementen aufgefüllt und die Texteingabe des Benutzers verwendet wird, um ein Element in der Liste zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d91ed-110">The following code example demonstrates how to create a basic <xref:System.Windows.Forms.ListView>, populate it with items, and use text input from the user to find an item in the list.</span></span>  
  
 [!code-cpp[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/cpp/form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/VB/form1.vb#1)]  
  
### <a name="to-find-an-item-using-x--and-y-coordinates"></a><span data-ttu-id="d91ed-111">So suchen Sie ein Element mit x-und y-Koordinaten</span><span class="sxs-lookup"><span data-stu-id="d91ed-111">To find an item using x- and y-coordinates</span></span>  
  
1. <span data-ttu-id="d91ed-112">Erstellen <xref:System.Windows.Forms.ListView> Sie ein-Objekt, bei dem die- <xref:System.Windows.Forms.View> Eigenschaft auf oder festgelegt <xref:System.Windows.Forms.View.SmallIcon> <xref:System.Windows.Forms.View.LargeIcon> ist, und füllen Sie dann <xref:System.Windows.Forms.ListView> mit Elementen.</span><span class="sxs-lookup"><span data-stu-id="d91ed-112">Create a <xref:System.Windows.Forms.ListView> with the <xref:System.Windows.Forms.View> property set to <xref:System.Windows.Forms.View.SmallIcon> or <xref:System.Windows.Forms.View.LargeIcon>, and then populate the <xref:System.Windows.Forms.ListView> with items.</span></span>  
  
2. <span data-ttu-id="d91ed-113">Nennen <xref:System.Windows.Forms.ListView.FindNearestItem%2A> Sie die-Methode, und übergeben Sie die gewünschten x-und y-Koordinaten sowie die Richtung, die Sie durchsuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="d91ed-113">Call the <xref:System.Windows.Forms.ListView.FindNearestItem%2A> method, passing the desired x- and y-coordinates and the direction you would like to search.</span></span>  
  
3. <span data-ttu-id="d91ed-114">Im folgenden Codebeispiel wird veranschaulicht, wie ein Basis Symbol erstellt <xref:System.Windows.Forms.ListView> , mit Elementen aufgefüllt und das-Ereignis aufgezeichnet wird, <xref:System.Windows.Forms.Control.MouseDown> um das nächste Element in der nach-oben-Richtung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d91ed-114">The following code example demonstrates how to create a basic icon <xref:System.Windows.Forms.ListView>, populate it with items, and capture the <xref:System.Windows.Forms.Control.MouseDown> event to find the nearest item in the up direction.</span></span>  
  
 [!code-cpp[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/cpp/form1.cpp#2)]
 [!code-csharp[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/CS/form1.cs#2)]
 [!code-vb[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/VB/form1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="d91ed-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d91ed-115">See also</span></span>

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.FindItemWithText%2A>
- <xref:System.Windows.Forms.ListView.FindNearestItem%2A>
- [<span data-ttu-id="d91ed-116">ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d91ed-116">ListView Control</span></span>](listview-control-windows-forms.md)
- [<span data-ttu-id="d91ed-117">Übersicht über das ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d91ed-117">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
- [<span data-ttu-id="d91ed-118">Vorgehensweise: Hinzufügen und Entfernen von Elementen mit dem ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d91ed-118">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
