---
title: Überprüfung von Benutzereingaben
description: Hier erfahren Sie, welche Möglichkeiten es gibt, um mit Windows Forms Benutzereingabe in Ihren Anwendungen zu überprüfen.
ms.date: 10/26/2020
ms.topic: overview
helpviewer_keywords:
- Windows Forms, validating user input
- validation [Windows Forms], Windows Forms user input
- user input [Windows Forms], validating in Windows Forms
- validating user input [Windows Forms], Windows Forms
ms.openlocfilehash: 16db8a1048c5f342f942f88a91a764d6b2a57f35
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942031"
---
# <a name="overview-of-how-to-validate-user-input-windows-forms-net"></a>Übersicht über die Überprüfung von Benutzereingaben (Windows Forms .NET)

Wenn Benutzer in Ihrer Anwendung Daten eingeben können, sollte überprüft werden, ob die Daten gültig sind, bevor sie in der Anwendung verwendet werden. So können Sie beispielsweise festlegen, dass die Länge bestimmter Textfelder nicht Null sein darf, ein Feld als Telefonnummer formatiert sein muss oder eine Zeichenfolge keine ungültigen Zeichen enthalten darf. Windows Forms bietet mehrere Möglichkeiten zum Überprüfen von Eingaben in einer Anwendung.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="maskedtextbox-control"></a>MaskedTextBox-Steuerelement

Wenn Sie festlegen müssen, dass Benutzer Daten in einem klar definierten Format eingeben, beispielsweise als Telefonnummer oder als Artikelnummer, können Sie dies mit dem <xref:System.Windows.Forms.MaskedTextBox>-Steuerelement mit minimalem Programmieraufwand schnell erreichen. Eine *Maske* ist eine Zeichenfolge, die aus Zeichen einer Maskierungssprache besteht, mit der festgelegt wird, welche Zeichen an einer bestimmten Position in einem Textfeld eingegeben werden können. Mit dem Steuerelement werden dem Benutzer verschiedene Eingabeaufforderungen angezeigt. Wenn der Benutzer einen falschen Eintrag eingibt, also beispielsweise einen Buchstaben, obwohl er eine Ziffer eingeben müsste, wird die Eingabe vom Steuerelement automatisch abgelehnt.

Die von <xref:System.Windows.Forms.MaskedTextBox> verwendete Maskierungssprache ist flexibel. Damit können Sie erforderliche Zeichen, optionale Zeichen, Literalzeichen wie Bindestriche und Klammern, Währungszeichen und Datumstrennzeichen angeben. Das Steuerelement kann auch gut verwendet werden, wenn es an eine Datenquelle gebunden ist. Das <xref:System.Windows.Forms.Binding.Format>-Ereignis in einer Datenbindung kann verwendet werden, um eingehende Daten entsprechend der Maske neu zu formatieren, während das <xref:System.Windows.Forms.Binding.Parse>-Ereignis verwendet werden kann, um ausgehende Daten entsprechend den Spezifikationen des Datenfelds neu zu formatieren.

<!-- TODO
For more information, see [MaskedTextBox Control](./controls/maskedtextbox-control-windows-forms.md).-->

## <a name="event-driven-validation"></a>Ereignisgesteuerte Überprüfung

Wenn Sie eine Überprüfung vollkommen programmgesteuert durchführen möchten oder eine komplexe Überprüfung durchführen müssen, sollten Sie die in den meisten Windows Forms-Steuerelementen integrierten Überprüfungsereignisse verwenden. Jedes Steuerelement, das Benutzereingaben ohne Formvorgaben unterstützt, weist ein <xref:System.Windows.Forms.Control.Validating>-Ereignis auf, das auftritt, wenn das Steuerelement eine Datenüberprüfung benötigt. Die Methode zur Behandlung von <xref:System.Windows.Forms.Control.Validating>-Ereignissen bietet verschiedene Möglichkeiten, Benutzereingaben zu überprüfen. Bei einem Textfeld, das eine Postleitzahl enthalten muss, gibt es folgende Möglichkeiten für die Überprüfung:

- Wenn die Postleitzahl einer bestimmten Gruppe von Postleitzahlen angehören muss, kann für die Eingabe ein Zeichenfolgenvergleich durchgeführt werden, um die vom Benutzer eingegebenen Daten zu überprüfen. Wenn sich die Postleitzahl in der Gruppe `{10001, 10002, 10003}` befinden muss, können die Daten mit einem Zeichenfolgenvergleich überprüft werden.

- Wenn die Postleitzahl ein bestimmtes Format aufweisen muss, können die vom Benutzer eingegebenen Daten mit regulären Ausdrücken überprüft werden. Wenn Sie beispielsweise überprüfen möchten, ob das Format `#####` bzw. `#####-####` verwendet wurde, können Sie den regulären Ausdruck `^(\d{5})(-\d{4})?$` verwenden. Wenn Sie überprüfen möchten, ob das Format `A#A #A#` verwendet wurde, können Sie den regulären Ausdruck `[A-Z]\d[A-Z] \d[A-Z]\d` verwenden. Weitere Informationen zu regulären Ausdrücken finden Sie unter [Reguläre Ausdrücke von .NET](/dotnet/standard/base-types/regular-expressions) und [Beispiel für regulären Ausdruck](/dotnet/standard/base-types/regular-expression-example-scanning-for-hrefs).

- Wenn es sich bei der Postleitzahl um eine gültige Postleitzahl in den USA handeln muss, können Sie zum Überprüfen der vom Benutzer eingegebenen Daten einen Webdienst für Postleitzahlen aufrufen.

Das <xref:System.Windows.Forms.Control.Validating>-Ereignis wird als Objekt vom Typ <xref:System.ComponentModel.CancelEventArgs> bereitgestellt. Wenn festgestellt wird, dass die Daten des Steuerelements ungültig sind, wird das <xref:System.Windows.Forms.Control.Validating>-Ereignis abgebrochen, vorausgesetzt, Sie haben die <xref:System.ComponentModel.CancelEventArgs.Cancel%2A>-Eigenschaft dieses Objekts auf `true` festgelegt. Wenn Sie die <xref:System.ComponentModel.CancelEventArgs.Cancel%2A>-Eigenschaft nicht festlegen, wird in Windows Forms davon ausgegangen, dass die Überprüfung für dieses Steuerelement erfolgreich war, und das <xref:System.Windows.Forms.Control.Validated>-Ereignis ausgelöst.

Ein Beispiel für Code, mit dem eine E-Mail-Adresse in einem <xref:System.Windows.Controls.TextBox> überprüft wird finden Sie in der Referenz zum <xref:System.Windows.Forms.Control.Validating>-Ereignis.

### <a name="event-driven-validation-data-bound-controls"></a>Ereignisgesteuerte Überprüfung bei datengebunden Steuerelementen

Eine Überprüfung ist nützlich, wenn Steuerelemente an eine Datenquelle wie etwa an eine Datenbanktabelle gebunden sind. Durch eine Überprüfung kann sichergestellt werden, dass die Daten eines Steuerelements das von der Datenquelle geforderte Format aufweisen und keine Sonderzeichen wie Anführungszeichen und umgekehrte Schrägstriche enthalten, die möglicherweise unsicher sind.

Bei Verwenden einer Datenbindung werden die Daten in einem Steuerelement bei der Ausführung des <xref:System.Windows.Forms.Control.Validating>-Ereignisses mit der Datenquelle synchronisiert. Wenn das <xref:System.Windows.Forms.Control.Validating>-Ereignis abgebrochen wird, werden die Daten nicht mit der Datenquelle synchronisiert.

> [!IMPORTANT]
> Wenn nach dem <xref:System.Windows.Forms.Control.Validating>-Ereignis eine benutzerdefinierte Überprüfung durchgeführt wird, hat das keine Auswirkungen auf die Datenbindung. Wenn also beispielsweise die Datenbindung durch Code in einem <xref:System.Windows.Forms.Control.Validated>-Ereignis abgebrochen wird, wird die Datenbindung dennoch hergestellt. Damit in diesem Fall die Überprüfung im <xref:System.Windows.Forms.Control.Validated>-Ereignis durchgeführt wird, ändern Sie die [`Binding.DataSourceUpdateMode`](xref:System.Windows.Forms.Binding.DataSourceUpdateMode)-Eigenschaft des Steuerelements von <xref:System.Windows.Forms.DataSourceUpdateMode.OnValidation?displayProperty=nameWithType> in <xref:System.Windows.Forms.DataSourceUpdateMode.Never?displayProperty=nameWithType> und fügen dem Überprüfungscode `your-control.DataBindings["field-name"].WriteValue()` hinzu.

## <a name="implicit-and-explicit-validation"></a>Implizite und explizite Überprüfung

Wann werden die Daten eines Steuerelements überprüft? Das bestimmen Sie als Entwickler. Je nach den Anforderungen Ihrer Anwendung können Sie eine implizite oder eine explizite Überprüfung verwenden.

### <a name="implicit-validation"></a>Implizite Überprüfung

Bei der impliziten Überprüfung werden Daten überprüft, während sie vom Benutzer eingegeben werden. Die Daten werden überprüft, indem die Tasten beim Drücken gelesen werden. Häufiger werden sie jedoch überprüft, wenn der Benutzer den Eingabefokus vom Steuerelement weg lenkt. Diese Vorgehensweise ist nützlich, wenn der Benutzer direkt bei der Eingabe Feedback erhalten soll.

Wenn für ein Steuerelement die implizite Überprüfung verwendet werden soll, legen Sie die <xref:System.Windows.Forms.ContainerControl.AutoValidate%2A>-Eigenschaft des Steuerelements auf <xref:System.Windows.Forms.AutoValidate.EnablePreventFocusChange> oder <xref:System.Windows.Forms.AutoValidate.EnableAllowFocusChange> fest. Das Verhalten eines Steuerelements beim Abbruch des <xref:System.Windows.Forms.Control.Validating>-Ereignisses wird durch den Wert bestimmt, der <xref:System.Windows.Forms.ContainerControl.AutoValidate%2A> zugewiesen wird. Wenn <xref:System.Windows.Forms.AutoValidate.EnablePreventFocusChange> zugewiesen wird, tritt das <xref:System.Windows.Forms.Control.Validated>-Ereignis beim Abbruch des Ereignisses nicht auf. Der Eingabefokus bleibt auf dem aktuellen Steuerelement, bis der Benutzer die Daten in einem gültigen Format eingibt. Wenn <xref:System.Windows.Forms.AutoValidate.EnableAllowFocusChange> zugewiesen wird, tritt das <xref:System.Windows.Forms.Control.Validated>-Ereignis beim Abbruch des Ereignisses nicht auf. Der Fokus wechselt dennoch zum nächsten Steuerelement.

Wenn der <xref:System.Windows.Forms.ContainerControl.AutoValidate%2A>-Eigenschaft <xref:System.Windows.Forms.AutoValidate.Disable> zugewiesen wird, wird die implizite Überprüfung insgesamt verhindert. Zur Überprüfung von Steuerelementen muss dann die explizite Überprüfung verwendet werden.

### <a name="explicit-validation"></a>Explizite Überprüfung

Bei der expliziten Überprüfung werden alle Daten auf einmal überprüft. Die Daten können als Reaktion auf eine Benutzeraktion wie etwa auf das Klicken auf eine **Speichern**-Schaltfläche oder auf einen **Weiter**-Link überprüft werden. Es gibt folgende Möglichkeiten, bei einer Benutzeraktion eine explizite Überprüfung auszulösen:

- Aufruf von <xref:System.Windows.Forms.ContainerControl.Validate%2A>, um das letzte Steuerelement zu überprüfen, das den Fokus verloren hat.
- Aufruf von <xref:System.Windows.Forms.ContainerControl.ValidateChildren%2A>, um alle untergeordneten Steuerelemente in einem Formular oder Containersteuerelement zu überprüfen.
- Aufruf einer benutzerdefinierten Methode, um die Daten in den Steuerelementen manuell zu überprüfen.

### <a name="default-implicit-validation-behavior-for-controls"></a>Implizites Standardüberprüfungsverhalten für Steuerelemente

Für die jeweilige <xref:System.Windows.Forms.ContainerControl.AutoValidate%2A>-Eigenschaft der verschiedenen Windows Forms-Steuerelemente gelten unterschiedliche Standardwerte. In der folgenden Tabelle sind die gebräuchlichsten Steuerelemente und deren Standardwerte aufgeführt.

| Control                                        | Standardüberprüfungsverhalten                                     |
|------------------------------------------------|-----------------------------------------------------------------|
| <xref:System.Windows.Forms.ContainerControl>   | <xref:System.Windows.Forms.AutoValidate.Inherit>                |
| <xref:System.Windows.Forms.Form>               | <xref:System.Windows.Forms.AutoValidate.EnableAllowFocusChange> |
| <xref:System.Windows.Forms.PropertyGrid>       | Eigenschaft in Visual Studio nicht verfügbar                           |
| <xref:System.Windows.Forms.ToolStripContainer> | Eigenschaft in Visual Studio nicht verfügbar                           |
| <xref:System.Windows.Forms.SplitContainer>     | <xref:System.Windows.Forms.AutoValidate.Inherit>                |
| <xref:System.Windows.Forms.UserControl>        | <xref:System.Windows.Forms.AutoValidate.EnableAllowFocusChange> |

## <a name="closing-the-form-and-overriding-validation"></a>Schließen des Formulars und Außerkraftsetzen der Überprüfung

Wenn ein Steuerelement den Fokus behält, weil die enthaltenen Daten ungültig sind, ist es nicht möglich, das übergeordnete Formular auf eine der üblichen Arten zu schließen:

- Durch Klicken auf die Schaltfläche **Schließen**.
- Durch Auswählen des Menüs **System** > **Schließen**.
- Durch programmgesteuertes Aufrufen der <xref:System.Windows.Forms.Form.Close%2A>-Methode.

In manchen Fällen soll es jedoch möglich sein, dass der Benutzer das Formular schließen kann, ganz gleich, ob die Werte in den Steuerelementen gültig sind. In diesen Fällen kann die Überprüfung außer Kraft gesetzt und ein Formular geschlossen werden, auch wenn es ungültige Daten enthält. Dazu muss für das <xref:System.Windows.Forms.Form.FormClosing>-Ereignis des Formulars ein Handler erstellt werden. Im Ereignis muss die <xref:System.ComponentModel.CancelEventArgs.Cancel%2A>-Eigenschaft auf `false` festgelegt werden. Dadurch wird das Schließen des Formulars erzwungen. Weitere Informationen und ein Beispiel finden Sie unter <xref:System.Windows.Forms.Form.FormClosing?displayProperty=nameWithType>.

> [!NOTE]
> Wenn erzwungen wird, dass das Formular auf diese Weise geschlossen wird, gehen nicht gespeicherte Daten in den Steuerelementen des Formulars verloren. Zudem wird in modalen Formularen der Inhalt von Steuerelementen beim Schließen nicht überprüft. Sie können dennoch die Überprüfung von Steuerelementen verwenden, um den Fokus auf einem Steuerelement zu sperren. Um das Verhalten beim Schließen des Formulars müssen Sie sich jedoch nicht kümmern.

## <a name="see-also"></a>Siehe auch

- [Verwenden von Tastaturereignissen (Windows Forms .NET)](events.md)
- <xref:System.Windows.Forms.Control.Validating?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Form.FormClosing?displayProperty=nameWithType>
- <xref:System.Windows.Forms.FormClosingEventArgs?displayProperty=nameWithType>
