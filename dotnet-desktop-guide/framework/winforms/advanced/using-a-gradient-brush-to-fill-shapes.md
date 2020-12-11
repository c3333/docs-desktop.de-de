---
title: Verwenden eines Pinsels für Farbverläufe zum Ausfüllen von Formen
ms.date: 03/30/2017
helpviewer_keywords:
- brushes [Windows Forms], gradient brushes
- gradient brushes
- examples [Windows Forms], gradient brushes
ms.assetid: 2c6037b9-05bd-44c0-a22a-19584b722524
ms.openlocfilehash: 7ff555ba4fd81e9123e5f9e9feed38a0ec9d0a08
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976044"
---
# <a name="using-a-gradient-brush-to-fill-shapes"></a><span data-ttu-id="0b7ff-102">Verwenden eines Pinsels für Farbverläufe zum Ausfüllen von Formen</span><span class="sxs-lookup"><span data-stu-id="0b7ff-102">Using a Gradient Brush to Fill Shapes</span></span>
<span data-ttu-id="0b7ff-103">Sie können einen Farbverlaufs Pinsel verwenden, um eine Form mit einer allmählich veränderlichen Farbe auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-103">You can use a gradient brush to fill a shape with a gradually changing color.</span></span> <span data-ttu-id="0b7ff-104">Beispielsweise können Sie einen horizontalen Farbverlauf verwenden, um eine Form mit Farben auszufüllen, die sich allmählich ändert, wenn Sie vom linken Rand der Form zum rechten Rand wechseln.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-104">For example, you can use a horizontal gradient to fill a shape with color that changes gradually as you move from the left edge of the shape to the right edge.</span></span> <span data-ttu-id="0b7ff-105">Stellen Sie sich ein Rechteck mit einem linken Rand vor, der schwarz ist (dargestellt durch die rote, grüne und blaue Komponente 0, 0, 0) und einen rechten roten Rand (dargestellt durch 255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="0b7ff-105">Imagine a rectangle with a left edge that is black (represented by red, green, and blue components 0, 0, 0) and a right edge that is red (represented by 255, 0, 0).</span></span> <span data-ttu-id="0b7ff-106">Wenn das Rechteck 256 Pixel breit ist, ist die rote Komponente eines gegebenen Pixels eine größer als die rote Komponente des Pixels links.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-106">If the rectangle is 256 pixels wide, the red component of a given pixel will be one greater than the red component of the pixel to its left.</span></span> <span data-ttu-id="0b7ff-107">Das äußteste linke Pixel in einer Zeile hat Farbkomponenten (0, 0, 0), das zweite Pixel hat (1, 0, 0), das dritte Pixel hat (2, 0, 0) usw., bis Sie zum äußersten äußersten Pixel mit Farbkomponenten (255, 0,0) gelangen.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-107">The leftmost pixel in a row has color components (0, 0, 0), the second pixel has (1, 0, 0), the third pixel has (2, 0, 0), and so on, until you get to the rightmost pixel, which has color components (255, 0, 0).</span></span> <span data-ttu-id="0b7ff-108">Diese interpoliert Farbwerte bilden den Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-108">These interpolated color values make up the color gradient.</span></span>  
  
 <span data-ttu-id="0b7ff-109">Die Farbe eines linearen Farbverlaufs ändert sich, wenn Sie horizontal, vertikal oder parallel zu einer angegebenen schrägen Linie wechseln.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-109">A linear gradient changes color as you move horizontally, vertically, or parallel to a specified slanted line.</span></span> <span data-ttu-id="0b7ff-110">Ein Pfad Farbverlauf ändert die Farbe, wenn Sie zum inneren und zur Grenze eines Pfads wechseln.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-110">A path gradient changes color as you move about the interior and boundary of a path.</span></span> <span data-ttu-id="0b7ff-111">Sie können Pfad Farbverläufe anpassen, um eine Vielzahl von Effekten zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-111">You can customize path gradients to achieve a wide variety of effects.</span></span>  
  
 <span data-ttu-id="0b7ff-112">Die folgende Abbildung zeigt ein Rechteck mit einem linearen Farbverlaufs Pinsel und einer Ellipse, die mit einem Pfad Farbverlaufs Pinsel gefüllt ist:</span><span class="sxs-lookup"><span data-stu-id="0b7ff-112">The following illustration shows a rectangle filled with a linear gradient brush and an ellipse filled with a path gradient brush:</span></span>  
  
 ![Ein Rechteck, das mit einem Farbverlaufs Pinsel mit einer Ellipse gefüllt ist.](./media/using-a-gradient-brush-to-fill-shapes/rectangle-ellipse-gradient-brush.png)  
  
## <a name="in-this-section"></a><span data-ttu-id="0b7ff-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0b7ff-114">In This Section</span></span>  
 [<span data-ttu-id="0b7ff-115">Vorgehensweise: Erstellen eines linearen Farbverlaufs</span><span class="sxs-lookup"><span data-stu-id="0b7ff-115">How to: Create a Linear Gradient</span></span>](how-to-create-a-linear-gradient.md)  
 <span data-ttu-id="0b7ff-116">Zeigt, wie ein linearer Farbverlauf mithilfe der-Klasse erstellt wird <xref:System.Drawing.Drawing2D.LinearGradientBrush> .</span><span class="sxs-lookup"><span data-stu-id="0b7ff-116">Shows how to create a linear gradient using the <xref:System.Drawing.Drawing2D.LinearGradientBrush> class.</span></span>  
  
 [<span data-ttu-id="0b7ff-117">Vorgehensweise: Erstellen eines linearen Pfadfarbverlaufs</span><span class="sxs-lookup"><span data-stu-id="0b7ff-117">How to: Create a Path Gradient</span></span>](how-to-create-a-path-gradient.md)  
 <span data-ttu-id="0b7ff-118">Beschreibt, wie ein Pfad Verlauf mithilfe der- <xref:System.Drawing.Drawing2D.PathGradientBrush> Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-118">Describes how to create a path gradient using the <xref:System.Drawing.Drawing2D.PathGradientBrush> class.</span></span>  
  
 [<span data-ttu-id="0b7ff-119">Vorgehensweise: Anwenden der Gammakorrektur bei einem Farbverlauf</span><span class="sxs-lookup"><span data-stu-id="0b7ff-119">How to: Apply Gamma Correction to a Gradient</span></span>](how-to-apply-gamma-correction-to-a-gradient.md)  
 <span data-ttu-id="0b7ff-120">Erläutert, wie die Gammakorrektur mit einem Farbverlaufs Pinsel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-120">Explains how to use gamma correction with a gradient brush.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="0b7ff-121">Verweis</span><span class="sxs-lookup"><span data-stu-id="0b7ff-121">Reference</span></span>  
 <xref:System.Drawing.Drawing2D.LinearGradientBrush?displayProperty=nameWithType>  
 <span data-ttu-id="0b7ff-122">Enthält eine Beschreibung dieser Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-122">Contains a description of this class and has links to all of its members.</span></span>  
  
 <xref:System.Drawing.Drawing2D.PathGradientBrush?displayProperty=nameWithType>  
 <span data-ttu-id="0b7ff-123">Enthält eine Beschreibung dieser Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="0b7ff-123">Contains a description of this class and has links to all of its members.</span></span>
