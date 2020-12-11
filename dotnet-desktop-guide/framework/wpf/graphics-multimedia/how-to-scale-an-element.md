---
title: 'Gewusst wie: Skalieren eines Elements'
ms.date: 03/30/2017
helpviewer_keywords:
- scaling [WPF], elements
- graphics [WPF], scaling elements
ms.assetid: 18158d94-bbe7-4f6a-814e-84d27fa748bf
ms.openlocfilehash: 34d954f68747be9eedc0ef71634e0c18b411d260
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977312"
---
# <a name="how-to-scale-an-element"></a><span data-ttu-id="1fbf2-102">Gewusst wie: Skalieren eines Elements</span><span class="sxs-lookup"><span data-stu-id="1fbf2-102">How to: Scale an Element</span></span>
<span data-ttu-id="1fbf2-103">Dieses Beispiel zeigt, wie ein- <xref:System.Windows.Media.ScaleTransform> Element zum Skalieren eines Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-103">This example shows how to use a <xref:System.Windows.Media.ScaleTransform> to scale an element.</span></span>  
  
 <span data-ttu-id="1fbf2-104">Verwenden <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> Sie die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> , um die Größe des Elements mit dem angegebenen Faktor zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-104">Use the <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> and <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> properties to resize the element by the factor you specify.</span></span> <span data-ttu-id="1fbf2-105">Beispielsweise wird <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> das-Element mit dem Wert 1,5 auf 150 Prozent seiner ursprünglichen Breite gestreckt.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-105">For example, a <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> value of 1.5 stretches the element to 150 percent of its original width.</span></span> <span data-ttu-id="1fbf2-106"><xref:System.Windows.Media.ScaleTransform.ScaleY%2A>Der Wert 0,5 verkleinert die Höhe eines Elements um 50 Prozent.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-106">A <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> value of 0.5 shrinks the height of an element by 50 percent.</span></span>  
  
 <span data-ttu-id="1fbf2-107">Verwenden <xref:System.Windows.Media.ScaleTransform.CenterX%2A> Sie die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.ScaleTransform.CenterY%2A> , um den Punkt anzugeben, der die Mitte des Skalierungs Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-107">Use the <xref:System.Windows.Media.ScaleTransform.CenterX%2A> and <xref:System.Windows.Media.ScaleTransform.CenterY%2A> properties to specify the point that is the center of the scale operation.</span></span> <span data-ttu-id="1fbf2-108">Standardmäßig wird eine <xref:System.Windows.Media.ScaleTransform> am Punkt (0,0) zentriert, der der oberen linken Ecke des Rechtecks entspricht.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-108">By default, a <xref:System.Windows.Media.ScaleTransform> is centered at the point (0,0), which corresponds to the upper-left corner of the rectangle.</span></span> <span data-ttu-id="1fbf2-109">Dies hat den Effekt, dass das Element verschoben wird, und auch, dass es größer erscheint, denn wenn Sie ein anwenden <xref:System.Windows.Media.Transform> , ändern Sie den Koordinaten Bereich, in dem sich das Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-109">This has the effect of moving the element and also of making it appear larger, because when you apply a <xref:System.Windows.Media.Transform>, you change the coordinate space in which the object resides.</span></span>  
  
 <span data-ttu-id="1fbf2-110">Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.ScaleTransform> , um die Größe von 50 x 50 zu verdoppeln <xref:System.Windows.Shapes.Rectangle> .</span><span class="sxs-lookup"><span data-stu-id="1fbf2-110">The following example uses a <xref:System.Windows.Media.ScaleTransform> to double the size of a 50-by-50 <xref:System.Windows.Shapes.Rectangle>.</span></span> <span data-ttu-id="1fbf2-111">Der <xref:System.Windows.Media.ScaleTransform> hat den Wert 0 (Standard) für <xref:System.Windows.Media.ScaleTransform.CenterX%2A> und <xref:System.Windows.Media.ScaleTransform.CenterY%2A> .</span><span class="sxs-lookup"><span data-stu-id="1fbf2-111">The <xref:System.Windows.Media.ScaleTransform> has a value of 0 (the default) for both <xref:System.Windows.Media.ScaleTransform.CenterX%2A> and <xref:System.Windows.Media.ScaleTransform.CenterY%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1fbf2-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1fbf2-112">Example</span></span>  
 [!code-xaml[transformsSample#21](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/ScaleTransformExample.xaml#21)]  
  
 <span data-ttu-id="1fbf2-113">In der Regel legen Sie <xref:System.Windows.Media.ScaleTransform.CenterX%2A> und <xref:System.Windows.Media.ScaleTransform.CenterY%2A> auf den Mittelpunkt des Objekts fest, das skaliert wird: ( <xref:System.Windows.FrameworkElement.Width%2A> /2, <xref:System.Windows.FrameworkElement.Height%2A> /2).</span><span class="sxs-lookup"><span data-stu-id="1fbf2-113">Typically, you set <xref:System.Windows.Media.ScaleTransform.CenterX%2A> and <xref:System.Windows.Media.ScaleTransform.CenterY%2A> to the center of the object that is scaled: (<xref:System.Windows.FrameworkElement.Width%2A>/2, <xref:System.Windows.FrameworkElement.Height%2A>/2).</span></span>  
  
 <span data-ttu-id="1fbf2-114">Das folgende Beispiel zeigt eine andere <xref:System.Windows.Shapes.Rectangle> , die die Größe verdoppelt, jedoch den <xref:System.Windows.Media.ScaleTransform> Wert 25 für <xref:System.Windows.Media.ScaleTransform.CenterX%2A> und <xref:System.Windows.Media.ScaleTransform.CenterY%2A> , was der Mitte des Rechtecks entspricht.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-114">The following example shows another <xref:System.Windows.Shapes.Rectangle> that is doubled in size; however, this <xref:System.Windows.Media.ScaleTransform> has a value of 25 for both <xref:System.Windows.Media.ScaleTransform.CenterX%2A> and <xref:System.Windows.Media.ScaleTransform.CenterY%2A>, which corresponds to the center of the rectangle.</span></span>  
  
 [!code-xaml[transformsSample#22](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/ScaleTransformExample.xaml#22)]  
  
 <span data-ttu-id="1fbf2-115">Die folgende Abbildung zeigt den Unterschied zwischen den beiden <xref:System.Windows.Media.ScaleTransform> Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-115">The following illustration shows the difference between the two <xref:System.Windows.Media.ScaleTransform> operations.</span></span> <span data-ttu-id="1fbf2-116">Die gepunktete Linie stellt die Größe und die Position des Rechtecks vor der Skalierung dar.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-116">The dotted line shows the size and position of the rectangle before scaling.</span></span>  
  
 <span data-ttu-id="1fbf2-117">![2-fach-Skalierung mit unterschiedlichen Mittelpunkten](./media/wcpsdk-graphicsmm-scalecenter.gif "wcpsdk_graphicsmm_scalecenter")</span><span class="sxs-lookup"><span data-stu-id="1fbf2-117">![2x scales with different center points](./media/wcpsdk-graphicsmm-scalecenter.gif "wcpsdk_graphicsmm_scalecenter")</span></span>  
<span data-ttu-id="1fbf2-118">Zwei ScaleTransform-Vorgänge mit identischen ScaleX- und ScaleY-Werten aber unterschiedlichen Mittelpunkten</span><span class="sxs-lookup"><span data-stu-id="1fbf2-118">Two ScaleTransform operations with identical ScaleX and ScaleY values but different centers</span></span>  
  
 <span data-ttu-id="1fbf2-119">Das komplette Beispiel finden Sie unter [Beispiel für 2D-Transformationen](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).</span><span class="sxs-lookup"><span data-stu-id="1fbf2-119">For the complete sample, see [2D Transforms Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fbf2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fbf2-120">See also</span></span>

- <xref:System.Windows.Media.Transform>
- <xref:System.Windows.Media.ScaleTransform>
- [<span data-ttu-id="1fbf2-121">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="1fbf2-121">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="1fbf2-122">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="1fbf2-122">How-to Topics</span></span>](transformations-how-to-topics.md)
