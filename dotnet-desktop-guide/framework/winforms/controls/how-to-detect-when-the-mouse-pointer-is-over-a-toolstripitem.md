---
title: 'Vorgehensweise: Erkennen des Mauszeigers auf einem ToolStripItem'
ms.date: 03/30/2017
helpviewer_keywords:
- toolbars [Windows Forms], detecting mouse movement
- ToolStrip control [Windows Forms], detecting mouse movement
- ToolStripItem class [Windows Forms], detecting mouse movement
- mouse [Windows Forms], detecting movement on toolbars
ms.assetid: d38b5082-aba7-4f6c-841b-bd9714e307fd
ms.openlocfilehash: f01a9acb3a566be40d65fb075c8487d4e9cb6e73
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975665"
---
# <a name="how-to-detect-when-the-mouse-pointer-is-over-a-toolstripitem"></a>Vorgehensweise: Erkennen des Mauszeigers auf einem ToolStripItem
Verwenden Sie das folgende Verfahren, um zu erkennen, wenn sich der Mauszeiger über einem befindet <xref:System.Windows.Forms.ToolStripItem> .  
  
### <a name="to-detect-when-the-pointer-is-over-a-toolstripitem"></a>So erkennen Sie, wenn sich der Zeiger über einem ToolStripItem befindet  
  
- Verwenden Sie die- <xref:System.Windows.Forms.ToolStripItem.Selected%2A> Eigenschaft für Elemente, in denen <xref:System.Windows.Forms.ToolStripItem.CanSelect%2A> ist `true` .  
  
     Dadurch wird verhindert, dass das <xref:System.Windows.Forms.ToolStripItem.MouseEnter> -Ereignis und das-Ereignis synchronisiert werden müssen <xref:System.Windows.Forms.ToolStripItem.MouseLeave> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripItem.Selected%2A>
- [Übersicht über das ToolStrip-Steuerelement](toolstrip-control-overview-windows-forms.md)
