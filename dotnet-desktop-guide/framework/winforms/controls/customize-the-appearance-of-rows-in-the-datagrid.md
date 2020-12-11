---
title: Anpassen der Darstellung von Zeilen im DataGridView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], customizing rows
- rows [Windows Forms], customizing in DataGridView control
- DataGridView control [Windows Forms], customizing rows
ms.assetid: d40b53d2-7e7c-48c5-8570-6e79d15c3bbb
ms.openlocfilehash: 099b2104e7a4887aa846c4d65273db2dd4f60559
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972194"
---
# <a name="how-to-customize-the-appearance-of-rows-in-the-windows-forms-datagridview-control"></a>Vorgehensweise: Anpassen der Darstellung von Zeilen im DataGridView-Steuerelement in Windows Forms
Sie können die Darstellung von <xref:System.Windows.Forms.DataGridView>-Zeilen steuern, indem Sie eines oder beide der Ereignisse <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType> und <xref:System.Windows.Forms.DataGridView.RowPostPaint?displayProperty=nameWithType> behandeln. Diese Ereignisse sind so konzipiert, dass Sie nur das Gewünschte zeichnen und das <xref:System.Windows.Forms.DataGridView>-Steuerelement den Rest zeichnen lassen. Wenn Sie beispielsweise einen benutzerdefinierten Hintergrund zeichnen möchten, können Sie das <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType>-Ereignis behandeln und dafür sorgen, dass einzelne Zellen ihren eigenen Vordergrundinhalt zeichnen. Alternativ können Sie dafür sorgen, dass sich die Zellen selbst zeichnen und in einem Handler des <xref:System.Windows.Forms.DataGridView.RowPostPaint?displayProperty=nameWithType>-Ereignisses benutzerdefinierte Vordergrundinhalte hinzufügen. Sie können auch das Zeichnen von Zellen deaktivieren und in einem <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType>-Ereignishandler alles selbst zeichnen.  
  
 Im folgende Codebeispiel werden Handler für beide Ereignisse implementiert, um einen Hintergrund mit einer Farbverlaufsauswahl und einige benutzerdefinierte Vordergrundinhalte bereitzustellen, die über mehrere Spalten gehen.  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[System.Windows.Forms.DataGridViewRowPainting#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRowPainting/CS/datagridviewrowpainting.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewRowPainting#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRowPainting/VB/datagridviewrowpainting.vb#00)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.RowPrePaint?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.RowPostPaint?displayProperty=nameWithType>
- [Anpassen des DataGridView-Steuerelements von Windows Forms](customizing-the-windows-forms-datagridview-control.md)
- [Architektur des DataGridView-Steuerelements](datagridview-control-architecture-windows-forms.md)
