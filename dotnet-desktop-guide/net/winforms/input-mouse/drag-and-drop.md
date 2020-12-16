---
title: Drag & Drop-Mausverhalten
description: Hier erfahren Sie mehr über die Funktionsweise von Drag & Drop-Vorgängen im Zusammenhang mit Windows Forms, einschließlich der Ausführung von Drag & Drop-Vorgängen mit der Maus.
ms.date: 10/26/2020
ms.topic: conceptual
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag and drop [Windows Forms], Windows Forms
- Windows Forms, drag and drop
ms.openlocfilehash: d434b0f0e80c610fffeea26a6fff44b43ca07fed
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942030"
---
# <a name="drag-and-drop-mouse-behavior-overview-windows-forms-net"></a><span data-ttu-id="42830-103">Übersicht über das Drag-&-Drop-Mausverhalten (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="42830-103">Drag-and-drop mouse behavior overview (Windows Forms .NET)</span></span>

<span data-ttu-id="42830-104">Windows Forms umfasst eine Reihe von Methoden, Ereignissen und Klassen, die das Drag &amp; Drop-Verhalten implementieren.</span><span class="sxs-lookup"><span data-stu-id="42830-104">Windows Forms includes a set of methods, events, and classes that implement drag-and-drop behavior.</span></span> <span data-ttu-id="42830-105">Dieses Thema enthält eine Übersicht über die Drag &amp; Drop-Unterstützung in Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="42830-105">This topic provides an overview of the drag-and-drop support in Windows Forms.</span></span><!-- TODO Also see [Drag-and-Drop Operations and Clipboard Support](./advanced/drag-and-drop-operations-and-clipboard-support.md).-->

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="drag-and-drop-events"></a><span data-ttu-id="42830-106">Drag & Drop-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="42830-106">Drag-and-drop events</span></span>

<span data-ttu-id="42830-107">Es gibt zwei Kategorien von Ereignissen in einem Drag & Drop-Vorgang: Ereignisse, die im aktuellen Ziel des Drag &amp; Drop-Vorgangs auftreten, und Ereignisse, die in der Quelle des Drag &amp; Drop-Vorgangs auftreten.</span><span class="sxs-lookup"><span data-stu-id="42830-107">There are two categories of events in a drag and drop operation: events that occur on the current target of the drag-and-drop operation, and events that occur on the source of the drag and drop operation.</span></span> <span data-ttu-id="42830-108">Sie müssen diese Ereignisse verarbeiten, um Drag & Drop-Vorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="42830-108">To perform drag-and-drop operations, you must handle these events.</span></span> <span data-ttu-id="42830-109">Wenn Sie die Daten aus den Ereignisargumenten dieser Ereignisse verwenden, können Sie Drag & Drop-Vorgänge problemlos vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="42830-109">By working with the information available in the event arguments of these events, you can easily facilitate drag-and-drop operations.</span></span>

## <a name="events-on-the-current-drop-target"></a><span data-ttu-id="42830-110">Ereignisse im aktuellen Ablageziel</span><span class="sxs-lookup"><span data-stu-id="42830-110">Events on the current drop target</span></span>

<span data-ttu-id="42830-111">Die folgende Tabelle zeigt die Ereignisse, die im aktuellen Ziel eines Drag &amp; Drop--Vorgangs auftreten.</span><span class="sxs-lookup"><span data-stu-id="42830-111">The following table shows the events that occur on the current target of a drag-and-drop operation.</span></span>

| <span data-ttu-id="42830-112">Mausereignis</span><span class="sxs-lookup"><span data-stu-id="42830-112">Mouse Event</span></span>                                   | <span data-ttu-id="42830-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42830-113">Description</span></span>                                                                                                                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <xref:System.Windows.Forms.Control.DragEnter> | <span data-ttu-id="42830-114">Dieses Ereignis tritt auf, wenn ein Objekt in die Begrenzungen des Steuerelements gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="42830-114">This event occurs when an object is dragged into the control's bounds.</span></span> <span data-ttu-id="42830-115">Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.DragEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="42830-115">The handler for this event receives an argument of type <xref:System.Windows.Forms.DragEventArgs>.</span></span>                              |
| <xref:System.Windows.Forms.Control.DragOver>  | <span data-ttu-id="42830-116">Dieses Ereignis tritt auf, wenn ein Objekt gezogen wird, während sich der Mauszeiger innerhalb der Grenzen des Steuerelements befindet.</span><span class="sxs-lookup"><span data-stu-id="42830-116">This event occurs when an object is dragged while the mouse pointer is within the control's bounds.</span></span> <span data-ttu-id="42830-117">Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.DragEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="42830-117">The handler for this event receives an argument of type <xref:System.Windows.Forms.DragEventArgs>.</span></span> |
| <xref:System.Windows.Forms.Control.DragDrop>  | <span data-ttu-id="42830-118">Dieses Ereignis tritt auf, wenn ein Drag &amp; Drop-Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="42830-118">This event occurs when a drag-and-drop operation is completed.</span></span> <span data-ttu-id="42830-119">Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.DragEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="42830-119">The handler for this event receives an argument of type <xref:System.Windows.Forms.DragEventArgs>.</span></span>                                      |
| <xref:System.Windows.Forms.Control.DragLeave> | <span data-ttu-id="42830-120">Dieses Ereignis tritt auf, wenn ein Objekt über die Grenzen des Steuerelements nach außen gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="42830-120">This event occurs when an object is dragged out of the control's bounds.</span></span> <span data-ttu-id="42830-121">Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.EventArgs>.</span><span class="sxs-lookup"><span data-stu-id="42830-121">The handler for this event receives an argument of type <xref:System.EventArgs>.</span></span>                                              |

<span data-ttu-id="42830-122">Die <xref:System.Windows.Forms.DragEventArgs>-Klasse stellt die Position des Mauszeigers, den aktuellen Zustand der Maustasten und der Zusatztasten der Tastatur, die gezogenen Daten und die <xref:System.Windows.Forms.DragDropEffects>-Werte bereit, die die Vorgänge, die für die Quelle des Ziehereignisses zulässig sind, sowie den Zielablegeeffekt für den Vorgang angeben.</span><span class="sxs-lookup"><span data-stu-id="42830-122">The <xref:System.Windows.Forms.DragEventArgs> class provides the location of the mouse pointer, the current state of the mouse buttons and modifier keys of the keyboard, the data being dragged, and <xref:System.Windows.Forms.DragDropEffects> values that specify the operations allowed by the source of the drag event and the target drop effect for the operation.</span></span>

## <a name="events-on-the-drop-source"></a><span data-ttu-id="42830-123">Ereignisse in der Ablagequelle</span><span class="sxs-lookup"><span data-stu-id="42830-123">Events on the drop source</span></span>

<span data-ttu-id="42830-124">Die folgende Tabelle zeigt die Ereignisse, die in der Quelle eines Drag &amp; Drop-Vorgangs auftreten.</span><span class="sxs-lookup"><span data-stu-id="42830-124">The following table shows the events that occur on the source of the drag-and-drop operation.</span></span>

|<span data-ttu-id="42830-125">Mausereignis</span><span class="sxs-lookup"><span data-stu-id="42830-125">Mouse Event</span></span>|<span data-ttu-id="42830-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42830-126">Description</span></span>|
|-----------------|-----------------|
|<xref:System.Windows.Forms.Control.GiveFeedback>|<span data-ttu-id="42830-127">Dieses Ereignis tritt während eines Ziehvorgangs auf.</span><span class="sxs-lookup"><span data-stu-id="42830-127">This event occurs during a drag operation.</span></span> <span data-ttu-id="42830-128">Es bietet die Möglichkeit, dem Benutzer einen visuellen Hinweis zu geben, dass der Drag &amp; Drop-Vorgang auftritt, z. B. Ändern des Mauszeigers.</span><span class="sxs-lookup"><span data-stu-id="42830-128">It provides an opportunity to give a visual cue to the user that the drag-and-drop operation is occurring, such as changing the mouse pointer.</span></span> <span data-ttu-id="42830-129">Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.GiveFeedbackEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="42830-129">The handler for this event receives an argument of type <xref:System.Windows.Forms.GiveFeedbackEventArgs>.</span></span>|
|<xref:System.Windows.Forms.Control.QueryContinueDrag>|<span data-ttu-id="42830-130">Dieses Ereignis wird während eines Drag & Drop-Vorgangs ausgelöst. Dadurch kann die Quelle des Ziehvorgangs bestimmen, ob der Drag &amp;amp; Drop-Vorgang abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="42830-130">This event is raised during a drag-and-drop operation and enables the drag source to determine whether the drag-and-drop operation should be canceled.</span></span> <span data-ttu-id="42830-131">Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.QueryContinueDragEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="42830-131">The handler for this event receives an argument of type <xref:System.Windows.Forms.QueryContinueDragEventArgs>.</span></span>|

<span data-ttu-id="42830-132">Die <xref:System.Windows.Forms.QueryContinueDragEventArgs>-Klasse stellt Folgendes bereit: den aktuellen Zustand der Maus und der Zusatztasten der Tastatur, einen Wert, der angibt, ob die ESC-Taste gedrückt wurde, und einen <xref:System.Windows.Forms.DragAction>-Wert, der festgelegt werden kann, um anzugeben, ob der Drag &amp; Drop-Vorgang fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="42830-132">The <xref:System.Windows.Forms.QueryContinueDragEventArgs> class provides the current state of the mouse buttons and modifier keys of the keyboard, a value specifying whether the ESC key was pressed, and a <xref:System.Windows.Forms.DragAction> value that can be set to specify whether the drag-and-drop operation should continue.</span></span>

## <a name="performing-drag-and-drop"></a><span data-ttu-id="42830-133">Ausführen von Drag & Drop-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="42830-133">Performing drag-and-drop</span></span>

<span data-ttu-id="42830-134">Drag & Drop-Vorgänge umfassen immer zwei Komponenten: die **Ziehquelle** und das **Ablageziel**.</span><span class="sxs-lookup"><span data-stu-id="42830-134">Drag-and-drop operations always involve two components, the **drag source** and the **drop target**.</span></span> <span data-ttu-id="42830-135">Sie müssen ein Steuerelement als Quelle festlegen und das <xref:System.Windows.Forms.Control.MouseDown>-Ereignis verarbeiten, um einen Drag & Drop-Vorgang starten zu können.</span><span class="sxs-lookup"><span data-stu-id="42830-135">To start a drag-and-drop operation, designate a control as the source and handle the <xref:System.Windows.Forms.Control.MouseDown> event.</span></span> <span data-ttu-id="42830-136">Rufen Sie im Ereignishandler die <xref:System.Windows.DragDrop.DoDragDrop%2A>-Methode auf, die die Daten bereitstellt, die der Ablage und dem <xref:System.Windows.DragDropEffects>-Wert zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="42830-136">In the event handler, call the <xref:System.Windows.DragDrop.DoDragDrop%2A> method providing the data associated with the drop and the a <xref:System.Windows.DragDropEffects> value.</span></span>

<span data-ttu-id="42830-137">Legen Sie die <xref:System.Windows.Forms.Control.AllowDrop>-Eigenschaft des Zielsteuerelements auf `true` fest, damit dieses Steuerelement einen Drag & Drop-Vorgang annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="42830-137">Set the target control's <xref:System.Windows.Forms.Control.AllowDrop> property set to `true` to allow that control to accept a drag-and-drop operation.</span></span> <span data-ttu-id="42830-138">Das Ziel verarbeitet zwei Ereignisse. Zuerst wird ein Ereignis als Reaktion auf das Ziehen über das Steuerelement verarbeitet (z. B. <xref:System.Windows.Forms.Control.DragOver>).</span><span class="sxs-lookup"><span data-stu-id="42830-138">The target handles two events, first an event in response to the drag being over the control, such as <xref:System.Windows.Forms.Control.DragOver>.</span></span> <span data-ttu-id="42830-139">Danach wird ein zweites Ereignis verarbeitet, bei dem es sich um die Ablageaktion selbst handelt (<xref:System.Windows.Forms.Control.DragDrop>).</span><span class="sxs-lookup"><span data-stu-id="42830-139">And a second event which is the drop action itself, <xref:System.Windows.Forms.Control.DragDrop>.</span></span>

<span data-ttu-id="42830-140">Das folgenden Beispiel veranschaulicht das Ziehen von einem <xref:System.Windows.Forms.Label>-Steuerelement in ein <xref:System.Windows.Forms.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="42830-140">The following example demonstrates a drag from a <xref:System.Windows.Forms.Label> control to a <xref:System.Windows.Forms.TextBox>.</span></span> <span data-ttu-id="42830-141">Wenn der Ziehvorgang abgeschlossen ist, antwortet das `TextBox`, indem es sich den Text der Bezeichnung selbst zuweist.</span><span class="sxs-lookup"><span data-stu-id="42830-141">When the drag is completed, the `TextBox` responds by assigning the label's text to itself.</span></span>

```csharp
// Initiate the drag
private void label1_MouseDown(object sender, MouseEventArgs e) =>
    DoDragDrop(((Label)sender).Text, DragDropEffects.All);

// Set the effect filter and allow the drop on this control
private void textBox1_DragOver(object sender, DragEventArgs e) =>
    e.Effect = DragDropEffects.All;

// React to the drop on this control
private void textBox1_DragDrop(object sender, DragEventArgs e) =>
    textBox1.Text = (string)e.Data.GetData(typeof(string));
```

```vb
' Initiate the drag
Private Sub Label1_MouseDown(sender As Object, e As MouseEventArgs)
    DoDragDrop(DirectCast(sender, Label).Text, DragDropEffects.All)
End Sub

' Set the effect filter and allow the drop on this control
Private Sub TextBox1_DragOver(sender As Object, e As DragEventArgs)
    e.Effect = DragDropEffects.All
End Sub

' React to the drop on this control
Private Sub TextBox1_DragDrop(sender As Object, e As DragEventArgs)
    TextBox1.Text = e.Data.GetData(GetType(String))
End Sub
```

<span data-ttu-id="42830-142">Weitere Informationen zu den Effekten von Ziehvorgängen finden Sie unter <xref:System.Windows.Forms.DragEventArgs.Data%2A> und <xref:System.Windows.Forms.DragEventArgs.AllowedEffect%2A>.</span><span class="sxs-lookup"><span data-stu-id="42830-142">For more information about the drag effects, see <xref:System.Windows.Forms.DragEventArgs.Data%2A> and <xref:System.Windows.Forms.DragEventArgs.AllowedEffect%2A>.</span></span>

## <a name="see-also"></a><span data-ttu-id="42830-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42830-143">See also</span></span>

- [<span data-ttu-id="42830-144">Übersicht über die Mausverwendung (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="42830-144">Overview of using the mouse (Windows Forms .NET)</span></span>](overview.md)
- <xref:System.Windows.Forms.Control.DragDrop?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.DragEnter?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.DragLeave?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.DragOver?displayProperty=nameWithType>
