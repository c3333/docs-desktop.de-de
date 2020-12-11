---
title: 'Vorgehensweise: Anwenden der Gammakorrektur bei einem Farbverlauf'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- gradient brushes [Windows Forms], gamma correction
- gradients [Windows Forms], gamma correction
ms.assetid: da4690e7-5fac-4fd2-b3f0-5cb35c165b92
ms.openlocfilehash: e812e441233c1d29a67dac639048e20a659549f0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975371"
---
# <a name="how-to-apply-gamma-correction-to-a-gradient"></a><span data-ttu-id="d1139-102">Vorgehensweise: Anwenden der Gammakorrektur bei einem Farbverlauf</span><span class="sxs-lookup"><span data-stu-id="d1139-102">How to: Apply Gamma Correction to a Gradient</span></span>
<span data-ttu-id="d1139-103">Sie können die Gammakorrektur für einen linearen Farbverlaufs Pinsel aktivieren, indem Sie die-Eigenschaft des Pinsels <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> auf festlegen `true` .</span><span class="sxs-lookup"><span data-stu-id="d1139-103">You can enable gamma correction for a linear gradient brush by setting the brush's <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> property to `true`.</span></span> <span data-ttu-id="d1139-104">Sie können die Gammakorrektur deaktivieren, indem Sie die- <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> Eigenschaft auf festlegen `false` .</span><span class="sxs-lookup"><span data-stu-id="d1139-104">You can disable gamma correction by setting the <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> property to `false`.</span></span> <span data-ttu-id="d1139-105">Die Gamma Korrektur ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d1139-105">Gamma correction is disabled by default.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d1139-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d1139-106">Example</span></span>  

<span data-ttu-id="d1139-107">Das folgende Beispiel ist eine Methode, die vom-Ereignishandler eines Steuer Elements aufgerufen wird <xref:System.Windows.Forms.Control.Paint> .</span><span class="sxs-lookup"><span data-stu-id="d1139-107">The following example is a method that is called from a control's <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="d1139-108">Im Beispiel wird ein linearer Farbverlaufs Pinsel erstellt und mithilfe dieses Pinsels zwei Rechtecke aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="d1139-108">The example creates a linear gradient brush and uses that brush to fill two rectangles.</span></span> <span data-ttu-id="d1139-109">Das erste Rechteck wird ohne Gammakorrektur gefüllt, und das zweite Rechteck wird mit der Gammakorrektur gefüllt.</span><span class="sxs-lookup"><span data-stu-id="d1139-109">The first rectangle is filled without gamma correction, and the second rectangle is filled with gamma correction.</span></span>  
  
 <span data-ttu-id="d1139-110">Die folgende Abbildung zeigt die zwei gefüllten Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="d1139-110">The following illustration shows the two filled rectangles.</span></span> <span data-ttu-id="d1139-111">Das obere Rechteck, das keine Gammakorrektur hat, wird in der Mitte dunkel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1139-111">The top rectangle, which does not have gamma correction, appears dark in the middle.</span></span> <span data-ttu-id="d1139-112">Das untere Rechteck, das über eine Gammakorrektur verfügt, scheint eine einheitlichere Intensität zu haben.</span><span class="sxs-lookup"><span data-stu-id="d1139-112">The bottom rectangle, which has gamma correction, appears to have more uniform intensity.</span></span>  
  
 ![Zwei mit einem Farbverlauf gefüllte Rechtecke mit und ohne Gammakorrektur.](./media/how-to-apply-gamma-correction-to-a-gradient/two-rectangles-gamma-gradient.png)  
  
 [!code-csharp[System.Drawing.UsingaGradientBrush#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingaGradientBrush#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="d1139-114">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="d1139-114">Compiling the Code</span></span>  
 <span data-ttu-id="d1139-115">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="d1139-115">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1139-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1139-116">See also</span></span>

- <xref:System.Drawing.Drawing2D.LinearGradientBrush?displayProperty=nameWithType>
- [<span data-ttu-id="d1139-117">Verwenden eines Pinsels für Farbverläufe zum Ausfüllen von Formen</span><span class="sxs-lookup"><span data-stu-id="d1139-117">Using a Gradient Brush to Fill Shapes</span></span>](using-a-gradient-brush-to-fill-shapes.md)
