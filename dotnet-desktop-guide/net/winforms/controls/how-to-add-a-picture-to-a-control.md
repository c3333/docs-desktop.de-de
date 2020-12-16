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
# <a name="how-to-display-an-image-on-a-control-windows-forms-net"></a><span data-ttu-id="e2bd4-104">Anzeigen eines Bilds in einem Steuerelement (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="e2bd4-104">How to display an image on a control (Windows Forms .NET)</span></span>

<span data-ttu-id="e2bd4-105">Mehrere Windows Forms-Steuerelemente können Bilder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e2bd4-105">Several Windows Forms controls can display images.</span></span> <span data-ttu-id="e2bd4-106">Diese Bilder können Symbole sein, die den Zweck des Steuerelements verdeutlichen. Ein Beispiel hierfür ist ein Diskettensymbol auf einer Schaltfläche für den Befehl „Speichern“.</span><span class="sxs-lookup"><span data-stu-id="e2bd4-106">These images can be icons that clarify the purpose of the control, such as a diskette icon on a button denoting the Save command.</span></span> <span data-ttu-id="e2bd4-107">Alternativ können die Symbole Hintergrundbilder sein, um dem Steuerelement das gewünschte Aussehen und Verhalten zu geben.</span><span class="sxs-lookup"><span data-stu-id="e2bd4-107">Alternatively, the icons can be background images to give the control the appearance and behavior you want.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="designer"></a><span data-ttu-id="e2bd4-108">Designer</span><span class="sxs-lookup"><span data-stu-id="e2bd4-108">Designer</span></span>

<span data-ttu-id="e2bd4-109">Wählen Sie im Fenster **Eigenschaften** von Visual Studio die Eigenschaft **Image** oder **BackgroundImage** des Steuerelements aus, und klicken Sie dann auf die Auslassungspunkte (![Schaltfläche mit Auslassungspunkten in Visual Studio](../media/visual-studio-ellipsis-button.png)), um das Dialogfeld **Ressource auswählen** anzuzeigen und dann das Bild auszuwählen, das angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2bd4-109">In the **Properties** window of Visual Studio, select the **Image** or **BackgroundImage** property of the control, and then select the ellipsis (![Ellipsis button in Visual Studio](../media/visual-studio-ellipsis-button.png)) to display the **Select Resource** dialog box and then select the image you want to display.</span></span>

:::image type="content" source="media/how-to-add-a-picture-to-a-control/properties-image.png" alt-text="Dialogfeld „Eigenschaften“ mit ausgewählter Image-Eigenschaft":::

## <a name="programmatic"></a><span data-ttu-id="e2bd4-111">Programmgesteuert</span><span class="sxs-lookup"><span data-stu-id="e2bd4-111">Programmatic</span></span>

<span data-ttu-id="e2bd4-112">Legen Sie die Eigenschaft `Image` oder `BackgroundImage` des Steuerelements auf ein Objekt des Typs <xref:System.Drawing.Image> fest.</span><span class="sxs-lookup"><span data-stu-id="e2bd4-112">Set the control's `Image` or `BackgroundImage` property to an object of type <xref:System.Drawing.Image>.</span></span> <span data-ttu-id="e2bd4-113">In der Regel laden Sie das Bild mithilfe der <xref:System.Drawing.Image.FromFile%2A>-Methode aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="e2bd4-113">Generally, you'll be loading the image from a file by using the <xref:System.Drawing.Image.FromFile%2A> method.</span></span>

<span data-ttu-id="e2bd4-114">Im folgenden Codebeispiel ist der Pfad, der für den Speicherort des Bilds festgelegt ist, der Ordner **Eigene Bilder**.</span><span class="sxs-lookup"><span data-stu-id="e2bd4-114">In the following code example, the path set for the location of the image is the **My Pictures** folder.</span></span> <span data-ttu-id="e2bd4-115">Die meisten Computer mit Windows-Betriebssystem enthalten dieses Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e2bd4-115">Most computers running the Windows operating system include this directory.</span></span> <span data-ttu-id="e2bd4-116">Dadurch können auch Benutzer mit minimalen Systemzugriffsebenen die Anwendung sicher ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2bd4-116">This also enables users with minimal system access levels to run the application safely.</span></span> <span data-ttu-id="e2bd4-117">Das folgende Codebeispiel setzt voraus, dass Sie bereits über ein Formular mit einem hinzugefügten <xref:System.Windows.Forms.PictureBox>-Steuerelement verfügen.</span><span class="sxs-lookup"><span data-stu-id="e2bd4-117">The following code example requires that you already have a form with a <xref:System.Windows.Forms.PictureBox> control added.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="e2bd4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2bd4-118">See also</span></span>

- <xref:System.Drawing.Image.FromFile%2A>
- <xref:System.Drawing.Image>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
