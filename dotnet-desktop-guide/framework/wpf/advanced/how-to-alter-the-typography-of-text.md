---
title: 'Gewusst wie: Ändern der Typografie von Text'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- setting Typography attributes [WPF]
- Typography attribute [WPF], setting
ms.assetid: 19a3b49b-60a2-4c11-a786-e26b4c965588
ms.openlocfilehash: 4c027424632f8671ba8d7cae1c899ef3a53edc26
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976395"
---
# <a name="how-to-alter-the-typography-of-text"></a>Gewusst wie: Ändern der Typografie von Text
Im folgenden Beispiel wird gezeigt, wie das- <xref:System.Windows.Documents.TextElement.Typography%2A> Attribut mithilfe von <xref:System.Windows.Documents.Paragraph> als Beispiel Element festgelegt wird.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[TextElementSnippets#_TextElement_TypogXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextElementSnippets/CSharp/Window1.xaml#_textelement_typogxaml)]  
  
 Die folgende Abbildung zeigt, wie dieses Beispiel gerendert wird.  
  
 ![Screenshot: Text mit geänderter Typografie](./media/textelement-typog.png "TextElement_Typog")  
  
 Im Gegensatz dazu zeigt die folgende Abbildung, wie ein ähnliches Beispiel mit typografischen Standardeigenschaften gerendert wird.  
  
 ![Screenshot: Text mit geänderter Typografie](./media/textelement-typog-default.png "TextElement_Typog_Default")  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie die-Eigenschaft Programm gesteuert festgelegt wird <xref:System.Windows.Controls.TextBox.Typography%2A> .  
  
 [!code-csharp[TextElementSnippets#_TextElement_Typog](~/samples/snippets/csharp/VS_Snippets_Wpf/TextElementSnippets/CSharp/Window1.xaml.cs#_textelement_typog)]
 [!code-vb[TextElementSnippets#_TextElement_Typog](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextElementSnippets/visualbasic/window1.xaml.vb#_textelement_typog)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Flussdokumente](flow-document-overview.md)
