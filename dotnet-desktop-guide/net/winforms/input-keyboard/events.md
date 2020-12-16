---
title: Verwenden von Tastaturereignissen
description: Hier finden Sie eine Übersicht über die Verwendung von Tastaturereignissen zum Verarbeiten von Tastatureingaben. Dieser Artikel enthält eine Liste der mit der Tastatur verknüpften Ereignisse und Verwendungszwecke.
ms.date: 10/26/2020
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- KeyPress event [Windows Forms]
- keyboards [Windows Forms], keyboard events
- KeyUp event
- KeyDown event
- keyboard events
- events [Windows Forms], keyboard
ms.openlocfilehash: 3e7493c9841fa036aa9d18aa00a1322d9758cbb1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942380"
---
# <a name="using-keyboard-events-windows-forms-net"></a>Verwenden von Tastaturereignissen (Windows Forms .NET)

Die meisten Windows Forms-Programme verarbeiten Tastatureingaben, indem sie Tastaturereignisse behandeln. Dieser Artikel bietet eine Übersicht über die Tastaturereignisse, einschließlich Details dazu, wann jedes Ereignis verwendet wird sowie zu den Daten, die für jedes Ereignis übergeben werden. Weitere Informationen zu Ereignissen im Allgemeinen finden Sie unter [Übersicht zu Ereignissen (Windows Forms .NET)](../forms/events.md).

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="keyboard-events"></a>Tastaturereignisse

Windows Forms stellen zwei Ereignisse bereit, die auftreten, wenn ein Benutzer eine Taste auf der Tastatur drückt, und ein Ereignis, wenn der Benutzer die Taste loslässt:

- Das <xref:System.Windows.Forms.Control.KeyDown>-Ereignis tritt einmal auf.
- Das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis, das mehrfach auftreten kann, wenn der Benutzer die gleiche Taste gedrückt hält.
- Das <xref:System.Windows.Forms.Control.KeyUp>-Ereignis tritt einmal auf, wenn der Benutzer eine Taste loslässt.

Wenn der Benutzer eine Taste drückt, ermittelt Windows Forms , welches Ereignis ausgelöst werden soll, und zwar basierend darauf, ob die Tastatureingabe eine Zeichentaste oder eine Steuer- bzw. Funktionstaste ist. Weitere Informationen zu Zeichentasten und physischen Tasten finden Sie unter [Tastaturübersicht: Tastaturereignisse](overview.md#keyboard-events).

In der folgenden Tabelle werden diese drei Tastaturereignisse beschrieben.

|Tastaturereignis|BESCHREIBUNG|Ergebnisse|
|--------------------|-----------------|-------------|
|<xref:System.Windows.Forms.Control.KeyDown>|Dieses Ereignis wird ausgelöst, wenn der Benutzer eine Steuer- bzw. Funktionstaste drückt.|Der Handler für <xref:System.Windows.Forms.Control.KeyDown> erhält Folgendes:<br /><br /> <ul><li>Einen <xref:System.Windows.Forms.KeyEventArgs>-Parameter, der die <xref:System.Windows.Forms.KeyEventArgs.KeyCode%2A>-Eigenschaft bereitstellt (womit eine Steuer- oder Funktionstaste angegeben wird).</li><li>Die <xref:System.Windows.Forms.KeyEventArgs.Modifiers%2A>-Eigenschaft (UMSCHALT, STRG oder ALT).</li><li>Die <xref:System.Windows.Forms.KeyEventArgs.KeyData%2A>-Eigenschaft (wodurch der Tastencode und der Modifizierer kombiniert werden). Der <xref:System.Windows.Forms.KeyEventArgs>-Parameter stellt zudem Folgendes bereit:<br /><br /> <ul><li>Die <xref:System.Windows.Forms.KeyEventArgs.Handled%2A>-Eigenschaft, die festgelegt werden kann, um zu verhindert, dass das zugrunde liegende Steuerelement auf den Tastendruck reagiert.</li><li>Die <xref:System.Windows.Forms.KeyEventArgs.SuppressKeyPress%2A>-Eigenschaft, die verwendet werden kann, um <xref:System.Windows.Forms.Control.KeyPress>- und <xref:System.Windows.Forms.Control.KeyUp>-Eigenschaften für diesen Tastendruck zu unterdrücken.</li></ul></li></ul>|
|<xref:System.Windows.Forms.Control.KeyPress>|Dieses Ereignis wird ausgelöst, wenn der oder die Tastendrücke ein Zeichen bewirken. Wenn der Benutzer beispielsweise die Tasten UMSCHALT und kleines "a" drückt, wird das Zeichen "A" in Großbuchstaben angezeigt.|<xref:System.Windows.Forms.Control.KeyPress> wird nach <xref:System.Windows.Forms.Control.KeyDown> ausgelöst.<br /><br /> <ul><li>Der Handler für <xref:System.Windows.Forms.Control.KeyPress> erhält Folgendes:</li><li>Einen <xref:System.Windows.Forms.KeyPressEventArgs>-Parameter, der den Zeichencode der gedrückten Taste enthält. Dieser Zeichencode ist für jede Kombination aus Zeichentaste und Modifizierertaste eindeutig.<br /><br />     So generiert die Taste "A" beispielsweise:<br /><br /> <ul><li>Den Zeichencode 65 in Verbindung mit der UMSCHALT-TASTE, oder</li><li>97 in Verbindung mit der FESTSTELLTASTE, wenn diese allein gedrückt wird,</li><li>und 1, wenn sie zusammen mit der STRG-TASTE gedrückt wird.</li></ul></li></ul>|
|<xref:System.Windows.Forms.Control.KeyUp>|Dieses Ereignis wird ausgelöst, wenn der Benutzer eine Steuer- bzw. Funktionstaste loslässt.|Der Handler für <xref:System.Windows.Forms.Control.KeyUp> erhält Folgendes:<br /><br /> <ul><li>Einen <xref:System.Windows.Forms.KeyEventArgs>-Parameter.<br /><br /> <ul><li>Dieser stellt die <xref:System.Windows.Forms.KeyEventArgs.KeyCode%2A>-Eigenschaft bereit (womit eine Steuer- oder Funktionstaste angegeben wird).</li><li>Die <xref:System.Windows.Forms.KeyEventArgs.Modifiers%2A>-Eigenschaft (UMSCHALT, STRG oder ALT).</li><li>Die <xref:System.Globalization.SortKey.KeyData%2A>-Eigenschaft (wodurch der Tastencode und der Modifizierer kombiniert werden).</li></ul></li></ul>|

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Verwendung der Tastatur (Windows Forms .NET)](overview.md)
- [Ändern von Tastaturtastenereignissen (Windows Forms .NET)](how-to-change-key-press.md)
- [Überprüfen der Tastendruckaktion für Zusatztasten (Windows Forms .NET)](how-to-check-modifier-key.md)
- [Simulieren von Tastaturereignissen (Windows Forms .NET)](how-to-simulate-events.md)
- [Verarbeiten von Tastatureingabemeldungen im Formular (Windows Forms .NET)](how-to-handle-forms.md)
