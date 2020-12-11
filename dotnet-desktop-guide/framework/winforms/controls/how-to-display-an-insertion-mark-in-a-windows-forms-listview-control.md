---
title: Einfügemarke im ListView-Steuerelement anzeigen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ListView control [Windows Forms], drag operations
- graphics [Windows Forms], insertion marks
- drop and drag [Windows Forms], insertion marks
- insertion marks
ms.assetid: 88d0a15b-25fd-4dc3-a685-297351311940
ms.openlocfilehash: eeae51223a21baaf4d2412de2ce11d0c6cbcae27
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976517"
---
# <a name="how-to-display-an-insertion-mark-in-a-windows-forms-listview-control"></a><span data-ttu-id="4a7b7-102">Vorgehensweise: Anzeigen einer Einfügemarke in einem ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4a7b7-102">How to: Display an Insertion Mark in a Windows Forms ListView Control</span></span>
<span data-ttu-id="4a7b7-103">Die Einfügemarke im <xref:System.Windows.Forms.ListView>-Steuerelement zeigt Benutzern die Stelle an, an der mit der Maus gezogene Elemente eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-103">The insertion mark in the <xref:System.Windows.Forms.ListView> control shows users the point where dragged items will be inserted.</span></span> <span data-ttu-id="4a7b7-104">Wenn ein Benutzer ein Element an eine Stelle zwischen zwei anderen Elementen zieht, gibt die Einfügemarke die erwartete neue Position des Elements an.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-104">When a user drags an item to a point between two other items, the insertion mark shows the item's expected new location.</span></span>  
  
 <span data-ttu-id="4a7b7-105">In der folgenden Abbildung ist eine Einfügemarke dargestellt:</span><span class="sxs-lookup"><span data-stu-id="4a7b7-105">The following image shows an insertion mark:</span></span>  
  
 <span data-ttu-id="4a7b7-106">![Screenshot, der eine ListView-Einfügemarke anzeigt.](./media/how-to-display-an-insertion-mark-in-a-windows-forms-listview-control/listview-insertion-mark.gif "Einfügemarkelistview")</span><span class="sxs-lookup"><span data-stu-id="4a7b7-106">![Screenshot that shows a ListView insertion mark.](./media/how-to-display-an-insertion-mark-in-a-windows-forms-listview-control/listview-insertion-mark.gif "ListViewInsertion")</span></span>  
  
 <span data-ttu-id="4a7b7-107">Im folgenden Codebeispiel wird die Verwendung dieser Funktion veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-107">The following code example demonstrates how to use this feature.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4a7b7-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4a7b7-108">Example</span></span>  
 [!code-cpp[System.Windows.Forms.ListView.InsertionMark#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListView.InsertionMark/CPP/listviewinsertionmarkexample.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListView.InsertionMark#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.InsertionMark/CS/listviewinsertionmarkexample.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.InsertionMark#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.InsertionMark/VB/listviewinsertionmarkexample.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="4a7b7-109">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="4a7b7-109">Compiling the Code</span></span>  
 <span data-ttu-id="4a7b7-110">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4a7b7-110">This example requires:</span></span>  
  
- <span data-ttu-id="4a7b7-111">Verweise auf die Assemblys "System" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="4a7b7-111">References to the System and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a7b7-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a7b7-112">See also</span></span>

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.InsertionMark%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ListViewInsertionMark>
- [<span data-ttu-id="4a7b7-113">ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="4a7b7-113">ListView Control</span></span>](listview-control-windows-forms.md)
- [<span data-ttu-id="4a7b7-114">Übersicht über das ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="4a7b7-114">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
- [<span data-ttu-id="4a7b7-115">Exemplarische Vorgehensweise: Ausführen von Drag &amp; Drop-Operationen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4a7b7-115">Walkthrough: Performing a Drag-and-Drop Operation in Windows Forms</span></span>](../advanced/walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md)
