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
# <a name="how-to-modify-keyboard-key-events-windows-forms-net"></a>Ändern von Tastaturtastenereignissen (Windows Forms .NET)

Windows Forms bietet die Möglichkeit, Tastatureingaben zu nutzen und zu ändern. Die Nutzung einer Taste bezieht sich auf die Behandlung einer Taste innerhalb einer Methode oder eines Ereignishandlers, sodass andere Methoden und Ereignisse weiter unten in der Meldungswarteschlange den Tastenwert nicht empfangen. Das Ändern einer Taste bezieht sich auf das Ändern des Werts einer Taste, sodass Methoden und Ereignishandler weiter unten in der Meldungswarteschlange einen anderen Tastenwert empfangen. In diesem Artikel wird erläutert, wie Sie diese Aufgaben ausführen.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="consume-a-key"></a>Nutzen einer Taste

Legen Sie in einem <xref:System.Windows.Forms.Control.KeyPress>-Ereignishandler die <xref:System.Windows.Forms.KeyPressEventArgs.Handled%2A>-Eigenschaft der <xref:System.Windows.Forms.KeyPressEventArgs>-Klasse auf `true` fest.

Oder

Legen Sie in einem <xref:System.Windows.Forms.Control.KeyDown>-Ereignishandler die <xref:System.Windows.Forms.KeyEventArgs.Handled%2A>-Eigenschaft der <xref:System.Windows.Forms.KeyEventArgs>-Klasse auf `true` fest.

> [!NOTE]
> Ein Festlegen der <xref:System.Windows.Forms.KeyEventArgs.Handled%2A>-Eigenschaft im <xref:System.Windows.Forms.Control.KeyDown>-Ereignishandler verhindert nicht, dass das <xref:System.Windows.Forms.Control.KeyPress>- und das <xref:System.Windows.Forms.Control.KeyUp>-Ereignis für die aktuelle Tastatureingabe ausgelöst werden. Verwenden Sie die <xref:System.Windows.Forms.KeyEventArgs.SuppressKeyPress%2A>-Eigenschaft für diesen Zweck.

Im folgenden Beispiel wird das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis verarbeitet, um die Tasten für die Zeichen `A` und `a` zu verwenden. Diese Tasten können nicht in das Textfeld eingegeben werden:

:::code language="csharp" source="snippets/how-to-change-key-press/csharp/Form1.cs" id="ConsumeKey":::
:::code language="vb" source="snippets/how-to-change-key-press/vb/Form1.vb" id="ConsumeKey":::

## <a name="modify-a-standard-character-key"></a>Ändern einer Standardzeichentaste

Legen Sie in einem <xref:System.Windows.Forms.Control.KeyPress>-Ereignishandler die <xref:System.Windows.Forms.KeyPressEventArgs.KeyChar%2A>-Eigenschaft der <xref:System.Windows.Forms.KeyPressEventArgs>-Klasse auf den Wert der neuen Zeichentaste fest.

Im folgenden Beispiel wird das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis verarbeitet, um die Tasten für die Zeichen `A` und `a` in `!` zu ändern:

:::code language="csharp" source="snippets/how-to-change-key-press/csharp/Form1.cs" id="ModifyKey":::
:::code language="vb" source="snippets/how-to-change-key-press/vb/Form1.vb" id="ModifyKey":::

## <a name="modify-a-non-character-key"></a>Ändern einer Nichtzeichentaste

Sie können Tastendruckaktionen für Nichtzeichentasten nur ändern, indem die <xref:System.Windows.Forms.Control.PreProcessMessage%2A>-Methode vom Steuerelement geerbt und überschrieben wird. Wenn die Eingabe <xref:System.Windows.Forms.Message> an das Steuerelement gesendet wird, wird sie verarbeitet, bevor das Steuerelement Ereignisse auslöst. Sie können diese Nachrichten abfangen, um sie zu ändern oder zu blockieren.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie mit der <xref:System.Windows.Forms.Message.WParam%2A>-Eigenschaft des <xref:System.Windows.Forms.Message>-Parameters die gedrückte Taste ändern. Dieser Code erkennt eine Taste von <kbd>F1</kbd> bis <kbd>F10</kbd> und übersetzt die Taste in eine numerische Taste von <kbd>0</kbd> bis <kbd>9</kbd> (wobei <kbd>F10</kbd> <kbd>0</kbd> ist).

:::code language="csharp" source="snippets/how-to-change-key-press/csharp/NewTextBox.cs" id="PreProcessMessage":::
:::code language="vb" source="snippets/how-to-change-key-press/vb/NewTextBox.vb" id="PreProcessMessage":::

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Verwendung der Tastatur (Windows Forms .NET)](overview.md)
- [Verwenden von Tastaturereignissen (Windows Forms .NET)](events.md)
- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.KeyDown>
- <xref:System.Windows.Forms.Control.KeyPress>
