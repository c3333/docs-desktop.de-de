---
title: Hinzufügen von Tabellen und Spalten zum DataGrid-Steuerelement mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- columns [Windows Forms], adding to DataGrid control
- tables [Windows Forms], adding to DataGrid control
- DataGrid control [Windows Forms], adding tables and columns
ms.assetid: 4a6d1b34-b696-476b-bf8a-57c6230aa9e1
ms.openlocfilehash: 7d00deb453793f7fc1f1c5d59913cb704ad546d9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975793"
---
# <a name="how-to-add-tables-and-columns-to-the-windows-forms-datagrid-control-using-the-designer"></a>Vorgehensweise: Hinzufügen von Tabellen und Spalten zum DataGrid-Steuerelement in Windows Forms mithilfe des Designers

> [!NOTE]
> Obwohl das <xref:System.Windows.Forms.DataGridView>-Steuerelement das <xref:System.Windows.Forms.DataGrid>-Steuerelement ersetzt und funktionell erweitert, wird das <xref:System.Windows.Forms.DataGrid>-Steuerelement sowohl aus Gründen der Abwärtskompatibilität als auch, falls gewünscht, für die zukünftige Verwendung beibehalten. Weitere Informationen finden Sie unter [Unterschiede zwischen dem DataGridView-Steuerelement und dem DataGrid-Steuerelement in Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).

Sie können Daten im Windows Forms- <xref:System.Windows.Forms.DataGrid> Steuerelement in Tabellen und Spalten anzeigen, indem Sie <xref:System.Windows.Forms.DataGridTableStyle> -Objekte erstellen und Sie dem-Objekt hinzufügen <xref:System.Windows.Forms.GridTableStylesCollection> , auf das über die <xref:System.Windows.Forms.DataGrid> -Eigenschaft des-Steuer Elements zugegriffen wird <xref:System.Windows.Forms.DataGrid.TableStyles%2A> . Jedes Tabellenformat zeigt den Inhalt einer beliebigen Datentabelle an, die in der- <xref:System.Windows.Forms.DataGridTableStyle.MappingName%2A> Eigenschaft von angegeben ist <xref:System.Windows.Forms.DataGridTableStyle> . Standardmäßig werden in einem Tabellenformat ohne angegebene Spalten Formate alle Spalten in der Datentabelle angezeigt. Sie können einschränken, welche Spalten aus der Tabelle angezeigt werden, indem Sie-Objekte hinzufügen <xref:System.Windows.Forms.DataGridColumnStyle> <xref:System.Windows.Forms.GridColumnStylesCollection> , auf die über die- <xref:System.Windows.Forms.DataGridTableStyle.GridColumnStyles%2A> Eigenschaft der einzelnen Objekte zugegriffen wird <xref:System.Windows.Forms.DataGridTableStyle> .

Die folgenden Prozeduren erfordern ein **Windows-Anwendungs** Projekt mit einem Formular, das ein-Steuerelement enthält <xref:System.Windows.Forms.DataGrid> . Weitere Informationen zum Einrichten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md). Standardmäßig befindet sich das Steuerelement in Visual Studio 2005 <xref:System.Windows.Forms.DataGrid> nicht in der **Toolbox**. Weitere Informationen zum Hinzufügen finden Sie unter Gewusst [wie: Hinzufügen von Elementen zur Toolbox](/previous-versions/visualstudio/visual-studio-2010/ms165355(v=vs.100)).

### <a name="to-add-a-table-to-the-datagrid-control-in-the-designer"></a>So fügen Sie dem DataGrid-Steuerelement im Designer eine Tabelle hinzu

1. Um Daten in der Tabelle anzuzeigen, müssen Sie zuerst das <xref:System.Windows.Forms.DataGrid> Steuerelement an ein DataSet binden. Weitere Informationen finden Sie unter Gewusst [wie: Binden des Windows Forms DataGrid-Steuer Elements an eine Datenquelle mithilfe des Designers](bind-wf-datagrid-control-to-a-data-source-using-the-designer.md).

2. Wählen Sie <xref:System.Windows.Forms.DataGrid> im Eigenschaftenfenster die-Eigenschaft des Steuer Elements <xref:System.Windows.Forms.DataGrid.TableStyles%2A> aus, und klicken Sie dann auf die Schaltfläche mit den Auslassungs Punkten ( ![ ...) in der Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ) neben der-Eigenschaft, um den **DataGridTableStyle**-Auflistungs-Editor anzuzeigen.

3. Klicken Sie im Auflistungs-Editor auf **Hinzufügen** , um einen Tabellen Stil einzufügen.

4. Klicken Sie auf **OK** , um den Auflistungs-Editor zu schließen, und öffnen Sie ihn dann erneut, indem Sie neben der-Eigenschaft auf die Schaltfläche <xref:System.Windows.Forms.DataGrid.TableStyles%2A>

     Wenn Sie den Auflistungs-Editor erneut öffnen, werden alle Datentabellen, die an das-Steuerelement gebunden sind, in der Dropdown Liste für die- <xref:System.Windows.Forms.DataGridTableStyle.MappingName%2A> Eigenschaft des Tabellen Stils angezeigt.

5. Klicken Sie im Auflistungs-Editor im Feld **Mitglieder** auf den Tabellen Stil.

6. Wählen Sie im **Eigenschaften** Feld des Auflistungs-Editors den <xref:System.Windows.Forms.DataGridTableStyle.MappingName%2A> Wert für die Tabelle aus, die Sie anzeigen möchten.

### <a name="to-add-a-column-to-the-datagrid-control-in-the-designer"></a>So fügen Sie dem DataGrid-Steuerelement im Designer eine Spalte hinzu

1. Wählen Sie im **DataGridTableStyle**-Auflistungs-Editor im Feld **Mitglieder** den entsprechenden Tabellen Stil aus. Wählen Sie im **Eigenschaften** Feld des Auflistungs-Editors die Auflistung aus <xref:System.Windows.Forms.DataGridTableStyle.GridColumnStyles%2A> , und klicken Sie dann auf die Schaltfläche mit den Auslassungs Punkten ( ![ ...) im Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ) neben der-Eigenschaft, um den **DataGridColumnStyle**-Auflistungs-Editor anzuzeigen.

2. Klicken Sie im Auflistungs-Editor auf **Hinzufügen** , um einen Spalten Stil einzufügen, oder auf den Pfeil nach unten neben **Hinzufügen** , um einen Spaltentyp anzugeben.

     Im Dropdown Feld können Sie entweder den- <xref:System.Windows.Forms.DataGridTextBoxColumn> Typ oder den- <xref:System.Windows.Forms.DataGridBoolColumn> Typ auswählen.

3. Klicken Sie auf OK, um den **DataGridColumnStyle**-Auflistungs-Editor zu schließen, und öffnen Sie ihn dann erneut, indem Sie neben der-Eigenschaft auf die Schaltfläche <xref:System.Windows.Forms.DataGridTableStyle.GridColumnStyles%2A>

     Wenn Sie den Auflistungs-Editor erneut öffnen, werden alle Datenspalten in der gebundenen Datentabelle in der Dropdown Liste für die- <xref:System.Windows.Forms.DataGridColumnStyle.MappingName%2A> Eigenschaft des Spalten Stils angezeigt.

4. Klicken Sie im Auflistungs-Editor im Feld **Mitglieder** auf den Spalten Stil.

5. Wählen Sie im **Eigenschaften** Feld des Auflistungs-Editors den <xref:System.Windows.Forms.DataGridColumnStyle.MappingName%2A> Wert für die Spalte aus, die Sie anzeigen möchten.

## <a name="see-also"></a>Siehe auch

- [DataGrid-Steuerelement](datagrid-control-windows-forms.md)
- [Vorgehensweise: Löschen oder Ausblenden von Spalten aus dem DataGrid-Steuerelement in Windows Forms](how-to-delete-or-hide-columns-in-the-windows-forms-datagrid-control.md)
