---
title: Übersicht über Tastatureingaben
description: Hier erfahren Sie, wie Tastatureingaben in Windows Forms für .NET funktionieren. Tastaturereignisse werden von Formularen und Steuerelementen ausgelöst und stehen für Tasten, die gedrückt, gedrückt gehalten oder nicht gedrückt sein können.
ms.date: 10/26/2020
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, keyboard input
- keyboard [Windows Forms], input
ms.openlocfilehash: dbebc89b4ec9e5824f7a1b44a75fe313c4ab683b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942038"
---
# <a name="overview-of-using-the-keyboard-windows-forms-net"></a>Übersicht über die Verwendung der Tastatur (Windows Forms .NET)

In Windows Forms werden Benutzereingaben in Form von [Windows-Meldungen](/windows/win32/winmsg/about-messages-and-message-queues) an Anwendungen gesendet. Eine Reihe überschreibbarer Methoden verarbeitet diese Meldungen auf Anwendungs-, Formular- und Steuerelementebene. Wenn diese Methoden tastaturbezogene Meldungen empfangen, lösen sie Ereignisse aus, die verarbeitet werden können, um Informationen über die Tastatureingabe zu erhalten. Oftmals können Windows Forms-Anwendungen sämtliche Benutzereingaben verarbeiten, indem einfach diese Ereignisse verarbeitet werden. In anderen Fällen kann eine Anwendung eine der Methoden überschreiben, die Nachrichten verarbeiten, um eine bestimmte Nachricht abzufangen, bevor diese von der Anwendung, dem Formular oder dem Steuerelement empfangen wird.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="keyboard-events"></a>Tastaturereignisse

Alle Windows Forms-Steuerelemente erben verschiedene Ereignisse, die mit Maus- und Tastatureingaben zu tun haben. Ein Steuerelement kann beispielsweise das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis verarbeiten, um den Zeichencode einer Taste zu bestimmen, die gedrückt wurde. Weitere Information finden Sie unter [Verwenden von Tastaturereignissen](events.md).

## <a name="methods-that-process-user-input-messages"></a>Methoden zum Verarbeiten von Benutzereingabemeldungen

Formulare und Steuerelemente haben Zugriff auf die Schnittstelle <xref:System.Windows.Forms.IMessageFilter> und mehrere überschreibbare Methoden, die Windows-Meldungen an verschiedenen Stellen der Nachrichtenwarteschlange verarbeiten. Diese Methoden verfügen alle über einen <xref:System.Windows.Forms.Message>-Parameter, der die genauen Details von Windows-Meldungen kapselt. Sie können diese Methoden implementieren oder überschreiben, um die Nachricht zu untersuchen und anschließend zu verarbeiten oder an den nächsten Consumer in der Nachrichtenwarteschlange zu übergeben. In der folgenden Tabelle werden die Methoden vorgestellt, die die Windows-Meldungen in Windows Forms verarbeiten.

| Methode     | Hinweise |
|------------|-----------|
| <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage%2A> | Diese Methode fängt in die Warteschlange eingereihte (veröffentlichte) Windows-Nachrichten auf Anwendungsebene ab.|
| <xref:System.Windows.Forms.Control.PreProcessMessage%2A>       | Diese Methode fängt Windows-Meldungen auf Formular- und Steuerelementebene ab, bevor diese verarbeitet werden.|
| <xref:System.Windows.Forms.Control.WndProc%2A>                 | Diese Methode verarbeitet Windows-Meldungen auf Formular- und Steuerelementebene.|
| <xref:System.Windows.Forms.Control.DefWndProc%2A>              | Diese Methode führt die Standardverarbeitung von Windows-Meldungen auf Formular- und Steuerelementebene aus. Hierdurch wird die minimale Funktionalität eines Fensters gewährleistet.|
| <xref:System.Windows.Forms.Control.OnNotifyMessage%2A>         | Diese Methode fängt Nachrichten auf Formular- und Steuerelementebene ab, nachdem diese verarbeitet wurden. Das Stilbit <xref:System.Windows.Forms.ControlStyles.EnableNotifyMessage> muss festgelegt werden, damit diese Methode aufgerufen wird.|

Tastatur- und Mausmeldungen werden auch durch zusätzliche überschreibbare Methoden verarbeitet, die für diese Meldungstypen spezifisch sind. Weitere Informationen finden Sie im Abschnitt [Vorverarbeiten von Tasten](#preprocessing-keys). <!-- TODO mouse link -->.

## <a name="types-of-keys"></a>Schlüsseltypen

Windows Forms identifiziert Tastatureingaben als virtuelle Tastencodes, die durch die bitweise <xref:System.Windows.Forms.Keys>-Enumeration dargestellt werden. Mit der <xref:System.Windows.Forms.Keys>-Enumeration können Sie eine Reihe gedrückter Tasten in einem einzelnen Wert kombinieren. Diese Werte entsprechen den Werten, die in den Windows-Nachrichten **WM_KEYDOWN** und **WM_SYSKEYDOWN** enthalten sind. Das Drücken der meisten physischen Tasten lässt sich durch Verarbeitung der Ereignisse <xref:System.Windows.Forms.Control.KeyDown> oder <xref:System.Windows.Forms.Control.KeyUp> erkennen. Zeichentasten sind eine Teilmenge der <xref:System.Windows.Forms.Keys>-Enumeration. Sie entsprechen den Werten, die in den Windows-Meldungen **WM_CHAR** und **WM_SYSCHAR** enthalten sind. Wenn durch Drücken einer Tastenkombination ein Zeichen entsteht, können Sie das Zeichen durch Bearbeitung des Ereignisses <xref:System.Windows.Forms.Control.KeyPress> erkennen. <!-- TODO is this still valid with .NET Core/5 ?? Alternatively, you can use <xref:Microsoft.VisualBasic.Devices.Keyboard>, exposed by Visual Basic programming interface, to discover which keys were pressed and send keys. For more information, see [Accessing the Keyboard](../../visual-basic/developing-apps/programming/computer-resources/accessing-the-keyboard.md).-->

## <a name="order-of-keyboard-events"></a>Reihenfolge von Tastaturereignissen

Wie oben aufgeführt gibt es drei mit der Tastatur verknüpfte Ereignisse, die in einem Steuerelement auftreten können. Die folgende Sequenz zeigt die allgemeine Reihenfolge der Ereignisse:

01. Der Benutzer drückt die Taste „a“, die Taste wird vorverarbeitet und gesendet, und ein Ereignis vom Typ <xref:System.Windows.Forms.Control.KeyDown> tritt auf.
01. Der Benutzer hält die Taste „a“ gedrückt, die Taste wird vorverarbeitet und gesendet, und ein Ereignis vom Typ <xref:System.Windows.Forms.Control.KeyPress> tritt auf.
    Dieses Ereignis tritt mehrmals auf, wenn der Benutzer eine Taste gedrückt hält.
01. Der Benutzer lässt die Taste „a“ los, die Taste wird vorverarbeitet und gesendet, und ein Ereignis vom Typ <xref:System.Windows.Forms.Control.KeyUp> tritt auf.

## <a name="preprocessing-keys"></a>Vorverarbeiten von Tasten

Tastaturnachrichten werden wie andere Nachrichten in der Methode <xref:System.Windows.Forms.Control.WndProc%2A> eines Formulars oder Steuerelements verarbeitet. Vor der Verarbeitung der Tastaturnachrichten ruft die Methode <xref:System.Windows.Forms.Control.PreProcessMessage%2A> jedoch mindestens eine Methode auf, die überschrieben werden kann, um Sonderzeichentasten und physische Tasten zu verarbeiten. Sie können diese Methoden zum Erkennen und Filtern bestimmter Tasten überschreiben, bevor die Nachrichten vom Steuerelement verarbeitet werden. Die folgende Tabelle zeigt die Aktion an, die ausgeführt wird und die zugehörige Methode die auftritt, in der Reihenfolge, in der die Methode auftritt.

### <a name="preprocessing-for-a-keydown-event"></a>Vorverarbeiten eines KeyDown-Ereignisses

|Aktion|Verknüpfte Methode|Hinweise|
|------------|--------------------|-----------|
|Überprüfen Sie, ob eine Befehlstaste vorhanden ist, z.B. eine Zugriffstaste oder eine Menü-Tastenkombination.|<xref:System.Windows.Forms.Control.ProcessCmdKey%2A>|Diese Methode verarbeitet eine Befehlstaste, die Vorrang gegenüber regulären Tasten hat. Wenn diese Methode `true` zurückgibt, wird die Schlüsselmeldung nicht weitergeleitet, und es tritt kein Schlüsselereignis auf. Wenn `false` zurückgegeben wird, wird <xref:System.Windows.Forms.Control.IsInputKey%2A> aufgerufen`.`|
|Suchen Sie nach einer Sondertaste, für die eine Vorverarbeitung erforderlich ist, oder nach einer normalen Zeichentaste, die ein Ereignis vom Typ <xref:System.Windows.Forms.Control.KeyDown> auslösen und an ein Steuerelement weitergeleitet werden sollte.|<xref:System.Windows.Forms.Control.IsInputKey%2A>|Wenn die Methode `true` zurückgibt, bedeutet dies, dass das Steuerelement ein normales Zeichen ist und ein Ereignis vom Typ <xref:System.Windows.Forms.Control.KeyDown> ausgelöst wird. Bei `false` wird <xref:System.Windows.Forms.Control.ProcessDialogKey%2A> aufgerufen. **Hinweis**:  Sie können das <xref:System.Windows.Forms.Control.PreviewKeyDown>-Ereignis verarbeiten und <xref:System.Windows.Forms.PreviewKeyDownEventArgs.IsInputKey%2A> der Klasse <xref:System.Windows.Forms.PreviewKeyDownEventArgs> für die gewünschten Tasten auf `true` festlegen, um sicherzustellen, dass ein Steuerelement eine Taste oder eine Kombination aus Tasten erhält.|
|Führen Sie eine Überprüfung auf eine Navigationstaste aus (ESC-, TAB-, Return oder Pfeiltaste).|<xref:System.Windows.Forms.Control.ProcessDialogKey%2A>|Diese Methode verarbeitet eine physische Taste, die eine besondere Funktionalität innerhalb des Steuerelements nutzt und z.B. den Fokus zwischen dem Steuerelement und seinem übergeordneten Element umschaltet. Wenn die Taste nicht vom direkten Steuerelement verarbeitet wird, wird <xref:System.Windows.Forms.Control.ProcessDialogKey%2A> im übergeordneten Steuerelement aufgerufen. Dies kann so lange fortgesetzt werden, bis das Steuerelement erreicht ist, das in der Hierarchie an oberster Stelle steht. Wenn diese Methode `true` zurückgibt, ist die Vorverarbeitung abgeschlossen, und es wird kein Tastenereignis generiert. Wenn `false` zurückgegeben wird, tritt ein <xref:System.Windows.Forms.Control.KeyDown>-Ereignis auf.|

### <a name="preprocessing-for-a-keypress-event"></a>Vorverarbeiten eines KeyPress-Ereignisses

|Aktion|Verknüpfte Methode|Hinweise|
|------------|--------------------|-----------|
|Überprüfen Sie, ob die Taste ein normales Zeichen darstellt, das vom Steuerelement verarbeitet werden sollte|<xref:System.Windows.Forms.Control.IsInputChar%2A>|Wenn es sich bei dem Zeichen um ein normales Zeichen handelt, gibt diese Methode `true` zurück, das Ereignis <xref:System.Windows.Forms.Control.KeyPress> wird ausgelöst, und es kommt zu keiner weiteren Vorverarbeitung. Andernfalls wird <xref:System.Windows.Forms.Control.ProcessDialogChar%2A> aufgerufen.|
|Überprüfen Sie, ob es sich bei dem Zeichen um ein mnemonisches Zeichen handelt (z.B. &OK auf einer Schaltfläche)|<xref:System.Windows.Forms.Control.ProcessDialogChar%2A>|Diese Methode wird ähnlich wie <xref:System.Windows.Forms.Control.ProcessDialogKey%2A> aufsteigend entlang der Hierarchie des Steuerelements aufgerufen. Wenn es sich bei dem Steuerelement um ein Containersteuerelement handelt, sucht es nach mnemonischen Zeichen, indem es <xref:System.Windows.Forms.Control.ProcessMnemonic%2A>für sich und seine untergeordneten Steuerelemente aufruft. Wenn `true` von <xref:System.Windows.Forms.Control.ProcessDialogChar%2A> zurückgegeben wird, tritt kein <xref:System.Windows.Forms.Control.KeyPress>-Ereignis auf.|

## <a name="processing-keyboard-messages"></a>Verarbeiten von Tastaturmeldungen

Nachdem Tastaturmeldungen die Methode <xref:System.Windows.Forms.Control.WndProc%2A> eines Formulars oder Steuerelements erreicht haben, werden sie durch eine Reihe von Methoden verarbeitet, die überschrieben werden können. Jede dieser Methoden gibt einen <xref:System.Boolean>-Wert zurück, der angibt, ob die Tastaturmeldung verarbeitet und vom Steuerelement verwendet wurde. Wenn eine der Methoden `true` zurückgibt, dann gilt die Nachricht als bearbeitet. Sie wird nicht zur weiteren Verarbeitung an das Basiselement oder das übergeordnete Element des Steuerelements übergeben. Andernfalls bleibt die Nachricht in der Nachrichtenwarteschlange und kann in einer anderen Methode im Basiselement oder übergeordneten Element des Steuerelements verarbeitet werden. Die folgende Tabelle enthält die Methoden, die Tastaturmeldungen verarbeiten.

|Methode|Hinweise|
|------------|-----------|
|<xref:System.Windows.Forms.Control.ProcessKeyMessage%2A>|Diese Methode verarbeitet alle Tastaturmeldungen, die von der <xref:System.Windows.Forms.Control.WndProc%2A>-Methode des Steuerelements empfangen werden.|
|<xref:System.Windows.Forms.Control.ProcessKeyPreview%2A>|Diese Methode sendet die Tastaturmeldung an das übergeordnete Element des Steuerelements. Wenn <xref:System.Windows.Forms.Control.ProcessKeyPreview%2A> `true` zurückgibt, wird kein Tastenereignis generiert, andernfalls wird <xref:System.Windows.Forms.Control.ProcessKeyEventArgs%2A> aufgerufen.|
|<xref:System.Windows.Forms.Control.ProcessKeyEventArgs%2A>|Diese Methode löst je nach Anforderung die Ereignisse <xref:System.Windows.Forms.Control.KeyDown>, <xref:System.Windows.Forms.Control.KeyPress> und <xref:System.Windows.Forms.Control.KeyUp> auf.|

## <a name="overriding-keyboard-methods"></a>Überschreiben von Tastaturmethoden

Es sind viele Methoden zum Überschreiben verfügbar, wenn eine Tastaturmeldung vorverarbeitet und verarbeitet wird. Einige Methoden sind jedoch besser geeignet als andere. Die folgende Tabelle enthält Aufgaben, die Sie möglicherweise ausführen möchten, sowie die beste Methode für das Überschreiben der Tastaturmethoden. Weitere Informationen zum Überschreiben von Methoden finden Sie unter [Vererbung (C#-Programmierleitfaden)](/dotnet/csharp/programming-guide/classes-and-structs/inheritance.md#abstract-and-virtual-methods) oder [Vererbung (Visual Basic)](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md#overriding-properties-and-methods-in-derived-classes).

|Aufgabe|Methode|
|----------|------------|
|Bei dieser Aufgabe wird eine Navigationstaste abgefangen und ein <xref:System.Windows.Forms.Control.KeyDown>-Ereignis ausgelöst. Beispiel: Sie möchten, dass die TAB- und die Return-Taste in einem Textfeld bearbeitet werden.|Überschreiben Sie <xref:System.Windows.Forms.Control.IsInputKey%2A>. **Hinweis**:  Alternativ können Sie das <xref:System.Windows.Forms.Control.PreviewKeyDown>-Ereignis verarbeiten und <xref:System.Windows.Forms.PreviewKeyDownEventArgs.IsInputKey%2A> der <xref:System.Windows.Forms.PreviewKeyDownEventArgs>-Klasse für die gewünschten Tasten auf `true` festlegen.|
|Nehmen Sie bei einem Steuerelement eine besondere Eingabe oder Navigationsbehandlung vor. Beispiel: Sie möchten bei dem ausgewählten Element die Verwendung der Pfeiltasten in Ihrem Listensteuerelement ändern.|Überschreiben Sie <xref:System.Windows.Forms.Control.ProcessDialogKey%2A>.|
|Bei dieser Aufgabe wird eine Navigationstaste abgefangen und ein <xref:System.Windows.Forms.Control.KeyPress>-Ereignis ausgelöst. Beispiel: Sie möchten, dass durch mehrfaches Drücken der Pfeiltaste in einem Drehfeld-Steuerelement der Fortschritt durch die Elemente beschleunigt wird.|Überschreiben Sie <xref:System.Windows.Forms.Control.IsInputChar%2A>.|
|Bei dieser Aufgabe wird die Verarbeitung einer Sondereingabe oder Navigation während eines <xref:System.Windows.Forms.Control.KeyPress>-Ereignisses durchgeführt. Beispiel: Wenn in einem Listensteuerelement die Taste „r“ gedrückt gehalten wird, werden Elemente übersprungen, die mit diesem Buchstaben beginnen.|Überschreiben Sie <xref:System.Windows.Forms.Control.ProcessDialogChar%2A>.|
|Führen Sie eine benutzerdefinierte Bearbeitung mnemonischer Zeichen durch. Beispiel: Sie möchten mnemonische Zeichen in von Benutzern gezeichneten Schaltflächen bearbeiten, die in einer Symbolleiste enthalten sind.|Überschreiben Sie <xref:System.Windows.Forms.Control.ProcessMnemonic%2A>.|

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.WndProc%2A>
- <xref:System.Windows.Forms.Control.PreProcessMessage%2A>
- [Verwenden von Tastaturereignissen (Windows Forms .NET)](events.md)
- [Ändern von Tastaturtastenereignissen (Windows Forms .NET)](how-to-change-key-press.md)
- [Überprüfen der Tastendruckaktion für Zusatztasten (Windows Forms .NET)](how-to-check-modifier-key.md)
- [Simulieren von Tastaturereignissen (Windows Forms .NET)](how-to-simulate-events.md)
- [Verarbeiten von Tastatureingabemeldungen im Formular (Windows Forms .NET)](how-to-handle-forms.md)
- [Hinzufügen eines Steuerelements (Windows Forms .NET)](../controls/how-to-add-to-a-form.md)
