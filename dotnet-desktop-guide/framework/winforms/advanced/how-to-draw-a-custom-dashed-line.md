---
title: 'Vorgehensweise: Zeichnen einer benutzerdefinierten gestrichelten Linie'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lines [Windows Forms], custom
- lines [Windows Forms], drawing
- lines [Windows Forms], dashed
ms.assetid: cd0ed96a-cce4-47b9-b58a-3bae2e3d1bee
ms.openlocfilehash: d2184a8d7d7f24b8f631818608ab4bcdb89857c7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972356"
---
# <a name="how-to-draw-a-custom-dashed-line"></a><span data-ttu-id="a9b5c-102">Vorgehensweise: Zeichnen einer benutzerdefinierten gestrichelten Linie</span><span class="sxs-lookup"><span data-stu-id="a9b5c-102">How to: Draw a Custom Dashed Line</span></span>
<span data-ttu-id="a9b5c-103">GDI+ stellt mehrere Dash-Stile bereit, die in der- <xref:System.Drawing.Drawing2D.DashStyle> Enumeration aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="a9b5c-103">GDI+ provides several dash styles that are listed in the <xref:System.Drawing.Drawing2D.DashStyle> enumeration.</span></span> <span data-ttu-id="a9b5c-104">Wenn diese standardmäßigen Dash-Stile nicht Ihren Anforderungen entsprechen, können Sie ein benutzerdefiniertes Bindestrich Muster erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9b5c-104">If those standard dash styles do not suit your needs, you can create a custom dash pattern.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a9b5c-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9b5c-105">Example</span></span>  
 <span data-ttu-id="a9b5c-106">Zum Zeichnen einer benutzerdefinierten gestrichelten Linie platzieren Sie die Längen der Bindestriche und Leerzeichen in einem Array, und weisen Sie das Array als Wert der- <xref:System.Drawing.Pen.DashPattern%2A> Eigenschaft eines- <xref:System.Drawing.Pen> Objekts zu.</span><span class="sxs-lookup"><span data-stu-id="a9b5c-106">To draw a custom dashed line, put the lengths of the dashes and spaces in an array and assign the array as the value of the <xref:System.Drawing.Pen.DashPattern%2A> property of a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="a9b5c-107">Im folgenden Beispiel wird eine benutzerdefinierte gestrichelte Linie auf Grundlage des-Arrays gezeichnet `{5, 2, 15, 4}` .</span><span class="sxs-lookup"><span data-stu-id="a9b5c-107">The following example draws a custom dashed line based on the array `{5, 2, 15, 4}`.</span></span> <span data-ttu-id="a9b5c-108">Wenn Sie die Elemente des Arrays mit der Stift Breite 5 multiplizieren, erhalten Sie `{25, 10, 75, 20}` .</span><span class="sxs-lookup"><span data-stu-id="a9b5c-108">If you multiply the elements of the array by the pen width of 5, you get `{25, 10, 75, 20}`.</span></span> <span data-ttu-id="a9b5c-109">Die angezeigten Bindestriche wechseln in eine Länge zwischen 25 und 75 und die Leerzeichen sind in der Länge zwischen 10 und 20.</span><span class="sxs-lookup"><span data-stu-id="a9b5c-109">The displayed dashes alternate in length between 25 and 75, and the spaces alternate in length between 10 and 20.</span></span>  
  
 <span data-ttu-id="a9b5c-110">In der folgenden Abbildung ist die resultierende gestrichelte Linie dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a9b5c-110">The following illustration shows the resulting dashed line.</span></span> <span data-ttu-id="a9b5c-111">Beachten Sie, dass der abschließende Bindestrich kürzer als 25 Einheiten sein muss, damit die Zeile auf (405, 5) enden kann.</span><span class="sxs-lookup"><span data-stu-id="a9b5c-111">Note that the final dash has to be shorter than 25 units so that the line can end at (405, 5).</span></span>  
  
 <span data-ttu-id="a9b5c-112">![Abbildung, die eine gestrichelte Linie anzeigt.](./media/how-to-draw-a-custom-dashed-line/dashed-line-illustration.gif "pens6")</span><span class="sxs-lookup"><span data-stu-id="a9b5c-112">![Illustration that shows a dashed line.](./media/how-to-draw-a-custom-dashed-line/dashed-line-illustration.gif "pens6")</span></span>  
  
 [!code-csharp[System.Drawing.UsingAPen#51](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#51)]
 [!code-vb[System.Drawing.UsingAPen#51](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#51)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a9b5c-113">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="a9b5c-113">Compiling the Code</span></span>  
 <span data-ttu-id="a9b5c-114">Erstellen Sie ein Windows Form, und behandeln Sie das-Ereignis des Formulars <xref:System.Windows.Forms.Control.Paint> .</span><span class="sxs-lookup"><span data-stu-id="a9b5c-114">Create a Windows Form and handle the form's <xref:System.Windows.Forms.Control.Paint> event.</span></span> <span data-ttu-id="a9b5c-115">Fügen Sie den vorangehenden Code in den- <xref:System.Windows.Forms.Control.Paint> Ereignishandler ein.</span><span class="sxs-lookup"><span data-stu-id="a9b5c-115">Paste the preceding code into the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9b5c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9b5c-116">See also</span></span>

- [<span data-ttu-id="a9b5c-117">Verwenden eines Stifts zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="a9b5c-117">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
