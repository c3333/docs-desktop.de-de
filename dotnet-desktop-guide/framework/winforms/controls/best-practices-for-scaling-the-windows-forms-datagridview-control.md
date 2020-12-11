---
title: Bewährte Methoden für das Skalieren des DataGridView-Steuer Elements
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], row sharing
- data grids [Windows Forms], best practices
- DataGridView control [Windows Forms], shared rows
- DataGridView control [Windows Forms], best practices
- best practices [Windows Forms], dataGridView control
- DataGridView control [Windows Forms], scaling
ms.assetid: 8321a8a6-6340-4fd1-b475-fa090b905aaf
ms.openlocfilehash: 63500a79def89510b4bc7a436abc4620a7265a79
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976028"
---
# <a name="best-practices-for-scaling-the-windows-forms-datagridview-control"></a>Empfohlene Vorgehensweisen für das Skalieren des DataGridView-Steuerelements in Windows Forms

Das- <xref:System.Windows.Forms.DataGridView> Steuerelement wurde entwickelt, um maximale Skalierbarkeit zu gewährleisten. Wenn Sie große Datenmengen anzeigen möchten, sollten Sie die in diesem Thema beschriebenen Richtlinien befolgen, um zu vermeiden, dass große Mengen an Arbeitsspeicher beansprucht werden oder die Reaktionsfähigkeit der Benutzeroberfläche (UI) beeinträchtigt wird. In diesem Thema werden die folgenden Punkte erläutert:

- Effizientes Verwenden von Zellstilen

- Effizientes Verwenden von Kontextmenüs

- Effizientes Verwenden der automatischen Größe der Größe

- Effizientes Verwenden der ausgewählten Zellen, Zeilen und Spalten Sammlungen

- Verwenden von freigegebenen Zeilen

- Verhindern, dass Zeilen freigegeben werden

Wenn Sie besondere Leistungsanforderungen haben, können Sie den virtuellen Modus implementieren und eigene Daten Verwaltungsvorgänge bereitstellen. Weitere Informationen finden Sie unter [Datenanzeige Modi im Windows Forms DataGridView-Steuer](data-display-modes-in-the-windows-forms-datagridview-control.md)Element.

## <a name="using-cell-styles-efficiently"></a>Effizientes Verwenden von Zellstilen

Jede Zelle, jede Zeile und jede Spalte kann eigene Stil Informationen aufweisen. Stil Informationen werden in- <xref:System.Windows.Forms.DataGridViewCellStyle> Objekten gespeichert. Das Erstellen von Zellen Stil Objekten für viele einzelne <xref:System.Windows.Forms.DataGridView> Elemente kann ineffizient sein, insbesondere bei der Arbeit mit großen Datenmengen. Verwenden Sie die folgenden Richtlinien, um eine Beeinträchtigung der Leistung zu vermeiden:

- Legen Sie keine Zellen Stileigenschaften für einzelne- <xref:System.Windows.Forms.DataGridViewCell> oder- <xref:System.Windows.Forms.DataGridViewRow> Objekte fest. Dies schließt das Zeilen Objekt ein, das von der-Eigenschaft angegeben wird <xref:System.Windows.Forms.DataGridView.RowTemplate%2A> . Jede neue Zeile, die aus der Zeilen Vorlage geklont wird, erhält eine eigene Kopie des Zellen Stil Objekts der Vorlage. Legen Sie für maximale Skalierbarkeit Zellen Stileigenschaften auf der <xref:System.Windows.Forms.DataGridView> Ebene fest. Legen Sie beispielsweise die- <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType> Eigenschaft anstelle der- <xref:System.Windows.Forms.DataGridViewCell.Style%2A?displayProperty=nameWithType> Eigenschaft fest.

- Wenn für einige Zellen eine andere Formatierung als die Standard Formatierung erforderlich ist, verwenden Sie die gleiche <xref:System.Windows.Forms.DataGridViewCellStyle> Instanz in Gruppen von Zellen, Zeilen oder Spalten. Legen Sie die Eigenschaften des Typs nicht <xref:System.Windows.Forms.DataGridViewCellStyle> für einzelne Zellen, Zeilen und Spalten direkt fest. Ein Beispiel für die Freigabe von Zellen Formaten finden [Sie unter Gewusst wie: Festlegen von Standardzellen Stilen für das Windows Forms DataGridView-Steuer](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md)Element. Sie können auch eine Leistungs Einbuße vermeiden, wenn Sie Zellen Stile einzeln festlegen, indem Sie den- <xref:System.Windows.Forms.DataGridView.CellFormatting> Ereignishandler verarbeiten. Ein Beispiel finden Sie unter Gewusst [wie: Anpassen der Datenformatierung im Windows Forms DataGridView-Steuer](how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md)Element.

- Wenn Sie den Stil einer Zelle ermitteln, verwenden Sie die- <xref:System.Windows.Forms.DataGridViewCell.InheritedStyle%2A?displayProperty=nameWithType> Eigenschaft anstelle der- <xref:System.Windows.Forms.DataGridViewCell.Style%2A?displayProperty=nameWithType> Eigenschaft. Durch den Zugriff auf die- <xref:System.Windows.Forms.DataGridViewCell.Style%2A> Eigenschaft wird eine neue Instanz der-Klasse erstellt, <xref:System.Windows.Forms.DataGridViewCellStyle> Wenn die-Eigenschaft nicht bereits verwendet wurde. Darüber hinaus enthält dieses Objekt möglicherweise nicht die gesamten Formatinformationen für die Zelle, wenn einige Stile von der Zeile, der Spalte oder dem Steuerelement geerbt werden. Weitere Informationen zur Vererbung von Zellen Formaten finden Sie unter [Zellen Stile im Windows Forms DataGridView-Steuer](cell-styles-in-the-windows-forms-datagridview-control.md)Element.

## <a name="using-shortcut-menus-efficiently"></a>Effizientes Verwenden von Kontextmenüs

Jede Zelle, Zeile und Spalte kann über ein eigenes Kontextmenü verfügen. Kontextmenüs im- <xref:System.Windows.Forms.DataGridView> Steuerelement werden durch Steuer <xref:System.Windows.Forms.ContextMenuStrip> Elemente dargestellt. Ebenso wie bei Zellen Stil Objekten wirkt sich das Erstellen von Kontextmenüs für viele einzelne <xref:System.Windows.Forms.DataGridView> Elemente negativ auf die Leistung aus. Um dieses Problem zu vermeiden, verwenden Sie die folgenden Richtlinien:

- Vermeiden Sie das Erstellen von Kontextmenüs für einzelne Zellen und Zeilen. Dies schließt die Zeilen Vorlage ein, die zusammen mit dem Kontextmenü geklont wird, wenn dem Steuerelement neue Zeilen hinzugefügt werden. Verwenden Sie für maximale Skalierbarkeit nur die-Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> , um ein einzelnes Kontextmenü für das gesamte-Steuerelement anzugeben.

- Wenn Sie mehrere Kontextmenüs für mehrere Zeilen oder Zellen benötigen, behandeln Sie das- <xref:System.Windows.Forms.DataGridView.CellContextMenuStripNeeded> Ereignis oder das- <xref:System.Windows.Forms.DataGridView.RowContextMenuStripNeeded> Ereignis. Mit diesen Ereignissen können Sie die Kontextmenü Objekte selbst verwalten, sodass Sie die Leistung optimieren können.

## <a name="using-automatic-resizing-efficiently"></a>Effizientes Verwenden der automatischen Größe der Größe

Zeilen, Spalten und Header können automatisch in der Größe geändert werden, wenn sich der Zellen Inhalt ändert, sodass der gesamte Inhalt der Zellen ohne Clipping angezeigt wird. Durch Ändern der Größen Anpassungs Modi können auch die Größe von Zeilen, Spalten und Headern geändert werden. Um die richtige Größe zu ermitteln, <xref:System.Windows.Forms.DataGridView> muss das Steuerelement den Wert jeder Zelle untersuchen, die er aufnehmen muss. Bei der Arbeit mit großen Datasets kann sich diese Analyse negativ auf die Leistung des Steuer Elements auswirken, wenn die automatische Größe geändert wird. Verwenden Sie die folgenden Richtlinien, um Leistungseinbußen zu vermeiden:

- Vermeiden Sie die automatische Größenanpassung für ein <xref:System.Windows.Forms.DataGridView> Steuerelement mit einem großen Satz von Zeilen. Wenn Sie die automatische Größenanpassung verwenden, ändern Sie die Größe nur basierend auf den angezeigten Zeilen. Verwenden Sie nur die angezeigten Zeilen im virtuellen Modus.

  - Verwenden Sie für Zeilen und Spalten das `DisplayedCells` `DisplayedCellsExceptHeaders` -Feld oder das <xref:System.Windows.Forms.DataGridViewAutoSizeRowsMode> -Feld der <xref:System.Windows.Forms.DataGridViewAutoSizeColumnsMode> <xref:System.Windows.Forms.DataGridViewAutoSizeColumnMode> Enumerationen, und.

  - Verwenden Sie für Zeilen Header das- <xref:System.Windows.Forms.DataGridViewRowHeadersWidthSizeMode.AutoSizeToDisplayedHeaders> Feld oder das- <xref:System.Windows.Forms.DataGridViewRowHeadersWidthSizeMode.AutoSizeToFirstHeader> Feld der- <xref:System.Windows.Forms.DataGridViewRowHeadersWidthSizeMode> Enumeration.

- Deaktivieren Sie für maximale Skalierbarkeit die automatische Größenanpassung, und verwenden Sie die programmgesteuerte Größenänderung.

Weitere Informationen finden Sie unter [Größen Anpassungsoptionen im Windows Forms DataGridView-Steuer](sizing-options-in-the-windows-forms-datagridview-control.md)Element.

## <a name="using-the-selected-cells-rows-and-columns-collections-efficiently"></a>Effizientes Verwenden der ausgewählten Zellen, Zeilen und Spalten Sammlungen

Die <xref:System.Windows.Forms.DataGridView.SelectedCells%2A> Sammlung wird nicht effizient mit großer Auswahl durchgeführt. Die <xref:System.Windows.Forms.DataGridView.SelectedRows%2A> -und-Auflistungen <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A> können auch ineffizient sein, aber in geringerem Maße, da es weniger Zeilen als Zellen in einem typischen Steuerelement gibt <xref:System.Windows.Forms.DataGridView> , und viele weniger Spalten als Zeilen. Verwenden Sie die folgenden Richtlinien, um bei der Arbeit mit diesen Sammlungen Leistungseinbußen zu vermeiden:

- <xref:System.Windows.Forms.DataGridView> <xref:System.Windows.Forms.DataGridView.SelectedCells%2A> Überprüfen Sie den Rückgabewert der-Methode, um zu bestimmen, ob alle Zellen in der ausgewählt wurden, bevor Sie auf den Inhalt der Auflistung zugreifen <xref:System.Windows.Forms.DataGridView.AreAllCellsSelected%2A> . Beachten Sie jedoch, dass diese Methode dazu führen kann, dass Zeilen nicht mehr freigegeben werden. Weitere Informationen finden Sie im nächsten Abschnitt.

- Vermeiden Sie die Verwendung der- <xref:System.Collections.ICollection.Count%2A> Eigenschaft des <xref:System.Windows.Forms.DataGridViewSelectedCellCollection?displayProperty=nameWithType> , um die Anzahl der ausgewählten Zellen zu bestimmen. Verwenden Sie stattdessen die <xref:System.Windows.Forms.DataGridView.GetCellCount%2A?displayProperty=nameWithType> -Methode, und übergeben Sie den- <xref:System.Windows.Forms.DataGridViewElementStates.Selected?displayProperty=nameWithType> Wert. Verwenden <xref:System.Windows.Forms.DataGridViewRowCollection.GetRowCount%2A?displayProperty=nameWithType> Sie die-Methode und die- <xref:System.Windows.Forms.DataGridViewColumnCollection.GetColumnCount%2A?displayProperty=nameWithType> Methode, um die Anzahl der ausgewählten Elemente zu ermitteln, anstatt auf die ausgewählten Zeilen-und Spalten Auflistungen zuzugreifen.

- Vermeiden Sie Zellen basierte Auswahl Modi. Legen Sie stattdessen die- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A?displayProperty=nameWithType> Eigenschaft auf <xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect?displayProperty=nameWithType> oder fest <xref:System.Windows.Forms.DataGridViewSelectionMode.FullColumnSelect?displayProperty=nameWithType> .

## <a name="using-shared-rows"></a>Verwenden von freigegebenen Zeilen

Die effiziente Arbeitsspeicher Nutzung wird im- <xref:System.Windows.Forms.DataGridView> Steuerelement durch freigegebene Zeilen erreicht. Zeilen geben so viele Informationen über ihre Darstellung und das Verhalten wie möglich frei, indem Instanzen der-Klasse freigegeben werden <xref:System.Windows.Forms.DataGridViewRow> .

Die Freigabe von Zeilen Instanzen spart Arbeitsspeicher, Zeilen können problemlos freigegeben werden. Wenn ein Benutzer beispielsweise direkt mit einer Zelle interagiert, wird seine Zeile nicht mehr freigegeben. Da dies nicht vermieden werden kann, sind die Richtlinien in diesem Thema nur nützlich, wenn Sie mit sehr großen Datenmengen arbeiten und nur dann, wenn Benutzer mit einem relativ kleinen Teil der Daten interagieren, wenn das Programm ausgeführt wird.

Eine Zeile kann nicht in einem ungebundenen Steuerelement freigegeben werden, <xref:System.Windows.Forms.DataGridView> Wenn eine ihrer Zellen Werte enthält. Wenn das <xref:System.Windows.Forms.DataGridView> Steuerelement an eine externe Datenquelle gebunden ist oder wenn Sie den virtuellen Modus implementieren und eine eigene Datenquelle bereitstellen, werden die Zellwerte außerhalb des Steuer Elements anstatt in Zell Objekten gespeichert, sodass die Zeilen freigegeben werden können.

Ein Row-Objekt kann nur freigegeben werden, wenn der Status aller Zellen aus dem Zustand der Zeile und den Zuständen der Spalten, die die Zellen enthalten, bestimmt werden kann. Wenn Sie den Zustand einer Zelle ändern, sodass Sie nicht mehr aus dem Zustand ihrer Zeile und Spalte abgeleitet werden kann, kann die Zeile nicht freigegeben werden.

Eine Zeile kann z. b. in einer der folgenden Situationen nicht freigegeben werden:

- Die Zeile enthält eine einzelne ausgewählte Zelle, die nicht in einer ausgewählten Spalte enthalten ist.

- Die Zeile enthält eine Zelle, deren-Eigenschaft oder-Eigenschaft <xref:System.Windows.Forms.DataGridViewCell.ToolTipText%2A> <xref:System.Windows.Forms.DataGridViewCell.ContextMenuStrip%2A> festgelegt ist.

- Die Zeile enthält eine, <xref:System.Windows.Forms.DataGridViewComboBoxCell> deren- <xref:System.Windows.Forms.DataGridViewComboBoxCell.Items%2A> Eigenschaft auf festgelegt ist.

Im gebundenen oder im virtuellen Modus können Sie Quick Infos und Kontextmenüs für einzelne Zellen bereitstellen, indem Sie das <xref:System.Windows.Forms.DataGridView.CellToolTipTextNeeded> -Ereignis und das- <xref:System.Windows.Forms.DataGridView.CellContextMenuStripNeeded> Ereignis behandeln.

Das- <xref:System.Windows.Forms.DataGridView> Steuerelement versucht automatisch, freigegebene Zeilen zu verwenden, wenn der Zeilen hinzugefügt werden <xref:System.Windows.Forms.DataGridViewRowCollection> . Verwenden Sie die folgenden Richtlinien, um sicherzustellen, dass Zeilen freigegeben werden

- Vermeiden Sie das Aufrufen der Überladung der `Add(Object[])` <xref:System.Windows.Forms.DataGridViewRowCollection.Add%2A> -Methode und der Überladung der- `Insert(Object[])` <xref:System.Windows.Forms.DataGridViewRowCollection.Insert%2A> Methode der <xref:System.Windows.Forms.DataGridView.Rows%2A?displayProperty=nameWithType> -Auflistung. Diese über Ladungen erstellen automatisch nicht freigegebene Zeilen.

- Stellen Sie sicher, dass die in der-Eigenschaft angegebene Zeile <xref:System.Windows.Forms.DataGridView.RowTemplate%2A?displayProperty=nameWithType> in den folgenden Fällen freigegeben werden kann:

  - Beim Aufrufen der- `Add()` oder- `Add(Int32)` über Ladungen der-Methode oder der Überladung der- <xref:System.Windows.Forms.DataGridViewRowCollection.Add%2A> `Insert(Int32,Int32)` <xref:System.Windows.Forms.DataGridViewRowCollection.Insert%2A> Methode der <xref:System.Windows.Forms.DataGridView.Rows%2A?displayProperty=nameWithType> -Auflistung.

  - Beim Erhöhen des Werts der- <xref:System.Windows.Forms.DataGridView.RowCount%2A?displayProperty=nameWithType> Eigenschaft.

  - Beim Festlegen der- <xref:System.Windows.Forms.DataGridView.DataSource%2A?displayProperty=nameWithType> Eigenschaft.

- Stellen Sie sicher, dass die durch den-Parameter festgelegten Zeilen frei `indexSource` gegeben werden kann, wenn Sie die <xref:System.Windows.Forms.DataGridViewRowCollection.AddCopy%2A> <xref:System.Windows.Forms.DataGridViewRowCollection.AddCopies%2A> Methoden,, <xref:System.Windows.Forms.DataGridViewRowCollection.InsertCopy%2A> und der-Auflistung aufrufen <xref:System.Windows.Forms.DataGridViewRowCollection.InsertCopies%2A> <xref:System.Windows.Forms.DataGridView.Rows%2A?displayProperty=nameWithType> .

- Stellen Sie sicher, dass die angegebene Zeile oder die Zeilen freigegeben werden können, wenn Sie die Überladung der- `Add(DataGridViewRow)` <xref:System.Windows.Forms.DataGridViewRowCollection.Add%2A> Methode aufrufen, die <xref:System.Windows.Forms.DataGridViewRowCollection.AddRange%2A> -Methode, die `Insert(Int32,DataGridViewRow)` -Überladung der <xref:System.Windows.Forms.DataGridViewRowCollection.Insert%2A> -Methode und die- <xref:System.Windows.Forms.DataGridViewRowCollection.InsertRange%2A> Methode der-Auflistung <xref:System.Windows.Forms.DataGridView.Rows%2A?displayProperty=nameWithType> .

Verwenden Sie die-Methode, um zu bestimmen, ob eine Zeile freigegeben ist, <xref:System.Windows.Forms.DataGridViewRowCollection.SharedRow%2A?displayProperty=nameWithType> und überprüfen Sie dann die-Eigenschaft des-Objekts <xref:System.Windows.Forms.DataGridViewBand.Index%2A> . Freigegebene Zeilen haben immer den- <xref:System.Windows.Forms.DataGridViewBand.Index%2A> Eigenschafts Wert – 1.

## <a name="preventing-rows-from-becoming-unshared"></a>Verhindern, dass Zeilen freigegeben werden

Freigegebene Zeilen können aufgrund von Code-oder Benutzeraktionen freigegeben werden. Um eine Beeinträchtigung der Leistung zu vermeiden, sollten Sie vermeiden, dass Zeilen freigegeben werden. Während der Anwendungsentwicklung können Sie das- <xref:System.Windows.Forms.DataGridView.RowUnshared> Ereignis behandeln, um zu bestimmen, wann Zeilen freigegeben werden. Dies ist nützlich, wenn Probleme mit der Zeilen Freigabe debuggt werden.

Verwenden Sie die folgenden Richtlinien, um zu verhindern, dass Zeilen freigegeben werden:

- Vermeiden Sie die Indizierung der Auflistung, <xref:System.Windows.Forms.DataGridView.Rows%2A> oder durchlaufen Sie Sie mit einer- `foreach` Schleife. Sie müssen in der Regel nicht direkt auf Zeilen zugreifen. <xref:System.Windows.Forms.DataGridView> Methoden, die auf Zeilen angewendet werden, übernehmen Zeilen Index Argumente anstelle von Zeilen Instanzen. Außerdem empfangen Handler für Zeilen bezogene Ereignisse Ereignis Argument Objekte mit Zeilen Eigenschaften, die Sie verwenden können, um Zeilen zu bearbeiten, ohne dass Sie freigegeben werden.

- Wenn Sie auf ein Zeilen Objekt zugreifen müssen, verwenden Sie die- <xref:System.Windows.Forms.DataGridViewRowCollection.SharedRow%2A?displayProperty=nameWithType> Methode, und übergeben Sie den tatsächlichen Index der Zeile. Beachten Sie jedoch, dass bei der Änderung eines freigegebenen Zeilen Objekts, das über diese Methode abgerufen wird, alle Zeilen geändert werden, die dieses Objekt gemeinsam verwenden. Die Zeile für neue Datensätze wird jedoch nicht gemeinsam mit anderen Zeilen verwendet, sodass Sie nicht beeinträchtigt wird, wenn Sie eine andere Zeile ändern. Beachten Sie auch, dass verschiedene Zeilen, die durch eine freigegebene Zeile dargestellt werden, unterschiedliche Kontextmenüs aufweisen können Um das richtige Kontextmenü aus einer freigegebenen Zeilen Instanz abzurufen, verwenden Sie die- <xref:System.Windows.Forms.DataGridViewRow.GetContextMenuStrip%2A> Methode, und übergeben Sie den tatsächlichen Index der Zeile. Wenn Sie stattdessen auf die-Eigenschaft der freigegebenen Zeile zugreifen <xref:System.Windows.Forms.DataGridViewRow.ContextMenuStrip%2A> , wird der freigegebene Zeilen Index "-1" verwendet, und es wird nicht das richtige Kontextmenü abgerufen.

- Vermeiden Sie das Indizieren der Auflistung <xref:System.Windows.Forms.DataGridViewRow.Cells%2A?displayProperty=nameWithType> . Wenn Sie direkt auf eine Zelle zugreifen, wird die Freigabe der übergeordneten Zeile aufgehoben, und eine neue wird instanziiert <xref:System.Windows.Forms.DataGridViewRow> . Handler für Zellen bezogene Ereignisse empfangen Ereignis Argument Objekte mit Zell Eigenschaften, die Sie zum Bearbeiten von Zellen verwenden können, ohne dass Zeilen freigegeben werden. Sie können auch die <xref:System.Windows.Forms.DataGridView.CurrentCellAddress%2A> -Eigenschaft verwenden, um die Zeilen-und Spalten Indizes der aktuellen Zelle abzurufen, ohne direkt auf die Zelle zuzugreifen.

- Vermeiden Sie Zellen basierte Auswahl Modi. Diese Modi bewirken, dass Zeilen freigegeben werden. Legen Sie stattdessen die- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A?displayProperty=nameWithType> Eigenschaft auf <xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect?displayProperty=nameWithType> oder fest <xref:System.Windows.Forms.DataGridViewSelectionMode.FullColumnSelect?displayProperty=nameWithType> .

- Behandeln Sie das- <xref:System.Windows.Forms.DataGridViewRowCollection.CollectionChanged?displayProperty=nameWithType> Ereignis oder das- <xref:System.Windows.Forms.DataGridView.RowStateChanged?displayProperty=nameWithType> Ereignis nicht. Diese Ereignisse bewirken, dass Zeilen freigegeben werden. Rufen Sie auch nicht die- <xref:System.Windows.Forms.DataGridViewRowCollection.OnCollectionChanged%2A?displayProperty=nameWithType> Methode oder die- <xref:System.Windows.Forms.DataGridView.OnRowStateChanged%2A?displayProperty=nameWithType> Methode auf, mit der diese Ereignisse erhoben werden.

- Greifen Sie nicht auf die Auflistung zu <xref:System.Windows.Forms.DataGridView.SelectedCells%2A?displayProperty=nameWithType> , wenn der- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A?displayProperty=nameWithType> Eigenschafts Wert <xref:System.Windows.Forms.DataGridViewSelectionMode.FullColumnSelect> , <xref:System.Windows.Forms.DataGridViewSelectionMode.ColumnHeaderSelect> , <xref:System.Windows.Forms.DataGridViewSelectionMode.FullRowSelect> oder ist <xref:System.Windows.Forms.DataGridViewSelectionMode.RowHeaderSelect> . Dies bewirkt, dass alle ausgewählten Zeilen freigegeben werden.

- Die-Methode wird nicht aufgerufen <xref:System.Windows.Forms.DataGridView.AreAllCellsSelected%2A?displayProperty=nameWithType> . Diese Methode kann bewirken, dass Zeilen freigegeben werden.

- Die-Methode wird nicht aufgerufen, <xref:System.Windows.Forms.DataGridView.SelectAll%2A?displayProperty=nameWithType> Wenn der- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A?displayProperty=nameWithType> Eigenschafts Wert ist <xref:System.Windows.Forms.DataGridViewSelectionMode.CellSelect> . Dies bewirkt, dass alle Zeilen freigegeben werden.

- Legen Sie die- <xref:System.Windows.Forms.DataGridViewCell.ReadOnly%2A> Eigenschaft oder die- <xref:System.Windows.Forms.DataGridViewCell.Selected%2A> Eigenschaft einer Zelle nicht auf fest, `false` Wenn die entsprechende-Eigenschaft in der-Spalte auf festgelegt ist `true` . Dies bewirkt, dass alle Zeilen freigegeben werden.

- Greifen Sie nicht auf die- <xref:System.Windows.Forms.DataGridViewRowCollection.List%2A?displayProperty=nameWithType> Eigenschaft zu. Dies bewirkt, dass alle Zeilen freigegeben werden.

- Die-Überladung der-Methode wird nicht aufgerufen `Sort(IComparer)` <xref:System.Windows.Forms.DataGridView.Sort%2A> . Das Sortieren mit einem benutzerdefinierten Vergleich bewirkt, dass alle Zeilen freigegeben werden.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- [Leistungsoptimierung im DataGridView-Steuerelement in Windows Forms](performance-tuning-in-the-windows-forms-datagridview-control.md)
- [Virtueller Modus im DataGridView-Steuerelement in Windows Forms](virtual-mode-in-the-windows-forms-datagridview-control.md)
- [Datenanzeigemodi im DataGridView-Steuerelement in Windows Forms](data-display-modes-in-the-windows-forms-datagridview-control.md)
- [Zellstile im DataGridView-Steuerelement in Windows Forms](cell-styles-in-the-windows-forms-datagridview-control.md)
- [Vorgehensweise: Festlegen von Standardzellenformaten für das DataGridView-Steuerelement in Windows Forms](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md)
- [Größenänderungsoptionen im DataGridView-Steuerelement in Windows Forms](sizing-options-in-the-windows-forms-datagridview-control.md)
