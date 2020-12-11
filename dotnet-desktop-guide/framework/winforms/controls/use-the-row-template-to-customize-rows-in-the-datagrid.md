---
title: Verwenden der Zeilen Vorlage zum Anpassen von Zeilen im DataGridView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- data grids [Windows Forms], customizing rows
- DataGridView control [Windows Forms], customizing rows
ms.assetid: 6db61607-7e57-4a84-8d63-9d6a7ed7f9ff
ms.openlocfilehash: 35cb95f22c0caa654bf149b5fc4fd0395696a411
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976629"
---
# <a name="how-to-use-the-row-template-to-customize-rows-in-the-windows-forms-datagridview-control"></a>Vorgehensweise: Verwenden der Zeilenvorlage zum Anpassen von Zeilen im DataGridView-Steuerelement in Windows Forms
Das- <xref:System.Windows.Forms.DataGridView> Steuerelement verwendet die Zeilen Vorlage als Grundlage für alle Zeilen, die dem Steuerelement entweder über die Datenbindung hinzugefügt werden, oder wenn die-Methode aufgerufen wird, <xref:System.Windows.Forms.DataGridViewRowCollection.Add%2A?displayProperty=nameWithType> ohne eine vorhandene zu verwendende Zeile anzugeben.  
  
 Mit der Zeilen Vorlage können Sie die Darstellung und das Verhalten von Zeilen besser steuern, als die- <xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A> Eigenschaft bereitstellt. Mit der Zeilen Vorlage können Sie alle Eigenschaften festlegen <xref:System.Windows.Forms.DataGridViewRow> , einschließlich <xref:System.Windows.Forms.DataGridViewRow.DefaultCellStyle%2A> .  
  
 Es gibt einige Situationen, in denen Sie die Zeilen Vorlage verwenden müssen, um einen bestimmten Effekt zu erzielen. Beispielsweise können Informationen zur Zeilenhöhe nicht in einem gespeichert werden <xref:System.Windows.Forms.DataGridViewCellStyle> . Daher müssen Sie eine Zeilen Vorlage verwenden, um die von allen Zeilen verwendete Standardhöhe zu ändern. Die Zeilen Vorlage ist auch nützlich, wenn Sie Ihre eigenen Klassen erstellen, die von abgeleitet <xref:System.Windows.Forms.DataGridViewRow> sind, und Sie möchten, dass der benutzerdefinierte Typ verwendet wird, wenn dem Steuerelement neue Zeilen hinzugefügt werden  
  
> [!NOTE]
> Die Zeilen Vorlage wird nur verwendet, wenn Zeilen hinzugefügt werden. Vorhandene Zeilen können nicht durch Ändern der Zeilen Vorlage geändert werden.  
  
### <a name="to-use-the-row-template"></a>So verwenden Sie die Zeilen Vorlage  
  
- Legen Sie Eigenschaften für das von der-Eigenschaft abgerufene Objekt fest <xref:System.Windows.Forms.DataGridView.RowTemplate%2A?displayProperty=nameWithType> .  
  
     [!code-cpp[System.Windows.Forms.DataGridView.RowTemplate#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.RowTemplate/CPP/datagridviewrowtemplate.cpp#1)]
     [!code-csharp[System.Windows.Forms.DataGridView.RowTemplate#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.RowTemplate/CS/datagridviewrowtemplate.cs#1)]
     [!code-vb[System.Windows.Forms.DataGridView.RowTemplate#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.RowTemplate/VB/datagridviewrowtemplate.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Ein <xref:System.Windows.Forms.DataGridView>-Steuerelement namens `dataGridView1`.  
  
- Verweise auf die Assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType> und <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- <xref:System.Windows.Forms.DataGridViewRow>
- <xref:System.Windows.Forms.DataGridView.RowTemplate%2A?displayProperty=nameWithType>
- [Grundlegende Formatierungen und Formate im DataGridView-Steuerelement in Windows Forms](basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)
- [Zellstile im DataGridView-Steuerelement in Windows Forms](cell-styles-in-the-windows-forms-datagridview-control.md)
