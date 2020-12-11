---
title: 'Vorgehensweise: Festlegen des ToolStrip-Renderers für eine Anwendung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Renderer property [Windows Forms]
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
- toolbars [Windows Forms], customizing
ms.assetid: 46acef3e-9844-4ae8-9a2e-3006fe99cadf
ms.openlocfilehash: c9250b723e68ac97d1486a896392bf64c66cdfbc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976758"
---
# <a name="how-to-set-the-toolstrip-renderer-for-an-application"></a><span data-ttu-id="88ce0-102">Vorgehensweise: Festlegen des ToolStrip-Renderers für eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="88ce0-102">How to: Set the ToolStrip Renderer for an Application</span></span>
<span data-ttu-id="88ce0-103">Sie können die Darstellung von <xref:System.Windows.Forms.ToolStrip>-Steuerelementen einzeln oder für alle <xref:System.Windows.Forms.ToolStrip>-Steuerelemente in Ihrer Anwendung anpassen.</span><span class="sxs-lookup"><span data-stu-id="88ce0-103">You can customize the appearance of your <xref:System.Windows.Forms.ToolStrip> controls individually or for all the <xref:System.Windows.Forms.ToolStrip> controls in your application.</span></span>  
  
## <a name="example"></a><span data-ttu-id="88ce0-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="88ce0-104">Example</span></span>  
 <span data-ttu-id="88ce0-105">Im folgenden Codebeispiel wird veranschaulicht, wie ein benutzerdefinierter Renderer selektiv auf ein <xref:System.Windows.Forms.ToolStrip>-Steuerelement und ein <xref:System.Windows.Forms.MenuStrip>-Steuerelement angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="88ce0-105">The following code example demonstrates how to selectively apply a custom renderer to a <xref:System.Windows.Forms.ToolStrip> control and a <xref:System.Windows.Forms.MenuStrip> control.</span></span>  
  
 <span data-ttu-id="88ce0-106">Um dieses Codebeispiel zu verwenden, kompilieren Sie die Anwendung, führen Sie diese aus, und wählen Sie dann den Bereich des benutzerdefinierten Renderings im <xref:System.Windows.Forms.ComboBox>-Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="88ce0-106">To use this code example, compile and run the application, and then select the scope of the custom rending from the <xref:System.Windows.Forms.ComboBox> control.</span></span> <span data-ttu-id="88ce0-107">Klicken Sie auf **Übernehmen**, um den Renderer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="88ce0-107">Click **Apply** to set the renderer.</span></span>  
  
 <span data-ttu-id="88ce0-108">Um das benutzerdefinierte Rendering von Menü Elementen anzuzeigen, wählen Sie die <xref:System.Windows.Forms.MenuStrip> Option im Steuerelement aus <xref:System.Windows.Forms.ComboBox> , klicken Sie auf über **nehmen,** und öffnen Sie dann das Menü Element **Datei** .</span><span class="sxs-lookup"><span data-stu-id="88ce0-108">To see custom menu item rendering, select the <xref:System.Windows.Forms.MenuStrip> option from the <xref:System.Windows.Forms.ComboBox> control, click **Apply**, and then open the **File** menu item.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#70](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#70)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#70](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#70)]  
  
 <span data-ttu-id="88ce0-109">Legen Sie die <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType>-Eigenschaft fest, damit ein benutzerdefinierter Renderer auf alle <xref:System.Windows.Forms.ToolStrip>-Steuerelemente in Ihrer Anwendung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="88ce0-109">Set the <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> property to apply a custom renderer to all the <xref:System.Windows.Forms.ToolStrip> controls in your application.</span></span>  
  
 <span data-ttu-id="88ce0-110">Legen Sie die <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType>-Eigenschaft fest, damit ein benutzerdefinierter Renderer auf ein einzelnes <xref:System.Windows.Forms.ToolStrip>-Steuerelement angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="88ce0-110">Set the <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> property to apply a custom renderer to an individual <xref:System.Windows.Forms.ToolStrip> control.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="88ce0-111">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="88ce0-111">Compiling the Code</span></span>  
 <span data-ttu-id="88ce0-112">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="88ce0-112">This example requires:</span></span>  
  
- <span data-ttu-id="88ce0-113">Verweise auf die Assemblys "System.Design", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="88ce0-113">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="88ce0-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88ce0-114">See also</span></span>

- <xref:System.Windows.Forms.ToolStripManager>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripProfessionalRenderer>
- [<span data-ttu-id="88ce0-115">ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="88ce0-115">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
