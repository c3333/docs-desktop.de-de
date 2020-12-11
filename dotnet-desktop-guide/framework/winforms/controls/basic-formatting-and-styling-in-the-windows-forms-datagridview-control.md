---
title: Grundlegende Formatierung und Formatierung im DataGridView-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], formatting and styling
- data grids [Windows Forms], formatting
ms.assetid: b9b90836-1f56-4aa9-8db8-edc78fe830e8
ms.openlocfilehash: d295718b7bd4f3bc4c5f63b6e6cb911f733525fe
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975144"
---
# <a name="basic-formatting-and-styling-in-the-windows-forms-datagridview-control"></a>Grundlegende Formatierungen und Formate im DataGridView-Steuerelement in Windows Forms
Das `DataGridView` -Steuerelement erleichtert das Definieren der grundlegenden Darstellung von Zellen und die Anzeige Formatierung von Zellwerten. Sie können Darstellung und Formatierungs Stile für einzelne Zellen, für Zellen in bestimmten Spalten und Zeilen oder für alle Zellen im Steuerelement definieren, indem Sie die Eigenschaften der Objekte festlegen, auf die `DataGridViewCellStyle` über verschiedene Steuerelement Eigenschaften zugegriffen wird `DataGridView` . Außerdem können Sie diese Stile dynamisch auf Grundlage von Faktoren wie dem Zellwert ändern, indem Sie das- `CellFormatting` Ereignis behandeln.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Vorgehensweise: Ändern des Rahmen- und Rasterlinienstils im DataGridView-Steuerelement in Windows Forms](change-the-border-and-gridline-styles-in-the-datagrid.md)  
 Beschreibt, wie Eigenschaften festgelegt werden `DataGridView` , die die Darstellung des Steuerelement Rahmens und der Begrenzungs Linien zwischen Zellen definieren.  
  
 [Zellstile im DataGridView-Steuerelement in Windows Forms](cell-styles-in-the-windows-forms-datagridview-control.md)  
 Beschreibt die `DataGridViewCellStyle` -Klasse und wie Eigenschaften dieses Typs interagieren, um zu definieren, wie Zellen im-Steuerelement angezeigt werden.  
  
 [Vorgehensweise: Festlegen von Standardzellenformaten für das DataGridView-Steuerelement in Windows Forms](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md)  
 Beschreibt, wie Eigenschaften verwendet werden `DataGridViewCellStyle` , um die Standarddarstellung von Zellen in bestimmten Zeilen und Spalten und im gesamten Steuerelement zu definieren.  
  
 [Vorgehensweise: Formatieren von Daten im DataGridView-Steuerelement in Windows Forms](how-to-format-data-in-the-windows-forms-datagridview-control.md)  
 Beschreibt, wie Zellen Anzeigewerte mithilfe von Eigenschaften formatiert werden `DataGridViewCellStyle` .  
  
 [Gewusst wie: Festlegen von Schriftart- und Farbstilen im DataGridView-Steuerelement in Windows Forms](how-to-set-font-and-color-styles-in-the-windows-forms-datagridview-control.md)  
 Beschreibt, wie die- `DefaultCellStyle` Eigenschaft verwendet wird, um grundlegende Anzeigeeigenschaften für alle Zellen im-Steuerelement festzulegen.  
  
 [Vorgehensweise: Festlegen von abwechselnden Zeilenstilen für das DataGridView-Steuerelement in Windows Forms](how-to-set-alternating-row-styles-for-the-windows-forms-datagridview-control.md)  
 Beschreibt, wie ein Ledger-ähnlicher Effekt im-Steuerelement mit abwechselnden Zeilen erstellt wird, die anders angezeigt werden.  
  
 [Vorgehensweise: Verwenden der Zeilenvorlage zum Anpassen von Zeilen im DataGridView-Steuerelement in Windows Forms](use-the-row-template-to-customize-rows-in-the-datagrid.md)  
 Beschreibt, wie die- `RowTemplate` Eigenschaft verwendet wird, um Zeilen Eigenschaften festzulegen, die für alle Zeilen im-Steuerelement verwendet werden.  
  
## <a name="reference"></a>Verweis  
 <xref:System.Windows.Forms.DataGridView>  
 Enthält die Referenzdokumentation für das <xref:System.Windows.Forms.DataGridView>-Steuerelement.  
  
 <xref:System.Windows.Forms.DataGridViewCellStyle>  
 Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridViewCellStyle> Klasse.  
  
 <xref:System.Windows.Forms.DataGridView.CellFormatting>  
 Enthält die Referenz Dokumentation für das- <xref:System.Windows.Forms.DataGridView.CellFormatting> Ereignis.  
  
 <xref:System.Windows.Forms.DataGridView.RowTemplate%2A>  
 Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridView.RowTemplate%2A> Eigenschaft.  
  
## <a name="related-sections"></a>Verwandte Abschnitte  
 [Anpassen des DataGridView-Steuerelements von Windows Forms](customizing-the-windows-forms-datagridview-control.md)  
 Enthält Themen, in denen das benutzerdefinierte Zeichnen von <xref:System.Windows.Forms.DataGridView>-Zellen und Zeilen und das Erstellen von abgeleiteten Zell-, Spalten- und Zeilentypen beschrieben wird.  
  
 [Grundlegende Spalten-, Zeilen- und Zellfunktionen im DataGridView-Steuerelement in Windows Forms](basic-column-row-and-cell-features-wf-datagridview-control.md)  
 Stellt Themen bereit, in denen häufig verwendete Zellen-, Zeilen-und Spalten Eigenschaften beschrieben werden.  
  
## <a name="see-also"></a>Siehe auch

- [DataGridView-Steuerelement](datagridview-control-windows-forms.md)
