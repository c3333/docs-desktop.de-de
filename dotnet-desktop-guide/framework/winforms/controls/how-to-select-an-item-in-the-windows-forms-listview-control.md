---
title: Wählen Sie ein Element im ListView-Steuerelement aus.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lists [Windows Forms], selecting items
- ListView control [Windows Forms], selecting items
- selection [Windows Forms], in list views
- list views [Windows Forms], selecting items
ms.assetid: ddea918e-1ddf-47f4-bd09-1e9b4c9d0c39
ms.openlocfilehash: 57e985af9d0347510d7d7782f68d5b414d36e077
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974747"
---
# <a name="how-to-select-an-item-in-the-windows-forms-listview-control"></a>Vorgehensweise: Auswählen eines Elements im ListView-Steuerelement in Windows Forms
In diesem Beispiel wird veranschaulicht, wie ein Element in einem Windows Forms-Steuerelement Programm gesteuert ausgewählt wird <xref:System.Windows.Forms.ListView> . Wenn Sie ein Element Programm gesteuert auswählen, wird der Fokus auf das Steuerelement nicht automatisch geändert <xref:System.Windows.Forms.ListView> . Aus diesem Grund möchten Sie das Element in der Regel auch als Fokus festlegen, wenn Sie ein Element auswählen.  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[System.Windows.Forms.ListView.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Misc/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.Misc/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Ein- <xref:System.Windows.Forms.ListView> Steuer `listView1` Element mit dem Namen, das mindestens ein Element enthält.  
  
- Verweise auf die Namespaces <xref:System?displayProperty=nameWithType> und <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListViewItem.Selected%2A?displayProperty=nameWithType>
