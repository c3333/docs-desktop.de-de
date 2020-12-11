---
title: Erstellen eines ungebundenen DataGridView-Steuer Elements
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data [Windows Forms], displaying without binding to data source
- DataGridView control [Windows Forms], unbound data
- DataGridView control [Windows Forms], displaying data without binding to a data source
- data [Windows Forms], unbound
- walkthroughs [Windows Forms], DataGridView control
ms.assetid: 5a8d6afa-1b4b-4b24-8db8-501086ffdebe
ms.openlocfilehash: ceb75d4ee845d1f643d4d88d5a9f1bde73edcc70
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977307"
---
# <a name="walkthrough-creating-an-unbound-windows-forms-datagridview-control"></a>Exemplarische Vorgehensweise: Erstellen eines ungebundenen DataGridView-Steuerelements in Windows Forms
Möglicherweise möchten Sie häufig Tabellendaten anzeigen, die nicht aus einer Datenbank stammen. Beispielsweise möchten Sie möglicherweise den Inhalt eines zweidimensionalen Arrays von Zeichen folgen anzeigen. Die <xref:System.Windows.Forms.DataGridView> -Klasse stellt eine einfache und hochgradig anpassbare Möglichkeit zum Anzeigen von Daten ohne Bindung an eine Datenquelle bereit. In dieser exemplarischen Vorgehensweise wird gezeigt, wie Sie ein Steuerelement auffüllen <xref:System.Windows.Forms.DataGridView> und das Hinzufügen und Löschen von Zeilen im ungebundenen Modus verwalten. Standardmäßig kann der Benutzer neue Zeilen hinzufügen. Um die Zeilen Addition zu verhindern, legen Sie die-Eigenschaft auf fest <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A> `false` .  
  
 Informationen zum Kopieren des Codes in diesem Thema als einzelne Auflistung finden Sie unter Gewusst [wie: Erstellen eines ungebundenen Windows Forms DataGridView-Steuer](how-to-create-an-unbound-windows-forms-datagridview-control.md)Elements.  
  
## <a name="creating-the-form"></a>Erstellen des Formulars  
  
#### <a name="to-use-an-unbound-datagridview-control"></a>So verwenden Sie ein ungebundenes DataGridView-Steuerelement  
  
1. Erstellen Sie eine Klasse, die von abgeleitet wird <xref:System.Windows.Forms.Form> und die folgenden Variablen Deklarationen und- `Main` Methoden enthält.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSimpleUnbound#01](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/CS/simpleunbound.cs#01)]
     [!code-vb[System.Windows.Forms.DataGridViewSimpleUnbound#01](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/VB/simpleunbound.vb#01)]  
    [!code-csharp[System.Windows.Forms.DataGridViewSimpleUnbound#02](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/CS/simpleunbound.cs#02)]
    [!code-vb[System.Windows.Forms.DataGridViewSimpleUnbound#02](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/VB/simpleunbound.vb#02)]  
  
2. Implementieren Sie eine `SetupLayout` Methode in der Klassendefinition Ihres Formulars, um das Layout des Formulars einzurichten.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSimpleUnbound#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/CS/simpleunbound.cs#20)]
     [!code-vb[System.Windows.Forms.DataGridViewSimpleUnbound#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/VB/simpleunbound.vb#20)]  
  
3. Erstellen Sie eine `SetupDataGridView` Methode zum Einrichten der <xref:System.Windows.Forms.DataGridView> Spalten und Eigenschaften.  
  
     Diese Methode fügt zuerst das <xref:System.Windows.Forms.DataGridView> -Steuerelement zur-Auflistung des Formulars hinzu <xref:System.Windows.Forms.Control.Controls%2A> . Als nächstes wird die Anzahl der anzuzeigenden Spalten mithilfe der- <xref:System.Windows.Forms.DataGridView.ColumnCount%2A> Eigenschaft festgelegt. Der Standardstil für die Spaltenheader wird festgelegt, indem <xref:System.Windows.Forms.DataGridViewCellStyle.BackColor%2A> die <xref:System.Windows.Forms.DataGridViewCellStyle.ForeColor%2A> Eigenschaften, und <xref:System.Windows.Forms.DataGridViewCellStyle.Font%2A> der von <xref:System.Windows.Forms.DataGridViewCellStyle> der-Eigenschaft zurückgegebenen <xref:System.Windows.Forms.DataGridView.ColumnHeadersDefaultCellStyle%2A> festgelegt werden.  
  
     Layout-und Darstellungs Eigenschaften werden festgelegt, und dann werden die Spaltennamen zugewiesen. Wenn diese Methode beendet wird, kann das Steuerelement aufgefüllt <xref:System.Windows.Forms.DataGridView> werden.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSimpleUnbound#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/CS/simpleunbound.cs#30)]
     [!code-vb[System.Windows.Forms.DataGridViewSimpleUnbound#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/VB/simpleunbound.vb#30)]  
  
4. Erstellen Sie eine- `PopulateDataGridView` Methode, um dem-Steuerelement Zeilen hinzuzufügen <xref:System.Windows.Forms.DataGridView> .  
  
     Jede Zeile stellt einen Song und die zugehörigen Informationen dar.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSimpleUnbound#40](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/CS/simpleunbound.cs#40)]
     [!code-vb[System.Windows.Forms.DataGridViewSimpleUnbound#40](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/VB/simpleunbound.vb#40)]  
  
5. Wenn die Hilfsprogrammmethoden vorhanden sind, können Sie Ereignishandler anfügen.  
  
     Sie behandeln die-Ereignisse der Schaltflächen **Hinzufügen** und **Löschen** <xref:System.Windows.Forms.Control.Click> , das-Ereignis des Formulars <xref:System.Windows.Forms.Form.Load> und das <xref:System.Windows.Forms.DataGridView> -Ereignis des-Steuer Elements <xref:System.Windows.Forms.DataGridView.CellFormatting> .  
  
     Wenn das-Ereignis der Schaltfläche " **Hinzufügen** " <xref:System.Windows.Forms.Control.Click> ausgelöst wird, wird dem eine neue leere Zeile hinzugefügt <xref:System.Windows.Forms.DataGridView> .  
  
     Wenn das-Ereignis der Schaltfläche " **Löschen** " <xref:System.Windows.Forms.Control.Click> ausgelöst wird, wird die ausgewählte Zeile gelöscht, es sei denn, es handelt sich um die Zeile für neue Datensätze, sodass der Benutzer neue Zeilen hinzufügen kann. Diese Zeile ist immer die letzte Zeile im- <xref:System.Windows.Forms.DataGridView> Steuerelement.  
  
     Wenn das-Ereignis des Formulars <xref:System.Windows.Forms.Form.Load> ausgelöst wird, `SetupLayout` `SetupDataGridView` werden die `PopulateDataGridView` Hilfsprogrammmethoden, und aufgerufen.  
  
     Wenn das- <xref:System.Windows.Forms.DataGridView.CellFormatting> Ereignis ausgelöst wird, wird jede Zelle in der `Date` Spalte als langes Datum formatiert, es sei denn, der Wert der Zelle kann nicht analysiert werden.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSimpleUnbound#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/CS/simpleunbound.cs#10)]
     [!code-vb[System.Windows.Forms.DataGridViewSimpleUnbound#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSimpleUnbound/VB/simpleunbound.vb#10)]  
  
## <a name="testing-the-application"></a>Testen der Anwendung  
 Sie können das Formular jetzt testen, um sicherzustellen, dass das Verhalten wie erwartet ausfällt.  
  
#### <a name="to-test-the-form"></a>So testen Sie das Formular  
  
- Drücken Sie F5, um die Anwendung auszuführen.  
  
     Ein Steuerelement wird <xref:System.Windows.Forms.DataGridView> angezeigt, in dem die in aufgeführten Titel angezeigt werden `PopulateDataGridView` . Mit der Schaltfläche **Zeile hinzufügen** können Sie neue Zeilen hinzufügen, und Sie können die ausgewählten Zeilen mit der Schaltfläche **Zeile löschen** löschen. Das ungebundene <xref:System.Windows.Forms.DataGridView> Steuerelement ist der Datenspeicher, und seine Daten sind unabhängig von einer externen Quelle, z. b. einem- <xref:System.Data.DataSet> Array oder einem-Array.  
  
## <a name="next-steps"></a>Nächste Schritte  
 Diese Anwendung enthält grundlegende Kenntnisse über die <xref:System.Windows.Forms.DataGridView> Funktionen des-Steuer Elements. Sie können die Darstellung und das Verhalten des <xref:System.Windows.Forms.DataGridView> Steuer Elements auf verschiedene Weise anpassen:  
  
- Ändern von Rahmen-und Header Stilen. Weitere Informationen finden Sie unter Gewusst [wie: Ändern der Rahmen-und Rasterlinien Stile im Windows Forms DataGridView-Steuer](change-the-border-and-gridline-styles-in-the-datagrid.md)Element.  
  
- Aktivieren oder Einschränken der Benutzereingaben für das <xref:System.Windows.Forms.DataGridView> Steuerelement. Weitere Informationen finden Sie unter Gewusst [wie: verhindern des Hinzufügens und Löschens von Zeilen im Windows Forms DataGridView-Steuer](prevent-row-addition-and-deletion-datagridview.md)Element und Gewusst [wie: Erstellen von Spalten Read-Only im Windows Forms DataGridView-Steuer](how-to-make-columns-read-only-in-the-windows-forms-datagridview-control.md)Element.  
  
- Überprüfen Sie die Benutzereingaben auf datenbankbezogene Fehler. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Behandeln von Fehlern, die während der Dateneingabe im Windows Forms DataGridView-Steuerelement auftreten](handling-errors-that-occur-during-data-entry-in-the-datagrid.md).  
  
- Verarbeiten Sie sehr große Datasets im virtuellen Modus. Weitere Informationen finden Sie unter Exemplarische [Vorgehensweise: Implementieren des virtuellen Modus im Windows Forms DataGridView-Steuer](implementing-virtual-mode-wf-datagridview-control.md)Element.  
  
- Passen Sie die Darstellung von Zellen an. Weitere Informationen finden Sie unter Gewusst [wie: Anpassen der Darstellung von Zellen im Windows Forms DataGridView-Steuer](customize-the-appearance-of-cells-in-the-datagrid.md) Element und Gewusst [wie: Festlegen von Standardzellen Formaten für das Windows Forms DataGridView-Steuer](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md)Element.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- [Anzeigen von Daten im DataGridView-Steuerelement in Windows Forms](displaying-data-in-the-windows-forms-datagridview-control.md)
- [Vorgehensweise: Erstellen eines ungebundenen DataGridView-Steuerelements in Windows Forms](how-to-create-an-unbound-windows-forms-datagridview-control.md)
- [Datenanzeigemodi im DataGridView-Steuerelement in Windows Forms](data-display-modes-in-the-windows-forms-datagridview-control.md)
