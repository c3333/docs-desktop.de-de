---
title: 'Vorgehensweise: Behandeln des Opening-Ereignisses von ContextMenuStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ContextMenuStrip control [Windows Forms]
- context menus [Windows Forms], event handling
- ToolStrip control [Windows Forms]
- event handling [Windows Forms], context menus
- shortcut menus [Windows Forms], event handling
ms.assetid: b661b3dd-7815-4cc2-a1aa-a9a391ab3427
ms.openlocfilehash: 3001480959ef90cb31048cbcf70aeff1632979fb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976297"
---
# <a name="how-to-handle-the-contextmenustrip-opening-event"></a><span data-ttu-id="7fb00-102">Vorgehensweise: Behandeln des Opening-Ereignisses von ContextMenuStrip</span><span class="sxs-lookup"><span data-stu-id="7fb00-102">How to: Handle the ContextMenuStrip Opening Event</span></span>
<span data-ttu-id="7fb00-103">Sie können das Verhalten des Steuer Elements anpassen, <xref:System.Windows.Forms.ContextMenuStrip> indem Sie das- <xref:System.Windows.Forms.ToolStripDropDown.Opening> Ereignis behandeln.</span><span class="sxs-lookup"><span data-stu-id="7fb00-103">You can customize the behavior of your <xref:System.Windows.Forms.ContextMenuStrip> control by handling the <xref:System.Windows.Forms.ToolStripDropDown.Opening> event.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7fb00-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7fb00-104">Example</span></span>  
 <span data-ttu-id="7fb00-105">Im folgenden Codebeispiel wird veranschaulicht, wie das-Ereignis behandelt wird <xref:System.Windows.Forms.ToolStripDropDown.Opening> .</span><span class="sxs-lookup"><span data-stu-id="7fb00-105">The following code example demonstrates how to handle the <xref:System.Windows.Forms.ToolStripDropDown.Opening> event.</span></span> <span data-ttu-id="7fb00-106">Der-Ereignishandler fügt einem-Steuerelement dynamisch Elemente hinzu <xref:System.Windows.Forms.ContextMenuStrip> .</span><span class="sxs-lookup"><span data-stu-id="7fb00-106">The event handler adds items dynamically to a <xref:System.Windows.Forms.ContextMenuStrip> control.</span></span> <span data-ttu-id="7fb00-107">Das gesamte Codebeispiel finden Sie unter Gewusst [wie: Dynamisches Hinzufügen von ToolStrip-Elementen](how-to-add-toolstrip-items-dynamically.md).</span><span class="sxs-lookup"><span data-stu-id="7fb00-107">For the complete code example, see [How to: Add ToolStrip Items Dynamically](how-to-add-toolstrip-items-dynamically.md).</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#42)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#42)]  
  
 <span data-ttu-id="7fb00-108">Legen Sie die- <xref:System.ComponentModel.CancelEventArgs.Cancel%2A?displayProperty=nameWithType> Eigenschaft auf fest `true` , um das Öffnen des Menüs zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7fb00-108">Set the <xref:System.ComponentModel.CancelEventArgs.Cancel%2A?displayProperty=nameWithType> property to `true` to prevent the menu from opening.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7fb00-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fb00-109">See also</span></span>

- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.ComponentModel.CancelEventArgs.Cancel%2A>
- <xref:System.Windows.Forms.ToolStripDropDown>
- [<span data-ttu-id="7fb00-110">ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7fb00-110">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
