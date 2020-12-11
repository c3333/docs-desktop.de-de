---
title: 'Vorgehensweise: Aktivieren des Aktivierungs- und Bildrands in ContextMenuStrip-Steuerelementen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ShowCheckMargin property [Windows Forms]
- ShowImageMargin property [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
ms.assetid: eb584e71-59da-4012-aaca-dbe1c7c7a156
ms.openlocfilehash: bf8440704a7e457d0c987c933cc26e0e12e9565f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976500"
---
# <a name="how-to-enable-check-margins-and-image-margins-in-contextmenustrip-controls"></a><span data-ttu-id="7f029-102">Vorgehensweise: Aktivieren des Aktivierungs- und Bildrands in ContextMenuStrip-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="7f029-102">How to: Enable Check Margins and Image Margins in ContextMenuStrip Controls</span></span>
<span data-ttu-id="7f029-103">Sie können die <xref:System.Windows.Forms.ToolStripMenuItem>-Objekte in Ihrem <xref:System.Windows.Forms.MenuStrip>-Steuerelement mit Häkchen und benutzerdefinierten Bildern anpassen.</span><span class="sxs-lookup"><span data-stu-id="7f029-103">You can customize the <xref:System.Windows.Forms.ToolStripMenuItem> objects in your <xref:System.Windows.Forms.MenuStrip> control with check marks and custom images.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7f029-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7f029-104">Example</span></span>  
 <span data-ttu-id="7f029-105">Im folgenden Codebeispiel wird veranschaulicht, wie Menüelemente erstellt werden, die Häkchen und benutzerdefinierte Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="7f029-105">The following code example demonstrates how to create menu items that have check marks and custom images.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#60](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#60)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#60](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#60)]  
  
 <span data-ttu-id="7f029-106">Legen Sie die Eigenschaften <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowCheckMargin%2A?displayProperty=nameWithType> und <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowImageMargin%2A?displayProperty=nameWithType> fest, um anzugeben, wann Häkchen und benutzerdefinierte Bilder in den Menüelementen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7f029-106">Set the <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowCheckMargin%2A?displayProperty=nameWithType> and <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowImageMargin%2A?displayProperty=nameWithType> properties to specify when check marks and custom images appear in your menu items.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="7f029-107">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="7f029-107">Compiling the Code</span></span>  
 <span data-ttu-id="7f029-108">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7f029-108">This example requires:</span></span>  
  
- <span data-ttu-id="7f029-109">Verweise auf die Assemblys "System.Design", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="7f029-109">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f029-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f029-110">See also</span></span>

- <xref:System.Windows.Forms.ToolStripMenuItem>
- <xref:System.Windows.Forms.ToolStripDropDownMenu>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- [<span data-ttu-id="7f029-111">ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7f029-111">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
