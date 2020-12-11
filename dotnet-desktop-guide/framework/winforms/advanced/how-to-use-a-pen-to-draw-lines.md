---
title: 'Vorgehensweise: Verwenden eines Stifts zum Zeichnen von Linien'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lines [Windows Forms], drawing
- pens [Windows Forms], drawing lines
ms.assetid: 0828c331-a438-4bdd-a4d6-3ef1e59e8795
ms.openlocfilehash: 263c0fbda377e64753cd2d607f633117b4b44253
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976108"
---
# <a name="how-to-use-a-pen-to-draw-lines"></a><span data-ttu-id="945e9-102">Vorgehensweise: Verwenden eines Stifts zum Zeichnen von Linien</span><span class="sxs-lookup"><span data-stu-id="945e9-102">How to: Use a Pen to Draw Lines</span></span>
<span data-ttu-id="945e9-103">Um Linien zu zeichnen, benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt.</span><span class="sxs-lookup"><span data-stu-id="945e9-103">To draw lines, you need a <xref:System.Drawing.Graphics> object and a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="945e9-104">Das <xref:System.Drawing.Graphics> -Objekt stellt die <xref:System.Drawing.Graphics.DrawLine%2A> -Methode bereit, und das- <xref:System.Drawing.Pen> Objekt speichert Funktionen der Zeile, z. b. Farbe und Breite.</span><span class="sxs-lookup"><span data-stu-id="945e9-104">The <xref:System.Drawing.Graphics> object provides the <xref:System.Drawing.Graphics.DrawLine%2A> method, and the <xref:System.Drawing.Pen> object stores features of the line, such as color and width.</span></span>  
  
## <a name="example"></a><span data-ttu-id="945e9-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="945e9-105">Example</span></span>  
 <span data-ttu-id="945e9-106">Im folgenden Beispiel wird eine Zeile von (20, 10) nach (300, 100) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="945e9-106">The following example draws a line from (20, 10) to (300, 100).</span></span> <span data-ttu-id="945e9-107">Die erste Anweisung verwendet den- <xref:System.Drawing.Pen.%23ctor%2A> Klassenkonstruktor, um einen schwarzen Stift zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="945e9-107">The first statement uses the <xref:System.Drawing.Pen.%23ctor%2A> class constructor to create a black pen.</span></span> <span data-ttu-id="945e9-108">Das einzige Argument, das an den <xref:System.Drawing.Pen.%23ctor%2A> Konstruktor übergeben wird, ist ein <xref:System.Drawing.Color> mit der-Methode erstelltes-Objekt <xref:System.Drawing.Color.FromArgb%2A> .</span><span class="sxs-lookup"><span data-stu-id="945e9-108">The one argument passed to the <xref:System.Drawing.Pen.%23ctor%2A> constructor is a <xref:System.Drawing.Color> object created with the <xref:System.Drawing.Color.FromArgb%2A> method.</span></span> <span data-ttu-id="945e9-109">Die Werte, die zum Erstellen des <xref:System.Drawing.Color> Objekts – (255, 0, 0, 0) – verwendet werden, entsprechen den Alpha-, rot-, grün-und blauen Komponenten der Farbe.</span><span class="sxs-lookup"><span data-stu-id="945e9-109">The values used to create the <xref:System.Drawing.Color> object — (255, 0, 0, 0) — correspond to the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="945e9-110">Diese Werte definieren einen nicht transparenten schwarzen Stift.</span><span class="sxs-lookup"><span data-stu-id="945e9-110">These values define an opaque black pen.</span></span>  
  
 [!code-csharp[System.Drawing.UsingAPen#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.UsingAPen#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="945e9-111">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="945e9-111">Compiling the Code</span></span>  
 <span data-ttu-id="945e9-112">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="945e9-112">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="945e9-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="945e9-113">See also</span></span>

- <xref:System.Drawing.Pen>
- [<span data-ttu-id="945e9-114">Verwenden eines Stifts zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="945e9-114">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="945e9-115">Stifte, Linien und Rechtecke in GDI+</span><span class="sxs-lookup"><span data-stu-id="945e9-115">Pens, Lines, and Rectangles in GDI+</span></span>](pens-lines-and-rectangles-in-gdi.md)
