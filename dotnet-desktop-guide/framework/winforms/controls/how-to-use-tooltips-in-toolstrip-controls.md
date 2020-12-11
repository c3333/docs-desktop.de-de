---
title: 'Vorgehensweise: Verwenden von QuickInfos in ToolStrip-Steuerelementen'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStrip control [Windows Forms], adding tooltips
- toolbars [Windows Forms], adding tooltips
- tooltips [Windows Forms], adding
ms.assetid: c5d86024-a7c5-44ee-8b3f-2daf53d80d3e
ms.openlocfilehash: 3f383b6cccba7825637ea65a0e13280b91b406c9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976742"
---
# <a name="how-to-use-tooltips-in-toolstrip-controls"></a><span data-ttu-id="5779e-102">Vorgehensweise: Verwenden von QuickInfos in ToolStrip-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="5779e-102">How to: Use ToolTips in ToolStrip Controls</span></span>
<span data-ttu-id="5779e-103">Sie können ein <xref:System.Windows.Forms.ToolTip> <xref:System.Windows.Forms.ToolStrip> -Objekt für das gewünschte Steuerelement anzeigen, indem Sie die-Eigenschaft des-Steuer Elements auf festlegen <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> `true` .</span><span class="sxs-lookup"><span data-stu-id="5779e-103">You can display a <xref:System.Windows.Forms.ToolTip> for the <xref:System.Windows.Forms.ToolStrip> control you want by setting the control's <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> property to `true`.</span></span>  
  
### <a name="to-display-a-tooltip"></a><span data-ttu-id="5779e-104">So zeigen Sie eine QuickInfo an</span><span class="sxs-lookup"><span data-stu-id="5779e-104">To display a ToolTip</span></span>  
  
- <span data-ttu-id="5779e-105">Legen Sie die- <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> Eigenschaft des-Steuer Elements auf fest `true` .</span><span class="sxs-lookup"><span data-stu-id="5779e-105">Set the <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> property of the control to `true`.</span></span>  
  
     <span data-ttu-id="5779e-106">Der Standardwert von <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A?displayProperty=nameWithType> ist `true` , und der Standardwert von <xref:System.Windows.Forms.MenuStrip.ShowItemToolTips%2A?displayProperty=nameWithType> und <xref:System.Windows.Forms.StatusStrip.ShowItemToolTips%2A?displayProperty=nameWithType> ist `false` .</span><span class="sxs-lookup"><span data-stu-id="5779e-106">The default value of <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A?displayProperty=nameWithType> is `true`, and the default value of <xref:System.Windows.Forms.MenuStrip.ShowItemToolTips%2A?displayProperty=nameWithType> and <xref:System.Windows.Forms.StatusStrip.ShowItemToolTips%2A?displayProperty=nameWithType> is `false`.</span></span>  
  
### <a name="to-use-the-tooltiptext-property-for-the-tooltip-text-of-a-toolstripbutton"></a><span data-ttu-id="5779e-107">So verwenden Sie die ToolTipText-Eigenschaft für den QuickInfo-Text eines ToolStripButton</span><span class="sxs-lookup"><span data-stu-id="5779e-107">To use the ToolTipText property for the ToolTip text of a ToolStripButton</span></span>  
  
1. <span data-ttu-id="5779e-108">Legen Sie die- <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> Eigenschaft der Schaltfläche auf fest `true` .</span><span class="sxs-lookup"><span data-stu-id="5779e-108">Set the <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> property of the button to `true`.</span></span>  
  
2. <span data-ttu-id="5779e-109">Legen Sie die- <xref:System.Windows.Forms.ToolStripButton.AutoToolTip%2A?displayProperty=nameWithType> Eigenschaft der Schaltfläche auf fest `false` .</span><span class="sxs-lookup"><span data-stu-id="5779e-109">Set the <xref:System.Windows.Forms.ToolStripButton.AutoToolTip%2A?displayProperty=nameWithType> property of the button to `false`.</span></span>  
  
     <span data-ttu-id="5779e-110">Die `AutoToolTip` -Eigenschaft ist `true` standardmäßig für <xref:System.Windows.Forms.ToolStripButton> , <xref:System.Windows.Forms.ToolStripDropDownButton> und <xref:System.Windows.Forms.ToolStripSplitButton> .</span><span class="sxs-lookup"><span data-stu-id="5779e-110">The `AutoToolTip` property is `true` by default for <xref:System.Windows.Forms.ToolStripButton>, <xref:System.Windows.Forms.ToolStripDropDownButton>, and <xref:System.Windows.Forms.ToolStripSplitButton>.</span></span>  
  
     <span data-ttu-id="5779e-111"><xref:System.Windows.Forms.ToolStripButton>Verwendet `Text` standardmäßig die-Eigenschaft für den <xref:System.Windows.Forms.ToolTip> Text.</span><span class="sxs-lookup"><span data-stu-id="5779e-111">A <xref:System.Windows.Forms.ToolStripButton> uses its `Text` property for the <xref:System.Windows.Forms.ToolTip> text by default.</span></span> <span data-ttu-id="5779e-112">Verwenden Sie dieses Verfahren, um benutzerdefinierten Text in einem anzuzeigen <xref:System.Windows.Forms.ToolStripButton> <xref:System.Windows.Forms.ToolTip> .</span><span class="sxs-lookup"><span data-stu-id="5779e-112">Use this procedure to display custom text in a <xref:System.Windows.Forms.ToolStripButton><xref:System.Windows.Forms.ToolTip>.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="5779e-113">Wenn Sie <xref:System.Windows.Forms.ToolStripItemDisplayStyle> auf <xref:System.Windows.Forms.ToolStripItemDisplayStyle.None> oder festlegen <xref:System.Windows.Forms.ToolStripItemDisplayStyle.Image> , wird kein Text auf der Schaltfläche angezeigt, aber die QuickInfo wird weiterhin angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5779e-113">If you set <xref:System.Windows.Forms.ToolStripItemDisplayStyle> to <xref:System.Windows.Forms.ToolStripItemDisplayStyle.None> or <xref:System.Windows.Forms.ToolStripItemDisplayStyle.Image>, no text will appear on the button, but the tool tip still appears.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5779e-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5779e-114">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A>
- <xref:System.Windows.Forms.ToolStripButton>
- <xref:System.Windows.Forms.ToolStripDropDownButton>
- <xref:System.Windows.Forms.ToolStripSplitButton>
- [<span data-ttu-id="5779e-115">Übersicht über das ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5779e-115">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
