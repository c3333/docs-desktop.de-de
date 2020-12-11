---
title: Standardverhalten von Tastatur und Maus im DataGrid-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- DataGrid [WPF], keyboard behavior
- DataGrid [WPF], mouse behavior
- keyboard behavior [WPF], DataGrid
- mouse behavior [WPF], DataGrid
ms.assetid: 563b8854-ca39-4d97-8235-17eaa0f93c8d
ms.openlocfilehash: a518c6123b21ae62742071a0b26c6a09fa272b17
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975412"
---
# <a name="default-keyboard-and-mouse-behavior-in-the-datagrid-control"></a>Standardverhalten von Tastatur und Maus im DataGrid-Steuerelement
In diesem Thema wird beschrieben, wie Benutzer mit dem <xref:System.Windows.Controls.DataGrid> -Steuerelement über die Tastatur und die Maus interagieren können.  
  
 Typische Interaktionen mit <xref:System.Windows.Controls.DataGrid> umfassen Navigation, Auswahl und Bearbeitung. Das Auswahl Verhalten wird von der <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> -Eigenschaft und der-Eigenschaft beeinflusst <xref:System.Windows.Controls.DataGrid.SelectionUnit%2A> . Die Standardwerte, die das in diesem Thema beschriebene Verhalten verursachen, sind <xref:System.Windows.Controls.DataGridSelectionMode.Extended?displayProperty=nameWithType> und <xref:System.Windows.Controls.DataGridSelectionUnit.FullRow?displayProperty=nameWithType> . Eine Änderung dieser Werte kann zu einem Verhalten führen, das sich von dem beschriebenen Verhalten unterscheidet. Wenn eine Zelle sich im Bearbeitungsmodus befindet, kann das Bearbeitungs Steuerelement das Standardtastatur Verhalten von überschreiben <xref:System.Windows.Controls.DataGrid> .  
  
## <a name="default-keyboard-behavior"></a>Standardmäßiges Tastatur Verhalten  
 In der folgenden Tabelle ist das Standardtastatur Verhalten für das aufgeführt <xref:System.Windows.Controls.DataGrid> .  
  
|Schlüssel-oder Schlüssel Kombination|BESCHREIBUNG|  
|----------------------------|-----------------|  
|NACH-UNTEN-TASTE|Verschiebt den Fokus direkt unterhalb der aktuellen Zelle in die Zelle. Wenn sich der Fokus in der letzten Zeile befindet, bewirkt das Drücken der nach-unten-Taste nichts.|  
|NACH-OBEN-TASTE|Verschiebt den Fokus direkt oberhalb der aktuellen Zelle in die Zelle. Wenn sich der Fokus in der ersten Zeile befindet, bewirkt das Drücken der nach-oben-Taste nichts.|  
|NACH-LINKS-TASTE|Verschiebt den Fokus auf die vorherige Zelle in der Zeile. Wenn sich der Fokus in der ersten Zelle in der Zeile befindet, bewirkt das Drücken der nach-links-Taste nichts.|  
|NACH-RECHTS-TASTE|Verschiebt den Fokus auf die nächste Zelle in der Zeile. Wenn sich der Fokus in der letzten Zelle in der Zeile befindet, bewirkt das Drücken der nach-rechts-Taste nichts.|  
|POS1|Verschiebt den Fokus auf die erste Zelle in der aktuellen Zeile.|  
|ENDE|Verschiebt den Fokus auf die letzte Zelle in der aktuellen Zeile.|  
|BILD-AB|Wenn die Zeilen nicht gruppiert sind, wird das Steuerelement durch die Anzahl der Zeilen, die vollständig angezeigt werden, nach unten verschoben. Verschiebt den Fokus auf die letzte vollständig angezeigte Zeile, ohne die Spalten zu ändern.<br /><br /> Wenn Zeilen gruppiert sind, verschiebt den Fokus in die letzte Zeile in, <xref:System.Windows.Controls.DataGrid> ohne dass Spalten geändert werden.|  
|BILD-AUF|Wenn die Zeilen nicht gruppiert sind, wird das Steuerelement durch die Anzahl der Zeilen, die vollständig angezeigt werden, nach oben verschoben. Verschiebt den Fokus auf die erste angezeigte Zeile, ohne die Spalten zu ändern.<br /><br /> Wenn Zeilen gruppiert sind, verschiebt den Fokus auf die erste Zeile in, <xref:System.Windows.Controls.DataGrid> ohne dass Spalten geändert werden.|  
|TAB|Verschiebt den Fokus auf die nächste Zelle in der aktuellen Zeile. Wenn sich der Fokus in der letzten Zelle der Zeile befindet, verschiebt den Fokus auf die erste Zelle in der nächsten Zeile. Wenn sich der Fokus in der letzten Zelle im-Steuerelement befindet, verschiebt den Fokus auf das nächste Steuerelement in der Aktivier Reihenfolge des übergeordneten Containers.<br /><br /> Wenn sich die aktive Zelle im Bearbeitungsmodus befindet und durch Drücken der Tab-Taste der Fokus von der aktuellen Zeile entfernt wird, wird für alle an der Zeile vorgenommenen Änderungen ein Commit ausgeführt, bevor der Fokus geändert wird.|  
|UMSCHALT+TAB|Verschiebt den Fokus auf die vorherige Zelle in der aktuellen Zeile. Wenn sich der Fokus bereits in der ersten Zelle der Zeile befindet, verschiebt den Fokus auf die letzte Zelle in der vorherigen Zeile. Wenn sich der Fokus in der ersten Zelle im-Steuerelement befindet, verschiebt den Fokus auf das vorherige Steuerelement in der Aktivier Reihenfolge des übergeordneten Containers.<br /><br /> Wenn sich die aktive Zelle im Bearbeitungsmodus befindet und durch Drücken der Tab-Taste der Fokus von der aktuellen Zeile entfernt wird, wird für alle an der Zeile vorgenommenen Änderungen ein Commit ausgeführt, bevor der Fokus geändert wird.|  
|STRG+NACH-UNTEN-TASTE|Verschiebt den Fokus auf die letzte Zelle in der aktuellen Spalte.|  
|STRG+NACH-OBEN-TASTE|Verschiebt den Fokus auf die erste Zelle in der aktuellen Spalte.|  
|STRG+NACH-RECHTS|Verschiebt den Fokus auf die letzte Zelle in der aktuellen Zeile.|  
|STRG+NACH-LINKS|Verschiebt den Fokus auf die erste Zelle in der aktuellen Zeile.|  
|STRG+POS1|Verschiebt den Fokus auf die erste Zelle im-Steuerelement.|  
|STRG+ENDE|Verschiebt den Fokus auf die letzte Zelle im-Steuerelement.|  
|STRG+BILD-AB|Identisch mit der Seite nach unten.|  
|STRG+BILD-AUF|Identisch mit der Seitenansicht.|  
|F2|Wenn die <xref:System.Windows.Controls.DataGrid.IsReadOnly%2A?displayProperty=nameWithType> -Eigenschaft `false` und die- <xref:System.Windows.Controls.DataGridColumn.IsReadOnly%2A?displayProperty=nameWithType> Eigenschaft `false` für die aktuelle Spalte ist, wird die aktuelle Zelle in den Zellen Bearbeitungsmodus versetzt.|  
|EINGABETASTE|Führt einen Commit für alle Änderungen an der aktuellen Zelle und Zeile aus und verschiebt den Fokus direkt unterhalb der aktuellen Zelle in die Zelle. Wenn sich der Fokus in der letzten Zeile befindet, führt einen Commit für alle Änderungen aus, ohne den Fokus zu verschieben.|  
|ESC|Wenn sich das Steuerelement im Bearbeitungsmodus befindet, bricht die Bearbeitung ab und stellt alle Änderungen wieder her, die im Steuerelement vorgenommen wurden. Wenn die zugrunde liegende Datenquelle implementiert <xref:System.ComponentModel.IEditableObject> , wird durch Drücken von ESC ein zweites Mal der Bearbeitungsmodus für die gesamte Zeile abgebrochen.|  
|RÜCKTASTE|Löscht das Zeichen vor dem Cursor, wenn eine Zelle bearbeitet wird.|  
|Delete|Löscht das Zeichen nach dem Cursor, wenn eine Zelle bearbeitet wird.|  
|STRG+EINGABE|Führt einen Commit für alle Änderungen an der aktuellen Zelle aus, ohne den Fokus zu verschieben.|  
|STRG+A|Wenn <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> auf festgelegt ist <xref:System.Windows.Controls.DataGridSelectionMode.Extended> , wählt alle Zeilen in aus <xref:System.Windows.Controls.DataGrid> .|  
  
## <a name="selection-keys"></a>Auswahl Schlüssel  
 Wenn die- <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> Eigenschaft auf festgelegt ist <xref:System.Windows.Controls.DataGridSelectionMode.Extended> , ändert sich das Navigationsverhalten nicht, aber die Navigation mit der Tastatur beim Drücken der Umschalttaste (einschließlich STRG + UMSCHALT) ändert eine mehrzeilige Auswahl. Vor dem Start der Navigation markiert das Steuerelement die aktuelle Zeile als Anker Zeile. Wenn Sie beim Drücken der UMSCHALTTASTE navigieren, umfasst die Auswahl alle Zeilen zwischen der Anker Zeile und der aktuellen Zeile.  
  
 Mit den folgenden Auswahl Schlüsseln wird die Auswahl von mehreren Zeilen geändert.  
  
- UMSCHALT+NACH-UNTEN-TASTE  
  
- UMSCHALT+NACH-OBEN-TASTE  
  
- UMSCHALT+BILD-AB  
  
- UMSCHALT+BILD-AUF  
  
- STRG+UMSCHALT+NACH-UNTEN  
  
- STRG+UMSCHALT+NACH-OBEN  
  
- STRG+UMSCHALT+POS1  
  
- STRG+UMSCHALT+ENDE  
  
## <a name="default-mouse-behavior"></a>Standardmäßiges Maus Verhalten  
 In der folgenden Tabelle ist das Standard-Maus Verhalten für das aufgeführt <xref:System.Windows.Controls.DataGrid> .  
  
|Mausaktion|BESCHREIBUNG|  
|------------------|-----------------|  
|Klicken Sie auf eine nicht ausgewählte Zeile.|Bewirkt, dass die angeklickte Zeile die aktuelle Zeile und die angeklickte Zelle die aktuelle Zelle ist.|  
|Klicken Sie auf die aktuelle Zelle.|Versetzt die aktuelle Zelle in den Bearbeitungsmodus.|  
|Ziehen einer Spaltenheader Zelle|Wenn die <xref:System.Windows.Controls.DataGrid.CanUserReorderColumns%2A?displayProperty=nameWithType> -Eigenschaft `true` und die- <xref:System.Windows.Controls.DataGridColumn.CanUserReorder%2A?displayProperty=nameWithType> Eigenschaft `true` für die aktuelle Spalte ist, verschiebt die-Spalte so, dass Sie an einer neuen Position abgelegt werden kann.|  
|Spaltenheader Trennzeichen ziehen|Wenn die <xref:System.Windows.Controls.DataGrid.CanUserResizeColumns%2A?displayProperty=nameWithType> -Eigenschaft `true` und die- <xref:System.Windows.Controls.DataGridColumn.CanUserResize%2A?displayProperty=nameWithType> Eigenschaft `true` für die aktuelle Spalte ist, wird die Größe der Spalte geändert.|  
|Doppelklicken Sie auf ein Spaltenheader Trennzeichen.|Wenn die <xref:System.Windows.Controls.DataGrid.CanUserResizeColumns%2A?displayProperty=nameWithType> -Eigenschaft `true` und die- <xref:System.Windows.Controls.DataGridColumn.CanUserResize%2A?displayProperty=nameWithType> Eigenschaft `true` für die aktuelle Spalte ist, wird die Spalte mit dem Größen Anpassungs <xref:System.Windows.Controls.DataGridLength.Auto%2A> Modus automatisch skalieren.|  
|Klicken Sie auf eine Spaltenheader Zelle.|Wenn die <xref:System.Windows.Controls.DataGrid.CanUserSortColumns%2A?displayProperty=nameWithType> -Eigenschaft `true` und die- <xref:System.Windows.Controls.DataGridColumn.CanUserSort%2A?displayProperty=nameWithType> Eigenschaft `true` für die aktuelle Spalte ist, wird die-Spalte sortiert.<br /><br /> Wenn Sie auf den Header einer bereits sortierten Spalte klicken, wird die Sortierreihenfolge dieser Spalte umgekehrt.<br /><br /> Wenn Sie die UMSCHALTTASTE drücken, während Sie auf mehrere Spaltenüberschriften klicken, werden Sie nach mehreren Spalten in der angegebenen Reihenfolge sortiert|  
|Strg + Klick auf eine Zeile|Wenn <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> auf festgelegt ist <xref:System.Windows.Controls.DataGridSelectionMode.Extended> , ändert eine nicht zusammenhängende Auswahl aus mehreren Zeilen.<br /><br /> Wenn die Zeile bereits ausgewählt ist, wird die Zeile deaktiviert.|  
|UMSCHALT + Klicken auf eine Zeile|Wenn <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> auf festgelegt ist <xref:System.Windows.Controls.DataGridSelectionMode.Extended> , wird eine zusammenhängende Auswahl von mehreren Zeilen geändert.|  
|Klicken Sie auf einen Zeilen Gruppen Header.|Erweitert oder reduziert die Gruppe.|  
|Klicken Sie in der oberen linken Ecke der auf die Schaltfläche Alle auswählen. <xref:System.Windows.Controls.DataGrid>|Wenn <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> auf festgelegt ist <xref:System.Windows.Controls.DataGridSelectionMode.Extended> , wählt alle Zeilen in aus <xref:System.Windows.Controls.DataGrid> .|  
  
## <a name="mouse-selection"></a>Maus Auswahl  
 Wenn die- <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> Eigenschaft auf festgelegt ist <xref:System.Windows.Controls.DataGridSelectionMode.Extended> , wird durch Klicken auf eine Zeile beim Drücken von STRG oder UMSCHALT eine mehrzeilige Auswahl geändert.  
  
 Wenn Sie beim Drücken der STRG-Taste auf eine Zeile klicken, wird der Auswahl Zustand der Zeile geändert, während alle anderen Zeilen Ihren aktuellen Auswahl Zustand beibehalten. Wählen Sie diese Option aus, um nicht angrenzende Zeilen auszuwählen.  
  
 Wenn Sie beim Drücken der UMSCHALTTASTE auf eine Zeile klicken, umfasst die Auswahl alle Zeilen zwischen der aktuellen Zeile und eine Anker Zeile, die sich an der Position der aktuellen Zeile vor dem Klick befindet. Nachfolgende Klicks beim Drücken der Umschalttaste ändern die aktuelle Zeile, jedoch nicht die Anker Zeile. Wählen Sie diese Option aus, um einen Bereich von angrenzenden Zeilen auszuwählen.  
  
 STRG + UMSCHALT kann kombiniert werden, um nicht angrenzende Bereiche von angrenzenden Zeilen auszuwählen. Wählen Sie hierzu den ersten Bereich mithilfe von Umschalt + Klick aus, wie zuvor beschrieben. Nachdem der erste Bereich von Zeilen ausgewählt ist, wählen Sie mit STRG + Klicken die erste Zeile im nächsten Bereich aus, und klicken Sie dann auf die letzte Zeile im nächsten Bereich, während Sie STRG + UMSCHALT drücken.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.DataGrid>
- <xref:System.Windows.Controls.DataGrid.SelectionMode%2A>
