---
title: 'Vorgehensweise: Abflachen eines Kurvenpfads zu einer Linie'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], flattening curves into lines
- curves [Windows Forms], flattening
- GraphicsPath object
- paths [Windows Forms], flattening
- drawing [Windows Forms], flattening curves
ms.assetid: e654b8de-25f4-4735-9208-42e4514a589c
ms.openlocfilehash: d59a802618ddd5080c651e822ed4c09641f7f170
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976162"
---
# <a name="how-to-flatten-a-curved-path-into-a-line"></a><span data-ttu-id="91bc8-102">Vorgehensweise: Abflachen eines Kurvenpfads zu einer Linie</span><span class="sxs-lookup"><span data-stu-id="91bc8-102">How to: Flatten a Curved Path into a Line</span></span>
<span data-ttu-id="91bc8-103">Ein <xref:System.Drawing.Drawing2D.GraphicsPath> -Objekt speichert eine Sequenz von Linien und Bézier-Splines.</span><span class="sxs-lookup"><span data-stu-id="91bc8-103">A <xref:System.Drawing.Drawing2D.GraphicsPath> object stores a sequence of lines and Bézier splines.</span></span> <span data-ttu-id="91bc8-104">Sie können einem Pfad mehrere Arten von Kurven (Ellipsen, Arcs, kardinale Splines) hinzufügen, aber jede Kurve wird in eine Bézier-Spline konvertiert, bevor Sie im Pfad gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="91bc8-104">You can add several types of curves (ellipses, arcs, cardinal splines) to a path, but each curve is converted to a Bézier spline before it is stored in the path.</span></span> <span data-ttu-id="91bc8-105">Das Vereinfachen eines Pfads besteht darin, jede Bézier-Spline im Pfad in eine Sequenz von geraden Zeilen umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="91bc8-105">Flattening a path consists of converting each Bézier spline in the path to a sequence of straight lines.</span></span> <span data-ttu-id="91bc8-106">Die folgende Abbildung zeigt einen Pfad vor und nach der Vereinfachung.</span><span class="sxs-lookup"><span data-stu-id="91bc8-106">The following illustration shows a path before and after flattening.</span></span>  
  
 <span data-ttu-id="91bc8-107">![Gerade Linien und Kurven](./media/aboutgdip02-art32a.gif "AboutGdip02_Art32A")</span><span class="sxs-lookup"><span data-stu-id="91bc8-107">![Straight Lines and Curves](./media/aboutgdip02-art32a.gif "AboutGdip02_Art32A")</span></span>  
  
### <a name="to-flatten-a-path"></a><span data-ttu-id="91bc8-108">So vereinfachen Sie einen Pfad</span><span class="sxs-lookup"><span data-stu-id="91bc8-108">To Flatten a Path</span></span>  
  
- <span data-ttu-id="91bc8-109">Ruft die- <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> Methode eines- <xref:System.Drawing.Drawing2D.GraphicsPath> Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="91bc8-109">call the <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> method of a <xref:System.Drawing.Drawing2D.GraphicsPath> object.</span></span> <span data-ttu-id="91bc8-110">Die <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> -Methode empfängt ein abflachungs-Argument, das den maximalen Abstand zwischen dem vereinfachten Pfad und dem ursprünglichen Pfad angibt.</span><span class="sxs-lookup"><span data-stu-id="91bc8-110">The <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> method receives a flatness argument that specifies the maximum distance between the flattened path and the original path.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91bc8-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91bc8-111">See also</span></span>

- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- [<span data-ttu-id="91bc8-112">Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="91bc8-112">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="91bc8-113">Erstellen und Zeichnen von Pfaden</span><span class="sxs-lookup"><span data-stu-id="91bc8-113">Constructing and Drawing Paths</span></span>](constructing-and-drawing-paths.md)
