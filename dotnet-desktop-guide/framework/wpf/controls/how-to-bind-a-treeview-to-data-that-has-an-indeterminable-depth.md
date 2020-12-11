---
title: 'Gewusst wie: Binden einer TreeView an Daten mit nicht bestimmbarer Tiefe'
ms.date: 03/30/2017
helpviewer_keywords:
- TreeView control [WPF], binding to data of indeterminate depth
ms.assetid: daddcd74-1b0f-4ffd-baeb-ec934c5e0f53
ms.openlocfilehash: 3d9d082b712750d66c63ae0a309afb9cd3c9b4d8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975511"
---
# <a name="how-to-bind-a-treeview-to-data-that-has-an-indeterminable-depth"></a>Gewusst wie: Binden einer TreeView an Daten mit nicht bestimmbarer Tiefe
Es kann vorkommen, dass Sie ein <xref:System.Windows.Controls.TreeView> an eine Datenquelle binden möchten, deren Tiefe nicht bekannt ist.  Dies kann vorkommen, wenn die Daten rekursiv sind, z. b. ein Dateisystem, in dem Ordner Ordner enthalten können, oder die Organisationsstruktur eines Unternehmens, in der Mitarbeiter andere Mitarbeiter als direktberichte haben.  
  
 Die Datenquelle muss über ein hierarchisches Objektmodell verfügen. Eine- `Employee` Klasse kann z. b. eine Auflistung von Employee-Objekten enthalten, bei denen es sich um die direkten Berichte eines Mitarbeiters handelt. Wenn die Daten auf eine nicht hierarchische Weise dargestellt werden, müssen Sie eine hierarchische Darstellung der Daten erstellen.  
  
 Wenn Sie die <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A?displayProperty=nameWithType> -Eigenschaft festlegen und <xref:System.Windows.Controls.ItemsControl> ein <xref:System.Windows.Controls.ItemsControl> für jedes untergeordnete Element generiert, verwendet das unter <xref:System.Windows.Controls.ItemsControl> geordnete Element dasselbe <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A> wie das übergeordnete Element. Wenn Sie z. b. die <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A> -Eigenschaft für ein Daten gebundenes festlegen <xref:System.Windows.Controls.TreeView> , verwendet jedes generierte, das der- <xref:System.Windows.Controls.TreeViewItem> <xref:System.Windows.DataTemplate> <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A> Eigenschaft von zugewiesen wurde <xref:System.Windows.Controls.TreeView> .  
  
 <xref:System.Windows.HierarchicalDataTemplate>Mit können Sie <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> für einen <xref:System.Windows.Controls.TreeViewItem> oder eine beliebige <xref:System.Windows.Controls.HeaderedItemsControl> in der Daten Vorlage angeben. Wenn Sie die- <xref:System.Windows.HierarchicalDataTemplate.ItemsSource%2A?displayProperty=nameWithType> Eigenschaft festlegen, wird dieser Wert verwendet, wenn <xref:System.Windows.HierarchicalDataTemplate> angewendet wird. Mithilfe eines <xref:System.Windows.HierarchicalDataTemplate> können Sie die <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> für jeden in rekursiv festlegen <xref:System.Windows.Controls.TreeViewItem> <xref:System.Windows.Controls.TreeView> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie ein <xref:System.Windows.Controls.TreeView> an hierarchische Daten gebunden wird und mit einem <xref:System.Windows.HierarchicalDataTemplate> die für jede Angabe angegeben wird <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> <xref:System.Windows.Controls.TreeViewItem> .  Der <xref:System.Windows.Controls.TreeView> bindet an XML-Daten, die die Mitarbeiter in einem Unternehmen darstellen.  Jedes- `Employee` Element kann andere- `Employee` Elemente enthalten, um anzugeben, wer an wen berichtet. Da die Daten rekursiv sind, <xref:System.Windows.HierarchicalDataTemplate> kann auf jede Ebene angewendet werden.  
  
 [!code-xaml[TreeViewWithUnknownDepth#1](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewWithUnknownDepth/CS/Window1.xaml#1)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Übersicht über Datenvorlagen](../data/data-templating-overview.md)
