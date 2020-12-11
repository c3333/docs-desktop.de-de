---
title: 'Gewusst wie: Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- row groups [WPF], manipulating through RowGroups property
- RowGroups property [WPF], manipulating row groups
- documents [WPF], manipulating row groups through RowGroups property
- properties [WPF], RowGroups [WPF], manipulating row groups
ms.assetid: ea61440f-08ae-44ed-b314-5716aaaae3ed
ms.openlocfilehash: 195920af64888bd3671b45befc0fe4cde463ae7b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977756"
---
# <a name="how-to-manipulate-a-tables-row-groups-through-the-rowgroups-property"></a><span data-ttu-id="7b366-102">Gewusst wie: Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b366-102">How to: Manipulate a Table's Row Groups through the RowGroups Property</span></span>
<span data-ttu-id="7b366-103">In diesem Beispiel werden einige der gängigeren Vorgänge veranschaulicht, die über die-Eigenschaft für die Zeilen Gruppen einer Tabelle ausgeführt werden können <xref:System.Windows.Documents.Table.RowGroups%2A> .</span><span class="sxs-lookup"><span data-stu-id="7b366-103">This example demonstrates some of the more common operations that can be performed on a table's row groups through the <xref:System.Windows.Documents.Table.RowGroups%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7b366-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b366-104">Example</span></span>  
 <span data-ttu-id="7b366-105">Im folgenden Beispiel wird eine neue Tabelle erstellt, und anschließend wird die <xref:System.Windows.Documents.TableRowGroupCollection.Add%2A> -Methode verwendet, um der-Auflistung der Tabelle Spalten hinzuzufügen <xref:System.Windows.Documents.Table.RowGroups%2A> .</span><span class="sxs-lookup"><span data-stu-id="7b366-105">The following example creates a new table and then uses the <xref:System.Windows.Documents.TableRowGroupCollection.Add%2A> method to add columns to the table's <xref:System.Windows.Documents.Table.RowGroups%2A> collection.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_RowGroups_Add](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_rowgroups_add)]
 [!code-vb[TableSnippets2#_Table_RowGroups_Add](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_rowgroups_add)]  
  
## <a name="example"></a><span data-ttu-id="7b366-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b366-106">Example</span></span>  
 <span data-ttu-id="7b366-107">Im folgenden Beispiel wird eine neue eingefügt <xref:System.Windows.Documents.TableRowGroup> .</span><span class="sxs-lookup"><span data-stu-id="7b366-107">The following example inserts a new <xref:System.Windows.Documents.TableRowGroup>.</span></span>  <span data-ttu-id="7b366-108">Die neue Spalte wird an der Indexposition 0 eingefügt, sodass Sie die neue erste Zeilen Gruppe in der Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="7b366-108">The new column is inserted at index position 0, making it the new first row group in the table.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7b366-109">Die <xref:System.Windows.Documents.TableRowGroupCollection> -Auflistung verwendet die standardmäßige NULL basierte Indizierung.</span><span class="sxs-lookup"><span data-stu-id="7b366-109">The <xref:System.Windows.Documents.TableRowGroupCollection> collection uses standard zero-based indexing.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_RowGroups_Insert](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_rowgroups_insert)]
 [!code-vb[TableSnippets2#_Table_RowGroups_Insert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_rowgroups_insert)]  
  
## <a name="example"></a><span data-ttu-id="7b366-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b366-110">Example</span></span>  
 <span data-ttu-id="7b366-111">Im folgenden Beispiel werden mehrere Zeilen zu einem bestimmten <xref:System.Windows.Documents.TableRowGroup> (durch Index angegebenen) in der-Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7b366-111">The following example adds several rows to a particular <xref:System.Windows.Documents.TableRowGroup> (specified by index) in the table.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_RowGroups_AddRows](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_rowgroups_addrows)]
 [!code-vb[TableSnippets2#_Table_RowGroups_AddRows](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_rowgroups_addrows)]  
  
## <a name="example"></a><span data-ttu-id="7b366-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b366-112">Example</span></span>  
 <span data-ttu-id="7b366-113">Im folgenden Beispiel wird auf einige beliebige Eigenschaften von Zeilen in der ersten Zeilen Gruppe in der-Tabelle zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="7b366-113">The following example accesses some arbitrary properties on rows in the first row group in the table.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_RowGroups_ManipRows](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_rowgroups_maniprows)]
 [!code-vb[TableSnippets2#_Table_RowGroups_ManipRows](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_rowgroups_maniprows)]  
  
## <a name="example"></a><span data-ttu-id="7b366-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b366-114">Example</span></span>  
 <span data-ttu-id="7b366-115">Im folgenden Beispiel werden mehrere Zellen zu einem bestimmten <xref:System.Windows.Documents.TableRow> (durch Index angegebenen) in der-Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7b366-115">The following example adds several cells to a particular <xref:System.Windows.Documents.TableRow> (specified by index) in the table.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_RowGroups_AddCells](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_rowgroups_addcells)]
 [!code-vb[TableSnippets2#_Table_RowGroups_AddCells](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_rowgroups_addcells)]  
  
## <a name="example"></a><span data-ttu-id="7b366-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b366-116">Example</span></span>  
 <span data-ttu-id="7b366-117">Im folgenden Beispiel wird auf einige beliebige Methoden und Eigenschaften für Zellen in der ersten Zeile in der ersten Zeilen Gruppe zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="7b366-117">The following example access some arbitrary methods and properties on cells in the first row in the first row group.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_RowGroups_ManipCells](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_rowgroups_manipcells)]
 [!code-vb[TableSnippets2#_Table_RowGroups_ManipCells](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_rowgroups_manipcells)]  
  
## <a name="example"></a><span data-ttu-id="7b366-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b366-118">Example</span></span>  
 <span data-ttu-id="7b366-119">Im folgenden Beispiel wird die Anzahl von Elementen zurückgegeben, die <xref:System.Windows.Documents.TableRowGroup> von der-Tabelle gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="7b366-119">The following example returns the number of <xref:System.Windows.Documents.TableRowGroup> elements hosted by the table.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_RowGroups_Count](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_rowgroups_count)]
 [!code-vb[TableSnippets2#_Table_RowGroups_Count](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_rowgroups_count)]  
  
## <a name="example"></a><span data-ttu-id="7b366-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b366-120">Example</span></span>  
 <span data-ttu-id="7b366-121">Im folgenden Beispiel wird eine bestimmte Zeilen Gruppe nach Verweis entfernt.</span><span class="sxs-lookup"><span data-stu-id="7b366-121">The following example removes a particular row group by reference.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_RowGroups_DelRef](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_rowgroups_delref)]
 [!code-vb[TableSnippets2#_Table_RowGroups_DelRef](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_rowgroups_delref)]  
  
## <a name="example"></a><span data-ttu-id="7b366-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b366-122">Example</span></span>  
 <span data-ttu-id="7b366-123">Im folgenden Beispiel wird eine bestimmte Zeilen Gruppe nach Index entfernt.</span><span class="sxs-lookup"><span data-stu-id="7b366-123">The following example removes a particular row group by index.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_RowGroups_DelIndex](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_rowgroups_delindex)]
 [!code-vb[TableSnippets2#_Table_RowGroups_DelIndex](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_rowgroups_delindex)]  
  
## <a name="example"></a><span data-ttu-id="7b366-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7b366-124">Example</span></span>  
 <span data-ttu-id="7b366-125">Im folgenden Beispiel werden alle Zeilen Gruppen aus der Zeilen Gruppen Auflistung der Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="7b366-125">The following example removes all row groups from the table's row groups collection.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_RowGroups_Clear](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_rowgroups_clear)]
 [!code-vb[TableSnippets2#_Table_RowGroups_Clear](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_rowgroups_clear)]  
  
## <a name="see-also"></a><span data-ttu-id="7b366-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b366-126">See also</span></span>

- [<span data-ttu-id="7b366-127">Gewusst wie: Bearbeiten von fortlaufenden Inhalts Elementen mit der Inlines-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b366-127">How-to: Manipulate Flow Content Elements through the Inlines Property</span></span>](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
- [<span data-ttu-id="7b366-128">Bearbeiten von einem FlowDocument mit der Blocks-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b366-128">Manipulate a FlowDocument through the Blocks Property</span></span>](how-to-manipulate-a-flowdocument-through-the-blocks-property.md)
- [<span data-ttu-id="7b366-129">Bearbeiten der Spalten einer Tabelle mit der Columns-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b366-129">Manipulate a Table's Columns through the Columns Property</span></span>](how-to-manipulate-table-columns-through-the-columns-property.md)
