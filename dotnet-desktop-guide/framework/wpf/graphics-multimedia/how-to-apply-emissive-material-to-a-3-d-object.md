---
title: 'Gewusst wie: Anwenden von emissive Material auf ein 3D-Objekt'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- EmissiveMaterial [WPF], applying to 3D objects
- 3D objects [WPF], applying EmissiveMaterial
ms.assetid: fd442cc2-5adc-487a-ba70-e45ed54bb3b4
ms.openlocfilehash: bf32b41ec2410c01ad137ec0ca9311f7c2b70061
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977768"
---
# <a name="how-to-apply-emissive-material-to-a-3d-object"></a><span data-ttu-id="cba1c-102">Gewusst wie: Anwenden von emissive Material auf ein 3D-Objekt</span><span class="sxs-lookup"><span data-stu-id="cba1c-102">How to: Apply Emissive Material to a 3D Object</span></span>
<span data-ttu-id="cba1c-103">Im folgenden Beispiel wird gezeigt, wie verwendet wird, <xref:System.Windows.Media.Media3D.EmissiveMaterial> um einem vorhandenen Material, das der Farbe des EmissiveMaterial-Pinsels entspricht, Farben hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cba1c-103">The following example shows how to use <xref:System.Windows.Media.Media3D.EmissiveMaterial> to add color to an existing Material equal to the color of the EmissiveMaterial's brush.</span></span> <span data-ttu-id="cba1c-104">Der folgende Code zeigt <xref:System.Windows.Media.Media3D.DiffuseMaterial> und <xref:System.Windows.Media.Media3D.EmissiveMaterial> wird in Kombination angewendet, um der Darstellung von DiffuseMaterial blau hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cba1c-104">The code below shows <xref:System.Windows.Media.Media3D.DiffuseMaterial> and <xref:System.Windows.Media.Media3D.EmissiveMaterial> applied in combination to add blue to the DiffuseMaterial's appearance.</span></span>  
  
 [!code-xaml[3DGallery_snip#EmmisiveMaterialAnimationExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/EmissiveMaterialExample.xaml#emmisivematerialanimationexampleinline1)]  
  
 <span data-ttu-id="cba1c-105">In prozeduralem Code:</span><span class="sxs-lookup"><span data-stu-id="cba1c-105">In procedural code:</span></span>  
  
 [!code-csharp[3DGallery_procedural_snip#EmissiveMaterialCodeExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/EmissiveMaterialExample.cs#emissivematerialcodeexampleinline1)]
 [!code-vb[3DGallery_procedural_snip#EmissiveMaterialCodeExampleInline1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/3DGallery_procedural_snip/visualbasic/emissivematerialexample.vb#emissivematerialcodeexampleinline1)]  
  
## <a name="example"></a><span data-ttu-id="cba1c-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cba1c-106">Example</span></span>  
 <span data-ttu-id="cba1c-107">Der folgende Code zeigt das gesamte Beispiel in XAML.</span><span class="sxs-lookup"><span data-stu-id="cba1c-107">The following code shows the entire sample in XAML.</span></span>  
  
 [!code-xaml[3DGallery_snip#EmissiveMaterialExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/EmissiveMaterialExample.xaml#emissivematerialexamplewholepage)]  
  
## <a name="example"></a><span data-ttu-id="cba1c-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cba1c-108">Example</span></span>  
 <span data-ttu-id="cba1c-109">Im folgenden finden Sie das gesamte Beispiel in prozeduralem Code.</span><span class="sxs-lookup"><span data-stu-id="cba1c-109">Below is the entire sample in procedural code.</span></span>  
  
 [!code-csharp[3DGallery_procedural_snip#EmissiveMaterialCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/EmissiveMaterialExample.cs#emissivematerialcodeexamplewholepage)]
 [!code-vb[3DGallery_procedural_snip#EmissiveMaterialCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/3DGallery_procedural_snip/visualbasic/emissivematerialexample.vb#emissivematerialcodeexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="cba1c-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cba1c-110">See also</span></span>

- [<span data-ttu-id="cba1c-111">Erstellen einer 3D-Szene</span><span class="sxs-lookup"><span data-stu-id="cba1c-111">Create a 3D Scene</span></span>](how-to-create-a-3-d-scene.md)
- [<span data-ttu-id="cba1c-112">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="cba1c-112">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="cba1c-113">Animieren von Materialeigenschaften in einer 3D-Szene</span><span class="sxs-lookup"><span data-stu-id="cba1c-113">Animate Material Properties in a 3D Scene</span></span>](how-to-animate-material-properties-in-a-3-d-scene.md)
- [<span data-ttu-id="cba1c-114">Anwenden von Material auf die Vorder- und Rückseite eines 3D-Objekts</span><span class="sxs-lookup"><span data-stu-id="cba1c-114">Apply Material to the Front and Back of a 3D Object</span></span>](how-to-apply-material-to-the-front-and-back-of-a-3-d-object.md)
