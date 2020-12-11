---
title: Festlegen des von einem Steuerelement angezeigten Bilds
ms.date: 08/20/2019
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Button control [Windows Forms], images
- Windows Forms controls, images
- controls [Windows Forms], images
- images [Windows Forms], Windows Forms controls
- examples [Windows Forms], controls
ms.assetid: 9445af8f-4f62-48b0-a3f6-068058964b9f
ms.openlocfilehash: 5df0068c8462bbaab0cb0135de1dd1b91ababe06
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976763"
---
# <a name="how-to-set-the-image-displayed-by-a-windows-forms-control"></a>Gewusst wie: Festlegen des von einem Windows Forms Steuerelement angezeigten Bilds

Mehrere Windows Forms Steuerelemente können Bilder anzeigen. Diese Bilder können Symbole sein, die den Zweck des Steuer Elements verdeutlichen, wie z. b. ein Diskettensymbol auf einer Schaltfläche, die den Befehl "Speichern" bezeichnet. Alternativ können die Symbole Hintergrundbilder sein, um dem Steuerelement das gewünschte Aussehen und Verhalten zu geben.

## <a name="programmatic"></a>Programmgesteuert

Legen Sie die- `Image` Eigenschaft oder-Eigenschaft des Steuer Elements `BackgroundImage` auf ein Objekt vom Typ fest <xref:System.Drawing.Image> . Im allgemeinen laden Sie das Bild mithilfe der-Methode aus einer Datei <xref:System.Drawing.Image.FromFile%2A> .

Im folgenden Codebeispiel ist der Pfad, der für den Speicherort des Bilds festgelegt wurde, der Ordner **eigene Bilder** . Die meisten Computer unter dem Windows-Betriebssystem enthalten dieses Verzeichnis. Dies ermöglicht es Benutzern mit minimalen System Zugriffsebenen, die Anwendung sicher auszuführen. Im folgenden Codebeispiel ist es erforderlich, dass Sie bereits über ein Formular mit einem <xref:System.Windows.Forms.PictureBox> hinzugefügten Steuerelement verfügen.

```vb
' Replace the image named below with your own icon.
PictureBox1.Image = Image.FromFile _
   (System.Environment.GetFolderPath _
   (System.Environment.SpecialFolder.MyPictures) _
   & "\Image.gif")
```

```csharp
// Replace the image named below with your own icon.
// Note the escape character used (@) when specifying the path.
pictureBox1.Image = Image.FromFile
   (System.Environment.GetFolderPath
   (System.Environment.SpecialFolder.MyPictures)
   + @"\Image.gif");
```

```cpp
// Replace the image named below with your own icon.
pictureBox1->Image = Image::FromFile(String::Concat
   (System::Environment::GetFolderPath
   (System::Environment::SpecialFolder::MyPictures),
   "\\Image.gif"));
```

## <a name="designer"></a>Designer

1. Wählen Sie im **Eigenschaften** Fenster von Visual Studio die **Bild** -oder **BackgroundImage** -Eigenschaft des Steuer Elements aus, und klicken Sie dann auf die Schaltfläche mit den Auslassungs Zeichen ( ![ Ellipsen in Visual Studio ](./media/visual-studio-ellipsis-button.png) ), um das Dialogfeld **Ressource auswählen** anzuzeigen.

2. Wählen Sie das Abbild aus, das Sie anzeigen möchten.

## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Image.FromFile%2A>
- <xref:System.Drawing.Image>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
