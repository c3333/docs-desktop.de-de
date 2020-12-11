---
title: 'Gewusst wie: Erstellen eines Expanders mit einem ScrollViewer'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], Expander
- ScrollViewer control [WPF], with Expander control
- Expander control [WPF], creating
- controls [WPF], ScrollViewer
ms.assetid: 2ad124d2-2406-4157-aaf2-64e067298f01
ms.openlocfilehash: ef0bc5d344f7d465de9209708430d3e61d40d4f7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977654"
---
# <a name="how-to-create-an-expander-with-a-scrollviewer"></a><span data-ttu-id="02308-102">Gewusst wie: Erstellen eines Expanders mit einem ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="02308-102">How to: Create an Expander with a ScrollViewer</span></span>
<span data-ttu-id="02308-103">In diesem Beispiel wird gezeigt, wie ein-Steuerelement erstellt <xref:System.Windows.Controls.Expander> wird, das komplexen Inhalt enthält, z. b. ein Bild und Text.</span><span class="sxs-lookup"><span data-stu-id="02308-103">This example shows how to create an <xref:System.Windows.Controls.Expander> control that contains complex content, such as an image and text.</span></span> <span data-ttu-id="02308-104">Im Beispiel wird auch der Inhalt von <xref:System.Windows.Controls.Expander> in einem-Steuerelement eingeschlossen <xref:System.Windows.Controls.ScrollViewer> .</span><span class="sxs-lookup"><span data-stu-id="02308-104">The example also encloses the content of the <xref:System.Windows.Controls.Expander> in a <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="02308-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="02308-105">Example</span></span>  
 <span data-ttu-id="02308-106">Im folgenden Beispiel wird gezeigt, wie ein erstellt wird <xref:System.Windows.Controls.Expander> .</span><span class="sxs-lookup"><span data-stu-id="02308-106">The following example shows how to create an <xref:System.Windows.Controls.Expander>.</span></span> <span data-ttu-id="02308-107">Das Beispiel verwendet ein <xref:System.Windows.Controls.Primitives.BulletDecorator> -Steuerelement, das ein Bild und Text enthält, um zu definieren <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> .</span><span class="sxs-lookup"><span data-stu-id="02308-107">The example uses a <xref:System.Windows.Controls.Primitives.BulletDecorator> control, which contains an image and text, in order to define the <xref:System.Windows.Controls.HeaderedContentControl.Header%2A>.</span></span> <span data-ttu-id="02308-108">Ein- <xref:System.Windows.Controls.ScrollViewer> Steuerelement stellt eine Methode für den Bildlauf im erweiterten Inhalt bereit.</span><span class="sxs-lookup"><span data-stu-id="02308-108">A <xref:System.Windows.Controls.ScrollViewer> control provides a method for scrolling the expanded content.</span></span>  
  
 <span data-ttu-id="02308-109">Beachten Sie, dass im Beispiel die- <xref:System.Windows.FrameworkElement.Height%2A> Eigenschaft für <xref:System.Windows.Controls.ScrollViewer> anstelle von für den Inhalt festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="02308-109">Note that the example sets the <xref:System.Windows.FrameworkElement.Height%2A> property on the <xref:System.Windows.Controls.ScrollViewer> instead of on the content.</span></span> <span data-ttu-id="02308-110">Wenn <xref:System.Windows.FrameworkElement.Height%2A> für den Inhalt festgelegt ist, kann der <xref:System.Windows.Controls.ScrollViewer> Benutzer nicht durch den Inhalt scrollen.</span><span class="sxs-lookup"><span data-stu-id="02308-110">If the <xref:System.Windows.FrameworkElement.Height%2A> is set on the content, the <xref:System.Windows.Controls.ScrollViewer> does not allow the user to scroll the content.</span></span> <span data-ttu-id="02308-111">Die- <xref:System.Windows.FrameworkElement.Width%2A> Eigenschaft wird für das-Steuerelement festgelegt <xref:System.Windows.Controls.Expander> , und diese Einstellung gilt für den <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> und den erweiterten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="02308-111">The <xref:System.Windows.FrameworkElement.Width%2A> property is set on the <xref:System.Windows.Controls.Expander> control and this setting applies to the <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> and the expanded content.</span></span>  
  
 [!code-xaml[ExpanderRichContent#CreateExpander](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderRichContent/CSharp/Window1.xaml#createexpander)]  
  
 [!code-csharp[ExpanderRichContent#CreateExpanderCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderRichContent/CSharp/Window1.xaml.cs#createexpandercode)]  
  
## <a name="see-also"></a><span data-ttu-id="02308-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02308-112">See also</span></span>

- <xref:System.Windows.Controls.Expander>
- [<span data-ttu-id="02308-113">Übersicht über Expander-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="02308-113">Expander Overview</span></span>](expander-overview.md)
- [<span data-ttu-id="02308-114">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="02308-114">How-to Topics</span></span>](expander-how-to-topics.md)
