---
title: Virtueller Modus im DataGridView-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], virtual mode
ms.assetid: feae5d43-2848-4b1a-8ea7-77085dc415b5
ms.openlocfilehash: 0d82f0fc9946e5b61ea171f2f5d2ab5690db0c71
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977255"
---
# <a name="virtual-mode-in-the-windows-forms-datagridview-control"></a>Virtueller Modus im DataGridView-Steuerelement in Windows Forms
Mit dem virtuellen Modus können Sie die Interaktion zwischen dem <xref:System.Windows.Forms.DataGridView> Steuerelement und einem benutzerdefinierten Daten Cache verwalten. Wenn Sie den virtuellen Modus implementieren möchten, legen <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> Sie die-Eigenschaft auf fest, `true` und behandeln Sie mindestens eines der in diesem Thema beschriebenen Ereignisse. Normalerweise verarbeiten Sie zumindest das- `CellValueNeeded` Ereignis, das dem Steuerelement das Suchen nach Werten im Daten Cache ermöglicht.  
  
## <a name="bound-mode-and-virtual-mode"></a>Gebundener Modus und virtueller Modus  
 Der virtuelle Modus ist nur erforderlich, wenn Sie den gebundenen Modus ergänzen oder ersetzen müssen. Im gebundenen Modus wird die-Eigenschaft festgelegt, <xref:System.Windows.Forms.DataGridView.DataSource%2A> und das-Steuerelement lädt die Daten automatisch aus der angegebenen Quelle und übermittelt die Benutzer Änderungen zurück an die-Eigenschaft. Sie können steuern, welche der gebundenen Spalten angezeigt werden, und die Datenquelle selbst verarbeitet Vorgänge wie z. b. die Sortierung.  
  
## <a name="supplementing-bound-mode"></a>Ergänzen des gebundenen Modus  
 Sie können den gebundenen Modus ergänzen, indem Sie ungebundene Spalten zusammen mit den gebundenen Spalten anzeigen. Dies wird manchmal als "gemischter Modus" bezeichnet und eignet sich zum Anzeigen von Elementen wie berechneten Werten oder Benutzeroberflächen Steuerelementen (UI).  
  
 Da ungebundene Spalten sich außerhalb der Datenquelle befinden, werden Sie von den Sortiervorgängen der Datenquelle ignoriert. Wenn Sie die Sortierung im gemischten Modus aktivieren, müssen Sie daher die ungebundenen Daten in einem lokalen Cache verwalten und den virtuellen Modus implementieren, damit das <xref:System.Windows.Forms.DataGridView> Steuerelement mit dem Steuerelement interagieren kann.  
  
 Weitere Informationen zum Verwenden des virtuellen Modus zum Verwalten der Werte in ungebundenen Spalten finden Sie in den Beispielen in den <xref:System.Windows.Forms.DataGridViewCheckBoxColumn.ThreeState%2A?displayProperty=nameWithType> Themen zu Eigenschaften und <xref:System.Windows.Forms.DataGridViewComboBoxColumn?displayProperty=nameWithType> Klassenreferenz.  
  
## <a name="replacing-bound-mode"></a>Ersetzen des gebundenen Modus  
 Wenn der gebundene Modus nicht Ihren Leistungsanforderungen entspricht, können Sie alle Daten in einem benutzerdefinierten Cache mithilfe von Ereignis Handlern im virtuellen Modus verwalten. Beispielsweise können Sie den virtuellen Modus verwenden, um einen Just-in-Time-Mechanismus zum Laden von Daten zu implementieren, der nur so viele Daten aus einer Netzwerk Datenbank abruft, wie dies für eine optimale Leistung erforderlich ist. Dieses Szenario ist besonders nützlich, wenn Sie mit großen Datenmengen über eine langsame Netzwerkverbindung oder mit Client Computern arbeiten, die nur über eine begrenzte Menge an RAM oder Speicherplatz verfügen.  
  
 Weitere Informationen zum Verwenden des virtuellen Modus in einem Just-in-Time-Szenario finden Sie unter [Implementieren des virtuellen Modus mit Just-in-Time-Laden von Daten in das Windows Forms DataGridView-Steuer](implementing-virtual-mode-jit-data-loading-in-the-datagrid.md)Element.  
  
## <a name="virtual-mode-events"></a>Ereignisse Virtual-Mode  
 Wenn Ihre Daten schreibgeschützt sind, kann das `CellValueNeeded` Ereignis das einzige Ereignis sein, das Sie behandeln müssen. Zusätzliche Ereignisse im virtuellen Modus ermöglichen es Ihnen, bestimmte Funktionen wie Benutzer bearbeitvorgänge, Zeilen Addition und-Löschung sowie Transaktionen auf Zeilenebene zu aktivieren.  
  
 Einige Standard <xref:System.Windows.Forms.DataGridView> Ereignisse (z. b. Ereignisse, die auftreten, wenn Benutzer Zeilen hinzufügen oder löschen oder Zellen Werte bearbeitet, analysiert, validiert oder formatiert werden) sind ebenfalls im virtuellen Modus nützlich. Sie können auch Ereignisse behandeln, mit denen Sie Werte verwalten können, die in der Regel nicht in einer gebundenen Datenquelle gespeichert sind, wie z. b. Zellen-QuickInfo-Text, Zellen-und Zeilen Fehlertext, Zellen-und Zeilen Kontextmenü Daten und Zeilen Höhendaten  
  
 Weitere Informationen zum Implementieren des virtuellen Modus zum Verwalten von Daten mit Lese-/Schreibzugriff mit einem commitbereich auf Zeilenebene finden Sie unter Exemplarische [Vorgehensweise: Implementieren des virtuellen Modus im Windows Forms DataGridView-Steuer](implementing-virtual-mode-wf-datagridview-control.md)Element.  
  
 Ein Beispiel, das den virtuellen Modus mit einem commitbereich auf Zellen Ebene implementiert, finden Sie im Thema zu den <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> Eigenschaften verweisen.  
  
 Die folgenden Ereignisse treten nur auf, wenn die- <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> Eigenschaft auf festgelegt ist `true` .  
  
|Ereignis|BESCHREIBUNG|  
|-----------|-----------------|  
|<xref:System.Windows.Forms.DataGridView.CellValueNeeded>|Wird vom-Steuerelement verwendet, um einen Zellwert aus dem Daten Cache für die Anzeige abzurufen. Dieses Ereignis tritt nur bei Zellen in ungebundenen Spalten auf.|  
|<xref:System.Windows.Forms.DataGridView.CellValuePushed>|Wird vom-Steuerelement verwendet, um Benutzereingaben für eine Zelle in den Daten Cache zu übertragen. Dieses Ereignis tritt nur bei Zellen in ungebundenen Spalten auf.<br /><br /> Ruft die- <xref:System.Windows.Forms.DataGridView.UpdateCellValue%2A> Methode auf, wenn ein zwischen gespeicherter Wert außerhalb eines- <xref:System.Windows.Forms.DataGridView.CellValuePushed> Ereignis Handlers geändert wird, um sicherzustellen, dass der aktuelle Wert im Steuerelement angezeigt wird und alle automatischen Größen Anpassungs Modi angewendet werden.|  
|<xref:System.Windows.Forms.DataGridView.NewRowNeeded>|Wird vom-Steuerelement verwendet, um die Notwendigkeit einer neuen Zeile im Daten Cache anzugeben.|  
|<xref:System.Windows.Forms.DataGridView.RowDirtyStateNeeded>|Wird vom-Steuerelement verwendet, um zu bestimmen, ob für eine Zeile Änderungen ohne Commit ausgeführt wurden.|  
|<xref:System.Windows.Forms.DataGridView.CancelRowEdit>|Wird vom-Steuerelement verwendet, um anzugeben, dass eine Zeile auf die zwischengespeicherten Werte zurückgesetzt werden soll.|  
  
 Die folgenden Ereignisse sind im virtuellen Modus nützlich, können aber unabhängig von der- <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> Eigenschafts Einstellung verwendet werden.  
  
|Events|BESCHREIBUNG|  
|------------|-----------------|  
|<xref:System.Windows.Forms.DataGridView.UserDeletingRow><br /><br /> <xref:System.Windows.Forms.DataGridView.UserDeletedRow><br /><br /> <xref:System.Windows.Forms.DataGridView.RowsRemoved><br /><br /> <xref:System.Windows.Forms.DataGridView.RowsAdded>|Wird vom-Steuerelement verwendet, um anzugeben, wann Zeilen gelöscht oder hinzugefügt werden, sodass Sie den Daten Cache entsprechend aktualisieren können.|  
|<xref:System.Windows.Forms.DataGridView.CellFormatting><br /><br /> <xref:System.Windows.Forms.DataGridView.CellParsing><br /><br /> <xref:System.Windows.Forms.DataGridView.CellValidating><br /><br /> <xref:System.Windows.Forms.DataGridView.CellValidated><br /><br /> <xref:System.Windows.Forms.DataGridView.RowValidating><br /><br /> <xref:System.Windows.Forms.DataGridView.RowValidated>|Wird vom-Steuerelement zum Formatieren von Zellwerten für die Anzeige und zum Analysieren und Validieren von Benutzereingaben verwendet.|  
|<xref:System.Windows.Forms.DataGridView.CellToolTipTextNeeded>|Wird vom-Steuerelement verwendet, um den Text der QuickInfo beim Festlegen der- <xref:System.Windows.Forms.DataGridView.DataSource%2A> Eigenschaft oder der- <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> Eigenschaft abzurufen `true` .<br /><br /> Cell Quick Tips werden nur angezeigt, wenn der- <xref:System.Windows.Forms.DataGridView.ShowCellToolTips%2A> Eigenschafts Wert ist `true` .|  
|<xref:System.Windows.Forms.DataGridView.CellErrorTextNeeded><br /><br /> <xref:System.Windows.Forms.DataGridView.RowErrorTextNeeded>|Wird vom-Steuerelement verwendet, um den Fehlertext von Zellen oder Zeilen abzurufen, wenn die- <xref:System.Windows.Forms.DataGridView.DataSource%2A> Eigenschaft festgelegt wird oder die- <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> Eigenschaft ist `true`<br /><br /> Ruft die- <xref:System.Windows.Forms.DataGridView.UpdateCellErrorText%2A> Methode oder die- <xref:System.Windows.Forms.DataGridView.UpdateRowErrorText%2A> Methode auf, wenn Sie den Fehlertext der Zelle oder Zeile ändern, um sicherzustellen, dass der aktuelle Wert im Steuerelement angezeigt wird.<br /><br /> Zeilen-und Zeilen Fehler Symbole werden angezeigt, wenn die <xref:System.Windows.Forms.DataGridView.ShowCellErrors%2A> -und- <xref:System.Windows.Forms.DataGridView.ShowRowErrors%2A> Eigenschaftswerte sind `true` .|  
|<xref:System.Windows.Forms.DataGridView.CellContextMenuStripNeeded><br /><br /> <xref:System.Windows.Forms.DataGridView.RowContextMenuStripNeeded>|Wird vom-Steuerelement zum Abrufen einer Zelle oder Zeile verwendet, <xref:System.Windows.Forms.ContextMenuStrip> Wenn die Steuerelement <xref:System.Windows.Forms.DataGridView.DataSource%2A> Eigenschaft festgelegt ist oder die- <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> Eigenschaft ist `true` .|  
|<xref:System.Windows.Forms.DataGridView.RowHeightInfoNeeded><br /><br /> <xref:System.Windows.Forms.DataGridView.RowHeightInfoPushed>|Wird vom-Steuerelement verwendet, um Informationen zur Zeilenhöhe im Daten Cache abzurufen oder zu speichern. Ruft die- <xref:System.Windows.Forms.DataGridView.UpdateRowHeightInfo%2A> Methode auf, wenn die zwischengespeicherten Zeilen Höheninformationen außerhalb eines- <xref:System.Windows.Forms.DataGridView.RowHeightInfoPushed> Ereignis Handlers geändert werden, um sicherzustellen, dass der aktuelle Wert in der Anzeige des Steuer Elements verwendet wird.|  
  
## <a name="best-practices-in-virtual-mode"></a>Bewährte Methoden im virtuellen Modus  
 Wenn Sie den virtuellen Modus implementieren, um effizient mit großen Datenmengen arbeiten zu können, sollten Sie auch sicherstellen, dass Sie effizient mit dem Steuerelement <xref:System.Windows.Forms.DataGridView> selbst arbeiten. Weitere Informationen zur effizienten Verwendung von Zellen Stilen, der automatischen Größenanpassung, der Auswahl und der Zeilen Freigabe finden Sie unter [bewährte Methoden zum Skalieren des Windows Forms DataGridView-Steuer](best-practices-for-scaling-the-windows-forms-datagridview-control.md)Elements.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.VirtualMode%2A>
- [Leistungsoptimierung im DataGridView-Steuerelement in Windows Forms](performance-tuning-in-the-windows-forms-datagridview-control.md)
- [Empfohlene Vorgehensweisen für das Skalieren des DataGridView-Steuerelements in Windows Forms](best-practices-for-scaling-the-windows-forms-datagridview-control.md)
- [Exemplarische Vorgehensweise: Implementieren des virtuellen Modus im DataGridView-Steuerelement in Windows Forms](implementing-virtual-mode-wf-datagridview-control.md)
- [Implementieren des virtuellen Modus mit Just-In-Time-Laden von Daten in das DataGridView-Steuerelement in Windows Forms](implementing-virtual-mode-jit-data-loading-in-the-datagrid.md)
