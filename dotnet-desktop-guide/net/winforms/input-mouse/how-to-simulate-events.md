---
title: Simulieren von Mausereignissen
description: Hier erfahren Sie, wie Sie Mausereignisse in Windows Forms für .NET simulieren.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- mouse [Windows Forms], event simulation
- user input [Windows Forms], simulating
- SendKeys [Windows Forms], using
ms.openlocfilehash: 443611163d33a266b3c49d03df13131c994b0bd3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942097"
---
# <a name="how-to-simulate-mouse-events-windows-forms-net"></a><span data-ttu-id="c0bc9-103">Simulieren von Mausereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="c0bc9-103">How to simulate mouse events (Windows Forms .NET)</span></span>

<span data-ttu-id="c0bc9-104">Das Simulieren von Mausereignissen in Windows Forms ist etwas komplexer als das Simulieren von Tastaturereignissen.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-104">Simulating mouse events in Windows Forms isn't as straight forward as simulating keyboard events.</span></span> <span data-ttu-id="c0bc9-105">Windows Forms bietet keine Hilfsprogrammklasse, mit der die Maus verschoben werden kann und Mausklickaktionen aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-105">Windows Forms doesn't provide a helper class to move the mouse and invoke mouse-click actions.</span></span> <span data-ttu-id="c0bc9-106">Die einzige Option, die Maus zu steuern, ist die Verwendung nativer Windows-Methoden.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-106">The only option for controlling the mouse is to use native Windows methods.</span></span> <span data-ttu-id="c0bc9-107">Wenn Sie mit einem benutzerdefinierten Steuerelement oder einem Formular arbeiten, können Sie ein Mausereignis simulieren, Sie können die Maus jedoch nicht direkt steuern.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-107">If you're working with a custom control or a form, you can simulate a mouse event, but you can't directly control the mouse.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="events"></a><span data-ttu-id="c0bc9-108">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c0bc9-108">Events</span></span>

<span data-ttu-id="c0bc9-109">Die meisten Ereignisse verfügen über eine entsprechende Methode, die sie aufruft und im Muster `On` gefolgt von `EventName` (z. B. `OnMouseMove`) benannt wird.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-109">Most events have a corresponding method that invokes them, named in the pattern of `On` followed by `EventName`, such as `OnMouseMove`.</span></span> <span data-ttu-id="c0bc9-110">Diese Option wird normalerweise nur in benutzerdefinierten Steuerelementen und Formularen unterstützt, weil die Methoden geschützt sind und außerhalb des Kontexts des Steuerelements oder Formulars nicht aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-110">This option is only possible within custom controls or forms, because these methods are protected and can't be accessed from outside the context of the control or form.</span></span> <span data-ttu-id="c0bc9-111">Der Nachteil der Verwendung einer Methode wie `OnMouseMove` besteht darin, dass die Maus so nicht gesteuert werden kann und dass keine Interaktionen mit dem Steuerelement möglich sind. Es wird einfach nur das dazugehörige Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-111">The disadvantage to using a method such as `OnMouseMove` is that it doesn't actually control the mouse or interact with the control, it simply raises the associated event.</span></span> <span data-ttu-id="c0bc9-112">Wenn Sie beispielsweise das Bewegen des Mauszeigers über einem Element in einer <xref:System.Windows.Forms.ListBox>-Klasse simulieren möchten, reagieren `OnMouseMove` und `ListBox` nicht visuell durch ein hervorgehobenes Element unter dem Cursor.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-112">For example, if you wanted to simulate hovering over an item in a <xref:System.Windows.Forms.ListBox>, `OnMouseMove` and the `ListBox` doesn't visually react with a highlighted item under the cursor.</span></span>

<span data-ttu-id="c0bc9-113">Diese geschützten Methoden sind zum Simulieren von Mausereignissen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-113">These protected methods are available to simulate mouse events.</span></span>

- `OnMouseDown`
- `OnMouseEnter`
- `OnMouseHover`
- `OnMouseLeave`
- `OnMouseMove`
- `OnMouseUp`
- `OnMouseWheel`
- `OnMouseClick`
- `OnMouseDoubleClick`

<span data-ttu-id="c0bc9-114">Weitere Informationen zu diesen Ereignissen finden Sie unter [Verwenden von Mausereignissen (Windows Forms .NET)](events.md).</span><span class="sxs-lookup"><span data-stu-id="c0bc9-114">For more information about these events, see [Using mouse events (Windows Forms .NET)](events.md)</span></span>

## <a name="invoke-a-click"></a><span data-ttu-id="c0bc9-115">Aufrufen eines Klicks</span><span class="sxs-lookup"><span data-stu-id="c0bc9-115">Invoke a click</span></span>

<span data-ttu-id="c0bc9-116">Angesichts der Tatsache, dass auf das Klicken auf ein Steuerelement in den meisten Fällen eine Reaktion erfolgt, z. B. eine Schaltfläche, die Benutzercode aufruft, oder ein Kontrollkästchen, für das der Aktivierungszustand geändert wird, bietet Windows Forms eine einfache Möglichkeit, einen Klick auszulösen.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-116">Considering most controls do something when clicked, like a button calling user code, or checkbox change its checked state, Windows Forms provides an easy way to trigger the click.</span></span> <span data-ttu-id="c0bc9-117">Manche Steuerelemente, z. B. ComboBox-Steuerelemente, reagieren nicht, wenn auf sie geklickt wird. Eine Simulation eines solchen Klicks hat also keine Auswirkung auf das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-117">Some controls, such as a combobox, don't do anything special when clicked and simulating a click has no effect on the control.</span></span>

### <a name="performclick"></a><span data-ttu-id="c0bc9-118">PerformClick</span><span class="sxs-lookup"><span data-stu-id="c0bc9-118">PerformClick</span></span>

<span data-ttu-id="c0bc9-119">Die <xref:System.Windows.Forms.IButtonControl?displayProperty=nameWithType>-Schnittstelle stellt die <xref:System.Windows.Forms.IButtonControl.PerformClick%2A>-Methode bereit, die ein Klick auf das Steuerelement simuliert.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-119">The <xref:System.Windows.Forms.IButtonControl?displayProperty=nameWithType> interface provides the <xref:System.Windows.Forms.IButtonControl.PerformClick%2A> method which simulates a click on the control.</span></span> <span data-ttu-id="c0bc9-120">Sowohl das <xref:System.Windows.Forms.Button?displayProperty=nameWithType>- als auch das <xref:System.Windows.Forms.LinkLabel?displayProperty=nameWithType>-Steuerelement implementieren diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-120">Both the <xref:System.Windows.Forms.Button?displayProperty=nameWithType> and <xref:System.Windows.Forms.LinkLabel?displayProperty=nameWithType> controls implement this interface.</span></span>

:::code language="csharp" source="snippets/how-to-simulate-events/csharp/Form1.cs" id="PerformClick":::
:::code language="vb" source="snippets/how-to-simulate-events/vb/Form1.vb" id="PerformClick":::

### <a name="invokeclick"></a><span data-ttu-id="c0bc9-121">InvokeClick</span><span class="sxs-lookup"><span data-stu-id="c0bc9-121">InvokeClick</span></span>

<span data-ttu-id="c0bc9-122">Verwenden Sie für ein Formular oder ein benutzerdefiniertes Steuerelement die <xref:System.Windows.Forms.Control.InvokeOnClick%2A>-Methode zum Simulieren eines Mausklicks.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-122">With a form a custom control, use the <xref:System.Windows.Forms.Control.InvokeOnClick%2A> method to simulate a mouse click.</span></span> <span data-ttu-id="c0bc9-123">Dabei handelt es sich um eine geschützte Methode, die nur von innerhalb eines Formulars oder eines abgeleiteten benutzerdefinierten Steuerelements aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-123">This is a protected method that can only be called from within the form or a derived custom control.</span></span>

<span data-ttu-id="c0bc9-124">Durch den folgenden Code wird beispielsweise ein Kontrollkästchen in `button1` angeklickt.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-124">For example, the following code clicks a checkbox from `button1`.</span></span>

:::code language="csharp" source="snippets/how-to-simulate-events/csharp/Form1.cs" id="ClickCheckbox":::
:::code language="vb" source="snippets/how-to-simulate-events/vb/Form1.vb" id="ClickCheckbox":::

## <a name="use-native-windows-methods"></a><span data-ttu-id="c0bc9-125">Verwenden nativer Windows-Methoden</span><span class="sxs-lookup"><span data-stu-id="c0bc9-125">Use native Windows methods</span></span>

<span data-ttu-id="c0bc9-126">Windows bietet Methoden, die Sie aufrufen können, um Mausbewegungen und -klicks wie [`User32.dll SendInput`](/windows/win32/api/winuser/nf-winuser-sendinput) und [`User32.dll SetCursorPos`](/windows/win32/api/winuser/nf-winuser-setcursorpos) zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="c0bc9-126">Windows provides methods you can call to simulate mouse movements and clicks such as [`User32.dll SendInput`](/windows/win32/api/winuser/nf-winuser-sendinput) and [`User32.dll SetCursorPos`](/windows/win32/api/winuser/nf-winuser-setcursorpos).</span></span> <span data-ttu-id="c0bc9-127">Im folgenden Beispiel wird der Mauszeiger in die Mitte eines Steuerelements verschoben:</span><span class="sxs-lookup"><span data-stu-id="c0bc9-127">The following example moves the mouse cursor to the center of a control:</span></span>

:::code language="csharp" source="snippets/how-to-simulate-events/csharp/Form2.cs" id="MoveCursor":::
:::code language="vb" source="snippets/how-to-simulate-events/vb/Form2.vb" id="MoveCursor":::

## <a name="see-also"></a><span data-ttu-id="c0bc9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0bc9-128">See also</span></span>

- [<span data-ttu-id="c0bc9-129">Übersicht über die Mausverwendung (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="c0bc9-129">Overview of using the mouse (Windows Forms .NET)</span></span>](overview.md)
- [<span data-ttu-id="c0bc9-130">Verwenden von Mausereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="c0bc9-130">Using mouse events (Windows Forms .NET)</span></span>](events.md)
- [<span data-ttu-id="c0bc9-131">Unterscheiden zwischen Klicks und Doppelklicks (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="c0bc9-131">How to distinguish between clicks and double-clicks (Windows Forms .NET)</span></span>](how-to-distinguish-between-clicks-and-double-clicks.md)
- [<span data-ttu-id="c0bc9-132">Verwalten von Mauszeigern (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="c0bc9-132">Manage mouse pointers (Windows Forms .NET)</span></span>](how-to-manage-cursor-pointer.md)
