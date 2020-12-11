---
title: 'Vorgehensweise: Ändern der Größe oder Platzierung eines Bildes zur Laufzeit'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- images [Windows Forms], controlling placement in PictureBox control [Windows Forms]
- examples [Windows Forms], PictureBox control
- PictureBox control [Windows Forms], picture size and alignment
- pictures [Windows Forms], controlling placement in PictureBox control [Windows Forms]
ms.assetid: d0b332a3-fae2-4891-957c-dc3e17743326
ms.openlocfilehash: fea813d7b9fe585e35b729b8b64e3a5f414ef76d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975619"
---
# <a name="how-to-modify-the-size-or-placement-of-a-picture-at-run-time-windows-forms"></a>Gewusst wie: Ändern der Größe oder Platzierung eines Bildes zur Laufzeit (Windows Forms)
Wenn Sie das Windows Forms- <xref:System.Windows.Forms.PictureBox> Steuerelement in einem Formular verwenden, können Sie für die-Eigenschaft Folgendes festlegen <xref:System.Windows.Forms.PictureBox.SizeMode%2A> :  
  
- Ausrichten der oberen linken Ecke des Bilds mit der linken oberen Ecke des Steuer Elements  
  
- Zentrieren des Bilds innerhalb des Steuer Elements  
  
- Passen Sie die Größe des Steuer Elements an das Bild an, das es anzeigt.  
  
- Bildstrecken, das angezeigt wird, um das Steuerelement anzupassen  
  
 Das Strecken eines Bilds (insbesondere eines im Bitmapformat) kann zu einem Verlust bei der Bildqualität führen. Metadatendateien, die Listen mit Grafik Anweisungen zum Zeichnen von Bildern zur Laufzeit sind, eignen sich besser für die Streckung als Bitmaps.  
  
### <a name="to-set-the-sizemode-property-at-run-time"></a>So legen Sie die SizeMode-Eigenschaft zur Laufzeit fest  
  
1. Legen <xref:System.Windows.Forms.PictureBox.SizeMode%2A> Sie auf <xref:System.Windows.Forms.PictureBoxSizeMode.Normal> (die Standardeinstellung), <xref:System.Windows.Forms.PictureBoxSizeMode.AutoSize> , <xref:System.Windows.Forms.PictureBoxSizeMode.CenterImage> oder fest <xref:System.Windows.Forms.PictureBoxSizeMode.StretchImage> . <xref:System.Windows.Forms.PictureBoxSizeMode.Normal> bedeutet, dass das Bild in der linken oberen Ecke des Steuer Elements platziert wird. Wenn das Bild größer als das Steuerelement ist, werden die unteren und rechten Ränder abgeschnitten. <xref:System.Windows.Forms.PictureBoxSizeMode.CenterImage> bedeutet, dass das Bild im-Steuerelement zentriert ist. Wenn das Bild größer als das Steuerelement ist, werden die äußeren Ränder des Bilds abgeschnitten. <xref:System.Windows.Forms.PictureBoxSizeMode.AutoSize> bedeutet, dass die Größe des Steuer Elements an die Größe des Bilds angepasst wird. <xref:System.Windows.Forms.PictureBoxSizeMode.StretchImage> ist der umgekehrte und bedeutet, dass die Größe des Bilds an die Größe des Steuer Elements angepasst wird.  
  
     Im folgenden Beispiel ist der Pfad, der für den Speicherort des Bilds festgelegt ist, der Ordner "eigene Dateien". Dies geschieht, da Sie davon ausgehen können, dass die meisten Computer, auf denen das Windows-Betriebssystem ausgeführt wird, dieses Verzeichnis enthalten. Dadurch können auch Benutzer mit minimalen Systemzugriffsebenen die Anwendung sicher ausführen. Im folgenden Beispiel wird davon ausgegangen, dass ein Formular <xref:System.Windows.Forms.PictureBox> bereits hinzugefügt wurde.  
  
    ```vb  
    Private Sub StretchPic()  
       ' Stretch the picture to fit the control.  
       PictureBox1.SizeMode = PictureBoxSizeMode.StretchImage  
       ' Load the picture into the control.  
       ' You should replace the bold image
       ' in the sample below with an icon of your own choosing.  
       PictureBox1.Image = Image.FromFile _  
       (System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.Personal) _  
       & "\Image.gif")  
    End Sub  
    ```  
  
    ```csharp  
    private void StretchPic(){  
       // Stretch the picture to fit the control.  
       PictureBox1.SizeMode = PictureBoxSizeMode.StretchImage;  
       // Load the picture into the control.  
       // You should replace the bold image
       // in the sample below with an icon of your own choosing.  
       // Note the escape character used (@) when specifying the path.  
       PictureBox1.Image = Image.FromFile _  
       (System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.Personal) _  
       + @"\Image.gif")  
    }  
    ```  
  
    ```cpp  
    private:  
       void StretchPic()  
       {  
          // Stretch the picture to fit the control.  
          pictureBox1->SizeMode = PictureBoxSizeMode::StretchImage;  
          // Load the picture into the control.  
          // You should replace the bold image
          // in the sample below with an icon of your own choosing.  
          pictureBox1->Image = Image::FromFile(String::Concat(  
             System::Environment::GetFolderPath(  
             System::Environment::SpecialFolder::Personal),  
             "\\Image.gif"));  
       }  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.PictureBox>
- [Vorgehensweise: Laden eines Bilds mithilfe des Designers](how-to-load-a-picture-using-the-designer-windows-forms.md)
- [Übersicht über das PictureBox-Steuerelement](picturebox-control-overview-windows-forms.md)
- [Vorgehensweise: Festlegen von Bildern zur Laufzeit](how-to-set-pictures-at-run-time-windows-forms.md)
- [PictureBox-Steuerelement](picturebox-control-windows-forms.md)
