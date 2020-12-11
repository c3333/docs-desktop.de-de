---
title: 'Gewusst wie: Anwenden einer Transformation auf ein Element beim Auftreten eines Ereignisses'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], transformations as event responses
- properties [WPF], LayoutTransform
- transformations as event responses [WPF]
- properties [WPF], RenderTransform
- LayoutTransform property [WPF]
ms.assetid: 71e4327e-ca57-444c-a3cf-09fb381491a0
ms.openlocfilehash: 8f04db274432c0e89c6839bef825976c8a2f853c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975318"
---
# <a name="how-to-apply-a-transform-to-an-element-when-an-event-occurs"></a><span data-ttu-id="bc147-102">Gewusst wie: Anwenden einer Transformation auf ein Element beim Auftreten eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="bc147-102">How to: Apply a Transform to an Element When an Event Occurs</span></span>
<span data-ttu-id="bc147-103">Dieses Beispiel zeigt, wie ein-Ereignis angewendet wird, <xref:System.Windows.Media.ScaleTransform> Wenn ein Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="bc147-103">This example shows how to apply a <xref:System.Windows.Media.ScaleTransform> when an event occurs.</span></span> <span data-ttu-id="bc147-104">Mithilfe des hier dargestellten Konzepts können Sie auch andere Transformationstypen anwenden.</span><span class="sxs-lookup"><span data-stu-id="bc147-104">The concept that is shown here is the same that you use for applying other types of transformations.</span></span> <span data-ttu-id="bc147-105">Weitere Informationen zu den verfügbaren Transformations Typen finden Sie in der <xref:System.Windows.Media.Transform> [Übersicht](transforms-overview.md)über Klassen oder Transformationen.</span><span class="sxs-lookup"><span data-stu-id="bc147-105">For more information about the available types of transformations, see the <xref:System.Windows.Media.Transform> class or [Transforms Overview](transforms-overview.md).</span></span>  
  
 <span data-ttu-id="bc147-106">Sie können mit einem der folgenden beiden Verfahren eine Transformation auf ein Element anwenden:</span><span class="sxs-lookup"><span data-stu-id="bc147-106">You can apply a transform to an element in either of these two ways:</span></span>  
  
- <span data-ttu-id="bc147-107">Wenn sich die Transformation *nicht* auf das Layout auswirken soll, verwenden Sie die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft des-Elements.</span><span class="sxs-lookup"><span data-stu-id="bc147-107">If you do *not* want the transform to affect layout, use the <xref:System.Windows.UIElement.RenderTransform%2A> property of the element.</span></span>  
  
- <span data-ttu-id="bc147-108">Wenn sich die Transformation auf das Layout auswirken soll, verwenden Sie die- <xref:System.Windows.FrameworkElement.LayoutTransform%2A> Eigenschaft des-Elements.</span><span class="sxs-lookup"><span data-stu-id="bc147-108">If you do want the transform to affect layout, use the <xref:System.Windows.FrameworkElement.LayoutTransform%2A> property of the element.</span></span>  
  
 <span data-ttu-id="bc147-109">Im folgenden Beispiel wird ein <xref:System.Windows.Media.ScaleTransform> auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft einer Schaltfläche angewendet.</span><span class="sxs-lookup"><span data-stu-id="bc147-109">The following example applies a <xref:System.Windows.Media.ScaleTransform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property of a button.</span></span> <span data-ttu-id="bc147-110">Wenn die Maus über die Schaltfläche bewegt wird, <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> werden die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> des <xref:System.Windows.Media.ScaleTransform> auf festgelegt `2` , wodurch die Schaltfläche vergrößert wird.</span><span class="sxs-lookup"><span data-stu-id="bc147-110">When the mouse moves over the button, the <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> and <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> properties of the <xref:System.Windows.Media.ScaleTransform> are set to `2`, which causes the button to become larger.</span></span> <span data-ttu-id="bc147-111">Wenn der Mauszeiger von der Schaltfläche bewegt wird <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> und <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> auf festgelegt `1` ist, wird die Schaltfläche auf Ihre ursprüngliche Größe zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="bc147-111">When the mouse moves off the button, <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> and <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> are set to `1`, which causes the button to return to its original size.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bc147-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bc147-112">Example</span></span>  
 [!code-xaml[ButtonTransform#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ButtonTransform/CSharp/ButtonTransformExample.xaml#1)]  
  
 [!code-csharp[ButtonTransform#1cb](~/samples/snippets/csharp/VS_Snippets_Wpf/ButtonTransform/CSharp/ButtonTransformExample.xaml.cs#1cb)]
 [!code-vb[ButtonTransform#1cb](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ButtonTransform/VisualBasic/ButtonTransformExample.xaml.vb#1cb)]  
  
## <a name="see-also"></a><span data-ttu-id="bc147-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc147-113">See also</span></span>

- <xref:System.Windows.Media.Transform>
- <xref:System.Windows.Media.ScaleTransform>
- [<span data-ttu-id="bc147-114">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="bc147-114">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="bc147-115">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="bc147-115">How-to Topics</span></span>](transformations-how-to-topics.md)
- [<span data-ttu-id="bc147-116">Übersicht über Routingereignisse</span><span class="sxs-lookup"><span data-stu-id="bc147-116">Routed Events Overview</span></span>](../advanced/routed-events-overview.md)
