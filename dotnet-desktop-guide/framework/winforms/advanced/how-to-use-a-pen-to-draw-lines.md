---
title: 'Vorgehensweise: Verwenden eines Stifts zum Zeichnen von Linien'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lines [Windows Forms], drawing
- pens [Windows Forms], drawing lines
ms.assetid: 0828c331-a438-4bdd-a4d6-3ef1e59e8795
ms.openlocfilehash: 263c0fbda377e64753cd2d607f633117b4b44253
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976108"
---
# <a name="how-to-use-a-pen-to-draw-lines"></a>Vorgehensweise: Verwenden eines Stifts zum Zeichnen von Linien
Um Linien zu zeichnen, benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt und ein- <xref:System.Drawing.Pen> Objekt. Das <xref:System.Drawing.Graphics> -Objekt stellt die <xref:System.Drawing.Graphics.DrawLine%2A> -Methode bereit, und das- <xref:System.Drawing.Pen> Objekt speichert Funktionen der Zeile, z. b. Farbe und Breite.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine Zeile von (20, 10) nach (300, 100) gezeichnet. Die erste Anweisung verwendet den- <xref:System.Drawing.Pen.%23ctor%2A> Klassenkonstruktor, um einen schwarzen Stift zu erstellen. Das einzige Argument, das an den <xref:System.Drawing.Pen.%23ctor%2A> Konstruktor übergeben wird, ist ein <xref:System.Drawing.Color> mit der-Methode erstelltes-Objekt <xref:System.Drawing.Color.FromArgb%2A> . Die Werte, die zum Erstellen des <xref:System.Drawing.Color> Objekts – (255, 0, 0, 0) – verwendet werden, entsprechen den Alpha-, rot-, grün-und blauen Komponenten der Farbe. Diese Werte definieren einen nicht transparenten schwarzen Stift.  
  
 [!code-csharp[System.Drawing.UsingAPen#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.UsingAPen#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Pen>
- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](using-a-pen-to-draw-lines-and-shapes.md)
- [Stifte, Linien und Rechtecke in GDI+](pens-lines-and-rectangles-in-gdi.md)
