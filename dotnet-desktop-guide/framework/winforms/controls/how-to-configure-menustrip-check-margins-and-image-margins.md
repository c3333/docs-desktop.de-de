---
title: 'Vorgehensweise: Konfigurieren des Aktivierungs- und Bildrands von MenuStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- margins [Windows Forms], setting in MenuStrip controls
- menus [Windows Forms], setting margins
- MenuStrip control [Windows Forms], configuring check and image margins
ms.assetid: 45a9075d-4bea-4ce2-9b2c-7619aa39f8ce
ms.openlocfilehash: fa099012fa77daacd1f428e64abd662ee1738f84
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975701"
---
# <a name="how-to-configure-menustrip-check-margins-and-image-margins"></a><span data-ttu-id="6c1e4-102">Vorgehensweise: Konfigurieren des Aktivierungs- und Bildrands von MenuStrip</span><span class="sxs-lookup"><span data-stu-id="6c1e4-102">How to: Configure MenuStrip Check Margins and Image Margins</span></span>
<span data-ttu-id="6c1e4-103">Sie können eine <xref:System.Windows.Forms.MenuStrip>-Instanz anpassen, indem Sie die <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowImageMargin%2A>- und die <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowCheckMargin%2A>-Eigenschaft in verschiedenen Kombinationen festlegen.</span><span class="sxs-lookup"><span data-stu-id="6c1e4-103">You can customize a <xref:System.Windows.Forms.MenuStrip> by setting the <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowImageMargin%2A> and <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowCheckMargin%2A> properties in various combinations.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6c1e4-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6c1e4-104">Example</span></span>  
 <span data-ttu-id="6c1e4-105">Im folgenden Codebeispiel wird veranschaulicht, wie die <xref:System.Windows.Forms.ContextMenuStrip>-Aktivierungs-und -Bildränder festgelegt und angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="6c1e4-105">The following code example demonstrates how to set and customize the <xref:System.Windows.Forms.ContextMenuStrip> check margins and image margins.</span></span> <span data-ttu-id="6c1e4-106">Die Vorgehensweise ist für eine <xref:System.Windows.Forms.ContextMenuStrip>- oder eine <xref:System.Windows.Forms.MenuStrip>-Instanz identisch.</span><span class="sxs-lookup"><span data-stu-id="6c1e4-106">The procedure is the same for a <xref:System.Windows.Forms.ContextMenuStrip> or a <xref:System.Windows.Forms.MenuStrip>.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#60](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#60)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#60](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#60)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="6c1e4-107">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="6c1e4-107">Compiling the Code</span></span>  
 <span data-ttu-id="6c1e4-108">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6c1e4-108">This example requires:</span></span>  
  
- <span data-ttu-id="6c1e4-109">Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="6c1e4-109">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c1e4-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c1e4-110">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.ToolStripDropDown>
- [<span data-ttu-id="6c1e4-111">ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6c1e4-111">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
- [<span data-ttu-id="6c1e4-112">Vorgehensweise: Aktivieren des Aktivierungs- und Bildrands in ContextMenuStrip-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="6c1e4-112">How to: Enable Check Margins and Image Margins in ContextMenuStrip Controls</span></span>](how-to-enable-check-margins-and-image-margins-in-contextmenustrip-controls.md)
