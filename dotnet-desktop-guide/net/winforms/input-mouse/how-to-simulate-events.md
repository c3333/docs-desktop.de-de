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
# <a name="how-to-simulate-mouse-events-windows-forms-net"></a>Simulieren von Mausereignissen (Windows Forms .NET)

Das Simulieren von Mausereignissen in Windows Forms ist etwas komplexer als das Simulieren von Tastaturereignissen. Windows Forms bietet keine Hilfsprogrammklasse, mit der die Maus verschoben werden kann und Mausklickaktionen aufgerufen werden können. Die einzige Option, die Maus zu steuern, ist die Verwendung nativer Windows-Methoden. Wenn Sie mit einem benutzerdefinierten Steuerelement oder einem Formular arbeiten, können Sie ein Mausereignis simulieren, Sie können die Maus jedoch nicht direkt steuern.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="events"></a>Ereignisse

Die meisten Ereignisse verfügen über eine entsprechende Methode, die sie aufruft und im Muster `On` gefolgt von `EventName` (z. B. `OnMouseMove`) benannt wird. Diese Option wird normalerweise nur in benutzerdefinierten Steuerelementen und Formularen unterstützt, weil die Methoden geschützt sind und außerhalb des Kontexts des Steuerelements oder Formulars nicht aufgerufen werden können. Der Nachteil der Verwendung einer Methode wie `OnMouseMove` besteht darin, dass die Maus so nicht gesteuert werden kann und dass keine Interaktionen mit dem Steuerelement möglich sind. Es wird einfach nur das dazugehörige Ereignis ausgelöst. Wenn Sie beispielsweise das Bewegen des Mauszeigers über einem Element in einer <xref:System.Windows.Forms.ListBox>-Klasse simulieren möchten, reagieren `OnMouseMove` und `ListBox` nicht visuell durch ein hervorgehobenes Element unter dem Cursor.

Diese geschützten Methoden sind zum Simulieren von Mausereignissen verfügbar.

- `OnMouseDown`
- `OnMouseEnter`
- `OnMouseHover`
- `OnMouseLeave`
- `OnMouseMove`
- `OnMouseUp`
- `OnMouseWheel`
- `OnMouseClick`
- `OnMouseDoubleClick`

Weitere Informationen zu diesen Ereignissen finden Sie unter [Verwenden von Mausereignissen (Windows Forms .NET)](events.md).

## <a name="invoke-a-click"></a>Aufrufen eines Klicks

Angesichts der Tatsache, dass auf das Klicken auf ein Steuerelement in den meisten Fällen eine Reaktion erfolgt, z. B. eine Schaltfläche, die Benutzercode aufruft, oder ein Kontrollkästchen, für das der Aktivierungszustand geändert wird, bietet Windows Forms eine einfache Möglichkeit, einen Klick auszulösen. Manche Steuerelemente, z. B. ComboBox-Steuerelemente, reagieren nicht, wenn auf sie geklickt wird. Eine Simulation eines solchen Klicks hat also keine Auswirkung auf das Steuerelement.

### <a name="performclick"></a>PerformClick

Die <xref:System.Windows.Forms.IButtonControl?displayProperty=nameWithType>-Schnittstelle stellt die <xref:System.Windows.Forms.IButtonControl.PerformClick%2A>-Methode bereit, die ein Klick auf das Steuerelement simuliert. Sowohl das <xref:System.Windows.Forms.Button?displayProperty=nameWithType>- als auch das <xref:System.Windows.Forms.LinkLabel?displayProperty=nameWithType>-Steuerelement implementieren diese Schnittstelle.

:::code language="csharp" source="snippets/how-to-simulate-events/csharp/Form1.cs" id="PerformClick":::
:::code language="vb" source="snippets/how-to-simulate-events/vb/Form1.vb" id="PerformClick":::

### <a name="invokeclick"></a>InvokeClick

Verwenden Sie für ein Formular oder ein benutzerdefiniertes Steuerelement die <xref:System.Windows.Forms.Control.InvokeOnClick%2A>-Methode zum Simulieren eines Mausklicks. Dabei handelt es sich um eine geschützte Methode, die nur von innerhalb eines Formulars oder eines abgeleiteten benutzerdefinierten Steuerelements aufgerufen werden kann.

Durch den folgenden Code wird beispielsweise ein Kontrollkästchen in `button1` angeklickt.

:::code language="csharp" source="snippets/how-to-simulate-events/csharp/Form1.cs" id="ClickCheckbox":::
:::code language="vb" source="snippets/how-to-simulate-events/vb/Form1.vb" id="ClickCheckbox":::

## <a name="use-native-windows-methods"></a>Verwenden nativer Windows-Methoden

Windows bietet Methoden, die Sie aufrufen können, um Mausbewegungen und -klicks wie [`User32.dll SendInput`](/windows/win32/api/winuser/nf-winuser-sendinput) und [`User32.dll SetCursorPos`](/windows/win32/api/winuser/nf-winuser-setcursorpos) zu simulieren. Im folgenden Beispiel wird der Mauszeiger in die Mitte eines Steuerelements verschoben:

:::code language="csharp" source="snippets/how-to-simulate-events/csharp/Form2.cs" id="MoveCursor":::
:::code language="vb" source="snippets/how-to-simulate-events/vb/Form2.vb" id="MoveCursor":::

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Mausverwendung (Windows Forms .NET)](overview.md)
- [Verwenden von Mausereignissen (Windows Forms .NET)](events.md)
- [Unterscheiden zwischen Klicks und Doppelklicks (Windows Forms .NET)](how-to-distinguish-between-clicks-and-double-clicks.md)
- [Verwalten von Mauszeigern (Windows Forms .NET)](how-to-manage-cursor-pointer.md)
