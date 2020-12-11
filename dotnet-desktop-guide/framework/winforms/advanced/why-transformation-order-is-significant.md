---
title: Bedeutung der Transformationsreihenfolge
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- transformations [Windows Forms], order significance
ms.assetid: 37d5f9dc-a5cf-4475-aa5d-34d714e808a9
ms.openlocfilehash: 08927ebaa460e19e558dce22f39c13c31f0e49d0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975815"
---
# <a name="why-transformation-order-is-significant"></a>Bedeutung der Transformationsreihenfolge
Ein einzelnes- <xref:System.Drawing.Drawing2D.Matrix> Objekt kann eine einzelne Transformation oder eine Sequenz von Transformationen speichern. Letzteres wird als zusammengesetzte Transformation bezeichnet. Die Matrix einer zusammengesetzten Transformation wird abgerufen, indem die Matrizen einzelner Transformationen multipliziert werden.  
  
## <a name="composite-transform-examples"></a>Beispiele für zusammengesetzte Transformation  
 In einer zusammengesetzten Transformation ist die Reihenfolge der einzelnen Transformationen wichtig. Wenn Sie z. b. zuerst drehen, dann skalieren und dann übersetzen, erhalten Sie ein anderes Ergebnis als bei der ersten Übersetzung, dann drehen und skalieren. In GDI+ werden zusammengesetzte Transformationen von links nach rechts erstellt. Wenn es sich bei S, R und T um Skalierungs-, Rotations-und Übersetzungs Matrizen handelt, ist das Produkt SRT (in dieser Reihenfolge) die Matrix der zusammengesetzten Transformation, die zuerst skaliert, dann rotiert und dann übersetzt. Die vom Produkt SRT erzeugte Matrix unterscheidet sich von der Matrix, die vom Produkt TRS erzeugt wird.  
  
 Eine Grundordnung ist wichtig, wenn Transformationen wie Drehung und Skalierung in Bezug auf den Ursprung des Koordinatensystems ausgeführt werden. Das Skalieren eines Objekts, das am Ursprung zentriert ist, erzeugt ein anderes Ergebnis als das Skalieren eines Objekts, das vom Ursprung entfernt wurde. Entsprechend erzeugt das Drehen eines Objekts, das am Ursprung zentriert ist, ein anderes Ergebnis als das Drehen eines Objekts, das vom Ursprung entfernt wurde.  
  
 Im folgenden Beispiel werden die Skalierung, Drehung und Übersetzung (in dieser Reihenfolge) kombiniert, um eine zusammengesetzte Transformation zu bilden. Das <xref:System.Drawing.Drawing2D.MatrixOrder.Append> an die-Methode über gegebene Argument <xref:System.Drawing.Graphics.RotateTransform%2A> gibt an, dass die Drehung der Skalierung folgt. Ebenso <xref:System.Drawing.Drawing2D.MatrixOrder.Append> gibt das an die-Methode übergebenen-Argument an <xref:System.Drawing.Graphics.TranslateTransform%2A> , dass die Übersetzung der Drehung folgt. <xref:System.Drawing.Drawing2D.MatrixOrder.Append> und <xref:System.Drawing.Drawing2D.MatrixOrder.Prepend> sind Member der- <xref:System.Drawing.Drawing2D.MatrixOrder> Enumeration.  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.MiscLegacyTopics#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#21)]  
  
 Im folgenden Beispiel wird dieselbe Methode wie im vorherigen Beispiel aufgerufen, aber die Reihenfolge der Aufrufe wird umgekehrt. Die sich ergebende Reihenfolge der Vorgänge wird zuerst übersetzt, dann drehen und dann skalieren, was ein sehr anderes Ergebnis als das erste skalieren und dann drehen und übersetzen liefert.  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#22)]
 [!code-vb[System.Drawing.MiscLegacyTopics#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#22)]  
  
 Eine Möglichkeit, die Reihenfolge einzelner Transformationen in einer zusammengesetzten Transformation umzukehren, besteht darin, die Reihenfolge einer Sequenz von Methoden aufrufen umzukehren. Eine zweite Möglichkeit, die Reihenfolge der Vorgänge zu steuern, besteht darin, das Matrix Reihen folgen Argument zu ändern. Das folgende Beispiel ist mit dem vorherigen Beispiel identisch, mit dem Unterschied, dass <xref:System.Drawing.Drawing2D.MatrixOrder.Append> in geändert wurde <xref:System.Drawing.Drawing2D.MatrixOrder.Prepend> . Die Matrix Multiplikation erfolgt in der Reihenfolge SRT, in der "S", "R" und "T" die Matrizen für "Scale", "Rotation" und "Translation" sind. Die Reihenfolge der zusammengesetzten Transformation ist die erste Skalierung, dann drehen und dann übersetzen.  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#23)]
 [!code-vb[System.Drawing.MiscLegacyTopics#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#23)]  
  
 Das Ergebnis des unmittelbar vorhergehenden Beispiels ist das gleiche wie das Ergebnis des ersten Beispiels in diesem Thema. Dies liegt daran, dass wir sowohl die Reihenfolge der Methodenaufrufe als auch die Reihenfolge der Matrix Multiplikation rückgängig gemacht haben.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Drawing2D.Matrix>
- [Koordinatensysteme und Transformationen](coordinate-systems-and-transformations.md)
- [Verwenden von Transformationen in Managed GDI+](using-transformations-in-managed-gdi.md)
