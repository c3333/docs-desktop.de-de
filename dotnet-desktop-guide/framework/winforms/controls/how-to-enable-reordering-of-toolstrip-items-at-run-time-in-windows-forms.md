---
title: 'Vorgehensweise: Aktivieren der Neuanordnung von ToolStrip-Elementen zur Laufzeit'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], examples
- examples [Windows Forms], toolbars
- toolbars [Windows Forms], rearranging controls
- ToolStrip control [Windows Forms], reordering items
ms.assetid: 8480b69a-379f-4dc2-8dcf-365ed93692b2
ms.openlocfilehash: 44b52bf997819f090569d08eb395d8af18f61370
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976501"
---
# <a name="how-to-enable-reordering-of-toolstrip-items-at-run-time-in-windows-forms"></a>Gewusst wie: Aktivieren der Neuanordnung von ToolStrip-Elementen zur Laufzeit in Windows Forms
Sie können es dem Benutzer ermöglichen, Steuer <xref:System.Windows.Forms.ToolStripItem> Elemente auf dem neu anzuordnen <xref:System.Windows.Forms.ToolStrip> .  
  
### <a name="to-enable-toolstripitem-rearrangement-at-run-time"></a>So aktivieren Sie die Neuanordnung von ToolStripItem zur Laufzeit  
  
- Legen Sie die <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> -Eigenschaft auf `true`fest. Standardmäßig <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> ist `false` .  
  
     Zur Laufzeit hält der Benutzer die Alt-Taste und die linke Maustaste gedrückt, um an <xref:System.Windows.Forms.ToolStripItem> eine andere Position auf dem zu ziehen <xref:System.Windows.Forms.ToolStrip> .  
  
    ```vb  
    toolStrip1.AllowItemReorder = True  
    ```  
  
    ```csharp  
    toolStrip1.AllowItemReorder = true;  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A>
- [Übersicht über das ToolStrip-Steuerelement](toolstrip-control-overview-windows-forms.md)
- [Architektur des ToolStrip-Steuerelements](toolstrip-control-architecture.md)
- [Zusammenfassung der ToolStrip-Technologie](toolstrip-technology-summary.md)
