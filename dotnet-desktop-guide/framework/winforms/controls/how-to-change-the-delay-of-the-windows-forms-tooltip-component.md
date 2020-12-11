---
title: Ändern der Verzögerung der ToolTip-Komponente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ToolTip component [Windows Forms], delay values
- tooltips [Windows Forms], delay values
- examples [Windows Forms], tooltips
ms.assetid: 08979ba7-dd84-477b-ab17-8d06e759be99
ms.openlocfilehash: 8ab0b0760e8c82d752eaada19f14cae57fa63fdc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976351"
---
# <a name="how-to-change-the-delay-of-the-windows-forms-tooltip-component"></a><span data-ttu-id="55cb0-102">Vorgehensweise: Ändern der Verzögerung der ToolTip-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="55cb0-102">How to: Change the Delay of the Windows Forms ToolTip Component</span></span>
<span data-ttu-id="55cb0-103">Es gibt mehrere Delay-Werte, die Sie für eine Windows Forms <xref:System.Windows.Forms.ToolTip> Komponente festlegen können.</span><span class="sxs-lookup"><span data-stu-id="55cb0-103">There are multiple delay values that you can set for a Windows Forms <xref:System.Windows.Forms.ToolTip> component.</span></span> <span data-ttu-id="55cb0-104">Die Maßeinheit für alle diese Eigenschaften beträgt Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="55cb0-104">The unit of measure for all these properties is milliseconds.</span></span> <span data-ttu-id="55cb0-105">Die- <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> Eigenschaft bestimmt, wie lange der Benutzer auf das zugeordnete Steuerelement zeigen muss, damit die QuickInfo-Zeichenfolge angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="55cb0-105">The <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> property determines how long the user must point at the associated control for the ToolTip string to appear.</span></span> <span data-ttu-id="55cb0-106">Mit der- <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> Eigenschaft wird die Anzahl der Millisekunden festgelegt, die für die Anzeige von nachfolgenden QuickInfo-Zeichen folgen benötigt wird, wenn die Maus von einem ToolTip-zugeordneten Steuerelement</span><span class="sxs-lookup"><span data-stu-id="55cb0-106">The <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> property sets the number of milliseconds it takes for subsequent ToolTip strings to appear as the mouse moves from one ToolTip-associated control to another.</span></span> <span data-ttu-id="55cb0-107">Die- <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> Eigenschaft bestimmt, wie lange die QuickInfo-Zeichenfolge angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="55cb0-107">The <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> property determines the length of time the ToolTip string is shown.</span></span> <span data-ttu-id="55cb0-108">Sie können diese Werte einzeln festlegen oder indem Sie den Wert der- <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> Eigenschaft festlegen. die anderen Verzögerungs Eigenschaften werden basierend auf dem Wert festgelegt, der der-Eigenschaft zugewiesen ist <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> .</span><span class="sxs-lookup"><span data-stu-id="55cb0-108">You can set these values individually, or by setting the value of the <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> property; the other delay properties are set based on the value assigned to the <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> property.</span></span> <span data-ttu-id="55cb0-109">Wenn z. b. <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> auf einen Wert n festgelegt ist, wird auf n festgelegt <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> , <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> wird auf den Wert <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> dividiert durch 5 (oder N/5) festgelegt, und <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> wird auf einen Wert festgelegt, der fünfmal den Wert der- <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> Eigenschaft (oder 5N) ist.</span><span class="sxs-lookup"><span data-stu-id="55cb0-109">For example, when <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> is set to a value N, <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> is set to N, <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> is set to the value of <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> divided by five (or N/5), and <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> is set to a value that is five times the value of the <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> property (or 5N).</span></span>  
  
### <a name="to-set-the-delay"></a><span data-ttu-id="55cb0-110">So legen Sie die Verzögerung fest</span><span class="sxs-lookup"><span data-stu-id="55cb0-110">To set the delay</span></span>  
  
1. <span data-ttu-id="55cb0-111">Legen Sie die folgenden Eigenschaften fest, wie in diesem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="55cb0-111">Set the following properties as shown in this example.</span></span>  
  
    ```vb  
    ToolTip1.InitialDelay = 500  
    ToolTip1.ReshowDelay = 100  
    ToolTip1.AutoPopDelay = 5000  
    ```  
  
    ```csharp  
    ToolTip1.InitialDelay = 500;  
    ToolTip1.ReshowDelay = 100;  
    ToolTip1.AutoPopDelay = 5000;  
    ```  
  
    ```cpp  
    toolTip1->InitialDelay = 500;  
    toolTip1->ReshowDelay = 100;  
    toolTip1->AutoPopDelay = 5000;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="55cb0-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55cb0-112">See also</span></span>

- [<span data-ttu-id="55cb0-113">Übersicht über die ToolTip-Komponente</span><span class="sxs-lookup"><span data-stu-id="55cb0-113">ToolTip Component Overview</span></span>](tooltip-component-overview-windows-forms.md)
- [<span data-ttu-id="55cb0-114">Vorgehensweise: Festlegen von QuickInfos für Steuerelemente auf einem Windows Form zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="55cb0-114">How to: Set ToolTips for Controls on a Windows Form at Design Time</span></span>](how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time.md)
- [<span data-ttu-id="55cb0-115">ToolTip-Komponente</span><span class="sxs-lookup"><span data-stu-id="55cb0-115">ToolTip Component</span></span>](tooltip-component-windows-forms.md)
