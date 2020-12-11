---
title: Binden von Daten an das DataGridView-Steuerelement mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, binding to a data source
- data sources [Windows Forms], binding to Windows Forms controls
- DataGridView control [Windows Forms], data binding
ms.assetid: f4f46009-cec2-441b-8668-6b5af057558b
ms.openlocfilehash: 6a8ffdbf950eb0fcda7b4752e6e9dd73a6df3f6f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975120"
---
# <a name="how-to-bind-data-to-the-windows-forms-datagridview-control-using-the-designer"></a>Vorgehensweise: Binden von Daten an das DataGridView-Steuerelement in Windows Forms mithilfe des Designers

Sie können den-Designer verwenden, um ein- <xref:System.Windows.Forms.DataGridView> Steuerelement mit Datenquellen verschiedener Variationen, einschließlich Datenbanken, Geschäftsobjekten oder Webdiensten, zu verbinden. Wenn Sie das Steuerelement mithilfe des Designers an eine Datenquelle binden, wird das Steuerelement automatisch an eine Komponente gebunden, die <xref:System.Windows.Forms.BindingSource> die Datenquelle darstellt. Darüber hinaus werden automatisch Spalten im Steuerelement erstellt, damit sie den Schemainformationen der Datenquelle entsprechen.

 Nachdem die Spalten erzeugt wurden, können Sie sie Ihren Bedürfnissen entsprechend ändern. Sie können z.B. Spalten entfernen oder ausblenden, die für Sie nicht interessant sind, die Spalten neu anordnen oder die Typen der Spalten ändern. Weitere Informationen zum Modifizieren von Spalten finden Sie in den Themen im Abschnitt „Siehe auch“.

 Sie können auch mehrere Steuer <xref:System.Windows.Forms.DataGridView> Elemente an verknüpfte Tabellen binden, um Master-/Detailbeziehungen zu erstellen. In dieser Konfiguration zeigt ein Steuerelement eine übergeordnete Tabelle und ein anderes Steuerelement nur die Reihen einer untergeordneten Tabelle an, die sich auf die aktuelle Reihe in der übergeordneten Tabelle beziehen. Weitere Informationen finden Sie unter [Vorgehensweise: Anzeigen von verknüpften Daten in einer Windows Forms-Anwendung](/previous-versions/visualstudio/visual-studio-2013/57tx3hhe(v=vs.120)).

 Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein <xref:System.Windows.Forms.DataGridView> -Steuerelement oder zwei-Steuerelemente für eine Master/Detail-Beziehung enthält. Weitere Informationen zum Starten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).

## <a name="to-bind-the-control-to-a-data-source"></a>So binden Sie das Steuerelement an eine Datenquelle

1. Klicken Sie ![ ](./media/designer-actions-glyph.gif) in der oberen rechten Ecke des Steuer Elements auf das Symbol für Designer Aktionen (kleiner schwarzer Pfeil) <xref:System.Windows.Forms.DataGridView> .

2. Klicken Sie auf den Dropdownpfeil für die Option **Datenquelle auswählen**.

3. Klicken Sie auf **Projektdatenquelle hinzufügen**, wenn Ihr Projekt noch nicht über eine Datenquelle verfügt, und befolgen Sie die Schritte des Assistenten.

     Weitere Informationen finden Sie unter [Assistent zum Konfigurieren von Datenquellen](/previous-versions/visualstudio/visual-studio-2013/w4dd7z6t(v=vs.120)). Die neue Datenquelle wird im Dropdownfenster **Datenquelle auswählen** angezeigt. Wenn Ihre neue Datenquelle nur einen Member enthält, z.B. eine einzelne Datenbanktabelle, bindet das Steuerelement automatisch an diesen Member. Fahren Sie andernfalls mit dem nächsten Schritt fort.

4. Erweitern Sie die Knoten **Weitere Datenquellen** und **Projektdatenquellen**, wenn Sie noch nicht erweitert sind, und wählen Sie die Datenquelle aus, an die Sie das Steuerelement binden wollen.

5. Wenn die Datenquelle mehr als ein Element enthält, z. b. Wenn Sie eine erstellt haben, die <xref:System.Data.DataSet?displayProperty=nameWithType> mehrere Tabellen enthält, erweitern Sie die Datenquelle, und wählen Sie dann den bestimmten Member aus, an den die Bindung erfolgen soll.

6. Zum Erstellen einer Master/Detail-Beziehung erweitern Sie im Dropdown Fenster **Datenquelle auswählen** für ein zweites <xref:System.Windows.Forms.DataGridView> Steuerelement das <xref:System.Windows.Forms.BindingSource> für die übergeordnete Tabelle erstellte, und wählen Sie dann in der angezeigten Liste die zugehörige untergeordnete Tabelle aus.

    > [!NOTE]
    > Wenn Ihr Projekt bereits über eine Datenquelle verfügt, können Sie auch das Fenster **Datenquellen** verwenden, um ein Datenformular zu erstellen. Weitere Informationen finden Sie unter [Datenquellenfenster](/previous-versions/visualstudio/visual-studio-2013/6ckyxa83(v=vs.120)).

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- <xref:System.Windows.Forms.DataGridView.DataMember%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.DataSource%2A?displayProperty=nameWithType>
- [Gewusst wie: Herstellen einer Verbindung zu Daten in einer Datenbank](/previous-versions/visualstudio/visual-studio-2013/fxk9yw1t(v=vs.120))
- [Vorgehensweise: Hinzufügen und Entfernen von Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers](add-and-remove-columns-in-the-datagrid-using-the-designer.md)
- [Vorgehensweise: Ändern der Reihenfolge von Spalten des DataGridView-Steuerelements in Windows Forms mithilfe des Designers](change-the-order-of-columns-in-the-datagrid-using-the-designer.md)
- [Vorgehensweise: Ändern des Typs einer DataGridView-Spalte in Windows Forms mithilfe des Designers](change-the-type-of-a-wf-datagridview-column-using-the-designer.md)
- [Vorgehensweise: Fixieren von Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers](freeze-columns-in-the-datagrid-using-the-designer.md)
- [Vorgehensweise: Ausblenden von Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers](hide-columns-in-the-datagrid-using-the-designer.md)
- [Vorgehensweise: Festlegen von schreibgeschützten Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers](make-columns-read-only-in-the-datagrid-using-the-designer.md)
- [Vorgehensweise: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [How to: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md)
- [Datenquellenfenster](/previous-versions/visualstudio/visual-studio-2013/6ckyxa83(v=vs.120))
- [Gewusst wie: Anzeigen von verknüpften Daten in einer Windows Forms-Anwendung](/previous-versions/visualstudio/visual-studio-2013/57tx3hhe(v=vs.120))
