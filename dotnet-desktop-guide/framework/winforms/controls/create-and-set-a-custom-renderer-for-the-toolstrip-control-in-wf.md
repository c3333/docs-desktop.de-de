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
# <a name="how-to-create-and-set-a-custom-renderer-for-the-toolstrip-control-in-windows-forms"></a>Vorgehensweise: Erstellen und Festlegen eines benutzerdefinierten Renderers für das ToolStrip-Steuerelement in Windows Forms
<xref:System.Windows.Forms.ToolStrip> Steuerelemente erleichtern die Unterstützung von Designs und Stilen. Sie können ein vollständiges benutzerdefiniertes Aussehen und Verhalten (Aussehen und Verhalten) erzielen, indem Sie entweder die- <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> Eigenschaft oder die- <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> Eigenschaft auf einen benutzerdefinierten Renderer festlegen.  
  
 Sie können jedem einzelnen-,-,-oder-Steuerelement Renderer zuweisen <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.MenuStrip> <xref:System.Windows.Forms.ContextMenuStrip> <xref:System.Windows.Forms.StatusStrip> , oder Sie können die-Eigenschaft verwenden, <xref:System.Windows.Forms.ToolStripManager.Renderer%2A> um alle-Objekte zu beeinflussen, indem Sie die- <xref:System.Windows.Forms.ToolStrip.RenderMode%2A?displayProperty=nameWithType> Eigenschaft auf festlegen <xref:System.Windows.Forms.ToolStripRenderMode.ManagerRenderMode?displayProperty=nameWithType> .  
  
> [!NOTE]
> <xref:System.Windows.Forms.ToolStrip.RenderMode%2A> gibt <xref:System.Windows.Forms.ToolStripRenderMode.Custom> nur dann zurück, wenn der Wert von <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> nicht ist `null` .  
  
### <a name="to-create-a-custom-renderer"></a>So erstellen Sie einen benutzerdefinierten Renderer  
  
1. Erweitern Sie die- <xref:System.Windows.Forms.ToolStripRenderer> Klasse.  
  
2. Implementieren Sie das gewünschte benutzerdefinierte Rendering, indem Sie die entsprechenden Optionen *überschreiben.* members  
  
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
  
### <a name="to-set-the-custom-renderer-to-be-the-current-renderer"></a>So legen Sie den benutzerdefinierten Renderer als aktuellen Renderer fest  
  
1. Um den benutzerdefinierten Renderer für einen festzulegen <xref:System.Windows.Forms.ToolStrip> , legen Sie die- <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> Eigenschaft auf den benutzerdefinierten Renderer fest.  
  
    ```vb  
    toolStrip1.Renderer = New RedTextRenderer()  
    ```  
  
    ```csharp  
    toolStrip1.Renderer = new RedTextRenderer();  
    ```  
  
2. Wenn Sie den benutzerdefinierten Renderer für alle <xref:System.Windows.Forms.ToolStrip> in der Anwendung enthaltenen Klassen festlegen möchten, legen Sie die <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> -Eigenschaft auf den benutzerdefinierten Renderer fest, und legen Sie die- <xref:System.Windows.Forms.ToolStrip.RenderMode%2A> Eigenschaft auf fest <xref:System.Windows.Forms.ToolStripRenderMode.ManagerRenderMode> .  
  
    ```vb  
    toolStrip1.RenderMode = ToolStripRenderMode.ManagerRenderMode  
    ToolStripManager.Renderer = New RedTextRenderer()  
    ```  
  
    ```csharp  
    toolStrip1.RenderMode = ToolStripRenderMode.ManagerRenderMode;  
    ToolStripManager.Renderer = new RedTextRenderer();  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStripManager.Renderer%2A>
- <xref:System.Windows.Forms.ToolStripRenderer>
- <xref:System.Windows.Forms.ToolStrip.RenderMode%2A>
- [Übersicht über das ToolStrip-Steuerelement](toolstrip-control-overview-windows-forms.md)
- [Architektur des ToolStrip-Steuerelements](toolstrip-control-architecture.md)
- [Zusammenfassung der ToolStrip-Technologie](toolstrip-technology-summary.md)
