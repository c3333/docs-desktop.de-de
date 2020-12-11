---
title: 'Gewusst wie: Transformieren der Skalierung eines 3D-Modells'
ms.date: 03/30/2017
helpviewer_keywords:
- scaling [WPF], 3D objects
- 3D objects [WPF], scaling
ms.assetid: f3fdfe33-f7dc-44b0-84a5-e43b89947f35
ms.openlocfilehash: be41a0e10929912c1b54bf7140d743d9453199bf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976859"
---
# <a name="how-to-transform-the-scale-of-a-3d-model"></a><span data-ttu-id="61404-102">Gewusst wie: Transformieren der Skalierung eines 3D-Modells</span><span class="sxs-lookup"><span data-stu-id="61404-102">How to: Transform the Scale of a 3D Model</span></span>
<span data-ttu-id="61404-103">In diesem Beispiel wird gezeigt, wie ein 3D-Objekt skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="61404-103">This example shows how to scale a 3D object.</span></span> <span data-ttu-id="61404-104">Verwenden Sie zum Skalieren eines 3D-Objekts einen <xref:System.Windows.Media.Media3D.ScaleTransform3D> .</span><span class="sxs-lookup"><span data-stu-id="61404-104">To scale a 3D object, use a <xref:System.Windows.Media.Media3D.ScaleTransform3D>.</span></span> <span data-ttu-id="61404-105">Die <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A> <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A> Eigenschaften, und <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleZ%2A> ändern die Größe des-Elements mit dem von Ihnen angegebenen Faktor.</span><span class="sxs-lookup"><span data-stu-id="61404-105">The <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A>, <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A>, and <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleZ%2A> properties resize the element by the factor you specify.</span></span> <span data-ttu-id="61404-106">Beispielsweise wird ein <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A> Objekt mit dem Wert 1,5 auf 150 Prozent seiner ursprünglichen Breite gestreckt.</span><span class="sxs-lookup"><span data-stu-id="61404-106">For example, a <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A> value of 1.5 stretches an object to 150 percent of its original width.</span></span> <span data-ttu-id="61404-107"><xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A>Der Wert 0,5 verkleinert die Höhe eines Objekts um 50 Prozent.</span><span class="sxs-lookup"><span data-stu-id="61404-107">A <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A> value of 0.5 shrinks the height of an object by 50 percent.</span></span> <span data-ttu-id="61404-108">Der folgende Code zeigt die Verwendung <xref:System.Windows.Media.Media3D.ScaleTransform3D> von als Transformation für eine <xref:System.Windows.Media.Media3D.GeometryModel3D> .</span><span class="sxs-lookup"><span data-stu-id="61404-108">The code below shows using a <xref:System.Windows.Media.Media3D.ScaleTransform3D> as the transform for a <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span></span>  
  
 [!code-xaml[3DGallery_snip#ScaleTransform3DExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ScaleTransform3DExample.xaml#scaletransform3dexampleinline1)]  
  
## <a name="example"></a><span data-ttu-id="61404-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="61404-109">Example</span></span>  
 <span data-ttu-id="61404-110">Der folgende Code zeigt das gesamte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="61404-110">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[3DGallery_snip#ScaleTransform3DExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ScaleTransform3DExample.xaml#scaletransform3dexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="61404-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61404-111">See also</span></span>

- [<span data-ttu-id="61404-112">Animieren von 3D-Translationen</span><span class="sxs-lookup"><span data-stu-id="61404-112">Animate 3D Translations</span></span>](how-to-animate-3-d-translations.md)
- [<span data-ttu-id="61404-113">Erstellen einer 3D-Szene</span><span class="sxs-lookup"><span data-stu-id="61404-113">Create a 3D Scene</span></span>](how-to-create-a-3-d-scene.md)
- [<span data-ttu-id="61404-114">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="61404-114">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
