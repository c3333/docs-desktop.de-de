---
title: Gruppieren von Elementen im ListView-Steuerelement mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- ListView control [Windows Forms], grouping items
- grouping
- groups [Windows Forms], in Windows Forms controls
ms.assetid: 8b615000-69d9-4c64-acaf-b54fa09b69e3
ms.openlocfilehash: 935d8d75517e1028e686ca229f6ada656f58b01e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976484"
---
# <a name="how-to-group-items-in-a-windows-forms-listview-control-using-the-designer"></a><span data-ttu-id="5c988-102">Vorgehensweise: Gruppieren von Elementen in einem ListView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="5c988-102">How to: Group Items in a Windows Forms ListView Control Using the Designer</span></span>

<span data-ttu-id="5c988-103">Mit der Gruppierungs Funktion des- <xref:System.Windows.Forms.ListView> Steuer Elements können Sie Verwandte Gruppen von Elementen in Gruppen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5c988-103">The grouping feature of the <xref:System.Windows.Forms.ListView> control enables you to display related sets of items in groups.</span></span> <span data-ttu-id="5c988-104">Diese Gruppen werden auf dem Bildschirm durch horizontale Gruppen Kopfzeilen getrennt, die die Gruppentitel enthalten.</span><span class="sxs-lookup"><span data-stu-id="5c988-104">These groups are separated on the screen by horizontal group headers that contain the group titles.</span></span> <span data-ttu-id="5c988-105">Mithilfe von Gruppen können Sie <xref:System.Windows.Forms.ListView> die Navigation durch große Listen vereinfachen, indem Sie Elemente alphabetisch, nach Datum oder nach einer anderen logischen Gruppierung gruppieren.</span><span class="sxs-lookup"><span data-stu-id="5c988-105">You can use <xref:System.Windows.Forms.ListView> groups to make navigating large lists easier by grouping items alphabetically, by date, or by any other logical grouping.</span></span> <span data-ttu-id="5c988-106">Die folgende Abbildung zeigt einige gruppierte Elemente:</span><span class="sxs-lookup"><span data-stu-id="5c988-106">The following image shows some grouped items:</span></span>

![Zahlen, die in ungerade und gerade Gruppen aufgeteilt sind.](./media/how-to-group-items-in-a-windows-forms-listview-control-using-the-designer/odd-even-list-view-groups.gif)

<span data-ttu-id="5c988-108">Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein-Steuerelement enthält <xref:System.Windows.Forms.ListView> .</span><span class="sxs-lookup"><span data-stu-id="5c988-108">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.ListView> control.</span></span> <span data-ttu-id="5c988-109">Weitere Informationen zum Einrichten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="5c988-109">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>

<span data-ttu-id="5c988-110">Um die Gruppierung zu aktivieren, müssen Sie zunächst ein oder mehrere <xref:System.Windows.Forms.ListViewGroup> Objekte entweder im Designer oder Programm gesteuert erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c988-110">To enable grouping, you must first create one or more <xref:System.Windows.Forms.ListViewGroup> objects either in the designer or programmatically.</span></span> <span data-ttu-id="5c988-111">Nachdem eine Gruppe definiert wurde, können Sie Ihr Elemente zuweisen.</span><span class="sxs-lookup"><span data-stu-id="5c988-111">Once a group has been defined, you can assign items to it.</span></span>

## <a name="to-add-or-remove-groups-in-the-designer"></a><span data-ttu-id="5c988-112">So können Sie Gruppen im Designer hinzufügen oder entfernen</span><span class="sxs-lookup"><span data-stu-id="5c988-112">To add or remove groups in the designer</span></span>

1. <span data-ttu-id="5c988-113">Klicken Sie im **Eigenschaften** Fenster auf die Auslassungs **Punkte (** die Schaltfläche mit den Auslassungs Punkten ![ (...) in der Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ) neben der- <xref:System.Windows.Forms.ListView.Groups%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5c988-113">In the **Properties** window, click the **Ellipsis** (![The Ellipsis button (...) in the Properties window of Visual Studio.](./media/visual-studio-ellipsis-button.png)) button next to the <xref:System.Windows.Forms.ListView.Groups%2A> property.</span></span>

     <span data-ttu-id="5c988-114">Der **ListViewGroup-Sammlungs-Editor** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c988-114">The **ListViewGroup Collection Editor** appears.</span></span>

2. <span data-ttu-id="5c988-115">Um eine Gruppe hinzuzufügen, klicken Sie auf die Schaltfläche **Hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="5c988-115">To add a group, click the **Add** button.</span></span> <span data-ttu-id="5c988-116">Sie können dann Eigenschaften der neuen Gruppe festlegen, z <xref:System.Windows.Forms.ListViewGroup.Header%2A> . b. die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.ListViewGroup.HeaderAlignment%2A> .</span><span class="sxs-lookup"><span data-stu-id="5c988-116">You can then set properties of the new group, such as the <xref:System.Windows.Forms.ListViewGroup.Header%2A> and <xref:System.Windows.Forms.ListViewGroup.HeaderAlignment%2A> properties.</span></span> <span data-ttu-id="5c988-117">Um eine Gruppe zu entfernen, wählen Sie Sie aus und klicken auf die Schaltfläche **Entfernen** .</span><span class="sxs-lookup"><span data-stu-id="5c988-117">To remove a group, select it and click the **Remove** button.</span></span>

## <a name="to-assign-items-to-groups-in-the-designer"></a><span data-ttu-id="5c988-118">So weisen Sie Gruppen im Designer Elemente zu</span><span class="sxs-lookup"><span data-stu-id="5c988-118">To assign items to groups in the designer</span></span>

1. <span data-ttu-id="5c988-119">Klicken Sie im **Eigenschaften** Fenster auf die Auslassungs **Punkte (** die Schaltfläche mit den Auslassungs Punkten ![ (...) in der Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ) neben der- <xref:System.Windows.Forms.ListView.Items%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5c988-119">In the **Properties** window, click the **Ellipsis** (![The Ellipsis button (...) in the Properties window of Visual Studio.](./media/visual-studio-ellipsis-button.png)) button next to the <xref:System.Windows.Forms.ListView.Items%2A> property.</span></span>

     <span data-ttu-id="5c988-120">Der **ListViewItem-Auflistungs-Editor** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c988-120">The **ListViewItem Collection Editor** appears.</span></span>

2. <span data-ttu-id="5c988-121">Um ein neues Element hinzuzufügen, klicken Sie auf die Schaltfläche **Hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="5c988-121">To add a new item, click the **Add** button.</span></span> <span data-ttu-id="5c988-122">Sie können dann die Eigenschaften des neuen Elements festlegen, z. b <xref:System.Windows.Forms.ListViewItem.Text%2A> . die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> .</span><span class="sxs-lookup"><span data-stu-id="5c988-122">You can then set properties of the new item, such as the <xref:System.Windows.Forms.ListViewItem.Text%2A> and <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> properties.</span></span>

3. <span data-ttu-id="5c988-123">Wählen Sie die <xref:System.Windows.Forms.ListViewItem.Group%2A> Eigenschaft aus, und wählen Sie eine Gruppe aus der Dropdown Liste aus.</span><span class="sxs-lookup"><span data-stu-id="5c988-123">Select the <xref:System.Windows.Forms.ListViewItem.Group%2A> property and choose a group from the drop-down list.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c988-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c988-124">See also</span></span>

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.Groups%2A>
- <xref:System.Windows.Forms.ListViewGroup>
- [<span data-ttu-id="5c988-125">ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5c988-125">ListView Control</span></span>](listview-control-windows-forms.md)
- [<span data-ttu-id="5c988-126">Übersicht über das ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5c988-126">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
- [<span data-ttu-id="5c988-127">Vorgehensweise: Hinzufügen und Entfernen von Elementen mit dem ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5c988-127">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
