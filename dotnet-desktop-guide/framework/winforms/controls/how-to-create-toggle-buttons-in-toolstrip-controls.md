---
title: 'Vorgehensweise: Erstellen von Umschaltflächen in ToolStrip-Steuerelementen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toggle buttons [Windows Forms], creating
- examples [Windows Forms], toolbars
- ToolStrip control [Windows Forms], creating toggle buttons
ms.assetid: d9c197df-4c65-43f2-beee-b68b52b2befc
ms.openlocfilehash: 6a003b91cd4db5db2790a20db97dbaa4d8925e96
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976328"
---
# <a name="how-to-create-toggle-buttons-in-toolstrip-controls"></a><span data-ttu-id="5da83-102">Vorgehensweise: Erstellen von Umschaltflächen in ToolStrip-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="5da83-102">How to: Create Toggle Buttons in ToolStrip Controls</span></span>

<span data-ttu-id="5da83-103">Wenn ein Benutzer auf eine UMSCHALT Fläche klickt, wird er abgeversenkt angezeigt und behält die abgesendeten Darstellung bei, bis der Benutzer erneut auf die Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="5da83-103">When a user clicks a toggle button, it appears sunken and retains the sunken appearance until the user clicks the button again.</span></span>

## <a name="to-create-a-toggling-toolstripbutton"></a><span data-ttu-id="5da83-104">So erstellen Sie ein UMSCHALT Fläche-Tool Strip Button</span><span class="sxs-lookup"><span data-stu-id="5da83-104">To create a toggling ToolStripButton</span></span>

- <span data-ttu-id="5da83-105">Verwenden Sie Code wie im folgenden Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="5da83-105">Use code such as the following code example.</span></span> <span data-ttu-id="5da83-106">In diesem Code wird davon ausgegangen, dass das Formular ein <xref:System.Windows.Forms.ToolStrip> -Steuerelement enthält und dass die zugehörige Auflistung <xref:System.Windows.Forms.ToolStrip.Items%2A> einen <xref:System.Windows.Forms.ToolStripButton> aufgerufenen enthält `toolStripButton1`</span><span class="sxs-lookup"><span data-stu-id="5da83-106">This code assumes that your form contains a <xref:System.Windows.Forms.ToolStrip> control, and that its <xref:System.Windows.Forms.ToolStrip.Items%2A> collection contains a <xref:System.Windows.Forms.ToolStripButton> called `toolStripButton1`.</span></span> <span data-ttu-id="5da83-107">Außerdem wird davon ausgegangen, dass Sie über einen Ereignishandler namens verfügen `toolStripButton1_CheckedChanged` .</span><span class="sxs-lookup"><span data-stu-id="5da83-107">It also assumes that you have an event handler called `toolStripButton1_CheckedChanged`.</span></span>

    ```vb
    toolStripButton1.CheckOnClick = True
    toolStripButton1.CheckedChanged AddressOf _
    EventHandler(toolStripButton1_CheckedChanged);
    ```

    ```csharp
    toolStripButton1.CheckOnClick = true;
    toolStripButton1.CheckedChanged += new _
    EventHandler(toolStripButton1_CheckedChanged);
    ```

## <a name="see-also"></a><span data-ttu-id="5da83-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5da83-108">See also</span></span>

- <xref:System.Windows.Forms.ToolStripButton>
- [<span data-ttu-id="5da83-109">Übersicht über das ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5da83-109">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
