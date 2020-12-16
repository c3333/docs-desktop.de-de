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
# <a name="how-to-simulate-keyboard-events-windows-forms-net"></a>Simulieren von Tastaturereignissen (Windows Forms .NET)

Windows Forms stellt einige Optionen zur programmgesteuerten Simulation von Tastatureingaben bereit. Dieser Artikel bietet eine Übersicht über diese Optionen.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="use-sendkeys"></a>Verwenden von SendKeys

Windows Forms stellt die <xref:System.Windows.Forms.SendKeys?displayProperty=fullName>-Klasse bereit, um Tastatureingaben an die aktive Anwendung zu senden. Es gibt zwei Methoden zum Senden von Tastatureingaben an eine Anwendung: <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> und <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType>. Der Unterschied zwischen den beiden Methoden besteht darin, dass `SendWait` im Gegensatz zu `Send` den aktuellen Thread blockiert, wenn die Tastatureingabe gesendet wird, und dann auf eine Antwort wartet. Weitere Informationen zu `SendWait` finden Sie unter [Senden einer Tastatureingabe an eine andere Anwendung](#to-send-a-keystroke-to-a-different-application).

> [!CAUTION]
> Wenn Ihre Anwendung für internationale Verwendung mit unterschiedlichen Tastaturen vorgesehen ist, kann ein Verwenden von <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> zu unvorhersehbaren Ergebnissen führen und sollte vermieden werden.

Im Hintergrund verwendet `SendKeys` eine ältere Windows-Implementierung zum Senden von Eingaben, bei der im Zusammenhang mit modernen Windows-Betriebssystemen möglicherweise ein Fehler auftritt, da hier erwartet wird, dass die Anwendung nicht mit Administratorrechten ausgeführt wird. Wenn bei der älteren Implementierung ein Fehler auftritt, versucht der Code automatisch, die neuere Windows-Implementierung zum Senden von Eingaben zu verwenden. Wenn die <xref:System.Windows.Forms.SendKeys>-Klasse die neue Implementierung verwendet, blockiert die <xref:System.Windows.Forms.SendKeys.SendWait%2A>-Methode zudem den aktuellen Thread nicht mehr, wenn Tastatureingaben an eine andere Anwendung gesendet werden.

> [!IMPORTANT]
> Ist für Ihre Anwendung ein einheitliches, vom Betriebssystem unabhängiges Verhalten erforderlich, können Sie für die <xref:System.Windows.Forms.SendKeys> -Klasse das Verwenden der neuen Implementierung erzwingen, indem Sie die folgende Anwendungseinstellung in Ihre "app.config"-Datei einfügen.
>
> ```xml
> <appSettings>
>   <add key="SendKeys" value="SendInput"/>
> </appSettings>
> ```
>
> Verwenden Sie stattdessen den Wert `"JournalHook"`, wenn die <xref:System.Windows.Forms.SendKeys>-Klasse gezwungen werden soll, _nur_ die vorherige Implementierung zu nutzen.

### <a name="to-send-a-keystroke-to-the-same-application"></a>So senden Sie eine Tastatureingabe an dieselbe Anwendung

Rufen Sie die <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> - oder die <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType> -Methode der <xref:System.Windows.Forms.SendKeys> -Klasse auf. Die angegebenen Tastatureingaben werden vom aktiven Steuerelement der Anwendung empfangen.

Im folgenden Codebeispiel wird `Send` verwendet, um das gleichzeitige Drücken der Tasten <kbd>ALT</kbd> und <kbd>NACH-UNTEN</kbd> zu simulieren. Diese Tastatureingaben bewirken, dass das <xref:System.Windows.Forms.ComboBox>-Steuerelement sein Dropdownmenü anzeigt. In diesem Beispiel wird eine <xref:System.Windows.Forms.Form>-Klasse mit einer <xref:System.Windows.Forms.Button>- und einer <xref:System.Windows.Forms.ComboBox>-Klasse vorausgesetzt.

:::code language="csharp" source="snippets/how-to-simulate-events/csharp/Form1.cs" id="ShowDropDown":::
:::code language="vb" source="snippets/how-to-simulate-events/vb/Form1.vb" id="ShowDropDown":::

### <a name="to-send-a-keystroke-to-a-different-application"></a>So senden Sie eine Tastatureingabe an eine andere Anwendung

Die Methoden <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=nameWithType> und <xref:System.Windows.Forms.SendKeys.SendWait%2A?displayProperty=nameWithType> senden Tastatureingaben an die aktive Anwendung, bei der es sich normalerweise um die Anwendung handelt, über die Sie Tastatureingaben senden. Sie müssen eine andere Anwendung zuerst aktivieren, um Tastatureingaben an diese senden zu können. Da keine verwaltete Methode zum Aktivieren einer anderen Anwendung vorhanden ist, müssen Sie native Windows-Methoden verwenden, um den Fokus auf die andere Anwendung zu lenken. Im folgenden Codebeispiel wird ein Plattformaufruf dazu verwendet, die Methoden `FindWindow` und `SetForegroundWindow` aufzurufen, um das Anwendungsfenster Rechner zu aktivieren, und dann wird `Send` aufgerufen, um einige Berechnungselemente an Rechner zu senden.

Im folgenden Codebeispiel wird `Send` verwendet, um das Drücken von Tasten in der Rechneranwendung unter Windows 10 zu simulieren. Zuerst wird nach einem Anwendungsfenster mit dem Titel `Calculator` gesucht und dieses dann aktiviert. Nach der Aktivierung werden Tastatureingaben zum Berechnen der Summe von „10“ und „10“ gesendet.

:::code language="csharp" source="snippets/how-to-simulate-events/csharp/Form2.cs" id="Calculator":::
:::code language="vb" source="snippets/how-to-simulate-events/vb/Form2.vb" id="Calculator":::

## <a name="use-oneventname-methods"></a>Verwenden von OnEventName-Methoden

Die einfachste Möglichkeit zum Simulieren von Tastaturereignissen besteht darin, eine Methode für das Objekt aufzurufen, das das Ereignis auslöst. Die meisten Ereignisse verfügen über eine entsprechende Methode, die sie aufruft und im Muster `On` gefolgt von `EventName` (z. B. `OnKeyPress`) benannt wird. Diese Option wird normalerweise nur in benutzerdefinierten Steuerelementen und Formularen unterstützt, weil die Methoden geschützt sind und außerhalb des Kontexts des Steuerelements oder Formulars nicht aufgerufen werden können.

Diese geschützten Methoden sind zum Simulieren von Tastaturereignissen verfügbar.

- `OnKeyDown`
- `OnKeyPress`
- `OnKeyUp`

Weitere Informationen zu diesen Ereignissen finden Sie unter [Verwenden von Tastaturereignissen (Windows Forms .NET)](events.md).

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Verwendung der Tastatur (Windows Forms .NET)](overview.md)
- [Verwenden von Tastaturereignissen (Windows Forms .NET)](events.md)
- [Verwenden von Mausereignissen (Windows Forms .NET)](../input-mouse/events.md)
- <xref:System.Windows.Forms.SendKeys>
- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.KeyDown>
- <xref:System.Windows.Forms.Control.KeyPress>
