---
title: 'Gewusst wie: Erstellen einfacher und komplexer TreeViews'
ms.date: 03/30/2017
helpviewer_keywords:
- TreeView control [WPF], creating
- Control class [WPF], TreeView [WPF], creating
ms.assetid: 1defbb78-b8e7-4c0e-b650-576453ac828d
ms.openlocfilehash: 7edb4933ebcc0f0d2cb02754238c2342ee9dd4a2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977816"
---
# <a name="how-to-create-simple-or-complex-treeviews"></a><span data-ttu-id="e14ba-102">Gewusst wie: Erstellen einfacher und komplexer TreeViews</span><span class="sxs-lookup"><span data-stu-id="e14ba-102">How to: Create Simple or Complex TreeViews</span></span>
<span data-ttu-id="e14ba-103">Dieses Beispiel zeigt, wie einfache oder komplexe Steuer <xref:System.Windows.Controls.TreeView> Elemente erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e14ba-103">This example shows how to create simple or complex <xref:System.Windows.Controls.TreeView> controls.</span></span>  
  
 <span data-ttu-id="e14ba-104">Ein <xref:System.Windows.Controls.TreeView> besteht aus einer Hierarchie von Steuer <xref:System.Windows.Controls.TreeViewItem> Elementen, die einfache Text Zeichenfolgen und außerdem komplexere Inhalte enthalten können, z. b. Steuer <xref:System.Windows.Controls.Button> Elemente oder ein <xref:System.Windows.Controls.StackPanel> mit eingebettetem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="e14ba-104">A <xref:System.Windows.Controls.TreeView> consists of a hierarchy of <xref:System.Windows.Controls.TreeViewItem> controls, which can contain simple text strings and also more complex content, such as <xref:System.Windows.Controls.Button> controls or a <xref:System.Windows.Controls.StackPanel> with embedded content.</span></span> <span data-ttu-id="e14ba-105">Sie können den Inhalt explizit definieren, <xref:System.Windows.Controls.TreeView> oder eine Datenquelle kann den Inhalt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e14ba-105">You can explicitly define the <xref:System.Windows.Controls.TreeView> content or a data source can provide the content.</span></span> <span data-ttu-id="e14ba-106">Dieses Thema enthält Beispiele für diese Konzepte.</span><span class="sxs-lookup"><span data-stu-id="e14ba-106">This topic provides examples of these concepts.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e14ba-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e14ba-107">Example</span></span>  
 <span data-ttu-id="e14ba-108">Die- <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> Eigenschaft des <xref:System.Windows.Controls.TreeViewItem> enthält den Inhalt, der von <xref:System.Windows.Controls.TreeView> für dieses Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e14ba-108">The <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> property of the <xref:System.Windows.Controls.TreeViewItem> contains the content that the <xref:System.Windows.Controls.TreeView> displays for that item.</span></span> <span data-ttu-id="e14ba-109">Ein <xref:System.Windows.Controls.TreeViewItem> kann auch über Steuerelemente als untergeordnete Elemente verfügen, <xref:System.Windows.Controls.TreeViewItem> und Sie können diese untergeordneten Elemente mithilfe der- <xref:System.Windows.Controls.ItemsControl.Items%2A> Eigenschaft definieren.</span><span class="sxs-lookup"><span data-stu-id="e14ba-109">A <xref:System.Windows.Controls.TreeViewItem> can also have <xref:System.Windows.Controls.TreeViewItem> controls as its child elements and you can define these child elements by using the <xref:System.Windows.Controls.ItemsControl.Items%2A> property.</span></span>  
  
 <span data-ttu-id="e14ba-110">Im folgenden Beispiel wird gezeigt, wie Sie Inhalte explizit definieren, <xref:System.Windows.Controls.TreeViewItem> indem Sie die- <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> Eigenschaft auf eine Text Zeichenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="e14ba-110">The following example shows how to explicitly define <xref:System.Windows.Controls.TreeViewItem> content by setting the <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> property to a text string.</span></span>  
  
 [!code-xaml[TreeViewSimple#1](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#1)]  
  
 <span data-ttu-id="e14ba-111">Im folgenden Beispiel wird gezeigt, wie untergeordnete Elemente einer definiert <xref:System.Windows.Controls.TreeViewItem> werden, indem definiert <xref:System.Windows.Controls.ItemsControl.Items%2A> wird <xref:System.Windows.Controls.Button></span><span class="sxs-lookup"><span data-stu-id="e14ba-111">The following example show how to define child elements of a <xref:System.Windows.Controls.TreeViewItem> by defining <xref:System.Windows.Controls.ItemsControl.Items%2A> that are <xref:System.Windows.Controls.Button> controls.</span></span>  
  
 [!code-xaml[TreeViewSimple#3](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#3)]  
  
 <span data-ttu-id="e14ba-112">Im folgenden Beispiel wird gezeigt, wie ein erstellt wird, <xref:System.Windows.Controls.TreeView> in dem ein <xref:System.Windows.Data.XmlDataProvider> <xref:System.Windows.Controls.TreeViewItem> -Inhalt bereitstellt und eine <xref:System.Windows.HierarchicalDataTemplate> die Darstellung des Inhalts definiert.</span><span class="sxs-lookup"><span data-stu-id="e14ba-112">The following example shows how to create a <xref:System.Windows.Controls.TreeView> where an <xref:System.Windows.Data.XmlDataProvider> provides <xref:System.Windows.Controls.TreeViewItem> content and a <xref:System.Windows.HierarchicalDataTemplate> defines the appearance of the content.</span></span>  
  
 [!code-xaml[TreeViewSimple#6](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#6)]  
  
 [!code-xaml[TreeViewSimple#7](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#7)]  
  
 [!code-xaml[TreeViewSimple#5](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#5)]  
  
 <span data-ttu-id="e14ba-113">Im folgenden Beispiel wird gezeigt, wie ein erstellt wird, <xref:System.Windows.Controls.TreeView> in dem der <xref:System.Windows.Controls.TreeViewItem> Inhalt Steuer <xref:System.Windows.Controls.DockPanel> Elemente enthält, die über eingebetteten Inhalt verfügen.</span><span class="sxs-lookup"><span data-stu-id="e14ba-113">The following example shows how to create a <xref:System.Windows.Controls.TreeView> where the <xref:System.Windows.Controls.TreeViewItem> content contains <xref:System.Windows.Controls.DockPanel> controls that have embedded content.</span></span>  
  
 [!code-xaml[TreeViewSimple#9](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#9)]  
  
## <a name="see-also"></a><span data-ttu-id="e14ba-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e14ba-114">See also</span></span>

- <xref:System.Windows.Controls.TreeView>
- <xref:System.Windows.Controls.TreeViewItem>
- [<span data-ttu-id="e14ba-115">Übersicht über TreeView</span><span class="sxs-lookup"><span data-stu-id="e14ba-115">TreeView Overview</span></span>](treeview-overview.md)
- [<span data-ttu-id="e14ba-116">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="e14ba-116">How-to Topics</span></span>](treeview-how-to-topics.md)
