---
title: 'Vorgehensweise: Einrichten des automatischem Zusammenführens von Menüs für MDI-Anwendungen (Multiple Document Interface)'
ms.date: 03/30/2017
helpviewer_keywords:
- MenuStrip [Windows Forms], merging
- Merging [Windows Forms], automatic menu
ms.assetid: 55e32cad-1141-4a56-aa33-d9543ca3d393
ms.openlocfilehash: 33e07bb655d81c6a802ebdce871a2fed845a5c96
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976644"
---
# <a name="how-to-set-up-automatic-menu-merging-for-mdi-applications"></a><span data-ttu-id="926b2-102">Vorgehensweise: Einrichten des automatischem Zusammenführens von Menüs für MDI-Anwendungen (Multiple Document Interface)</span><span class="sxs-lookup"><span data-stu-id="926b2-102">How to: Set Up Automatic Menu Merging for MDI Applications</span></span>
<span data-ttu-id="926b2-103">Das folgende Verfahren enthält die grundlegenden Schritte zum Einrichten der automatischen Zusammenführung in einer MDI-Anwendung (Multiple Document Interface) mit <xref:System.Windows.Forms.MenuStrip> .</span><span class="sxs-lookup"><span data-stu-id="926b2-103">The following procedure gives the basic steps for setting up automatic merging in a multiple-document interface (MDI) application with <xref:System.Windows.Forms.MenuStrip>.</span></span>  
  
### <a name="to-set-up-automatic-menu-merging"></a><span data-ttu-id="926b2-104">So richten Sie die automatische Zusammenführung des Menüs ein</span><span class="sxs-lookup"><span data-stu-id="926b2-104">To set up automatic menu merging</span></span>  
  
1. <span data-ttu-id="926b2-105">Erstellen Sie das übergeordnete MDI-Formular <xref:System.Windows.Forms.Form.IsMdiContainer%2A> , indem Sie dessen-Eigenschaft auf festlegen `true` .</span><span class="sxs-lookup"><span data-stu-id="926b2-105">Create the MDI parent form by setting its <xref:System.Windows.Forms.Form.IsMdiContainer%2A> property to `true`.</span></span>  
  
2. <span data-ttu-id="926b2-106">Fügen Sie <xref:System.Windows.Forms.MenuStrip> das übergeordnete MDI-Element hinzu, und legen Sie dessen- <xref:System.Windows.Forms.Form.MainMenuStrip%2A> Eigenschaft auf fest <xref:System.Windows.Forms.MenuStrip> .</span><span class="sxs-lookup"><span data-stu-id="926b2-106">Add a <xref:System.Windows.Forms.MenuStrip> to the MDI parent, setting its <xref:System.Windows.Forms.Form.MainMenuStrip%2A> property to that <xref:System.Windows.Forms.MenuStrip>.</span></span>  
  
3. <span data-ttu-id="926b2-107">Erstellen Sie ein untergeordnetes MDI-Formular, und legen Sie dessen- <xref:System.Windows.Forms.Form.MdiParent%2A> Eigenschaft auf den Namen des übergeordneten Formulars fest.</span><span class="sxs-lookup"><span data-stu-id="926b2-107">Create an MDI child form, and set its <xref:System.Windows.Forms.Form.MdiParent%2A> property to the name of the parent form.</span></span>  
  
4. <span data-ttu-id="926b2-108">Fügen Sie <xref:System.Windows.Forms.MenuStrip> dem untergeordneten MDI-Formular ein hinzu.</span><span class="sxs-lookup"><span data-stu-id="926b2-108">Add a <xref:System.Windows.Forms.MenuStrip> to the MDI child form.</span></span>  
  
5. <span data-ttu-id="926b2-109">Legen Sie im untergeordneten Formular die- <xref:System.Windows.Forms.ToolStripItem.Visible%2A> Eigenschaft von <xref:System.Windows.Forms.MenuStrip> auf fest `false` .</span><span class="sxs-lookup"><span data-stu-id="926b2-109">On the child form, set the <xref:System.Windows.Forms.ToolStripItem.Visible%2A> property of the <xref:System.Windows.Forms.MenuStrip> to `false`.</span></span>  
  
6. <span data-ttu-id="926b2-110">Fügen Sie dem untergeordneten Formular Menü Elemente hinzu, die Sie im übergeordneten Formular zusammen <xref:System.Windows.Forms.MenuStrip> führen möchten, <xref:System.Windows.Forms.MenuStrip> Wenn das untergeordnete Formular aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="926b2-110">Add menu items to the child form's <xref:System.Windows.Forms.MenuStrip> that you want to merge into the parent form's <xref:System.Windows.Forms.MenuStrip> when the child form is activated.</span></span>  
  
7. <span data-ttu-id="926b2-111">Verwenden <xref:System.Windows.Forms.ToolStripItem.MergeAction%2A> Sie die-Eigenschaft in den Menü Elementen im unter <xref:System.Windows.Forms.MenuStrip> geordneten Formular, um zu steuern, wie Sie im übergeordneten Formular zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="926b2-111">Use the <xref:System.Windows.Forms.ToolStripItem.MergeAction%2A> property on the menu items in the child form's <xref:System.Windows.Forms.MenuStrip> to control how they merge into the parent form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="926b2-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="926b2-112">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [<span data-ttu-id="926b2-113">Übersicht über das MenuStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="926b2-113">MenuStrip Control Overview</span></span>](menustrip-control-overview-windows-forms.md)
