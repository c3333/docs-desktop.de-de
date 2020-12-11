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
# <a name="how-to-manipulate-flow-content-elements-through-the-inlines-property"></a>Gewusst wie: Bearbeiten von fortlaufenden Inhaltselementen mit der Inlines-Eigenschaft
In diesen Beispielen werden einige der gängigeren Vorgänge veranschaulicht, die für Inline-fortlaufende Inhaltselemente (und Container solcher Elemente, wie z <xref:System.Windows.Controls.TextBlock> . b.), durch die **Inlines** -Eigenschaft ausgeführt werden können. Diese Eigenschaft wird verwendet, um Elemente hinzuzufügen und zu entfernen <xref:System.Windows.Documents.InlineCollection> . Fortlaufende Inhaltselemente, die eine **Inlines** -Eigenschaft enthalten, umfassen Folgendes:  
  
- <xref:System.Windows.Documents.Bold>  
  
- <xref:System.Windows.Documents.Hyperlink>  
  
- <xref:System.Windows.Documents.Italic>  
  
- <xref:System.Windows.Documents.Paragraph>  
  
- <xref:System.Windows.Documents.Span>  
  
- <xref:System.Windows.Documents.Underline>  
  
 Diese Beispiele werden als fortlaufendes <xref:System.Windows.Documents.Span> Inhalts Element verwendet, diese Techniken gelten jedoch für alle Elemente oder Steuerelemente, die eine Auflistung hosten <xref:System.Windows.Documents.InlineCollection> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein neues <xref:System.Windows.Documents.Span> -Objekt erstellt. Anschließend wird die **Add** -Methode verwendet, um zwei Textläufe als untergeordnete Elemente des hinzuzufügen <xref:System.Windows.Documents.Span> .  
  
 [!code-csharp[SpanSnippets#_SpanInlinesAdd](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesadd)]
 [!code-vb[SpanSnippets#_SpanInlinesAdd](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesadd)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein neues <xref:System.Windows.Documents.Run> -Element erstellt, das am Anfang der eingefügt wird <xref:System.Windows.Documents.Span> .  
  
 [!code-csharp[SpanSnippets#_SpanInlinesInsert](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesinsert)]
 [!code-vb[SpanSnippets#_SpanInlinesInsert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesinsert)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die Anzahl der Elemente der obersten Ebene abgerufen, die <xref:System.Windows.Documents.Inline> in enthalten sind <xref:System.Windows.Documents.Span> .  
  
 [!code-csharp[SpanSnippets#_SpanInlinesCount](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinescount)]
 [!code-vb[SpanSnippets#_SpanInlinesCount](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinescount)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird das letzte- <xref:System.Windows.Documents.Inline> Element in gelöscht <xref:System.Windows.Documents.Span> .  
  
 [!code-csharp[SpanSnippets#_SpanInlinesRemoveLast](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesremovelast)]
 [!code-vb[SpanSnippets#_SpanInlinesRemoveLast](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesremovelast)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird der gesamte Inhalt (- <xref:System.Windows.Documents.Inline> Elemente) aus dem gelöscht <xref:System.Windows.Documents.Span> .  
  
 [!code-csharp[SpanSnippets#_SpanInlinesClear](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesclear)]
 [!code-vb[SpanSnippets#_SpanInlinesClear](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesclear)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Documents.BlockCollection>
- <xref:System.Windows.Documents.InlineCollection>
- <xref:System.Windows.Documents.ListItemCollection>
- [Übersicht über Flussdokumente](flow-document-overview.md)
- [Bearbeiten von einem FlowDocument mit der Blocks-Eigenschaft](how-to-manipulate-a-flowdocument-through-the-blocks-property.md)
- [Bearbeiten der Spalten einer Tabelle mit der Columns-Eigenschaft](how-to-manipulate-table-columns-through-the-columns-property.md)
- [Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
