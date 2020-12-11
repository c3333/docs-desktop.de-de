---
title: 'Vorgehensweise: Umgang mit dem ToolStrip-Überlauf'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], managing overflow
- toolbars [Windows Forms], managing overflow
- examples [Windows Forms], toolbars
- CanOverflow property
ms.assetid: fa10e0ad-4cbf-4c0d-9082-359c2f855d4e
ms.openlocfilehash: 52cc02e626bee2d2457355028ecddc17e462d8fa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974803"
---
# <a name="how-to-manage-toolstrip-overflow-in-windows-forms"></a><span data-ttu-id="fd07f-102">Gewusst wie: Umgang mit dem ToolStrip-Überlauf in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fd07f-102">How to: Manage ToolStrip Overflow in Windows Forms</span></span>

<span data-ttu-id="fd07f-103">Wenn alle Elemente in einem <xref:System.Windows.Forms.ToolStrip> -Steuerelement nicht in den zugewiesenen Speicherplatz passen, können Sie die Überlauf Funktion für die aktivieren <xref:System.Windows.Forms.ToolStrip> und das Überlauf Verhalten bestimmter <xref:System.Windows.Forms.ToolStripItem> s bestimmen.</span><span class="sxs-lookup"><span data-stu-id="fd07f-103">When all the items on a <xref:System.Windows.Forms.ToolStrip> control do not fit in the allotted space, you can enable overflow functionality on the <xref:System.Windows.Forms.ToolStrip> and determine the overflow behavior of specific <xref:System.Windows.Forms.ToolStripItem>s.</span></span>

<span data-ttu-id="fd07f-104">Wenn Sie s hinzufügen <xref:System.Windows.Forms.ToolStripItem> , die mehr Speicherplatz benötigen, als für die <xref:System.Windows.Forms.ToolStrip> aktuelle Größe des Formulars zugewiesen ist, wird <xref:System.Windows.Forms.ToolStripOverflowButton> automatisch auf dem angezeigt <xref:System.Windows.Forms.ToolStrip> .</span><span class="sxs-lookup"><span data-stu-id="fd07f-104">When you add <xref:System.Windows.Forms.ToolStripItem>s that require more space than is allotted to the <xref:System.Windows.Forms.ToolStrip> given the form's current size, a <xref:System.Windows.Forms.ToolStripOverflowButton> automatically appears on the <xref:System.Windows.Forms.ToolStrip>.</span></span> <span data-ttu-id="fd07f-105">Die <xref:System.Windows.Forms.ToolStripOverflowButton> angezeigten Elemente und Überlauf aktivierte Elemente werden in das Dropdown Menü Überlauf verschoben.</span><span class="sxs-lookup"><span data-stu-id="fd07f-105">The <xref:System.Windows.Forms.ToolStripOverflowButton> appears, and overflow-enabled items are moved into the drop-down overflow menu.</span></span> <span data-ttu-id="fd07f-106">Auf diese Weise können Sie anpassen und priorisieren, wie Ihre <xref:System.Windows.Forms.ToolStrip> Elemente ordnungsgemäß an verschiedene Formular Größen angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="fd07f-106">This allows you to customize and prioritize how your <xref:System.Windows.Forms.ToolStrip> items properly adjust to different form sizes.</span></span> <span data-ttu-id="fd07f-107">Sie können auch die Darstellung Ihrer Elemente ändern, wenn Sie in den Überlauf geraten, indem Sie die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.ToolStripItem.Placement%2A> <xref:System.Windows.Forms.ToolStripOverflow.DisplayedItems%2A?displayProperty=nameWithType> sowie das- <xref:System.Windows.Forms.ToolStrip.LayoutCompleted> Ereignis verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd07f-107">You can also change the appearance of your items when they fall into the overflow by using the <xref:System.Windows.Forms.ToolStripItem.Placement%2A> and <xref:System.Windows.Forms.ToolStripOverflow.DisplayedItems%2A?displayProperty=nameWithType> properties and the <xref:System.Windows.Forms.ToolStrip.LayoutCompleted> event.</span></span> <span data-ttu-id="fd07f-108">Wenn Sie das Formular entweder zur Entwurfszeit oder zur Laufzeit vergrößern, <xref:System.Windows.Forms.ToolStripItem> können weitere s auf dem Hauptfenster angezeigt werden, <xref:System.Windows.Forms.ToolStrip> und die wird <xref:System.Windows.Forms.ToolStripOverflowButton> möglicherweise sogar ausgeblendet, bis Sie die Größe des Formulars verringern.</span><span class="sxs-lookup"><span data-stu-id="fd07f-108">If you enlarge the form at either design time or run time, more <xref:System.Windows.Forms.ToolStripItem>s can be displayed on the main <xref:System.Windows.Forms.ToolStrip> and the <xref:System.Windows.Forms.ToolStripOverflowButton> might even disappear until you decrease the size of the form.</span></span>

## <a name="to-enable-overflow-on-a-toolstrip-control"></a><span data-ttu-id="fd07f-109">So aktivieren Sie den Überlauf für ein ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="fd07f-109">To enable overflow on a ToolStrip control</span></span>

- <span data-ttu-id="fd07f-110">Stellen Sie sicher, dass die- <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> Eigenschaft nicht auf für festgelegt ist `false` <xref:System.Windows.Forms.ToolStrip> .</span><span class="sxs-lookup"><span data-stu-id="fd07f-110">Ensure that the <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> property is not set to `false` for the <xref:System.Windows.Forms.ToolStrip>.</span></span> <span data-ttu-id="fd07f-111">Der Standardwert ist `True`.</span><span class="sxs-lookup"><span data-stu-id="fd07f-111">The default is `True`.</span></span>

     <span data-ttu-id="fd07f-112">Wenn <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> ist `True` (der Standardwert), <xref:System.Windows.Forms.ToolStripItem> wird eine an das Dropdown-Überlauf Menü gesendet, wenn der Inhalt von <xref:System.Windows.Forms.ToolStripItem> die Breite eines horizontalen <xref:System.Windows.Forms.ToolStrip> oder der Höhe eines vertikalen überschreitet <xref:System.Windows.Forms.ToolStrip> .</span><span class="sxs-lookup"><span data-stu-id="fd07f-112">When <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> is `True` (the default), a <xref:System.Windows.Forms.ToolStripItem> is sent to the drop-down overflow menu when the content of the <xref:System.Windows.Forms.ToolStripItem> exceeds the width of a horizontal <xref:System.Windows.Forms.ToolStrip> or the height of a vertical <xref:System.Windows.Forms.ToolStrip>.</span></span>

## <a name="to-specify-overflow-behavior-of-a-specific-toolstripitem"></a><span data-ttu-id="fd07f-113">So geben Sie das Überlauf Verhalten eines bestimmten Tool Strip Item an</span><span class="sxs-lookup"><span data-stu-id="fd07f-113">To specify overflow behavior of a specific ToolStripItem</span></span>

- <span data-ttu-id="fd07f-114">Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> Eigenschaft des <xref:System.Windows.Forms.ToolStripItem> auf den gewünschten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="fd07f-114">Set the <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> property of the <xref:System.Windows.Forms.ToolStripItem> to the desired value.</span></span> <span data-ttu-id="fd07f-115">Die Möglichkeiten sind `Always` , `Never` und `AsNeeded` .</span><span class="sxs-lookup"><span data-stu-id="fd07f-115">The possibilities are `Always`, `Never`, and `AsNeeded`.</span></span> <span data-ttu-id="fd07f-116">Der Standardwert ist `AsNeeded`.</span><span class="sxs-lookup"><span data-stu-id="fd07f-116">The default is `AsNeeded`.</span></span>

    ```vb
    toolStripTextBox1.Overflow = _
    System.Windows.Forms.ToolStripItemOverflow.Never
    ```

    ```csharp
    toolStripTextBox1.Overflow = _
    System.Windows.Forms.ToolStripItemOverflow.Never;
    ```

## <a name="see-also"></a><span data-ttu-id="fd07f-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd07f-117">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripOverflowButton>
- <xref:System.Windows.Forms.ToolStripItem.Overflow%2A>
- <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A>
- [<span data-ttu-id="fd07f-118">Übersicht über das ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="fd07f-118">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
- [<span data-ttu-id="fd07f-119">Architektur des ToolStrip-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="fd07f-119">ToolStrip Control Architecture</span></span>](toolstrip-control-architecture.md)
- [<span data-ttu-id="fd07f-120">Zusammenfassung der ToolStrip-Technologie</span><span class="sxs-lookup"><span data-stu-id="fd07f-120">ToolStrip Technology Summary</span></span>](toolstrip-technology-summary.md)
