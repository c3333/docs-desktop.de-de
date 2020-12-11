---
title: Ändern der Darstellung von TabControl
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- icons [Windows Forms], displaying on tabs
- TabControl control [Windows Forms], changing page appearance
- tabs [Windows Forms], controlling appearance
- buttons [Windows Forms], displaying tabs as
ms.assetid: 7c6cc443-ed62-4d26-b94d-b8913b44f773
ms.openlocfilehash: 056070177e6bbaba0c93c7b94f5adfd7887be6a8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976352"
---
# <a name="how-to-change-the-appearance-of-the-windows-forms-tabcontrol"></a><span data-ttu-id="4780e-102">Vorgehensweise: Ändern der Darstellung der TabControl-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4780e-102">How to: Change the Appearance of the Windows Forms TabControl</span></span>
<span data-ttu-id="4780e-103">Sie können die Darstellung von Registerkarten in Windows Forms ändern, indem Sie die Eigenschaften des <xref:System.Windows.Forms.TabControl> -Objekts und das- <xref:System.Windows.Forms.TabPage> Objekt verwenden, die die einzelnen Registerkarten des Steuer Elements bilden.</span><span class="sxs-lookup"><span data-stu-id="4780e-103">You can change the appearance of tabs in Windows Forms by using properties of the <xref:System.Windows.Forms.TabControl> and the <xref:System.Windows.Forms.TabPage> objects that make up the individual tabs on the control.</span></span> <span data-ttu-id="4780e-104">Durch Festlegen dieser Eigenschaften können Sie Bilder auf Registerkarten anzeigen, Registerkarten vertikal anstatt horizontal anzeigen, mehrere Zeilen von Registerkarten anzeigen und Registerkarten Programm gesteuert aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4780e-104">By setting these properties, you can display images on tabs, display tabs vertically instead of horizontally, display multiple rows of tabs, and enable or disable tabs programmatically.</span></span>  
  
### <a name="to-display-an-icon-on-the-label-part-of-a-tab"></a><span data-ttu-id="4780e-105">So zeigen Sie ein Symbol auf dem Bezeichnungs Teil einer Registerkarte an</span><span class="sxs-lookup"><span data-stu-id="4780e-105">To display an icon on the label part of a tab</span></span>  
  
1. <span data-ttu-id="4780e-106">Fügen Sie <xref:System.Windows.Forms.ImageList> dem Formular ein-Steuerelement hinzu.</span><span class="sxs-lookup"><span data-stu-id="4780e-106">Add an <xref:System.Windows.Forms.ImageList> control to the form.</span></span>  
  
2. <span data-ttu-id="4780e-107">Fügen Sie der Bildliste Bilder hinzu.</span><span class="sxs-lookup"><span data-stu-id="4780e-107">Add images to the image list.</span></span>  
  
     <span data-ttu-id="4780e-108">Weitere Informationen zu Bildlisten finden Sie unter [ImageList-Komponente](imagelist-component-windows-forms.md) und Gewusst [wie: Hinzufügen oder Entfernen von Bildern mit der Windows Forms ImageList-Komponente](how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span><span class="sxs-lookup"><span data-stu-id="4780e-108">For more information about image lists, see [ImageList Component](imagelist-component-windows-forms.md) and [How to: Add or Remove Images with the Windows Forms ImageList Component](how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span></span>  
  
3. <span data-ttu-id="4780e-109">Legen Sie die- <xref:System.Windows.Forms.TabControl.ImageList%2A> Eigenschaft von <xref:System.Windows.Forms.TabControl> auf das-Steuerelement fest <xref:System.Windows.Forms.ImageList> .</span><span class="sxs-lookup"><span data-stu-id="4780e-109">Set the <xref:System.Windows.Forms.TabControl.ImageList%2A> property of the <xref:System.Windows.Forms.TabControl> to the <xref:System.Windows.Forms.ImageList> control.</span></span>  
  
4. <span data-ttu-id="4780e-110">Legen Sie die- <xref:System.Windows.Forms.TabPage.ImageIndex%2A> Eigenschaft des-Objekts <xref:System.Windows.Forms.TabPage> auf den Index eines entsprechenden Bilds in der Liste fest.</span><span class="sxs-lookup"><span data-stu-id="4780e-110">Set the <xref:System.Windows.Forms.TabPage.ImageIndex%2A> property of the <xref:System.Windows.Forms.TabPage> to the index of an appropriate image in the list.</span></span>  
  
### <a name="to-create-multiple-rows-of-tabs"></a><span data-ttu-id="4780e-111">So erstellen Sie mehrere Zeilen von Registerkarten</span><span class="sxs-lookup"><span data-stu-id="4780e-111">To create multiple rows of tabs</span></span>  
  
1. <span data-ttu-id="4780e-112">Fügen Sie die gewünschte Anzahl von Registerkarten hinzu.</span><span class="sxs-lookup"><span data-stu-id="4780e-112">Add the number of tab pages you want.</span></span>  
  
2. <span data-ttu-id="4780e-113">Legen Sie die <xref:System.Windows.Forms.TabControl.Multiline%2A>-Eigenschaft von <xref:System.Windows.Forms.TabControl> auf `true` fest.</span><span class="sxs-lookup"><span data-stu-id="4780e-113">Set the <xref:System.Windows.Forms.TabControl.Multiline%2A> property of the <xref:System.Windows.Forms.TabControl> to `true`.</span></span>  
  
3. <span data-ttu-id="4780e-114">Wenn die Registerkarten nicht bereits in mehreren Zeilen angezeigt werden, legen <xref:System.Windows.Forms.Control.Width%2A> Sie die-Eigenschaft von auf einen engeren Wert fest <xref:System.Windows.Forms.TabControl> als alle Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="4780e-114">If the tabs do not already appear in multiple rows, set the <xref:System.Windows.Forms.Control.Width%2A> property of the <xref:System.Windows.Forms.TabControl> to be narrower than all the tabs.</span></span>  
  
### <a name="to-arrange-tabs-on-the-side-of-the-control"></a><span data-ttu-id="4780e-115">So ordnen Sie Registerkarten auf der Seite des Steuer Elements an</span><span class="sxs-lookup"><span data-stu-id="4780e-115">To arrange tabs on the side of the control</span></span>  
  
- <span data-ttu-id="4780e-116">Legen Sie die- <xref:System.Windows.Forms.TabControl.Alignment%2A> Eigenschaft von <xref:System.Windows.Forms.TabControl> auf <xref:System.Windows.Forms.TabAlignment.Left> oder fest <xref:System.Windows.Forms.TabAlignment.Right> .</span><span class="sxs-lookup"><span data-stu-id="4780e-116">Set the <xref:System.Windows.Forms.TabControl.Alignment%2A> property of the <xref:System.Windows.Forms.TabControl> to <xref:System.Windows.Forms.TabAlignment.Left> or <xref:System.Windows.Forms.TabAlignment.Right>.</span></span>  
  
### <a name="to-programmatically-enable-or-disable-all-controls-on-a-tab"></a><span data-ttu-id="4780e-117">So aktivieren oder deaktivieren Sie alle Steuerelemente auf einer Registerkarte Programm gesteuert</span><span class="sxs-lookup"><span data-stu-id="4780e-117">To programmatically enable or disable all controls on a tab</span></span>  
  
1. <span data-ttu-id="4780e-118">Legen Sie die- <xref:System.Windows.Forms.TabPage.Enabled%2A> Eigenschaft von <xref:System.Windows.Forms.TabPage> auf `true` oder fest `false` .</span><span class="sxs-lookup"><span data-stu-id="4780e-118">Set the <xref:System.Windows.Forms.TabPage.Enabled%2A> property of the <xref:System.Windows.Forms.TabPage> to `true` or `false`.</span></span>  
  
    ```vb  
    TabPage1.Enabled = False  
    ```  
  
    ```csharp  
    tabPage1.Enabled = false;  
    ```  
  
    ```cpp  
    tabPage1->Enabled = false;  
    ```  
  
### <a name="to-display-tabs-as-buttons"></a><span data-ttu-id="4780e-119">Anzeigen von Registerkarten als Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="4780e-119">To display tabs as buttons</span></span>  
  
- <span data-ttu-id="4780e-120">Legen Sie die- <xref:System.Windows.Forms.TabControl.Appearance%2A> Eigenschaft von <xref:System.Windows.Forms.TabControl> auf <xref:System.Windows.Forms.TabAppearance.Buttons> oder fest <xref:System.Windows.Forms.TabAppearance.FlatButtons> .</span><span class="sxs-lookup"><span data-stu-id="4780e-120">Set the <xref:System.Windows.Forms.TabControl.Appearance%2A> property of the <xref:System.Windows.Forms.TabControl> to <xref:System.Windows.Forms.TabAppearance.Buttons> or <xref:System.Windows.Forms.TabAppearance.FlatButtons>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4780e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4780e-121">See also</span></span>

- [<span data-ttu-id="4780e-122">TabControl-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="4780e-122">TabControl Control</span></span>](tabcontrol-control-windows-forms.md)
- [<span data-ttu-id="4780e-123">Übersicht über das TabControl-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="4780e-123">TabControl Control Overview</span></span>](tabcontrol-control-overview-windows-forms.md)
- [<span data-ttu-id="4780e-124">Vorgehensweise: Hinzufügen eines Steuerelements zu einer Registerkarte</span><span class="sxs-lookup"><span data-stu-id="4780e-124">How to: Add a Control to a Tab Page</span></span>](how-to-add-a-control-to-a-tab-page.md)
- [<span data-ttu-id="4780e-125">Vorgehensweise: Deaktivieren von Registerkartenseiten</span><span class="sxs-lookup"><span data-stu-id="4780e-125">How to: Disable Tab Pages</span></span>](how-to-disable-tab-pages.md)
- [<span data-ttu-id="4780e-126">Vorgehensweise: Hinzufügen und Entfernen von Registerkarten mit dem TabControl-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4780e-126">How to: Add and Remove Tabs with the Windows Forms TabControl</span></span>](how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
