---
title: Ändern von Tastaturtastenereignissen
description: Hier erfahren Sie, wie Sie eine Tastatureingabe abfangen und dann ändern, welche Taste in einer Windows Forms-.NET-Anwendung gedrückt wird.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- keyboard input [Windows Forms], modifying
- modifying keyboard input
- Windows Forms, modifying keyboard input
- keyboards [Windows Forms], keyboard input
ms.openlocfilehash: 94a003a8eb5fbffd9dbaf817a3ce95ca93a7d370
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942040"
---
# <a name="how-to-modify-keyboard-key-events-windows-forms-net"></a><span data-ttu-id="78a28-103">Ändern von Tastaturtastenereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="78a28-103">How to modify keyboard key events (Windows Forms .NET)</span></span>

<span data-ttu-id="78a28-104">Windows Forms bietet die Möglichkeit, Tastatureingaben zu nutzen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="78a28-104">Windows Forms provides the ability to consume and modify keyboard input.</span></span> <span data-ttu-id="78a28-105">Die Nutzung einer Taste bezieht sich auf die Behandlung einer Taste innerhalb einer Methode oder eines Ereignishandlers, sodass andere Methoden und Ereignisse weiter unten in der Meldungswarteschlange den Tastenwert nicht empfangen.</span><span class="sxs-lookup"><span data-stu-id="78a28-105">Consuming a key refers to handling a key within a method or event handler so that other methods and events further down the message queue don't receive the key value.</span></span> <span data-ttu-id="78a28-106">Das Ändern einer Taste bezieht sich auf das Ändern des Werts einer Taste, sodass Methoden und Ereignishandler weiter unten in der Meldungswarteschlange einen anderen Tastenwert empfangen.</span><span class="sxs-lookup"><span data-stu-id="78a28-106">And, modifying a key refers to modifying the value of a key so that methods and event handlers further down the message queue receive a different key value.</span></span> <span data-ttu-id="78a28-107">In diesem Artikel wird erläutert, wie Sie diese Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="78a28-107">This article shows how to accomplish these tasks.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="consume-a-key"></a><span data-ttu-id="78a28-108">Nutzen einer Taste</span><span class="sxs-lookup"><span data-stu-id="78a28-108">Consume a key</span></span>

<span data-ttu-id="78a28-109">Legen Sie in einem <xref:System.Windows.Forms.Control.KeyPress>-Ereignishandler die <xref:System.Windows.Forms.KeyPressEventArgs.Handled%2A>-Eigenschaft der <xref:System.Windows.Forms.KeyPressEventArgs>-Klasse auf `true` fest.</span><span class="sxs-lookup"><span data-stu-id="78a28-109">In a <xref:System.Windows.Forms.Control.KeyPress> event handler, set the <xref:System.Windows.Forms.KeyPressEventArgs.Handled%2A> property of the <xref:System.Windows.Forms.KeyPressEventArgs> class to `true`.</span></span>

<span data-ttu-id="78a28-110">Oder</span><span class="sxs-lookup"><span data-stu-id="78a28-110">-or-</span></span>

<span data-ttu-id="78a28-111">Legen Sie in einem <xref:System.Windows.Forms.Control.KeyDown>-Ereignishandler die <xref:System.Windows.Forms.KeyEventArgs.Handled%2A>-Eigenschaft der <xref:System.Windows.Forms.KeyEventArgs>-Klasse auf `true` fest.</span><span class="sxs-lookup"><span data-stu-id="78a28-111">In a <xref:System.Windows.Forms.Control.KeyDown> event handler, set the <xref:System.Windows.Forms.KeyEventArgs.Handled%2A> property of the <xref:System.Windows.Forms.KeyEventArgs> class to `true`.</span></span>

> [!NOTE]
> <span data-ttu-id="78a28-112">Ein Festlegen der <xref:System.Windows.Forms.KeyEventArgs.Handled%2A>-Eigenschaft im <xref:System.Windows.Forms.Control.KeyDown>-Ereignishandler verhindert nicht, dass das <xref:System.Windows.Forms.Control.KeyPress>- und das <xref:System.Windows.Forms.Control.KeyUp>-Ereignis für die aktuelle Tastatureingabe ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="78a28-112">Setting the <xref:System.Windows.Forms.KeyEventArgs.Handled%2A> property in the <xref:System.Windows.Forms.Control.KeyDown> event handler does not prevent the <xref:System.Windows.Forms.Control.KeyPress> and <xref:System.Windows.Forms.Control.KeyUp> events from being raised for the current keystroke.</span></span> <span data-ttu-id="78a28-113">Verwenden Sie die <xref:System.Windows.Forms.KeyEventArgs.SuppressKeyPress%2A>-Eigenschaft für diesen Zweck.</span><span class="sxs-lookup"><span data-stu-id="78a28-113">Use the <xref:System.Windows.Forms.KeyEventArgs.SuppressKeyPress%2A> property for this purpose.</span></span>

<span data-ttu-id="78a28-114">Im folgenden Beispiel wird das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis verarbeitet, um die Tasten für die Zeichen `A` und `a` zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="78a28-114">The following example handles the <xref:System.Windows.Forms.Control.KeyPress> event to consume the `A` and `a` character keys.</span></span> <span data-ttu-id="78a28-115">Diese Tasten können nicht in das Textfeld eingegeben werden:</span><span class="sxs-lookup"><span data-stu-id="78a28-115">Those keys can't be typed into the text box:</span></span>

:::code language="csharp" source="snippets/how-to-change-key-press/csharp/Form1.cs" id="ConsumeKey":::
:::code language="vb" source="snippets/how-to-change-key-press/vb/Form1.vb" id="ConsumeKey":::

## <a name="modify-a-standard-character-key"></a><span data-ttu-id="78a28-116">Ändern einer Standardzeichentaste</span><span class="sxs-lookup"><span data-stu-id="78a28-116">Modify a standard character key</span></span>

<span data-ttu-id="78a28-117">Legen Sie in einem <xref:System.Windows.Forms.Control.KeyPress>-Ereignishandler die <xref:System.Windows.Forms.KeyPressEventArgs.KeyChar%2A>-Eigenschaft der <xref:System.Windows.Forms.KeyPressEventArgs>-Klasse auf den Wert der neuen Zeichentaste fest.</span><span class="sxs-lookup"><span data-stu-id="78a28-117">In a <xref:System.Windows.Forms.Control.KeyPress> event handler, set the <xref:System.Windows.Forms.KeyPressEventArgs.KeyChar%2A> property of the <xref:System.Windows.Forms.KeyPressEventArgs> class to the value of the new character key.</span></span>

<span data-ttu-id="78a28-118">Im folgenden Beispiel wird das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis verarbeitet, um die Tasten für die Zeichen `A` und `a` in `!` zu ändern:</span><span class="sxs-lookup"><span data-stu-id="78a28-118">The following example handles the <xref:System.Windows.Forms.Control.KeyPress> event to change any `A` and `a` character keys to `!`:</span></span>

:::code language="csharp" source="snippets/how-to-change-key-press/csharp/Form1.cs" id="ModifyKey":::
:::code language="vb" source="snippets/how-to-change-key-press/vb/Form1.vb" id="ModifyKey":::

## <a name="modify-a-non-character-key"></a><span data-ttu-id="78a28-119">Ändern einer Nichtzeichentaste</span><span class="sxs-lookup"><span data-stu-id="78a28-119">Modify a non-character key</span></span>

<span data-ttu-id="78a28-120">Sie können Tastendruckaktionen für Nichtzeichentasten nur ändern, indem die <xref:System.Windows.Forms.Control.PreProcessMessage%2A>-Methode vom Steuerelement geerbt und überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="78a28-120">You can only modify non-character key presses by inheriting from the control and overriding the <xref:System.Windows.Forms.Control.PreProcessMessage%2A> method.</span></span> <span data-ttu-id="78a28-121">Wenn die Eingabe <xref:System.Windows.Forms.Message> an das Steuerelement gesendet wird, wird sie verarbeitet, bevor das Steuerelement Ereignisse auslöst.</span><span class="sxs-lookup"><span data-stu-id="78a28-121">As the   input <xref:System.Windows.Forms.Message> is sent to the control, it's processed before the control raising events.</span></span> <span data-ttu-id="78a28-122">Sie können diese Nachrichten abfangen, um sie zu ändern oder zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="78a28-122">You can intercept these messages to modify or block them.</span></span>

<span data-ttu-id="78a28-123">Im folgenden Codebeispiel wird veranschaulicht, wie Sie mit der <xref:System.Windows.Forms.Message.WParam%2A>-Eigenschaft des <xref:System.Windows.Forms.Message>-Parameters die gedrückte Taste ändern.</span><span class="sxs-lookup"><span data-stu-id="78a28-123">The following code example demonstrates how to use the <xref:System.Windows.Forms.Message.WParam%2A> property of the <xref:System.Windows.Forms.Message> parameter to change the key pressed.</span></span> <span data-ttu-id="78a28-124">Dieser Code erkennt eine Taste von <kbd>F1</kbd> bis <kbd>F10</kbd> und übersetzt die Taste in eine numerische Taste von <kbd>0</kbd> bis <kbd>9</kbd> (wobei <kbd>F10</kbd> <kbd>0</kbd> ist).</span><span class="sxs-lookup"><span data-stu-id="78a28-124">This code detects a key from <kbd>F1</kbd> through <kbd>F10</kbd> and translates the key into a numeric key ranging from <kbd>0</kbd> through <kbd>9</kbd> (where <kbd>F10</kbd> maps to <kbd>0</kbd>).</span></span>

:::code language="csharp" source="snippets/how-to-change-key-press/csharp/NewTextBox.cs" id="PreProcessMessage":::
:::code language="vb" source="snippets/how-to-change-key-press/vb/NewTextBox.vb" id="PreProcessMessage":::

## <a name="see-also"></a><span data-ttu-id="78a28-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78a28-125">See also</span></span>

- [<span data-ttu-id="78a28-126">Übersicht über die Verwendung der Tastatur (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="78a28-126">Overview of using the keyboard (Windows Forms .NET)</span></span>](overview.md)
- [<span data-ttu-id="78a28-127">Verwenden von Tastaturereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="78a28-127">Using keyboard events (Windows Forms .NET)</span></span>](events.md)
- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.KeyDown>
- <xref:System.Windows.Forms.Control.KeyPress>
