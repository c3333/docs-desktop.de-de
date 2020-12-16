---
title: Übersicht über Ereignisse
description: Hier erhalten Sie eine kurze Übersicht über Ereignisse bei .NET Windows Forms.
ms.date: 10/26/2020
ms.topic: overview
helpviewer_keywords:
- Windows Forms, event handling
- events [Windows Forms], about events
- delegates [Windows Forms], multicast
- delegates [Windows Forms], events and
- multicast event delegates
- Windows Forms controls, events
ms.openlocfilehash: aed33b7b856da210855a5b06ccf53610a6551b47
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942115"
---
# <a name="events-overview-windows-forms-net"></a>Übersicht über Ereignisse (Windows Forms .NET)

Bei einem Ereignis handelt es sich um eine Aktion, auf die Sie reagieren oder die Sie mittels Code „behandeln“ können. Ereignisse können durch eine Benutzeraktion generiert werden, z. B. durch Klicken mit der Maus oder Drücken einer Taste; durch Programmcode oder durch das System.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

Ereignisgesteuerte Anwendungen führen Code als Reaktion auf ein Ereignis aus. Jedes Formular und jedes Steuerelement macht eine vordefinierte Gruppe von Ereignissen verfügbar, die Sie programmieren können. Wenn eines dieser Ereignisse auftritt und Code im zugeordneten Ereignishandler vorhanden ist, wird der Code aufgerufen.

Die von einem Objektarray ausgelösten Ereignistypen unterscheiden sich, viele ähneln aber den meisten Steuerelementen. Die meisten Objekte behandeln beispielsweise ein <xref:System.Windows.Forms.Control.Click>-Ereignis. Wenn ein Benutzer auf ein Formular klickt, wird der Code im <xref:System.Windows.Forms.Control.Click>-Ereignishandler des Formulars ausgeführt.

> [!NOTE]
> Viele Ereignisse treten im Zusammenhang mit anderen Ereignissen auf. Wenn beispielsweise ein <xref:System.Windows.Forms.Control.DoubleClick>-Ereignis auftritt, treten auch die <xref:System.Windows.Forms.Control.MouseDown>, <xref:System.Windows.Forms.Control.MouseUp>- und <xref:System.Windows.Forms.Control.Click>-Ereignisse auf.

Informationen zum Auslösen und Nutzen eines Ereignisses finden Sie unter [Behandeln und Auslösen von Ereignissen](/dotnet/standard/events/index).

## <a name="delegates-and-their-role"></a>Delegaten und ihre Rolle

Delegaten sind Klassen, die häufig in den in .NET zu erstellenden Mechanismen zur Behandlung von Ereignissen verwendet werden. Delegaten entsprechen in etwa Funktionszeigern, die häufig in Visual C++ und anderen objektorientierten Sprachen verwendet werden. Im Gegensatz zu Funktionszeigern sind Delegaten objektorientiert, typsicher und sicher. Darüber hinaus bestehen sie im Vergleich zu Funktionszeigern, die nur einen Verweis auf eine bestimmte Funktion enthalten, aus einem Verweis auf ein Objekt und Verweisen auf mindestens eine Methode in dem Objekt.

Im Ereignismodell werden *Delegaten* zum Binden von Ereignissen an Methoden zur Behandlung dieser Ereignisse verwendet. Mit dem Delegat können andere Klassen für eine Ereignisbenachrichtigung registriert werden, indem eine Handlermethode angegeben wird. Wenn das Ereignis auftritt, ruft der Delegat die gebundene Methode auf. Weitere Informationen zum Definieren von Delegaten finden Sie unter [Behandeln und Auslösen von Ereignissen](/dotnet/standard/events/index).

Delegaten können an eine einzelne oder mehrere Methoden gebunden werden, das bezeichnet man als Multicasting. Beim Erstellen eines Delegaten für ein Ereignis wird in der Regel ein Multicastereignis erstellt. Eine seltene Ausnahme dazu ist möglicherweise ein Ereignis, das zu einer bestimmten Prozedur führt (z. B. das Anzeigen eines Dialogfelds), die logischerweise nicht mehrmals pro Ereignis auftritt. Informationen zum Erstellen von Multicastdelegaten finden Sie unter [Kombinieren von Delegaten (Multicastdelegaten)](/dotnet/csharp/programming-guide/delegates/how-to-combine-delegates-multicast-delegates).

Mit einem Multicastdelegat wird eine Aufrufliste der Methoden verwaltet, an die er gebunden ist. Der Multicast-Delegat unterstützt eine <xref:System.Delegate.Combine%2A>-Methode zum Hinzufügen einer Methode zur Aufrufliste und eine <xref:System.Delegate.Remove%2A>-Methode, um sie zu entfernen.

Wenn ein Ereignis von der Anwendung aufgezeichnet wird, löst das Steuerelement das Ereignis aus, indem es den Delegaten für das Ereignis aufruft. Der Delegat wiederum ruft die gebundene Methode auf. Im häufigsten Fall (einem Multicastdelegat) wird wiederum vom Delegat jede gebundene Methode in der Aufrufliste aufgerufen, sodass eine 1:n-Benachrichtigung bereitgestellt wird. Das heißt, Zielobjektlisten für die Ereignisbenachrichtigung müssen nicht vom Steuerelement verwaltet werden, da alle Registrierungen und Benachrichtigungen vom Delegat behandelt werden.

Mit Delegaten können auch mehrere Ereignisse an dieselbe Methode gebunden werden, sodass eine viele-zu-eins-Benachrichtigung bereitgestellt werden kann.  Ein Klick-Ereignis einer Schaltfläche und ein Menübefehl-Klick-Ereignis können beide denselben Delegaten aufrufen, der dann eine einzelne Methode aufruft, um diese separaten Ereignisse gleich zu behandeln.

Der mit Delegaten verwendete Bindungsmechanismus ist dynamisch: ein Delegat kann zur Laufzeit an jede Methode gebunden werden, dessen Signatur mit der des Ereignishandlers übereinstimmt. Mit dieser Funktion können Sie die gebundene Methode abhängig von einer Bedingung einrichten oder ändern und einen Ereignishandler dynamisch an ein Steuerelement anfügen.

## <a name="see-also"></a>Siehe auch

- [Behandeln und Auslösen von Ereignissen](/dotnet/standard/events/index)

<!-- TODO
- [Creating Event Handlers in Windows Forms](creating-event-handlers-in-windows-forms.md)
- [Event Handlers Overview](event-handlers-overview-windows-forms.md)-->
