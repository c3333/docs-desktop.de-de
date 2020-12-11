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
# <a name="constructing-and-drawing-curves"></a>Erstellen und Zeichnen von Kurven
GDI+ unterstützt verschiedene Arten von Kurven: Ellipsen, Arcs, kardinale Splines und Bézier-Splines. Eine Ellipse wird durch das umgebende Rechteck definiert. ein Bogen ist ein Teil einer Ellipse, die durch einen Anfangs Winkel und einen Pfeil Winkel definiert wird. Ein kardinalspline wird durch ein Array von Punkten und einen Spannungs Parameter definiert – die Kurve verläuft nahtlos durch jeden Punkt im Array, und der Tension-Parameter wirkt sich auf die Art und Weise der Kurve aus. Eine Bézier-Spline wird durch zwei Endpunkte definiert, und zwei Kontrollpunkte, die die Kurve nicht durch die Steuerpunkte übergibt, aber die Steuerungs Punkte beeinflussen die Richtung und die Kurve, wenn die Kurve von einem Endpunkt zum anderen wechselt.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Vorgehensweise: Zeichnen von kardinalen Splines](how-to-draw-cardinal-splines.md)  
 Beschreibt die kardinale Splines und wie Sie gezeichnet werden.  
  
 [Vorgehensweise: Zeichnen eines einzelnen Bézier-Splines](how-to-draw-a-single-bezier-spline.md)  
 Beschreibt eine Bézier-Spline und wie Sie gezeichnet werden.  
  
 [Vorgehensweise: Zeichnen einer Folge von Bézier-Splines](how-to-draw-a-sequence-of-bezier-splines.md)  
 Erläutert, wie mehrere Bézier-Splines nacheinander gezeichnet werden.
