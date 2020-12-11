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
# <a name="how-to-enable-reordering-of-toolstrip-items-at-run-time-in-windows-forms"></a><span data-ttu-id="04817-102">Gewusst wie: Aktivieren der Neuanordnung von ToolStrip-Elementen zur Laufzeit in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="04817-102">How to: Enable Reordering of ToolStrip Items at Run Time in Windows Forms</span></span>
<span data-ttu-id="04817-103">Sie können es dem Benutzer ermöglichen, Steuer <xref:System.Windows.Forms.ToolStripItem> Elemente auf dem neu anzuordnen <xref:System.Windows.Forms.ToolStrip> .</span><span class="sxs-lookup"><span data-stu-id="04817-103">You can enable the user to rearrange <xref:System.Windows.Forms.ToolStripItem> controls on the <xref:System.Windows.Forms.ToolStrip>.</span></span>  
  
### <a name="to-enable-toolstripitem-rearrangement-at-run-time"></a><span data-ttu-id="04817-104">So aktivieren Sie die Neuanordnung von ToolStripItem zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="04817-104">To enable ToolStripItem rearrangement at run time</span></span>  
  
- <span data-ttu-id="04817-105">Legen Sie die <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> -Eigenschaft auf `true`fest.</span><span class="sxs-lookup"><span data-stu-id="04817-105">Set the <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> property to `true`.</span></span> <span data-ttu-id="04817-106">Standardmäßig <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> ist `false` .</span><span class="sxs-lookup"><span data-stu-id="04817-106">By default, <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> is `false`.</span></span>  
  
     <span data-ttu-id="04817-107">Zur Laufzeit hält der Benutzer die Alt-Taste und die linke Maustaste gedrückt, um an <xref:System.Windows.Forms.ToolStripItem> eine andere Position auf dem zu ziehen <xref:System.Windows.Forms.ToolStrip> .</span><span class="sxs-lookup"><span data-stu-id="04817-107">At run time, the user holds down the ALT key and the left mouse button to drag a <xref:System.Windows.Forms.ToolStripItem> to a different location on the <xref:System.Windows.Forms.ToolStrip>.</span></span>  
  
    ```vb  
    toolStrip1.AllowItemReorder = True  
    ```  
  
    ```csharp  
    toolStrip1.AllowItemReorder = true;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="04817-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04817-108">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A>
- [<span data-ttu-id="04817-109">Übersicht über das ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="04817-109">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
- [<span data-ttu-id="04817-110">Architektur des ToolStrip-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="04817-110">ToolStrip Control Architecture</span></span>](toolstrip-control-architecture.md)
- [<span data-ttu-id="04817-111">Zusammenfassung der ToolStrip-Technologie</span><span class="sxs-lookup"><span data-stu-id="04817-111">ToolStrip Technology Summary</span></span>](toolstrip-technology-summary.md)
