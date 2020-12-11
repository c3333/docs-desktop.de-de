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
# <a name="how-to-enable-the-tab-key-to-move-out-of-a-toolstrip-control"></a>Vorgehensweise: Aktivieren der TAB-TASTE zum Verlassen eines ToolStrip-Steuerelements
Verwenden Sie das folgende Verfahren, um dem Benutzer das Drücken der Tab-Taste zu ermöglichen, um von einem <xref:System.Windows.Forms.ToolStrip> zum nächsten Steuerelement in der Aktivier Reihenfolge zu wechseln.  
  
 Der <xref:System.Windows.Forms.ToolStrip> akzeptiert das erste Drücken der Tab-Taste, und die Pfeiltasten wählen Elemente in aus <xref:System.Windows.Forms.ToolStrip> . Wenn der Benutzer die Tab-Taste ein zweites Mal drückt, wird der Benutzer zum nächsten Steuerelement in der Aktivier Reihenfolge.  
  
### <a name="to-enable-the-user-to-press-the-tab-key-to-move-out-of-a-toolstrip-to-the-next-control"></a>So aktivieren Sie den Benutzer zum durch Drücken der Tab-Taste, um von einem ToolStrip zum nächsten Steuerelement zu wechseln  
  
- Legen Sie die <xref:System.Windows.Forms.ToolStrip.TabStop%2A>-Eigenschaft von <xref:System.Windows.Forms.ToolStrip> auf `true` fest.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.TabStop%2A>
- [Übersicht über das ToolStrip-Steuerelement](toolstrip-control-overview-windows-forms.md)
