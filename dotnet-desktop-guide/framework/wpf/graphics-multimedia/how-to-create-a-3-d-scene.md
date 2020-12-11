---
title: 'Gewusst wie: Erstellen einer 3D-Szene'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- scenes [WPF], 3D
- 3D scenes
ms.assetid: adb4a598-71a2-4dd5-b677-ea3fc11b78b2
ms.openlocfilehash: 36453894e06e7b59f339c21713449140c17f6851
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977622"
---
# <a name="how-to-create-a-3d-scene"></a><span data-ttu-id="3d0b0-102">Gewusst wie: Erstellen einer 3D-Szene</span><span class="sxs-lookup"><span data-stu-id="3d0b0-102">How to: Create a 3D Scene</span></span>
<span data-ttu-id="3d0b0-103">Dieses Beispiel zeigt, wie ein 3D-Objekt erstellt wird, das wie ein Papierblatt aussieht, das gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="3d0b0-103">This example shows how to create a 3D object that looks like a flat sheet of paper which has been rotated.</span></span> <span data-ttu-id="3d0b0-104">Eine <xref:System.Windows.Controls.Viewport3D> zusammen mit den folgenden Komponenten wird verwendet, um diese einfache 3D-Szene zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="3d0b0-104">A <xref:System.Windows.Controls.Viewport3D> along with the following components are used to create this simple 3D scene:</span></span>  
  
- <span data-ttu-id="3d0b0-105">Eine Kamera wird mit einem erstellt <xref:System.Windows.Media.Media3D.PerspectiveCamera> .</span><span class="sxs-lookup"><span data-stu-id="3d0b0-105">A camera is created using a <xref:System.Windows.Media.Media3D.PerspectiveCamera>.</span></span> <span data-ttu-id="3d0b0-106">Die Kamera gibt an, welcher Teil der 3D-Szene angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d0b0-106">The camera specifies what part of the 3D scene is viewable.</span></span>  
  
- <span data-ttu-id="3d0b0-107">Ein Mesh wird erstellt, um die Form des 3D-Objekts (Blatt des Papiers) mithilfe der- <xref:System.Windows.Media.Media3D.GeometryModel3D.Geometry%2A> Eigenschaft von anzugeben <xref:System.Windows.Media.Media3D.GeometryModel3D> .</span><span class="sxs-lookup"><span data-stu-id="3d0b0-107">A mesh is created to specify the shape of 3D object (sheet of paper) using the <xref:System.Windows.Media.Media3D.GeometryModel3D.Geometry%2A> property of <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span></span>  
  
- <span data-ttu-id="3d0b0-108">Mithilfe der-Eigenschaft von wird ein Material angegeben, das auf der Oberfläche des-Objekts (linearer Farbverlauf in diesem Beispiel) angezeigt werden soll <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> <xref:System.Windows.Media.Media3D.GeometryModel3D> .</span><span class="sxs-lookup"><span data-stu-id="3d0b0-108">A material is specified to be displayed on the surface of the object (linear gradient in this sample) using the <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> property of <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span></span>  
  
- <span data-ttu-id="3d0b0-109">Ein Licht wird erstellt, um für das-Objekt zu glänzen, das verwendet <xref:System.Windows.Media.Media3D.DirectionalLight> .</span><span class="sxs-lookup"><span data-stu-id="3d0b0-109">A light is created to shine on the object using <xref:System.Windows.Media.Media3D.DirectionalLight>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3d0b0-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3d0b0-110">Example</span></span>  
 <span data-ttu-id="3d0b0-111">Der folgende Code zeigt, wie Sie eine 3D-Szene in XAML erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d0b0-111">The code below shows how to create a 3D scene in XAML.</span></span>  
  
 [!code-xaml[3DGallery_snip#Basic3DShapeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/Basic3DShapeExample.xaml#basic3dshapeexamplewholepage)]  
  
## <a name="example"></a><span data-ttu-id="3d0b0-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3d0b0-112">Example</span></span>  
 <span data-ttu-id="3d0b0-113">Der folgende Code zeigt, wie die gleiche 3D-Szene in prozeduralem Code erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3d0b0-113">The code below shows how to create the same 3D scene in procedural code.</span></span>  
  
 [!code-csharp[3DGallery_procedural_snip#Basic3DShapeCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/Basic3DShapeExample.cs#basic3dshapecodeexamplewholepage)]
 [!code-vb[3DGallery_procedural_snip#Basic3DShapeCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/3DGallery_procedural_snip/visualbasic/basic3dshapeexample.vb#basic3dshapecodeexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="3d0b0-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d0b0-114">See also</span></span>

- [<span data-ttu-id="3d0b0-115">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="3d0b0-115">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
