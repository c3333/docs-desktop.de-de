---
title: 'Vorgehensweise: Darstellen von Bildern mit GDI+'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- images [Windows Forms], creating
- GDI+, rendering existing images
ms.assetid: c128b79a-3e31-47d8-9e66-3470f570a056
ms.openlocfilehash: fffe1f1052d7323d234985b7e752866f2e89657d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976138"
---
# <a name="how-to-render-images-with-gdi"></a>Vorgehensweise: Darstellen von Bildern mit GDI+
Sie können GDI+ zum Rendering von Bildern verwenden, die als Dateien in Ihren Anwendungen vorhanden sind. Hierzu erstellen Sie ein neues-Objekt einer- <xref:System.Drawing.Image> Klasse (z. b. <xref:System.Drawing.Bitmap> ), erstellen ein <xref:System.Drawing.Graphics> -Objekt, das auf die zu verwendende Zeichnungs Oberfläche verweist, und rufen die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode des-Objekts auf <xref:System.Drawing.Graphics> . Das Bild wird auf die Zeichenoberfläche gezeichnet, die durch die Grafikklasse dargestellt wird. Sie können die Bildbearbeitung zum Erstellen und Bearbeiten von Bilddateien zur Entwurfszeit verwenden und Sie zur Laufzeit mit GDI+ Renderen. Weitere Informationen finden Sie unter [Bildbearbeitung für Symbole](/cpp/windows/image-editor-for-icons).  
  
### <a name="to-render-an-image-with-gdi"></a>So rendern Sie ein Bild mit GDI+  
  
1. Erstellen Sie ein Objekt, das das anzuzeigende Bild darstellt. Dieses Objekt muss ein Member einer Klasse sein, die von erbt <xref:System.Drawing.Image> , z <xref:System.Drawing.Bitmap> . b <xref:System.Drawing.Imaging.Metafile> . oder. Ein Beispiel:  
  
    ```vb  
    ' Uses the System.Environment.GetFolderPath to get the path to the
    ' current user's MyPictures folder.  
    Dim myBitmap as New Bitmap _  
       (System.Environment.GetFolderPath _  
          (System.Environment.SpecialFolder.MyPictures))  
    ```  
  
    ```csharp  
    // Uses the System.Environment.GetFolderPath to get the path to the
    // current user's MyPictures folder.  
    Bitmap myBitmap = new Bitmap  
       (System.Environment.GetFolderPath  
          (System.Environment.SpecialFolder.MyPictures));  
    ```  
  
    ```cpp  
    // Uses the System.Environment.GetFolderPath to get the path to the
    // current user's MyPictures folder.  
    Bitmap^ myBitmap = gcnew Bitmap  
       (System::Environment::GetFolderPath  
          (System::Environment::SpecialFolder::MyPictures));  
    ```  
  
2. Erstellen Sie ein- <xref:System.Drawing.Graphics> Objekt, das die zu verwendende Zeichen Oberfläche darstellt. Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](how-to-create-graphics-objects-for-drawing.md).  
  
    ```vb  
    ' Creates a Graphics object that represents the drawing surface of
    ' Button1.  
    Dim g as Graphics = Button1.CreateGraphics  
    ```  
  
    ```csharp  
    // Creates a Graphics object that represents the drawing surface of
    // Button1.  
    Graphics g = Button1.CreateGraphics();  
    ```  
  
    ```cpp  
    // Creates a Graphics object that represents the drawing surface of
    // Button1.  
    Graphics^ g = button1->CreateGraphics();  
    ```  
  
3. Ruft den <xref:System.Drawing.Graphics.DrawImage%2A> des Grafik Objekts auf, um das Bild zu renderken. Sie müssen das Bild angeben, das gezeichnet werden soll, und die Koordinaten, an denen es gezeichnet werden soll.  
  
    ```vb  
    g.DrawImage(myBitmap, 1, 1)  
    ```  
  
    ```csharp  
    g.DrawImage(myBitmap, 1, 1);  
    ```  
  
    ```cpp  
    g->DrawImage(myBitmap, 1, 1);  
    ```  
  
## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit Grafikprogrammierung](getting-started-with-graphics-programming.md)
- [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](how-to-create-graphics-objects-for-drawing.md)
- [Stifte, Linien und Rechtecke in GDI+](pens-lines-and-rectangles-in-gdi.md)
- [Vorgehensweise: Zeichnen von Text in einem Windows Form](how-to-draw-text-on-a-windows-form.md)
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Zeichnen von Linien oder geschlossenen Figuren](/cpp/windows/drawing-lines-or-closed-figures-image-editor-for-icons)
- [Bildbearbeitung für Symbole](/cpp/windows/image-editor-for-icons)
