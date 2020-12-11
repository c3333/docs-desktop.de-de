---
title: 'Gewusst wie: Erstellen einer Textdekoration'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [WPF], baseline
- text [WPF], decorations
- fonts [WPF], underline
- fonts [WPF], overline
- strikethrough type [WPF]
- fonts [WPF], strikethrough
- overline type [WPF]
- underline type [WPF]
- typography [WPF], text decorations
- baseline type [WPF]
ms.assetid: cf3cb4e7-782a-4be7-b2d4-e0935e21e4e0
ms.openlocfilehash: cf3b3c3bcb75153a0be4f7ced03b38134b79a930
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977550"
---
# <a name="how-to-create-a-text-decoration"></a>Gewusst wie: Erstellen einer Textdekoration
Ein- <xref:System.Windows.TextDecoration> Objekt ist eine visuelle Verzierung, die Sie Text hinzufügen können. Es gibt vier Arten von Text Dekorationen: Unterstreichung, Baseline, durchgestrichen und über Linien. Im folgenden Beispiel werden die Positionen der Text Dekorationen relativ zum Text dargestellt.  
  
 ![Diagramm der Text Dekorations Typen](./media/how-to-create-a-text-decoration/text-decoration-types.gif)  
  
 Zum Hinzufügen einer Text Dekoration zu Text erstellen Sie ein <xref:System.Windows.TextDecoration> -Objekt, und ändern Sie seine Eigenschaften. Verwenden Sie die- <xref:System.Windows.TextDecoration.Location%2A> Eigenschaft, um anzugeben, wo die Text Dekoration angezeigt wird, z.b. Unterstreichung. Verwenden Sie die- <xref:System.Windows.TextDecoration.Pen%2A> Eigenschaft, um die Darstellung der Text Dekoration anzugeben, z. b. eine voll Tonfarbe oder Farbverlaufs Farbe. Wenn Sie keinen Wert für die-Eigenschaft angeben <xref:System.Windows.TextDecoration.Pen%2A> , wird standardmäßig dieselbe Farbe wie für den Text verwendet. Nachdem Sie ein-Objekt definiert haben <xref:System.Windows.TextDecoration> , fügen Sie es der-Auflistung <xref:System.Windows.TextDecorations> des gewünschten Text Objekts hinzu.  
  
 Das folgende Beispiel zeigt eine Text Dekoration, die mit einem linearen Farbverlaufs Pinsel und einem gestrichelten Stift formatiert wurde.  
  
 ![Textergänzung mit linearer Farbverlaufsunterstreichung](./media/how-to-create-a-text-decoration/text-decoration-gradient.png)  
  
 Das <xref:System.Windows.Documents.Hyperlink> -Objekt ist ein fortlaufendes Inhalts Element auf Inline Ebene, mit dem Sie Hyperlinks innerhalb des fortlaufenden Inhalts hosten können. Standardmäßig wird von <xref:System.Windows.Documents.Hyperlink> ein-Objekt verwendet, <xref:System.Windows.TextDecoration> um einen Unterstrich anzuzeigen. <xref:System.Windows.TextDecoration> die Instanziieren von Objekten kann sehr Leistungs intensiv sein, insbesondere, wenn Sie über viele <xref:System.Windows.Documents.Hyperlink> Objekte verfügen. Wenn Sie Elemente umfassend verwenden, empfiehlt es sich <xref:System.Windows.Documents.Hyperlink> möglicherweise, beim Auslösen eines Ereignisses, z. b. des Ereignisses, eine Unterstreichung anzuzeigen <xref:System.Windows.ContentElement.MouseEnter> .  
  
 Im folgenden Beispiel ist die Unterstreichung für den Link "My MSN" dynamisch – Sie wird nur angezeigt, wenn das <xref:System.Windows.ContentElement.MouseEnter> Ereignis ausgelöst wird.  
  
 ![Links mit TextDecorations](./media/how-to-create-a-text-decoration/text-decorations-hyperlinks.png)  

 Weitere Informationen finden Sie unter [Specify Whether a Hyperlink is Underlined (Angeben, ob ein Link unterstrichen wird)](how-to-specify-whether-a-hyperlink-is-underlined.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird bei einer Unterstreichung der Text Dekoration der Standard Schriftart Wert verwendet.  
  
 [!code-csharp[TextDecorationSnippets#TextDecorationSnippets1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml.cs#textdecorationsnippets1)]
 [!code-vb[TextDecorationSnippets#TextDecorationSnippets1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextDecorationSnippets/visualbasic/window1.xaml.vb#textdecorationsnippets1)]
 [!code-xaml[TextDecorationSnippets#TextDecorationSnippets1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml#textdecorationsnippets1)]  
  
 Im folgenden Codebeispiel wird eine Unterstreichung der Text Dekoration mit einem Pinsel mit voll Tonfarbe für den Stift erstellt.  
  
 [!code-csharp[TextDecorationSnippets#TextDecorationSnippets2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml.cs#textdecorationsnippets2)]
 [!code-vb[TextDecorationSnippets#TextDecorationSnippets2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextDecorationSnippets/visualbasic/window1.xaml.vb#textdecorationsnippets2)]
 [!code-xaml[TextDecorationSnippets#TextDecorationSnippets2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml#textdecorationsnippets2)]  
  
 Im folgenden Codebeispiel wird eine Unterstreichung der Text Dekoration mit einem linearen Farbverlaufs Pinsel für den gestrichelten Stift erstellt.  
  
 [!code-csharp[TextDecorationSnippets#TextDecorationSnippets3](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml.cs#textdecorationsnippets3)]
 [!code-vb[TextDecorationSnippets#TextDecorationSnippets3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextDecorationSnippets/visualbasic/window1.xaml.vb#textdecorationsnippets3)]
 [!code-xaml[TextDecorationSnippets#TextDecorationSnippets3](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml#textdecorationsnippets3)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.TextDecoration>
- <xref:System.Windows.Documents.Hyperlink>
- [Angeben, ob ein Hyperlink unterstrichen wird](how-to-specify-whether-a-hyperlink-is-underlined.md)
