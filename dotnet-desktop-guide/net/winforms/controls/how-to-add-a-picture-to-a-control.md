---
title: Anzeigen eines Bilds in einem Steuerelement
description: Hier erfahren Sie, wie Sie ein Bild in einem Windows Forms-Steuerelement anzeigen. Viele Steuerelemente (z. B. PictureBox) können ein Bild anzeigen.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Button control [Windows Forms], images
- Windows Forms controls, images
- controls [Windows Forms], images
- images [Windows Forms], Windows Forms contr ols
- examples [Windows Forms], controls
ms.openlocfilehash: a0b95d51f852df4c9ddc190903369faa41f7deae
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942068"
---
# <a name="how-to-display-an-image-on-a-control-windows-forms-net"></a>Anzeigen eines Bilds in einem Steuerelement (Windows Forms .NET)

Mehrere Windows Forms-Steuerelemente können Bilder anzeigen. Diese Bilder können Symbole sein, die den Zweck des Steuerelements verdeutlichen. Ein Beispiel hierfür ist ein Diskettensymbol auf einer Schaltfläche für den Befehl „Speichern“. Alternativ können die Symbole Hintergrundbilder sein, um dem Steuerelement das gewünschte Aussehen und Verhalten zu geben.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="designer"></a>Designer

Wählen Sie im Fenster **Eigenschaften** von Visual Studio die Eigenschaft **Image** oder **BackgroundImage** des Steuerelements aus, und klicken Sie dann auf die Auslassungspunkte (![Schaltfläche mit Auslassungspunkten in Visual Studio](../media/visual-studio-ellipsis-button.png)), um das Dialogfeld **Ressource auswählen** anzuzeigen und dann das Bild auszuwählen, das angezeigt werden soll.

:::image type="content" source="media/how-to-add-a-picture-to-a-control/properties-image.png" alt-text="Dialogfeld „Eigenschaften“ mit ausgewählter Image-Eigenschaft":::

## <a name="programmatic"></a>Programmgesteuert

Legen Sie die Eigenschaft `Image` oder `BackgroundImage` des Steuerelements auf ein Objekt des Typs <xref:System.Drawing.Image> fest. In der Regel laden Sie das Bild mithilfe der <xref:System.Drawing.Image.FromFile%2A>-Methode aus einer Datei.

Im folgenden Codebeispiel ist der Pfad, der für den Speicherort des Bilds festgelegt ist, der Ordner **Eigene Bilder**. Die meisten Computer mit Windows-Betriebssystem enthalten dieses Verzeichnis. Dadurch können auch Benutzer mit minimalen Systemzugriffsebenen die Anwendung sicher ausführen. Das folgende Codebeispiel setzt voraus, dass Sie bereits über ein Formular mit einem hinzugefügten <xref:System.Windows.Forms.PictureBox>-Steuerelement verfügen.

```csharp
// Replace the image named below with your own icon.
// Note the escape character used (@) when specifying the path.
pictureBox1.Image = Image.FromFile
   (System.Environment.GetFolderPath
   (System.Environment.SpecialFolder.MyPictures)
   + @"\Image.gif");
```

```vb
' Replace the image named below with your own icon.
PictureBox1.Image = Image.FromFile _
   (System.Environment.GetFolderPath _
   (System.Environment.SpecialFolder.MyPictures) _
   & "\Image.gif")
```

## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Image.FromFile%2A>
- <xref:System.Drawing.Image>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
