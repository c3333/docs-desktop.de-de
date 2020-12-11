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
# <a name="how-to-manipulate-flow-content-elements-through-the-blocks-property"></a>Gewusst wie: Bearbeiten von fortlaufenden Inhaltselementen mit der Blocks-Eigenschaft
In diesen Beispielen werden einige der gängigeren Vorgänge veranschaulicht, die für fortlaufende Inhaltselemente mithilfe der **Blocks** -Eigenschaft ausgeführt werden können. Diese Eigenschaft wird verwendet, um Elemente hinzuzufügen und zu entfernen <xref:System.Windows.Documents.BlockCollection> . Fortlaufende Inhaltselemente, die eine **Blocks** -Eigenschaft enthalten, umfassen Folgendes:  
  
- <xref:System.Windows.Documents.Figure>  
  
- <xref:System.Windows.Documents.Floater>  
  
- <xref:System.Windows.Documents.ListItem>  
  
- <xref:System.Windows.Documents.Section>  
  
- <xref:System.Windows.Documents.TableCell>  
  
 Diese Beispiele werden als fortlaufendes <xref:System.Windows.Documents.Section> Inhalts Element verwendet. diese Techniken gelten jedoch für alle Elemente, die eine Auflistung von fortlaufenden Inhalts Elementen hosten.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein neuer erstellt, <xref:System.Windows.Documents.Section> und anschließend wird die **Add** -Methode verwendet, um dem **Abschnitts** Inhalt einen neuen Absatz hinzuzufügen.  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksAdd](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksadd)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksAdd](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksadd)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein neues <xref:System.Windows.Documents.Paragraph> -Element erstellt, das am Anfang der eingefügt wird <xref:System.Windows.Documents.Section> .  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksInsert](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksinsert)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksInsert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksinsert)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die Anzahl der Elemente der obersten Ebene abgerufen, die <xref:System.Windows.Documents.Block> in enthalten sind <xref:System.Windows.Documents.Section> .  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksCount](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblockscount)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksCount](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblockscount)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird das letzte- <xref:System.Windows.Documents.Block> Element in gelöscht <xref:System.Windows.Documents.Section> .  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksRemoveLast](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksremovelast)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksRemoveLast](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksremovelast)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird der gesamte Inhalt (- <xref:System.Windows.Documents.Block> Elemente) aus dem gelöscht <xref:System.Windows.Documents.Section> .  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksClear](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksclear)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksClear](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksclear)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Documents.BlockCollection>
- <xref:System.Windows.Documents.InlineCollection>
- <xref:System.Windows.Documents.ListItemCollection>
- [Übersicht über Flussdokumente](flow-document-overview.md)
- [Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
- [Bearbeiten der Spalten einer Tabelle mit der Columns-Eigenschaft](how-to-manipulate-table-columns-through-the-columns-property.md)
- [Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
