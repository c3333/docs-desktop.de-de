---
title: 'Gewusst wie: Animieren von 3D-Übersetzungen'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], 3D translations
- 3D translations [WPF], animating
ms.assetid: d4eece1f-0cd2-4a2c-8370-293354c380e4
ms.openlocfilehash: 7d4fff9c74663bd220ad5d15a983bcb639621afd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975332"
---
# <a name="how-to-animate-3d-translations"></a><span data-ttu-id="e6144-102">Gewusst wie: Animieren von 3D-Übersetzungen</span><span class="sxs-lookup"><span data-stu-id="e6144-102">How to: Animate 3D Translations</span></span>
<span data-ttu-id="e6144-103">In diesem Thema wird veranschaulicht, wie Sie eine Übersetzungs Transformation für ein 3D-Modell animieren.</span><span class="sxs-lookup"><span data-stu-id="e6144-103">This topic demonstrates how to animate a translation transformation set on a 3D model.</span></span>  
  
 <span data-ttu-id="e6144-104">Der folgende Code zeigt die Anwendung eines- <xref:System.Windows.Media.Media3D.TranslateTransform3D> Objekts für die- <xref:System.Windows.Media.Media3D.Model3D.Transform%2A> Eigenschaft eines <xref:System.Windows.Media.Media3D.GeometryModel3D> .</span><span class="sxs-lookup"><span data-stu-id="e6144-104">The code below shows the application of a <xref:System.Windows.Media.Media3D.TranslateTransform3D> object to the <xref:System.Windows.Media.Media3D.Model3D.Transform%2A> property of a <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationinline1)]  
  
 <span data-ttu-id="e6144-105">Die- <xref:System.Windows.Media.Media3D.TranslateTransform3D.OffsetX%2A> Eigenschaft dieses- <xref:System.Windows.Media.Media3D.TranslateTransform3D> Objekts wird mithilfe des folgenden Codes animiert.</span><span class="sxs-lookup"><span data-stu-id="e6144-105">The <xref:System.Windows.Media.Media3D.TranslateTransform3D.OffsetX%2A> property of this <xref:System.Windows.Media.Media3D.TranslateTransform3D> object is animated using the code below.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationInline2](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationinline2)]  
  
## <a name="example"></a><span data-ttu-id="e6144-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e6144-106">Example</span></span>  
 <span data-ttu-id="e6144-107">Der folgende Code zeigt das gesamte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e6144-107">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="e6144-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6144-108">See also</span></span>

- [<span data-ttu-id="e6144-109">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="e6144-109">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="e6144-110">Erstellen einer 3D-Szene</span><span class="sxs-lookup"><span data-stu-id="e6144-110">Create a 3D Scene</span></span>](how-to-create-a-3-d-scene.md)
- [<span data-ttu-id="e6144-111">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="e6144-111">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="e6144-112">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="e6144-112">Transforms Overview</span></span>](transforms-overview.md)
