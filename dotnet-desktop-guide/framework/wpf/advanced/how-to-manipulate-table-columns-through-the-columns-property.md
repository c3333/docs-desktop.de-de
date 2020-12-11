---
title: 'Gewusst wie: Bearbeiten der Spalten einer Tabelle mit der Columns-Eigenschaft'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- documents [WPF], manipulating table columns
- properties [WPF], Columns [WPF], manipulating table columns
- tables [WPF], manipulating columns
- Columns property [WPF]
ms.assetid: 3f8884f4-7e1f-456b-be06-fbd3cf469bf3
ms.openlocfilehash: 18a26c76688ebf668293cb1254404d6d2cf15208
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977757"
---
# <a name="how-to-manipulate-a-tables-columns-through-the-columns-property"></a><span data-ttu-id="529e3-102">Gewusst wie: Bearbeiten der Spalten einer Tabelle mit der Columns-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="529e3-102">How to: Manipulate a Table's Columns through the Columns Property</span></span>
<span data-ttu-id="529e3-103">In diesem Beispiel werden einige der gängigeren Vorgänge veranschaulicht, die über die-Eigenschaft für die Spalten einer Tabelle ausgeführt werden können <xref:System.Windows.Documents.Table.Columns%2A> .</span><span class="sxs-lookup"><span data-stu-id="529e3-103">This example demonstrates some of the more common operations that can be performed on a table's columns through the <xref:System.Windows.Documents.Table.Columns%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="529e3-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="529e3-104">Example</span></span>  
 <span data-ttu-id="529e3-105">Im folgenden Beispiel wird eine neue Tabelle erstellt, und anschließend wird die <xref:System.Windows.Documents.TableColumnCollection.Add%2A> -Methode verwendet, um der-Auflistung der Tabelle Spalten hinzuzufügen <xref:System.Windows.Documents.Table.Columns%2A> .</span><span class="sxs-lookup"><span data-stu-id="529e3-105">The following example creates a new table and then uses the <xref:System.Windows.Documents.TableColumnCollection.Add%2A> method to add columns to the table's <xref:System.Windows.Documents.Table.Columns%2A> collection.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_Columns_Add](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_add)]
 [!code-vb[TableSnippets2#_Table_Columns_Add](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_add)]  
  
## <a name="example"></a><span data-ttu-id="529e3-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="529e3-106">Example</span></span>  
 <span data-ttu-id="529e3-107">Im folgenden Beispiel wird eine neue eingefügt <xref:System.Windows.Documents.TableColumn> .</span><span class="sxs-lookup"><span data-stu-id="529e3-107">The following example inserts a new <xref:System.Windows.Documents.TableColumn>.</span></span>  <span data-ttu-id="529e3-108">Die neue Spalte wird an der Indexposition 0 eingefügt, sodass Sie die neue erste Spalte in der Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="529e3-108">The new column is inserted at index position 0, making it the new first column in the table.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="529e3-109">Die <xref:System.Windows.Documents.TableColumnCollection> -Auflistung verwendet die standardmäßige NULL basierte Indizierung.</span><span class="sxs-lookup"><span data-stu-id="529e3-109">The <xref:System.Windows.Documents.TableColumnCollection> collection uses standard zero-based indexing.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_Columns_Insert](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_insert)]
 [!code-vb[TableSnippets2#_Table_Columns_Insert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_insert)]  
  
## <a name="example"></a><span data-ttu-id="529e3-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="529e3-110">Example</span></span>  
 <span data-ttu-id="529e3-111">Im folgenden Beispiel wird auf einige beliebige Eigenschaften von Spalten in der-Auflistung zugegriffen <xref:System.Windows.Documents.TableColumnCollection> , die auf bestimmte Spalten nach Index verweisen.</span><span class="sxs-lookup"><span data-stu-id="529e3-111">The following example accesses some arbitrary properties on columns in the <xref:System.Windows.Documents.TableColumnCollection> collection, referring to particular columns by index.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_Columns_Manip](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_manip)]
 [!code-vb[TableSnippets2#_Table_Columns_Manip](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_manip)]  
  
## <a name="example"></a><span data-ttu-id="529e3-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="529e3-112">Example</span></span>  
 <span data-ttu-id="529e3-113">Im folgenden Beispiel wird die Anzahl der Spalten abgerufen, die derzeit von der-Tabelle gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="529e3-113">The following example gets the number of columns currently hosted by the table.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_Columns_Count](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_count)]
 [!code-vb[TableSnippets2#_Table_Columns_Count](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_count)]  
  
## <a name="example"></a><span data-ttu-id="529e3-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="529e3-114">Example</span></span>  
 <span data-ttu-id="529e3-115">Im folgenden Beispiel wird eine bestimmte Spalte als Verweis entfernt.</span><span class="sxs-lookup"><span data-stu-id="529e3-115">The following example removes a particular column by reference.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_Columns_DelRef](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_delref)]
 [!code-vb[TableSnippets2#_Table_Columns_DelRef](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_delref)]  
  
## <a name="example"></a><span data-ttu-id="529e3-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="529e3-116">Example</span></span>  
 <span data-ttu-id="529e3-117">Im folgenden Beispiel wird eine bestimmte Spalte nach dem Index entfernt.</span><span class="sxs-lookup"><span data-stu-id="529e3-117">The following example removes a particular column by index.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_Columns_DelIndex](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_delindex)]
 [!code-vb[TableSnippets2#_Table_Columns_DelIndex](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_delindex)]  
  
## <a name="example"></a><span data-ttu-id="529e3-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="529e3-118">Example</span></span>  
 <span data-ttu-id="529e3-119">Im folgenden Beispiel werden alle Spalten aus der Columns-Auflistung der Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="529e3-119">The following example removes all columns from the table's columns collection.</span></span>  
  
 [!code-csharp[TableSnippets2#_Table_Columns_Clear](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_clear)]
 [!code-vb[TableSnippets2#_Table_Columns_Clear](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_clear)]  
  
## <a name="see-also"></a><span data-ttu-id="529e3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="529e3-120">See also</span></span>

- [<span data-ttu-id="529e3-121">Tabellen Übersicht</span><span class="sxs-lookup"><span data-stu-id="529e3-121">Table Overview</span></span>](table-overview.md)
- [<span data-ttu-id="529e3-122">Definieren einer Tabelle mit XAML</span><span class="sxs-lookup"><span data-stu-id="529e3-122">Define a Table with XAML</span></span>](how-to-define-a-table-with-xaml.md)
- [<span data-ttu-id="529e3-123">Programmgesteuertes Erstellen einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="529e3-123">Build a Table Programmatically</span></span>](how-to-build-a-table-programmatically.md)
- [<span data-ttu-id="529e3-124">Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="529e3-124">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
- [<span data-ttu-id="529e3-125">Bearbeiten von einem FlowDocument mit der Blocks-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="529e3-125">Manipulate a FlowDocument through the Blocks Property</span></span>](how-to-manipulate-a-flowdocument-through-the-blocks-property.md)
- [<span data-ttu-id="529e3-126">Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="529e3-126">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
