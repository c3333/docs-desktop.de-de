---
title: 'Gewusst wie: Verwenden von FlowDocument-Attributen für die Trennung von Spalten'
ms.date: 03/30/2017
helpviewer_keywords:
- FlowDocument column-separating attributes
- column-separating attributes
- documents [WPF], FlowDocument column-separating attributes
ms.assetid: c7a822f8-aeca-45bd-a258-2852ff28005c
ms.openlocfilehash: 27491b21da587fa198061ba52d8daed5d3f28de3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977839"
---
# <a name="how-to-use-flowdocument-column-separating-attributes"></a><span data-ttu-id="d7277-102">Gewusst wie: Verwenden von FlowDocument-Attributen für die Trennung von Spalten</span><span class="sxs-lookup"><span data-stu-id="d7277-102">How to: Use FlowDocument Column-Separating Attributes</span></span>
<span data-ttu-id="d7277-103">In diesem Beispiel wird gezeigt, wie die Spalten Trennungs Funktionen eines verwendet werden <xref:System.Windows.Documents.FlowDocument> .</span><span class="sxs-lookup"><span data-stu-id="d7277-103">This example shows how to use the column-separating features of a <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d7277-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d7277-104">Example</span></span>  
 <span data-ttu-id="d7277-105">Im folgenden Beispiel wird eine definiert <xref:System.Windows.Documents.FlowDocument> und die <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A> Attribute, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A> und festgelegt <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> .</span><span class="sxs-lookup"><span data-stu-id="d7277-105">The following example defines a <xref:System.Windows.Documents.FlowDocument>, and sets the <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, and <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributes.</span></span>  <span data-ttu-id="d7277-106">Der <xref:System.Windows.Documents.FlowDocument> enthält einen einzelnen Absatz von Beispiel Inhalt.</span><span class="sxs-lookup"><span data-stu-id="d7277-106">The <xref:System.Windows.Documents.FlowDocument> contains a single paragraph of sample content.</span></span>  
  
 [!code-xaml[FlowDocumentSnippets#_FlowDocumentColumnStuffXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml#_flowdocumentcolumnstuffxaml)]  
  
 <span data-ttu-id="d7277-107">In der folgenden Abbildung werden die Auswirkungen der <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A> <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A> Attribute, und <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> in einem gerenderten dargestellt <xref:System.Windows.Documents.FlowDocument> .</span><span class="sxs-lookup"><span data-stu-id="d7277-107">The following figure shows the effects of the <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, and <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributes in a rendered <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 ![Screenshot, der das Attribut "FlowDocument Intra Column" anzeigt.](./media/how-to-use-flowdocument-column-separating-attributes/flowdocument-intra-column.png)
