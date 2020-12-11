---
title: 'Gewusst wie: Erstellen und Festlegen eines benutzerdefinierten Renderers für das ToolStrip-Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], custom rendering
- toolbars [Windows Forms], rendering
- examples [Windows Forms], toolbars
- ToolStrip control [Windows Forms], rendering
ms.assetid: 88a804ba-679f-4ba3-938a-0dc396199c5b
ms.openlocfilehash: 49db0d785155f19b7220ac64011eaf4253aaa7e9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972211"
---
# <a name="how-to-create-and-set-a-custom-renderer-for-the-toolstrip-control-in-windows-forms"></a><span data-ttu-id="7f3a1-102">Vorgehensweise: Erstellen und Festlegen eines benutzerdefinierten Renderers für das ToolStrip-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7f3a1-102">How to: Create and Set a Custom Renderer for the ToolStrip Control in Windows Forms</span></span>
<span data-ttu-id="7f3a1-103"><xref:System.Windows.Forms.ToolStrip> Steuerelemente erleichtern die Unterstützung von Designs und Stilen.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-103"><xref:System.Windows.Forms.ToolStrip> controls give easy support to themes and styles.</span></span> <span data-ttu-id="7f3a1-104">Sie können ein vollständiges benutzerdefiniertes Aussehen und Verhalten (Aussehen und Verhalten) erzielen, indem Sie entweder die- <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> Eigenschaft oder die- <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> Eigenschaft auf einen benutzerdefinierten Renderer festlegen.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-104">You can achieve completely custom appearance and behavior (look and feel) by setting either the <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> property or the <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> property to a custom renderer.</span></span>  
  
 <span data-ttu-id="7f3a1-105">Sie können jedem einzelnen-,-,-oder-Steuerelement Renderer zuweisen <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.MenuStrip> <xref:System.Windows.Forms.ContextMenuStrip> <xref:System.Windows.Forms.StatusStrip> , oder Sie können die-Eigenschaft verwenden, <xref:System.Windows.Forms.ToolStripManager.Renderer%2A> um alle-Objekte zu beeinflussen, indem Sie die- <xref:System.Windows.Forms.ToolStrip.RenderMode%2A?displayProperty=nameWithType> Eigenschaft auf festlegen <xref:System.Windows.Forms.ToolStripRenderMode.ManagerRenderMode?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="7f3a1-105">You can assign renderers to each individual <xref:System.Windows.Forms.ToolStrip>, <xref:System.Windows.Forms.MenuStrip>, <xref:System.Windows.Forms.ContextMenuStrip>, or <xref:System.Windows.Forms.StatusStrip> control, or you can use the <xref:System.Windows.Forms.ToolStripManager.Renderer%2A> property to affect all objects by setting the <xref:System.Windows.Forms.ToolStrip.RenderMode%2A?displayProperty=nameWithType> property to <xref:System.Windows.Forms.ToolStripRenderMode.ManagerRenderMode?displayProperty=nameWithType>.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7f3a1-106"><xref:System.Windows.Forms.ToolStrip.RenderMode%2A> gibt <xref:System.Windows.Forms.ToolStripRenderMode.Custom> nur dann zurück, wenn der Wert von <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> nicht ist `null` .</span><span class="sxs-lookup"><span data-stu-id="7f3a1-106"><xref:System.Windows.Forms.ToolStrip.RenderMode%2A> returns <xref:System.Windows.Forms.ToolStripRenderMode.Custom> only if the value of <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> is not `null`.</span></span>  
  
### <a name="to-create-a-custom-renderer"></a><span data-ttu-id="7f3a1-107">So erstellen Sie einen benutzerdefinierten Renderer</span><span class="sxs-lookup"><span data-stu-id="7f3a1-107">To create a custom renderer</span></span>  
  
1. <span data-ttu-id="7f3a1-108">Erweitern Sie die- <xref:System.Windows.Forms.ToolStripRenderer> Klasse.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-108">Extend the <xref:System.Windows.Forms.ToolStripRenderer> class.</span></span>  
  
2. <span data-ttu-id="7f3a1-109">Implementieren Sie das gewünschte benutzerdefinierte Rendering, indem Sie die entsprechenden Optionen *überschreiben.*</span><span class="sxs-lookup"><span data-stu-id="7f3a1-109">Implement desired custom rendering by overriding appropriate *On…*</span></span> <span data-ttu-id="7f3a1-110">members</span><span class="sxs-lookup"><span data-stu-id="7f3a1-110">members</span></span>  
  
    ```vb  
    Public Class RedTextRenderer  
        Inherits System.Windows.Forms.ToolStripRenderer  
        Protected Overrides Sub OnRenderItemText(ByVal e As _  
            ToolStripItemTextRenderEventArgs)
            e.TextColor = Color.Red  
            e.TextFont = New Font("Helvetica", 7, FontStyle.Bold)  
            MyBase.OnRenderItemText(e)  
        End Sub  
    End Class  
    ```  
  
    ```csharp  
    public class RedTextRenderer : _  
        System.Windows.Forms.ToolStripRenderer  
    {  
        protected override void _  
            OnRenderItemText(ToolStripItemTextRenderEventArgs e)  
        {  
            e.TextColor = Color.Red;  
            e.TextFont = new Font("Helvetica", 7, FontStyle.Bold);  
           base.OnRenderItemText(e);  
        }  
    }  
    ```  
  
### <a name="to-set-the-custom-renderer-to-be-the-current-renderer"></a><span data-ttu-id="7f3a1-111">So legen Sie den benutzerdefinierten Renderer als aktuellen Renderer fest</span><span class="sxs-lookup"><span data-stu-id="7f3a1-111">To set the custom renderer to be the current renderer</span></span>  
  
1. <span data-ttu-id="7f3a1-112">Um den benutzerdefinierten Renderer für einen festzulegen <xref:System.Windows.Forms.ToolStrip> , legen Sie die- <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> Eigenschaft auf den benutzerdefinierten Renderer fest.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-112">To set the custom renderer for one <xref:System.Windows.Forms.ToolStrip>, set the <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> property to the custom renderer.</span></span>  
  
    ```vb  
    toolStrip1.Renderer = New RedTextRenderer()  
    ```  
  
    ```csharp  
    toolStrip1.Renderer = new RedTextRenderer();  
    ```  
  
2. <span data-ttu-id="7f3a1-113">Wenn Sie den benutzerdefinierten Renderer für alle <xref:System.Windows.Forms.ToolStrip> in der Anwendung enthaltenen Klassen festlegen möchten, legen Sie die <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> -Eigenschaft auf den benutzerdefinierten Renderer fest, und legen Sie die- <xref:System.Windows.Forms.ToolStrip.RenderMode%2A> Eigenschaft auf fest <xref:System.Windows.Forms.ToolStripRenderMode.ManagerRenderMode> .</span><span class="sxs-lookup"><span data-stu-id="7f3a1-113">Or to set the custom renderer for all <xref:System.Windows.Forms.ToolStrip> classes contained in your application: Set the <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> property to the custom renderer and set the <xref:System.Windows.Forms.ToolStrip.RenderMode%2A> property to <xref:System.Windows.Forms.ToolStripRenderMode.ManagerRenderMode>.</span></span>  
  
    ```vb  
    toolStrip1.RenderMode = ToolStripRenderMode.ManagerRenderMode  
    ToolStripManager.Renderer = New RedTextRenderer()  
    ```  
  
    ```csharp  
    toolStrip1.RenderMode = ToolStripRenderMode.ManagerRenderMode;  
    ToolStripManager.Renderer = new RedTextRenderer();  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="7f3a1-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f3a1-114">See also</span></span>

- <xref:System.Windows.Forms.ToolStripManager.Renderer%2A>
- <xref:System.Windows.Forms.ToolStripRenderer>
- <xref:System.Windows.Forms.ToolStrip.RenderMode%2A>
- [<span data-ttu-id="7f3a1-115">Übersicht über das ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7f3a1-115">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
- [<span data-ttu-id="7f3a1-116">Architektur des ToolStrip-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="7f3a1-116">ToolStrip Control Architecture</span></span>](toolstrip-control-architecture.md)
- [<span data-ttu-id="7f3a1-117">Zusammenfassung der ToolStrip-Technologie</span><span class="sxs-lookup"><span data-stu-id="7f3a1-117">ToolStrip Technology Summary</span></span>](toolstrip-technology-summary.md)
