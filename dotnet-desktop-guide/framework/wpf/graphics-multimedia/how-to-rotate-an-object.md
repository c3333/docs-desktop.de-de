---
title: 'Gewusst wie: Drehen eines Objekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], rotating objects [WPF]
- rotating objects [WPF]
ms.assetid: ee3466cd-e66f-4e8f-8a5a-71d77bc1e390
ms.openlocfilehash: e17d3b7b9986b477df198480129edaf4c139c6bc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977270"
---
# <a name="how-to-rotate-an-object"></a><span data-ttu-id="7e208-102">Gewusst wie: Drehen eines Objekts</span><span class="sxs-lookup"><span data-stu-id="7e208-102">How to: Rotate an Object</span></span>
<span data-ttu-id="7e208-103">Dieses Beispiel zeigt, wie ein Objekt gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="7e208-103">This example shows how to rotate an object.</span></span> <span data-ttu-id="7e208-104">Im Beispiel wird zunächst ein erstellt <xref:System.Windows.Media.RotateTransform> und dann der <xref:System.Windows.Media.RotateTransform.Angle%2A> in Grad angegeben.</span><span class="sxs-lookup"><span data-stu-id="7e208-104">The example first creates a <xref:System.Windows.Media.RotateTransform> and then specifies its <xref:System.Windows.Media.RotateTransform.Angle%2A> in degrees.</span></span>  
  
 <span data-ttu-id="7e208-105">Im folgenden Beispiel wird ein- <xref:System.Windows.Shapes.Polyline> Objekt um 45 Grad um die linke obere Ecke gedreht.</span><span class="sxs-lookup"><span data-stu-id="7e208-105">The following example rotates a <xref:System.Windows.Shapes.Polyline> object 45 degrees about its upper-left corner.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7e208-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7e208-106">Example</span></span>  
 [!code-xaml[Transforms_snip#RotatePolylineAboutTopLeft](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/RotateTransformExample.xaml#rotatepolylineabouttopleft)]  
  
 [!code-csharp[Transforms_Procedural_snip#RotatePolylineAboutTopLeft](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/RotateTransformExample.cs#rotatepolylineabouttopleft)]
 [!code-vb[Transforms_Procedural_snip#RotatePolylineAboutTopLeft](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/RotateTransformExample.vb#rotatepolylineabouttopleft)]  
  
 <span data-ttu-id="7e208-107">Die <xref:System.Windows.Media.RotateTransform.CenterX%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.RotateTransform.CenterY%2A> des- <xref:System.Windows.Media.RotateTransform> Objekts geben den Punkt an, an dem das Objekt gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="7e208-107">The <xref:System.Windows.Media.RotateTransform.CenterX%2A> and <xref:System.Windows.Media.RotateTransform.CenterY%2A> properties of the <xref:System.Windows.Media.RotateTransform> specify the point about which the object is rotated.</span></span> <span data-ttu-id="7e208-108">Dieser Mittelpunkt wird im Koordinatenraum des Elements ausgedrückt, das transformiert wird.</span><span class="sxs-lookup"><span data-stu-id="7e208-108">This center point is expressed in the coordinate space of the element that is transformed.</span></span> <span data-ttu-id="7e208-109">Standardmäßig wird die Drehung um den Punkt (0,0), die obere linke Ecke des zu transformierenden Objekts, vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="7e208-109">By default, the rotation is applied to (0,0), which is the upper-left corner of the object to transform.</span></span>  
  
 <span data-ttu-id="7e208-110">Im nächsten Beispiel wird ein- <xref:System.Windows.Shapes.Polyline> Objekt um 45 Grad im Uhrzeigersinn um den Punkt gedreht (25, 50).</span><span class="sxs-lookup"><span data-stu-id="7e208-110">The next example rotates a <xref:System.Windows.Shapes.Polyline> object clockwise 45 degrees about the point (25,50).</span></span>  
  
 [!code-xaml[Transforms_snip#RotatePolylineAboutCenter](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/RotateTransformExample.xaml#rotatepolylineaboutcenter)]  
  
 [!code-csharp[Transforms_Procedural_snip#RotatePolylineAboutCenter](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/RotateTransformExample.cs#rotatepolylineaboutcenter)]
 [!code-vb[Transforms_Procedural_snip#RotatePolylineAboutCenter](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/RotateTransformExample.vb#rotatepolylineaboutcenter)]  
  
 <span data-ttu-id="7e208-111">Die folgende Abbildung zeigt die Ergebnisse der Anwendung eines <xref:System.Windows.Media.Transform> auf die beiden-Objekte.</span><span class="sxs-lookup"><span data-stu-id="7e208-111">The following illustration shows the results of applying a <xref:System.Windows.Media.Transform> to the two objects.</span></span>  
  
 <span data-ttu-id="7e208-112">![45-Grad-Drehungen mit unterschiedlichen Mittelpunkten](./media/wcpsdk-graphicsmm-rotatetransform45degrees.gif "wcpsdk_graphicsmm_rotatetransform45degrees")</span><span class="sxs-lookup"><span data-stu-id="7e208-112">![45 degree rotations with different center points](./media/wcpsdk-graphicsmm-rotatetransform45degrees.gif "wcpsdk_graphicsmm_rotatetransform45degrees")</span></span>  
<span data-ttu-id="7e208-113">Zwei Objekte, die um unterschiedliche Drehpunkte um 45 Grad gedreht werden</span><span class="sxs-lookup"><span data-stu-id="7e208-113">Two objects that rotate 45 degrees from different rotational centers</span></span>  
  
 <span data-ttu-id="7e208-114">Das <xref:System.Windows.Shapes.Polyline> in den vorherigen Beispielen ist ein <xref:System.Windows.UIElement> .</span><span class="sxs-lookup"><span data-stu-id="7e208-114">The <xref:System.Windows.Shapes.Polyline> in the previous examples is a <xref:System.Windows.UIElement>.</span></span> <span data-ttu-id="7e208-115">Wenn Sie <xref:System.Windows.Media.Transform> auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft eines anwenden <xref:System.Windows.UIElement> , können Sie die-Eigenschaft verwenden, <xref:System.Windows.UIElement.RenderTransformOrigin%2A> um einen Ursprung für jeden anzugeben, <xref:System.Windows.Media.Transform> den Sie auf das Element anwenden.</span><span class="sxs-lookup"><span data-stu-id="7e208-115">When you apply a <xref:System.Windows.Media.Transform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property of a <xref:System.Windows.UIElement>, you can use the <xref:System.Windows.UIElement.RenderTransformOrigin%2A> property to specify an origin for every <xref:System.Windows.Media.Transform> that you apply to the element.</span></span> <span data-ttu-id="7e208-116">Da die- <xref:System.Windows.UIElement.RenderTransformOrigin%2A> Eigenschaft relative Koordinaten verwendet, können Sie eine Transformation auf den Mittelpunkt des Elements anwenden, auch wenn Sie Ihre Größe nicht kennen.</span><span class="sxs-lookup"><span data-stu-id="7e208-116">Because the <xref:System.Windows.UIElement.RenderTransformOrigin%2A> property uses relative coordinates, you can apply a transformation to the center of the element even if you do not know its size.</span></span> <span data-ttu-id="7e208-117">Weitere Informationen und ein Beispiel finden [Sie unter Angeben des Ursprungs einer Transformation mithilfe von relativen Werten](how-to-specify-the-origin-of-a-transform-by-using-relative-values.md).</span><span class="sxs-lookup"><span data-stu-id="7e208-117">For more information and for an example, see [Specify the Origin of a Transform by Using Relative Values](how-to-specify-the-origin-of-a-transform-by-using-relative-values.md).</span></span>  
  
 <span data-ttu-id="7e208-118">Das komplette Beispiel finden Sie unter [Beispiel für 2D-Transformationen](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).</span><span class="sxs-lookup"><span data-stu-id="7e208-118">For the complete sample, see [2D Transforms Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e208-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e208-119">See also</span></span>

- <xref:System.Windows.Media.Transform>
- [<span data-ttu-id="7e208-120">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="7e208-120">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="7e208-121">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="7e208-121">How-to Topics</span></span>](transformations-how-to-topics.md)
