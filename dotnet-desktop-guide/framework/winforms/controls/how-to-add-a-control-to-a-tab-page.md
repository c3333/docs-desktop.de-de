---
title: 'Vorgehensweise: Hinzufügen eines Steuerelements zu einer Registerkarte'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TabPage control
- tab controls [Windows Forms], tab order
- tab pages [Windows Forms], adding controls
ms.assetid: b092532e-7346-469f-b9a1-897f9bea4fb7
ms.openlocfilehash: 9806583fda60f1cb8a5ef2d97f42eba158593f61
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975751"
---
# <a name="how-to-add-a-control-to-a-tab-page"></a><span data-ttu-id="b708e-102">Vorgehensweise: Hinzufügen eines Steuerelements zu einer Registerkarte</span><span class="sxs-lookup"><span data-stu-id="b708e-102">How to: Add a Control to a Tab Page</span></span>
<span data-ttu-id="b708e-103">Sie können den Windows Forms verwenden <xref:System.Windows.Forms.TabControl> , um andere Steuerelemente auf organisierte Weise anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b708e-103">You can use the Windows Forms <xref:System.Windows.Forms.TabControl> to display other controls in an organized fashion.</span></span> <span data-ttu-id="b708e-104">Im folgenden Verfahren wird gezeigt, wie Sie der ersten Registerkarte eine Schaltfläche hinzufügen. Weitere Informationen zum Hinzufügen eines Symbols zum Bezeichnungs Teil einer Registerkarte finden Sie unter Gewusst [wie: Ändern der Darstellung des Windows Forms TabControl](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="b708e-104">The following procedure shows how to add a button to the first tab. For information about adding an icon to the label part of a tab page, see [How to: Change the Appearance of the Windows Forms TabControl](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md).</span></span>  
  
### <a name="to-add-a-control-programmatically"></a><span data-ttu-id="b708e-105">So fügen Sie ein-Steuerelement Programm gesteuert hinzu</span><span class="sxs-lookup"><span data-stu-id="b708e-105">To add a control programmatically</span></span>  
  
1. <span data-ttu-id="b708e-106">Verwenden Sie die-Methode der Auflistung, die <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> von der-Eigenschaft von zurückgegeben wird <xref:System.Windows.Forms.Control.Controls%2A> <xref:System.Windows.Forms.TabPage> :</span><span class="sxs-lookup"><span data-stu-id="b708e-106">Use the <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> method of the collection returned by the <xref:System.Windows.Forms.Control.Controls%2A> property of <xref:System.Windows.Forms.TabPage>:</span></span>  
  
     [!code-cpp[TabPageControlCollectionHowToAdd#1](~/samples/snippets/cpp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cpp/add.cpp#1)]
     [!code-csharp[TabPageControlCollectionHowToAdd#1](~/samples/snippets/csharp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cs/add.cs#1)]
     [!code-vb[TabPageControlCollectionHowToAdd#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/vb/add.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="b708e-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b708e-107">See also</span></span>

- [<span data-ttu-id="b708e-108">TabControl-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b708e-108">TabControl Control</span></span>](tabcontrol-control-windows-forms.md)
- [<span data-ttu-id="b708e-109">Übersicht über das TabControl-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b708e-109">TabControl Control Overview</span></span>](tabcontrol-control-overview-windows-forms.md)
- [<span data-ttu-id="b708e-110">Vorgehensweise: Ändern der Darstellung der TabControl-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b708e-110">How to: Change the Appearance of the Windows Forms TabControl</span></span>](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
- [<span data-ttu-id="b708e-111">Vorgehensweise: Deaktivieren von Registerkartenseiten</span><span class="sxs-lookup"><span data-stu-id="b708e-111">How to: Disable Tab Pages</span></span>](how-to-disable-tab-pages.md)
- [<span data-ttu-id="b708e-112">Vorgehensweise: Hinzufügen und Entfernen von Registerkarten mit dem TabControl-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b708e-112">How to: Add and Remove Tabs with the Windows Forms TabControl</span></span>](how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
