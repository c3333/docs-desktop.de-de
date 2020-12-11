---
title: Festlegen von Symbolen für das TreeView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- TreeView control [Windows Forms], node icons
- ImageList component [Windows Forms], adding images
- icons [Windows Forms], setting for TreeView control
- tree nodes in TreeView control [Windows Forms], icons
ms.assetid: c14ddcc0-e5a6-4c21-a2d5-6799fd491781
ms.openlocfilehash: e3d7fc35c6d9f70822cdd0b69dd12f3d469f4ffa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975439"
---
# <a name="how-to-set-icons-for-the-windows-forms-treeview-control"></a><span data-ttu-id="7d37e-102">Vorgehensweise: Festlegen von Symbolen für das TreeView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7d37e-102">How to: Set Icons for the Windows Forms TreeView Control</span></span>
<span data-ttu-id="7d37e-103">Das Windows Forms <xref:System.Windows.Forms.TreeView> Steuerelement kann Symbole neben den einzelnen Knoten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7d37e-103">The Windows Forms <xref:System.Windows.Forms.TreeView> control can display icons next to each node.</span></span> <span data-ttu-id="7d37e-104">Die Symbole werden direkt links neben dem Knoten Text positioniert.</span><span class="sxs-lookup"><span data-stu-id="7d37e-104">The icons are positioned to the immediate left of the node text.</span></span> <span data-ttu-id="7d37e-105">Um diese Symbole anzuzeigen, müssen Sie die Strukturansicht einem-Steuerelement zuordnen <xref:System.Windows.Forms.ImageList> .</span><span class="sxs-lookup"><span data-stu-id="7d37e-105">To display these icons, you must associate the tree view with an <xref:System.Windows.Forms.ImageList> control.</span></span> <span data-ttu-id="7d37e-106">Weitere Informationen zu Bildlisten finden Sie unter [ImageList-Komponente](imagelist-component-windows-forms.md) und Gewusst [wie: Hinzufügen oder Entfernen von Bildern mit der Windows Forms ImageList-Komponente](how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span><span class="sxs-lookup"><span data-stu-id="7d37e-106">For more information about image lists, see [ImageList Component](imagelist-component-windows-forms.md) and [How to: Add or Remove Images with the Windows Forms ImageList Component](how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7d37e-107">Ein Fehler in Microsoft .NET Framework-Version 1,1 verhindert, dass Bilder auf Knoten angezeigt werden, <xref:System.Windows.Forms.TreeView> Wenn die Anwendung aufruft <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="7d37e-107">A bug in Microsoft .NET Framework version 1.1 prevents images from appearing on <xref:System.Windows.Forms.TreeView> nodes when your application calls <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="7d37e-108">Um diesen Fehler zu umgehen, rufen <xref:System.Windows.Forms.Application.DoEvents%2A?displayProperty=nameWithType> Sie direkt nach dem Aufrufen von in Ihrer- `Main` Methode auf <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> .</span><span class="sxs-lookup"><span data-stu-id="7d37e-108">To work around this bug, call <xref:System.Windows.Forms.Application.DoEvents%2A?displayProperty=nameWithType> in your `Main` method immediately after calling <xref:System.Windows.Forms.Application.EnableVisualStyles%2A>.</span></span> <span data-ttu-id="7d37e-109">Dieser Fehler wurde in .NET Framework 2,0 behoben.</span><span class="sxs-lookup"><span data-stu-id="7d37e-109">This bug is fixed in .NET Framework 2.0.</span></span>  
  
### <a name="to-display-images-in-a-tree-view"></a><span data-ttu-id="7d37e-110">So zeigen Sie Bilder in einer Strukturansicht an</span><span class="sxs-lookup"><span data-stu-id="7d37e-110">To display images in a tree view</span></span>  
  
1. <span data-ttu-id="7d37e-111">Legen <xref:System.Windows.Forms.TreeView> Sie die-Eigenschaft des Steuer Elements <xref:System.Windows.Forms.TreeView.ImageList%2A> auf das vorhandene Steuerelement fest, das <xref:System.Windows.Forms.ImageList> Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="7d37e-111">Set the <xref:System.Windows.Forms.TreeView> control's <xref:System.Windows.Forms.TreeView.ImageList%2A> property to the existing <xref:System.Windows.Forms.ImageList> control you wish to use.</span></span>  
  
     <span data-ttu-id="7d37e-112">Diese Eigenschaften können im Designer mit dem Eigenschaftenfenster oder im Code festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7d37e-112">These properties can be set in the designer with the Properties window, or in code.</span></span>  
  
    ```vb  
    TreeView1.ImageList = ImageList1  
    ```  
  
    ```csharp  
    treeView1.ImageList = imageList1;  
    ```  
  
    ```cpp  
    treeView1->ImageList = imageList1;  
    ```  
  
2. <span data-ttu-id="7d37e-113">Legen Sie die Eigenschaften und des Knotens fest <xref:System.Windows.Forms.TreeNode.ImageIndex%2A> <xref:System.Windows.Forms.TreeNode.SelectedImageIndex%2A> .</span><span class="sxs-lookup"><span data-stu-id="7d37e-113">Set the node's <xref:System.Windows.Forms.TreeNode.ImageIndex%2A> and <xref:System.Windows.Forms.TreeNode.SelectedImageIndex%2A> properties.</span></span> <span data-ttu-id="7d37e-114">Die <xref:System.Windows.Forms.TreeNode.ImageIndex%2A> -Eigenschaft bestimmt das Bild, das für den normalen und erweiterten Status des Knotens angezeigt wird, und die- <xref:System.Windows.Forms.TreeNode.SelectedImageIndex%2A> Eigenschaft bestimmt das Bild, das für den ausgewählten Status des Knotens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7d37e-114">The <xref:System.Windows.Forms.TreeNode.ImageIndex%2A> property determines the image displayed for the node's normal and expanded states, and the <xref:System.Windows.Forms.TreeNode.SelectedImageIndex%2A> property determines the image displayed for the node's selected state.</span></span>  
  
     <span data-ttu-id="7d37e-115">Diese Eigenschaften können im Code oder im TreeNode-Editor festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7d37e-115">These properties can be set in code, or within the TreeNode Editor.</span></span> <span data-ttu-id="7d37e-116">Um den TreeNode-Editor zu öffnen, klicken Sie auf die Schaltfläche mit den Auslassungs Zeichen ( ![ ...) im Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ) neben der- <xref:System.Windows.Forms.TreeView.Nodes%2A> Eigenschaft auf der Eigenschaftenfenster.</span><span class="sxs-lookup"><span data-stu-id="7d37e-116">To open the TreeNode Editor, click the ellipsis button ( ![The Ellipsis button (...) in the Properties window of Visual Studio.](./media/visual-studio-ellipsis-button.png)) next to the <xref:System.Windows.Forms.TreeView.Nodes%2A> property on the Properties window.</span></span>  
  
    ```vb  
    ' (Assumes that ImageList1 contains at least two images and  
    ' the TreeView control contains a selected image.)  
    TreeView1.SelectedNode.ImageIndex = 0  
    TreeView1.SelectedNode.SelectedImageIndex = 1  
    ```  
  
    ```csharp  
    // (Assumes that imageList1 contains at least two images and  
    // the TreeView control contains a selected image.)  
    treeView1.SelectedNode.ImageIndex = 0;  
    treeView1.SelectedNode.SelectedImageIndex = 1;  
    ```  
  
    ```cpp  
    // (Assumes that imageList1 contains at least two images and  
    // the TreeView control contains a selected image.)  
    treeView1->SelectedNode->ImageIndex = 0;  
    treeView1->SelectedNode->SelectedImageIndex = 1;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="7d37e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d37e-117">See also</span></span>

- [<span data-ttu-id="7d37e-118">Übersicht über das TreeView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7d37e-118">TreeView Control Overview</span></span>](treeview-control-overview-windows-forms.md)
- [<span data-ttu-id="7d37e-119">Vorgehensweise: Hinzufügen oder Entfernen von Knoten mit dem TreeView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7d37e-119">How to: Add and Remove Nodes with the Windows Forms TreeView Control</span></span>](how-to-add-and-remove-nodes-with-the-windows-forms-treeview-control.md)
- [<span data-ttu-id="7d37e-120">Vorgehensweise: Durchlaufen aller Knoten eines TreeView-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7d37e-120">How to: Iterate Through All Nodes of a Windows Forms TreeView Control</span></span>](how-to-iterate-through-all-nodes-of-a-windows-forms-treeview-control.md)
- [<span data-ttu-id="7d37e-121">Vorgehensweise: Ermitteln des per Mausklick ausgewählten TreeView-Knotens</span><span class="sxs-lookup"><span data-stu-id="7d37e-121">How to: Determine Which TreeView Node Was Clicked</span></span>](how-to-determine-which-treeview-node-was-clicked-windows-forms.md)
- [<span data-ttu-id="7d37e-122">Vorgehensweise: Hinzufügen von benutzerdefinierten Daten zu einem TreeView- oder ListView-Steuerelement (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="7d37e-122">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](add-custom-information-to-a-treeview-or-listview-control-wf.md)
