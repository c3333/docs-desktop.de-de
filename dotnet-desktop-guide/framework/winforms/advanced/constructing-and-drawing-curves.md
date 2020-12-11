---
title: Erstellen und Zeichnen von Kurven
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [Windows Forms], curves
- examples [Windows Forms], drawing curves
- curves [Windows Forms], drawing
ms.assetid: 76e92623-4130-4644-b867-faca58bdb3a2
ms.openlocfilehash: 4c1b0cc6c6f878569fcf0c392f1b6f9683ec8afc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975048"
---
# <a name="constructing-and-drawing-curves"></a><span data-ttu-id="0f7f7-102">Erstellen und Zeichnen von Kurven</span><span class="sxs-lookup"><span data-stu-id="0f7f7-102">Constructing and Drawing Curves</span></span>
<span data-ttu-id="0f7f7-103">GDI+ unterstützt verschiedene Arten von Kurven: Ellipsen, Arcs, kardinale Splines und Bézier-Splines.</span><span class="sxs-lookup"><span data-stu-id="0f7f7-103">GDI+ supports several types of curves: ellipses, arcs, cardinal splines, and Bézier splines.</span></span> <span data-ttu-id="0f7f7-104">Eine Ellipse wird durch das umgebende Rechteck definiert. ein Bogen ist ein Teil einer Ellipse, die durch einen Anfangs Winkel und einen Pfeil Winkel definiert wird.</span><span class="sxs-lookup"><span data-stu-id="0f7f7-104">An ellipse is defined by its bounding rectangle; an arc is a portion of an ellipse defined by a starting angle and a sweep angle.</span></span> <span data-ttu-id="0f7f7-105">Ein kardinalspline wird durch ein Array von Punkten und einen Spannungs Parameter definiert – die Kurve verläuft nahtlos durch jeden Punkt im Array, und der Tension-Parameter wirkt sich auf die Art und Weise der Kurve aus.</span><span class="sxs-lookup"><span data-stu-id="0f7f7-105">A cardinal spline is defined by an array of points and a tension parameter — the curve passes smoothly through each point in the array, and the tension parameter influences the way the curve bends.</span></span> <span data-ttu-id="0f7f7-106">Eine Bézier-Spline wird durch zwei Endpunkte definiert, und zwei Kontrollpunkte, die die Kurve nicht durch die Steuerpunkte übergibt, aber die Steuerungs Punkte beeinflussen die Richtung und die Kurve, wenn die Kurve von einem Endpunkt zum anderen wechselt.</span><span class="sxs-lookup"><span data-stu-id="0f7f7-106">A Bézier spline is defined by two endpoints and two control points  the curve does not pass through the control points, but the control points influence the direction and bend as the curve goes from one endpoint to the other.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="0f7f7-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0f7f7-107">In This Section</span></span>  
 [<span data-ttu-id="0f7f7-108">Vorgehensweise: Zeichnen von kardinalen Splines</span><span class="sxs-lookup"><span data-stu-id="0f7f7-108">How to: Draw Cardinal Splines</span></span>](how-to-draw-cardinal-splines.md)  
 <span data-ttu-id="0f7f7-109">Beschreibt die kardinale Splines und wie Sie gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="0f7f7-109">Describes cardinal splines and how to draw them.</span></span>  
  
 [<span data-ttu-id="0f7f7-110">Vorgehensweise: Zeichnen eines einzelnen Bézier-Splines</span><span class="sxs-lookup"><span data-stu-id="0f7f7-110">How to: Draw a Single Bézier Spline</span></span>](how-to-draw-a-single-bezier-spline.md)  
 <span data-ttu-id="0f7f7-111">Beschreibt eine Bézier-Spline und wie Sie gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="0f7f7-111">Describes a Bézier spline and how to draw one.</span></span>  
  
 [<span data-ttu-id="0f7f7-112">Vorgehensweise: Zeichnen einer Folge von Bézier-Splines</span><span class="sxs-lookup"><span data-stu-id="0f7f7-112">How to: Draw a Sequence of Bézier Splines</span></span>](how-to-draw-a-sequence-of-bezier-splines.md)  
 <span data-ttu-id="0f7f7-113">Erläutert, wie mehrere Bézier-Splines nacheinander gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="0f7f7-113">Explains how to draw several Bézier splines in sequence.</span></span>
