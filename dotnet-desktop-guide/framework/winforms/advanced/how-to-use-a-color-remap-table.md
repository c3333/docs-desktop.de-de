---
title: 'Vorgehensweise: Verwenden einer Farbneuzuordnungstabelle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- color tables [Windows Forms], remapping colors with
- custom colors [Windows Forms], creating with color remap table
- color remap tables [Windows Forms], using
ms.assetid: 977df1ce-8665-42d4-9fb1-ef7f0ff63419
ms.openlocfilehash: 360ec30563ee5001d784dc7c4ccdb50563867c29
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975859"
---
# <a name="how-to-use-a-color-remap-table"></a>Vorgehensweise: Verwenden einer Farbneuzuordnungstabelle
Beim Neuzuordnen werden die Farben in einem Bild entsprechend einer Farb Umwandlungs Tabelle umgerechnet. Die Farb Umwandlungs Tabelle ist ein Array von- <xref:System.Drawing.Imaging.ColorMap> Objekten. Jedes <xref:System.Drawing.Imaging.ColorMap> -Objekt im-Array verfügt über eine <xref:System.Drawing.Imaging.ColorMap.OldColor%2A> -Eigenschaft und eine- <xref:System.Drawing.Imaging.ColorMap.NewColor%2A> Eigenschaft.  
  
 Wenn GDI+ ein Bild zeichnet, wird jedes Pixel des Bilds mit dem Array Alter Farben verglichen. Wenn die Farbe eines Pixels mit einer alten Farbe übereinstimmt, wird seine Farbe in die entsprechende neue Farbe geändert. Die Farben werden nur für das Rendering geändert – die Farbwerte des Bilds selbst (in einem <xref:System.Drawing.Image> - <xref:System.Drawing.Bitmap> Objekt oder-Objekt gespeichert) werden nicht geändert.  
  
 Um ein neu zugeordnete Bild zu zeichnen, initialisieren Sie ein Array von- <xref:System.Drawing.Imaging.ColorMap> Objekten. Übergeben Sie dieses Array an die <xref:System.Drawing.Imaging.ImageAttributes.SetRemapTable%2A> -Methode eines <xref:System.Drawing.Imaging.ImageAttributes> -Objekts, und übergeben Sie dann das- <xref:System.Drawing.Imaging.ImageAttributes> Objekt an die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datei RemapInput.bmp erstellt. Der Code erstellt eine Farb Umwandlungs Tabelle, die aus einem einzelnen- <xref:System.Drawing.Imaging.ColorMap> Objekt besteht. Die <xref:System.Drawing.Imaging.ColorMap.OldColor%2A> -Eigenschaft des `ColorRemap` -Objekts ist rot, und die- <xref:System.Drawing.Imaging.ColorMap.NewColor%2A> Eigenschaft ist blau. Das Bild wird einmal ohne Neuzuordnen und einmal mit Neuzuordnung gezeichnet. Der neuzustellungs Prozess ändert alle roten Pixel in blau.  
  
 Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das neu zugeordnete Bild auf der rechten Seite.  
  
 ![Screenshot, der das ursprüngliche Bild und das neu zugeordnete Bild anzeigt.](./media/how-to-use-a-color-remap-table/original-image-remap-colors.png)  
  
 [!code-csharp[System.Drawing.RecoloringImages#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.RecoloringImages#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- [Neueinfärben von Bildern](recoloring-images.md)
- [Bilder, Bitmaps und Metadatendateien](images-bitmaps-and-metafiles.md)
