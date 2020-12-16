---
title: Überprüfen, welche Zusatztaste gedrückt wird
description: Hier erfahren Sie, wie Sie erkennen können, wann die Tasten SHIFT, ALT oder STRG in Windows Forms für .NET gedrückt werden.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- keyboard input
- shift keys
- events [Windows Forms], mouse
- Keys.ControlKey enumeration member
- keys [Windows Forms], control keys
- user input [Windows Forms], checking for keyboard
- keys [Windows Forms], determining last pressed
- keys [Windows Forms], shift keys
- keys [Windows Forms], modifier keys
- control keys
- keys [Windows Forms], alt keys
- alt keys
- Keys.Shift enumeration member
- events [Windows Forms], keyboard
- keyboards [Windows Forms], keyboard input
- Keys.Alt enumeration member
- modifier keys
ms.openlocfilehash: 7feda0f604e1cb40b34f7bf42aa122d817a5a95e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942080"
---
# <a name="how-to-check-for-modifier-key-presses-windows-forms-net"></a><span data-ttu-id="43cd2-103">Überprüfen der Tastendruckaktion für Zusatztasten (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="43cd2-103">How to check for modifier key presses (Windows Forms .NET)</span></span>

<span data-ttu-id="43cd2-104">Wenn der Benutzer Tasten in Ihrer Anwendung drückt, können Sie gedrückte Zusatztasten wie <kbd>SHIFT</kbd>, <kbd>ALT</kbd> und <kbd>STRG</kbd> überwachen.</span><span class="sxs-lookup"><span data-stu-id="43cd2-104">As the user types keys into your application, you can monitor for pressed modifier keys such as the <kbd>SHIFT</kbd>, <kbd>ALT</kbd>, and <kbd>CTRL</kbd>.</span></span> <span data-ttu-id="43cd2-105">Wenn eine Zusatztaste in Kombination mit anderen Tasten oder sogar einem Mausklick gedrückt wird, kann die Anwendung entsprechend reagieren.</span><span class="sxs-lookup"><span data-stu-id="43cd2-105">When a modifier key is pressed in combination with other keys or even a mouse click, your application can respond appropriately.</span></span> <span data-ttu-id="43cd2-106">Wenn Sie beispielsweise die Taste <kbd>S</kbd> drücken, wird möglicherweise ein „s“ auf dem Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="43cd2-106">For example, pressing the <kbd>S</kbd> key may cause an "s" to appear on the screen.</span></span> <span data-ttu-id="43cd2-107">Wenn die Tasten <kbd>STRG+S</kbd> gedrückt werden, kann das aktuelle Dokument gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="43cd2-107">If the keys <kbd>CTRL+S</kbd> are pressed, instead, the current document may be saved.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

<span data-ttu-id="43cd2-108">Wenn Sie das <xref:System.Windows.Forms.Control.KeyDown>-Ereignis verarbeiten, gibt die vom Ereignishandler empfangene <xref:System.Windows.Forms.KeyEventArgs.Modifiers?displayProperty=nameWithType>-Eigenschaft an, welche Zusatztasten gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="43cd2-108">If you handle the <xref:System.Windows.Forms.Control.KeyDown> event, the <xref:System.Windows.Forms.KeyEventArgs.Modifiers?displayProperty=nameWithType> property received by the event handler specifies which modifier keys are pressed.</span></span> <span data-ttu-id="43cd2-109">Außerdem gibt die <xref:System.Windows.Forms.KeyEventArgs.KeyData?displayProperty=nameWithType>-Eigenschaft das Zeichen an, das zusammen mit allen beliebigen Zusatztasten in Kombination mit einem bitweisen OR gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="43cd2-109">Also, the <xref:System.Windows.Forms.KeyEventArgs.KeyData?displayProperty=nameWithType> property specifies the character that was pressed along with any modifier keys combined with a bitwise OR.</span></span>

<span data-ttu-id="43cd2-110">Wenn Sie das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis oder ein Mausereignis verarbeiten, empfängt der Ereignishandler diese Informationen nicht.</span><span class="sxs-lookup"><span data-stu-id="43cd2-110">If you're handling the <xref:System.Windows.Forms.Control.KeyPress> event or a mouse event, the event handler doesn't receive this information.</span></span> <span data-ttu-id="43cd2-111">Verwenden Sie die <xref:System.Windows.Forms.Control.ModifierKeys%2A>-Eigenschaft der <xref:System.Windows.Forms.Control>-Klasse, um einen Tastenmodifizierer zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="43cd2-111">Use the <xref:System.Windows.Forms.Control.ModifierKeys%2A> property of the <xref:System.Windows.Forms.Control> class to detect a key modifier.</span></span> <span data-ttu-id="43cd2-112">In beiden Fällen müssen Sie ein bitweises AND für den entsprechenden <xref:System.Windows.Forms.Keys>-Wert und den getesteten Wert ausführen.</span><span class="sxs-lookup"><span data-stu-id="43cd2-112">In either case, you must perform a bitwise AND of the appropriate <xref:System.Windows.Forms.Keys> value and the value you're testing.</span></span> <span data-ttu-id="43cd2-113">Die <xref:System.Windows.Forms.Keys>-Enumeration bietet Variationen der einzelnen Zusatztasten, weshalb es wichtig ist, dass Sie den bitweisen AND-Vorgang mit dem korrekten Wert durchführen.</span><span class="sxs-lookup"><span data-stu-id="43cd2-113">The <xref:System.Windows.Forms.Keys> enumeration offers variations of each modifier key, so it's important that you do the bitwise AND check with the correct value.</span></span>

<span data-ttu-id="43cd2-114">Die <kbd>SHIFT-TASTE</kbd> wird beispielsweise durch die folgenden Tastenwerte dargestellt:</span><span class="sxs-lookup"><span data-stu-id="43cd2-114">For example, the <kbd>SHIFT</kbd> key is represented by the following key values:</span></span>

- <xref:System.Windows.Forms.Keys.Shift?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Keys.ShiftKey?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Keys.RShiftKey?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Keys.LShiftKey?displayProperty=nameWithType>

<span data-ttu-id="43cd2-115">Der korrekte Wert zum Testen von <kbd>SHIFT</kbd> als Zusatztaste ist <xref:System.Windows.Forms.Keys.Shift?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="43cd2-115">The correct value to test <kbd>SHIFT</kbd> as a modifier key is <xref:System.Windows.Forms.Keys.Shift?displayProperty=nameWithType>.</span></span> <span data-ttu-id="43cd2-116">Wenn Sie <kbd>STRG</kbd> und <kbd>ALT</kbd> als Modifizierer testen, sollten Sie auf die gleiche Weise die Werte <xref:System.Windows.Forms.Keys.Control?displayProperty=nameWithType> bzw. <xref:System.Windows.Forms.Keys.Alt?displayProperty=nameWithType> verwenden.</span><span class="sxs-lookup"><span data-stu-id="43cd2-116">Similarly, to test for <kbd>CTRL</kbd> and <kbd>ALT</kbd> as modifiers you should use the <xref:System.Windows.Forms.Keys.Control?displayProperty=nameWithType> and <xref:System.Windows.Forms.Keys.Alt?displayProperty=nameWithType> values, respectively.</span></span>

## <a name="detect-modifier-key"></a><span data-ttu-id="43cd2-117">Erkennen von Zusatztasten</span><span class="sxs-lookup"><span data-stu-id="43cd2-117">Detect modifier key</span></span>

<span data-ttu-id="43cd2-118">Sie können ermitteln, ob eine Zusatztaste gedrückt wird, indem Sie die <xref:System.Windows.Forms.Control.ModifierKeys%2A>-Eigenschaft und den <xref:System.Windows.Forms.Keys>-Enumerationswert mit einem bitweisen AND-Operator vergleichen.</span><span class="sxs-lookup"><span data-stu-id="43cd2-118">Detect if a modifier key is pressed by comparing the <xref:System.Windows.Forms.Control.ModifierKeys%2A> property and the <xref:System.Windows.Forms.Keys> enumeration value with a bitwise AND operator.</span></span>

<span data-ttu-id="43cd2-119">Im folgenden Codebeispiel wird veranschaulicht, wie bestimmt wird, ob die <kbd>SHIFT-TASTE</kbd> in den Ereignishandlern <xref:System.Windows.Forms.Control.KeyPress> und <xref:System.Windows.Forms.Control.KeyDown> gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="43cd2-119">The following code example shows how to determine whether the <kbd>SHIFT</kbd> key is pressed within the <xref:System.Windows.Forms.Control.KeyPress> and <xref:System.Windows.Forms.Control.KeyDown> event handlers.</span></span>

:::code language="csharp" source="snippets/how-to-check-modifier-key/csharp/Form1.cs" id="DetectModifier":::
:::code language="vb" source="snippets/how-to-check-modifier-key/vb/Form1.vb" id="DetectModifier":::

## <a name="see-also"></a><span data-ttu-id="43cd2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43cd2-120">See also</span></span>

- [<span data-ttu-id="43cd2-121">Übersicht über die Verwendung der Tastatur (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="43cd2-121">Overview of using the keyboard (Windows Forms .NET)</span></span>](overview.md)
- [<span data-ttu-id="43cd2-122">Verwenden von Tastaturereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="43cd2-122">Using keyboard events (Windows Forms .NET)</span></span>](events.md)
- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.ModifierKeys>
- <xref:System.Windows.Forms.Control.KeyDown>
- <xref:System.Windows.Forms.Control.KeyPress>
