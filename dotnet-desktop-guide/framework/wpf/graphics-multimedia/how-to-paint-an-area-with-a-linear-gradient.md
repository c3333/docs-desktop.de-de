---
title: 'Gewusst wie: Zeichnen eines Bereichs mit einem linearen Farbverlauf'
ms.date: 03/30/2017
helpviewer_keywords:
- linear gradients [WPF], painting with
- brushes [WPF], painting with linear gradients
- painting [WPF], with linear gradients
ms.assetid: 00e0cd04-48c0-4ec5-850e-d321beb37a34
ms.openlocfilehash: 76c491632911c48db34d932ba3895278591378a5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976542"
---
# <a name="how-to-paint-an-area-with-a-linear-gradient"></a><span data-ttu-id="7ee4c-102">Gewusst wie: Zeichnen eines Bereichs mit einem linearen Farbverlauf</span><span class="sxs-lookup"><span data-stu-id="7ee4c-102">How to: Paint an Area with a Linear Gradient</span></span>
<span data-ttu-id="7ee4c-103">In diesem Beispiel wird gezeigt, wie die-Klasse verwendet wird <xref:System.Windows.Media.LinearGradientBrush> , um einen Bereich mit einem linearen Farbverlauf zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-103">This example shows how to use the <xref:System.Windows.Media.LinearGradientBrush> class to paint an area with a linear gradient.</span></span> <span data-ttu-id="7ee4c-104">Im folgenden Beispiel <xref:System.Windows.Shapes.Shape.Fill%2A> wird der eines <xref:System.Windows.Shapes.Rectangle> mit einem diagonalen linearen Farbverlauf gezeichnet, der von gelb zu rot zu blau in Kalk grün übergeht.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-104">In the following example, the <xref:System.Windows.Shapes.Shape.Fill%2A> of a <xref:System.Windows.Shapes.Rectangle> is painted with a diagonal linear gradient that transitions from yellow to red to blue to lime green.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7ee4c-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7ee4c-105">Example</span></span>  
 [!code-xaml[GradientBrushExamples_snip#DiagonalGradient1XAML](~/samples/snippets/xaml/VS_Snippets_Wpf/GradientBrushExamples_snip/XAML/LinearGradientBrushExample.xaml#diagonalgradient1xaml)]  
  
 [!code-csharp[GradientBrushExamples_snip#DiagonalGradient1CSharp](~/samples/snippets/csharp/VS_Snippets_Wpf/GradientBrushExamples_snip/CSharp/LinearGradientBrushExample.cs#diagonalgradient1csharp)]  
  
 <span data-ttu-id="7ee4c-106">Die folgende Abbildung zeigt den im vorherigen Beispiel erstellten Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-106">The following illustration shows the gradient created by the previous example.</span></span>  
  
 <span data-ttu-id="7ee4c-107">![Diagonaler, linearer Farbverlauf](./media/graphicsmm-diagonallgb.jpg "graphicsmm_DiagonalLGB")</span><span class="sxs-lookup"><span data-stu-id="7ee4c-107">![Diagonal linear gradient](./media/graphicsmm-diagonallgb.jpg "graphicsmm_DiagonalLGB")</span></span>  
  
 <span data-ttu-id="7ee4c-108">Um einen horizontalen linearen Farbverlauf zu erstellen, <xref:System.Windows.Media.LinearGradientBrush.StartPoint%2A> ändern <xref:System.Windows.Media.LinearGradientBrush.EndPoint%2A> Sie und von <xref:System.Windows.Media.LinearGradientBrush> in (0,0) und (1, 0,5).</span><span class="sxs-lookup"><span data-stu-id="7ee4c-108">To create a horizontal linear gradient, change the <xref:System.Windows.Media.LinearGradientBrush.StartPoint%2A> and <xref:System.Windows.Media.LinearGradientBrush.EndPoint%2A> of the <xref:System.Windows.Media.LinearGradientBrush> to (0,0.5) and (1,0.5).</span></span> <span data-ttu-id="7ee4c-109">Im folgenden Beispiel <xref:System.Windows.Shapes.Rectangle> wird ein mit einem horizontalen linearen Farbverlauf gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-109">In the following example, a <xref:System.Windows.Shapes.Rectangle> is painted with a horizontal linear gradient.</span></span>  
  
 [!code-xaml[GradientBrushExamples_snip#HorizontalGradient1XAML](~/samples/snippets/xaml/VS_Snippets_Wpf/GradientBrushExamples_snip/XAML/LinearGradientBrushExample.xaml#horizontalgradient1xaml)]  
  
 [!code-csharp[GradientBrushExamples_snip#HorizontalGradient1CSharp](~/samples/snippets/csharp/VS_Snippets_Wpf/GradientBrushExamples_snip/CSharp/LinearGradientBrushExample.cs#horizontalgradient1csharp)]  
  
 <span data-ttu-id="7ee4c-110">Die folgende Abbildung zeigt den im vorherigen Beispiel erstellten Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-110">The following illustration shows the gradient created by the previous example.</span></span>  
  
 <span data-ttu-id="7ee4c-111">![Ein horizontaler, linearer Farbverlauf](./media/graphicsmm-horizontallgb.jpg "graphicsmm_HorizontalLGB")</span><span class="sxs-lookup"><span data-stu-id="7ee4c-111">![A horizontal linear gradient](./media/graphicsmm-horizontallgb.jpg "graphicsmm_HorizontalLGB")</span></span>  
  
 <span data-ttu-id="7ee4c-112">Um einen vertikalen linearen Farbverlauf zu erstellen, <xref:System.Windows.Media.LinearGradientBrush.StartPoint%2A> ändern <xref:System.Windows.Media.LinearGradientBrush.EndPoint%2A> Sie und von <xref:System.Windows.Media.LinearGradientBrush> in (0,5, 0) und (0,5, 1).</span><span class="sxs-lookup"><span data-stu-id="7ee4c-112">To create a vertical linear gradient, change the <xref:System.Windows.Media.LinearGradientBrush.StartPoint%2A> and <xref:System.Windows.Media.LinearGradientBrush.EndPoint%2A> of the <xref:System.Windows.Media.LinearGradientBrush> to (0.5,0) and (0.5,1).</span></span> <span data-ttu-id="7ee4c-113">Im folgenden Beispiel <xref:System.Windows.Shapes.Rectangle> wird ein mit einem vertikalen linearen Farbverlauf gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-113">In the following example, a <xref:System.Windows.Shapes.Rectangle> is painted with a vertical linear gradient.</span></span>  
  
 [!code-xaml[GradientBrushExamples_snip#VerticalGradient1XAML](~/samples/snippets/xaml/VS_Snippets_Wpf/GradientBrushExamples_snip/XAML/LinearGradientBrushExample.xaml#verticalgradient1xaml)]  
  
 [!code-csharp[GradientBrushExamples_snip#VerticalGradient1CSharp](~/samples/snippets/csharp/VS_Snippets_Wpf/GradientBrushExamples_snip/CSharp/LinearGradientBrushExample.cs#verticalgradient1csharp)]  
  
 <span data-ttu-id="7ee4c-114">Die folgende Abbildung zeigt den im vorherigen Beispiel erstellten Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-114">The following illustration shows the gradient created by the previous example.</span></span>  
  
 <span data-ttu-id="7ee4c-115">![Vertikaler, linearer Farbverlauf](./media/graphicsmm-verticallgb.jpg "graphicsmm_VerticalLGB")</span><span class="sxs-lookup"><span data-stu-id="7ee4c-115">![Vertical linear gradient](./media/graphicsmm-verticallgb.jpg "graphicsmm_VerticalLGB")</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7ee4c-116">In den Beispielen in diesem Thema wird das Standard Koordinatensystem zum Festlegen von Startpunkten und Endpunkten verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-116">The examples in this topic use the default coordinate system for setting start points and end points.</span></span> <span data-ttu-id="7ee4c-117">Das Standard Koordinatensystem ist relativ zu einem umgebenden Feld: 0 gibt 0 Prozent des umgebenden Felds an, und 1 gibt 100 Prozent des umgebenden Felds an.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-117">The default coordinate system is relative to a bounding box: 0 indicates 0 percent of the bounding box, and 1 indicates 100 percent of the bounding box.</span></span> <span data-ttu-id="7ee4c-118">Sie können dieses Koordinatensystem ändern, indem Sie die- <xref:System.Windows.Media.GradientBrush.MappingMode%2A> Eigenschaft auf den Wert festlegen <xref:System.Windows.Media.BrushMappingMode.Absolute?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="7ee4c-118">You can change this coordinate system by setting the <xref:System.Windows.Media.GradientBrush.MappingMode%2A> property to the value <xref:System.Windows.Media.BrushMappingMode.Absolute?displayProperty=nameWithType>.</span></span> <span data-ttu-id="7ee4c-119">Ein absolutes Koordinatensystem ist nicht relativ zu einem umgebenden Feld.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-119">An absolute coordinate system is not relative to a bounding box.</span></span> <span data-ttu-id="7ee4c-120">Werte werden direkt im lokalen Raum interpretiert.</span><span class="sxs-lookup"><span data-stu-id="7ee4c-120">Values are interpreted directly in local space.</span></span>  
  
 <span data-ttu-id="7ee4c-121">Weitere Beispiele finden Sie unter [Beispiel für Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes).</span><span class="sxs-lookup"><span data-stu-id="7ee4c-121">For additional examples, see [Brushes Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes).</span></span> <span data-ttu-id="7ee4c-122">Weitere Informationen zu Farbverläufen und anderen Pinseltypen finden Sie unter Übersicht über das Zeichnen [mit voll Tonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7ee4c-122">For more information about gradients and other types of brushes, see [Painting with Solid Colors and Gradients Overview](painting-with-solid-colors-and-gradients-overview.md).</span></span>
