---
title: Erstellen einer Nachschlage Tabelle für das ComboBox-, ListBox-oder CheckedListBox-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- CheckedListBox control [Windows Forms], creating lookup tables
- lookup tables
- list boxes [Windows Forms], lookup tables
- ListBox control [Windows Forms], lookup tables
- ComboBox control [Windows Forms], lookup table
- lookup tables [Windows Forms], creating for controls
- combo boxes [Windows Forms], lookup tables
- ListBox control [Windows Forms], creating lookup tables
ms.assetid: 4ce35f12-1f4e-4317-92d1-af8686a8cfaa
ms.openlocfilehash: 57dc95fc16d77ee1492f53bf57eac001a343ca8f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972216"
---
# <a name="how-to-create-a-lookup-table-for-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a>Vorgehensweise: Erstellen einer Suchtabelle für ComboBox-, ListBox- oder CheckedListBox-Steuerelemente in Windows Forms

Manchmal ist es sinnvoll, Daten in einem benutzerfreundlichen Format in einem Windows Form anzuzeigen, aber Sie sollten die Daten in einem Format speichern, das vor allem für Ihr Programm sinnvoll ist. Beispielsweise können in einem Bestellformular für Nahrungsmittel die Menüelemente nach Namen in einem Listenfeld angezeigt werden. Die zur Erfassung der Bestellung verwendete Datentabelle enthält hingegen die eindeutigen ID-Nummern der Nahrungsmittel. Die folgende Tabelle enthält ein Beispiel zum Speichern und Anzeigen von Bestellformulardaten für Nahrungsmittel.  
  
### <a name="orderdetailstable"></a>OrderDetailsTable  
  
|OrderID|Artikel-ID|Menge|  
|-------------|------------|--------------|  
|4085|12|1|  
|4086|13|3|  
  
### <a name="itemtable"></a>ItemTable  
  
|id|Name|  
|--------|----------|  
|12|Kartoffel|  
|13|Huhn|  
  
 In diesem Szenario speichert eine Tabelle, **OrderDetailsTable**, die tatsächlichen Informationen, die Sie beim Anzeigen und speichern berücksichtigen. Allerdings geschieht dies aus Platzgründen auf eine ziemlich kryptische Art und Weise. Die andere Tabelle, **ItemTable**, enthält nur Darstellungs bezogene Informationen darüber, welche ID-Nummer mit welchem Nahrungsmittel Namen übereinstimmt, und nichts über die tatsächlichen Nahrungsmittel Bestellungen.  
  
 Das **ItemTable** -Steuerelement ist mit dem <xref:System.Windows.Forms.ComboBox> Steuerelement, <xref:System.Windows.Forms.ListBox> oder <xref:System.Windows.Forms.CheckedListBox> über drei Eigenschaften verbunden. Die- `DataSource` Eigenschaft enthält den Namen dieser Tabelle. Die- `DisplayMember` Eigenschaft enthält die Datenspalte der Tabelle, die im-Steuerelement (dem Nahrungsmittel Namen) angezeigt werden soll. Die- `ValueMember` Eigenschaft enthält die Datenspalte der Tabelle mit den gespeicherten Informationen (ID-Nummer).  
  
 " **OrderDetailsTable** " ist über seine Bindungs Auflistung mit dem Steuerelement verbunden, und der Zugriff erfolgt über die- <xref:System.Windows.Forms.Control.DataBindings%2A> Eigenschaft. Wenn Sie der Auflistung ein Bindungs Objekt hinzufügen, verbinden Sie eine Steuerelement Eigenschaft mit einem bestimmten Datenmember (der Spalte mit ID-Nummern) in einer Datenquelle ( **OrderDetailsTable**). Wenn im Steuerelement eine Auswahl getroffen wird, wird die Formulareingabe in dieser Tabelle gespeichert.  
  
### <a name="to-create-a-lookup-table"></a>So erstellen Sie eine Suchtabelle  
  
1. Fügen Sie dem Formular ein Steuerelement "<xref:System.Windows.Forms.ComboBox>", "<xref:System.Windows.Forms.ListBox>", oder "<xref:System.Windows.Forms.CheckedListBox>" hinzu.  
  
2. Stellen Sie eine Verbindung zur Datenquelle her.  
  
3. Richten Sie eine Datenbeziehung zwischen den beiden Tabellen ein. Weitere [Informationen finden Sie unter Einführung in DataRelations-Objekte](/previous-versions/visualstudio/visual-studio-2013/0k21zcyx(v=vs.120)).  
  
4. Legen Sie die folgenden Eigenschaften fest. Sie können im Code oder im Designer festgelegt werden.  
  
    |Eigenschaft|Einstellung|  
    |--------------|-------------|  
    |<xref:System.Windows.Forms.ListControl.DataSource%2A>|Die Tabelle, die Informationen darüber enthält, welche ID-Nummer welchem Element entspricht. Im vorherigen Szenario ist dies `ItemTable` .|  
    |<xref:System.Windows.Forms.ListControl.DisplayMember%2A>|Die Spalte der Datenquellentabelle, die im Steuerelement angezeigt werden soll. Im vorherigen Szenario ist dies `"Name"` (um im Code festzulegen, die Verwendung von Anführungszeichen).|  
    |<xref:System.Windows.Forms.ListControl.ValueMember%2A>|Die Spalte der Datenquellentabelle, die die gespeicherten Informationen enthält. Im vorherigen Szenario ist dies `"ID"` (um im Code festzulegen, die Verwendung von Anführungszeichen).|  
  
5. Rufen Sie in einer Prozedur die Methode "<xref:System.Windows.Forms.ControlBindingsCollection.Add%2A>" der Klasse "<xref:System.Windows.Forms.ControlBindingsCollection>" auf, um die Eigenschaft "<xref:System.Windows.Forms.ListControl.SelectedValue%2A>" des Steuerelements an die Tabelle zu binden, die die Formulareingabe erfasst. Sie können dies auch im Designer anstelle von im Code durchführen, indem Sie <xref:System.Windows.Forms.Control.DataBindings%2A> im **Eigenschaften** Fenster auf die-Eigenschaft des Steuer Elements zugreifen. Im vorherigen Szenario ist dies `OrderDetailsTable` , und die-Spalte ist `"ItemID"` .  
  
    ```vb  
    ListBox1.DataBindings.Add("SelectedValue", OrderDetailsTable, "ItemID")  
    ```  
  
    ```csharp  
    listBox1.DataBindings.Add("SelectedValue", OrderDetailsTable, "ItemID");  
    ```  
  
## <a name="see-also"></a>Siehe auch

- [Datenbindung und Windows Forms](../data-binding-and-windows-forms.md)
- [Übersicht über das ListBox-Steuerelement](listbox-control-overview-windows-forms.md)
- [Übersicht über das ComboBox-Steuerelement](combobox-control-overview-windows-forms.md)
- [Übersicht über das CheckedListBox-Steuerelement](checkedlistbox-control-overview-windows-forms.md)
- [Steuerelemente in Windows Forms zum Auflisten von Optionen](windows-forms-controls-used-to-list-options.md)
