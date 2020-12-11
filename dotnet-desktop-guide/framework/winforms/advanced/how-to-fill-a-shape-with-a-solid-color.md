---
title: 'Vorgehensweise: Ausfüllen einer Form mit einer Volltonfarbe'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], adding to shapes
- shapes [Windows Forms], filling
ms.assetid: 06088b31-bac9-4ef3-9ebe-06c2c764d6df
ms.openlocfilehash: d6fe7a252029ff80f21d99f7342fabb1d29fbe24
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975909"
---
# <a name="how-to-fill-a-shape-with-a-solid-color"></a><span data-ttu-id="a4b7d-102">Vorgehensweise: Ausfüllen einer Form mit einer Volltonfarbe</span><span class="sxs-lookup"><span data-stu-id="a4b7d-102">How to: Fill a Shape with a Solid Color</span></span>
<span data-ttu-id="a4b7d-103">Um eine Form mit einer voll Tonfarbe auszufüllen, erstellen Sie ein <xref:System.Drawing.SolidBrush> -Objekt, und übergeben Sie das <xref:System.Drawing.SolidBrush> Objekt dann als Argument an eine der Fill-Methoden der- <xref:System.Drawing.Graphics> Klasse.</span><span class="sxs-lookup"><span data-stu-id="a4b7d-103">To fill a shape with a solid color, create a <xref:System.Drawing.SolidBrush> object, and then pass that <xref:System.Drawing.SolidBrush> object as an argument to one of the fill methods of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="a4b7d-104">Im folgenden Beispiel wird gezeigt, wie eine Ellipse mit der Farbe rot gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="a4b7d-104">The following example shows how to fill an ellipse with the color red.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a4b7d-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a4b7d-105">Example</span></span>  
 <span data-ttu-id="a4b7d-106">Im folgenden Code nimmt der- <xref:System.Drawing.SolidBrush.%23ctor%2A> Konstruktor ein- <xref:System.Drawing.Color> Objekt als einziges Argument an.</span><span class="sxs-lookup"><span data-stu-id="a4b7d-106">In the following code, the <xref:System.Drawing.SolidBrush.%23ctor%2A> constructor takes a <xref:System.Drawing.Color> object as its only argument.</span></span> <span data-ttu-id="a4b7d-107">Die Werte, die von der-Methode verwendet werden, <xref:System.Drawing.Color.FromArgb%2A> stellen die Alpha-, rot-, grün-und Blau-Komponenten der Farbe dar.</span><span class="sxs-lookup"><span data-stu-id="a4b7d-107">The values used by the <xref:System.Drawing.Color.FromArgb%2A> method represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="a4b7d-108">Jeder dieser Werte muss zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="a4b7d-108">Each of these values must be in the range 0 through 255.</span></span> <span data-ttu-id="a4b7d-109">Der erste 255 gibt an, dass die Farbe vollständig undurchsichtig ist, und der zweite 255 gibt an, dass die rote Komponente vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="a4b7d-109">The first 255 indicates that the color is fully opaque, and the second 255 indicates that the red component is at full intensity.</span></span> <span data-ttu-id="a4b7d-110">Die beiden Nullen zeigen an, dass die grünen und blauen Komponenten beide eine Intensität von 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a4b7d-110">The two zeros indicate that the green and blue components both have an intensity of 0.</span></span>  
  
 <span data-ttu-id="a4b7d-111">Die vier Zahlen (0, 0, 100, 60), die an die-Methode übergeben werden, <xref:System.Drawing.Graphics.FillEllipse%2A> geben den Speicherort und die Größe des umschließenden Rechtecks für die Ellipse an.</span><span class="sxs-lookup"><span data-stu-id="a4b7d-111">The four numbers (0, 0, 100, 60) passed to the <xref:System.Drawing.Graphics.FillEllipse%2A> method specify the location and size of the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="a4b7d-112">Das Rechteck hat eine linke obere Ecke von (0,0), eine Breite von 100 und eine Höhe von 60.</span><span class="sxs-lookup"><span data-stu-id="a4b7d-112">The rectangle has an upper-left corner of (0, 0), a width of 100, and a height of 60.</span></span>  
  
 [!code-csharp[System.Drawing.UsingABrush#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.UsingABrush#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a4b7d-113">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="a4b7d-113">Compiling the Code</span></span>  
 <span data-ttu-id="a4b7d-114">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="a4b7d-114">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4b7d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4b7d-115">See also</span></span>

- [<span data-ttu-id="a4b7d-116">Verwenden eines Pinsels zum Ausfüllen von Formen</span><span class="sxs-lookup"><span data-stu-id="a4b7d-116">Using a Brush to Fill Shapes</span></span>](using-a-brush-to-fill-shapes.md)
