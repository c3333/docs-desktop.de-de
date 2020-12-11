---
title: 'Gewusst wie: Horizontales oder vertikales Kippen eines UIElement'
ms.date: 03/30/2017
helpviewer_keywords:
- flipping UIElements [WPF]
- UIElements [WPF], flipping
ms.assetid: 02c6730f-65c0-40d5-a553-4cb663721882
ms.openlocfilehash: 6b3da322493d17e4f8e36a35b9a0e40fdc9dc685
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977570"
---
# <a name="how-to-flip-a-uielement-horizontally-or-vertically"></a><span data-ttu-id="7eaf8-102">Gewusst wie: Horizontales oder vertikales Kippen eines UIElement</span><span class="sxs-lookup"><span data-stu-id="7eaf8-102">How to: Flip a UIElement Horizontally or Vertically</span></span>
<span data-ttu-id="7eaf8-103">Dieses Beispiel zeigt, wie Sie einen <xref:System.Windows.Media.ScaleTransform> <xref:System.Windows.UIElement> horizontal oder vertikal mit einem kippen.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-103">This example shows how to use a <xref:System.Windows.Media.ScaleTransform> to flip a <xref:System.Windows.UIElement> horizontally or vertically.</span></span> <span data-ttu-id="7eaf8-104">In diesem Beispiel wird ein- <xref:System.Windows.Controls.Button> Steuerelement (ein Typ von <xref:System.Windows.UIElement> ) durch Anwenden eines <xref:System.Windows.Media.ScaleTransform> auf seine- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft gekippt.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-104">In this example, a <xref:System.Windows.Controls.Button> control (a type of <xref:System.Windows.UIElement>) is flipped by applying a <xref:System.Windows.Media.ScaleTransform> to its <xref:System.Windows.UIElement.RenderTransform%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7eaf8-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7eaf8-105">Example</span></span>  
 <span data-ttu-id="7eaf8-106">Die folgende Abbildung zeigt die Schaltfläche zum kippen.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-106">The following illustration shows the button to flip.</span></span>  
  
 <span data-ttu-id="7eaf8-107">![Eine Schaltfläche ohne Transformierung](./media/graphicsmm-buttonflipbeforeflip.gif "graphicsmm_buttonflipbeforeflip")</span><span class="sxs-lookup"><span data-stu-id="7eaf8-107">![A button with no transform](./media/graphicsmm-buttonflipbeforeflip.gif "graphicsmm_buttonflipbeforeflip")</span></span>  
<span data-ttu-id="7eaf8-108">Das zu kippen UIElement.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-108">The UIElement to flip</span></span>  
  
 <span data-ttu-id="7eaf8-109">Der folgende Code zeigt den Code, mit dem die Schaltfläche erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-109">The following shows the code that creates the button.</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMButtonWithoutFlip](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmbuttonwithoutflip)]  
  
## <a name="example"></a><span data-ttu-id="7eaf8-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7eaf8-110">Example</span></span>  
 <span data-ttu-id="7eaf8-111">Um die Schaltfläche horizontal zu kippen, erstellen Sie einen, <xref:System.Windows.Media.ScaleTransform> und legen <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> Sie dessen-Eigenschaft auf-1 fest.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-111">To flip the button horizontally, create a <xref:System.Windows.Media.ScaleTransform> and set its <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> property to -1.</span></span> <span data-ttu-id="7eaf8-112">Wenden <xref:System.Windows.Media.ScaleTransform> Sie auf die-Eigenschaft der Schaltfläche an <xref:System.Windows.UIElement.RenderTransform%2A> .</span><span class="sxs-lookup"><span data-stu-id="7eaf8-112">Apply the <xref:System.Windows.Media.ScaleTransform> to the button's <xref:System.Windows.UIElement.RenderTransform%2A> property.</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMFlipButtonExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmflipbuttonexample1)]  
  
 <span data-ttu-id="7eaf8-113">![Eine mit horizontaler Umschaltfläche &#40;0,0&#41;](./media/graphicsmm-buttonfliphorizontalflip-displaced.gif "graphicsmm_buttonfliphorizontalflip_displaced")</span><span class="sxs-lookup"><span data-stu-id="7eaf8-113">![A button flipped horizontally about &#40;0,0&#41;](./media/graphicsmm-buttonfliphorizontalflip-displaced.gif "graphicsmm_buttonfliphorizontalflip_displaced")</span></span>  
<span data-ttu-id="7eaf8-114">Die Schaltfläche nach dem Anwenden von ScaleTransform</span><span class="sxs-lookup"><span data-stu-id="7eaf8-114">The button after applying the ScaleTransform</span></span>  
  
## <a name="example"></a><span data-ttu-id="7eaf8-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7eaf8-115">Example</span></span>  
 <span data-ttu-id="7eaf8-116">Wie Sie in der vorherigen Abbildung sehen können, wurde die Schaltfläche gekippt, aber auch verschoben.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-116">As you can see from the previous illustration, the button was flipped, but it was also moved.</span></span> <span data-ttu-id="7eaf8-117">Das liegt daran, dass die Schaltfläche von der oberen linken Ecke aus gekippt wurde.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-117">That's because the button was flipped from its top left corner.</span></span> <span data-ttu-id="7eaf8-118">Um die Schaltfläche zu kippen, sollten Sie den <xref:System.Windows.Media.ScaleTransform> auf seine Mitte, nicht auf seine Ecke anwenden.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-118">To flip the button in place, you want to apply the <xref:System.Windows.Media.ScaleTransform> to its center, not its corner.</span></span> <span data-ttu-id="7eaf8-119">Eine einfache Möglichkeit, das <xref:System.Windows.Media.ScaleTransform> auf das Schaltflächen-Center anzuwenden, besteht darin, die-Eigenschaft der Schaltfläche <xref:System.Windows.UIElement.RenderTransformOrigin%2A> auf 0,5, 0,5 festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-119">An easy way to apply the <xref:System.Windows.Media.ScaleTransform> to the buttons center is to set the button's <xref:System.Windows.UIElement.RenderTransformOrigin%2A> property to 0.5, 0.5.</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMFlipButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmflipbuttonexample2)]  
  
 <span data-ttu-id="7eaf8-120">![Eine horizontal um ihren Mittelpunkt gekippte Schaltfläche](./media/graphicsmm-buttonfliphorizontalflip-inplace.gif "graphicsmm_buttonfliphorizontalflip_inplace")</span><span class="sxs-lookup"><span data-stu-id="7eaf8-120">![A button flipped horizontally about its center](./media/graphicsmm-buttonfliphorizontalflip-inplace.gif "graphicsmm_buttonfliphorizontalflip_inplace")</span></span>  
<span data-ttu-id="7eaf8-121">Die Schaltfläche mit einem RenderTransformOrigin von 0,5, 0,5</span><span class="sxs-lookup"><span data-stu-id="7eaf8-121">The button with a RenderTransformOrigin of 0.5, 0.5</span></span>  
  
## <a name="example"></a><span data-ttu-id="7eaf8-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7eaf8-122">Example</span></span>  
 <span data-ttu-id="7eaf8-123">Wenn Sie die Schaltfläche vertikal kippen möchten, legen Sie die <xref:System.Windows.Media.ScaleTransform> -Eigenschaft des-Objekts <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> anstelle der- <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7eaf8-123">To flip the button vertically, set the <xref:System.Windows.Media.ScaleTransform> object's <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> property instead of its <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> property.</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMVerticalFlipButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmverticalflipbuttonexample2)]  
  
 <span data-ttu-id="7eaf8-124">![Eine vertikal um ihren Mittelpunkt gekippte Schaltfläche](./media/graphicsmm-buttonflipverticalflip-inplace.gif "graphicsmm_buttonflipverticalflip_inplace")</span><span class="sxs-lookup"><span data-stu-id="7eaf8-124">![A button flipped vertically about its center](./media/graphicsmm-buttonflipverticalflip-inplace.gif "graphicsmm_buttonflipverticalflip_inplace")</span></span>  
<span data-ttu-id="7eaf8-125">Die vertikal geflickte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="7eaf8-125">The vertically flipped button</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7eaf8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7eaf8-126">See also</span></span>

- [<span data-ttu-id="7eaf8-127">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="7eaf8-127">Transforms Overview</span></span>](../graphics-multimedia/transforms-overview.md)
