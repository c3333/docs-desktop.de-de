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
# <a name="how-to-handle-keyboard-input-messages-in-the-form-windows-forms-net"></a><span data-ttu-id="9bb4c-103">Verarbeiten von Tastatureingabemeldungen im Formular (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="9bb4c-103">How to handle keyboard input messages in the form (Windows Forms .NET)</span></span>

<span data-ttu-id="9bb4c-104">Windows Forms bieten die Möglichkeit, Tastatureingaben auf Formularebene zu behandeln, bevor die Eingaben an ein Steuerelement weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9bb4c-104">Windows Forms provides the ability to handle keyboard messages at the form level, before the messages reach a control.</span></span> <span data-ttu-id="9bb4c-105">In diesem Artikel wird erläutert, wie Sie diese Aufgabe ausführen.</span><span class="sxs-lookup"><span data-stu-id="9bb4c-105">This article shows how to accomplish this task.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="handle-a-keyboard-message"></a><span data-ttu-id="9bb4c-106">Verarbeiten einer Tastaturmeldung</span><span class="sxs-lookup"><span data-stu-id="9bb4c-106">Handle a keyboard message</span></span>

<span data-ttu-id="9bb4c-107">Verarbeiten Sie das Ereignis <xref:System.Windows.Forms.Control.KeyPress> oder <xref:System.Windows.Forms.Control.KeyDown> des aktiven Formulars, und legen Sie die <xref:System.Windows.Forms.Form.KeyPreview%2A>-Eigenschaft des Formulars auf `true` fest.</span><span class="sxs-lookup"><span data-stu-id="9bb4c-107">Handle the <xref:System.Windows.Forms.Control.KeyPress> or <xref:System.Windows.Forms.Control.KeyDown> event of the active form and set the <xref:System.Windows.Forms.Form.KeyPreview%2A> property of the form to `true`.</span></span> <span data-ttu-id="9bb4c-108">Diese Eigenschaft bewirkt, dass die Tastatureingabe vom Formular empfangen wird, bevor sie Steuerelemente im Formular erreicht.</span><span class="sxs-lookup"><span data-stu-id="9bb4c-108">This property causes the keyboard to be received by the form before they reach any controls on the form.</span></span> <span data-ttu-id="9bb4c-109">Im folgenden Codebeispiel wird das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis verarbeitet, indem alle Zahlentasten erkannt und <kbd>1</kbd>, <kbd>4</kbd> und <kbd>7</kbd> verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9bb4c-109">The following code example handles the <xref:System.Windows.Forms.Control.KeyPress> event by detecting all of the number keys and consuming <kbd>1</kbd>, <kbd>4</kbd>, and <kbd>7</kbd>.</span></span>

:::code language="csharp" source="snippets/how-to-handle-forms/csharp/Form1.cs" id="HandleKey":::
:::code language="vb" source="snippets/how-to-handle-forms/vb/Form1.vb" id="HandleKey":::

## <a name="see-also"></a><span data-ttu-id="9bb4c-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bb4c-110">See also</span></span>

- [<span data-ttu-id="9bb4c-111">Übersicht über die Verwendung der Tastatur (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="9bb4c-111">Overview of using the keyboard (Windows Forms .NET)</span></span>](overview.md)
- [<span data-ttu-id="9bb4c-112">Verwenden von Tastaturereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="9bb4c-112">Using keyboard events (Windows Forms .NET)</span></span>](events.md)
- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.ModifierKeys>
- <xref:System.Windows.Forms.Control.KeyDown>
- <xref:System.Windows.Forms.Control.KeyPress>
