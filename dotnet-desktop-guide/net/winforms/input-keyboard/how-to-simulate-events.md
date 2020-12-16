---
title: Simulieren von Tastaturereignissen
description: Hier erfahren Sie, wie Sie Tastaturereignisse in Windows Forms für .NET simulieren.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- keyboards [Windows Forms], event simulation
- user input [Windows Forms], simulating
- SendKeys [Windows Forms], using
ms.openlocfilehash: 5ac62ca4311461ba95a2c31876d038baffe678a2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942125"
---
# <a name="how-to-simulate-keyboard-events-windows-forms-net"></a><span data-ttu-id="c8ced-103">Simulieren von Tastaturereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="c8ced-103">How to simulate keyboard events (Windows Forms .NET)</span></span>

<span data-ttu-id="c8ced-104">Windows Forms stellt einige Optionen zur programmgesteuerten Simulation von Tastatureingaben bereit.</span><span class="sxs-lookup"><span data-stu-id="c8ced-104">Windows Forms provides a few options for programmatically simulating keyboard input.</span></span> <span data-ttu-id="c8ced-105">Dieser Artikel bietet eine Übersicht über diese Optionen.</span><span class="sxs-lookup"><span data-stu-id="c8ced-105">This article provides an overview of these options.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="use-sendkeys"></a><span data-ttu-id="c8ced-106">Verwenden von SendKeys</span><span class="sxs-lookup"><span data-stu-id="c8ced-106">Use SendKeys</span></span>

<span data-ttu-id="c8ced-107">Windows Forms stellt die <xref:System.Windows.Forms.SendKeys?displayProperty=fullName>-Klasse bereit, um Tastatureingaben an die aktive Anwendung zu senden.</span><span class="sxs-lookup"><span data-stu-id="c8ced-107">Windows Forms provides the <xref:System.Windows.Forms.SendKeys?displayProperty=fullName> class for sending keystrokes to the active application.</span></span> <span data-ttu-id="c8ced-108">Es gibt zwei Methoden zum Senden von Tastatureingaben an eine Anwendung: <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> und <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="c8ced-108">There are two methods to send keystrokes to an application: <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> and <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="c8ced-109">Der Unterschied zwischen den beiden Methoden besteht darin, dass `SendWait` im Gegensatz zu `Send` den aktuellen Thread blockiert, wenn die Tastatureingabe gesendet wird, und dann auf eine Antwort wartet.</span><span class="sxs-lookup"><span data-stu-id="c8ced-109">The difference between the two methods is that `SendWait` blocks the current thread when the keystroke is sent, waiting for a response, while `Send` doesn't.</span></span> <span data-ttu-id="c8ced-110">Weitere Informationen zu `SendWait` finden Sie unter [Senden einer Tastatureingabe an eine andere Anwendung](#to-send-a-keystroke-to-a-different-application).</span><span class="sxs-lookup"><span data-stu-id="c8ced-110">For more information about `SendWait`, see [To send a keystroke to a different application](#to-send-a-keystroke-to-a-different-application).</span></span>

> [!CAUTION]
> <span data-ttu-id="c8ced-111">Wenn Ihre Anwendung für internationale Verwendung mit unterschiedlichen Tastaturen vorgesehen ist, kann ein Verwenden von <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> zu unvorhersehbaren Ergebnissen führen und sollte vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="c8ced-111">If your application is intended for international use with a variety of keyboards, the use of <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> could yield unpredictable results and should be avoided.</span></span>

<span data-ttu-id="c8ced-112">Im Hintergrund verwendet `SendKeys` eine ältere Windows-Implementierung zum Senden von Eingaben, bei der im Zusammenhang mit modernen Windows-Betriebssystemen möglicherweise ein Fehler auftritt, da hier erwartet wird, dass die Anwendung nicht mit Administratorrechten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8ced-112">Behind the scenes, `SendKeys` uses an older Windows implementation for sending input, which may fail on modern Windows where it's expected that the application isn't running with administrative rights.</span></span> <span data-ttu-id="c8ced-113">Wenn bei der älteren Implementierung ein Fehler auftritt, versucht der Code automatisch, die neuere Windows-Implementierung zum Senden von Eingaben zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8ced-113">If the older implementation fails, the code automatically tries the newer Windows implementation for sending input.</span></span> <span data-ttu-id="c8ced-114">Wenn die <xref:System.Windows.Forms.SendKeys>-Klasse die neue Implementierung verwendet, blockiert die <xref:System.Windows.Forms.SendKeys.SendWait%2A>-Methode zudem den aktuellen Thread nicht mehr, wenn Tastatureingaben an eine andere Anwendung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8ced-114">Additionally, when the <xref:System.Windows.Forms.SendKeys> class uses the new implementation, the <xref:System.Windows.Forms.SendKeys.SendWait%2A> method no longer blocks the current thread when sending keystrokes to another application.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8ced-115">Ist für Ihre Anwendung ein einheitliches, vom Betriebssystem unabhängiges Verhalten erforderlich, können Sie für die <xref:System.Windows.Forms.SendKeys> -Klasse das Verwenden der neuen Implementierung erzwingen, indem Sie die folgende Anwendungseinstellung in Ihre "app.config"-Datei einfügen.</span><span class="sxs-lookup"><span data-stu-id="c8ced-115">If your application relies on consistent behavior regardless of the operating system, you can force the <xref:System.Windows.Forms.SendKeys> class to use the new implementation by adding the following application setting to your app.config file.</span></span>
>
> ```xml
> <appSettings>
>   <add key="SendKeys" value="SendInput"/>
> </appSettings>
> ```
>
> <span data-ttu-id="c8ced-116">Verwenden Sie stattdessen den Wert `"JournalHook"`, wenn die <xref:System.Windows.Forms.SendKeys>-Klasse gezwungen werden soll, _nur_ die vorherige Implementierung zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="c8ced-116">To force the <xref:System.Windows.Forms.SendKeys> class to _only_ use the previous implementation, use the value `"JournalHook"` instead.</span></span>

### <a name="to-send-a-keystroke-to-the-same-application"></a><span data-ttu-id="c8ced-117">So senden Sie eine Tastatureingabe an dieselbe Anwendung</span><span class="sxs-lookup"><span data-stu-id="c8ced-117">To send a keystroke to the same application</span></span>

<span data-ttu-id="c8ced-118">Rufen Sie die <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> - oder die <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType> -Methode der <xref:System.Windows.Forms.SendKeys> -Klasse auf.</span><span class="sxs-lookup"><span data-stu-id="c8ced-118">Call the <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> or <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType> method of the <xref:System.Windows.Forms.SendKeys> class.</span></span> <span data-ttu-id="c8ced-119">Die angegebenen Tastatureingaben werden vom aktiven Steuerelement der Anwendung empfangen.</span><span class="sxs-lookup"><span data-stu-id="c8ced-119">The specified keystrokes will be received by the active control of the application.</span></span>

<span data-ttu-id="c8ced-120">Im folgenden Codebeispiel wird `Send` verwendet, um das gleichzeitige Drücken der Tasten <kbd>ALT</kbd> und <kbd>NACH-UNTEN</kbd> zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="c8ced-120">The following code example uses `Send` to simulate pressing the <kbd>ALT</kbd> and <kbd>DOWN</kbd> keys together.</span></span> <span data-ttu-id="c8ced-121">Diese Tastatureingaben bewirken, dass das <xref:System.Windows.Forms.ComboBox>-Steuerelement sein Dropdownmenü anzeigt.</span><span class="sxs-lookup"><span data-stu-id="c8ced-121">These keystrokes cause the <xref:System.Windows.Forms.ComboBox> control to display its dropdown.</span></span> <span data-ttu-id="c8ced-122">In diesem Beispiel wird eine <xref:System.Windows.Forms.Form>-Klasse mit einer <xref:System.Windows.Forms.Button>- und einer <xref:System.Windows.Forms.ComboBox>-Klasse vorausgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c8ced-122">This example assumes a <xref:System.Windows.Forms.Form> with a <xref:System.Windows.Forms.Button> and <xref:System.Windows.Forms.ComboBox>.</span></span>

:::code language="csharp" source="snippets/how-to-simulate-events/csharp/Form1.cs" id="ShowDropDown":::
:::code language="vb" source="snippets/how-to-simulate-events/vb/Form1.vb" id="ShowDropDown":::

### <a name="to-send-a-keystroke-to-a-different-application"></a><span data-ttu-id="c8ced-123">So senden Sie eine Tastatureingabe an eine andere Anwendung</span><span class="sxs-lookup"><span data-stu-id="c8ced-123">To send a keystroke to a different application</span></span>

<span data-ttu-id="c8ced-124">Die Methoden <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> und <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType> senden Tastatureingaben an die aktive Anwendung, bei der es sich normalerweise um die Anwendung handelt, über die Sie Tastatureingaben senden.</span><span class="sxs-lookup"><span data-stu-id="c8ced-124">The <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> and <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType> methods send keystrokes to the active application, which is usually the application you're sending keystrokes from.</span></span> <span data-ttu-id="c8ced-125">Sie müssen eine andere Anwendung zuerst aktivieren, um Tastatureingaben an diese senden zu können.</span><span class="sxs-lookup"><span data-stu-id="c8ced-125">To send keystrokes to another application, you first need to activate it.</span></span> <span data-ttu-id="c8ced-126">Da keine verwaltete Methode zum Aktivieren einer anderen Anwendung vorhanden ist, müssen Sie native Windows-Methoden verwenden, um den Fokus auf die andere Anwendung zu lenken.</span><span class="sxs-lookup"><span data-stu-id="c8ced-126">Because there's no managed method to activate another application, you must use native Windows methods to focus the other application.</span></span> <span data-ttu-id="c8ced-127">Im folgenden Codebeispiel wird ein Plattformaufruf dazu verwendet, die Methoden `FindWindow` und `SetForegroundWindow` aufzurufen, um das Anwendungsfenster Rechner zu aktivieren, und dann wird `Send` aufgerufen, um einige Berechnungselemente an Rechner zu senden.</span><span class="sxs-lookup"><span data-stu-id="c8ced-127">The following code example uses platform invoke to call the `FindWindow` and `SetForegroundWindow` methods to activate the Calculator application window, and then calls `Send` to issue a series of calculations to the Calculator application.</span></span>

<span data-ttu-id="c8ced-128">Im folgenden Codebeispiel wird `Send` verwendet, um das Drücken von Tasten in der Rechneranwendung unter Windows 10 zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="c8ced-128">The following code example uses `Send` to simulate pressing keys into the Windows 10 Calculator application.</span></span> <span data-ttu-id="c8ced-129">Zuerst wird nach einem Anwendungsfenster mit dem Titel `Calculator` gesucht und dieses dann aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8ced-129">It first searches for an application window with title of `Calculator` and then activates it.</span></span> <span data-ttu-id="c8ced-130">Nach der Aktivierung werden Tastatureingaben zum Berechnen der Summe von „10“ und „10“ gesendet.</span><span class="sxs-lookup"><span data-stu-id="c8ced-130">Once activated, the keystrokes are sent to calculate 10 plus 10.</span></span>

:::code language="csharp" source="snippets/how-to-simulate-events/csharp/Form2.cs" id="Calculator":::
:::code language="vb" source="snippets/how-to-simulate-events/vb/Form2.vb" id="Calculator":::

## <a name="use-oneventname-methods"></a><span data-ttu-id="c8ced-131">Verwenden von OnEventName-Methoden</span><span class="sxs-lookup"><span data-stu-id="c8ced-131">Use OnEventName methods</span></span>

<span data-ttu-id="c8ced-132">Die einfachste Möglichkeit zum Simulieren von Tastaturereignissen besteht darin, eine Methode für das Objekt aufzurufen, das das Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="c8ced-132">The easiest way to simulate keyboard events is to call a method on the object that raises the event.</span></span> <span data-ttu-id="c8ced-133">Die meisten Ereignisse verfügen über eine entsprechende Methode, die sie aufruft und im Muster `On` gefolgt von `EventName` (z. B. `OnKeyPress`) benannt wird.</span><span class="sxs-lookup"><span data-stu-id="c8ced-133">Most events have a corresponding method that invokes them, named in the pattern of `On` followed by `EventName`, such as `OnKeyPress`.</span></span> <span data-ttu-id="c8ced-134">Diese Option wird normalerweise nur in benutzerdefinierten Steuerelementen und Formularen unterstützt, weil die Methoden geschützt sind und außerhalb des Kontexts des Steuerelements oder Formulars nicht aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="c8ced-134">This option is only possible within custom controls or forms, because these methods are protected and can't be accessed from outside the context of the control or form.</span></span>

<span data-ttu-id="c8ced-135">Diese geschützten Methoden sind zum Simulieren von Tastaturereignissen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8ced-135">These protected methods are available to simulate keyboard events.</span></span>

- `OnKeyDown`
- `OnKeyPress`
- `OnKeyUp`

<span data-ttu-id="c8ced-136">Weitere Informationen zu diesen Ereignissen finden Sie unter [Verwenden von Tastaturereignissen (Windows Forms .NET)](events.md).</span><span class="sxs-lookup"><span data-stu-id="c8ced-136">For more information about these events, see [Using keyboard events (Windows Forms .NET)](events.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c8ced-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8ced-137">See also</span></span>

- [<span data-ttu-id="c8ced-138">Übersicht über die Verwendung der Tastatur (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="c8ced-138">Overview of using the keyboard (Windows Forms .NET)</span></span>](overview.md)
- [<span data-ttu-id="c8ced-139">Verwenden von Tastaturereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="c8ced-139">Using keyboard events (Windows Forms .NET)</span></span>](events.md)
- [<span data-ttu-id="c8ced-140">Verwenden von Mausereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="c8ced-140">Using mouse events (Windows Forms .NET)</span></span>](../input-mouse/events.md)
- <xref:System.Windows.Forms.SendKeys>
- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.KeyDown>
- <xref:System.Windows.Forms.Control.KeyPress>
