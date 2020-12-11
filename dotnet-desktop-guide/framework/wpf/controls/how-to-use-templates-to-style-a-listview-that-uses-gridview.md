---
title: 'Gewusst wie: Formatieren eines ListView-Steuerelements mit einem GridView mithilfe von Vorlagen'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 94bf964b-96c8-4bdf-a0c3-f5271b7cb565
ms.openlocfilehash: 1caa652c4a2a3a7d0a8d40fe703df7a3e8038c9b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974659"
---
# <a name="how-to-use-templates-to-style-a-listview-that-uses-gridview"></a>Gewusst wie: Formatieren eines ListView-Steuerelements mit einem GridView mithilfe von Vorlagen
Dieses Beispiel zeigt, wie das <xref:System.Windows.DataTemplate> -Objekt und das-Objekt verwendet werden, <xref:System.Windows.Style> um die Darstellung eines Steuer Elements anzugeben <xref:System.Windows.Controls.ListView> , das einen <xref:System.Windows.Controls.GridView> Ansichtsmodus verwendet.  
  
## <a name="example"></a>Beispiel  
 In den folgenden Beispielen werden <xref:System.Windows.Style> -Objekte und-Objekte gezeigt, die die Darstellung eines <xref:System.Windows.DataTemplate> Spalten Headers für einen anpassen <xref:System.Windows.Controls.GridViewColumn> .  
  
 [!code-xaml[ListViewTemplate#GridViewHeaderStyle](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewheaderstyle)]  
  
 [!code-xaml[ListViewTemplate#GridViewHeaderTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewheadertemplate)]  
  
 Im folgenden Beispiel wird gezeigt, wie diese <xref:System.Windows.Style> -und- <xref:System.Windows.DataTemplate> Objekte zum Festlegen der <xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A> -Eigenschaft und der-Eigenschaft eines verwendet werden <xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A> <xref:System.Windows.Controls.GridViewColumn> . Die- <xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A> Eigenschaft definiert den Inhalt der Spalten Zellen.  
  
 [!code-xaml[ListViewTemplate#GridViewColumnTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewcolumntemplate)]  
  
 <xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A>Und <xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A> sind nur zwei verschiedene Eigenschaften, die Sie verwenden können, um die Darstellung der Spalten Kopfzeile für ein-Steuerelement anzupassen <xref:System.Windows.Controls.GridView> . Weitere Informationen finden Sie unter [Übersicht über GridView-Spaltenheaderstile und -Spaltenheadervorlagen](gridview-column-header-styles-and-templates-overview.md).  
  
 Im folgenden Beispiel wird gezeigt, wie ein definiert wird <xref:System.Windows.DataTemplate> , das die Darstellung der Zellen in einem anpasst <xref:System.Windows.Controls.GridViewColumn> .  
  
 [!code-xaml[ListViewTemplate#GridViewCellTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewcelltemplate)]  
  
 Im folgenden Beispiel wird gezeigt, wie diese verwendet wird <xref:System.Windows.DataTemplate> , um den Inhalt einer Zelle zu definieren <xref:System.Windows.Controls.GridViewColumn> . Diese Vorlage wird anstelle der Eigenschaft verwendet <xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A> , die im vorherigen Beispiel dargestellt wurde <xref:System.Windows.Controls.GridViewColumn> .  
  
 [!code-xaml[ListViewTemplate#CellTemplateProperty](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#celltemplateproperty)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Übersicht über GridView](gridview-overview.md)
- [Artikel zu Vorgehensweisen](listview-how-to-topics.md)
- [Übersicht über ListView](listview-overview.md)
