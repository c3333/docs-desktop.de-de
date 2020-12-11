---
title: 'Vorgehensweise: Zeichnen eines ausgefüllten Rechtecks in Windows Forms'
description: Erfahren Sie, wie Sie ein ausgefülltes Rechteck Programm gesteuert in einem Windows Form zeichnen. Erfahren Sie auch mehr über das Kompilieren von Code.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- Graphics.FillRectangle
helpviewer_keywords:
- drawing [Windows Forms], rectangles
- rectangles [Windows Forms], drawing
- drawing rectangles
ms.assetid: d656a93c-987d-4809-aafd-493fe17450f0
ms.openlocfilehash: 0ad8ec97000e29b2194a9eda713aa43d5557b44c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972353"
---
# <a name="how-to-draw-a-filled-rectangle-on-a-windows-form"></a><span data-ttu-id="fcbed-104">Vorgehensweise: Zeichnen eines ausgefüllten Rechtecks in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fcbed-104">How to: Draw a Filled Rectangle on a Windows Form</span></span>
<span data-ttu-id="fcbed-105">In diesem Beispiel wird ein ausgefülltes Rechteck in einem Formular gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fcbed-105">This example draws a filled rectangle on a form.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fcbed-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fcbed-106">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#2](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#2)]
 [!code-csharp[System.Drawing.ConceptualHowTos#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#2)]
 [!code-vb[System.Drawing.ConceptualHowTos#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#2)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="fcbed-107">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="fcbed-107">Compiling the Code</span></span>  
 <span data-ttu-id="fcbed-108">Diese Methode kann nicht im- <xref:System.Windows.Forms.Form.Load> Ereignishandler aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fcbed-108">You cannot call this method in the <xref:System.Windows.Forms.Form.Load> event handler.</span></span> <span data-ttu-id="fcbed-109">Der gezeichnete Inhalt wird nicht neu gezeichnet, wenn die Größe des Formulars geändert oder durch ein anderes Formular verdeckt wird.</span><span class="sxs-lookup"><span data-stu-id="fcbed-109">The drawn content will not be redrawn if the form is resized or obscured by another form.</span></span> <span data-ttu-id="fcbed-110">Damit Ihre Inhalte automatisch neu gezeichnet werden, sollten Sie die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="fcbed-110">To make your content automatically repaint, you should override the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="fcbed-111">Stabile Programmierung</span><span class="sxs-lookup"><span data-stu-id="fcbed-111">Robust Programming</span></span>  
 <span data-ttu-id="fcbed-112">Sie sollten immer <xref:System.IDisposable.Dispose%2A> für alle-Objekte, die Systemressourcen nutzen, z <xref:System.Drawing.Brush> . b.-und-Objekte, Abrufen <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="fcbed-112">You should always call <xref:System.IDisposable.Dispose%2A> on any objects that consume system resources, such as <xref:System.Drawing.Brush> and <xref:System.Drawing.Graphics> objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fcbed-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcbed-113">See also</span></span>

- <xref:System.Drawing.Graphics.FillRectangle%2A>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- [<span data-ttu-id="fcbed-114">Erste Schritte mit Grafikprogrammierung</span><span class="sxs-lookup"><span data-stu-id="fcbed-114">Getting Started with Graphics Programming</span></span>](getting-started-with-graphics-programming.md)
- [<span data-ttu-id="fcbed-115">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fcbed-115">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="fcbed-116">Verwenden eines Stifts zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="fcbed-116">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="fcbed-117">Pinsel und gefüllte Formen in GDI+</span><span class="sxs-lookup"><span data-stu-id="fcbed-117">Brushes and Filled Shapes in GDI+</span></span>](brushes-and-filled-shapes-in-gdi.md)
