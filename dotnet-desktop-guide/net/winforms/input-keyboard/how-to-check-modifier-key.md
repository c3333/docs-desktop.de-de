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
# <a name="how-to-check-for-modifier-key-presses-windows-forms-net"></a>Überprüfen der Tastendruckaktion für Zusatztasten (Windows Forms .NET)

Wenn der Benutzer Tasten in Ihrer Anwendung drückt, können Sie gedrückte Zusatztasten wie <kbd>SHIFT</kbd>, <kbd>ALT</kbd> und <kbd>STRG</kbd> überwachen. Wenn eine Zusatztaste in Kombination mit anderen Tasten oder sogar einem Mausklick gedrückt wird, kann die Anwendung entsprechend reagieren. Wenn Sie beispielsweise die Taste <kbd>S</kbd> drücken, wird möglicherweise ein „s“ auf dem Bildschirm angezeigt. Wenn die Tasten <kbd>STRG+S</kbd> gedrückt werden, kann das aktuelle Dokument gespeichert werden.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

Wenn Sie das <xref:System.Windows.Forms.Control.KeyDown>-Ereignis verarbeiten, gibt die vom Ereignishandler empfangene <xref:System.Windows.Forms.KeyEventArgs.Modifiers?displayProperty=nameWithType>-Eigenschaft an, welche Zusatztasten gedrückt werden. Außerdem gibt die <xref:System.Windows.Forms.KeyEventArgs.KeyData?displayProperty=nameWithType>-Eigenschaft das Zeichen an, das zusammen mit allen beliebigen Zusatztasten in Kombination mit einem bitweisen OR gedrückt wurde.

Wenn Sie das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis oder ein Mausereignis verarbeiten, empfängt der Ereignishandler diese Informationen nicht. Verwenden Sie die <xref:System.Windows.Forms.Control.ModifierKeys%2A>-Eigenschaft der <xref:System.Windows.Forms.Control>-Klasse, um einen Tastenmodifizierer zu erkennen. In beiden Fällen müssen Sie ein bitweises AND für den entsprechenden <xref:System.Windows.Forms.Keys>-Wert und den getesteten Wert ausführen. Die <xref:System.Windows.Forms.Keys>-Enumeration bietet Variationen der einzelnen Zusatztasten, weshalb es wichtig ist, dass Sie den bitweisen AND-Vorgang mit dem korrekten Wert durchführen.

Die <kbd>SHIFT-TASTE</kbd> wird beispielsweise durch die folgenden Tastenwerte dargestellt:

- <xref:System.Windows.Forms.Keys.Shift?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Keys.ShiftKey?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Keys.RShiftKey?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Keys.LShiftKey?displayProperty=nameWithType>

Der korrekte Wert zum Testen von <kbd>SHIFT</kbd> als Zusatztaste ist <xref:System.Windows.Forms.Keys.Shift?displayProperty=nameWithType>. Wenn Sie <kbd>STRG</kbd> und <kbd>ALT</kbd> als Modifizierer testen, sollten Sie auf die gleiche Weise die Werte <xref:System.Windows.Forms.Keys.Control?displayProperty=nameWithType> bzw. <xref:System.Windows.Forms.Keys.Alt?displayProperty=nameWithType> verwenden.

## <a name="detect-modifier-key"></a>Erkennen von Zusatztasten

Sie können ermitteln, ob eine Zusatztaste gedrückt wird, indem Sie die <xref:System.Windows.Forms.Control.ModifierKeys%2A>-Eigenschaft und den <xref:System.Windows.Forms.Keys>-Enumerationswert mit einem bitweisen AND-Operator vergleichen.

Im folgenden Codebeispiel wird veranschaulicht, wie bestimmt wird, ob die <kbd>SHIFT-TASTE</kbd> in den Ereignishandlern <xref:System.Windows.Forms.Control.KeyPress> und <xref:System.Windows.Forms.Control.KeyDown> gedrückt wird.

:::code language="csharp" source="snippets/how-to-check-modifier-key/csharp/Form1.cs" id="DetectModifier":::
:::code language="vb" source="snippets/how-to-check-modifier-key/vb/Form1.vb" id="DetectModifier":::

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Verwendung der Tastatur (Windows Forms .NET)](overview.md)
- [Verwenden von Tastaturereignissen (Windows Forms .NET)](events.md)
- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.ModifierKeys>
- <xref:System.Windows.Forms.Control.KeyDown>
- <xref:System.Windows.Forms.Control.KeyPress>
