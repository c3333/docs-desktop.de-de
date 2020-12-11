---
title: Anzeigen von unter Elementen in Spalten mit dem ListView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- list items
- Details view
- ListView control [Windows Forms], adding ListSubItems
- subitems
ms.assetid: e465f044-cde7-4fd9-a687-788a73a0f554
ms.openlocfilehash: 5c6d807410ad4ee0198d6334844bd65b148edff4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976505"
---
# <a name="how-to-display-subitems-in-columns-with-the-windows-forms-listview-control"></a><span data-ttu-id="e704c-102">Vorgehensweise: Anzeigen von Unterelementen in Spalten mit dem ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e704c-102">How to: Display Subitems in Columns with the Windows Forms ListView Control</span></span>
<span data-ttu-id="e704c-103">Das Windows Forms <xref:System.Windows.Forms.ListView> Steuerelement kann für jedes Element in der Detailansicht zusätzlichen Text oder unter Elemente anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e704c-103">The Windows Forms <xref:System.Windows.Forms.ListView> control can display additional text, or subitems, for each item in the Details view.</span></span> <span data-ttu-id="e704c-104">In der ersten Spalte wird der Element Text angezeigt, z. b. eine Mitarbeiternummer.</span><span class="sxs-lookup"><span data-stu-id="e704c-104">The first column displays the item text, for example an employee number.</span></span> <span data-ttu-id="e704c-105">In den zweiten, dritten und nachfolgenden Spalten werden das erste, zweite und nachfolgende zugehörige Unterelement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e704c-105">The second, third, and subsequent columns display the first, second, and subsequent associated subitems.</span></span>  
  
### <a name="to-add-subitems-to-a-list-item"></a><span data-ttu-id="e704c-106">So fügen Sie einem Listenelement unter Elemente hinzu</span><span class="sxs-lookup"><span data-stu-id="e704c-106">To add subitems to a list item</span></span>  
  
1. <span data-ttu-id="e704c-107">Fügen Sie alle benötigten Spalten hinzu.</span><span class="sxs-lookup"><span data-stu-id="e704c-107">Add any columns needed.</span></span> <span data-ttu-id="e704c-108">Da in der ersten Spalte die-Eigenschaft des Elements angezeigt wird <xref:System.Windows.Forms.ListView.Text%2A> , benötigen Sie eine weitere Spalte, als untergeordnete Elemente vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e704c-108">Because the first column will display the item's <xref:System.Windows.Forms.ListView.Text%2A> property, you need one more column than there are subitems.</span></span> <span data-ttu-id="e704c-109">Weitere Informationen zum Hinzufügen von Spalten finden Sie unter Gewusst [wie: Hinzufügen von Spalten zum Windows Forms ListView-Steuer](how-to-add-columns-to-the-windows-forms-listview-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="e704c-109">For more information on adding columns, see [How to: Add Columns to the Windows Forms ListView Control](how-to-add-columns-to-the-windows-forms-listview-control.md).</span></span>  
  
2. <span data-ttu-id="e704c-110">Ruft die-Methode der-Auflistung auf, die <xref:System.Windows.Forms.ListViewItem.ListViewSubItemCollection.Add%2A> von der- <xref:System.Windows.Forms.ListViewItem.SubItems%2A> Eigenschaft eines Elements zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e704c-110">Call the <xref:System.Windows.Forms.ListViewItem.ListViewSubItemCollection.Add%2A> method of the collection returned by the <xref:System.Windows.Forms.ListViewItem.SubItems%2A> property of an item.</span></span> <span data-ttu-id="e704c-111">Im folgenden Codebeispiel werden der Mitarbeiter Name und die Abteilung für ein Listenelement festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e704c-111">The code example below sets the employee name and department for a list item.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#61)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#61)]  
  
## <a name="see-also"></a><span data-ttu-id="e704c-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e704c-112">See also</span></span>

- [<span data-ttu-id="e704c-113">Übersicht über das ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e704c-113">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
- [<span data-ttu-id="e704c-114">Vorgehensweise: Hinzufügen und Entfernen von Elementen mit dem ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e704c-114">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
- [<span data-ttu-id="e704c-115">Vorgehensweise: Hinzufügen von Spalten zum ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e704c-115">How to: Add Columns to the Windows Forms ListView Control</span></span>](how-to-add-columns-to-the-windows-forms-listview-control.md)
- [<span data-ttu-id="e704c-116">Vorgehensweise: Anzeigen von Symbolen für das ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e704c-116">How to: Display Icons for the Windows Forms ListView Control</span></span>](how-to-display-icons-for-the-windows-forms-listview-control.md)
- [<span data-ttu-id="e704c-117">Vorgehensweise: Hinzufügen von benutzerdefinierten Daten zu einem TreeView- oder ListView-Steuerelement (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="e704c-117">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](add-custom-information-to-a-treeview-or-listview-control-wf.md)
