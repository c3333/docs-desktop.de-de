---
title: Übersicht über GridView-Spaltenheaderstile und -Spaltenheadervorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- column headers [WPF], customizing
- ListView controls [WPF], GridView column header styles
- controls [WPF], ListView
- headers [WPF], customizing
- GridView view mode [WPF], customizing column headers
ms.assetid: 74835674-a39e-4ab5-9418-ad7f6ab7b956
ms.openlocfilehash: 83643d8acea706bad439683702e4228d240b97bc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975512"
---
# <a name="gridview-column-header-styles-and-templates-overview"></a>Übersicht über GridView-Spaltenheaderstile und -Spaltenheadervorlagen
In dieser Übersicht wird die Rangfolge der Eigenschaften erläutert, mit denen Sie eine Spaltenüberschrift im <xref:System.Windows.Controls.GridView> Ansichtsmodus eines-Steuer Elements anpassen <xref:System.Windows.Controls.ListView> .  
  
## <a name="customizing-a-column-header-in-a-gridview"></a>Anpassen eines Spalten Headers in einer GridView-Ansicht  
 Die Eigenschaften, die den Inhalt, das Layout und den Stil eines Spalten Headers in einem definieren, <xref:System.Windows.Controls.GridView> werden in vielen verknüpften Klassen gefunden. Einige dieser Eigenschaften verfügen über ähnliche Funktionen wie die gleichen.  
  
 Die Zeilen in der folgenden Tabelle zeigen Gruppen von Eigenschaften an, die dieselbe Funktion ausführen. Sie können diese Eigenschaften verwenden, um die Spaltenüberschriften in einer anzupassen <xref:System.Windows.Controls.GridView> . Die Rangfolge von verknüpften Eigenschaften ist von rechts nach links, wobei die-Eigenschaft in der Spalte mit der äußersten rechten Spalte die höchste Rangfolge hat. Wenn z. b. ein für <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> das-Objekt festgelegt ist und für die zugeordnete <xref:System.Windows.Controls.GridViewColumnHeader> <xref:System.Windows.Controls.GridViewColumn.HeaderTemplateSelector%2A> festgelegt wird <xref:System.Windows.Controls.GridViewColumn> , hat <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> Vorrang. In diesem Szenario <xref:System.Windows.Controls.GridViewColumn.HeaderTemplateSelector%2A> hat keine Auswirkungen.  
  
 **Verwandte Eigenschaften für Spaltenüberschriften in einer GridView**  
  
|||||  
|-|-|-|-|  
|**Klassen**|<xref:System.Windows.Controls.GridView>|<xref:System.Windows.Controls.GridViewColumn>|<xref:System.Windows.Controls.GridViewColumnHeader>|  
|**Kontextmenü Eigenschaften**|<xref:System.Windows.Controls.GridView.ColumnHeaderContextMenu%2A>|Nicht zutreffend|<xref:System.Windows.FrameworkElement.ContextMenu%2A>|  
|**ToolTip**<br /><br /> **Eigenschaften**|<xref:System.Windows.Controls.GridView.ColumnHeaderToolTip%2A>|Nicht zutreffend|<xref:System.Windows.FrameworkElement.ToolTip%2A>|  
|**Header Vorlage**<br /><br /> **Eigenschaften**|<xref:System.Windows.Controls.GridView.ColumnHeaderTemplate%2A><sup>1</sup>/<br /><br /> <xref:System.Windows.Controls.GridView.ColumnHeaderTemplateSelector%2A>|<xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A><sup>1</sup>/<br /><br /> <xref:System.Windows.Controls.GridViewColumn.HeaderTemplateSelector%2A>|<xref:System.Windows.Controls.ContentControl.ContentTemplate%2A><sup>1</sup>/<br /><br /> <xref:System.Windows.Controls.ContentControl.ContentTemplateSelector%2A>|  
|**Formateigenschaften**|<xref:System.Windows.Controls.GridView.ColumnHeaderContainerStyle%2A>|<xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A>|<xref:System.Windows.FrameworkElement.Style%2A>|  
  
 <sup>1</sup> Wenn Sie für **Header Vorlagen Eigenschaften** sowohl die Vorlagen-als auch die Vorlagen Auswahl Eigenschaften festlegen, hat die Vorlagen Eigenschaft Vorrang. Wenn Sie z. b. die <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> -Eigenschaft und die- <xref:System.Windows.Controls.ContentControl.ContentTemplateSelector%2A> Eigenschaft festlegen, hat die- <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> Eigenschaft Vorrang.  
  
## <a name="see-also"></a>Siehe auch

- [Artikel zu Vorgehensweisen](listview-how-to-topics.md)
- [Übersicht über ListView](listview-overview.md)
- [Übersicht über GridView](gridview-overview.md)
