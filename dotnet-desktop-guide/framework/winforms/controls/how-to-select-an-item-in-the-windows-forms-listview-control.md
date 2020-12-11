---
title: Wählen Sie ein Element im ListView-Steuerelement aus.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lists [Windows Forms], selecting items
- ListView control [Windows Forms], selecting items
- selection [Windows Forms], in list views
- list views [Windows Forms], selecting items
ms.assetid: ddea918e-1ddf-47f4-bd09-1e9b4c9d0c39
ms.openlocfilehash: 57e985af9d0347510d7d7782f68d5b414d36e077
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974747"
---
# <a name="how-to-select-an-item-in-the-windows-forms-listview-control"></a><span data-ttu-id="01b75-102">Vorgehensweise: Auswählen eines Elements im ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="01b75-102">How to: Select an Item in the Windows Forms ListView Control</span></span>
<span data-ttu-id="01b75-103">In diesem Beispiel wird veranschaulicht, wie ein Element in einem Windows Forms-Steuerelement Programm gesteuert ausgewählt wird <xref:System.Windows.Forms.ListView> .</span><span class="sxs-lookup"><span data-stu-id="01b75-103">This example demonstrates how to programmatically select an item in a Windows Forms <xref:System.Windows.Forms.ListView> control.</span></span> <span data-ttu-id="01b75-104">Wenn Sie ein Element Programm gesteuert auswählen, wird der Fokus auf das Steuerelement nicht automatisch geändert <xref:System.Windows.Forms.ListView> .</span><span class="sxs-lookup"><span data-stu-id="01b75-104">Selecting an item programmatically does not automatically change the focus to the <xref:System.Windows.Forms.ListView> control.</span></span> <span data-ttu-id="01b75-105">Aus diesem Grund möchten Sie das Element in der Regel auch als Fokus festlegen, wenn Sie ein Element auswählen.</span><span class="sxs-lookup"><span data-stu-id="01b75-105">For this reason, you will typically also want to set the item as focused when selecting an item.</span></span>  
  
## <a name="example"></a><span data-ttu-id="01b75-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="01b75-106">Example</span></span>  
 [!code-csharp[System.Windows.Forms.ListView.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Misc/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.Misc/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="01b75-107">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="01b75-107">Compiling the Code</span></span>  
 <span data-ttu-id="01b75-108">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="01b75-108">This example requires:</span></span>  
  
- <span data-ttu-id="01b75-109">Ein- <xref:System.Windows.Forms.ListView> Steuer `listView1` Element mit dem Namen, das mindestens ein Element enthält.</span><span class="sxs-lookup"><span data-stu-id="01b75-109">A <xref:System.Windows.Forms.ListView> control named `listView1` that contains at least one item.</span></span>  
  
- <span data-ttu-id="01b75-110">Verweise auf die Namespaces <xref:System?displayProperty=nameWithType> und <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="01b75-110">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> namespaces.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01b75-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01b75-111">See also</span></span>

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListViewItem.Selected%2A?displayProperty=nameWithType>
