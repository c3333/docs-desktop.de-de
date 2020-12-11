---
title: 'Gewusst wie: Erstellen von ListViewItems mit einem Kontrollkästchen'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], ListView
- controls [WPF], CheckBox
- ListView controls [WPF], CheckBox controls
- CheckBox control [WPF], ListView control
ms.assetid: f6d66c7f-906c-4f65-a55a-0ede9d00e26a
ms.openlocfilehash: b09d5ad11b0961febf524cec1e19cb1e59832e44
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977819"
---
# <a name="how-to-create-listviewitems-with-a-checkbox"></a>Gewusst wie: Erstellen von ListViewItems mit einem Kontrollkästchen
In diesem Beispiel wird gezeigt, wie eine Spalte von <xref:System.Windows.Controls.CheckBox> Steuerelementen in einem-Steuerelement angezeigt wird <xref:System.Windows.Controls.ListView> , das einen verwendet <xref:System.Windows.Controls.GridView> .  
  
## <a name="example"></a>Beispiel  
 Um eine Spalte zu erstellen, die Steuer <xref:System.Windows.Controls.CheckBox> Elemente in einem enthält <xref:System.Windows.Controls.ListView> , erstellen Sie eine <xref:System.Windows.DataTemplate> , die eine enthält <xref:System.Windows.Controls.CheckBox> . Legen Sie dann die <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> eines <xref:System.Windows.Controls.GridViewColumn> auf die fest <xref:System.Windows.DataTemplate> .  
  
 Das folgende Beispiel zeigt eine <xref:System.Windows.DataTemplate> , die eine enthält <xref:System.Windows.Controls.CheckBox> . Im Beispiel wird die- <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> Eigenschaft des- <xref:System.Windows.Controls.CheckBox> Objekts an den- <xref:System.Windows.Controls.ListBoxItem.IsSelected%2A> Eigenschafts Wert des-Objekts gebunden, das <xref:System.Windows.Controls.ListViewItem> es enthält. Wenn die, die <xref:System.Windows.Controls.ListViewItem> das enthält <xref:System.Windows.Controls.CheckBox> , ausgewählt ist, wird daher der <xref:System.Windows.Controls.CheckBox> aktiviert.  
  
 [!code-xaml[ListViewChkBox#CheckBoxDataTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#checkboxdatatemplate)]  
  
 Im folgenden Beispiel wird gezeigt, wie eine Spalte von-Steuerelementen erstellt wird <xref:System.Windows.Controls.CheckBox> . Um die Spalte zu erstellen, wird im Beispiel die- <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> Eigenschaft von auf festgelegt <xref:System.Windows.Controls.GridViewColumn> <xref:System.Windows.DataTemplate> .  
  
 [!code-xaml[ListViewChkBox#GridViewColumnCheckBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#gridviewcolumncheckbox)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Control>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Übersicht über ListView](listview-overview.md)
- [Artikel zu Vorgehensweisen](listview-how-to-topics.md)
- [Übersicht über GridView](gridview-overview.md)
