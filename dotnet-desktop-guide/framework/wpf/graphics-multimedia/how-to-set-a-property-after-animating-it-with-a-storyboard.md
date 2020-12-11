---
title: 'Gewusst wie: Festlegen einer Eigenschaft nach einer Storyboard-Animation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], changing property values after
ms.assetid: 79466556-4dbf-40bd-9c1e-a77613b07077
ms.openlocfilehash: 593d3fcefe3bb81518d0886afde82f9a172874ba
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976870"
---
# <a name="how-to-set-a-property-after-animating-it-with-a-storyboard"></a><span data-ttu-id="6e979-102">Gewusst wie: Festlegen einer Eigenschaft nach einer Storyboard-Animation</span><span class="sxs-lookup"><span data-stu-id="6e979-102">How to: Set a Property After Animating It with a Storyboard</span></span>
<span data-ttu-id="6e979-103">In einigen Fällen kann es vorkommen, dass Sie den Wert einer Eigenschaft nach dem Animieren nicht ändern können.</span><span class="sxs-lookup"><span data-stu-id="6e979-103">In some cases, it might appear that you can't change the value of a property after it has been animated.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6e979-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e979-104">Example</span></span>  
 <span data-ttu-id="6e979-105">Im folgenden Beispiel <xref:System.Windows.Media.Animation.Storyboard> wird ein verwendet, um die Farbe eines zu animieren <xref:System.Windows.Media.SolidColorBrush> .</span><span class="sxs-lookup"><span data-stu-id="6e979-105">In the following example, a <xref:System.Windows.Media.Animation.Storyboard> is used to animate the color of a <xref:System.Windows.Media.SolidColorBrush>.</span></span> <span data-ttu-id="6e979-106">Das Storyboard wird ausgelöst, wenn auf die Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="6e979-106">The storyboard is triggered when the button is clicked.</span></span> <span data-ttu-id="6e979-107">Das <xref:System.Windows.Media.Animation.Timeline.Completed> Ereignis wird behandelt, damit das Programm benachrichtigt wird, wenn <xref:System.Windows.Media.Animation.ColorAnimation> abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="6e979-107">The <xref:System.Windows.Media.Animation.Timeline.Completed> event is handled so that the program is notified when the <xref:System.Windows.Media.Animation.ColorAnimation> completes.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#GraphicsMMButton1Declaration](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml#graphicsmmbutton1declaration)]  
  
## <a name="example"></a><span data-ttu-id="6e979-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e979-108">Example</span></span>  
 <span data-ttu-id="6e979-109">Nachdem der <xref:System.Windows.Media.Animation.ColorAnimation> abgeschlossen ist, versucht das Programm, die Farbe des Pinsels in blau zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6e979-109">After the <xref:System.Windows.Media.Animation.ColorAnimation> completes, the program attempts to change the brush's color to blue.</span></span>  
  
 [!code-csharp[timingbehaviors_snip#GraphicsMMButton1Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml.cs#graphicsmmbutton1handler)]
 [!code-vb[timingbehaviors_snip#GraphicsMMButton1Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_snip/visualbasic/animatethensetpropertyexample.xaml.vb#graphicsmmbutton1handler)]  
  
 <span data-ttu-id="6e979-110">Der vorherige Code scheint nichts zu tun: der Pinsel bleibt Gelb, d. h. der Wert, der von der bereitgestellt wird, die <xref:System.Windows.Media.Animation.ColorAnimation> den Pinsel animiert hat.</span><span class="sxs-lookup"><span data-stu-id="6e979-110">The previous code doesn't appear to do anything: the brush remains yellow, which is the value supplied by the <xref:System.Windows.Media.Animation.ColorAnimation> that animated the brush.</span></span> <span data-ttu-id="6e979-111">Der zugrunde liegende Eigenschafts Wert (der Basiswert) wird tatsächlich in blau geändert.</span><span class="sxs-lookup"><span data-stu-id="6e979-111">The underlying property value (the base value) is actually changed to blue.</span></span> <span data-ttu-id="6e979-112">Der effektive oder aktuelle Wert bleibt jedoch gelb, da der <xref:System.Windows.Media.Animation.ColorAnimation> den Basiswert weiterhin überschreibt.</span><span class="sxs-lookup"><span data-stu-id="6e979-112">However, the effective, or current, value remains yellow because the <xref:System.Windows.Media.Animation.ColorAnimation> is still overriding the base value.</span></span> <span data-ttu-id="6e979-113">Wenn der Basiswert wieder der effektive Wert werden soll, müssen Sie die Animation daran hindern, die Eigenschaft zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="6e979-113">If you want the base value to become the effective value again, you must stop the animation from influencing the property.</span></span> <span data-ttu-id="6e979-114">Es gibt drei Möglichkeiten, um dies mit Storyboard-Animationen zu erreichen:</span><span class="sxs-lookup"><span data-stu-id="6e979-114">There are three ways to do this with storyboard animations:</span></span>  
  
- <span data-ttu-id="6e979-115">Legen Sie die-Eigenschaft der Animation auf fest. <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A><xref:System.Windows.Media.Animation.FillBehavior.Stop></span><span class="sxs-lookup"><span data-stu-id="6e979-115">Set the animation's <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> property to <xref:System.Windows.Media.Animation.FillBehavior.Stop></span></span>  
  
- <span data-ttu-id="6e979-116">Entfernen Sie das gesamte Storyboard.</span><span class="sxs-lookup"><span data-stu-id="6e979-116">Remove the entire Storyboard.</span></span>  
  
- <span data-ttu-id="6e979-117">Entfernen Sie die Animation aus der einzelnen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e979-117">Remove the animation from the individual property.</span></span>  
  
## <a name="set-the-animations-fillbehavior-property-to-stop"></a><span data-ttu-id="6e979-118">Festlegen der FillBehavior-Eigenschaft der Animation auf "wird beendet"</span><span class="sxs-lookup"><span data-stu-id="6e979-118">Set the animation's FillBehavior property to Stop</span></span>  
 <span data-ttu-id="6e979-119">Wenn <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> Sie auf festlegen <xref:System.Windows.Media.Animation.FillBehavior.Stop> , teilen Sie der Animation mit, dass die Ziel Eigenschaft nicht mehr beeinträchtigt wird, nachdem das Ende des aktiven Zeitraums erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="6e979-119">By setting <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> to <xref:System.Windows.Media.Animation.FillBehavior.Stop>, you tell the animation to stop affecting its target property after it reaches the end of its active period.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#GraphicsMMButton2Declaration](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml#graphicsmmbutton2declaration)]  
  
 [!code-csharp[timingbehaviors_snip#GraphicsMMButton2Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml.cs#graphicsmmbutton2handler)]
 [!code-vb[timingbehaviors_snip#GraphicsMMButton2Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_snip/visualbasic/animatethensetpropertyexample.xaml.vb#graphicsmmbutton2handler)]  
  
## <a name="remove-the-entire-storyboard"></a><span data-ttu-id="6e979-120">Entfernen des gesamten Storyboards</span><span class="sxs-lookup"><span data-stu-id="6e979-120">Remove the entire storyboard</span></span>  
 <span data-ttu-id="6e979-121">Wenn Sie einen- <xref:System.Windows.Media.Animation.RemoveStoryboard> oder die- <xref:System.Windows.Media.Animation.Storyboard.Remove%2A?displayProperty=nameWithType> Methode verwenden, teilen Sie den Storyboard-Animationen mit, dass Ihre Zieleigenschaften nicht mehr beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="6e979-121">By using a <xref:System.Windows.Media.Animation.RemoveStoryboard> trigger or the <xref:System.Windows.Media.Animation.Storyboard.Remove%2A?displayProperty=nameWithType> method, you tell the storyboard animations to stop affecting their target properties.</span></span> <span data-ttu-id="6e979-122">Der Unterschied zwischen diesem Ansatz und dem Festlegen der- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> Eigenschaft besteht darin, dass Sie das Storyboard jederzeit entfernen können, während die- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> Eigenschaft nur dann wirksam wird, wenn die Animation das Ende des aktiven Zeitraums erreicht.</span><span class="sxs-lookup"><span data-stu-id="6e979-122">The difference between this approach and setting the <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> property is that you can remove the storyboard at anytime, while the <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> property only has an effect when the animation reaches the end of its active period.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#GraphicsMMButton3Declaration](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml#graphicsmmbutton3declaration)]  
  
 [!code-csharp[timingbehaviors_snip#GraphicsMMButton3Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml.cs#graphicsmmbutton3handler)]
 [!code-vb[timingbehaviors_snip#GraphicsMMButton3Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_snip/visualbasic/animatethensetpropertyexample.xaml.vb#graphicsmmbutton3handler)]  
  
## <a name="remove-an-animation-from-an-individual-property"></a><span data-ttu-id="6e979-123">Entfernen einer Animation aus einer einzelnen Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6e979-123">Remove an animation from an individual property</span></span>  
 <span data-ttu-id="6e979-124">Eine andere Möglichkeit, eine Animation daran zu hindern, eine Eigenschaft zu beeinflussen, ist die Verwendung der- <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%28System.Windows.DependencyProperty%2CSystem.Windows.Media.Animation.AnimationTimeline%29> Methode des zu animierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="6e979-124">Another technique to stop an animation from affecting a property is to use the <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%28System.Windows.DependencyProperty%2CSystem.Windows.Media.Animation.AnimationTimeline%29> method of the object being animated.</span></span> <span data-ttu-id="6e979-125">Geben Sie die zu animierende Eigenschaft als ersten Parameter und `null` als zweiten an.</span><span class="sxs-lookup"><span data-stu-id="6e979-125">Specify the property being animated as the first parameter and `null` as the second.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#GraphicsMMButton4Declaration](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml#graphicsmmbutton4declaration)]  
  
 [!code-csharp[timingbehaviors_snip#GraphicsMMButton4Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml.cs#graphicsmmbutton4handler)]
 [!code-vb[timingbehaviors_snip#GraphicsMMButton4Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_snip/visualbasic/animatethensetpropertyexample.xaml.vb#graphicsmmbutton4handler)]  
  
 <span data-ttu-id="6e979-126">Diese Technik funktioniert auch für nicht-Storyboard-Animationen.</span><span class="sxs-lookup"><span data-stu-id="6e979-126">This technique also works for non-storyboard animations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e979-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e979-127">See also</span></span>

- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A>
- <xref:System.Windows.Media.Animation.Storyboard.Remove%2A?displayProperty=nameWithType>
- <xref:System.Windows.Media.Animation.RemoveStoryboard>
- [<span data-ttu-id="6e979-128">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="6e979-128">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="6e979-129">Übersicht über die Verfahren zur Animation von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e979-129">Property Animation Techniques Overview</span></span>](property-animation-techniques-overview.md)
