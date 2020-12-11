---
title: Datenformatierung im DataGridView-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], formatting data
- data [Windows Forms], formatting in grids
- data grids [Windows Forms], formatting data
ms.assetid: 07bf558d-3748-42ba-8ba0-37fdef924081
ms.openlocfilehash: 3a09acf72841a2135ed2d155f3715ccc30860856
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972178"
---
# <a name="data-formatting-in-the-windows-forms-datagridview-control"></a>Datenformatierung im DataGridView-Steuerelement in Windows Forms

Das <xref:System.Windows.Forms.DataGridView> -Steuerelement ermöglicht die automatische Konvertierung zwischen Zellwerten und den Datentypen, die in den übergeordneten Spalten angezeigt werden. Text Feld Spalten zeigen z. b. Zeichen folgen Darstellungen von Datums-, Uhrzeit-, Zahlen-und Enumerationswerten an und Konvertieren vom Benutzer eingegebene Zeichen folgen Werte in die vom Datenspeicher benötigten Typen.  
  
## <a name="formatting-with-the-datagridviewcellstyle-class"></a>Formatieren mit der DataGridViewCellStyle-Klasse  

 Das- <xref:System.Windows.Forms.DataGridView> Steuerelement stellt grundlegende Datenformatierung von Zellwerten über die- <xref:System.Windows.Forms.DataGridViewCellStyle> Klasse bereit. Sie können die <xref:System.Windows.Forms.DataGridViewCellStyle.Format%2A> -Eigenschaft verwenden, um Datums-, Uhrzeit-, Zahlen-und Enumerationswerte für die aktuelle Standard Kultur mithilfe der in [Formatierungs Typen](/dotnet/standard/base-types/formatting-types)beschriebenen Formatspezifizierer zu formatieren. Sie können diese Werte auch für bestimmte Kulturen formatieren, indem Sie die- <xref:System.Windows.Forms.DataGridViewCellStyle.FormatProvider%2A> Eigenschaft verwenden. Das angegebene Format wird sowohl zum Anzeigen von Daten als auch zum Analysieren von Daten verwendet, die vom Benutzer im angegebenen Format eingegeben werden.  
  
 Die <xref:System.Windows.Forms.DataGridViewCellStyle> -Klasse stellt zusätzliche Formatierungs Eigenschaften für WordWrap, Textausrichtung und die benutzerdefinierte Anzeige von NULL-Daten bankwerten bereit. Weitere Informationen finden Sie unter [Vorgehensweise: Formatieren von Daten im DataGridView-Steuerelement in Windows Forms](how-to-format-data-in-the-windows-forms-datagridview-control.md).  
  
## <a name="formatting-with-the-cellformatting-event"></a>Formatieren mit dem cellformatierung-Ereignis  

 Wenn die grundlegende Formatierung nicht Ihren Anforderungen entspricht, können Sie eine benutzerdefinierte Datenformatierung in einem Handler für das-Ereignis bereitstellen <xref:System.Windows.Forms.DataGridView.CellFormatting?displayProperty=nameWithType> . Das <xref:System.Windows.Forms.DataGridViewCellFormattingEventArgs> an den Handler über gegebene verfügt über eine- <xref:System.Windows.Forms.ConvertEventArgs.Value%2A> Eigenschaft, die anfänglich den Zellwert enthält. Normalerweise wird dieser Wert automatisch in den Anzeigetyp konvertiert. Wenn Sie den Wert selbst konvertieren möchten, legen Sie die- <xref:System.Windows.Forms.ConvertEventArgs.Value%2A> Eigenschaft auf einen Wert des Anzeige Typs fest.  
  
> [!NOTE]
> Wenn für die Zelle eine Format Zeichenfolge aktiviert ist, überschreibt Sie die Änderung des <xref:System.Windows.Forms.ConvertEventArgs.Value%2A> Eigenschafts Werts, es sei denn, Sie legen die- <xref:System.Windows.Forms.DataGridViewCellFormattingEventArgs.FormattingApplied%2A> Eigenschaft auf fest `true` .  
  
 Das <xref:System.Windows.Forms.DataGridView.CellFormatting> Ereignis ist auch nützlich, wenn Sie <xref:System.Windows.Forms.DataGridViewCellStyle> Eigenschaften für einzelne Zellen basierend auf ihren Werten festlegen möchten. Weitere Informationen finden Sie unter Gewusst [wie: Anpassen der Datenformatierung im Windows Forms DataGridView-Steuer](how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md)Element.  
  
 Wenn die standardmäßige Verarbeitung von benutzerdefinierten Werten nicht Ihren Anforderungen entspricht, können Sie das-Ereignis des-Steuer Elements behandeln, <xref:System.Windows.Forms.DataGridView.CellParsing> <xref:System.Windows.Forms.DataGridView> um eine benutzerdefinierte-Verarbeitung bereitzustellen.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- [Anzeigen von Daten im DataGridView-Steuerelement in Windows Forms](displaying-data-in-the-windows-forms-datagridview-control.md)
- [Zellstile im DataGridView-Steuerelement in Windows Forms](cell-styles-in-the-windows-forms-datagridview-control.md)
- [Vorgehensweise: Formatieren von Daten im DataGridView-Steuerelement in Windows Forms](how-to-format-data-in-the-windows-forms-datagridview-control.md)
- [Gewusst wie: Anpassen der Datenformatierung im DataGridView-Steuerelement in Windows Forms](how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md)
