---
title: Übersicht über das StatusStrip-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- StatusStrip
helpviewer_keywords:
- StatusStrip control [Windows Forms], about StatusStrip control
- status bars [Windows Forms], about status bars
ms.assetid: c0d9bcbb-f8b8-46ef-bae2-4146b8c8ce99
ms.openlocfilehash: 9f2426220e8fe0f13d2098de8975be2ad2e43845
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976456"
---
# <a name="statusstrip-control-overview"></a>Übersicht über das StatusStrip-Steuerelement

Ein <xref:System.Windows.Forms.StatusStrip>-Steuerelement zeigt Informationen zu einem Objekt an, das in einem <xref:System.Windows.Forms.Form> angezeigt wird, zu den Komponenten des Objekts oder Kontextinformationen, die sich auf die Operation dieses Objekts in Ihrer Anwendung beziehen. Ein <xref:System.Windows.Forms.StatusStrip>-Steuerelement besteht normalerweise aus <xref:System.Windows.Forms.ToolStripStatusLabel>-Objekten, von denen jedes Text, ein Symbol oder beides anzeigt. Der <xref:System.Windows.Forms.StatusStrip> kann zudem auch <xref:System.Windows.Forms.ToolStripDropDownButton>-, <xref:System.Windows.Forms.ToolStripSplitButton> und <xref:System.Windows.Forms.ToolStripProgressBar>-Steuerelemente enthalten.  
  
 Der standardmäßige <xref:System.Windows.Forms.StatusStrip> weist keine Panels auf. Verwenden Sie die <xref:System.Windows.Forms.ToolStripItemCollection.AddRange%2A?displayProperty=nameWithType>-Methode, um einem <xref:System.Windows.Forms.StatusStrip> Panels hinzuzufügen.  
  
 Es gibt umfassende Unterstützung für den Umgang mit <xref:System.Windows.Forms.StatusStrip>-Elementen und häufig verwendeten Befehle in Visual Studio.  
  
 Siehe auch Dialog Feld "Status Strip-Elementauflistungs- [Editor](/previous-versions/visualstudio/visual-studio-2010/ms233631(v=vs.100)) " und " [Status Strip-Aufgaben](/previous-versions/visualstudio/visual-studio-2010/ms233642(v=vs.100))".  
  
 Obwohl <xref:System.Windows.Forms.StatusStrip> das <xref:System.Windows.Forms.StatusBar>-Steuerelement vorheriger Versionen ersetzt und erweitert, wird das <xref:System.Windows.Forms.StatusBar>-Steuerelement sowohl aus Gründen der Abwärtskompatibilität als auch, falls gewünscht, für die zukünftige Verwendung beibehalten.  
  
### <a name="important-statusstrip-members"></a>Wichtige StatusStrip-Member  
  
|Name|BESCHREIBUNG|  
|----------|-----------------|  
|<xref:System.Windows.Forms.StatusStrip.CanOverflow%2A>|Ruft einen Wert ab, der angibt, ob <xref:System.Windows.Forms.StatusStrip> Überlauffunktionen unterstützt, bzw. legt diesen fest.|  
|<xref:System.Windows.Forms.StatusStrip.Stretch%2A>|Ruft einen Wert ab, der angibt, ob sich das <xref:System.Windows.Forms.StatusStrip>-Objekt in seinem <xref:System.Windows.Forms.ToolStripContainer>-Objekt von einem Ende zum anderen Ende erstreckt, oder legt diesen Wert fest.|  
  
### <a name="important-statusstrip-companion-classes"></a>Wichtige StatusStrip-Begleitklassen  
  
|Name|BESCHREIBUNG|  
|----------|-----------------|  
|<xref:System.Windows.Forms.ToolStripStatusLabel>|Stellt ein Panel in einem <xref:System.Windows.Forms.StatusStrip>-Steuerelement dar.|  
|<xref:System.Windows.Forms.ToolStripDropDownButton>|Zeigt eine zugehörige <xref:System.Windows.Forms.ToolStripDropDown> an, aus der der Benutzer ein einzelnes Element auswählen kann.|  
|<xref:System.Windows.Forms.ToolStripSplitButton>|Stellt ein zweiteiliges Steuerelement dar, das aus einer Standardschaltfläche und einem Dropdownmenü besteht.|  
|<xref:System.Windows.Forms.ToolStripProgressBar>|Zeigt den Fortschrittsstatus eines Prozesses an.|  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.StatusStrip>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- <xref:System.Windows.Forms.ToolStripStatusLabel.Spring%2A>
