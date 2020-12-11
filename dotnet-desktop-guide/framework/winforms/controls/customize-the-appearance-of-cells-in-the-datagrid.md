---
title: Anpassen der Darstellung von Zellen im DataGridView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], customizing cells
- DataGridView control [Windows Forms], customizing cells
- cells [Windows Forms], customizing in DataGridView control
ms.assetid: 478b20c9-625c-4116-9c5c-5a16e6f4ec67
ms.openlocfilehash: 754932427a365a7b032c1ac9627d3237d1f7d0c6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972195"
---
# <a name="how-to-customize-the-appearance-of-cells-in-the-windows-forms-datagridview-control"></a>Gewusst wie: Anpassen der Darstellung von Zellen im DataGridView-Steuerelement von Windows Forms
Sie können die Darstellung jeder Zelle anpassen, indem Sie das <xref:System.Windows.Forms.DataGridView> -Ereignis des-Steuer Elements verarbeiten <xref:System.Windows.Forms.DataGridView.CellPainting> . Sie können die des <xref:System.Windows.Forms.DataGridView> -Steuer Elements <xref:System.Drawing.Graphics> aus der- <xref:System.Windows.Forms.DataGridViewCellPaintingEventArgs.Graphics%2A> Eigenschaft von extrahieren <xref:System.Windows.Forms.DataGridViewCellPaintingEventArgs> . Dadurch <xref:System.Drawing.Graphics> können Sie sich auf die Darstellung des gesamten Steuer Elements auswirken <xref:System.Windows.Forms.DataGridView> , aber Sie sollten sich in der Regel nur auf die Darstellung der Zelle auswirken, die gerade gezeichnet wird. Mithilfe der- <xref:System.Windows.Forms.DataGridViewCellPaintingEventArgs.ClipBounds%2A> Eigenschaft von <xref:System.Windows.Forms.DataGridViewCellPaintingEventArgs> können Sie Ihre Zeichnungsvorgänge auf die Zelle einschränken, die gerade gezeichnet wird.  
  
 Im folgenden Codebeispiel zeichnen Sie alle Zellen in einer `ContactName` Spalte mit dem <xref:System.Windows.Forms.DataGridView> Farbschema des Steuer Elements. Der Text Inhalt jeder Zelle wird in gezeichnet <xref:System.Drawing.Color.Crimson%2A> , und ein einfügen-Rechteck wird in derselben Farbe wie die <xref:System.Windows.Forms.DataGridView> -Eigenschaft des Steuer Elements gezeichnet <xref:System.Windows.Forms.DataGridView.GridColor%2A> .  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[System.Windows.Forms.DataGridViewCellPainting#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCellPainting/CS/form1.cs#10)]
 [!code-vb[System.Windows.Forms.DataGridViewCellPainting#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCellPainting/VB/form1.vb#10)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Ein <xref:System.Windows.Forms.DataGridView> Steuerelement `dataGridView1` mit dem Namen mit einer `ContactName` Spalte, z. b. in der Tabelle Customers in der Beispieldatenbank Northwind.  
  
- Verweise auf die Assemblys "System", "System.Windows.Forms" und "System.Drawing".  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.CellPainting>
- [Anpassen des DataGridView-Steuerelements von Windows Forms](customizing-the-windows-forms-datagridview-control.md)
