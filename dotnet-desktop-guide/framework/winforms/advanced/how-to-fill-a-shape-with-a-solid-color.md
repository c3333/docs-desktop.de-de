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
# <a name="how-to-fill-a-shape-with-a-solid-color"></a>Vorgehensweise: Ausfüllen einer Form mit einer Volltonfarbe
Um eine Form mit einer voll Tonfarbe auszufüllen, erstellen Sie ein <xref:System.Drawing.SolidBrush> -Objekt, und übergeben Sie das <xref:System.Drawing.SolidBrush> Objekt dann als Argument an eine der Fill-Methoden der- <xref:System.Drawing.Graphics> Klasse. Im folgenden Beispiel wird gezeigt, wie eine Ellipse mit der Farbe rot gefüllt wird.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Code nimmt der- <xref:System.Drawing.SolidBrush.%23ctor%2A> Konstruktor ein- <xref:System.Drawing.Color> Objekt als einziges Argument an. Die Werte, die von der-Methode verwendet werden, <xref:System.Drawing.Color.FromArgb%2A> stellen die Alpha-, rot-, grün-und Blau-Komponenten der Farbe dar. Jeder dieser Werte muss zwischen 0 und 255 liegen. Der erste 255 gibt an, dass die Farbe vollständig undurchsichtig ist, und der zweite 255 gibt an, dass die rote Komponente vollständig ist. Die beiden Nullen zeigen an, dass die grünen und blauen Komponenten beide eine Intensität von 0 aufweisen.  
  
 Die vier Zahlen (0, 0, 100, 60), die an die-Methode übergeben werden, <xref:System.Drawing.Graphics.FillEllipse%2A> geben den Speicherort und die Größe des umschließenden Rechtecks für die Ellipse an. Das Rechteck hat eine linke obere Ecke von (0,0), eine Breite von 100 und eine Höhe von 60.  
  
 [!code-csharp[System.Drawing.UsingABrush#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.UsingABrush#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden eines Pinsels zum Ausfüllen von Formen](using-a-brush-to-fill-shapes.md)
