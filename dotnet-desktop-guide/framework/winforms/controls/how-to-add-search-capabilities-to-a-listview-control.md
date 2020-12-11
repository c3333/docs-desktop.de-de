---
title: 'Vorgehensweise: Hinzufügen von Suchfunktionen zu einem ListView-Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- lists [Windows Forms], enabling searching
- list views [Windows Forms], enabling searching
- ListView control [Windows Forms], adding search capabilities
- searching [Windows Forms], adding search capabilities to ListView control
ms.assetid: 557782d9-b705-4bab-b496-9938afddac82
ms.openlocfilehash: d5d4dae55fc9f0613ab6535b2fe57e262d0ef141
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976246"
---
# <a name="how-to-add-search-capabilities-to-a-listview-control"></a>Vorgehensweise: Hinzufügen von Suchfunktionen zu einem ListView-Steuerelement
Oft, wenn Sie mit einer großen Liste von Elementen in einem Steuerelement arbeiten <xref:System.Windows.Forms.ListView> , möchten Sie dem Benutzer Suchfunktionen anbieten. Das <xref:System.Windows.Forms.ListView> -Steuerelement bietet diese Funktion auf zwei verschiedene Arten: Text Übereinstimmung und Suche nach Orten.  
  
 Mit der <xref:System.Windows.Forms.ListView.FindItemWithText%2A> -Methode können Sie eine Text Suche für eine <xref:System.Windows.Forms.ListView> in der Listen-oder Detailansicht ausführen, wenn eine Such Zeichenfolge und ein optionaler Start-und endIndex angegeben werden. Im Gegensatz dazu ermöglicht die- <xref:System.Windows.Forms.ListView.FindNearestItem%2A> Methode das Auffinden eines Elements in einem <xref:System.Windows.Forms.ListView> in-Symbol oder einer Kachel Ansicht, wenn ein Satz von x-und y-Koordinaten und eine zu durchsuchende Richtung angegeben wird.  
  
### <a name="to-find-an-item-using-text"></a>So suchen Sie ein Element mithilfe von Text  
  
1. Erstellen <xref:System.Windows.Forms.ListView> Sie ein-Objekt, bei dem die- <xref:System.Windows.Forms.ListView.View%2A> Eigenschaft auf oder festgelegt <xref:System.Windows.Forms.View.Details> <xref:System.Windows.Forms.View.List> ist, und füllen Sie dann <xref:System.Windows.Forms.ListView> mit Elementen.  
  
2. Wenden Sie die- <xref:System.Windows.Forms.ListView.FindItemWithText%2A> Methode an, und übergeben Sie den Text des Elements, das Sie suchen möchten.  
  
3. Im folgenden Codebeispiel wird veranschaulicht, wie ein einfaches erstellt <xref:System.Windows.Forms.ListView> , mit Elementen aufgefüllt und die Texteingabe des Benutzers verwendet wird, um ein Element in der Liste zu suchen.  
  
 [!code-cpp[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/cpp/form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/VB/form1.vb#1)]  
  
### <a name="to-find-an-item-using-x--and-y-coordinates"></a>So suchen Sie ein Element mit x-und y-Koordinaten  
  
1. Erstellen <xref:System.Windows.Forms.ListView> Sie ein-Objekt, bei dem die- <xref:System.Windows.Forms.View> Eigenschaft auf oder festgelegt <xref:System.Windows.Forms.View.SmallIcon> <xref:System.Windows.Forms.View.LargeIcon> ist, und füllen Sie dann <xref:System.Windows.Forms.ListView> mit Elementen.  
  
2. Nennen <xref:System.Windows.Forms.ListView.FindNearestItem%2A> Sie die-Methode, und übergeben Sie die gewünschten x-und y-Koordinaten sowie die Richtung, die Sie durchsuchen möchten.  
  
3. Im folgenden Codebeispiel wird veranschaulicht, wie ein Basis Symbol erstellt <xref:System.Windows.Forms.ListView> , mit Elementen aufgefüllt und das-Ereignis aufgezeichnet wird, <xref:System.Windows.Forms.Control.MouseDown> um das nächste Element in der nach-oben-Richtung zu suchen.  
  
 [!code-cpp[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/cpp/form1.cpp#2)]
 [!code-csharp[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/CS/form1.cs#2)]
 [!code-vb[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/VB/form1.vb#2)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.FindItemWithText%2A>
- <xref:System.Windows.Forms.ListView.FindNearestItem%2A>
- [ListView-Steuerelement](listview-control-windows-forms.md)
- [Übersicht über das ListView-Steuerelement](listview-control-overview-windows-forms.md)
- [Vorgehensweise: Hinzufügen und Entfernen von Elementen mit dem ListView-Steuerelement in Windows Forms](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
