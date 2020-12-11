---
title: 'Vorgehensweise: Erstellen von Figuren aus Linien, Kurven und Formen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- figures [Windows Forms], creating from shapes
- figures [Windows Forms], creating from lines
ms.assetid: 82fd56c7-b443-4765-9b7c-62ce030656ec
ms.openlocfilehash: c8cf7a7e08bed56fb704bba4e30ff369bc3fcf89
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974828"
---
# <a name="how-to-create-figures-from-lines-curves-and-shapes"></a>Vorgehensweise: Erstellen von Figuren aus Linien, Kurven und Formen
Um eine Abbildung zu erstellen, erstellen Sie einen <xref:System.Drawing.Drawing2D.GraphicsPath> , und rufen Sie dann Methoden, wie z <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> . b <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A> . und, auf, um primitive dem Pfad hinzuzufügen.  
  
## <a name="example"></a>Beispiel  
 In den folgenden Codebeispielen werden Pfade mit Abbildungen erstellt:  
  
- Im ersten Beispiel wird ein Pfad erstellt, der über eine einzelne Abbildung verfügt. Die Abbildung besteht aus einem einzelnen Bogen. Der Bogen hat einen Mittelpunktswinkel von – 180 Grad, der im Standard Koordinatensystem gegen den Uhrzeigersinn steht.  
  
- Im zweiten Beispiel wird ein Pfad mit zwei Abbildungen erstellt. Die erste Abbildung ist ein Bogen, gefolgt von einer Zeile. Die zweite Abbildung ist eine Zeile, auf die eine Kurve folgt, gefolgt von einer Zeile. Die erste Abbildung ist links geöffnet, und die zweite Abbildung ist geschlossen.  
  
 [!code-csharp[System.Drawing.ConstructingDrawingPaths#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.ConstructingDrawingPaths#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/VB/Class1.vb#21)]  
  
 [!code-csharp[System.Drawing.ConstructingDrawingPaths#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/CS/Class1.cs#22)]
 [!code-vb[System.Drawing.ConstructingDrawingPaths#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/VB/Class1.vb#22)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Die vorherigen Beispiele sind für die Verwendung mit Windows Forms konzipiert und erfordern <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Drawing2D.GraphicsPath>
- [Erstellen und Zeichnen von Pfaden](constructing-and-drawing-paths.md)
- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](using-a-pen-to-draw-lines-and-shapes.md)
