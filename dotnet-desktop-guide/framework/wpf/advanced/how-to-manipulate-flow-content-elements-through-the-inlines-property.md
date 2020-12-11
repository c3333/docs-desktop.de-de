---
title: 'Gewusst wie: Bearbeiten von fortlaufenden Inhaltselementen mit der Inlines-Eigenschaft'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flow content elements [WPF], manipulating through Inlines property
- documents [WPF], manipulating flow Content elements through Inlines property
- Inlines property [WPF], manipulating flow Content elements
- properties [WPF], Inlines [WPF], manipulating flow Content elements
ms.assetid: 510780d2-3da1-4360-8763-7054bda22ea3
ms.openlocfilehash: 92f23fbf44464eb7658f3382f873f3db63f7cb26
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977069"
---
# <a name="how-to-manipulate-flow-content-elements-through-the-inlines-property"></a><span data-ttu-id="73c40-102">Gewusst wie: Bearbeiten von fortlaufenden Inhaltselementen mit der Inlines-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="73c40-102">How to: Manipulate Flow Content Elements through the Inlines Property</span></span>
<span data-ttu-id="73c40-103">In diesen Beispielen werden einige der gängigeren Vorgänge veranschaulicht, die für Inline-fortlaufende Inhaltselemente (und Container solcher Elemente, wie z <xref:System.Windows.Controls.TextBlock> . b.), durch die **Inlines** -Eigenschaft ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="73c40-103">These examples demonstrate some of the more common operations that can be performed on inline flow content elements (and containers of such elements, such as <xref:System.Windows.Controls.TextBlock>) through the **Inlines** property.</span></span> <span data-ttu-id="73c40-104">Diese Eigenschaft wird verwendet, um Elemente hinzuzufügen und zu entfernen <xref:System.Windows.Documents.InlineCollection> .</span><span class="sxs-lookup"><span data-stu-id="73c40-104">This property is used to add and remove items from <xref:System.Windows.Documents.InlineCollection>.</span></span> <span data-ttu-id="73c40-105">Fortlaufende Inhaltselemente, die eine **Inlines** -Eigenschaft enthalten, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="73c40-105">Flow content elements that feature an **Inlines** property include:</span></span>  
  
- <xref:System.Windows.Documents.Bold>  
  
- <xref:System.Windows.Documents.Hyperlink>  
  
- <xref:System.Windows.Documents.Italic>  
  
- <xref:System.Windows.Documents.Paragraph>  
  
- <xref:System.Windows.Documents.Span>  
  
- <xref:System.Windows.Documents.Underline>  
  
 <span data-ttu-id="73c40-106">Diese Beispiele werden als fortlaufendes <xref:System.Windows.Documents.Span> Inhalts Element verwendet, diese Techniken gelten jedoch für alle Elemente oder Steuerelemente, die eine Auflistung hosten <xref:System.Windows.Documents.InlineCollection> .</span><span class="sxs-lookup"><span data-stu-id="73c40-106">These examples happen to use <xref:System.Windows.Documents.Span> as the flow content element, but these techniques are applicable to all elements or controls that host an <xref:System.Windows.Documents.InlineCollection> collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="73c40-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="73c40-107">Example</span></span>  
 <span data-ttu-id="73c40-108">Im folgenden Beispiel wird ein neues <xref:System.Windows.Documents.Span> -Objekt erstellt. Anschließend wird die **Add** -Methode verwendet, um zwei Textläufe als untergeordnete Elemente des hinzuzufügen <xref:System.Windows.Documents.Span> .</span><span class="sxs-lookup"><span data-stu-id="73c40-108">The following example creates a new <xref:System.Windows.Documents.Span> object, and then uses the **Add** method to add two text runs as content children of the <xref:System.Windows.Documents.Span>.</span></span>  
  
 [!code-csharp[SpanSnippets#_SpanInlinesAdd](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesadd)]
 [!code-vb[SpanSnippets#_SpanInlinesAdd](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesadd)]  
  
## <a name="example"></a><span data-ttu-id="73c40-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="73c40-109">Example</span></span>  
 <span data-ttu-id="73c40-110">Im folgenden Beispiel wird ein neues <xref:System.Windows.Documents.Run> -Element erstellt, das am Anfang der eingefügt wird <xref:System.Windows.Documents.Span> .</span><span class="sxs-lookup"><span data-stu-id="73c40-110">The following example creates a new <xref:System.Windows.Documents.Run> element and inserts it at the beginning of the <xref:System.Windows.Documents.Span>.</span></span>  
  
 [!code-csharp[SpanSnippets#_SpanInlinesInsert](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesinsert)]
 [!code-vb[SpanSnippets#_SpanInlinesInsert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesinsert)]  
  
## <a name="example"></a><span data-ttu-id="73c40-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="73c40-111">Example</span></span>  
 <span data-ttu-id="73c40-112">Im folgenden Beispiel wird die Anzahl der Elemente der obersten Ebene abgerufen, die <xref:System.Windows.Documents.Inline> in enthalten sind <xref:System.Windows.Documents.Span> .</span><span class="sxs-lookup"><span data-stu-id="73c40-112">The following example gets the number of top-level <xref:System.Windows.Documents.Inline> elements contained in the <xref:System.Windows.Documents.Span>.</span></span>  
  
 [!code-csharp[SpanSnippets#_SpanInlinesCount](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinescount)]
 [!code-vb[SpanSnippets#_SpanInlinesCount](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinescount)]  
  
## <a name="example"></a><span data-ttu-id="73c40-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="73c40-113">Example</span></span>  
 <span data-ttu-id="73c40-114">Im folgenden Beispiel wird das letzte- <xref:System.Windows.Documents.Inline> Element in gelöscht <xref:System.Windows.Documents.Span> .</span><span class="sxs-lookup"><span data-stu-id="73c40-114">The following example deletes the last <xref:System.Windows.Documents.Inline> element in the <xref:System.Windows.Documents.Span>.</span></span>  
  
 [!code-csharp[SpanSnippets#_SpanInlinesRemoveLast](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesremovelast)]
 [!code-vb[SpanSnippets#_SpanInlinesRemoveLast](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesremovelast)]  
  
## <a name="example"></a><span data-ttu-id="73c40-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="73c40-115">Example</span></span>  
 <span data-ttu-id="73c40-116">Im folgenden Beispiel wird der gesamte Inhalt (- <xref:System.Windows.Documents.Inline> Elemente) aus dem gelöscht <xref:System.Windows.Documents.Span> .</span><span class="sxs-lookup"><span data-stu-id="73c40-116">The following example clears all of the contents (<xref:System.Windows.Documents.Inline> elements) from the <xref:System.Windows.Documents.Span>.</span></span>  
  
 [!code-csharp[SpanSnippets#_SpanInlinesClear](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesclear)]
 [!code-vb[SpanSnippets#_SpanInlinesClear](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesclear)]  
  
## <a name="see-also"></a><span data-ttu-id="73c40-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73c40-117">See also</span></span>

- <xref:System.Windows.Documents.BlockCollection>
- <xref:System.Windows.Documents.InlineCollection>
- <xref:System.Windows.Documents.ListItemCollection>
- [<span data-ttu-id="73c40-118">Übersicht über Flussdokumente</span><span class="sxs-lookup"><span data-stu-id="73c40-118">Flow Document Overview</span></span>](flow-document-overview.md)
- [<span data-ttu-id="73c40-119">Bearbeiten von einem FlowDocument mit der Blocks-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="73c40-119">Manipulate a FlowDocument through the Blocks Property</span></span>](how-to-manipulate-a-flowdocument-through-the-blocks-property.md)
- [<span data-ttu-id="73c40-120">Bearbeiten der Spalten einer Tabelle mit der Columns-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="73c40-120">Manipulate a Table's Columns through the Columns Property</span></span>](how-to-manipulate-table-columns-through-the-columns-property.md)
- [<span data-ttu-id="73c40-121">Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="73c40-121">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
