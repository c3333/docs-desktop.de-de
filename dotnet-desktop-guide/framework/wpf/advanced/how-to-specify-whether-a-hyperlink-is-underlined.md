---
title: 'Gewusst wie: Angeben, ob ein Hyperlink unterstrichen wird'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Hyperlink control type [WPF]
ms.assetid: 3996cfe6-1dac-4835-aeb3-c719ce9cfee5
ms.openlocfilehash: 5718912e24a0697f209669b0ab4e7f4df1765ed3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974868"
---
# <a name="how-to-specify-whether-a-hyperlink-is-underlined"></a>Gewusst wie: Angeben, ob ein Hyperlink unterstrichen wird
Das <xref:System.Windows.Documents.Hyperlink> -Objekt ist ein fortlaufendes Inhalts Element auf Inline Ebene, mit dem Sie Hyperlinks innerhalb des fortlaufenden Inhalts hosten können. Standardmäßig wird von <xref:System.Windows.Documents.Hyperlink> ein-Objekt verwendet, <xref:System.Windows.TextDecoration> um einen Unterstrich anzuzeigen. <xref:System.Windows.TextDecoration> die Instanziieren von Objekten kann sehr Leistungs intensiv sein, insbesondere, wenn Sie über viele <xref:System.Windows.Documents.Hyperlink> Objekte verfügen. Wenn Sie Elemente umfassend verwenden, empfiehlt es sich <xref:System.Windows.Documents.Hyperlink> möglicherweise, beim Auslösen eines Ereignisses, z. b. des Ereignisses, eine Unterstreichung anzuzeigen <xref:System.Windows.ContentElement.MouseEnter> .  
  
 Im folgenden Beispiel ist die Unterstreichung für den Link "My MSN" dynamisch, d. h., er wird nur angezeigt, wenn das <xref:System.Windows.ContentElement.MouseEnter> Ereignis ausgelöst wird.  
  
  ![Links mit TextDecorations](./media/how-to-specify-whether-a-hyperlink-is-underlined/text-decorations-hyperlinks.png)  

## <a name="example"></a>Beispiel  
 Das folgende Markup Beispiel zeigt einen, der <xref:System.Windows.Documents.Hyperlink> mit und ohne Unterstreichung definiert ist:  
  
 [!code-xaml[Performance#PerformanceSnippet11](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/Hyperlink.xaml#performancesnippet11)]  
  
 Im folgenden Codebeispiel wird veranschaulicht, wie ein Unterstrich für das <xref:System.Windows.Documents.Hyperlink> <xref:System.Windows.ContentElement.MouseEnter> -Ereignis erstellt und für das-Ereignis entfernt wird <xref:System.Windows.ContentElement.MouseLeave> .  
  
 [!code-csharp[Performance#PerformanceSnippet15](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/Hyperlink.xaml.cs#performancesnippet15)]
 [!code-vb[Performance#PerformanceSnippet15](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Performance/visualbasic/hyperlink.xaml.vb#performancesnippet15)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.TextDecoration>
- <xref:System.Windows.Documents.Hyperlink>
- [Optimieren der WPF-Anwendungsleistung](optimizing-wpf-application-performance.md)
- [Erstellen einer Textdekoration](how-to-create-a-text-decoration.md)
