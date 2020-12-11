---
title: Zusammenführen von Menü Elementen im MenuStrip-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- MenuStrip [Windows Forms], merging
- merging [Windows Forms], general concepts
ms.assetid: 95e113ba-f362-4dda-8a76-6d95ddc45cee
ms.openlocfilehash: 9fc2b40ef23d72db51853c124095b734a7646cda
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976704"
---
# <a name="merging-menu-items-in-the-windows-forms-menustrip-control"></a>Zusammenführen von Menüelementen im MenuStrip-Steuerelement von Windows Forms
Wenn Sie über eine MDI-Anwendung (Multiple Document Interface) verfügen, können Sie Menü Elemente oder gesamte Menüs aus dem untergeordneten Formular in den Menüs des übergeordneten Formulars zusammenführen.  
  
 In diesem Thema werden die grundlegenden Konzepte beschrieben, die für das Zusammenführen von Menü Elementen in einer MDI-Anwendung  
  
## <a name="general-concepts"></a>Allgemeine Konzepte  
 Beim Zusammenführen von Prozeduren werden eine Ziel-und eine Quell Code Verwaltung  
  
- Das Ziel ist das <xref:System.Windows.Forms.MenuStrip> Steuerelement auf dem übergeordneten Haupt-oder MDI-Formular, in dem Sie Menü Elemente zusammenführen.  
  
- Die Quelle ist das <xref:System.Windows.Forms.MenuStrip> Steuerelement auf dem untergeordneten MDI-Formular, das die Menü Elemente enthält, die Sie mit dem Zielmenü zusammenführen möchten.  
  
 Die <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> -Eigenschaft identifiziert das Menü Element, dessen Dropdown Liste mit den Titeln der untergeordneten MDI-untergeordneten MDI-Formulare aufgefüllt wird. Beispielsweise Listen Sie in der Regel die untergeordneten MDI-Elemente auf, die derzeit im Menü **Fenster** geöffnet sind.  
  
 Die- <xref:System.Windows.Forms.ToolStripMenuItem.IsMdiWindowListEntry%2A> Eigenschaft identifiziert, welche Menü Elemente von einem <xref:System.Windows.Forms.MenuStrip> auf einem untergeordneten MDI-Formular stammen.  
  
 Sie können Menü Elemente manuell oder automatisch zusammenführen. Die Menü Elemente werden für beide Methoden auf die gleiche Weise zusammengeführt, aber die Zusammenführung wird anders aktiviert, wie in den Abschnitten "Manuelles zusammenführen" und "Automatisches zusammenführen" weiter unten in diesem Thema erläutert. Bei manueller und automatischer Zusammenführung wirkt sich jede Merge-Aktion auf die nächste Zusammenführungs Aktion aus.  
  
 <xref:System.Windows.Forms.MenuStrip> beim Zusammenführen werden Menü Elemente von einem <xref:System.Windows.Forms.ToolStrip> zu einem anderen verschoben, anstatt Sie zu klonen, wie es bei der Fall war <xref:System.Windows.Forms.MainMenu> .  
  
## <a name="mergeaction-values"></a>MergeAction-Werte  
 Sie legen die Merge-Aktion für Menü Elemente in der Quelle <xref:System.Windows.Forms.MenuStrip> mithilfe der- <xref:System.Windows.Forms.MergeAction> Eigenschaft fest.  
  
 In der folgenden Tabelle werden die Bedeutung und die typische Verwendung der verfügbaren Merge-Aktionen beschrieben.  
  
|MergeAction-Wert|BESCHREIBUNG|Typische Verwendung|  
|-----------------------|-----------------|-----------------|  
|<xref:System.Windows.Forms.MergeAction.Append>|Vorgegebene Fügt das Quell Element am Ende der Auflistung des Ziel Elements hinzu.|Hinzufügen von Menü Elementen am Ende des Menüs, wenn ein Teil des Programms aktiviert ist.|  
|<xref:System.Windows.Forms.MergeAction.Insert>|Fügt der Auflistung des Ziel Elements das Quell Element an dem Speicherort hinzu, der durch die <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> für das Quell Element festgelegte-Eigenschaft angegeben wird.|Hinzufügen von Menü Elementen zur Mitte oder am Anfang des Menüs, wenn ein Teil des Programms aktiviert ist.<br /><br /> Wenn der Wert von <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> für beide Menü Elemente identisch ist, werden Sie in umgekehrter Reihenfolge hinzugefügt. Legen <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> Sie entsprechend fest, um die ursprüngliche Reihenfolge beizubehalten.|  
|<xref:System.Windows.Forms.MergeAction.Replace>|Sucht eine Text Übereinstimmung oder verwendet den <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> Wert, wenn keine Text Übereinstimmung gefunden wurde, und ersetzt dann das entsprechende Ziel Menü Element durch das Quell Menü Element.|Ersetzen eines Ziel Menü Elements durch ein Quell Menü Element desselben Namens, das etwas anderes unterscheidet.|  
|<xref:System.Windows.Forms.MergeAction.MatchOnly>|Findet eine Text Übereinstimmung oder verwendet den- <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> Wert, wenn keine Text Übereinstimmung gefunden wird, und fügt dann alle Dropdown Elemente aus der Quelle zum Ziel hinzu.|Aufbau einer Menüstruktur, die Menü Elemente in einem Untermenü einfügt oder hinzufügt oder Menü Elemente aus einem Untermenü entfernt. Beispielsweise können Sie ein Menü Element aus einem untergeordneten MDI- <xref:System.Windows.Forms.MenuStrip> Menü einem Hauptmenü **Speichern** unter Hinzufügen.<br /><br /> <xref:System.Windows.Forms.MergeAction.MatchOnly> ermöglicht es Ihnen, durch die Menüstruktur zu navigieren, ohne eine Aktion durchlaufen zu müssen. Sie bietet eine Möglichkeit, die nachfolgenden Elemente auszuwerten.|  
|<xref:System.Windows.Forms.MergeAction.Remove>|Sucht eine Text Übereinstimmung oder verwendet den <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> Wert, wenn keine Text Übereinstimmung gefunden wurde, und entfernt dann das Element aus dem Ziel.|Ein Menü Element wird aus dem Ziel entfernt <xref:System.Windows.Forms.MenuStrip> .|  
  
## <a name="manual-merging"></a>Manuelles Mergen  
 Nur Steuer <xref:System.Windows.Forms.MenuStrip> Elemente nehmen an der automatischen Zusammenführung Teil. Um die Elemente anderer Steuerelemente, z. b.-und-Steuerelemente, zu kombinieren, <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.StatusStrip> müssen Sie Sie manuell zusammenführen, indem Sie die <xref:System.Windows.Forms.ToolStripManager.Merge%2A> -Methode und die- <xref:System.Windows.Forms.ToolStripManager.RevertMerge%2A> Methode in Ihrem Code  
  
## <a name="automatic-merging"></a>Automatisches Mergen  
 Sie können die automatische Zusammenführung für MDI-Anwendungen verwenden, indem Sie das Quell Formular aktivieren. Wenn Sie <xref:System.Windows.Forms.MenuStrip> in einer MDI-Anwendung verwenden möchten, legen Sie die- <xref:System.Windows.Forms.Form.MainMenuStrip%2A> Eigenschaft auf das Ziel fest, <xref:System.Windows.Forms.MenuStrip> damit die für die Quelle ausgeführten Zusammenführungs Aktionen <xref:System.Windows.Forms.MenuStrip> im Ziel wiedergegeben werden <xref:System.Windows.Forms.MenuStrip> .  
  
 Sie können das automatische Zusammenführen durch Aktivieren von <xref:System.Windows.Forms.MenuStrip> für die MDI-Quelle auslöst. Bei Aktivierung wird die Quelle <xref:System.Windows.Forms.MenuStrip> in das MDI-Ziel zusammengeführt. Wenn ein neues Formular aktiv wird, wird die Zusammenführung im letzten Formular wieder hergestellt und im neuen Formular ausgelöst. Sie können dieses Verhalten steuern, indem Sie die <xref:System.Windows.Forms.ToolStripItem.MergeAction%2A> -Eigenschaft auf jeden Bedarf festlegen <xref:System.Windows.Forms.ToolStripItem> und die- <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> Eigenschaft für jede festlegen <xref:System.Windows.Forms.MenuStrip> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStripManager>
- <xref:System.Windows.Forms.MenuStrip>
- [MenuStrip-Steuerelement](menustrip-control-windows-forms.md)
- [Vorgehensweise: Erstellen einer MDI-Fensterliste mithilfe von MenuStrip](how-to-create-an-mdi-window-list-with-menustrip-windows-forms.md)
- [Vorgehensweise: Einrichten des automatischem Zusammenführens von Menüs für MDI-Anwendungen (Multiple Document Interface)](how-to-set-up-automatic-menu-merging-for-mdi-applications.md)
