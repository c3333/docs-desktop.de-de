---
title: 'Gewusst wie: Anwenden von Material auf die Vorder-und Rückseite eines 3D-Objekts'
ms.date: 03/30/2017
helpviewer_keywords:
- 3D objects [WPF], applying Material class
- Material class [WPF], applying to both sides of 3D object
- classes [WPF], Material
ms.assetid: d93c8ad6-4939-4d29-9544-4d16d98093c1
ms.openlocfilehash: 5c24879d97e7857fb07fcef4a9ba8efa901e4a39
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975315"
---
# <a name="how-to-apply-material-to-the-front-and-back-of-a-3d-object"></a><span data-ttu-id="e233d-102">Gewusst wie: Anwenden von Material auf die Vorder-und Rückseite eines 3D-Objekts</span><span class="sxs-lookup"><span data-stu-id="e233d-102">How to: Apply Material to the Front and Back of a 3D Object</span></span>
<span data-ttu-id="e233d-103">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Media.Media3D.Material> auf die Vorder-und Rückseite eines 3D-Objekts angewendet und das-Objekt animiert wird, um beide Seiten des-Objekts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e233d-103">The following example shows how to apply a <xref:System.Windows.Media.Media3D.Material> to the front and back of a 3D object and animate the object to show both sides of the object.</span></span> <span data-ttu-id="e233d-104">Die <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> -Eigenschaft eines <xref:System.Windows.Media.Media3D.GeometryModel3D> -Objekts wird verwendet, um ein rotes <xref:System.Windows.Media.Brush> auf die Vorderseite des-Objekts anzuwenden, und die- <xref:System.Windows.Media.Media3D.GeometryModel3D.BackMaterial%2A> Eigenschaft von <xref:System.Windows.Media.Media3D.GeometryModel3D> wird verwendet, um einen blauen <xref:System.Windows.Media.Brush> auf die Rückseite des-Objekts anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="e233d-104">The <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> property of a <xref:System.Windows.Media.Media3D.GeometryModel3D> is used to apply a red <xref:System.Windows.Media.Brush> to the front side of the object and the <xref:System.Windows.Media.Media3D.GeometryModel3D.BackMaterial%2A> property of the <xref:System.Windows.Media.Media3D.GeometryModel3D> is used to apply a blue <xref:System.Windows.Media.Brush> to the back side of the object.</span></span> <span data-ttu-id="e233d-105">Der folgende Code zeigt die Anwendung der Materialien für das-Objekt:</span><span class="sxs-lookup"><span data-stu-id="e233d-105">The code below shows the application of the materials to the object:</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#BackMaterialAnimationExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/BackMaterialAnimationExample.xaml#backmaterialanimationexampleinline1)]  
  
## <a name="example"></a><span data-ttu-id="e233d-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e233d-106">Example</span></span>  
 <span data-ttu-id="e233d-107">Der folgende Code zeigt das gesamte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e233d-107">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#BackMaterialAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/BackMaterialAnimationExample.xaml#backmaterialanimationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="e233d-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e233d-108">See also</span></span>

- [<span data-ttu-id="e233d-109">Erstellen einer 3D-Szene</span><span class="sxs-lookup"><span data-stu-id="e233d-109">Create a 3D Scene</span></span>](how-to-create-a-3-d-scene.md)
- [<span data-ttu-id="e233d-110">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="e233d-110">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="e233d-111">Animieren von Materialeigenschaften in einer 3D-Szene</span><span class="sxs-lookup"><span data-stu-id="e233d-111">Animate Material Properties in a 3D Scene</span></span>](how-to-animate-material-properties-in-a-3-d-scene.md)
- [<span data-ttu-id="e233d-112">Anwenden von selbstleuchtendem Material auf ein 3D-Objekt</span><span class="sxs-lookup"><span data-stu-id="e233d-112">Apply Emissive Material to a 3D Object</span></span>](how-to-apply-emissive-material-to-a-3-d-object.md)
