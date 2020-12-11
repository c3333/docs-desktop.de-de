---
title: 'Vorgehensweise: Abrufen von Schriftarteigenschaften'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [Windows Forms], obtaining metrics
- font metrics [Windows Forms], obtaining
ms.assetid: ff7c0616-67f7-4fa2-84ee-b8d642f2b09b
ms.openlocfilehash: 7d7ad92199bb8a8f01290066f8ae023a14c2f9ce
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976144"
---
# <a name="how-to-obtain-font-metrics"></a>Vorgehensweise: Abrufen von Schriftarteigenschaften
Die- <xref:System.Drawing.FontFamily> Klasse stellt die folgenden Methoden bereit, die verschiedene Metriken für eine bestimmte Kombination aus Familie und Stil abrufen:  
  
- <xref:System.Drawing.FontFamily.GetEmHeight%2A>FontStyle  
  
- <xref:System.Drawing.FontFamily.GetCellAscent%2A>FontStyle  
  
- <xref:System.Drawing.FontFamily.GetCellDescent%2A>FontStyle  
  
- <xref:System.Drawing.FontFamily.GetLineSpacing%2A>FontStyle  
  
 Die von diesen Methoden zurückgegebenen Werte sind in Schriftart Entwurfs Einheiten, sodass Sie unabhängig von der Größe und den Einheiten eines bestimmten <xref:System.Drawing.Font> Objekts sind.  
  
 Die folgende Abbildung zeigt die verschiedenen Metriken:
  
 ![Abbildung der Schriftart Metriken: Aufstieg, Abstieg und Zeilenabstand.](./media/how-to-obtain-font-metrics/various-font-metrics.png)  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden die Metriken für den regulären Stil der Arial-Schriftfamilie angezeigt. Der Code erstellt auch ein <xref:System.Drawing.Font> -Objekt (basierend auf der Arial-Familie) mit einer Größe von 16 Pixel und zeigt die Metriken (in Pixel) für das jeweilige <xref:System.Drawing.Font> Objekt an.  
  
 Die folgende Abbildung zeigt die Ausgabe des Beispielcodes:
  
 ![Beispielcode Ausgabe von Arial Schriftart Metriken.](./media/how-to-obtain-font-metrics/example-output-code-arial-font.png)  
  
 Beachten Sie die ersten beiden Zeilen der Ausgabe in der obigen Abbildung. Das <xref:System.Drawing.Font> -Objekt gibt eine Größe von 16 zurück, und das- <xref:System.Drawing.FontFamily> Objekt gibt eine EM-Höhe von 2.048 zurück. Diese beiden Zahlen (16 und 2.048) sind der Schlüssel für die Umstellung zwischen Schriftart Entwurfs Einheiten und den Einheiten (in diesem Fall Pixel) des- <xref:System.Drawing.Font> Objekts.  
  
 Beispielsweise können Sie den Aufstieg wie folgt von Entwurfs Einheiten in Pixel konvertieren:  
  
 ![Formel, die die Konvertierung von Entwurfs Einheiten in Pixel anzeigt](./media/how-to-obtain-font-metrics/convert-font-units-example.png)  
  
 Der folgende Code positioniert Text vertikal, indem der <xref:System.Drawing.PointF.Y%2A> Datenmember eines-Objekts festgelegt wird <xref:System.Drawing.PointF> . Die y-Koordinate wird von `font.Height` für jede neue Textzeile um erweitert. Die- <xref:System.Drawing.Font.Height%2A> Eigenschaft eines- <xref:System.Drawing.Font> Objekts gibt den Zeilenabstand (in Pixel) für dieses bestimmte <xref:System.Drawing.Font> Objekt zurück. In diesem Beispiel ist die von zurückgegebene Zahl <xref:System.Drawing.Font.Height%2A> 19. Beachten Sie, dass dies mit der Zahl (aufgerundet auf eine ganze Zahl) identisch ist, die durch das umrechnen der Zeilen Abstands Metrik in Pixel erreicht wurde.  
  
 Beachten Sie, dass die EM-Höhe (auch "size" oder "em size" genannt) nicht die Summe aus der Besteigung und der Abfahrt ist. Die Summe des Aufstiegs und der Abstieg wird als Zellhöhe bezeichnet. Die Zellen Höhe abzüglich der internen führenden ist gleich der EM-Höhe. Die Zellen Höhe zuzüglich der externen führenden ist gleich dem Zeilenabstand.  
  
 [!code-csharp[System.Drawing.FontsAndText#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.FontsAndText#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Verwenden von Schriftarten und Text](using-fonts-and-text.md)
