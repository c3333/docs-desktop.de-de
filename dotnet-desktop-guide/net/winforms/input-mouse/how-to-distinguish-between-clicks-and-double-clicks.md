---
title: Unterscheiden zwischen Klicks und Doppelklicks
description: Hier werden verschiedene Möglichkeiten beschrieben, um mit einem Steuerelement oder einem Formular für Windows Forms für .NET den Unterschied zwischen einem einfachen Klick und einem Doppelklick zu erkennen.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- mouse [Windows Forms], click
- mouse [Windows Forms], double-click
- mouse clicks [Windows Forms], single versus double
ms.openlocfilehash: 7b58896a85ffd16ae2637b94d58845ed7a721c4d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942036"
---
# <a name="how-to-distinguish-between-clicks-and-double-clicks-windows-forms-net"></a><span data-ttu-id="15bb6-103">Unterscheiden zwischen Klicks und Doppelklicks (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="15bb6-103">How to distinguish between clicks and double-clicks (Windows Forms .NET)</span></span>

<span data-ttu-id="15bb6-104">In der Regel wird mit einem einzigen *Klick* eine Benutzerschnittstellenaktion initiiert, und mit einem *Doppelklick* wird die Aktion erweitert.</span><span class="sxs-lookup"><span data-stu-id="15bb6-104">Typically, a single *click* initiates a user interface action and a *double-click* extends the action.</span></span> <span data-ttu-id="15bb6-105">So wird mit einem einzigen Klick ein Element markiert, und mit einem Doppelklick wird das ausgewählte Element bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="15bb6-105">For example, one click usually selects an item, and a double-click edits the selected item.</span></span> <span data-ttu-id="15bb6-106">Allerdings lassen sich die Windows Forms-Klickereignisse nicht so einfach an ein Szenario anpassen, in dem ein Klick und ein Doppelklick inkompatible Aktionen ausführen, da eine Aktion, die mit dem <xref:System.Windows.Forms.Control.Click>- oder <xref:System.Windows.Forms.Control.MouseClick>-Ereignis verknüpft ist, ausgeführt wird, bevor die mit dem <xref:System.Windows.Forms.Control.DoubleClick>- oder <xref:System.Windows.Forms.Control.MouseDoubleClick>-Ereignis verknüpfte Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15bb6-106">However, the Windows Forms click events do not easily accommodate a scenario where a click and a double-click perform incompatible actions, because an action tied to the <xref:System.Windows.Forms.Control.Click> or <xref:System.Windows.Forms.Control.MouseClick> event is performed before the action tied to the <xref:System.Windows.Forms.Control.DoubleClick> or <xref:System.Windows.Forms.Control.MouseDoubleClick> event.</span></span> <span data-ttu-id="15bb6-107">In diesem Thema werden zwei Lösungen für dieses Problem erörtert.</span><span class="sxs-lookup"><span data-stu-id="15bb6-107">This topic demonstrates two solutions to this problem.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

<span data-ttu-id="15bb6-108">Eine Lösung besteht darin, das Doppelklickereignis zu behandeln und ein Rollback der Aktionen in der Behandlung des Klickereignisses zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="15bb6-108">One solution is to handle the double-click event and roll back the actions in the handling of the click event.</span></span> <span data-ttu-id="15bb6-109">In selten Fällen müssen Sie ggf. das Klick- und Doppelklickverhalten simulieren, indem Sie das <xref:System.Windows.Forms.Control.MouseDown>-Ereignis behandeln und dabei die Eigenschaften <xref:System.Windows.Forms.SystemInformation.DoubleClickTime%2A> und <xref:System.Windows.Forms.SystemInformation.DoubleClickSize%2A> der <xref:System.Windows.Forms.SystemInformation>-Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="15bb6-109">In rare situations you may need to simulate click and double-click behavior by handling the <xref:System.Windows.Forms.Control.MouseDown> event and by using the <xref:System.Windows.Forms.SystemInformation.DoubleClickTime%2A> and <xref:System.Windows.Forms.SystemInformation.DoubleClickSize%2A> properties of the <xref:System.Windows.Forms.SystemInformation> class.</span></span> <span data-ttu-id="15bb6-110">Sie messen die Zeit zwischen den Klicks, und wenn ein zweiter Klick erfolgt, bevor der Wert von <xref:System.Windows.Forms.SystemInformation.DoubleClickTime%2A> erreicht wurde und der Klick innerhalb des von <xref:System.Windows.Forms.SystemInformation.DoubleClickSize%2A> definierten Rechtecks erfolgt ist, führen Sie die Doppelklickaktion aus, andernfalls führen Sie die Klickaktion aus.</span><span class="sxs-lookup"><span data-stu-id="15bb6-110">You measure the time between clicks and if a second click occurs before the value of <xref:System.Windows.Forms.SystemInformation.DoubleClickTime%2A> is reached and the click is within a rectangle defined by <xref:System.Windows.Forms.SystemInformation.DoubleClickSize%2A>, perform the double-click action; otherwise, perform the click action.</span></span>

## <a name="to-roll-back-a-click-action"></a><span data-ttu-id="15bb6-111">So führen Sie ein Rollback einer Klickaktion durch</span><span class="sxs-lookup"><span data-stu-id="15bb6-111">To roll back a click action</span></span>

<span data-ttu-id="15bb6-112">Vergewissern Sie sich, dass das Steuerelement, mit dem Sie arbeiten, über das standardmäßig Doppelklickverhalten verfügt.</span><span class="sxs-lookup"><span data-stu-id="15bb6-112">Ensure that the control you are working with has standard double-click behavior.</span></span> <span data-ttu-id="15bb6-113">Andernfalls aktivieren Sie das Steuerelement mit der <xref:System.Windows.Forms.Control.SetStyle%2A>-Methode.</span><span class="sxs-lookup"><span data-stu-id="15bb6-113">If not, enable the control with the <xref:System.Windows.Forms.Control.SetStyle%2A> method.</span></span> <span data-ttu-id="15bb6-114">Behandeln Sie das Doppelklickereignis, und führen Sie ein Rollback der Klickaktion und der Doppelklickaktion durch.</span><span class="sxs-lookup"><span data-stu-id="15bb6-114">Handle the double-click event and roll back the click action as well as the double-click action.</span></span> <span data-ttu-id="15bb6-115">Im folgenden Codebeispiel wird gezeigt, wie eine benutzerdefinierte Schaltfläche mit aktiviertem Doppelklick erstellt und wie ein Rollback der Klickaktion im Behandlungscode des Doppelklickereignisses initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="15bb6-115">The following code example demonstrates a how to create a custom button with double-click enabled, as well as how to roll back the click action in the double-click event handling code.</span></span>

<span data-ttu-id="15bb6-116">In diesem Codebeispiel wird ein neues Schaltflächen-Steuerelement verwendet, das Doppelklicks ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="15bb6-116">This code example uses a new button control that enables double-clicks:</span></span>

:::code language="csharp" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/csharp/DoubleClickButton.cs" id="DoubleClickButton":::
:::code language="vb" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/vb/DoubleClickButton.vb" id="DoubleClickButton":::

<span data-ttu-id="15bb6-117">Der folgende Code veranschaulicht, wie ein Formular die Rahmenart des neuen Schaltflächen-Steuerelements basierend auf einem Klick oder Doppelklick ändert:</span><span class="sxs-lookup"><span data-stu-id="15bb6-117">The following code demonstrates how a form changes the style of border based on a click or double-click of the new button control:</span></span>

:::code language="csharp" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/csharp/Form1.cs" id="RollbackForm":::
:::code language="vb" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/vb/Form1.vb" id="RollbackForm":::

## <a name="to-distinguish-between-clicks"></a><span data-ttu-id="15bb6-118">Unterscheiden zwischen Klicks</span><span class="sxs-lookup"><span data-stu-id="15bb6-118">To distinguish between clicks</span></span>

<span data-ttu-id="15bb6-119">Verarbeiten Sie das <xref:System.Windows.Forms.Control.MouseDown>-Ereignis, und ermitteln Sie mit der <xref:System.Windows.Forms.SystemInformation>-Eigenschaft und einer <xref:System.Windows.Forms.Timer>-Komponente die Position und die Zeitspanne zwischen Klicks.</span><span class="sxs-lookup"><span data-stu-id="15bb6-119">Handle the <xref:System.Windows.Forms.Control.MouseDown> event and determine the location and time span between clicks using the <xref:System.Windows.Forms.SystemInformation> property and a <xref:System.Windows.Forms.Timer> component.</span></span> <span data-ttu-id="15bb6-120">Machen Sie die geeignete Aktion davon abhängig, ob ein Klick oder ein Doppelklick stattfindet.</span><span class="sxs-lookup"><span data-stu-id="15bb6-120">Perform the appropriate action depending on whether a click or double-click takes place.</span></span> <span data-ttu-id="15bb6-121">Das folgende Codebeispiel veranschaulicht, wie Sie dabei vorgehen.</span><span class="sxs-lookup"><span data-stu-id="15bb6-121">The following code example demonstrates how this can be done.</span></span>

:::code language="csharp" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/csharp/Form2.cs":::
:::code language="vb" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/vb/Form2.vb":::

## <a name="see-also"></a><span data-ttu-id="15bb6-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15bb6-122">See also</span></span>

- [<span data-ttu-id="15bb6-123">Übersicht über die Mausverwendung (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="15bb6-123">Overview of using the mouse (Windows Forms .NET)</span></span>](overview.md)
- [<span data-ttu-id="15bb6-124">Verwenden von Mausereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="15bb6-124">Using mouse events (Windows Forms .NET)</span></span>](events.md)
- [<span data-ttu-id="15bb6-125">Verwalten von Mauszeigern (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="15bb6-125">Manage mouse pointers (Windows Forms .NET)</span></span>](how-to-manage-cursor-pointer.md)
- [<span data-ttu-id="15bb6-126">Simulieren von Mausereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="15bb6-126">How to simulate mouse events (Windows Forms .NET)</span></span>](how-to-simulate-events.md)
- <xref:System.Windows.Forms.Control.Click?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.MouseDown?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.SetStyle%2A?displayProperty=nameWithType>
