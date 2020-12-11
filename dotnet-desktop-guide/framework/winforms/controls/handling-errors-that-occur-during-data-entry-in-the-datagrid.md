---
title: 'Exemplarische Vorgehensweise: Behandeln von Fehlern, die während der Dateneingabe im DataGridView-Steuerelement auftreten'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- error handling [Windows Forms], dataGridView control
- data grids [Windows Forms], error handling
- DataGridView control [Windows Forms], error handling
- data entry [Windows Forms], error handling
- error handling [Windows Forms], data entry
- walkthroughs [Windows Forms], DataGridView control
ms.assetid: 30a68b85-d3af-4946-83c1-1e2d010d0511
ms.openlocfilehash: d65dd038ddc276ec09a1db3af4f14fc87fec56f2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975984"
---
# <a name="walkthrough-handling-errors-that-occur-during-data-entry-in-the-windows-forms-datagridview-control"></a>Exemplarische Vorgehensweise: Behandeln von Fehlern, die während der Dateneingabe im DataGridView-Steuerelement in Windows Forms auftreten

Das Behandeln von Fehlern aus dem zugrunde liegenden Datenspeicher ist ein erforderliches Feature für eine Dateneingabe Anwendung. Das Windows Forms-Steuerelement vereinfacht <xref:System.Windows.Forms.DataGridView> dies durch das verfügbar machen des- <xref:System.Windows.Forms.DataGridView.DataError> Ereignisses, das ausgelöst wird, wenn der Datenspeicher eine Einschränkungs Verletzung oder eine unterbrochene Geschäftsregel erkennt.

In dieser exemplarischen Vorgehensweise rufen Sie Zeilen aus der `Customers` -Tabelle in der Northwind-Beispieldatenbank ab und zeigen Sie in einem-Steuerelement an <xref:System.Windows.Forms.DataGridView> . Wenn ein doppelter `CustomerID` Wert in einer neuen Zeile oder einer bearbeiteten vorhandenen Zeile erkannt wird, tritt das- <xref:System.Windows.Forms.DataGridView.DataError> Ereignis auf, das durch Anzeigen einer behandelt wird, die <xref:System.Windows.Forms.MessageBox> die Ausnahme beschreibt.

Informationen zum Kopieren des Codes in diesem Thema als einzelne Auflistung finden Sie unter Gewusst [wie: Behandeln von Fehlern, die während der Dateneingabe im Windows Forms DataGridView-Steuerelement auftreten](handle-errors-that-occur-during-data-entry-in-the-datagrid.md).

## <a name="prerequisites"></a>Voraussetzungen

Für die Durchführung dieser exemplarischen Vorgehensweise benötigen Sie Folgendes:

- Zugriff auf einen Server mit der Beispieldatenbank Northwind SQL Server.

## <a name="creating-the-form"></a>Erstellen des Formulars

#### <a name="to-handle-data-entry-errors-in-the-datagridview-control"></a>So verarbeiten Sie Dateneingabe Fehler im DataGridView-Steuerelement

1. Erstellen Sie eine Klasse, die von abgeleitet ist <xref:System.Windows.Forms.Form> und ein <xref:System.Windows.Forms.DataGridView> -Steuerelement und eine- <xref:System.Windows.Forms.BindingSource> Komponente enthält.

    Im folgenden Codebeispiel wird die grundlegende Initialisierung und eine-Methode bereitstellt `Main` .

    [!code-csharp[System.Windows.Forms.DataGridView.DataError#01](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#01)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#01](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#01)]
    [!code-csharp[System.Windows.Forms.DataGridView.DataError#02](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#02)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#02](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#02)]

2. Implementieren Sie eine Methode in der Klassendefinition Ihres Formulars, um die Details der Verbindungs Herstellung mit der Datenbank zu verarbeiten.

    Dieses Codebeispiel verwendet eine- `GetData` Methode, die ein aufgefülltes Objekt zurückgibt <xref:System.Data.DataTable> . Stellen Sie sicher, dass Sie die `connectionString` Variable auf einen Wert festlegen, der für Ihre Datenbank geeignet ist.

    > [!IMPORTANT]
    > Das Speichern vertraulicher Informationen (z. B. eines Kennworts) innerhalb der Verbindungszeichenfolge kann die Sicherheit einer Anwendung beeinträchtigen. Der Zugriff auf eine Datenbank lässt sich mithilfe der Windows-Authentifizierung (wird auch als integrierte Sicherheit bezeichnet) sicherer steuern. Weitere Informationen finden Sie unter [Protecting Connection Information (Schützen von Verbindungsinformationen)](/dotnet/framework/data/adonet/protecting-connection-information).

    [!code-csharp[System.Windows.Forms.DataGridView.DataError#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#30)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#30)]

3. Implementieren Sie einen Handler für das- <xref:System.Windows.Forms.Form.Load> Ereignis des Formulars, das und initialisiert, <xref:System.Windows.Forms.DataGridView> <xref:System.Windows.Forms.BindingSource> und richtet die Datenbindung ein.

    [!code-csharp[System.Windows.Forms.DataGridView.DataError#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#10)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#10)]

4. Behandeln Sie das- <xref:System.Windows.Forms.DataGridView.DataError> Ereignis auf dem <xref:System.Windows.Forms.DataGridView> .

    Wenn der Kontext für den Fehler ein Commitvorgang ist, wird der Fehler in einem angezeigt <xref:System.Windows.Forms.MessageBox> .

    [!code-csharp[System.Windows.Forms.DataGridView.DataError#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#20)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#20)]

## <a name="testing-the-application"></a>Testen der Anwendung

Sie können das Formular jetzt testen, um sicherzustellen, dass das Verhalten wie erwartet ausfällt.

#### <a name="to-test-the-form"></a>So testen Sie das Formular

- Drücken Sie F5, um die Anwendung auszuführen.

  Sie sehen ein Steuerelement, <xref:System.Windows.Forms.DataGridView> das mit Daten aus der Customers-Tabelle gefüllt wird. Wenn Sie einen doppelten Wert für eingeben `CustomerID` und den Bearbeitungs Commit durchführen, wird der Zellwert automatisch wieder hergestellt, und es wird ein <xref:System.Windows.Forms.MessageBox> angezeigt, in dem der Dateneingabe Fehler angezeigt wird.

## <a name="next-steps"></a>Nächste Schritte

Diese Anwendung enthält grundlegende Kenntnisse über die <xref:System.Windows.Forms.DataGridView> Funktionen des-Steuer Elements. Sie können die Darstellung und das Verhalten des <xref:System.Windows.Forms.DataGridView> Steuer Elements auf verschiedene Weise anpassen:

- Ändern von Rahmen-und Header Stilen. Weitere Informationen finden Sie unter Gewusst [wie: Ändern der Rahmen-und Rasterlinien Stile im Windows Forms DataGridView-Steuer](change-the-border-and-gridline-styles-in-the-datagrid.md)Element.

- Aktivieren oder Einschränken der Benutzereingaben für das <xref:System.Windows.Forms.DataGridView> Steuerelement. Weitere Informationen finden Sie unter Gewusst [wie: verhindern des Hinzufügens und Löschens von Zeilen im Windows Forms DataGridView-Steuer](prevent-row-addition-and-deletion-datagridview.md)Element und Gewusst [wie: Erstellen von Spalten Read-Only im Windows Forms DataGridView-Steuer](how-to-make-columns-read-only-in-the-windows-forms-datagridview-control.md)Element.

- Überprüfen Sie die Benutzereingaben für das <xref:System.Windows.Forms.DataGridView> Steuerelement. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Validieren von Daten im Windows Forms DataGridView-Steuer](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)Element.

- Verarbeiten Sie sehr große Datasets im virtuellen Modus. Weitere Informationen finden Sie unter Exemplarische [Vorgehensweise: Implementieren des virtuellen Modus im Windows Forms DataGridView-Steuer](implementing-virtual-mode-wf-datagridview-control.md)Element.

- Passen Sie die Darstellung von Zellen an. Weitere Informationen finden Sie unter Gewusst [wie: Anpassen der Darstellung von Zellen im Windows Forms DataGridView-Steuer](customize-the-appearance-of-cells-in-the-datagrid.md) Element und Gewusst [wie: Festlegen von Standardzellen Formaten für das Windows Forms DataGridView-Steuer](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md)Element.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [Dateneingabe im DataGridView-Steuerelement in Windows Forms](data-entry-in-the-windows-forms-datagridview-control.md)
- [Vorgehensweise: Behandeln von Fehlern, die während der Dateneingabe im DataGridView-Steuerelement in Windows Forms auftreten](handle-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [Exemplarische Vorgehensweise: Validieren von Daten im DataGridView-Steuerelement in Windows Forms](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [Schützen von Verbindungsinformationen](/dotnet/framework/data/adonet/protecting-connection-information)
