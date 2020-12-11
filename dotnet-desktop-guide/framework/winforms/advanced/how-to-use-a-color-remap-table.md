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
# <a name="how-to-use-a-color-remap-table"></a><span data-ttu-id="15226-102">Vorgehensweise: Verwenden einer Farbneuzuordnungstabelle</span><span class="sxs-lookup"><span data-stu-id="15226-102">How to: Use a Color Remap Table</span></span>
<span data-ttu-id="15226-103">Beim Neuzuordnen werden die Farben in einem Bild entsprechend einer Farb Umwandlungs Tabelle umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="15226-103">Remapping is the process of converting the colors in an image according to a color remap table.</span></span> <span data-ttu-id="15226-104">Die Farb Umwandlungs Tabelle ist ein Array von- <xref:System.Drawing.Imaging.ColorMap> Objekten.</span><span class="sxs-lookup"><span data-stu-id="15226-104">The color remap table is an array of <xref:System.Drawing.Imaging.ColorMap> objects.</span></span> <span data-ttu-id="15226-105">Jedes <xref:System.Drawing.Imaging.ColorMap> -Objekt im-Array verfügt über eine <xref:System.Drawing.Imaging.ColorMap.OldColor%2A> -Eigenschaft und eine- <xref:System.Drawing.Imaging.ColorMap.NewColor%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="15226-105">Each <xref:System.Drawing.Imaging.ColorMap> object in the array has an <xref:System.Drawing.Imaging.ColorMap.OldColor%2A> property and a <xref:System.Drawing.Imaging.ColorMap.NewColor%2A> property.</span></span>  
  
 <span data-ttu-id="15226-106">Wenn GDI+ ein Bild zeichnet, wird jedes Pixel des Bilds mit dem Array Alter Farben verglichen.</span><span class="sxs-lookup"><span data-stu-id="15226-106">When GDI+ draws an image, each pixel of the image is compared to the array of old colors.</span></span> <span data-ttu-id="15226-107">Wenn die Farbe eines Pixels mit einer alten Farbe übereinstimmt, wird seine Farbe in die entsprechende neue Farbe geändert.</span><span class="sxs-lookup"><span data-stu-id="15226-107">If a pixel's color matches an old color, its color is changed to the corresponding new color.</span></span> <span data-ttu-id="15226-108">Die Farben werden nur für das Rendering geändert – die Farbwerte des Bilds selbst (in einem <xref:System.Drawing.Image> - <xref:System.Drawing.Bitmap> Objekt oder-Objekt gespeichert) werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="15226-108">The colors are changed only for rendering — the color values of the image itself (stored in an <xref:System.Drawing.Image> or <xref:System.Drawing.Bitmap> object) are not changed.</span></span>  
  
 <span data-ttu-id="15226-109">Um ein neu zugeordnete Bild zu zeichnen, initialisieren Sie ein Array von- <xref:System.Drawing.Imaging.ColorMap> Objekten.</span><span class="sxs-lookup"><span data-stu-id="15226-109">To draw a remapped image, initialize an array of <xref:System.Drawing.Imaging.ColorMap> objects.</span></span> <span data-ttu-id="15226-110">Übergeben Sie dieses Array an die <xref:System.Drawing.Imaging.ImageAttributes.SetRemapTable%2A> -Methode eines <xref:System.Drawing.Imaging.ImageAttributes> -Objekts, und übergeben Sie dann das- <xref:System.Drawing.Imaging.ImageAttributes> Objekt an die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts.</span><span class="sxs-lookup"><span data-stu-id="15226-110">Pass that array to the <xref:System.Drawing.Imaging.ImageAttributes.SetRemapTable%2A> method of an <xref:System.Drawing.Imaging.ImageAttributes> object, and then pass the <xref:System.Drawing.Imaging.ImageAttributes> object to the <xref:System.Drawing.Graphics.DrawImage%2A> method of a <xref:System.Drawing.Graphics> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="15226-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="15226-111">Example</span></span>  
 <span data-ttu-id="15226-112">Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datei RemapInput.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="15226-112">The following example creates an <xref:System.Drawing.Image> object from the file RemapInput.bmp.</span></span> <span data-ttu-id="15226-113">Der Code erstellt eine Farb Umwandlungs Tabelle, die aus einem einzelnen- <xref:System.Drawing.Imaging.ColorMap> Objekt besteht.</span><span class="sxs-lookup"><span data-stu-id="15226-113">The code creates a color remap table that consists of a single <xref:System.Drawing.Imaging.ColorMap> object.</span></span> <span data-ttu-id="15226-114">Die <xref:System.Drawing.Imaging.ColorMap.OldColor%2A> -Eigenschaft des `ColorRemap` -Objekts ist rot, und die- <xref:System.Drawing.Imaging.ColorMap.NewColor%2A> Eigenschaft ist blau.</span><span class="sxs-lookup"><span data-stu-id="15226-114">The <xref:System.Drawing.Imaging.ColorMap.OldColor%2A> property of the `ColorRemap` object is red, and the <xref:System.Drawing.Imaging.ColorMap.NewColor%2A> property is blue.</span></span> <span data-ttu-id="15226-115">Das Bild wird einmal ohne Neuzuordnen und einmal mit Neuzuordnung gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="15226-115">The image is drawn once without remapping and once with remapping.</span></span> <span data-ttu-id="15226-116">Der neuzustellungs Prozess ändert alle roten Pixel in blau.</span><span class="sxs-lookup"><span data-stu-id="15226-116">The remapping process changes all the red pixels to blue.</span></span>  
  
 <span data-ttu-id="15226-117">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das neu zugeordnete Bild auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="15226-117">The following illustration shows the original image on the left and the remapped image on the right.</span></span>  
  
 ![Screenshot, der das ursprüngliche Bild und das neu zugeordnete Bild anzeigt.](./media/how-to-use-a-color-remap-table/original-image-remap-colors.png)  
  
 [!code-csharp[System.Drawing.RecoloringImages#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.RecoloringImages#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="15226-119">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="15226-119">Compiling the Code</span></span>  
 <span data-ttu-id="15226-120">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="15226-120">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15226-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15226-121">See also</span></span>

- [<span data-ttu-id="15226-122">Neueinfärben von Bildern</span><span class="sxs-lookup"><span data-stu-id="15226-122">Recoloring Images</span></span>](recoloring-images.md)
- [<span data-ttu-id="15226-123">Bilder, Bitmaps und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="15226-123">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
