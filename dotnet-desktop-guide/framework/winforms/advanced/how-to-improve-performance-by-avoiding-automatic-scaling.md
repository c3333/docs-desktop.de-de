---
title: 'Vorgehensweise: Verbessern der Leistung durch das Vermeiden der automatischen Skalierung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- automatic scaling
- images [Windows Forms], improving performance
- images [Windows Forms], using without automatic scaling
- performance [Windows Forms], improving image
ms.assetid: 5fe2c95d-8653-4d55-bf0d-e5afa28f223b
ms.openlocfilehash: dd1a1545dce33de1ce11938db8495ebf311dadda
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975907"
---
# <a name="how-to-improve-performance-by-avoiding-automatic-scaling"></a>Vorgehensweise: Verbessern der Leistung durch das Vermeiden der automatischen Skalierung
GDI+ kann ein Abbild beim Zeichnen automatisch skalieren, wodurch die Leistung beeinträchtigt wird. Alternativ können Sie die Skalierung des Bilds steuern, indem Sie die Dimensionen des Ziel Rechtecks an die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode übergeben.  
  
 Beispielsweise gibt der folgende-Aufrufe der- <xref:System.Drawing.Graphics.DrawImage%2A> Methode eine linke obere Ecke von (50, 30) an, gibt jedoch kein Ziel Rechteck an.  
  
 [!code-csharp[System.Drawing.WorkingWithImages#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.WorkingWithImages#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#31)]  
  
 Obwohl dies die einfachste Version der- <xref:System.Drawing.Graphics.DrawImage%2A> Methode in Bezug auf die Anzahl der erforderlichen Argumente ist, ist dies nicht unbedingt die effizienteste Methode. Wenn die von GDI+ (in der Regel 96 Punkte pro Zoll) verwendete Auflösung von der im-Objekt gespeicherten Auflösung abweicht <xref:System.Drawing.Image> , wird das Bild von der- <xref:System.Drawing.Graphics.DrawImage%2A> Methode skaliert. Nehmen wir beispielsweise an, ein <xref:System.Drawing.Image> Objekt hat eine Breite von 216 Pixeln und einen gespeicherten horizontalen Auflösungswert von 72 Punkten pro Zoll. Da 216/72 gleich 3 ist, <xref:System.Drawing.Graphics.DrawImage%2A> wird das Bild von so skaliert, dass es eine Breite von 3 Zoll bei einer Auflösung von 96 Punkten pro Zoll aufweist. Das heißt, es <xref:System.Drawing.Graphics.DrawImage%2A> wird ein Bild mit einer Breite von 96x3 = 288 Pixel angezeigt.  
  
 Auch wenn die Bildschirmauflösung von 96 Punkten pro Zoll abweicht, skaliert GDI+ das Bild wahrscheinlich so, als ob es sich bei der Bildschirmauflösung um 96 Punkte pro Zoll handelt. Das liegt daran, dass ein GDI+ <xref:System.Drawing.Graphics> -Objekt einem Gerätekontext zugeordnet ist, und wenn GDI+ den Gerätekontext für die Bildschirmauflösung abfragt, ist das Ergebnis in der Regel 96, unabhängig von der tatsächlichen Bildschirmauflösung. Sie können die automatische Skalierung vermeiden, indem Sie das Ziel Rechteck in der- <xref:System.Drawing.Graphics.DrawImage%2A> Methode angeben.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird das gleiche Bild zweimal gezeichnet. Im ersten Fall werden die Breite und Höhe des Ziel Rechtecks nicht angegeben, und das Bild wird automatisch skaliert. Im zweiten Fall werden Breite und Höhe (gemessen in Pixel) des Ziel Rechtecks als identisch mit der Breite und Höhe des ursprünglichen Bilds angegeben. Die folgende Abbildung zeigt, wie das Bild zweimal gerendert wird:  
  
 ![Screenshot, der Bilder mit skalierter Textur anzeigt.](./media/how-to-improve-performance-by-avoiding-automatic-scaling/two-scaled-texture-images.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#32](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#32)]
 [!code-vb[System.Drawing.WorkingWithImages#32](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#32)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist. Ersetzen Sie Texture.jpg durch einen Bildnamen und einen Pfad, die auf Ihrem System gültig sind.  
  
## <a name="see-also"></a>Siehe auch

- [Bilder, Bitmaps und Metadatendateien](images-bitmaps-and-metafiles.md)
- [Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien](working-with-images-bitmaps-icons-and-metafiles.md)
