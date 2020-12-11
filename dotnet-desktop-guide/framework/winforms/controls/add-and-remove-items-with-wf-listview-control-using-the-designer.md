---
title: Hinzufügen und Entfernen von Elementen mit dem ListView-Steuerelement mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- ListView control [Windows Forms], populating
- ListView control [Windows Forms], adding list items
ms.assetid: 217611ee-fd11-4d39-9a54-a37c3e781be1
ms.openlocfilehash: cab40c556d9e5d21ce15bcd3d4da367bc08f33ab
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975160"
---
# <a name="how-to-add-and-remove-items-with-the-windows-forms-listview-control-using-the-designer"></a><span data-ttu-id="c362a-102">Vorgehensweise: Hinzufügen und Entfernen von Elementen mit dem ListView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="c362a-102">How to: Add and Remove Items with the Windows Forms ListView Control Using the Designer</span></span>

<span data-ttu-id="c362a-103">Das Hinzufügen eines Elements zu einem Windows Forms <xref:System.Windows.Forms.ListView> Steuerelement besteht hauptsächlich darin, das Element anzugeben und ihm Eigenschaften zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="c362a-103">The process of adding an item to a Windows Forms <xref:System.Windows.Forms.ListView> control consists primarily of specifying the item and assigning properties to it.</span></span> <span data-ttu-id="c362a-104">Das Hinzufügen oder Entfernen von Listenelementen ist jederzeit möglich.</span><span class="sxs-lookup"><span data-stu-id="c362a-104">Adding or removing list items can be done at any time.</span></span>

<span data-ttu-id="c362a-105">Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein-Steuerelement enthält <xref:System.Windows.Forms.ListView> .</span><span class="sxs-lookup"><span data-stu-id="c362a-105">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.ListView> control.</span></span> <span data-ttu-id="c362a-106">Weitere Informationen zum Einrichten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="c362a-106">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>

### <a name="to-add-or-remove-items-using-the-designer"></a><span data-ttu-id="c362a-107">So können Sie Elemente mithilfe des Designers hinzufügen oder entfernen</span><span class="sxs-lookup"><span data-stu-id="c362a-107">To add or remove items using the designer</span></span>

1. <span data-ttu-id="c362a-108">Wählen Sie das <xref:System.Windows.Forms.ListView>-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c362a-108">Select the <xref:System.Windows.Forms.ListView> control.</span></span>

2. <span data-ttu-id="c362a-109">Klicken Sie im **Eigenschaften** Fenster auf die Auslassungs **Punkte (** die Schaltfläche mit den Auslassungs Punkten ![ (...) in der Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ) neben der- <xref:System.Windows.Forms.ListView.Items%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c362a-109">In the **Properties** window, click the **Ellipsis** (![The Ellipsis button (...) in the Properties window of Visual Studio.](./media/visual-studio-ellipsis-button.png)) button next to the <xref:System.Windows.Forms.ListView.Items%2A> property.</span></span>

     <span data-ttu-id="c362a-110">Der **ListViewItem-Auflistungs-Editor** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c362a-110">The **ListViewItem Collection Editor** appears.</span></span>

3. <span data-ttu-id="c362a-111">Um ein Element hinzuzufügen, klicken Sie auf die Schaltfläche **Hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="c362a-111">To add an item, click the **Add** button.</span></span> <span data-ttu-id="c362a-112">Sie können dann die Eigenschaften des neuen Elements festlegen, z. b <xref:System.Windows.Forms.ListView.Text%2A> . die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> .</span><span class="sxs-lookup"><span data-stu-id="c362a-112">You can then set properties of the new item, such as the <xref:System.Windows.Forms.ListView.Text%2A> and <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> properties.</span></span>

4. <span data-ttu-id="c362a-113">Um ein Element zu entfernen, wählen Sie es aus und klicken auf die Schaltfläche **Entfernen** .</span><span class="sxs-lookup"><span data-stu-id="c362a-113">To remove an item, select it and click the **Remove** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="c362a-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c362a-114">See also</span></span>

- [<span data-ttu-id="c362a-115">Übersicht über das ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c362a-115">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
- [<span data-ttu-id="c362a-116">Vorgehensweise: Hinzufügen von Spalten zum ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c362a-116">How to: Add Columns to the Windows Forms ListView Control</span></span>](how-to-add-columns-to-the-windows-forms-listview-control.md)
- [<span data-ttu-id="c362a-117">Vorgehensweise: Anzeigen von Unterelementen in Spalten mit dem ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c362a-117">How to: Display Subitems in Columns with the Windows Forms ListView Control</span></span>](how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md)
- [<span data-ttu-id="c362a-118">Vorgehensweise: Anzeigen von Symbolen für das ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c362a-118">How to: Display Icons for the Windows Forms ListView Control</span></span>](how-to-display-icons-for-the-windows-forms-listview-control.md)
- [<span data-ttu-id="c362a-119">Vorgehensweise: Hinzufügen von benutzerdefinierten Daten zu einem TreeView- oder ListView-Steuerelement (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="c362a-119">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](add-custom-information-to-a-treeview-or-listview-control-wf.md)
- [<span data-ttu-id="c362a-120">Vorgehensweise: Gruppieren von Elementen in einem ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c362a-120">How to: Group Items in a Windows Forms ListView Control</span></span>](how-to-group-items-in-a-windows-forms-listview-control.md)
