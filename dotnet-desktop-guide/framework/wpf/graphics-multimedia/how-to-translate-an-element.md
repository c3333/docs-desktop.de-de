---
title: 'Gewusst wie: Übersetzen eines Elements'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], translations
ms.assetid: 461c8273-15df-42f6-8672-89ba22887cc0
ms.openlocfilehash: addff0e22fb3f27ea924887809c0635aeb3ad67d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976858"
---
# <a name="how-to-translate-an-element"></a><span data-ttu-id="101df-102">Gewusst wie: Übersetzen eines Elements</span><span class="sxs-lookup"><span data-stu-id="101df-102">How to: Translate an Element</span></span>
<span data-ttu-id="101df-103">In diesem Beispiel wird gezeigt, wie ein Element mithilfe eines übersetzt (verschoben) werden kann <xref:System.Windows.Media.TranslateTransform> .</span><span class="sxs-lookup"><span data-stu-id="101df-103">This example shows how to translate (move) an element by using a <xref:System.Windows.Media.TranslateTransform>.</span></span>  
  
 <span data-ttu-id="101df-104">Die- <xref:System.Windows.Media.TranslateTransform> Klasse ist besonders nützlich zum Verschieben von Elementen in Bereichen, die keine absolute Positionierung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="101df-104">The <xref:System.Windows.Media.TranslateTransform> class is especially useful for moving elements inside panels that do not support absolute positioning.</span></span> <span data-ttu-id="101df-105">Wenn Sie z. b. ein <xref:System.Windows.Media.TranslateTransform> auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft eines-Elements anwenden, können Sie ein Element innerhalb von <xref:System.Windows.Controls.StackPanel> oder verschieben <xref:System.Windows.Controls.DockPanel> .</span><span class="sxs-lookup"><span data-stu-id="101df-105">For example, by applying a <xref:System.Windows.Media.TranslateTransform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property of an element, you can move an element within a <xref:System.Windows.Controls.StackPanel> or <xref:System.Windows.Controls.DockPanel>.</span></span>  
  
 <span data-ttu-id="101df-106">Verwenden Sie die- <xref:System.Windows.Media.TranslateTransform.X%2A> Eigenschaft des, <xref:System.Windows.Media.TranslateTransform> um den Betrag in Pixel anzugeben, um das Element entlang der x-Achse zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="101df-106">Use the <xref:System.Windows.Media.TranslateTransform.X%2A> property of the <xref:System.Windows.Media.TranslateTransform> to specify the amount, in pixels, to move the element along the x-axis.</span></span> <span data-ttu-id="101df-107">Verwenden Sie die- <xref:System.Windows.Media.TranslateTransform.Y%2A> Eigenschaft, um den Betrag in Pixel anzugeben, um das Element entlang der y-Achse zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="101df-107">Use the <xref:System.Windows.Media.TranslateTransform.Y%2A> property to specify the amount, in pixels, to move the element along the y-axis.</span></span> <span data-ttu-id="101df-108">Wenden Sie schließlich das <xref:System.Windows.Media.TranslateTransform> auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft des-Elements an.</span><span class="sxs-lookup"><span data-stu-id="101df-108">Finally, apply the <xref:System.Windows.Media.TranslateTransform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property of the element.</span></span>  
  
 <span data-ttu-id="101df-109">Im folgenden Beispiel wird ein <xref:System.Windows.Media.TranslateTransform> -Element verwendet, um ein Element 50 Pixel nach rechts und 50 Pixel nach unten zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="101df-109">The following example uses a <xref:System.Windows.Media.TranslateTransform> to move an element 50 pixels to the right and 50 pixels down.</span></span>  
  
## <a name="example"></a><span data-ttu-id="101df-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="101df-110">Example</span></span>  
 [!code-xaml[transformsSample#53](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/TranslateTransformExample.xaml#53)]  
  
 <span data-ttu-id="101df-111">Das komplette Beispiel finden Sie unter [Beispiel für 2D-Transformationen](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).</span><span class="sxs-lookup"><span data-stu-id="101df-111">For the complete sample, see [2D Transforms Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="101df-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="101df-112">See also</span></span>

- [<span data-ttu-id="101df-113">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="101df-113">Transforms Overview</span></span>](transforms-overview.md)
