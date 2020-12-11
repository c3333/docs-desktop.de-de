---
title: 'Vorgehensweise: Aktivieren der TAB-TASTE zum Verlassen eines ToolStrip-Steuerelements'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], moving between
- TAB key [Windows Forms], enabling
- ToolStrip control [Windows Forms], moving from
ms.assetid: 40f9e88b-09a3-428e-8da8-c00bb65079c6
ms.openlocfilehash: 7fee9f685b9a9b402cbfe9c265669f7905434986
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975641"
---
# <a name="how-to-enable-the-tab-key-to-move-out-of-a-toolstrip-control"></a><span data-ttu-id="92e33-102">Vorgehensweise: Aktivieren der TAB-TASTE zum Verlassen eines ToolStrip-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="92e33-102">How to: Enable the TAB Key to Move Out of a ToolStrip Control</span></span>
<span data-ttu-id="92e33-103">Verwenden Sie das folgende Verfahren, um dem Benutzer das Drücken der Tab-Taste zu ermöglichen, um von einem <xref:System.Windows.Forms.ToolStrip> zum nächsten Steuerelement in der Aktivier Reihenfolge zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="92e33-103">Use the following procedure to enable the user to press the TAB key to move out of a <xref:System.Windows.Forms.ToolStrip> to the next control in the tab order.</span></span>  
  
 <span data-ttu-id="92e33-104">Der <xref:System.Windows.Forms.ToolStrip> akzeptiert das erste Drücken der Tab-Taste, und die Pfeiltasten wählen Elemente in aus <xref:System.Windows.Forms.ToolStrip> .</span><span class="sxs-lookup"><span data-stu-id="92e33-104">The <xref:System.Windows.Forms.ToolStrip> accepts the first press of the TAB key, and the arrow keys select items within the <xref:System.Windows.Forms.ToolStrip>.</span></span> <span data-ttu-id="92e33-105">Wenn der Benutzer die Tab-Taste ein zweites Mal drückt, wird der Benutzer zum nächsten Steuerelement in der Aktivier Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="92e33-105">When the user presses the TAB key a second time, it takes the user to the next control in the tab order.</span></span>  
  
### <a name="to-enable-the-user-to-press-the-tab-key-to-move-out-of-a-toolstrip-to-the-next-control"></a><span data-ttu-id="92e33-106">So aktivieren Sie den Benutzer zum durch Drücken der Tab-Taste, um von einem ToolStrip zum nächsten Steuerelement zu wechseln</span><span class="sxs-lookup"><span data-stu-id="92e33-106">To enable the user to press the TAB key to move out of a ToolStrip to the next control</span></span>  
  
- <span data-ttu-id="92e33-107">Legen Sie die <xref:System.Windows.Forms.ToolStrip.TabStop%2A>-Eigenschaft von <xref:System.Windows.Forms.ToolStrip> auf `true` fest.</span><span class="sxs-lookup"><span data-stu-id="92e33-107">Set the <xref:System.Windows.Forms.ToolStrip.TabStop%2A> property of the <xref:System.Windows.Forms.ToolStrip> to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="92e33-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92e33-108">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.TabStop%2A>
- [<span data-ttu-id="92e33-109">Übersicht über das ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="92e33-109">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
