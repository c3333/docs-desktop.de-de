---
title: 'Vorgehensweise: Anfügen eines Kontextmenüs an einen Strukturansichtsknoten'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- shortcut menus [Windows Forms], adding to TreeView controls
- TreeView control [Windows Forms], adding shortcut menus
- tree nodes in TreeView control [Windows Forms], shortcut menus
ms.assetid: a23c6752-fd8f-44ad-b781-bab37962fc7c
ms.openlocfilehash: f818cccb3103866af993f1aff527a9c1a7c82109
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975720"
---
# <a name="how-to-attach-a-shortcut-menu-to-a-treeview-node"></a><span data-ttu-id="940a7-102">Vorgehensweise: Anfügen eines Kontextmenüs an einen Strukturansichtsknoten</span><span class="sxs-lookup"><span data-stu-id="940a7-102">How to: Attach a ShortCut Menu to a TreeView Node</span></span>
<span data-ttu-id="940a7-103">Das Windows Forms <xref:System.Windows.Forms.TreeView> Steuerelement zeigt eine Hierarchie von Knoten an, ähnlich den Dateien und Ordnern, die im linken Fensterbereich von Windows-Explorer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="940a7-103">The Windows Forms <xref:System.Windows.Forms.TreeView> control displays a hierarchy of nodes, similar to the files and folders displayed in the left pane of Windows Explorer.</span></span> <span data-ttu-id="940a7-104">Durch Festlegen der <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> -Eigenschaft können Sie dem Benutzer kontextabhängige Vorgänge bereitstellen, wenn Sie mit der rechten Maustaste auf das Steuerelement klicken <xref:System.Windows.Forms.TreeView> .</span><span class="sxs-lookup"><span data-stu-id="940a7-104">By setting the <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> property, you can provide context-sensitive operations to the user when they right-click the <xref:System.Windows.Forms.TreeView> control.</span></span> <span data-ttu-id="940a7-105">Durch Zuordnen einer <xref:System.Windows.Forms.ContextMenuStrip> Komponente <xref:System.Windows.Forms.TreeNode> zu einzelnen Elementen können Sie den Steuerelementen eine angepasste Ebene von Kontextmenü Funktionen hinzufügen <xref:System.Windows.Forms.TreeView> .</span><span class="sxs-lookup"><span data-stu-id="940a7-105">By associating a <xref:System.Windows.Forms.ContextMenuStrip> component with individual <xref:System.Windows.Forms.TreeNode> items, you can add a customized level of shortcut menu functionality to your <xref:System.Windows.Forms.TreeView> controls.</span></span>  
  
### <a name="to-associate-a-shortcut-menu-with-a-treenode-programmatically"></a><span data-ttu-id="940a7-106">So ordnen Sie ein Kontextmenü Programm gesteuert einem TreeNode zu</span><span class="sxs-lookup"><span data-stu-id="940a7-106">To associate a shortcut menu with a TreeNode programmatically</span></span>  
  
1. <span data-ttu-id="940a7-107">Instanziieren <xref:System.Windows.Forms.TreeView> Sie ein-Steuerelement mit den entsprechenden Eigenschaften Einstellungen, erstellen Sie ein Stamm <xref:System.Windows.Forms.TreeNode> Verzeichnis, und fügen Sie dann untergeordnete Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="940a7-107">Instantiate a <xref:System.Windows.Forms.TreeView> control with the appropriate property settings, create a root <xref:System.Windows.Forms.TreeNode>, and then add subnodes.</span></span>  
  
2. <span data-ttu-id="940a7-108">Instanziieren <xref:System.Windows.Forms.ContextMenuStrip> Sie eine-Komponente, und fügen <xref:System.Windows.Forms.ToolStripMenuItem> Sie dann für jeden Vorgang, den Sie zur Laufzeit zur Verfügung stellen möchten, ein hinzu.</span><span class="sxs-lookup"><span data-stu-id="940a7-108">Instantiate a <xref:System.Windows.Forms.ContextMenuStrip> component, and then add a <xref:System.Windows.Forms.ToolStripMenuItem> for each operation you want to make available at run time.</span></span>  
  
3. <span data-ttu-id="940a7-109">Legen Sie die- <xref:System.Windows.Forms.TreeNode.ContextMenuStrip%2A> Eigenschaft der entsprechenden <xref:System.Windows.Forms.TreeNode> auf das Kontextmenü fest, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="940a7-109">Set the <xref:System.Windows.Forms.TreeNode.ContextMenuStrip%2A> property of the appropriate <xref:System.Windows.Forms.TreeNode> to the shortcut menu you create.</span></span>  
  
4. <span data-ttu-id="940a7-110">Wenn diese Eigenschaft festgelegt ist, wird das Kontextmenü angezeigt, wenn Sie mit der rechten Maustaste auf den Knoten klicken.</span><span class="sxs-lookup"><span data-stu-id="940a7-110">When this property is set, the shortcut menu will be displayed when you right-click the node.</span></span>  
  
 <span data-ttu-id="940a7-111">Im folgenden Codebeispiel wird ein einfaches-Element erstellt, das <xref:System.Windows.Forms.TreeView> <xref:System.Windows.Forms.ContextMenuStrip> dem Stamm des zugeordnet ist <xref:System.Windows.Forms.TreeNode> <xref:System.Windows.Forms.TreeView> .</span><span class="sxs-lookup"><span data-stu-id="940a7-111">The following code example creates a basic <xref:System.Windows.Forms.TreeView> and <xref:System.Windows.Forms.ContextMenuStrip> associated with the root <xref:System.Windows.Forms.TreeNode> of the <xref:System.Windows.Forms.TreeView>.</span></span> <span data-ttu-id="940a7-112">Sie müssen die Menü Optionen an die von <xref:System.Windows.Forms.TreeView> Ihnen entwickelten Optionen anpassen.</span><span class="sxs-lookup"><span data-stu-id="940a7-112">You will need to customize the menu choices to those that fit the <xref:System.Windows.Forms.TreeView> you are developing.</span></span> <span data-ttu-id="940a7-113">Außerdem sollten Sie Code schreiben, um die <xref:System.Windows.Forms.ToolStripItem.Click> Ereignisse für diese Menü Elemente zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="940a7-113">Additionally, you will want to write code to handle the <xref:System.Windows.Forms.ToolStripItem.Click> events for these menu items.</span></span>  
  
 [!code-cpp[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/cpp/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/cpp/Form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/csharp/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/VB/Form1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="940a7-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="940a7-114">See also</span></span>

- <xref:System.Windows.Forms.ContextMenuStrip>
- [<span data-ttu-id="940a7-115">TreeView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="940a7-115">TreeView Control</span></span>](treeview-control-windows-forms.md)
