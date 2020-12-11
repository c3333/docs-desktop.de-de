---
title: Einschränken der Zeichenfläche in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- GDI+, clipping
- clipping [Windows Forms], using GDI+
- GDI+, restricting drawing surface
ms.assetid: 8b5f71d9-d2f0-4540-9c41-740f90fd4c26
ms.openlocfilehash: d0508166f905b45789ce638b03d0747dd6fa904e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976065"
---
# <a name="restricting-the-drawing-surface-in-gdi"></a><span data-ttu-id="b5f69-102">Einschränken der Zeichenfläche in GDI+</span><span class="sxs-lookup"><span data-stu-id="b5f69-102">Restricting the Drawing Surface in GDI+</span></span>
<span data-ttu-id="b5f69-103">Beim Clipping wird das Zeichnen auf ein bestimmtes Rechteck oder eine bestimmte Region eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="b5f69-103">Clipping involves restricting drawing to a certain rectangle or region.</span></span> <span data-ttu-id="b5f69-104">Die folgende Abbildung zeigt die Zeichenfolge "Hello", die auf einen herzförmigen Bereich zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="b5f69-104">The following illustration shows the string "Hello" clipped to a heart-shaped region.</span></span>  
  
 <span data-ttu-id="b5f69-105">![Eingeschränkte Zeichnungsoberfläche](./media/aboutgdip02-art30.gif "AboutGdip02_Art30")</span><span class="sxs-lookup"><span data-stu-id="b5f69-105">![Restricted Drawing Surface](./media/aboutgdip02-art30.gif "AboutGdip02_Art30")</span></span>  
  
## <a name="clipping-with-regions"></a><span data-ttu-id="b5f69-106">Clipping mit Regionen</span><span class="sxs-lookup"><span data-stu-id="b5f69-106">Clipping with Regions</span></span>  
 <span data-ttu-id="b5f69-107">Bereiche können aus Pfaden erstellt werden, und Pfade können die Gliederungen von Zeichen folgen enthalten, sodass Sie den Text für das Clipping verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b5f69-107">Regions can be constructed from paths, and paths can contain the outlines of strings, so you can use outlined text for clipping.</span></span> <span data-ttu-id="b5f69-108">Die folgende Abbildung zeigt einen Satz konzentrischer Ellipsen, die auf das Innere einer Text Zeichenfolge zugeschnitten sind.</span><span class="sxs-lookup"><span data-stu-id="b5f69-108">The following illustration shows a set of concentric ellipses clipped to the interior of a string of text.</span></span>  
  
 <span data-ttu-id="b5f69-109">![Eingeschränkte Zeichnungsoberfläche](./media/aboutgdip02-art31.gif "AboutGdip02_Art31")</span><span class="sxs-lookup"><span data-stu-id="b5f69-109">![Restricted Drawing Surface](./media/aboutgdip02-art31.gif "AboutGdip02_Art31")</span></span>  
  
 <span data-ttu-id="b5f69-110">Um mit Clipping zu zeichnen, erstellen Sie ein <xref:System.Drawing.Graphics> -Objekt, legen Sie seine <xref:System.Drawing.Graphics.Clip%2A> -Eigenschaft fest, und rufen Sie dann die Zeichnungs Methoden desselben <xref:System.Drawing.Graphics> Objekts auf:</span><span class="sxs-lookup"><span data-stu-id="b5f69-110">To draw with clipping, create a <xref:System.Drawing.Graphics> object, set its <xref:System.Drawing.Graphics.Clip%2A> property, and then call the drawing methods of that same <xref:System.Drawing.Graphics> object:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#91](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#91)]
 [!code-vb[LinesCurvesAndShapes#91](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#91)]  
  
## <a name="see-also"></a><span data-ttu-id="b5f69-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5f69-111">See also</span></span>

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Region?displayProperty=nameWithType>
- [<span data-ttu-id="b5f69-112">Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="b5f69-112">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="b5f69-113">Verwenden von Bereichen</span><span class="sxs-lookup"><span data-stu-id="b5f69-113">Using Regions</span></span>](using-regions.md)
