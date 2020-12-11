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
# <a name="how-to-use-tooltips-in-toolstrip-controls"></a>Vorgehensweise: Verwenden von QuickInfos in ToolStrip-Steuerelementen
Sie können ein <xref:System.Windows.Forms.ToolTip> <xref:System.Windows.Forms.ToolStrip> -Objekt für das gewünschte Steuerelement anzeigen, indem Sie die-Eigenschaft des-Steuer Elements auf festlegen <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> `true` .  
  
### <a name="to-display-a-tooltip"></a>So zeigen Sie eine QuickInfo an  
  
- Legen Sie die- <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> Eigenschaft des-Steuer Elements auf fest `true` .  
  
     Der Standardwert von <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A?displayProperty=nameWithType> ist `true` , und der Standardwert von <xref:System.Windows.Forms.MenuStrip.ShowItemToolTips%2A?displayProperty=nameWithType> und <xref:System.Windows.Forms.StatusStrip.ShowItemToolTips%2A?displayProperty=nameWithType> ist `false` .  
  
### <a name="to-use-the-tooltiptext-property-for-the-tooltip-text-of-a-toolstripbutton"></a>So verwenden Sie die ToolTipText-Eigenschaft für den QuickInfo-Text eines ToolStripButton  
  
1. Legen Sie die- <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> Eigenschaft der Schaltfläche auf fest `true` .  
  
2. Legen Sie die- <xref:System.Windows.Forms.ToolStripButton.AutoToolTip%2A?displayProperty=nameWithType> Eigenschaft der Schaltfläche auf fest `false` .  
  
     Die `AutoToolTip` -Eigenschaft ist `true` standardmäßig für <xref:System.Windows.Forms.ToolStripButton> , <xref:System.Windows.Forms.ToolStripDropDownButton> und <xref:System.Windows.Forms.ToolStripSplitButton> .  
  
     <xref:System.Windows.Forms.ToolStripButton>Verwendet `Text` standardmäßig die-Eigenschaft für den <xref:System.Windows.Forms.ToolTip> Text. Verwenden Sie dieses Verfahren, um benutzerdefinierten Text in einem anzuzeigen <xref:System.Windows.Forms.ToolStripButton> <xref:System.Windows.Forms.ToolTip> .  
  
> [!NOTE]
> Wenn Sie <xref:System.Windows.Forms.ToolStripItemDisplayStyle> auf <xref:System.Windows.Forms.ToolStripItemDisplayStyle.None> oder festlegen <xref:System.Windows.Forms.ToolStripItemDisplayStyle.Image> , wird kein Text auf der Schaltfläche angezeigt, aber die QuickInfo wird weiterhin angezeigt.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A>
- <xref:System.Windows.Forms.ToolStripButton>
- <xref:System.Windows.Forms.ToolStripDropDownButton>
- <xref:System.Windows.Forms.ToolStripSplitButton>
- [Übersicht über das ToolStrip-Steuerelement](toolstrip-control-overview-windows-forms.md)
