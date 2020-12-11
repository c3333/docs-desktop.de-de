---
title: Anpassen des DataGridView-Steuer Elements
ms.date: 03/30/2017
helpviewer_keywords:
- data grids [Windows Forms], customization
- DataGridView control [Windows Forms], customization
ms.assetid: 01ea5d4c-a736-4596-b0e9-a67a1b86e15f
ms.openlocfilehash: 348c78d091679418f2452326555d49229bd2a8ea
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972192"
---
# <a name="customizing-the-windows-forms-datagridview-control"></a>Anpassen des DataGridView-Steuerelements von Windows Forms
Das `DataGridView` -Steuerelement bietet mehrere Eigenschaften, mit denen Sie die Darstellung und das grundlegende Verhalten (Aussehen und Verhalten) der Zellen, Zeilen und Spalten anpassen können. Wenn Sie besondere Anforderungen haben, die über die Funktionen der-Klasse hinausgehen, <xref:System.Windows.Forms.DataGridViewCellStyle> können Sie jedoch auch die Besitzer Zeichnung für das Steuerelement implementieren oder die Funktionen erweitern, indem Sie benutzerdefinierte Zellen, Spalten und Zeilen erstellen.  
  
 Um Zellen und Zeilen selbst zu zeichnen, können Sie verschiedene Zeichnungs `DataGridView` Ereignisse verarbeiten. Wenn Sie vorhandene Funktionen ändern oder neue Funktionen bereitstellen möchten, können Sie eigene Typen erstellen, die von den vorhandenen `DataGridViewCell` Typen, und abgeleitet werden `DataGridViewColumn` `DataGridViewRow` . Sie können auch neue Bearbeitungsfunktionen bereitstellen, indem Sie abgeleitete Typen erstellen, die ein Steuerelement ihrer Wahl anzeigen, wenn sich eine Zelle im Bearbeitungsmodus befindet.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Gewusst wie: Anpassen der Darstellung von Zellen im DataGridView-Steuerelement von Windows Forms](customize-the-appearance-of-cells-in-the-datagrid.md)  
 Beschreibt, wie das-Ereignis behandelt wird, <xref:System.Windows.Forms.DataGridView.CellPainting> um Zellen manuell zu zeichnen.  
  
 [Vorgehensweise: Anpassen der Darstellung von Zeilen im DataGridView-Steuerelement in Windows Forms](customize-the-appearance-of-rows-in-the-datagrid.md)  
 Beschreibt, wie das <xref:System.Windows.Forms.DataGridView.RowPrePaint> -Ereignis und das-Ereignis behandelt werden, um <xref:System.Windows.Forms.DataGridView.RowPostPaint> Zeilen mit einem benutzerdefinierten, Farbverlaufs Hintergrund und Inhalt zu zeichnen, der mehrere Spalten umfasst.  
  
 [Vorgehensweise: Anpassen von Zellen und Spalten im DataGridView-Steuerelement in Windows Forms durch Erweitern des Aussehens und Verhaltens](customize-cells-and-columns-in-the-datagrid-by-extending-behavior.md)  
 Beschreibt, wie benutzerdefinierte Typen erstellt werden, die von und abgeleitet werden `DataGridViewCell` `DataGridViewColumn` , um Zellen hervorzuheben, wenn der Mauszeiger darauf liegt.  
  
 [Vorgehensweise: Deaktivieren von Schaltflächen in einer Schaltflächenspalte im DataGridView-Steuerelement von Windows Forms](disable-buttons-in-a-button-column-in-the-datagrid.md)  
 Beschreibt, wie benutzerdefinierte Typen erstellt werden, die von und abgeleitet werden <xref:System.Windows.Forms.DataGridViewButtonCell> <xref:System.Windows.Forms.DataGridViewButtonColumn> , um deaktivierte Schaltflächen in einer Schaltflächen Spalte anzuzeigen.  
  
 [Vorgehensweise: Hosten von Steuerelementen in DataGridView-Zellen in Windows Forms](how-to-host-controls-in-windows-forms-datagridview-cells.md)  
 Beschreibt das Implementieren der- `IDataGridViewEditingControl` Schnittstelle und das Erstellen von benutzerdefinierten Typen, die von und abgeleitet werden `DataGridViewCell` `DataGridViewColumn` , um ein-Steuerelement anzuzeigen, <xref:System.Windows.Forms.DateTimePicker> Wenn sich eine Zelle im Bearbeitungsmodus befindet  
  
## <a name="reference"></a>Verweis  
 <xref:System.Windows.Forms.DataGridView>  
 Enthält die Referenzdokumentation für das <xref:System.Windows.Forms.DataGridView>-Steuerelement.  
  
 <xref:System.Windows.Forms.DataGridViewCell>  
 Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridViewCell> Klasse.  
  
 <xref:System.Windows.Forms.DataGridViewRow>  
 Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridViewRow> Klasse.  
  
 <xref:System.Windows.Forms.DataGridViewColumn>  
 Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridViewColumn> Klasse.  
  
 <xref:System.Windows.Forms.IDataGridViewEditingControl>  
 Enthält eine Referenz Dokumentation für die- <xref:System.Windows.Forms.IDataGridViewEditingControl> Schnittstelle.  
  
## <a name="related-sections"></a>Verwandte Abschnitte  
 [Grundlegende Formatierungen und Formate im DataGridView-Steuerelement in Windows Forms](basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)  
 Enthält Themen, in denen erörtert wird, wie die grundlegende Darstellung des Steuerelements sowie das Anzeigeformat von Zelldaten geändert werden.  
  
## <a name="see-also"></a>Siehe auch

- [DataGridView-Steuerelement](datagridview-control-windows-forms.md)
- [Spaltentypen im DataGridView-Steuerelement in Windows Forms](column-types-in-the-windows-forms-datagridview-control.md)
