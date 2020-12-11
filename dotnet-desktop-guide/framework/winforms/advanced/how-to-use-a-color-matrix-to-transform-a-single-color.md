---
title: 'Vorgehensweise: Verwenden einer Farbmatrix zum Transformieren einer Farbe'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image colors [Windows Forms], transforming
- color matrices [Windows Forms], using
ms.assetid: 44df4556-a433-49c0-ac0f-9a12063a5860
ms.openlocfilehash: 2df74e022b842f7e5c9ff80f6aeddfce51af5eab
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976116"
---
# <a name="how-to-use-a-color-matrix-to-transform-a-single-color"></a>Vorgehensweise: Verwenden einer Farbmatrix zum Transformieren einer Farbe
GDI+ stellt die <xref:System.Drawing.Image> -Klasse und die- <xref:System.Drawing.Bitmap> Klasse zum Speichern und Bearbeiten von Bildern bereit. <xref:System.Drawing.Image> -und <xref:System.Drawing.Bitmap> -Objekte speichern die Farbe jedes Pixels als 32-Bit-Zahl: 8 Bits für Rot, grün, blau und alpha. Jede der vier Komponenten ist eine Zahl zwischen 0 und 255, wobei 0 keine Intensität und 255 die volle Intensität darstellt. Die Alpha Komponente gibt die Transparenz der Farbe an: 0 ist vollständig transparent, und 255 ist vollständig undurchsichtig.  
  
 Ein Farb Vektor ist ein 4-Tupel im Formular (rot, grün, blau, Alpha). Der Farb Vektor (0, 255, 0, 255) stellt z. b. eine nicht transparente Farbe dar, die nicht rot oder blau ist, aber grün mit voller Intensität aufweist.  
  
 Eine weitere Konvention für das darstellen von Farben verwendet die Zahl 1 für die volle Intensität. Mithilfe dieser Konvention würde die im vorangehenden Absatz beschriebene Farbe durch den Vektor (0, 1, 0, 1) dargestellt werden. GDI+ verwendet die Konvention 1 als vollständige Intensität, wenn Farb Transformationen durchführt werden.  
  
 Sie können lineare Transformationen (Drehung, Skalierung und ähnliches) auf Farb Vektoren anwenden, indem Sie die Farb Vektoren mit einer 4 × 4-Matrix multiplizieren. Es ist jedoch nicht möglich, eine 4 × 4-Matrix zum Durchführen einer Übersetzung (Nonlinear) zu verwenden. Wenn Sie jedem der Farb Vektoren eine dummyminietkoordinate (z. b. die Zahl 1) hinzufügen, können Sie eine beliebige Kombination aus linearen Transformationen und Übersetzungen mit einer 5 × 5-Matrix anwenden. Eine Transformation, die aus einer linearen Transformation, gefolgt von einer Übersetzung, besteht, wird als affine Transformation bezeichnet.  
  
 Nehmen Sie beispielsweise an, Sie möchten mit der Farbe (0,2, 0,0, 0,4, 1,0) beginnen und die folgenden Transformationen anwenden:  
  
1. Doppelte der roten Komponente  
  
2. Fügen Sie 0,2 der roten, grünen und blauen Komponenten hinzu.  
  
 Die folgende Matrix Multiplikation führt das Transformations Paar in der aufgeführten Reihenfolge aus.  
  
 ![Screenshot einer Transformationsmatrix für Transformationen.](./media/how-to-use-a-color-matrix-to-transform-a-single-color/multiplication-color-matrix.gif)
  
 Die Elemente einer Farbmatrix werden nach Zeile und Spalte indiziert (null basiert). Der Eintrag in der fünften Zeile und die dritte Spalte der Matrix M werden z. b. durch M [4] [2] bezeichnet.  
  
 Die 5 × 5-Identitätsmatrix (in der folgenden Abbildung dargestellt) verfügt über 1 s auf der diagonalen und an allen anderen Orten. Wenn Sie einen Farb Vektor anhand der Identitätsmatrix multiplizieren, wird der Farb Vektor nicht geändert. Eine bequeme Möglichkeit zum bilden der Matrix einer Farb Transformation besteht darin, mit der Identitätsmatrix zu beginnen und eine kleine Änderung vorzunehmen, die die gewünschte Transformation erzeugt.  
  
 ![Screenshot einer 5 x 5-Identitätsmatrix für die Farb Transformation.](./media/how-to-use-a-color-matrix-to-transform-a-single-color/5x5-identity-matrix-color-transformation.gif)  
  
 Eine ausführlichere Erörterung von Matrizen und Transformationen finden Sie unter [Koordinatensysteme und Transformationen](coordinate-systems-and-transformations.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Bild mit allen Farben (0,2, 0,0, 0,4, 1,0) angenommen, und die in den vorherigen Abschnitten beschriebene Transformation wird angewendet.  
  
 Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das transformierte Bild auf der rechten Seite.  
  
 ![Ein Violettes Quadrat auf der linken Seite und ein Fuchsia-Quadrat auf der rechten Seite.](./media/how-to-use-a-color-matrix-to-transform-a-single-color/color-transformation.png)  
  
 Der Code im folgenden Beispiel verwendet die folgenden Schritte, um die Neueinfärbung durchzuführen:  
  
1. Initialisieren Sie ein- <xref:System.Drawing.Imaging.ColorMatrix> Objekt.  
  
2. Erstellen <xref:System.Drawing.Imaging.ImageAttributes> Sie ein-Objekt, und übergeben Sie das- <xref:System.Drawing.Imaging.ColorMatrix> Objekt an die- <xref:System.Drawing.Imaging.ImageAttributes.SetColorMatrix%2A> Methode des- <xref:System.Drawing.Imaging.ImageAttributes> Objekts.  
  
3. Übergeben Sie das- <xref:System.Drawing.Imaging.ImageAttributes> Objekt an die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts.  
  
 [!code-csharp[System.Drawing.RecoloringImages#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.RecoloringImages#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- [Neueinfärben von Bildern](recoloring-images.md)
- [Koordinatensysteme und Transformationen](coordinate-systems-and-transformations.md)
