---
title: 'Vorgehensweise: Erstellen eines MDI-Formulars mit ToolStripPanel-Steuerelementen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStripPanel control [Windows Forms]
- MDI [Windows Forms], creating forms
- multiple document interface forms
- MDI forms [Windows Forms]
- ToolStrip control [Windows Forms]
- MDI forms [Windows Forms], creating
ms.assetid: d198ef8e-f7c4-4b3f-a7f5-ce858cb90cec
ms.openlocfilehash: 4dae528d69c6c08c2005fd30d7d16fafa67afb53
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976332"
---
# <a name="how-to-create-an-mdi-form-with-toolstrippanel-controls"></a><span data-ttu-id="359d8-102">Vorgehensweise: Erstellen eines MDI-Formulars mit ToolStripPanel-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="359d8-102">How to: Create an MDI Form with ToolStripPanel Controls</span></span>
<span data-ttu-id="359d8-103">Sie können ein Formular mit einer mehrfachen Dokumentschnittstelle (MDI) erstellen, das mit <xref:System.Windows.Forms.ToolStrip>-Steuerelementen auf allen vier Seiten umrahmt wird.</span><span class="sxs-lookup"><span data-stu-id="359d8-103">You can create a multiple document interface (MDI) form that has <xref:System.Windows.Forms.ToolStrip> controls framing it on all four sides.</span></span>  
  
## <a name="example"></a><span data-ttu-id="359d8-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="359d8-104">Example</span></span>  
 <span data-ttu-id="359d8-105">Im folgenden Codebeispiel wird gezeigt, wie Sie angedockte <xref:System.Windows.Forms.ToolStripPanel>-Steuerelemente verwenden, um ein MDI-Fenster mit vier <xref:System.Windows.Forms.ToolStrip>-Steuerelementen einzurahmen.</span><span class="sxs-lookup"><span data-stu-id="359d8-105">The following code example demonstrates how to use docked <xref:System.Windows.Forms.ToolStripPanel> controls to frame an MDI window with four <xref:System.Windows.Forms.ToolStrip> controls.</span></span>  
  
 <span data-ttu-id="359d8-106">In diesem Beispiel fügt die <xref:System.Windows.Forms.ToolStripPanel.Join%2A>-Methode die <xref:System.Windows.Forms.ToolStrip>-Steuerelemente an die entsprechenden <xref:System.Windows.Forms.ToolStripPanel>-Steuerelemente an.</span><span class="sxs-lookup"><span data-stu-id="359d8-106">In the example, the <xref:System.Windows.Forms.ToolStripPanel.Join%2A> method attaches the <xref:System.Windows.Forms.ToolStrip> controls to the corresponding <xref:System.Windows.Forms.ToolStripPanel> controls.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#10)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#10)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="359d8-107">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="359d8-107">Compiling the Code</span></span>  
 <span data-ttu-id="359d8-108">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="359d8-108">This example requires:</span></span>  
  
- <span data-ttu-id="359d8-109">Verweise auf die Assemblys ""System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="359d8-109">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="359d8-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="359d8-110">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripPanel>
- <xref:System.Windows.Forms.ToolStripPanel.Join%2A>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [<span data-ttu-id="359d8-111">ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="359d8-111">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
