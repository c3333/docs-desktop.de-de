---
title: 'Vorgehensweise: Verwenden des Mischmodus zum Steuern des Alphablendings'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- alpha blending [Windows Forms], compositing
- colors [Windows Forms], blending
- colors [Windows Forms], controlling transparency
ms.assetid: f331df2d-b395-4b0a-95be-24fec8c9bbb5
ms.openlocfilehash: 6863e59efa25323f80933bf8ab595316b430ef53
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976102"
---
# <a name="how-to-use-compositing-mode-to-control-alpha-blending"></a>Vorgehensweise: Verwenden des Mischmodus zum Steuern des Alphablendings
Es kann vorkommen, dass Sie eine Offscreen-Bitmap erstellen möchten, die über die folgenden Eigenschaften verfügt:  
  
- Farben haben alpha-Werte, die kleiner als 255 sind.  
  
- Farben werden bei der Erstellung der Bitmap nicht mit einander gemischt.  
  
- Wenn Sie die fertige Bitmap anzeigen, werden Farben in der Bitmap mit den Hintergrundfarben auf dem Anzeigegerät gemischt.  
  
 Um eine solche Bitmap zu erstellen, erstellen Sie ein leeres <xref:System.Drawing.Bitmap> -Objekt, und erstellen Sie dann ein- <xref:System.Drawing.Graphics> Objekt, das auf dieser Bitmap basiert. Legen Sie den Zusammensetzung-Modus des- <xref:System.Drawing.Graphics> Objekts auf fest <xref:System.Drawing.Drawing2D.CompositingMode.SourceCopy?displayProperty=nameWithType> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Drawing.Graphics> Objekt basierend auf einem- <xref:System.Drawing.Bitmap> Objekt erstellt. Der Code verwendet das- <xref:System.Drawing.Graphics> Objekt zusammen mit zwei semitransparenten Pinseln (Alpha = 160), um die Bitmap zu zeichnen. Der Code füllt eine rote Ellipse und eine grüne Ellipse mithilfe der semitransparenten Pinsel. Die grüne Ellipse überlappt die rote Ellipse, das grüne wird jedoch nicht mit der roten Ellipse kombiniert, da der Zusammensetzung-Modus des- <xref:System.Drawing.Graphics> Objekts auf festgelegt ist <xref:System.Drawing.Drawing2D.CompositingMode.SourceCopy> .  
  
 Der Code zeichnet die Bitmap zweimal auf dem Bildschirm: einmal auf einem weißen Hintergrund und einmal in einem mehrfarbigen Hintergrund. Die Pixel in der Bitmap, die Teil der beiden Ellipsen sind, haben eine Alpha Komponente von 160, sodass die Ellipsen mit den Hintergrundfarben auf dem Bildschirm kombiniert werden.  
  
 Die folgende Abbildung zeigt die Ausgabe des Code Beispiels. Beachten Sie, dass die Ellipsen mit dem Hintergrund kombiniert werden, aber nicht miteinander vermischt werden.  
  
 ![Das Diagramm zeigt Ellipsen, die mit dem Hintergrund gemischt sind, nicht gegenseitig.](./media/how-to-use-compositing-mode-to-control-alpha-blending/ellipses-blended-background.png)  
  
 Das Codebeispiel enthält diese Anweisung:  
  
 [!code-csharp[System.Drawing.AlphaBlending#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlphaBlending/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.AlphaBlending#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlphaBlending/VB/Class1.vb#41)]  
  
 Wenn Sie möchten, dass die Ellipsen miteinander und mit dem Hintergrund kombiniert werden sollen, ändern Sie die Anweisung wie folgt:  
  
 [!code-csharp[System.Drawing.AlphaBlending#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlphaBlending/CS/Class1.cs#42)]
 [!code-vb[System.Drawing.AlphaBlending#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlphaBlending/VB/Class1.vb#42)]  
  
 Die folgende Abbildung zeigt die Ausgabe des überarbeiteten Codes.  
  
 ![Diagramm, das Ellipsen zeigt, die miteinander gemischt und mit Hintergrund kombiniert werden.](./media/how-to-use-compositing-mode-to-control-alpha-blending/blend-ellipses-background.png)  
  
 [!code-csharp[System.Drawing.AlphaBlending#43](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlphaBlending/CS/Class1.cs#43)]
 [!code-vb[System.Drawing.AlphaBlending#43](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlphaBlending/VB/Class1.vb#43)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Color.FromArgb%2A>
- [Alphablending von Linien und Füllungen](alpha-blending-lines-and-fills.md)
