---
title: Übersicht über Mauseingaben
description: Hier erfahren Sie, wie Mauseingaben in Windows Forms für .NET funktionieren. Mausereignisse werden von Formularen und Steuerelementen ausgelöst und geben die Position und den Schaltflächenzustand der Maus wieder.
ms.date: 10/26/2020
ms.topic: overview
helpviewer_keywords:
- Windows Forms, mouse input
- mouse [Windows Forms], input
ms.openlocfilehash: 3e85305796d724d9acdbcd2e7cb86e748c30b783
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942066"
---
# <a name="overview-of-using-the-mouse-windows-forms-net"></a>Übersicht über die Mausverwendung (Windows Forms .NET)

Das Empfangen und Verarbeiten von Mauseingaben ist ein wichtiger Bestandteil jeder Windows-Anwendung. Sie können Mausereignisse verarbeiten, um eine Aktion in Ihrer Anwendung auszuführen, oder mithilfe von Informationen zur Mausposition Treffertests oder andere Aktionen ausführen. Außerdem haben Sie die Möglichkeit zu ändern, wie die Steuerelemente in Ihrer Anwendung Mauseingaben verarbeiten. In diesem Artikel werden diese Mausereignisse ausführlich beschrieben. Zudem wird erläutert, wie Sie die Systemeinstellungen für die Maus abrufen und ändern.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

In Windows Forms werden Benutzereingaben in Form von [Windows-Meldungen](/windows/win32/winmsg/about-messages-and-message-queues) an Anwendungen gesendet. Eine Reihe überschreibbarer Methoden verarbeitet diese Meldungen auf Anwendungs-, Formular- und Steuerelementebene. Wenn diese Methoden mausbezogene Meldungen empfangen, lösen sie Ereignisse aus, die verarbeitet werden können, um Informationen über die Mauseingabe zu erhalten. Oftmals können Windows Forms-Anwendungen sämtliche Benutzereingaben verarbeiten, indem einfach diese Ereignisse verarbeitet werden. In anderen Fällen kann eine Anwendung eine der Methoden überschreiben, die Nachrichten verarbeiten, um eine bestimmte Nachricht abzufangen, bevor diese von der Anwendung, dem Formular oder dem Steuerelement empfangen wird.

## <a name="mouse-events"></a>Mausereignisse

Alle Windows Forms-Steuerelemente erben verschiedene Ereignisse, die mit Maus- und Tastatureingaben zu tun haben. Ein Steuerelement kann z. B. das Ereignis <xref:System.Windows.Forms.Control.MouseClick> verarbeiten, um die Position eines Mausklicks zu bestimmen. Weitere Informationen zu Mausereignissen finden Sie unter [Verwenden von Mausereignissen](events.md).

## <a name="mouse-location-and-hit-testing"></a>Mausposition und Treffertests

Wenn der Benutzer die Maus bewegt, verschiebt das Betriebssystem den Mauszeiger. Der Mauszeiger enthält ein einzelnes Pixel, den Hotspot, das vom Betriebssystem nachverfolgt und als Position des Zeigers erkannt wird. Wenn der Benutzer die Maus bewegt oder eine Maustaste drückt, löst das Steuerelement (<xref:System.Windows.Forms.Control>), das den Hotspot (<xref:System.Windows.Forms.Cursor.HotSpot%2A>-Eigenschaft) enthält, das entsprechende Mausereignis aus.

Sie können die aktuelle Mausposition mit der Eigenschaft <xref:System.Windows.Forms.MouseEventArgs.Location%2A> der Klasse <xref:System.Windows.Forms.MouseEventArgs> abrufen, wenn ein Mausereignis verarbeitet wird, oder indem Sie die Eigenschaft <xref:System.Windows.Forms.Cursor.Position%2A> der Klasse <xref:System.Windows.Forms.Cursor> verwenden. Anschließend können Sie mithilfe der Positionsinformationen der Maus Treffertests durchführen und eine Aktion auf Basis der Mausposition ausführen. Die Treffertestfunktion ist in Windows Forms in mehrere Steuerelemente integriert, z. B. in die Steuerelemente <xref:System.Windows.Forms.ListView>, <xref:System.Windows.Forms.TreeView>, <xref:System.Windows.Forms.MonthCalendar> und <xref:System.Windows.Forms.DataGridView>.

In Kombination mit dem richtigen Mausereignis, z. B. <xref:System.Windows.Forms.Control.MouseHover>, sind Treffertest sehr nützlich, um zu bestimmen, wann die Anwendung eine bestimmte Aktion durchführen soll.

## <a name="changing-mouse-input-settings"></a>Ändern der Einstellungen für die Mauseingabe

Sie können die Art, wie ein Steuerelement Mauseingaben verarbeitet, erkennen und ändern, indem Sie eine Ableitung vom Steuerelement durchführen und die Methoden <xref:System.Windows.Forms.Control.GetStyle%2A> und <xref:System.Windows.Forms.Control.SetStyle%2A> verwenden. Die Methode <xref:System.Windows.Forms.Control.SetStyle%2A> akzeptiert eine bitweise Kombination von <xref:System.Windows.Forms.ControlStyles>-Werten, um zu bestimmen, ob das Steuerelement Standardklick- oder Doppelklickverhalten aufweist oder aber die Mauseingabe selbst verarbeitet. Außerdem enthält die Klasse <xref:System.Windows.Forms.SystemInformation> Eigenschaften, die die Funktionen der Maus beschreiben und angeben, wie die Maus mit dem Betriebssystem interagiert. In der folgenden Tabelle werden diese Eigenschaften zusammengefasst.

| Eigenschaft                                                               | BESCHREIBUNG                                                                                                                                                            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <xref:System.Windows.Forms.SystemInformation.DoubleClickSize%2A>       | Ruft die Dimensionen des Bereichs, auf den Benutzer zweimal klicken müssen, damit zwei Mausklicks als Doppelklick erkannt werden, in Pixel ab                     |
| <xref:System.Windows.Forms.SystemInformation.DoubleClickTime%2A>       | Ruft die maximale Anzahl von Millisekunden ab, die zwischen dem ersten und dem darauffolgenden Mausklick verstreichen dürfen, damit die Mausaktion als Doppelklick gilt |
| <xref:System.Windows.Forms.SystemInformation.MouseButtons%2A>          | Ruft die Anzahl der Maustasten ab.                                                                                                                               |
| <xref:System.Windows.Forms.SystemInformation.MouseButtonsSwapped%2A>   | Ruft einen Wert ab, der angibt, ob die Funktionen der linken und der rechten Maustaste vertauscht wurden.                                                                   |
| <xref:System.Windows.Forms.SystemInformation.MouseHoverSize%2A>        | Ruft die Abmessungen des Rechtecks in Pixel ab, auf das der Mauszeiger für eine bestimmte Zeit zeigen muss, bevor eine Mausbewegungsmeldung generiert wird.        |
| <xref:System.Windows.Forms.SystemInformation.MouseHoverTime%2A>        | Ruft die Zeit in Millisekunden ab, für die sich der Mauszeiger im Bewegungsrechteck befinden muss, bevor eine Mausbewegungsmeldung generiert wird.                                   |
| <xref:System.Windows.Forms.SystemInformation.MousePresent%2A>          | Ruft einen Wert ab, der angibt, ob eine Maus installiert ist                                                                                                                  |
| <xref:System.Windows.Forms.SystemInformation.MouseSpeed%2A>            | Ruft einen Wert ab, der die aktuelle Mausgeschwindigkeit auf einer Skala von 1 bis 20 angibt                                                                                                         |
| <xref:System.Windows.Forms.SystemInformation.MouseWheelPresent%2A>     | Ruft einen Wert ab, der angibt, ob eine Maus mit einem Mausrad installiert ist.                                                                                               |
| <xref:System.Windows.Forms.SystemInformation.MouseWheelScrollDelta%2A> | Ruft die Größe des Deltawerts des Inkrements einer einzelnen Drehung des Mausrads ab                                                                                  |
| <xref:System.Windows.Forms.SystemInformation.MouseWheelScrollLines%2A> | Ruft die Anzahl der Zeilen ab, die mit einem Bildlauf erfasst werden, wenn das Mausrad gedreht wird.                                                                                                    |

## <a name="methods-that-process-user-input-messages"></a>Methoden zum Verarbeiten von Benutzereingabemeldungen

Formulare und Steuerelemente haben Zugriff auf die Schnittstelle <xref:System.Windows.Forms.IMessageFilter> und mehrere überschreibbare Methoden, die Windows-Meldungen an verschiedenen Stellen der Nachrichtenwarteschlange verarbeiten. Diese Methoden verfügen alle über einen <xref:System.Windows.Forms.Message>-Parameter, der die genauen Details von Windows-Meldungen kapselt. Sie können diese Methoden implementieren oder überschreiben, um die Nachricht zu untersuchen und anschließend zu verarbeiten oder an den nächsten Consumer in der Nachrichtenwarteschlange zu übergeben. In der folgenden Tabelle werden die Methoden vorgestellt, die die Windows-Meldungen in Windows Forms verarbeiten.

| Methode     | Hinweise |
|------------|-----------|
| <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage%2A> | Diese Methode fängt in die Warteschlange eingereihte (veröffentlichte) Windows-Nachrichten auf Anwendungsebene ab.|
| <xref:System.Windows.Forms.Control.PreProcessMessage%2A>       | Diese Methode fängt Windows-Meldungen auf Formular- und Steuerelementebene ab, bevor diese verarbeitet werden.|
| <xref:System.Windows.Forms.Control.WndProc%2A>                 | Diese Methode verarbeitet Windows-Meldungen auf Formular- und Steuerelementebene.|
| <xref:System.Windows.Forms.Control.DefWndProc%2A>              | Diese Methode führt die Standardverarbeitung von Windows-Meldungen auf Formular- und Steuerelementebene aus. Hierdurch wird die minimale Funktionalität eines Fensters gewährleistet.|
| <xref:System.Windows.Forms.Control.OnNotifyMessage%2A>         | Diese Methode fängt Nachrichten auf Formular- und Steuerelementebene ab, nachdem diese verarbeitet wurden. Das Stilbit <xref:System.Windows.Forms.ControlStyles.EnableNotifyMessage> muss festgelegt werden, damit diese Methode aufgerufen wird.|

## <a name="see-also"></a>Siehe auch

- [Verwenden von Mausereignissen (Windows Forms .NET)](events.md)
- [Übersicht über das Drag-&-Drop-Mausverhalten (Windows Forms .NET)](drag-and-drop.md)
- [Verwalten von Mauszeigern (Windows Forms .NET)](how-to-manage-cursor-pointer.md)
