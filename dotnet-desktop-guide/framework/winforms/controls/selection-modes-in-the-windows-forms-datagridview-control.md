---
title: Auswahl Modi im DataGridView-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- selection [Windows Forms], modes in DataGridView control
- DataGridView control [Windows Forms], selection mode
ms.assetid: a3ebfd3d-0525-479d-9d96-d9e017289b36
ms.openlocfilehash: e20bf6307d77bf189b698e847c6b855c249dc3c1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975975"
---
# <a name="selection-modes-in-the-windows-forms-datagridview-control"></a>Auswahlmodi im DataGridView-Steuerelement von Windows Forms

Manchmal möchten Sie, dass Ihre Anwendung Aktionen auf der Grundlage der Benutzer Auswahl in einem Steuerelement ausführt <xref:System.Windows.Forms.DataGridView> . Abhängig von den Aktionen können Sie die möglichen Auswahlmöglichkeiten einschränken. Nehmen Sie beispielsweise an, dass Ihre Anwendung einen Bericht für den aktuell ausgewählten Datensatz drucken kann. In diesem Fall empfiehlt es sich, das Steuerelement so zu konfigurieren, <xref:System.Windows.Forms.DataGridView> dass bei jedem Klicken auf eine beliebige Stelle in einer Zeile immer die gesamte Zeile ausgewählt wird, sodass jeweils nur eine Zeile ausgewählt werden kann.

Sie können die zulässige Auswahl angeben, indem Sie die- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A?displayProperty=nameWithType> Eigenschaft auf einen der folgenden <xref:System.Windows.Forms.DataGridViewSelectionMode> Enumerationswerte festlegen.

|DataGridViewSelectionMode-Wert|BESCHREIBUNG|
|-------------------------------------|-----------------|
|<xref:System.Windows.Forms.DataGridViewSelectionMode.CellSelect>|Durch Klicken auf eine Zelle wird Sie ausgewählt. Zeilen-und Spaltenheader können nicht zur Auswahl verwendet werden.|
|<xref:System.Windows.Forms.DataGridViewSelectionMode.ColumnHeaderSelect>|Durch Klicken auf eine Zelle wird Sie ausgewählt. Wenn Sie auf einen Spaltenheader klicken, wird die gesamte Spalte ausgewählt. Spaltenheader können nicht für die Sortierung verwendet werden.|
|<xref:System.Windows.Forms.DataGridViewSelectionMode.FullColumnSelect>|Wenn Sie auf eine Zelle oder einen Spaltenheader klicken, wird die gesamte Spalte ausgewählt. Spaltenheader können nicht für die Sortierung verwendet werden.|
|<xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect>|Durch Klicken auf eine Zelle oder einen Zeilen Header wird die gesamte Zeile ausgewählt.|
|<xref:System.Windows.Forms.DataGridViewSelectionMode.RowHeaderSelect>|Standardauswahl Modus. Durch Klicken auf eine Zelle wird Sie ausgewählt. Durch Klicken auf einen Zeilen Header wird die gesamte Zeile ausgewählt.|

> [!NOTE]
> Wenn Sie den Auswahlmodus zur Laufzeit ändern, wird die aktuelle Auswahl automatisch gelöscht.

Standardmäßig können Benutzer mehrere Zeilen, Spalten oder Zellen auswählen, indem Sie Sie mit der Maus ziehen, die STRG-Taste oder die UMSCHALTTASTE gedrückt halten, um eine Auswahl zu erweitern oder zu ändern, oder indem Sie auf die obere linke Header Zelle klicken, um alle Zellen im Steuerelement auszuwählen. Um dieses Verhalten zu verhindern, legen <xref:System.Windows.Forms.DataGridView.MultiSelect%2A> Sie die-Eigenschaft auf fest `false` .

<xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect>Mit den <xref:System.Windows.Forms.DataGridViewSelectionMode.RowHeaderSelect> Modi und können Benutzer Zeilen löschen, indem Sie Sie auswählen und die ENTF-Taste drücken. Benutzer können Zeilen nur löschen, wenn sich die aktuelle Zelle nicht im Bearbeitungsmodus befindet, die <xref:System.Windows.Forms.DataGridView.AllowUserToDeleteRows%2A> -Eigenschaft auf festgelegt ist `true` und die zugrunde liegende Datenquelle das Löschen von Zeilen unterstützt. Beachten Sie, dass diese Einstellungen das programmgesteuerte Löschen von Zeilen nicht verhindern.

## <a name="programmatic-selection"></a>Programmgesteuerte Auswahl

Der aktuelle Auswahlmodus schränkt das Verhalten der programmgesteuerten Auswahl und der Benutzer Auswahl ein. Sie können die aktuelle Auswahlprogramm gesteuert ändern, indem Sie die- `Selected` Eigenschaft von Zellen, Zeilen oder Spalten festlegen, die im-Steuerelement vorhanden sind <xref:System.Windows.Forms.DataGridView> . Sie können auch alle Zellen im-Steuerelement über die- <xref:System.Windows.Forms.DataGridView.SelectAll%2A> Methode auswählen, abhängig vom Auswahlmodus. Verwenden Sie die-Methode, um die Auswahl zu löschen <xref:System.Windows.Forms.DataGridView.ClearSelection%2A> .

Wenn die- <xref:System.Windows.Forms.DataGridView.MultiSelect%2A> Eigenschaft auf festgelegt ist `true` , können Sie Elemente hinzufügen <xref:System.Windows.Forms.DataGridView> oder aus der Auswahl entfernen, indem Sie die- `Selected` Eigenschaft des-Elements ändern. Andernfalls werden durch das Festlegen der- `Selected` Eigenschaft auf `true` für ein Element automatisch weitere Elemente aus der Auswahl entfernt.

Beachten Sie, dass das Ändern des Werts der- <xref:System.Windows.Forms.DataGridView.CurrentCell%2A> Eigenschaft die aktuelle Auswahl nicht ändert.

Sie können eine Auflistung der aktuell ausgewählten Zellen, Zeilen oder Spalten über die <xref:System.Windows.Forms.DataGridView.SelectedCells%2A> <xref:System.Windows.Forms.DataGridView.SelectedRows%2A> Eigenschaften, und <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A> des-Steuer <xref:System.Windows.Forms.DataGridView> Elements abrufen. Der Zugriff auf diese Eigenschaften ist ineffizient, wenn jede Zelle im Steuerelement ausgewählt wird. Um in diesem Fall eine Leistungs Einbuße zu vermeiden, verwenden Sie zuerst die- <xref:System.Windows.Forms.DataGridView.AreAllCellsSelected%2A> Methode. Außerdem kann der Zugriff auf diese Auflistungen zum Ermitteln der Anzahl ausgewählter Zellen, Zeilen oder Spalten ineffizient sein. Verwenden Sie stattdessen die <xref:System.Windows.Forms.DataGridView.GetCellCount%2A> <xref:System.Windows.Forms.DataGridViewRowCollection.GetRowCount%2A> Methode, oder <xref:System.Windows.Forms.DataGridViewColumnCollection.GetColumnCount%2A> , und übergeben Sie den <xref:System.Windows.Forms.DataGridViewElementStates.Selected> Wert.

> [!TIP]
> Beispielcode, der die programmgesteuerte Verwendung ausgewählter Zellen veranschaulicht, finden Sie in der <xref:System.Windows.Forms.DataGridView> Übersicht über die-Klasse.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.MultiSelect%2A>
- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A>
- <xref:System.Windows.Forms.DataGridViewSelectionMode>
- [Verwendung von Auswahl und Zwischenablage mit dem DataGridView-Steuerelement in Windows Forms](selection-and-clipboard-use-with-the-windows-forms-datagridview-control.md)
- [Vorgehensweise: Festlegen des Auswahlmodus des DataGridView-Steuerelements in Windows Forms](how-to-set-the-selection-mode-of-the-windows-forms-datagridview-control.md)
