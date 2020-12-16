---
title: Verarbeiten von Tastatureingaben auf Formularebene
description: Hier erfahren Sie, wie Sie Tastatureingaben für Windows Forms auf Formularebene verarbeiten, bevor Meldungen an ein Steuerelement weitergegeben werden.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- keyboard input [Windows Forms], at form level
- Windows Forms, handling keyboard input
- keyboards [Windows Forms], form-level input
ms.openlocfilehash: 51433eeb32f73385fd74d8a236a273526c1b72ed
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942062"
---
# <a name="how-to-handle-keyboard-input-messages-in-the-form-windows-forms-net"></a>Verarbeiten von Tastatureingabemeldungen im Formular (Windows Forms .NET)

Windows Forms bieten die Möglichkeit, Tastatureingaben auf Formularebene zu behandeln, bevor die Eingaben an ein Steuerelement weitergegeben werden. In diesem Artikel wird erläutert, wie Sie diese Aufgabe ausführen.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="handle-a-keyboard-message"></a>Verarbeiten einer Tastaturmeldung

Verarbeiten Sie das Ereignis <xref:System.Windows.Forms.Control.KeyPress> oder <xref:System.Windows.Forms.Control.KeyDown> des aktiven Formulars, und legen Sie die <xref:System.Windows.Forms.Form.KeyPreview%2A>-Eigenschaft des Formulars auf `true` fest. Diese Eigenschaft bewirkt, dass die Tastatureingabe vom Formular empfangen wird, bevor sie Steuerelemente im Formular erreicht. Im folgenden Codebeispiel wird das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis verarbeitet, indem alle Zahlentasten erkannt und <kbd>1</kbd>, <kbd>4</kbd> und <kbd>7</kbd> verarbeitet werden.

:::code language="csharp" source="snippets/how-to-handle-forms/csharp/Form1.cs" id="HandleKey":::
:::code language="vb" source="snippets/how-to-handle-forms/vb/Form1.vb" id="HandleKey":::

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Verwendung der Tastatur (Windows Forms .NET)](overview.md)
- [Verwenden von Tastaturereignissen (Windows Forms .NET)](events.md)
- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.ModifierKeys>
- <xref:System.Windows.Forms.Control.KeyDown>
- <xref:System.Windows.Forms.Control.KeyPress>
