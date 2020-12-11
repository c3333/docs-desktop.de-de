---
title: Festlegen des Hintergrunds eines Bereichs
description: Erfahren Sie, wie Sie die Hintergrundfarbe und das Hintergrundbild eines Windows Forms Panel mit dem Designer festlegen.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- background colors [Windows Forms], Windows Forms Panel controls
- background images [Windows Forms], Windows Forms Panel controls
- Panel control [Windows Forms], background
- colors [Windows Forms], Windows Forms Panel controls
ms.assetid: 096cbd8d-45cc-47b8-b1ef-a27f60ea8be0
ms.openlocfilehash: 109ff6184de9c79d1576207bbeb29ad939670b6f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975429"
---
# <a name="how-to-set-the-background-of-a-windows-forms-panel"></a><span data-ttu-id="2c431-103">Gewusst wie: Festlegen des Hintergrunds eines Windows Forms-Bereichs</span><span class="sxs-lookup"><span data-stu-id="2c431-103">How to: Set the Background of a Windows Forms Panel</span></span>
<span data-ttu-id="2c431-104">Ein Windows Forms <xref:System.Windows.Forms.Panel> -Steuerelement kann sowohl eine Hintergrundfarbe als auch ein Hintergrundbild anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2c431-104">A Windows Forms <xref:System.Windows.Forms.Panel> control can display both a background color and a background image.</span></span> <span data-ttu-id="2c431-105">Die- <xref:System.Windows.Forms.Control.BackColor%2A> Eigenschaft legt die Hintergrundfarbe für die enthaltenen Steuerelemente fest, z. b. Bezeichnungen und Options Felder.</span><span class="sxs-lookup"><span data-stu-id="2c431-105">The <xref:System.Windows.Forms.Control.BackColor%2A> property sets the background color for the contained controls, such as labels and radio buttons.</span></span> <span data-ttu-id="2c431-106">Wenn die <xref:System.Windows.Forms.Control.BackgroundImage%2A> Eigenschaft nicht festgelegt ist, wird der gesamte Bereich durch die <xref:System.Windows.Forms.Control.BackColor%2A> Auswahl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="2c431-106">If the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property is not set, the <xref:System.Windows.Forms.Control.BackColor%2A> selection will fill the entire panel.</span></span> <span data-ttu-id="2c431-107">Wenn die- <xref:System.Windows.Forms.Control.BackgroundImage%2A> Eigenschaft festgelegt ist, wird das Bild hinter den enthaltenen Steuerelementen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c431-107">If the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property is set, the image will be displayed behind the contained controls.</span></span>  
  
### <a name="to-set-the-background-programmatically"></a><span data-ttu-id="2c431-108">So legen Sie den Hintergrundprogramm gesteuert fest</span><span class="sxs-lookup"><span data-stu-id="2c431-108">To set the background programmatically</span></span>  
  
1. <span data-ttu-id="2c431-109">Legen Sie die- <xref:System.Windows.Forms.Control.BackColor%2A> Eigenschaft des Panels auf einen Wert vom Typ fest <xref:System.Drawing.Color?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="2c431-109">Set the panel's <xref:System.Windows.Forms.Control.BackColor%2A> property to a value of type <xref:System.Drawing.Color?displayProperty=nameWithType>.</span></span>  
  
    ```vb  
    Panel1.BackColor = Color.AliceBlue  
    ```  
  
    ```csharp  
    panel1.BackColor = Color.AliceBlue;  
    ```  
  
    ```cpp  
    panel1->BackColor = Color::AliceBlue;  
    ```  
  
2. <span data-ttu-id="2c431-110">Legen Sie die- <xref:System.Windows.Forms.Control.BackgroundImage%2A> Eigenschaft des Panels mithilfe der- <xref:System.Drawing.Image.FromFile%2A> Methode der- <xref:System.Drawing.Image?displayProperty=nameWithType> Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="2c431-110">Set the panel's <xref:System.Windows.Forms.Control.BackgroundImage%2A> property using the <xref:System.Drawing.Image.FromFile%2A> method of the <xref:System.Drawing.Image?displayProperty=nameWithType> class.</span></span>  
  
    ```vb  
    ' You should replace the bolded image
    ' in the sample below with an image of your own choosing.  
    Panel1.BackgroundImage = Image.FromFile _  
        (System.Environment.GetFolderPath _  
        (System.Environment.SpecialFolder.Personal) _  
        & "\Image.gif")  
    ```  
  
    ```csharp  
    // You should replace the bolded image
    // in the sample below with an image of your own choosing.  
    // Note the escape character used (@) when specifying the path.  
    panel1.BackgroundImage = Image.FromFile  
       (System.Environment.GetFolderPath  
       (System.Environment.SpecialFolder.Personal)  
       + @"\Image.gif");  
    ```  
  
    ```cpp  
    // You should replace the bolded image
    // in the sample below with an image of your own choosing.  
    panel1->BackgroundImage = Image::FromFile(String::Concat(  
       System::Environment::GetFolderPath  
       (System::Environment::SpecialFolder::Personal),  
       "\\Image.gif"));  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="2c431-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c431-111">See also</span></span>

- <xref:System.Windows.Forms.Control.BackColor%2A>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
- [<span data-ttu-id="2c431-112">Panelsteuerelement</span><span class="sxs-lookup"><span data-stu-id="2c431-112">Panel Control</span></span>](panel-control-windows-forms.md)
- [<span data-ttu-id="2c431-113">Übersicht über das Panel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="2c431-113">Panel Control Overview</span></span>](panel-control-overview-windows-forms.md)
