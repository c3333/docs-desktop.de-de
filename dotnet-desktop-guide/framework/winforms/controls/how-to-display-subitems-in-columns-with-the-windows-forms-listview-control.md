---
title: Anzeigen von unter Elementen in Spalten mit dem ListView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- list items
- Details view
- ListView control [Windows Forms], adding ListSubItems
- subitems
ms.assetid: e465f044-cde7-4fd9-a687-788a73a0f554
ms.openlocfilehash: 5c6d807410ad4ee0198d6334844bd65b148edff4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976505"
---
# <a name="how-to-display-subitems-in-columns-with-the-windows-forms-listview-control"></a>Vorgehensweise: Anzeigen von Unterelementen in Spalten mit dem ListView-Steuerelement in Windows Forms
Das Windows Forms <xref:System.Windows.Forms.ListView> Steuerelement kann für jedes Element in der Detailansicht zusätzlichen Text oder unter Elemente anzeigen. In der ersten Spalte wird der Element Text angezeigt, z. b. eine Mitarbeiternummer. In den zweiten, dritten und nachfolgenden Spalten werden das erste, zweite und nachfolgende zugehörige Unterelement angezeigt.  
  
### <a name="to-add-subitems-to-a-list-item"></a>So fügen Sie einem Listenelement unter Elemente hinzu  
  
1. Fügen Sie alle benötigten Spalten hinzu. Da in der ersten Spalte die-Eigenschaft des Elements angezeigt wird <xref:System.Windows.Forms.ListView.Text%2A> , benötigen Sie eine weitere Spalte, als untergeordnete Elemente vorhanden sind. Weitere Informationen zum Hinzufügen von Spalten finden Sie unter Gewusst [wie: Hinzufügen von Spalten zum Windows Forms ListView-Steuer](how-to-add-columns-to-the-windows-forms-listview-control.md)Element.  
  
2. Ruft die-Methode der-Auflistung auf, die <xref:System.Windows.Forms.ListViewItem.ListViewSubItemCollection.Add%2A> von der- <xref:System.Windows.Forms.ListViewItem.SubItems%2A> Eigenschaft eines Elements zurückgegeben wird. Im folgenden Codebeispiel werden der Mitarbeiter Name und die Abteilung für ein Listenelement festgelegt.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#61)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#61)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über das ListView-Steuerelement](listview-control-overview-windows-forms.md)
- [Vorgehensweise: Hinzufügen und Entfernen von Elementen mit dem ListView-Steuerelement in Windows Forms](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
- [Vorgehensweise: Hinzufügen von Spalten zum ListView-Steuerelement in Windows Forms](how-to-add-columns-to-the-windows-forms-listview-control.md)
- [Vorgehensweise: Anzeigen von Symbolen für das ListView-Steuerelement in Windows Forms](how-to-display-icons-for-the-windows-forms-listview-control.md)
- [Vorgehensweise: Hinzufügen von benutzerdefinierten Daten zu einem TreeView- oder ListView-Steuerelement (Windows Forms)](add-custom-information-to-a-treeview-or-listview-control-wf.md)
