---
title: 'Vorgehensweise: Bestimmen, welche Zusatztaste gedrückt wurde'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
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
ms.assetid: 1e184048-0ae3-4067-a200-d4ba31dbc2cb
ms.openlocfilehash: 9140834b4849ecb143ac57a6f6ae20e2d870859b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972299"
---
# <a name="how-to-determine-which-modifier-key-was-pressed"></a><span data-ttu-id="ad83f-102">Vorgehensweise: Bestimmen, welche Zusatztaste gedrückt wurde</span><span class="sxs-lookup"><span data-stu-id="ad83f-102">How to: Determine Which Modifier Key Was Pressed</span></span>

<span data-ttu-id="ad83f-103">Wenn Sie eine Anwendung erstellen, die die Tastatureingaben des Benutzers akzeptiert, können Sie auch auf Modifizierertasten wie die UMSCHALTTASTE, die Alt-Taste und die STRG-Taste überwachen.</span><span class="sxs-lookup"><span data-stu-id="ad83f-103">When you create an application that accepts the user's keystrokes, you may also want to monitor for modifier keys such as the SHIFT, ALT, and CTRL keys.</span></span> <span data-ttu-id="ad83f-104">Wenn eine Modifizierertaste in Kombination mit anderen Schlüsseln oder mit Mausklicks gedrückt wird, kann die Anwendung entsprechend reagieren.</span><span class="sxs-lookup"><span data-stu-id="ad83f-104">When a modifier key is pressed in combination with other keys, or with mouse clicks, your application can respond appropriately.</span></span> <span data-ttu-id="ad83f-105">Wenn z. b. der Buchstabe S gedrückt ist, kann dies dazu führen, dass auf dem Bildschirm nur ein "s" angezeigt wird, aber wenn die Tasten STRG + S gedrückt werden, kann das aktuelle Dokument gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ad83f-105">For example, if the letter S is pressed, this may simply cause an "s" to appear on the screen, but if the keys CTRL+S are pressed, the current document may be saved.</span></span> <span data-ttu-id="ad83f-106">Wenn Sie das- <xref:System.Windows.Forms.Control.KeyDown> Ereignis behandeln, <xref:System.Windows.Forms.KeyEventArgs.Modifiers%2A> gibt die-Eigenschaft des-Objekts, das <xref:System.Windows.Forms.KeyEventArgs> vom Ereignishandler empfangen wird, an, welche Modifizierertasten gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="ad83f-106">If you handle the <xref:System.Windows.Forms.Control.KeyDown> event, the <xref:System.Windows.Forms.KeyEventArgs.Modifiers%2A> property of the <xref:System.Windows.Forms.KeyEventArgs> received by the event handler specifies which modifier keys are pressed.</span></span> <span data-ttu-id="ad83f-107">Alternativ gibt die- <xref:System.Windows.Forms.KeyEventArgs.KeyData%2A> Eigenschaft von <xref:System.Windows.Forms.KeyEventArgs> das Zeichen an, das gedrückt wurde, sowie alle Modifizierertasten, die mit einem bitweisen OR kombiniert wurden.</span><span class="sxs-lookup"><span data-stu-id="ad83f-107">Alternatively, the <xref:System.Windows.Forms.KeyEventArgs.KeyData%2A> property of <xref:System.Windows.Forms.KeyEventArgs> specifies the character that was pressed as well as any modifier keys combined with a bitwise OR.</span></span> <span data-ttu-id="ad83f-108">Wenn Sie jedoch das- <xref:System.Windows.Forms.Control.KeyPress> Ereignis oder ein Maus Ereignis verarbeiten, empfängt der Ereignishandler diese Informationen nicht.</span><span class="sxs-lookup"><span data-stu-id="ad83f-108">However, if you are handling the <xref:System.Windows.Forms.Control.KeyPress> event or a mouse event, the event handler does not receive this information.</span></span> <span data-ttu-id="ad83f-109">In diesem Fall müssen Sie die- <xref:System.Windows.Forms.Control.ModifierKeys%2A> Eigenschaft der- <xref:System.Windows.Forms.Control> Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad83f-109">In this case, you must use the <xref:System.Windows.Forms.Control.ModifierKeys%2A> property of the <xref:System.Windows.Forms.Control> class.</span></span> <span data-ttu-id="ad83f-110">In beiden Fällen müssen Sie ein bitweises and mit dem entsprechenden <xref:System.Windows.Forms.Keys> Wert und dem zu testenden Wert ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad83f-110">In either case, you must perform a bitwise AND of the appropriate <xref:System.Windows.Forms.Keys> value and the value you are testing.</span></span> <span data-ttu-id="ad83f-111">Die- <xref:System.Windows.Forms.Keys> Enumeration bietet Variationen der einzelnen modifiziererschlüssel. Daher ist es wichtig, dass Sie das bitweise and mit dem korrekten Wert ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad83f-111">The <xref:System.Windows.Forms.Keys> enumeration offers variations of each modifier key, so it is important that you perform the bitwise AND with the correct value.</span></span> <span data-ttu-id="ad83f-112">Die UMSCHALTTASTE wird z. b. durch <xref:System.Windows.Forms.Keys.Shift> , <xref:System.Windows.Forms.Keys.ShiftKey> <xref:System.Windows.Forms.Keys.RShiftKey> und <xref:System.Windows.Forms.Keys.LShiftKey> den korrekten Wert zum Testen der Umschalttaste dargestellt, wenn eine Modifizierertaste ist <xref:System.Windows.Forms.Keys.Shift> .</span><span class="sxs-lookup"><span data-stu-id="ad83f-112">For example, the SHIFT key is represented by <xref:System.Windows.Forms.Keys.Shift>, <xref:System.Windows.Forms.Keys.ShiftKey>, <xref:System.Windows.Forms.Keys.RShiftKey> and <xref:System.Windows.Forms.Keys.LShiftKey> The correct value to test SHIFT as a modifier key is <xref:System.Windows.Forms.Keys.Shift>.</span></span> <span data-ttu-id="ad83f-113">Entsprechend sollten Sie zum Testen von STRG und alt als modifiziererer den <xref:System.Windows.Forms.Keys.Control> -Wert und den- <xref:System.Windows.Forms.Keys.Alt> Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad83f-113">Similarly, to test for CTRL and ALT as modifiers you should use the <xref:System.Windows.Forms.Keys.Control> and <xref:System.Windows.Forms.Keys.Alt> values, respectively.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ad83f-114">Visual Basic Programmierer können auch über die-Eigenschaft auf Schlüsselinformationen zugreifen. <xref:Microsoft.VisualBasic.Devices.Computer.Keyboard%2A></span><span class="sxs-lookup"><span data-stu-id="ad83f-114">Visual Basic programmers can also access key information through the <xref:Microsoft.VisualBasic.Devices.Computer.Keyboard%2A> property</span></span>  
  
### <a name="to-determine-which-modifier-key-was-pressed"></a><span data-ttu-id="ad83f-115">So bestimmen Sie, welche Modifizierertaste gedrückt wurde</span><span class="sxs-lookup"><span data-stu-id="ad83f-115">To determine which modifier key was pressed</span></span>  
  
- <span data-ttu-id="ad83f-116">Verwenden Sie den bitweisen `AND` Operator mit der <xref:System.Windows.Forms.Control.ModifierKeys%2A> -Eigenschaft und einem Wert der- <xref:System.Windows.Forms.Keys> Enumeration, um zu bestimmen, ob eine bestimmte Modifizierertaste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="ad83f-116">Use the bitwise `AND` operator with the <xref:System.Windows.Forms.Control.ModifierKeys%2A> property and a value of the <xref:System.Windows.Forms.Keys> enumeration to determine whether a particular modifier key is pressed.</span></span> <span data-ttu-id="ad83f-117">Im folgenden Codebeispiel wird veranschaulicht, wie bestimmt wird, ob die UMSCHALTTASTE innerhalb eines- <xref:System.Windows.Forms.Control.KeyPress> Ereignis Handlers gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="ad83f-117">The following code example shows how to determine whether the SHIFT key is pressed within a <xref:System.Windows.Forms.Control.KeyPress> event handler.</span></span>  
  
     [!code-cpp[System.Windows.Forms.DetermineModifierKey#5](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DetermineModifierKey/cpp/form1.cpp#5)]
     [!code-csharp[System.Windows.Forms.DetermineModifierKey#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DetermineModifierKey/CS/form1.cs#5)]
     [!code-vb[System.Windows.Forms.DetermineModifierKey#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DetermineModifierKey/VB/form1.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="ad83f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad83f-118">See also</span></span>

- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.ModifierKeys%2A>
- [<span data-ttu-id="ad83f-119">Tastatureingaben in einer Windows Forms-Anwendung</span><span class="sxs-lookup"><span data-stu-id="ad83f-119">Keyboard Input in a Windows Forms Application</span></span>](keyboard-input-in-a-windows-forms-application.md)
- <span data-ttu-id="ad83f-120">[Gewusst wie: bestimmen, ob CapsLock in Visual Basic](/previous-versions/visualstudio/visual-studio-2010/9c9d1fz9(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="ad83f-120">[How to: Determine If CapsLock is On in Visual Basic](/previous-versions/visualstudio/visual-studio-2010/9c9d1fz9(v=vs.100))</span></span>
