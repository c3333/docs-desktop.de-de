---
title: 'Vorgehensweise: Erstellen eines linearen Farbverlaufs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- linear gradients [Windows Forms], creating
- gradients [Windows Forms], creating linear
- colors [Windows Forms], creating linear gradients
- gradients
ms.assetid: 6c88e1cc-1217-4399-ac12-cb37592b9f01
ms.openlocfilehash: e55d27b454579268658192ae56daa52e0b28bb83
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974988"
---
# <a name="how-to-create-a-linear-gradient"></a>Vorgehensweise: Erstellen eines linearen Farbverlaufs
GDI+ stellt horizontale, vertikale und diagonale lineare Farbverläufe bereit. Standardmäßig ändert sich die Farbe in einem linearen Farbverlauf gleichmäßig. Sie können jedoch einen linearen Farbverlauf anpassen, sodass sich die Farbe auf nicht einheitliche Weise ändert.  

> [!NOTE]
> Die Beispiele in diesem Artikel sind Methoden, die vom-Ereignishandler eines Steuer Elements aufgerufen werden <xref:System.Windows.Forms.Control.Paint> .  

Im folgenden Beispiel werden eine Linie, eine Ellipse und ein Rechteck mit einem horizontalen linearen Farbverlaufs Pinsel gefüllt.  
  
Der <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> Konstruktor empfängt vier Argumente: zwei Punkte und zwei Farben. Der erste Punkt (0, 10) ist mit der ersten Farbe (rot) verknüpft, und der zweite Punkt (200, 10) wird der zweiten Farbe (blau) zugeordnet. Erwartungsgemäß wird die von (0, 10) zu (200, 10) gezogene Linie allmählich von rot in blau geändert.  
  
 Die 10S in den Punkten (0,0) und (200, 10) sind nicht wichtig. Wichtig ist, dass die beiden Punkte dieselbe zweite Koordinate aufweisen – die Linie, die Sie verbindet, ist horizontal. Die Ellipse und das Rechteck ändern sich auch allmählich von rot in blau, wenn die horizontale Koordinate von 0 bis 200 wechselt.  
  
 Die folgende Abbildung zeigt die Zeile, die Ellipse und das Rechteck. Beachten Sie, dass der Farbverlauf selbst wiederholt wird, wenn sich die horizontale Koordinate über 200 erhöht.  
  
 ![Eine Linie, eine Ellipse und ein Rechteck, das mit einem Farbverlauf gefüllt ist.](./media/how-to-create-a-linear-gradient/gradient-line-ellipse-rectangle.png)  
  
## <a name="to-use-horizontal-linear-gradients"></a>So verwenden Sie horizontale lineare Farbverläufe  
  
- Übergeben Sie als drittes und viertes Argument das nicht transparente rote und undurchsichtiges blau.  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#21)]
     [!code-vb[System.Drawing.UsingaGradientBrush#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#21)]  
  
 Im vorherigen Beispiel ändern sich die Farbkomponenten linear, wenn Sie von einer horizontalen Koordinate von 0 zu einer horizontalen Koordinate von 200 wechseln. Beispielsweise weist ein Punkt, dessen erste Koordinate die Hälfte zwischen 0 und 200 ist, eine blaue Komponente auf, die sich in der Mitte zwischen 0 und 255 befindet.  
  
 Mit GDI+ können Sie die Art und Weise anpassen, in der eine Farbe von einem Rand eines Farbverlaufs zum anderen abweicht. Angenommen, Sie möchten einen Farbverlaufs Pinsel erstellen, der gemäß der folgenden Tabelle von schwarz in rot geändert wird.  
  
|Horizontale Koordinate|RGB-Komponenten|  
|---------------------------|--------------------|  
|0|(0, 0, 0)|  
|40|(128, 0, 0)|  
|200|(255, 0, 0)|  
  
 Beachten Sie, dass die rote Komponente die halbe Intensität hat, wenn die horizontale Koordinate nur 20 Prozent der Art von 0 bis 200 ist.  
  
 Im folgenden Beispiel wird die-Eigenschaft so festgelegt <xref:System.Drawing.Drawing2D.LinearGradientBrush.Blend%2A?displayProperty=nameWithType> , dass drei relative Intensitäten mit drei relativen Positionen verknüpft werden. Wie in der obigen Tabelle ist eine relative Intensität von 0,5 mit einer relativen Position von 0,2 verknüpft. Der Code füllt eine Ellipse und ein Rechteck mit dem Farbverlaufs Pinsel.  
  
 In der folgenden Abbildung werden die resultierende Ellipse und das Rechteck gezeigt.  
  
 ![Eine Ellipse und ein Rechteck, das mit einem horizontalen Farbverlauf gefüllt ist.](./media/how-to-create-a-linear-gradient/gradient-ellipse-rectangle.png)  

## <a name="to-customize-linear-gradients"></a>So passen Sie lineare Farbverläufe an  
  
- Übergeben Sie als drittes und viertes Argument das nicht transparente schwarze und undurchsichtiges rot.  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#22)]
     [!code-vb[System.Drawing.UsingaGradientBrush#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#22)]  
  
 Die Farbverläufe in den vorangehenden Beispielen waren horizontal. Das heißt, die Farbe ändert sich allmählich, wenn Sie sich entlang einer horizontalen Linie bewegen. Sie können auch vertikale Farbverläufe und diagonale Farbverläufe definieren.  
  
 Im folgenden Beispiel werden die Punkte (0,0) und (200, 100) an einen- <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> Konstruktor übergeben. Die Farbe blau ist (0,0) zugeordnet, und die Farbe grün ist zugeordnet (200, 100). Eine Linie (mit der Stift Breite 10) und eine Ellipse werden mit dem linearen Farbverlaufs Pinsel gefüllt.  
  
 Die folgende Abbildung zeigt die Zeile und die Ellipse. Beachten Sie, dass sich die Farbe in der Ellipse allmählich ändert, wenn Sie eine beliebige Zeile bewegen, die parallel zur Zeile, die durchläuft (0,0) und (200, 100).  
  
 ![Eine Linie und eine Ellipse, die mit einem diagonalen Farbverlauf gefüllt sind.](./media/how-to-create-a-linear-gradient/gradient-line-ellipse.png)  
  
## <a name="to-create-diagonal-linear-gradients"></a>So erstellen Sie diagonal lineare Farbverläufe  
  
- Übergeben Sie als drittes und viertes Argument das nicht transparente blaue und undurchsichtiges grün.  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#23)]
     [!code-vb[System.Drawing.UsingaGradientBrush#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#23)]  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden eines Pinsels für Farbverläufe zum Ausfüllen von Formen](using-a-gradient-brush-to-fill-shapes.md)
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
