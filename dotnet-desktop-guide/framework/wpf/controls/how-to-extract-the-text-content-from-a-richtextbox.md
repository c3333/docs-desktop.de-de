---
title: 'Gewusst wie: Extrahieren von Textinhalt aus einer RichTextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text content [WPF], extracting
- RichTextBox control [WPF], extracting text content
- content [WPF], extracting
- extracting text content [WPF]
ms.assetid: f13c093f-1a05-45b3-ac8f-c9ea5e4a11c5
ms.openlocfilehash: d1d40f37c23455dfc48206f84bca1b8438fec6c4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977336"
---
# <a name="how-to-extract-the-text-content-from-a-richtextbox"></a><span data-ttu-id="6b8db-102">Gewusst wie: Extrahieren von Textinhalt aus einer RichTextBox</span><span class="sxs-lookup"><span data-stu-id="6b8db-102">How to: Extract the Text Content from a RichTextBox</span></span>
<span data-ttu-id="6b8db-103">In diesem Beispiel wird gezeigt, wie der Inhalt eines als nur-Text extrahiert wird <xref:System.Windows.Controls.RichTextBox> .</span><span class="sxs-lookup"><span data-stu-id="6b8db-103">This example shows how to extract the contents of a <xref:System.Windows.Controls.RichTextBox> as plain text.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6b8db-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6b8db-104">Example</span></span>  
 <span data-ttu-id="6b8db-105">Der folgende [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Code beschreibt ein benanntes <xref:System.Windows.Controls.RichTextBox> Steuerelement mit einfachem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="6b8db-105">The following [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] code describes a named <xref:System.Windows.Controls.RichTextBox> control with simple content.</span></span>  
  
 [!code-xaml[RichTextBoxSnippets#_RTB_XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxSnippets/CSharp/Window1.xaml#_rtb_xaml)]  
  
## <a name="example"></a><span data-ttu-id="6b8db-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6b8db-106">Example</span></span>  
 <span data-ttu-id="6b8db-107">Der folgende Code implementiert eine Methode, die eine <xref:System.Windows.Controls.RichTextBox> als Argument annimmt und eine Zeichenfolge zurückgibt, die den nur-Text-Inhalt von darstellt <xref:System.Windows.Controls.RichTextBox> .</span><span class="sxs-lookup"><span data-stu-id="6b8db-107">The following code implements a method that takes a <xref:System.Windows.Controls.RichTextBox> as an argument, and returns a string representing the plain text contents of the <xref:System.Windows.Controls.RichTextBox>.</span></span>  
  
 <span data-ttu-id="6b8db-108">Die-Methode erstellt eine neue <xref:System.Windows.Documents.TextRange> aus dem Inhalt des <xref:System.Windows.Controls.RichTextBox> , wobei und verwendet werden, <xref:System.Windows.Documents.FlowDocument.ContentStart%2A> <xref:System.Windows.Documents.FlowDocument.ContentEnd%2A> um den Bereich der zu extrahierenden Inhalte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6b8db-108">The method creates a new <xref:System.Windows.Documents.TextRange> from the contents of the <xref:System.Windows.Controls.RichTextBox>, using the <xref:System.Windows.Documents.FlowDocument.ContentStart%2A> and <xref:System.Windows.Documents.FlowDocument.ContentEnd%2A> to indicate the range of the contents to extract.</span></span>  <span data-ttu-id="6b8db-109"><xref:System.Windows.Documents.FlowDocument.ContentStart%2A> die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Documents.FlowDocument.ContentEnd%2A> geben jeweils einen zurück. <xref:System.Windows.Documents.TextPointer> auf das zugrunde liegende Fluss Dokument, das den Inhalt von darstellt, kann zugegriffen werden <xref:System.Windows.Controls.RichTextBox> .</span><span class="sxs-lookup"><span data-stu-id="6b8db-109"><xref:System.Windows.Documents.FlowDocument.ContentStart%2A> and <xref:System.Windows.Documents.FlowDocument.ContentEnd%2A> properties each return a <xref:System.Windows.Documents.TextPointer>, and are accessible on the underlying FlowDocument that represents the contents of the <xref:System.Windows.Controls.RichTextBox>.</span></span>  <span data-ttu-id="6b8db-110"><xref:System.Windows.Documents.TextRange> stellt eine Text Eigenschaft bereit, die die nur-Text-Teile von <xref:System.Windows.Documents.TextRange> als Zeichenfolge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6b8db-110"><xref:System.Windows.Documents.TextRange> provides a Text property, which returns the plain text portions of the <xref:System.Windows.Documents.TextRange> as a string.</span></span>  
  
 [!code-csharp[RichTextBoxSnippets#_RTB_StringFrom](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxSnippets/CSharp/Window1.xaml.cs#_rtb_stringfrom)]
 [!code-vb[RichTextBoxSnippets#_RTB_StringFrom](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBoxSnippets/visualbasic/window1.xaml.vb#_rtb_stringfrom)]  
  
## <a name="see-also"></a><span data-ttu-id="6b8db-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b8db-111">See also</span></span>

- [<span data-ttu-id="6b8db-112">Übersicht über RichTextBox</span><span class="sxs-lookup"><span data-stu-id="6b8db-112">RichTextBox Overview</span></span>](richtextbox-overview.md)
- [<span data-ttu-id="6b8db-113">Übersicht über TextBox</span><span class="sxs-lookup"><span data-stu-id="6b8db-113">TextBox Overview</span></span>](textbox-overview.md)
