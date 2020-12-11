---
title: Verwenden der globalen Transformation
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [Windows Forms], world transformation
- world transformation [Windows Forms], examples
ms.assetid: 1e717711-1361-448e-aa49-0f3ec43110c9
ms.openlocfilehash: f40d7e8cb814344365e8b88c2659751903b79d77
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975833"
---
# <a name="using-the-world-transformation"></a><span data-ttu-id="a46da-102">Verwenden der globalen Transformation</span><span class="sxs-lookup"><span data-stu-id="a46da-102">Using the World Transformation</span></span>
<span data-ttu-id="a46da-103">Die Welt Transformation ist eine Eigenschaft der- <xref:System.Drawing.Graphics> Klasse.</span><span class="sxs-lookup"><span data-stu-id="a46da-103">The world transformation is a property of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="a46da-104">Die Zahlen, die die globale Transformation angeben, werden in einem- <xref:System.Drawing.Drawing2D.Matrix> Objekt gespeichert, das eine 3 × 3-Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="a46da-104">The numbers that specify the world transformation are stored in a <xref:System.Drawing.Drawing2D.Matrix> object, which represents a 3×3 matrix.</span></span> <span data-ttu-id="a46da-105">Die <xref:System.Drawing.Drawing2D.Matrix> -Klasse und die- <xref:System.Drawing.Graphics> Klasse verfügen über mehrere Methoden zum Festlegen der Zahlen in der Transformationsmatrix der Welt.</span><span class="sxs-lookup"><span data-stu-id="a46da-105">The <xref:System.Drawing.Drawing2D.Matrix> and <xref:System.Drawing.Graphics> classes have several methods for setting the numbers in the world transformation matrix.</span></span>  
  
## <a name="different-types-of-transformations"></a><span data-ttu-id="a46da-106">Verschiedene Typen von Transformationen</span><span class="sxs-lookup"><span data-stu-id="a46da-106">Different Types of Transformations</span></span>  
 <span data-ttu-id="a46da-107">Im folgenden Beispiel erstellt der Code zunächst ein Rechteck mit 50 × 50 und legt es am Ursprung (0,0) ab.</span><span class="sxs-lookup"><span data-stu-id="a46da-107">In the following example, the code first creates a 50×50 rectangle and locates it at the origin (0, 0).</span></span> <span data-ttu-id="a46da-108">Der Ursprung befindet sich in der oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a46da-108">The origin is at the upper-left corner of the client area.</span></span>  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.MiscLegacyTopics#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#11)]  
  
 <span data-ttu-id="a46da-109">Der folgende Code wendet eine Skalierungs Transformation an, die das Rechteck um den Faktor 1,75 in der x-Richtung erweitert und das Rechteck um den Faktor 0,5 in der y-Richtung verkleinert:</span><span class="sxs-lookup"><span data-stu-id="a46da-109">The following code applies a scaling transformation that expands the rectangle by a factor of 1.75 in the x direction and shrinks the rectangle by a factor of 0.5 in the y direction:</span></span>  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#12)]
 [!code-vb[System.Drawing.MiscLegacyTopics#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#12)]  
  
 <span data-ttu-id="a46da-110">Das Ergebnis ist ein Rechteck, das in der x-Richtung länger und kürzer in der y-Richtung als die ursprüngliche ist.</span><span class="sxs-lookup"><span data-stu-id="a46da-110">The result is a rectangle that is longer in the x direction and shorter in the y direction than the original.</span></span>  
  
 <span data-ttu-id="a46da-111">Um das Rechteck zu drehen, anstatt es zu skalieren, verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="a46da-111">To rotate the rectangle instead of scaling it, use the following code:</span></span>  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#13](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#13)]
 [!code-vb[System.Drawing.MiscLegacyTopics#13](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#13)]  
  
 <span data-ttu-id="a46da-112">Verwenden Sie den folgenden Code, um das Rechteck zu übersetzen:</span><span class="sxs-lookup"><span data-stu-id="a46da-112">To translate the rectangle, use the following code:</span></span>  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#14](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#14)]
 [!code-vb[System.Drawing.MiscLegacyTopics#14](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#14)]  
  
## <a name="see-also"></a><span data-ttu-id="a46da-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a46da-113">See also</span></span>

- <xref:System.Drawing.Drawing2D.Matrix>
- [<span data-ttu-id="a46da-114">Koordinatensysteme und Transformationen</span><span class="sxs-lookup"><span data-stu-id="a46da-114">Coordinate Systems and Transformations</span></span>](coordinate-systems-and-transformations.md)
- [<span data-ttu-id="a46da-115">Verwenden von Transformationen in Managed GDI+</span><span class="sxs-lookup"><span data-stu-id="a46da-115">Using Transformations in Managed GDI+</span></span>](using-transformations-in-managed-gdi.md)
