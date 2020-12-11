---
title: Übersicht über das TextElement-Inhaltsmodell
ms.date: 03/30/2017
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- documents [WPF], flow documents
- TextElement content model [WPF]
- flow content elements [WPF], TextElement content model
ms.assetid: d0a7791c-b090-438c-812f-b9d009d83ee9
ms.openlocfilehash: b4bf5bf1810adec4eb71ae79e747d507952c0734
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977475"
---
# <a name="textelement-content-model-overview"></a>Übersicht über das TextElement-Inhaltsmodell
In dieser Übersicht über das Inhalts Modell werden die unterstützten Inhalte für eine beschrieben <xref:System.Windows.Documents.TextElement> . Die- <xref:System.Windows.Documents.Paragraph> Klasse ist ein Typ von <xref:System.Windows.Documents.TextElement> . Ein Inhaltsmodell beschreibt, welche Objekte/Elemente in anderen enthalten sein können. Diese Übersicht fasst das Inhalts Modell zusammen, das für von abgeleitete Objekte verwendet wird <xref:System.Windows.Documents.TextElement> . Weitere Informationen finden Sie unter [Übersicht über Fluss Dokumente](flow-document-overview.md).  

<a name="text_element_classes"></a>
## <a name="content-model-diagram"></a>Inhaltsmodelldiagramm  
 Im folgenden Diagramm ist das Inhalts Modell für Klassen zusammengefasst, die von abgeleitet sind, sowie die Art <xref:System.Windows.Documents.TextElement> und Weise, wie andere nicht- `TextElement` Klassen in dieses Modell passen.  
  
 ![Diagramm: Flussinhalt-Kapselungsschema](./media/flow-content-schema.png "Flow_Content_Schema")  
  
 Wie aus dem vorangehenden Diagramm ersichtlich ist, werden die untergeordneten Elemente, die für ein Element zulässig sind, nicht notwendigerweise bestimmt, ob eine Klasse von der-Klasse oder einer-Klasse abgeleitet ist <xref:System.Windows.Documents.Block> <xref:System.Windows.Documents.Inline> . Beispielsweise kann eine <xref:System.Windows.Documents.Span> (eine von <xref:System.Windows.Documents.Inline> abgeleitete Klasse) nur <xref:System.Windows.Documents.Inline> untergeordnete Elemente aufweisen, aber eine <xref:System.Windows.Documents.Figure> (auch eine von <xref:System.Windows.Documents.Inline> abgeleitete Klasse) kann nur untergeordnete <xref:System.Windows.Documents.Block> Elemente aufweisen. Aus diesem Grund ist ein Diagramm nützlich, um schnell zu bestimmen, welches Element in einem anderen eingeschlossen sein kann. Als Beispiel verwenden wir das Diagramm, um zu bestimmen, wie der fortlaufende Inhalt eines erstellt wird <xref:System.Windows.Controls.RichTextBox> .  
  
1. <xref:System.Windows.Controls.RichTextBox>Muss einen enthalten <xref:System.Windows.Documents.FlowDocument> , der wiederum ein von <xref:System.Windows.Documents.Block> abgeleitetes Objekt enthalten muss. Im Folgenden wird das entsprechende Segment aus dem vorherigen Diagramm dargestellt.  
  
     ![Diagramm: RichTextBox-Kapselungsregeln](./media/flow-ovw-schemawalkthrough1.png "Flow_Ovw_SchemaWalkThrough1")  
  
     Bis jetzt könnte das Markup wie folgt aussehen.  
  
     [!code-xaml[FlowOvwSnippets_snip#SchemaWalkThrough1](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowOvwSnippets_snip/CS/MiscSnippets.xaml#schemawalkthrough1)]  
  
2. Entsprechend dem Diagramm stehen mehrere <xref:System.Windows.Documents.Block> Elemente zur Auswahl, z. a.,,, <xref:System.Windows.Documents.Paragraph> <xref:System.Windows.Documents.Section> <xref:System.Windows.Documents.Table> <xref:System.Windows.Documents.List> und <xref:System.Windows.Documents.BlockUIContainer> (siehe von Block abgeleitete Klassen im vorangehenden Diagramm). Nehmen wir an, wir möchten ein <xref:System.Windows.Documents.Table> . Gemäß dem vorangehenden Diagramm enthält eine eine <xref:System.Windows.Documents.Table> <xref:System.Windows.Documents.TableRowGroup> enthaltende <xref:System.Windows.Documents.TableRow> Elemente, die Elemente enthalten, <xref:System.Windows.Documents.TableCell> die ein von <xref:System.Windows.Documents.Block> abgeleitetes Objekt enthalten. Im folgenden finden Sie das entsprechende Segment, das <xref:System.Windows.Documents.Table> aus dem vorherigen Diagramm entnommen wurde.  
  
     ![Diagramm: übergeordnetes&#47;untergeordnetes Schema für Tabelle](./media/flow-ovw-schemawalkthrough2.png "Flow_Ovw_SchemaWalkThrough2")  
  
     Im Folgenden wird das entsprechende Markup dargestellt.  
  
     [!code-xaml[FlowOvwSnippets_snip#SchemaWalkThrough2](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowOvwSnippets_snip/CS/MiscSnippets.xaml#schemawalkthrough2)]  
  
3. Ein oder mehrere- <xref:System.Windows.Documents.Block> Elemente sind unterhalb von erforderlich <xref:System.Windows.Documents.TableCell> . Um es einfach zu gestalten, fügen wir Text in die Zelle ein. Dies ist mit einem- <xref:System.Windows.Documents.Paragraph> <xref:System.Windows.Documents.Run> Element möglich. Im folgenden finden Sie die entsprechenden Segmente aus dem Diagramm, die zeigen, dass ein <xref:System.Windows.Documents.Paragraph> <xref:System.Windows.Documents.Inline> -Element akzeptiert und ein <xref:System.Windows.Documents.Run> (ein- <xref:System.Windows.Documents.Inline> Element) nur nur-Text annehmen kann.  
  
     ![Diagramm: übergeordnetes&#47;untergeordnetes Schema für Absatz](./media/flow-ovw-schemawalkthrough3.png "Flow_Ovw_SchemaWalkThrough3")  
  
     ![Diagramm: übergeordnetes&#47;untergeordnetes Schema für die Testlauf](./media/flow-ovw-schemawalkthrough4.png "Flow_Ovw_SchemaWalkThrough4")  
  
 Nachstehend finden Sie das gesamte Beispiel im Markup.  
  
 [!code-xaml[FlowOvwSnippets_snip#SchemaExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowOvwSnippets_snip/CS/SchemaExample.xaml#schemaexamplewholepage)]  
  
<a name="Using_the_Content_Property"></a>
## <a name="working-with-textelement-content-programmatically"></a>Programmgesteuertes Arbeiten mit TextElement-Inhalt  
 Der Inhalt eines <xref:System.Windows.Documents.TextElement> wird durch Auflistungen erstellt, sodass der Inhalt von Objekten Programm gesteuert <xref:System.Windows.Documents.TextElement> bearbeitet wird, indem er mit diesen Auflistungen arbeitet. Es gibt drei verschiedene Auflistungen, die von <xref:System.Windows.Documents.TextElement> abgeleiteten Klassen verwendet werden:  
  
- <xref:System.Windows.Documents.InlineCollection>: Stellt eine Auflistung von- <xref:System.Windows.Documents.Inline> Elementen dar. <xref:System.Windows.Documents.InlineCollection> definiert den zulässigen untergeordneten Inhalt der Elemente <xref:System.Windows.Documents.Paragraph>, <xref:System.Windows.Documents.Span> und <xref:System.Windows.Controls.TextBlock>.  
  
- <xref:System.Windows.Documents.BlockCollection>: Stellt eine Auflistung von- <xref:System.Windows.Documents.Block> Elementen dar. <xref:System.Windows.Documents.BlockCollection> definiert den zulässigen untergeordneten Inhalt der Elemente <xref:System.Windows.Documents.FlowDocument>, <xref:System.Windows.Documents.Section>, <xref:System.Windows.Documents.ListItem>, <xref:System.Windows.Documents.TableCell>, <xref:System.Windows.Documents.Floater> und <xref:System.Windows.Documents.Figure>.  
  
- <xref:System.Windows.Documents.ListItemCollection>: Ein fortlaufendes Inhalts Element, das ein bestimmtes Inhalts Element in einer geordneten oder ungeordneten darstellt <xref:System.Windows.Documents.List> .  
  
 Sie können diese Sammlungen mithilfe der entsprechenden Eigenschaften von **Inlines**, **Blocks** und **ListItems** bearbeiten (hinzufügen oder entfernen). In den folgenden Beispielen wird gezeigt, wie der Inhalt einer Spanne mithilfe der **Inlines** -Eigenschaft bearbeitet wird.  
  
> [!NOTE]
> Table verwendet mehrere Auflistungen, um den Inhalt zu bearbeiten. Diese werden hier aber nicht aufgeführt. Weitere Informationen finden Sie unter [Übersicht über Tabellen](table-overview.md).  
  
 Im folgenden Beispiel wird ein neues <xref:System.Windows.Documents.Span> -Objekt erstellt, und anschließend wird die-Methode verwendet, `Add` um zwei Textläufe als untergeordnete Elemente des hinzuzufügen <xref:System.Windows.Documents.Span> .  
  
 [!code-csharp[SpanSnippets#_SpanInlinesAdd](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesadd)]
 [!code-vb[SpanSnippets#_SpanInlinesAdd](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesadd)]  
  
 Im folgenden Beispiel wird ein neues <xref:System.Windows.Documents.Run> -Element erstellt, das am Anfang der eingefügt wird <xref:System.Windows.Documents.Span> .  
  
 [!code-csharp[SpanSnippets#_SpanInlinesInsert](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesinsert)]
 [!code-vb[SpanSnippets#_SpanInlinesInsert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesinsert)]  
  
 Im folgenden Beispiel wird das letzte- <xref:System.Windows.Documents.Inline> Element in gelöscht <xref:System.Windows.Documents.Span> .  
  
 [!code-csharp[SpanSnippets#_SpanInlinesRemoveLast](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesremovelast)]
 [!code-vb[SpanSnippets#_SpanInlinesRemoveLast](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesremovelast)]  
  
 Im folgenden Beispiel wird der gesamte Inhalt (- <xref:System.Windows.Documents.Inline> Elemente) aus dem gelöscht <xref:System.Windows.Documents.Span> .  
  
 [!code-csharp[SpanSnippets#_SpanInlinesClear](~/samples/snippets/csharp/VS_Snippets_Wpf/SpanSnippets/CSharp/Window1.xaml.cs#_spaninlinesclear)]
 [!code-vb[SpanSnippets#_SpanInlinesClear](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SpanSnippets/visualbasic/window1.xaml.vb#_spaninlinesclear)]  
  
<a name="Types_that_Share_this_Content_Model"></a>
## <a name="types-that-share-this-content-model"></a>Typen, für die dieses Inhaltsmodell freigegeben ist  
 Die folgenden Typen erben von der <xref:System.Windows.Documents.TextElement> -Klasse und können verwendet werden, um den in dieser Übersicht beschriebenen Inhalt anzuzeigen.  
  
 <xref:System.Windows.Documents.Bold>, <xref:System.Windows.Documents.Figure>, <xref:System.Windows.Documents.Floater>, <xref:System.Windows.Documents.Hyperlink>, <xref:System.Windows.Documents.InlineUIContainer>, <xref:System.Windows.Documents.Italic>, <xref:System.Windows.Documents.LineBreak>, <xref:System.Windows.Documents.List>, <xref:System.Windows.Documents.ListItem>, <xref:System.Windows.Documents.Paragraph>, <xref:System.Windows.Documents.Run>, <xref:System.Windows.Documents.Section>, <xref:System.Windows.Documents.Span>, <xref:System.Windows.Documents.Table>, <xref:System.Windows.Documents.Underline>.  
  
 Beachten Sie, dass diese Liste nur nicht abstrakte Typen umfasst, die mit dem Windows SDK verteilt sind. Sie können andere Typen verwenden, die von Erben <xref:System.Windows.Documents.TextElement> .  
  
<a name="Types_that_Can_Contain_ContentControl_Objects"></a>
## <a name="types-that-can-contain-textelement-objects"></a>Typen, die TextElement-Objekte enthalten können  
 Siehe [WPF-Inhalts Modell](../controls/wpf-content-model.md).  
  
## <a name="see-also"></a>Siehe auch

- [Bearbeiten von einem FlowDocument mit der Blocks-Eigenschaft](how-to-manipulate-a-flowdocument-through-the-blocks-property.md)
- [Bearbeiten von fortlaufenden Inhaltselementen mit der Blocks-Eigenschaft](how-to-manipulate-flow-content-elements-through-the-blocks-property.md)
- [Bearbeiten von einem FlowDocument mit der Blocks-Eigenschaft](how-to-manipulate-a-flowdocument-through-the-blocks-property.md)
- [Bearbeiten der Spalten einer Tabelle mit der Columns-Eigenschaft](how-to-manipulate-table-columns-through-the-columns-property.md)
- [Bearbeiten der Zeilengruppen einer Tabelle mit der RowGroups-Eigenschaft](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
