---
title: 'Vorgehensweise: Ausblenden von ToolStripMenuItems mithilfe des Designers'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], hiding menu items in designer
- MenuStrip control [Windows Forms], hiding menu items in designer
- menu items [Windows Forms], hiding
ms.assetid: 8f1b057e-3d8a-4f11-88df-935f7b29a836
ms.openlocfilehash: 0e1cd7d1868adabd4d3eec9510f6ee567ba3867d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975633"
---
# <a name="how-to-hide-toolstripmenuitems-using-the-designer"></a><span data-ttu-id="804a9-102">Vorgehensweise: Ausblenden von ToolStripMenuItems mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="804a9-102">How to: Hide ToolStripMenuItems Using the Designer</span></span>
<span data-ttu-id="804a9-103">Das Ausblenden von Menü Elementen ist eine Möglichkeit, die Benutzeroberfläche (UI) Ihrer Anwendung zu steuern und Benutzer Befehle einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="804a9-103">Hiding menu items is a way to control the user interface (UI) of your application and restrict user commands.</span></span> <span data-ttu-id="804a9-104">Häufig ist es ratsam, ein gesamtes Menü auszublenden, wenn alle Menü Elemente darin nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="804a9-104">Often, you will want to hide an entire menu when all of the menu items on it are unavailable.</span></span> <span data-ttu-id="804a9-105">Dies stellt weniger Ablenkungen für den Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="804a9-105">This presents fewer distractions for the user.</span></span> <span data-ttu-id="804a9-106">Außerdem empfiehlt es sich, das Menü oder das Menü Element auszublenden und zu deaktivieren, da durch das Ausblenden allein nicht verhindert wird, dass der Benutzer über eine Tastenkombination auf einen Menübefehl zugreift.</span><span class="sxs-lookup"><span data-stu-id="804a9-106">Furthermore, you might want to both hide and disable the menu or menu item, as hiding alone does not prevent the user from accessing a menu command by using a shortcut key.</span></span> <span data-ttu-id="804a9-107">Weitere Informationen zum Deaktivieren von Menü Elementen finden Sie unter Gewusst [wie: Deaktivieren von ToolStripMenuItems mithilfe des Designers](how-to-disable-toolstripmenuitems-using-the-designer.md).</span><span class="sxs-lookup"><span data-stu-id="804a9-107">For more information on disabling menu items, see [How to: Disable ToolStripMenuItems Using the Designer](how-to-disable-toolstripmenuitems-using-the-designer.md).</span></span>

## <a name="to-hide-a-top-level-menu-and-its-submenu-items"></a><span data-ttu-id="804a9-108">So blenden Sie ein Menü der obersten Ebene und seine unter Menü Elemente aus</span><span class="sxs-lookup"><span data-stu-id="804a9-108">To hide a top-level menu and its submenu items</span></span>

1. <span data-ttu-id="804a9-109">Wählen Sie das Menü Element der obersten Ebene aus, und legen Sie die- <xref:System.Windows.Forms.ToolStripItem.Visible%2A> oder- <xref:System.Windows.Forms.ToolStripItem.Available%2A> Eigenschaft auf fest `false`</span><span class="sxs-lookup"><span data-stu-id="804a9-109">Select the top-level menu item and set its <xref:System.Windows.Forms.ToolStripItem.Visible%2A> or <xref:System.Windows.Forms.ToolStripItem.Available%2A> property to `false`.</span></span>

     <span data-ttu-id="804a9-110">Wenn Sie das Menü Element der obersten Ebene ausblenden, werden alle Menü Elemente in diesem Menü ebenfalls ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="804a9-110">When you hide the top-level menu item, all menu items within that menu are also hidden.</span></span> <span data-ttu-id="804a9-111">Wenn Sie auf eine andere Stelle als auf der nach-Einstellung auf klicken <xref:System.Windows.Forms.MenuStrip> <xref:System.Windows.Forms.ToolStripItem.Visible%2A> `false` , werden das gesamte Menü Element der obersten Ebene und seine unter Menü Elemente aus dem Formular entfernt, sodass Sie die Lauf Zeit Wirkung ihrer Aktion angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="804a9-111">If you click somewhere other than on the <xref:System.Windows.Forms.MenuStrip> after setting <xref:System.Windows.Forms.ToolStripItem.Visible%2A> to `false`, the entire top-level menu item and its submenu items disappear from your form, thus showing you the run-time effect of your action.</span></span> <span data-ttu-id="804a9-112">Um das ausgeblendete Menü Element der obersten Ebene zur Entwurfszeit anzuzeigen, klicken Sie <xref:System.Windows.Forms.MenuStrip> in der **Komponenten Leiste**, in der **Dokument** Gliederung oder am oberen Rand des Eigenschaften Rasters auf das.</span><span class="sxs-lookup"><span data-stu-id="804a9-112">To display the hidden top-level menu item at design time, click on the <xref:System.Windows.Forms.MenuStrip> in the **Component Tray**, in **Document Outline**, or at the top of the property grid.</span></span>

> [!NOTE]
> <span data-ttu-id="804a9-113">Sie werden in einem Zusammenführungs Szenario selten ein gesamtes Menü mit Ausnahme von untergeordneten MDI-Menüs (Multiple Document Interface) ausblenden.</span><span class="sxs-lookup"><span data-stu-id="804a9-113">You will rarely hide an entire menu except for multiple document interface (MDI) child menus in a merging scenario.</span></span>

## <a name="to-hide-a-submenu-item"></a><span data-ttu-id="804a9-114">So blenden Sie ein unter Menü Element aus</span><span class="sxs-lookup"><span data-stu-id="804a9-114">To hide a submenu item</span></span>

1. <span data-ttu-id="804a9-115">Wählen Sie das unter Menü Element, und legen Sie dessen- <xref:System.Windows.Forms.ToolStripItem.Visible%2A> Eigenschaft auf fest `false` .</span><span class="sxs-lookup"><span data-stu-id="804a9-115">Select the submenu item and set its <xref:System.Windows.Forms.ToolStripItem.Visible%2A> property to `false`.</span></span>

     <span data-ttu-id="804a9-116">Wenn Sie ein unter Menü Element ausblenden, bleibt es zur Entwurfszeit auf dem Formular sichtbar, sodass Sie es für weitere Aufgaben problemlos auswählen können.</span><span class="sxs-lookup"><span data-stu-id="804a9-116">When you hide a submenu item, it remains visible on your form at design time so that you can easily select it for further work.</span></span> <span data-ttu-id="804a9-117">Sie wird zur Laufzeit ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="804a9-117">It will actually be hidden at run time.</span></span>

## <a name="see-also"></a><span data-ttu-id="804a9-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="804a9-118">See also</span></span>

- <xref:System.Windows.Forms.ToolStripItem.Visible%2A>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A>
- <xref:System.Windows.Forms.ToolStripItem.Available%2A>
- <xref:System.Windows.Forms.ToolStripMenuItem.Overflow%2A>
- [<span data-ttu-id="804a9-119">Übersicht über das MenuStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="804a9-119">MenuStrip Control Overview</span></span>](menustrip-control-overview-windows-forms.md)
- [<span data-ttu-id="804a9-120">Vorgehensweise: Deaktivieren von ToolStripMenuItems mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="804a9-120">How to: Disable ToolStripMenuItems Using the Designer</span></span>](how-to-disable-toolstripmenuitems-using-the-designer.md)
