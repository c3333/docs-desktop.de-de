---
title: Verwenden eines Stiftes zum Zeichnen von Linien und Formen
ms.date: 03/30/2017
helpviewer_keywords:
- pens
- examples [Windows Forms], drawing lines and shapes
- examples [Windows Forms], pens
- drawing
ms.assetid: 8a7542ab-3e9e-443f-8405-2d6053528e20
ms.openlocfilehash: d20b4e47c9f8a5dd7a144e6ebb3151d3ab65a800
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975235"
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="38c7f-102">Verwenden eines Stiftes zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="38c7f-102">Using a Pen to Draw Lines and Shapes</span></span>
<span data-ttu-id="38c7f-103">Verwenden Sie GDI+- `Pen` Objekte, um Liniensegmente, Kurven und die Kontur der Formen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="38c7f-103">Use GDI+ `Pen` objects to draw line segments, curves, and the outlines of shapes.</span></span> <span data-ttu-id="38c7f-104">In diesem Abschnitt bezieht sich *Zeile* auf diese, es sei denn, Sie gibt an, dass nur ein Liniensegment gemeint ist.</span><span class="sxs-lookup"><span data-stu-id="38c7f-104">In this section, *line* refers to any of these, unless specified to mean only a line segment.</span></span> <span data-ttu-id="38c7f-105">Legen Sie die Eigenschaften eines Stifts fest, um die Farbe, Breite, Ausrichtung und den Stil der Linien zu steuern, die mit diesem Stift gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="38c7f-105">Set the properties of a pen to control the color, width, alignment, and style of lines drawn with that pen.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="38c7f-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="38c7f-106">In This Section</span></span>  
 [<span data-ttu-id="38c7f-107">Vorgehensweise: Verwenden eines Stifts zum Zeichnen von Linien</span><span class="sxs-lookup"><span data-stu-id="38c7f-107">How to: Use a Pen to Draw Lines</span></span>](how-to-use-a-pen-to-draw-lines.md)  
 <span data-ttu-id="38c7f-108">Erläutert, wie Linien gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="38c7f-108">Explains how to draw lines.</span></span>  
  
 [<span data-ttu-id="38c7f-109">Vorgehensweise: Verwenden eines Stifts zum Zeichnen von Rechtecken</span><span class="sxs-lookup"><span data-stu-id="38c7f-109">How to: Use a Pen to Draw Rectangles</span></span>](how-to-use-a-pen-to-draw-rectangles.md)  
 <span data-ttu-id="38c7f-110">Beschreibt, wie Rechtecke gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="38c7f-110">Describes how to draw rectangles.</span></span>  
  
 [<span data-ttu-id="38c7f-111">Vorgehensweise: Festlegen von Stiftbreite und -ausrichtung</span><span class="sxs-lookup"><span data-stu-id="38c7f-111">How to: Set Pen Width and Alignment</span></span>](how-to-set-pen-width-and-alignment.md)  
 <span data-ttu-id="38c7f-112">Erläutert, wie die Breite und die Ausrichtung eines- `Pen` Objekts geändert werden.</span><span class="sxs-lookup"><span data-stu-id="38c7f-112">Explains how to change the width and alignment of a `Pen` object.</span></span>  
  
 [<span data-ttu-id="38c7f-113">Vorgehensweise: Zeichnen einer Linie mit Linienenden</span><span class="sxs-lookup"><span data-stu-id="38c7f-113">How to: Draw a Line with Line Caps</span></span>](how-to-draw-a-line-with-line-caps.md)  
 <span data-ttu-id="38c7f-114">Beschreibt das Hinzufügen von Endpunkten beim Zeichnen einer Linie.</span><span class="sxs-lookup"><span data-stu-id="38c7f-114">Describes how to add end caps when drawing a line.</span></span>  
  
 [<span data-ttu-id="38c7f-115">Vorgehensweise: Verknüpfen von Linien</span><span class="sxs-lookup"><span data-stu-id="38c7f-115">How to: Join Lines</span></span>](how-to-join-lines.md)  
 <span data-ttu-id="38c7f-116">Zeigt, wie zwei Zeilen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="38c7f-116">Shows how to join two lines.</span></span>  
  
 [<span data-ttu-id="38c7f-117">Vorgehensweise: Zeichnen einer benutzerdefinierten gestrichelten Linie</span><span class="sxs-lookup"><span data-stu-id="38c7f-117">How to: Draw a Custom Dashed Line</span></span>](how-to-draw-a-custom-dashed-line.md)  
 <span data-ttu-id="38c7f-118">Beschreibt, wie eine gestrichelte Linie gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="38c7f-118">Describes how to draw a dashed line.</span></span>  
  
 [<span data-ttu-id="38c7f-119">Vorgehensweise: Zeichnen einer mit einer Textur ausgefüllten Linie</span><span class="sxs-lookup"><span data-stu-id="38c7f-119">How to: Draw a Line Filled with a Texture</span></span>](how-to-draw-a-line-filled-with-a-texture.md)  
 <span data-ttu-id="38c7f-120">Erläutert, wie eine Textur gefüllte Linie gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="38c7f-120">Explains how to draw a texture-filled line.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="38c7f-121">Verweis</span><span class="sxs-lookup"><span data-stu-id="38c7f-121">Reference</span></span>  
 <xref:System.Drawing.Pen>  
 <span data-ttu-id="38c7f-122">Beschreibt diese Klasse und enthält Links zu allen deren Membern.</span><span class="sxs-lookup"><span data-stu-id="38c7f-122">Describes this class and has links to all its members.</span></span>
