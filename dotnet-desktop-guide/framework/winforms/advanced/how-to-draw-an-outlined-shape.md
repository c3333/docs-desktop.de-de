---
title: 'Vorgehensweise: Zeichnen der Kontur einer Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- Graphics.DrawEllipse
helpviewer_keywords:
- ellipses [Windows Forms], drawing
- circles [Windows Forms], drawing
- drawing [Windows Forms], shapes
- circular shapes
- forms [Windows Forms], drawing circular shapes
- circles
- outlined shapes [Windows Forms], examples
- outlined shapes [Windows Forms], drawing
- drawing [Windows Forms], circular shapes
- shapes [Windows Forms], drawing
ms.assetid: f4f9214c-607e-407d-8cdd-6549f0278451
ms.openlocfilehash: 019bbc19cc4b26c42f8539eccd93ec4ff87fab12
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975937"
---
# <a name="how-to-draw-an-outlined-shape"></a><span data-ttu-id="71b4b-102">Vorgehensweise: Zeichnen der Kontur einer Form</span><span class="sxs-lookup"><span data-stu-id="71b4b-102">How to: Draw an Outlined Shape</span></span>
<span data-ttu-id="71b4b-103">In diesem Beispiel werden die Auslassungs Punkte und Rechtecke in einem Formular gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="71b4b-103">This example draws outlined ellipses and rectangles on a form.</span></span>  
  
## <a name="example"></a><span data-ttu-id="71b4b-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="71b4b-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#6](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#6)]
 [!code-csharp[System.Drawing.ConceptualHowTos#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#6)]
 [!code-vb[System.Drawing.ConceptualHowTos#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#6)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="71b4b-105">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="71b4b-105">Compiling the Code</span></span>  
 <span data-ttu-id="71b4b-106">Diese Methode kann nicht im- <xref:System.Windows.Forms.Form.Load> Ereignishandler aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71b4b-106">You cannot call this method in the <xref:System.Windows.Forms.Form.Load> event handler.</span></span> <span data-ttu-id="71b4b-107">Der gezeichnete Inhalt wird nicht neu gezeichnet, wenn die Größe des Formulars geändert oder durch ein anderes Formular verdeckt wird.</span><span class="sxs-lookup"><span data-stu-id="71b4b-107">The drawn content will not be redrawn if the form is resized or obscured by another form.</span></span> <span data-ttu-id="71b4b-108">Damit Ihre Inhalte automatisch neu gezeichnet werden, sollten Sie die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="71b4b-108">To make your content automatically repaint, you should override the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="71b4b-109">Stabile Programmierung</span><span class="sxs-lookup"><span data-stu-id="71b4b-109">Robust Programming</span></span>  
 <span data-ttu-id="71b4b-110">Sie sollten immer <xref:System.IDisposable.Dispose%2A> für alle-Objekte, die Systemressourcen nutzen, z <xref:System.Drawing.Pen> . b.-und-Objekte, Abrufen <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="71b4b-110">You should always call <xref:System.IDisposable.Dispose%2A> on any objects that consume system resources, such as <xref:System.Drawing.Pen> and <xref:System.Drawing.Graphics> objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71b4b-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71b4b-111">See also</span></span>

- <xref:System.Drawing.Graphics.DrawEllipse%2A>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- <xref:System.Drawing.Graphics.DrawRectangle%2A>
- [<span data-ttu-id="71b4b-112">Erste Schritte mit Grafikprogrammierung</span><span class="sxs-lookup"><span data-stu-id="71b4b-112">Getting Started with Graphics Programming</span></span>](getting-started-with-graphics-programming.md)
- [<span data-ttu-id="71b4b-113">Verwenden eines Stifts zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="71b4b-113">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="71b4b-114">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="71b4b-114">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
