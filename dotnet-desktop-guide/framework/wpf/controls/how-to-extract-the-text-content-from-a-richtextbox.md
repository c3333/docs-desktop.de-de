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
# <a name="how-to-extract-the-text-content-from-a-richtextbox"></a>Gewusst wie: Extrahieren von Textinhalt aus einer RichTextBox
In diesem Beispiel wird gezeigt, wie der Inhalt eines als nur-Text extrahiert wird <xref:System.Windows.Controls.RichTextBox> .  
  
## <a name="example"></a>Beispiel  
 Der folgende [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Code beschreibt ein benanntes <xref:System.Windows.Controls.RichTextBox> Steuerelement mit einfachem Inhalt.  
  
 [!code-xaml[RichTextBoxSnippets#_RTB_XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxSnippets/CSharp/Window1.xaml#_rtb_xaml)]  
  
## <a name="example"></a>Beispiel  
 Der folgende Code implementiert eine Methode, die eine <xref:System.Windows.Controls.RichTextBox> als Argument annimmt und eine Zeichenfolge zurückgibt, die den nur-Text-Inhalt von darstellt <xref:System.Windows.Controls.RichTextBox> .  
  
 Die-Methode erstellt eine neue <xref:System.Windows.Documents.TextRange> aus dem Inhalt des <xref:System.Windows.Controls.RichTextBox> , wobei und verwendet werden, <xref:System.Windows.Documents.FlowDocument.ContentStart%2A> <xref:System.Windows.Documents.FlowDocument.ContentEnd%2A> um den Bereich der zu extrahierenden Inhalte anzugeben.  <xref:System.Windows.Documents.FlowDocument.ContentStart%2A> die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Documents.FlowDocument.ContentEnd%2A> geben jeweils einen zurück. <xref:System.Windows.Documents.TextPointer> auf das zugrunde liegende Fluss Dokument, das den Inhalt von darstellt, kann zugegriffen werden <xref:System.Windows.Controls.RichTextBox> .  <xref:System.Windows.Documents.TextRange> stellt eine Text Eigenschaft bereit, die die nur-Text-Teile von <xref:System.Windows.Documents.TextRange> als Zeichenfolge zurückgibt.  
  
 [!code-csharp[RichTextBoxSnippets#_RTB_StringFrom](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxSnippets/CSharp/Window1.xaml.cs#_rtb_stringfrom)]
 [!code-vb[RichTextBoxSnippets#_RTB_StringFrom](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBoxSnippets/visualbasic/window1.xaml.vb#_rtb_stringfrom)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über RichTextBox](richtextbox-overview.md)
- [Übersicht über TextBox](textbox-overview.md)
