---
title: 'Vorgehensweise: Erstellen von Figuren aus Linien, Kurven und Formen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- figures [Windows Forms], creating from shapes
- figures [Windows Forms], creating from lines
ms.assetid: 82fd56c7-b443-4765-9b7c-62ce030656ec
ms.openlocfilehash: c8cf7a7e08bed56fb704bba4e30ff369bc3fcf89
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974828"
---
# <a name="how-to-create-figures-from-lines-curves-and-shapes"></a><span data-ttu-id="45241-102">Vorgehensweise: Erstellen von Figuren aus Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="45241-102">How to: Create Figures from Lines, Curves, and Shapes</span></span>
<span data-ttu-id="45241-103">Um eine Abbildung zu erstellen, erstellen Sie einen <xref:System.Drawing.Drawing2D.GraphicsPath> , und rufen Sie dann Methoden, wie z <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> . b <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A> . und, auf, um primitive dem Pfad hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="45241-103">To create a figure, construct a <xref:System.Drawing.Drawing2D.GraphicsPath>, and then call methods, such as <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> and <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A>, to add primitives to the path.</span></span>  
  
## <a name="example"></a><span data-ttu-id="45241-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="45241-104">Example</span></span>  
 <span data-ttu-id="45241-105">In den folgenden Codebeispielen werden Pfade mit Abbildungen erstellt:</span><span class="sxs-lookup"><span data-stu-id="45241-105">The following code examples create paths that have figures:</span></span>  
  
- <span data-ttu-id="45241-106">Im ersten Beispiel wird ein Pfad erstellt, der über eine einzelne Abbildung verfügt.</span><span class="sxs-lookup"><span data-stu-id="45241-106">The first example creates a path that has a single figure.</span></span> <span data-ttu-id="45241-107">Die Abbildung besteht aus einem einzelnen Bogen. Der Bogen hat einen Mittelpunktswinkel von – 180 Grad, der im Standard Koordinatensystem gegen den Uhrzeigersinn steht.</span><span class="sxs-lookup"><span data-stu-id="45241-107">The figure consists of a single arc. The arc has a sweep angle of –180 degrees, which is counterclockwise in the default coordinate system.</span></span>  
  
- <span data-ttu-id="45241-108">Im zweiten Beispiel wird ein Pfad mit zwei Abbildungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="45241-108">The second example creates a path that has two figures.</span></span> <span data-ttu-id="45241-109">Die erste Abbildung ist ein Bogen, gefolgt von einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="45241-109">The first figure is an arc followed by a line.</span></span> <span data-ttu-id="45241-110">Die zweite Abbildung ist eine Zeile, auf die eine Kurve folgt, gefolgt von einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="45241-110">The second figure is a line followed by a curve followed by a line.</span></span> <span data-ttu-id="45241-111">Die erste Abbildung ist links geöffnet, und die zweite Abbildung ist geschlossen.</span><span class="sxs-lookup"><span data-stu-id="45241-111">The first figure is left open, and the second figure is closed.</span></span>  
  
 [!code-csharp[System.Drawing.ConstructingDrawingPaths#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.ConstructingDrawingPaths#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/VB/Class1.vb#21)]  
  
 [!code-csharp[System.Drawing.ConstructingDrawingPaths#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/CS/Class1.cs#22)]
 [!code-vb[System.Drawing.ConstructingDrawingPaths#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/VB/Class1.vb#22)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="45241-112">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="45241-112">Compiling the Code</span></span>  
 <span data-ttu-id="45241-113">Die vorherigen Beispiele sind für die Verwendung mit Windows Forms konzipiert und erfordern <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="45241-113">The previous examples are designed for use with Windows Forms, and they require <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="45241-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45241-114">See also</span></span>

- <xref:System.Drawing.Drawing2D.GraphicsPath>
- [<span data-ttu-id="45241-115">Erstellen und Zeichnen von Pfaden</span><span class="sxs-lookup"><span data-stu-id="45241-115">Constructing and Drawing Paths</span></span>](constructing-and-drawing-paths.md)
- [<span data-ttu-id="45241-116">Verwenden eines Stifts zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="45241-116">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
