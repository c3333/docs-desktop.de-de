---
title: Übersicht über das ToolStrip-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- Toolstrip
helpviewer_keywords:
- ToolStrip control [Windows Forms], about ToolStrip control
- toolbars [Windows Forms], what's new in Windows Forms
- toolbars [Windows Forms]
- what's new [Windows Forms], toolbars
ms.assetid: 81d067ed-297c-4dad-90de-1bcac15336ec
ms.openlocfilehash: 931a6a0ea09f9b684b793c05cb1c3db8ee8fb7c7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977171"
---
# <a name="toolstrip-control-overview-windows-forms"></a>Übersicht über das ToolStrip-Steuerelement (Windows Forms)
Das Windows Forms <xref:System.Windows.Forms.ToolStrip> -Steuerelement und die zugehörigen Klassen bieten ein gängiges Framework zum Kombinieren von Benutzeroberflächen Elementen in Symbolleisten, Status leisten und Menüs. <xref:System.Windows.Forms.ToolStrip> Steuerelemente bieten eine umfangreiche Entwurfszeit Darstellung, die eine direkte Aktivierung und Bearbeitung, ein benutzerdefiniertes Layout und ein Rafting umfasst. Dies ist die Fähigkeit von Symbolleisten, horizontalen oder vertikalen Raum freizugeben.  
  
 Obwohl <xref:System.Windows.Forms.ToolStrip> das-Steuerelement in früheren Versionen ersetzt und Funktionen zum-Steuerelement hinzufügt, wird bei Bedarf <xref:System.Windows.Forms.ToolBar> sowohl für die Abwärtskompatibilität als auch für die zukünftige Verwendung beibehalten.  
  
## <a name="features-of-the-toolstrip-controls"></a>Funktionen der ToolStrip-Steuerelemente  
 Verwenden <xref:System.Windows.Forms.ToolStrip> Sie das Steuerelement für Folgendes:  
  
- Stellen Sie eine gemeinsame Benutzeroberfläche in Containern dar.  
  
- Erstellen Sie einfach angepasste, häufig verwendete Symbolleisten, die erweiterte Benutzeroberflächen-und Layoutfunktionen unterstützen, wie z. b. andocken, Rafting, Schaltflächen mit Text und Bildern, Dropdown Schaltflächen und Steuerelemente, Überlauf Schaltflächen und die Neuanordnung von Elementen zur Laufzeit <xref:System.Windows.Forms.ToolStrip> .  
  
- Unterstützung von Überlauf-und Lauf Zeitelement-Neuanordnung von Elementen. Die Überlauf Funktion verschiebt Elemente in ein Dropdown Menü, wenn nicht genügend Platz vorhanden ist, um Sie in einem anzuzeigen <xref:System.Windows.Forms.ToolStrip> .  
  
- Unterstützen Sie das typische Aussehen und Verhalten des Betriebssystems durch ein gängiges Renderingmodell.  
  
- Behandeln Sie Ereignisse konsistent für alle Container und enthaltenen Elemente auf die gleiche Weise wie Ereignisse für andere Steuerelemente.  
  
- Ziehen Sie Elemente aus einem <xref:System.Windows.Forms.ToolStrip> in ein anderes oder innerhalb eines <xref:System.Windows.Forms.ToolStrip> .  
  
- Erstellen Sie Dropdown-Steuerelemente und benutzerschnittstellentyp-Editoren mit erweiterten Layouts in einer <xref:System.Windows.Forms.ToolStripDropDown> .  
  
 Verwenden <xref:System.Windows.Forms.ToolStripControlHost> Sie die-Klasse, um andere Steuerelemente auf einem zu verwenden <xref:System.Windows.Forms.ToolStrip> und <xref:System.Windows.Forms.ToolStrip> Funktionen für diese zu erhalten.  
  
 Sie können die Funktionalität erweitern und das Aussehen und Verhalten ändern, indem Sie <xref:System.Windows.Forms.ToolStripRenderer> , <xref:System.Windows.Forms.ToolStripProfessionalRenderer> und <xref:System.Windows.Forms.ToolStripManager> zusammen mit den <xref:System.Windows.Forms.ToolStripRenderMode> <xref:System.Windows.Forms.ToolStripManagerRenderMode> Enumerationen und verwenden.  
  
 Das <xref:System.Windows.Forms.ToolStrip> Steuerelement ist hochgradig konfigurier Bar und erweiterbar und bietet viele Eigenschaften, Methoden und Ereignisse, um Darstellung und Verhalten anzupassen. Unten sind einige wichtige Mitglieder aufgeführt:  
  
### <a name="important-toolstrip-members"></a>Wichtige ToolStrip-Member  
  
|Name|BESCHREIBUNG|  
|----------|-----------------|  
|<xref:System.Windows.Forms.ToolStrip.Dock%2A>|Ruft ab oder legt fest, an welchen Rand des übergeordneten Containers a <xref:System.Windows.Forms.ToolStrip> angedockt wird.|  
|<xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A>|Ruft einen Wert ab bzw. legt einen Wert fest, der angibt, ob Drag &amp; Drop und die Neuanordnung von Elementen von der <xref:System.Windows.Forms.ToolStrip>-Klasse privat behandelt werden.|  
|<xref:System.Windows.Forms.ToolStrip.LayoutStyle%2A>|Ruft einen Wert ab, der angibt, wie das <xref:System.Windows.Forms.ToolStrip> seine Elemente festlegt, oder legt diesen fest.|  
|<xref:System.Windows.Forms.ToolStripItem.Overflow%2A>|Ruft ab oder legt fest <xref:System.Windows.Forms.ToolStripItem> , ob ein an das oder das angefügt ist <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.ToolStripOverflowButton> oder zwischen beiden hängen kann.|  
|<xref:System.Windows.Forms.ToolStrip.IsDropDown%2A>|Ruft einen Wert ab, der angibt, ob ein <xref:System.Windows.Forms.ToolStripItem> andere Elemente in einer Dropdown Liste anzeigt, wenn auf das <xref:System.Windows.Forms.ToolStripItem> geklickt wird.|  
|<xref:System.Windows.Forms.ToolStrip.OverflowButton%2A>|Ruft das <xref:System.Windows.Forms.ToolStripItem>-Objekt ab, das der Überlaufschaltfläche für ein <xref:System.Windows.Forms.ToolStrip>-Objekt mit aktiviertem Überlauf entspricht.|  
|<xref:System.Windows.Forms.ToolStrip.Renderer%2A>|Ruft eine ab <xref:System.Windows.Forms.ToolStripRenderer> , mit der die Darstellung und das Verhalten (Aussehen und Verhalten) eines angepasst werden, oder legt diese fest <xref:System.Windows.Forms.ToolStrip> .|  
|<xref:System.Windows.Forms.ToolStrip.RenderMode%2A>|Ruft die Zeichenstile ab bzw. legt diese fest, die auf <xref:System.Windows.Forms.ToolStrip> angewendet werden sollen.|  
|<xref:System.Windows.Forms.ToolStrip.RendererChanged>|Wird ausgelöst, wenn sich die <xref:System.Windows.Forms.ToolStrip.Renderer%2A>-Eigenschaft ändert.|  
  
 Die <xref:System.Windows.Forms.ToolStrip> Flexibilität des Steuer Elements wird durch die Verwendung einer Reihe von begleitenden Klassen erreicht. Unten sind einige der bemerkenswertesten:  
  
### <a name="important-toolstrip-companion-classes"></a>Wichtige ToolStrip-Begleit Klassen  
  
|Name|BESCHREIBUNG|  
|----------|-----------------|  
|<xref:System.Windows.Forms.MenuStrip>|Ersetzt die-Klasse und fügt diese hinzu <xref:System.Windows.Forms.MainMenu> .|  
|<xref:System.Windows.Forms.StatusStrip>|Ersetzt die-Klasse und fügt diese hinzu <xref:System.Windows.Forms.StatusBar> .|  
|<xref:System.Windows.Forms.ContextMenuStrip>|Ersetzt die-Klasse und fügt diese hinzu <xref:System.Windows.Forms.ContextMenu> .|  
|<xref:System.Windows.Forms.ToolStripItem>|Eine abstrakte Basisklasse, die Ereignisse und das Layout für alle Elemente verwaltet, die ein-,-oder-Element <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.ToolStripControlHost> <xref:System.Windows.Forms.ToolStripDropDown> enthalten kann.|  
|<xref:System.Windows.Forms.ToolStripContainer>|Stellt einen Container mit einem Panel auf jeder Seite des Formulars bereit, in dem Steuerelemente auf verschiedene Arten angeordnet werden können.|  
|<xref:System.Windows.Forms.ToolStripRenderer>|Behandelt die Zeichenfunktionen für <xref:System.Windows.Forms.ToolStrip>-Objekte.|  
|<xref:System.Windows.Forms.ToolStripProfessionalRenderer>|Stellt Microsoft Office Darstellung bereit.|  
|<xref:System.Windows.Forms.ToolStripManager>|Steuert das Rendering und das Rafting von <xref:System.Windows.Forms.ToolStrip> sowie das Zusammenführen von Objekten vom Typ <xref:System.Windows.Forms.MenuStrip>, <xref:System.Windows.Forms.ToolStripDropDownMenu> und <xref:System.Windows.Forms.ToolStripMenuItem>.|  
|<xref:System.Windows.Forms.ToolStripManagerRenderMode>|Gibt den Zeichnungs Stil (Custom, Windows XP oder Microsoft Office Professional) an, der auf mehrere <xref:System.Windows.Forms.ToolStrip> in einem Formular enthaltene Objekte angewendet wird.|  
|<xref:System.Windows.Forms.ToolStripRenderMode>|Gibt den Zeichnungs Stil (Custom, Windows XP oder Microsoft Office Professional) an, der auf ein <xref:System.Windows.Forms.ToolStrip> in einem Formular enthaltenes Objekt angewendet wird.|  
|<xref:System.Windows.Forms.ToolStripControlHost>|Hostet andere Steuerelemente, die nicht speziell Steuerelemente sind, <xref:System.Windows.Forms.ToolStrip> für die Sie jedoch <xref:System.Windows.Forms.ToolStrip> Funktionen benötigen.|  
|<xref:System.Windows.Forms.ToolStripItemPlacement>|Gibt an, ob ein <xref:System.Windows.Forms.ToolStripItem> auf dem Haupt- <xref:System.Windows.Forms.ToolStrip> , im Überlauf-oder in keinem von beiden angeordnet werden soll <xref:System.Windows.Forms.ToolStrip> .|  
  
 Weitere Informationen finden Sie unter [ToolStrip-Technologie Zusammenfassung](toolstrip-technology-summary.md) und [ToolStrip-Steuerelement Architektur](toolstrip-control-architecture.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.StatusStrip>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripDropDown>
