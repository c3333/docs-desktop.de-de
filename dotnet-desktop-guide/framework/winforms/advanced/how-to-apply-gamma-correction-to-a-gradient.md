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
# <a name="how-to-apply-gamma-correction-to-a-gradient"></a>Vorgehensweise: Anwenden der Gammakorrektur bei einem Farbverlauf
Sie können die Gammakorrektur für einen linearen Farbverlaufs Pinsel aktivieren, indem Sie die-Eigenschaft des Pinsels <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> auf festlegen `true` . Sie können die Gammakorrektur deaktivieren, indem Sie die- <xref:System.Drawing.Drawing2D.LinearGradientBrush.GammaCorrection%2A> Eigenschaft auf festlegen `false` . Die Gamma Korrektur ist standardmäßig deaktiviert.  
  
## <a name="example"></a>Beispiel  

Das folgende Beispiel ist eine Methode, die vom-Ereignishandler eines Steuer Elements aufgerufen wird <xref:System.Windows.Forms.Control.Paint> . Im Beispiel wird ein linearer Farbverlaufs Pinsel erstellt und mithilfe dieses Pinsels zwei Rechtecke aufgefüllt. Das erste Rechteck wird ohne Gammakorrektur gefüllt, und das zweite Rechteck wird mit der Gammakorrektur gefüllt.  
  
 Die folgende Abbildung zeigt die zwei gefüllten Rechtecke. Das obere Rechteck, das keine Gammakorrektur hat, wird in der Mitte dunkel angezeigt. Das untere Rechteck, das über eine Gammakorrektur verfügt, scheint eine einheitlichere Intensität zu haben.  
  
 ![Zwei mit einem Farbverlauf gefüllte Rechtecke mit und ohne Gammakorrektur.](./media/how-to-apply-gamma-correction-to-a-gradient/two-rectangles-gamma-gradient.png)  
  
 [!code-csharp[System.Drawing.UsingaGradientBrush#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingaGradientBrush#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Drawing2D.LinearGradientBrush?displayProperty=nameWithType>
- [Verwenden eines Pinsels für Farbverläufe zum Ausfüllen von Formen](using-a-gradient-brush-to-fill-shapes.md)
