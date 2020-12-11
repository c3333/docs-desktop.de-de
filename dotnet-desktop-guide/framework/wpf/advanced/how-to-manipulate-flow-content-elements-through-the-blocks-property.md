---
title: 'Gewusst wie: Bearbeiten von fortlaufenden Inhaltselementen mit der Blocks-Eigenschaft'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- documents [WPF], manipulating flow content elements through Blocks property
- flow content elements [WPF], manipulating through Blocks property
- properties [WPF], Blocks [WPF], manipulating flow content elements
- Blocks property [WPF], manipulating flow content elements
ms.assetid: aeda4ece-b979-4818-a093-ef938e908751
ms.openlocfilehash: 3ca05590bd1adf7f9c486382a08cb334b4731ac9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974964"
---
# <a name="how-to-manipulate-flow-content-elements-through-the-blocks-property"></a><span data-ttu-id="f7575-102">Gewusst wie: Bearbeiten von fortlaufenden Inhaltselementen mit der Blocks-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7575-102">How to: Manipulate Flow Content Elements through the Blocks Property</span></span>
<span data-ttu-id="f7575-103">In diesen Beispielen werden einige der gängigeren Vorgänge veranschaulicht, die für fortlaufende Inhaltselemente mithilfe der **Blocks** -Eigenschaft ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="f7575-103">These examples demonstrate some of the more common operations that can be performed on flow content elements through the **Blocks** property.</span></span> <span data-ttu-id="f7575-104">Diese Eigenschaft wird verwendet, um Elemente hinzuzufügen und zu entfernen <xref:System.Windows.Documents.BlockCollection> .</span><span class="sxs-lookup"><span data-stu-id="f7575-104">This property is used to add and remove items from <xref:System.Windows.Documents.BlockCollection>.</span></span> <span data-ttu-id="f7575-105">Fortlaufende Inhaltselemente, die eine **Blocks** -Eigenschaft enthalten, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f7575-105">Flow content elements that feature a **Blocks** property include:</span></span>  
  
- <xref:System.Windows.Documents.Figure>  
  
- <xref:System.Windows.Documents.Floater>  
  
- <xref:System.Windows.Documents.ListItem>  
  
- <xref:System.Windows.Documents.Section>  
  
- <xref:System.Windows.Documents.TableCell>  
  
 <span data-ttu-id="f7575-106">Diese Beispiele werden als fortlaufendes <xref:System.Windows.Documents.Section> Inhalts Element verwendet. diese Techniken gelten jedoch für alle Elemente, die eine Auflistung von fortlaufenden Inhalts Elementen hosten.</span><span class="sxs-lookup"><span data-stu-id="f7575-106">These examples happen to use <xref:System.Windows.Documents.Section> as the flow content element, but these techniques are applicable to all elements that host a flow content element collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f7575-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7575-107">Example</span></span>  
 <span data-ttu-id="f7575-108">Im folgenden Beispiel wird ein neuer erstellt, <xref:System.Windows.Documents.Section> und anschließend wird die **Add** -Methode verwendet, um dem **Abschnitts** Inhalt einen neuen Absatz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f7575-108">The following example creates a new <xref:System.Windows.Documents.Section> and then uses the **Add** method to add a new Paragraph to the **Section** contents.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksAdd](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksadd)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksAdd](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksadd)]  
  
## <a name="example"></a><span data-ttu-id="f7575-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7575-109">Example</span></span>  
 <span data-ttu-id="f7575-110">Im folgenden Beispiel wird ein neues <xref:System.Windows.Documents.Paragraph> -Element erstellt, das am Anfang der eingefügt wird <xref:System.Windows.Documents.Section> .</span><span class="sxs-lookup"><span data-stu-id="f7575-110">The following example creates a new <xref:System.Windows.Documents.Paragraph> element and inserts it at the beginning of the <xref:System.Windows.Documents.Section>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksInsert](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksinsert)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksInsert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksinsert)]  
  
## <a name="example"></a><span data-ttu-id="f7575-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7575-111">Example</span></span>  
 <span data-ttu-id="f7575-112">Im folgenden Beispiel wird die Anzahl der Elemente der obersten Ebene abgerufen, die <xref:System.Windows.Documents.Block> in enthalten sind <xref:System.Windows.Documents.Section> .</span><span class="sxs-lookup"><span data-stu-id="f7575-112">The following example gets the number of top-level <xref:System.Windows.Documents.Block> elements contained in the <xref:System.Windows.Documents.Section>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksCount](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblockscount)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksCount](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblockscount)]  
  
## <a name="example"></a><span data-ttu-id="f7575-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7575-113">Example</span></span>  
 <span data-ttu-id="f7575-114">Im folgenden Beispiel wird das letzte- <xref:System.Windows.Documents.Block> Element in gelöscht <xref:System.Windows.Documents.Section> .</span><span class="sxs-lookup"><span data-stu-id="f7575-114">The following example deletes the last <xref:System.Windows.Documents.Block> element in the <xref:System.Windows.Documents.Section>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksRemoveLast](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksremovelast)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksRemoveLast](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksremovelast)]  
  
## <a name="example"></a><span data-ttu-id="f7575-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7575-115">Example</span></span>  
 <span data-ttu-id="f7575-116">Im folgenden Beispiel wird der gesamte Inhalt (- <xref:System.Windows.Documents.Block> Elemente) aus dem gelöscht <xref:System.Windows.Documents.Section> .</span><span class="sxs-lookup"><span data-stu-id="f7575-116">The following example clears all of the contents (<xref:System.Windows.Documents.Block> elements) from the <xref:System.Windows.Documents.Section>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksClear](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksclear)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksClear](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksclear)]  
  
## <a name="see-also"></a><span data-ttu-id="f7575-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7575-117">See also</span></span>

- <xref:System.Windows.Documents.BlockCollection>
- <xref:System.Windows.Documents.InlineCollection>
- <xref:System.Windows.Documents.ListItemCollection>
- [<span data-ttu-id="f7575-118">Übersicht über Flussdokumente</span><span class="sxs-lookup"><span data-stu-id="f7575-118">Flow Document Overview</span></span>](flow-document-overview.md)
- [<span data-ttu-id="f7575-119">Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7575-119">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
- [<span data-ttu-id="f7575-120">Bearbeiten der Spalten einer Tabelle mit der Columns-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7575-120">Manipulate a Table's Columns through the Columns Property</span></span>](how-to-manipulate-table-columns-through-the-columns-property.md)
- [<span data-ttu-id="f7575-121">Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7575-121">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
