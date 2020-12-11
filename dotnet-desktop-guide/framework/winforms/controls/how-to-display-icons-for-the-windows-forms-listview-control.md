---
title: Anzeigen von Symbolen für das ListView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], displaying icons
- icons [Windows Forms], displaying for ListView controls
- lists [Windows Forms], displaying icons
- ImageList component [Windows Forms], with ListView control
- list views [Windows Forms], displaying icons
ms.assetid: 9d577542-8595-429b-99e5-078770ec9d35
ms.openlocfilehash: 5fc54c448dae95cab50cdafa8403769fb421dffa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975660"
---
# <a name="how-to-display-icons-for-the-windows-forms-listview-control"></a>Vorgehensweise: Anzeigen von Symbolen für das ListView-Steuerelement in Windows Forms
Das Windows Forms <xref:System.Windows.Forms.ListView> Steuerelement kann Symbole aus drei Bildlisten anzeigen. In den Ansichten "List", "Details" und "SmallIcon" werden Bilder aus der in der-Eigenschaft angegebenen Bildliste angezeigt <xref:System.Windows.Forms.ListView.SmallImageList%2A> . In der LargeIcon-Ansicht werden Bilder aus der Bildliste angezeigt, die in der-Eigenschaft angegeben ist <xref:System.Windows.Forms.ListView.LargeImageList%2A> . In einer Listenansicht kann auch ein zusätzlicher Satz von Symbolen angezeigt werden, die in der- <xref:System.Windows.Forms.ListView.StateImageList%2A> Eigenschaft neben den großen oder kleinen Symbolen festgelegt sind. Weitere Informationen zu Bildlisten finden Sie unter [ImageList-Komponente](imagelist-component-windows-forms.md) und Gewusst [wie: Hinzufügen oder Entfernen von Bildern mit der Windows Forms ImageList-Komponente](how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).  
  
### <a name="to-display-images-in-a-list-view"></a>So zeigen Sie Bilder in einer Listenansicht an  
  
1. Legen Sie die entsprechende Eigenschaft – <xref:System.Windows.Forms.ListView.SmallImageList%2A> , <xref:System.Windows.Forms.ListView.LargeImageList%2A> oder <xref:System.Windows.Forms.ListView.StateImageList%2A> – auf die vorhandene Komponente fest, die <xref:System.Windows.Forms.ImageList> Sie verwenden möchten.  
  
     Diese Eigenschaften können im Designer mit dem Eigenschaftenfenster oder im Code festgelegt werden.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#41)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#41)]  
  
2. Legen Sie die- <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> Eigenschaft oder die- <xref:System.Windows.Forms.ListViewItem.StateImageIndex%2A> Eigenschaft für jedes Listenelement mit einem zugeordneten Symbol fest.  
  
     Diese Eigenschaften können im Code oder im **ListViewItem-Auflistungs-Editor** festgelegt werden. Um den **ListViewItem-Auflistungs-Editor** zu öffnen, klicken Sie auf die Schaltfläche mit den Auslassungs Zeichen ( ![ ...) im Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ) neben der- <xref:System.Windows.Forms.ListView.Items%2A> Eigenschaft im **Eigenschaften** Fenster.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#42)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#42)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über das ListView-Steuerelement](listview-control-overview-windows-forms.md)
- [Vorgehensweise: Hinzufügen und Entfernen von Elementen mit dem ListView-Steuerelement in Windows Forms](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
- [Vorgehensweise: Hinzufügen von Spalten zum ListView-Steuerelement in Windows Forms](how-to-add-columns-to-the-windows-forms-listview-control.md)
- [Vorgehensweise: Hinzufügen von benutzerdefinierten Daten zu einem TreeView- oder ListView-Steuerelement (Windows Forms)](add-custom-information-to-a-treeview-or-listview-control-wf.md)
- [ImageList-Komponente](imagelist-component-windows-forms.md)
