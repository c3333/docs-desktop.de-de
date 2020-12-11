---
title: Übersicht über das MenuStrip-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- MenuStrip
helpviewer_keywords:
- MenuStrip control [Windows Forms], about MenuStrip control
- menus [Windows Forms], creating
ms.assetid: f45516e5-bf01-4468-b851-d45f4c33c055
ms.openlocfilehash: a536d13cb7be3f4e4e4a085e1a4da1b0899b3a0c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976705"
---
# <a name="menustrip-control-overview-windows-forms"></a>Übersicht über das MenuStrip-Steuerelement (Windows Forms)
Menüs machen die Funktionalität für Ihre Benutzer verfügbar, indem Sie Befehle halten, die nach einem allgemeinen Design gruppiert sind.  
  
 Das- <xref:System.Windows.Forms.MenuStrip> Steuerelement wurde in Version 2,0 des .NET Framework eingeführt. Mit dem- <xref:System.Windows.Forms.MenuStrip> Steuerelement können Sie problemlos Menüs wie die in Microsoft Office erstellen.  
  
 Das <xref:System.Windows.Forms.MenuStrip> -Steuerelement unterstützt die MDI (Multiple Document Interface) und die Zusammenführung von Menüs, Quick Infos und Überlauf. Sie können die Benutzerfreundlichkeit und Lesbarkeit Ihrer Menüs verbessern, indem Sie Zugriffstasten, Tastenkombinationen, Häkchen, Bilder und Trenn leisten hinzufügen.  
  
 Das <xref:System.Windows.Forms.MenuStrip> -Steuerelement ersetzt und fügt Funktionen zum-Steuerelement hinzu. das-Steuerelement <xref:System.Windows.Forms.MainMenu> <xref:System.Windows.Forms.MainMenu> wird jedoch aus Gründen der Abwärtskompatibilität und zukünftiger Verwendung beibehalten, wenn Sie es auswählen.  
  
## <a name="ways-to-use-the-menustrip-control"></a>Möglichkeiten der Verwendung des MenuStrip-Steuer Elements  
 Verwenden <xref:System.Windows.Forms.MenuStrip> Sie das Steuerelement für Folgendes:  
  
- Erstellen Sie problemlos angepasste, häufig verwendete Menüs, die erweiterte Benutzeroberflächen-und Layoutfeatures unterstützen, wie z. b. Text-und Bild Anordnung und-Ausrichtung, Drag & Drop-Vorgänge, MDI, Überlauf und Alternative Zugriffsmöglichkeiten für Menübefehle.  
  
- Unterstützen Sie das typische Aussehen und Verhalten des Betriebssystems.  
  
- Behandeln Sie Ereignisse konsistent für alle Container und enthaltenen Elemente auf die gleiche Weise wie Ereignisse für andere Steuerelemente.  
  
 In der folgenden Tabelle werden einige besonders wichtige Eigenschaften von <xref:System.Windows.Forms.MenuStrip> und zugeordneten Klassen angezeigt.  
  
|Eigenschaft|BESCHREIBUNG|  
|--------------|-----------------|  
|<xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A>|Ruft den ab <xref:System.Windows.Forms.ToolStripMenuItem> , mit dem eine Liste von untergeordneten MDI-Formularen angezeigt wird, oder legt diesen fest.|  
|<xref:System.Windows.Forms.ToolStripItem.MergeAction%2A?displayProperty=nameWithType>|Ruft ab oder legt fest, wie untergeordnete Menüs mit übergeordneten Menüs in MDI-Anwendungen zusammengeführt werden.|  
|<xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A?displayProperty=nameWithType>|Ruft die Position eines zusammengeführten Elements in einem Menü in MDI-Anwendungen ab oder legt diese fest.|  
|<xref:System.Windows.Forms.Form.IsMdiContainer%2A?displayProperty=nameWithType>|Dient zum Abrufen oder Festlegen eines Werts, der angibt, ob das Formular ein Container für untergeordnete MDI-Formulare ist.|  
|<xref:System.Windows.Forms.MenuStrip.ShowItemToolTips%2A>|Ruft einen Wert ab, der angibt, ob Quick Infos für angezeigt werden, oder legt diesen fest <xref:System.Windows.Forms.MenuStrip> .|  
|<xref:System.Windows.Forms.MenuStrip.CanOverflow%2A>|Ruft einen Wert ab, der angibt, ob <xref:System.Windows.Forms.MenuStrip> Überlauffunktionen unterstützt, bzw. legt diesen fest.|  
|<xref:System.Windows.Forms.ToolStripMenuItem.ShortcutKeys%2A>|Ruft die Tastenkombinationen ab, die dem <xref:System.Windows.Forms.ToolStripMenuItem> zugeordnet sind, bzw. legt diese fest.|  
|<xref:System.Windows.Forms.ToolStripMenuItem.ShowShortcutKeys%2A>|Ruft einen Wert ab, der angibt, ob die Tastenkombinationen, die dem <xref:System.Windows.Forms.ToolStripMenuItem> zugeordnet sind, neben dem <xref:System.Windows.Forms.ToolStripMenuItem> angezeigt werden, bzw. legt diesen fest.|  
  
 In der folgenden Tabelle sind die wichtigen <xref:System.Windows.Forms.MenuStrip> Begleit Klassen aufgeführt.  
  
|Klasse|BESCHREIBUNG|  
|-----------|-----------------|  
|<xref:System.Windows.Forms.ToolStripMenuItem>|Stellt eine Option dar, die in einem <xref:System.Windows.Forms.MenuStrip> oder einem <xref:System.Windows.Forms.ContextMenuStrip> angezeigt wird, und die ausgewählt werden kann.|  
|<xref:System.Windows.Forms.ContextMenuStrip>|Stellt ein Kontextmenü dar.|  
|<xref:System.Windows.Forms.ToolStripDropDown>|Stellt ein Steuerelement dar, mit dem der Benutzer ein einzelnes Element aus einer Liste auswählen kann, die angezeigt wird, wenn der Benutzer auf ein <xref:System.Windows.Forms.ToolStripDropDownButton> Menü Element oder ein höheres Menü Element klickt.|  
|<xref:System.Windows.Forms.ToolStripDropDownItem>|Stellt grundlegende Funktionen für Steuerelemente bereit <xref:System.Windows.Forms.ToolStripItem> , die von diesen Dropdown Elementen angezeigt werden, wenn darauf geklickt wird.|  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.StatusStrip>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripDropDown>
