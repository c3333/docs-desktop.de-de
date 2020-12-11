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
# <a name="how-to-specify-whether-a-hyperlink-is-underlined"></a><span data-ttu-id="88263-102">Gewusst wie: Angeben, ob ein Hyperlink unterstrichen wird</span><span class="sxs-lookup"><span data-stu-id="88263-102">How to: Specify Whether a Hyperlink is Underlined</span></span>
<span data-ttu-id="88263-103">Das <xref:System.Windows.Documents.Hyperlink> -Objekt ist ein fortlaufendes Inhalts Element auf Inline Ebene, mit dem Sie Hyperlinks innerhalb des fortlaufenden Inhalts hosten können.</span><span class="sxs-lookup"><span data-stu-id="88263-103">The <xref:System.Windows.Documents.Hyperlink> object is an inline-level flow content element that allows you to host hyperlinks within the flow content.</span></span> <span data-ttu-id="88263-104">Standardmäßig wird von <xref:System.Windows.Documents.Hyperlink> ein-Objekt verwendet, <xref:System.Windows.TextDecoration> um einen Unterstrich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="88263-104">By default, <xref:System.Windows.Documents.Hyperlink> uses a <xref:System.Windows.TextDecoration> object to display an underline.</span></span> <span data-ttu-id="88263-105"><xref:System.Windows.TextDecoration> die Instanziieren von Objekten kann sehr Leistungs intensiv sein, insbesondere, wenn Sie über viele <xref:System.Windows.Documents.Hyperlink> Objekte verfügen.</span><span class="sxs-lookup"><span data-stu-id="88263-105"><xref:System.Windows.TextDecoration> objects can be performance intensive to instantiate, particularly if you have many <xref:System.Windows.Documents.Hyperlink> objects.</span></span> <span data-ttu-id="88263-106">Wenn Sie Elemente umfassend verwenden, empfiehlt es sich <xref:System.Windows.Documents.Hyperlink> möglicherweise, beim Auslösen eines Ereignisses, z. b. des Ereignisses, eine Unterstreichung anzuzeigen <xref:System.Windows.ContentElement.MouseEnter> .</span><span class="sxs-lookup"><span data-stu-id="88263-106">If you make extensive use of <xref:System.Windows.Documents.Hyperlink> elements, you may want to consider showing an underline only when triggering an event, such as the <xref:System.Windows.ContentElement.MouseEnter> event.</span></span>  
  
 <span data-ttu-id="88263-107">Im folgenden Beispiel ist die Unterstreichung für den Link "My MSN" dynamisch, d. h., er wird nur angezeigt, wenn das <xref:System.Windows.ContentElement.MouseEnter> Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="88263-107">In the following example, the underline for the "My MSN" link is dynamic, that is, it only appears when the <xref:System.Windows.ContentElement.MouseEnter> event is triggered.</span></span>  
  
  ![Links mit TextDecorations](./media/how-to-specify-whether-a-hyperlink-is-underlined/text-decorations-hyperlinks.png)  

## <a name="example"></a><span data-ttu-id="88263-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="88263-109">Example</span></span>  
 <span data-ttu-id="88263-110">Das folgende Markup Beispiel zeigt einen, der <xref:System.Windows.Documents.Hyperlink> mit und ohne Unterstreichung definiert ist:</span><span class="sxs-lookup"><span data-stu-id="88263-110">The following markup sample shows a <xref:System.Windows.Documents.Hyperlink> defined with and without an underline:</span></span>  
  
 [!code-xaml[Performance#PerformanceSnippet11](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/Hyperlink.xaml#performancesnippet11)]  
  
 <span data-ttu-id="88263-111">Im folgenden Codebeispiel wird veranschaulicht, wie ein Unterstrich für das <xref:System.Windows.Documents.Hyperlink> <xref:System.Windows.ContentElement.MouseEnter> -Ereignis erstellt und für das-Ereignis entfernt wird <xref:System.Windows.ContentElement.MouseLeave> .</span><span class="sxs-lookup"><span data-stu-id="88263-111">The following code sample shows how to create an underline for the <xref:System.Windows.Documents.Hyperlink> on the <xref:System.Windows.ContentElement.MouseEnter> event, and remove it on the <xref:System.Windows.ContentElement.MouseLeave> event.</span></span>  
  
 [!code-csharp[Performance#PerformanceSnippet15](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/Hyperlink.xaml.cs#performancesnippet15)]
 [!code-vb[Performance#PerformanceSnippet15](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Performance/visualbasic/hyperlink.xaml.vb#performancesnippet15)]  
  
## <a name="see-also"></a><span data-ttu-id="88263-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88263-112">See also</span></span>

- <xref:System.Windows.TextDecoration>
- <xref:System.Windows.Documents.Hyperlink>
- [<span data-ttu-id="88263-113">Optimieren der WPF-Anwendungsleistung</span><span class="sxs-lookup"><span data-stu-id="88263-113">Optimizing WPF Application Performance</span></span>](optimizing-wpf-application-performance.md)
- [<span data-ttu-id="88263-114">Erstellen einer Textdekoration</span><span class="sxs-lookup"><span data-stu-id="88263-114">Create a Text Decoration</span></span>](how-to-create-a-text-decoration.md)
