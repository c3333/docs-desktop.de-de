---
title: Hinzufügen von Quick Infos zu einzelnen Zellen im DataGridView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tooltips [Windows Forms], adding to data grids
- DataGridView control [Windows Forms], adding tooltips
- data grids [Windows Forms], adding tooltips
ms.assetid: 2a81f9de-d58b-4ea8-bc0b-8d93c2f4cf78
ms.openlocfilehash: ac86db5fa27a95adb20888cd59b5e236941d9177
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975155"
---
# <a name="how-to-add-tooltips-to-individual-cells-in-a-windows-forms-datagridview-control"></a>Vorgehensweise: Hinzufügen von QuickInfos zu einzelnen Zellen in einem DataGridView-Steuerelement in Windows Forms
Standardmäßig werden Quick Infos zum Anzeigen der Werte von Zellen verwendet <xref:System.Windows.Forms.DataGridView> , die zu klein sind, um den gesamten Inhalt anzuzeigen. Sie können dieses Verhalten jedoch überschreiben, um QuickInfo-Textwerte für einzelne Zellen festzulegen. Dies ist hilfreich, um Benutzern zusätzliche Informationen zu einer Zelle anzuzeigen oder Benutzern eine alternative Beschreibung der Zellen Inhalte bereitzustellen. Wenn Sie z. b. eine Zeile haben, in der Statussymbole angezeigt werden, können Sie mithilfe von Quick Infos Texterklärungen angeben.  
  
 Sie können auch die Anzeige von Quick Infos auf Zellen Ebene deaktivieren, indem Sie die- <xref:System.Windows.Forms.DataGridView.ShowCellToolTips%2A?displayProperty=nameWithType> Eigenschaft auf festlegen `false` .  
  
### <a name="to-add-a-tooltip-to-a-cell"></a>So fügen Sie einer Zelle eine QuickInfo hinzu  
  
- Legen Sie die <xref:System.Windows.Forms.DataGridViewCell.ToolTipText%2A?displayProperty=nameWithType>-Eigenschaft fest.  
  
     [!code-cpp[System.Windows.Forms.DataGridViewCell.ToolTipText#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCell.ToolTipText/cpp/datagridviewcell.tooltiptext.cpp#1)]
     [!code-csharp[System.Windows.Forms.DataGridViewCell.ToolTipText#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCell.ToolTipText/CS/datagridviewcell.tooltiptext.cs#1)]
     [!code-vb[System.Windows.Forms.DataGridViewCell.ToolTipText#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCell.ToolTipText/VB/datagridviewcell.tooltiptext.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
  
- Für dieses Beispiel benötigen Sie Folgendes:  
  
- Ein <xref:System.Windows.Forms.DataGridView> Steuerelement `dataGridView1` mit dem Namen, das eine Spalte mit dem Namen `Rating` zum Anzeigen von Zeichen folgen Werten von einem bis vier Sternchen ("*") enthält. Das- <xref:System.Windows.Forms.DataGridView.CellFormatting> Ereignis des-Steuer Elements muss der im Beispiel gezeigten Ereignishandlermethode zugeordnet werden.  
  
- Verweise auf die Assemblys <xref:System?displayProperty=nameWithType> und <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="robust-programming"></a>Stabile Programmierung  
 Wenn Sie das <xref:System.Windows.Forms.DataGridView> Steuerelement an eine externe Datenquelle binden oder durch Implementieren des virtuellen Modus eine eigene Datenquelle bereitstellen, treten möglicherweise Leistungsprobleme auf. Um eine Leistungs Einbuße bei der Arbeit mit großen Datenmengen zu vermeiden, behandeln Sie das- <xref:System.Windows.Forms.DataGridView.CellToolTipTextNeeded> Ereignis, anstatt die- <xref:System.Windows.Forms.DataGridViewCell.ToolTipText%2A> Eigenschaft mehrerer Zellen festzulegen. Wenn Sie dieses Ereignis behandeln, wird durch das erhalten des Werts einer Zell <xref:System.Windows.Forms.DataGridViewCell.ToolTipText%2A> Eigenschaft das-Ereignis ausgelöst, und der Wert der <xref:System.Windows.Forms.DataGridViewCellToolTipTextNeededEventArgs.ToolTipText%2A?displayProperty=nameWithType> Eigenschaft wird wie im-Ereignishandler angegeben zurückgegeben.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.ShowCellToolTips%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.CellToolTipTextNeeded?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewCell>
- <xref:System.Windows.Forms.DataGridViewCell.ToolTipText%2A?displayProperty=nameWithType>
- [Programmieren mit Zellen, Zeilen und Spalten im DataGridView-Steuerelement in Windows Forms](programming-with-cells-rows-and-columns-in-the-datagrid.md)
