---
title: Spaltentypen im DataGridView-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- columns [Windows Forms], types
- DataGridView control [Windows Forms], column types
- data grids [Windows Forms], columns
ms.assetid: f0a0a9f1-8757-4bfd-891f-d7d12870dbed
ms.openlocfilehash: e918394cca6350854074d4c1567890138b2a1462
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972242"
---
# <a name="column-types-in-the-windows-forms-datagridview-control"></a>Spaltentypen im DataGridView-Steuerelement in Windows Forms
Das <xref:System.Windows.Forms.DataGridView> -Steuerelement verwendet mehrere Spaltentypen, um seine Informationen anzuzeigen, und ermöglicht es Benutzern, Informationen zu ändern oder hinzuzufügen.  
  
 Wenn Sie ein Steuerelement binden <xref:System.Windows.Forms.DataGridView> und die- <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A> Eigenschaft auf festlegen `true` , werden Spalten automatisch mit den Standard Spaltentypen generiert, die für die in der gebundenen Datenquelle enthaltenen Datentypen geeignet sind.  
  
 Sie können auch Instanzen der Spalten Klassen selbst erstellen und Sie der Auflistung hinzufügen, die von der-Eigenschaft zurückgegeben wird <xref:System.Windows.Forms.DataGridView.Columns%2A> . Sie können diese Instanzen für die Verwendung als ungebundene Spalten erstellen, oder Sie können Sie manuell binden. Manuell gebundene Spalten sind nützlich, wenn Sie z. b. eine automatisch generierte Spalte eines Typs durch eine Spalte eines anderen Typs ersetzen möchten.  
  
 In der folgenden Tabelle werden die verschiedenen Spalten Klassen beschrieben, die für die Verwendung im-Steuerelement verfügbar sind <xref:System.Windows.Forms.DataGridView> .  
  
|Klasse|BESCHREIBUNG|  
|-----------|-----------------|  
|<xref:System.Windows.Forms.DataGridViewTextBoxColumn>|Wird mit textbasierten Werten verwendet. Wird automatisch generiert, wenn an Zahlen und Zeichen folgen gebunden wird.|  
|<xref:System.Windows.Forms.DataGridViewCheckBoxColumn>|Wird mit <xref:System.Boolean> -und- <xref:System.Windows.Forms.CheckState> Werten verwendet. Wird automatisch generiert, wenn an Werte dieser Typen gebunden wird.|  
|<xref:System.Windows.Forms.DataGridViewImageColumn>|Wird verwendet, um Bilder anzuzeigen. Wird automatisch generiert, wenn an Byte Arrays,- <xref:System.Drawing.Image> Objekte oder-Objekte gebunden wird <xref:System.Drawing.Icon> .|  
|<xref:System.Windows.Forms.DataGridViewButtonColumn>|Wird verwendet, um Schaltflächen in Zellen anzuzeigen. Wird bei der Bindung nicht automatisch generiert. Wird normalerweise als ungebundene Spalten verwendet.|  
|<xref:System.Windows.Forms.DataGridViewComboBoxColumn>|Wird verwendet, um Dropdown Listen in Zellen anzuzeigen. Wird bei der Bindung nicht automatisch generiert. In der Regel manuell Daten gebunden.|  
|<xref:System.Windows.Forms.DataGridViewLinkColumn>|Wird verwendet, um Links in Zellen anzuzeigen. Wird bei der Bindung nicht automatisch generiert. In der Regel manuell Daten gebunden.|  
|Ihr benutzerdefinierter Spaltentyp|Sie können eine eigene Spalten Klasse erstellen, indem Sie die- <xref:System.Windows.Forms.DataGridViewColumn> Klasse oder eine der abgeleiteten Klassen erbt, um benutzerdefinierte Darstellung, Verhalten oder gehostete Steuerelemente bereitzustellen. Weitere Informationen finden Sie unter Gewusst [wie: Anpassen von Zellen und Spalten im Windows Forms DataGridView-Steuerelement durch Erweiterung ihres Verhaltens und ihrer](customize-cells-and-columns-in-the-datagrid-by-extending-behavior.md) Darstellung|  
  
 Diese Spaltentypen werden in den folgenden Abschnitten ausführlicher beschrieben.  
  
## <a name="datagridviewtextboxcolumn"></a>DataGridViewTextBoxColumn  
 Der <xref:System.Windows.Forms.DataGridViewTextBoxColumn> ist ein allgemeiner Spaltentyp für die Verwendung mit textbasierten Werten, wie z. b. Zahlen und Zeichen folgen. Im Bearbeitungsmodus wird ein <xref:System.Windows.Forms.TextBox> Steuerelement in der aktiven Zelle angezeigt, sodass Benutzer den Zellwert ändern können.  
  
 Zellwerte werden für die Anzeige automatisch in Zeichen folgen konvertiert. Werte, die vom Benutzer eingegeben oder geändert werden, werden automatisch so analysiert, dass ein Zellwert des entsprechenden Datentyps erstellt wird. Sie können diese Konvertierungen anpassen, indem Sie die <xref:System.Windows.Forms.DataGridView.CellFormatting> -und- <xref:System.Windows.Forms.DataGridView.CellParsing> Ereignisse des-Steuer Elements verarbeiten <xref:System.Windows.Forms.DataGridView> .  
  
 Der zellwertdatentyp einer Spalte wird in der- <xref:System.Windows.Forms.DataGridViewColumn.ValueType%2A> Eigenschaft der Spalte angegeben.  
  
## <a name="datagridviewcheckboxcolumn"></a>DataGridViewCheckBoxColumn  
 Die <xref:System.Windows.Forms.DataGridViewCheckBoxColumn> wird mit <xref:System.Boolean> -und- <xref:System.Windows.Forms.CheckState> Werten verwendet. <xref:System.Boolean> Werte werden je nach Wert der-Eigenschaft als Kontrollkästchen mit zwei oder drei Zuständen angezeigt <xref:System.Windows.Forms.DataGridViewCheckBoxColumn.ThreeState%2A> . Wenn die Spalte an Werte gebunden ist <xref:System.Windows.Forms.CheckState> , <xref:System.Windows.Forms.DataGridViewCheckBoxColumn.ThreeState%2A> ist der Eigenschafts Wert `true` standardmäßig.  
  
 Kontrollkästchen Zellen Werte werden in der Regel entweder für den Speicher, z. b. für andere Daten, oder für die Durchführung von Massen Vorgängen bestimmt. Wenn Sie sofort reagieren möchten, wenn Benutzer auf eine Kontrollkästchen Zelle klicken, können Sie das- <xref:System.Windows.Forms.DataGridView.CellClick> Ereignis behandeln, aber dieses Ereignis tritt auf, bevor der Zellwert aktualisiert wird. Wenn Sie zum Zeitpunkt des klickfalls den neuen Wert benötigen, können Sie mit einer Option berechnen, welcher Wert auf Grundlage des aktuellen Werts erwartet wird. Ein anderer Ansatz besteht darin, die Änderung sofort zu übernehmen und das <xref:System.Windows.Forms.DataGridView.CellValueChanged> Ereignis zu behandeln, um darauf zu reagieren. Um die Änderung zu übernehmen, wenn auf die Zelle geklickt wird, müssen Sie das- <xref:System.Windows.Forms.DataGridView.CurrentCellDirtyStateChanged> Ereignis behandeln. Wenn die aktive Zelle im-Handler eine Kontrollkästchen Zelle ist, müssen Sie die <xref:System.Windows.Forms.DataGridView.CommitEdit%2A> -Methode aufzurufen und den- <xref:System.Windows.Forms.DataGridViewDataErrorContexts.Commit> Wert übergeben.  
  
## <a name="datagridviewimagecolumn"></a>DataGridViewImageColumn  
 <xref:System.Windows.Forms.DataGridViewImageColumn>Wird verwendet, um Bilder anzuzeigen. Bild Spalten können automatisch aus einer Datenquelle aufgefüllt, manuell für ungebundene Spalten aufgefüllt oder dynamisch in einem Handler für das-Ereignis aufgefüllt werden <xref:System.Windows.Forms.DataGridView.CellFormatting> .  
  
 Die automatische Auffüllung einer Bild Spalte aus einer Datenquelle funktioniert mit Byte Arrays in einer Vielzahl von Bildformaten, einschließlich aller Formate, die von der-Klasse unterstützt werden, <xref:System.Drawing.Image> und des OLE-Bildformats, das von Microsoft® Access und der Northwind-Beispieldatenbank verwendet wird.  
  
 Das manuelle Auffüllen einer Bild Spalte ist hilfreich, wenn Sie die Funktionalität eines <xref:System.Windows.Forms.DataGridViewButtonColumn> , aber mit einer angepassten Darstellung bereitstellen möchten. Sie können das- <xref:System.Windows.Forms.DataGridView.CellClick?displayProperty=nameWithType> Ereignis behandeln, um auf Klicks innerhalb einer Bildzelle zu reagieren.  
  
 Das Auffüllen der Zellen einer Bild Spalte in einem Handler für das <xref:System.Windows.Forms.DataGridView.CellFormatting> Ereignis ist hilfreich, wenn Sie Bilder für berechnete Werte oder Werte in nicht Bildformaten bereitstellen möchten. Sie können z. b. eine "Risk"-Spalte mit Zeichen folgen Werten wie `"high"` , und aufweisen, `"middle"` `"low"` die als Symbole angezeigt werden sollen. Alternativ haben Sie möglicherweise eine Spalte "Image", die die Speicherorte von Bildern enthält, die geladen werden müssen, und nicht den binären Inhalt der Bilder.  
  
## <a name="datagridviewbuttoncolumn"></a>DataGridViewButtonColumn  
 Mit dem <xref:System.Windows.Forms.DataGridViewButtonColumn> können Sie eine Spalte mit Zellen anzeigen, die Schaltflächen enthalten. Dies ist hilfreich, wenn Sie Ihren Benutzern eine einfache Möglichkeit zum Ausführen von Aktionen für bestimmte Datensätze bereitstellen möchten, z. b. das Platzieren einer Bestellung oder das Anzeigen von untergeordneten Datensätzen in einem separaten Fenster.  
  
 Schaltflächen Spalten werden nicht automatisch generiert, wenn ein Steuerelement an Daten gebunden wird <xref:System.Windows.Forms.DataGridView> . Um Schaltflächen Spalten zu verwenden, müssen Sie diese manuell erstellen und der Auflistung hinzufügen, die von der-Eigenschaft zurückgegeben wird <xref:System.Windows.Forms.DataGridView.Columns%2A?displayProperty=nameWithType> .  
  
 Sie können auf Benutzer Klicks in Schaltflächen Zellen reagieren, indem Sie das- <xref:System.Windows.Forms.DataGridView.CellClick?displayProperty=nameWithType> Ereignis behandeln.  
  
## <a name="datagridviewcomboboxcolumn"></a>DataGridViewComboBoxColumn  
 Mit dem <xref:System.Windows.Forms.DataGridViewComboBoxColumn> können Sie eine Spalte mit Zellen anzeigen, die Dropdown-Listenfelder enthalten. Dies ist nützlich für die Dateneingabe in Feldern, die nur bestimmte Werte enthalten können, z. b. die Kategoriespalte der Products-Tabelle in der Northwind-Beispieldatenbank.  
  
 Sie können die Dropdown Liste, die für alle Zellen verwendet wird, auf dieselbe Weise Auffüllen wie eine <xref:System.Windows.Forms.ComboBox> Dropdown Liste, entweder manuell durch die Auflistung, die von der <xref:System.Windows.Forms.DataGridViewComboBoxColumn.Items%2A> -Eigenschaft zurückgegeben wird, oder indem Sie Sie über die <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DataSource%2A> Eigenschaften, und an eine Datenquelle binden <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DisplayMember%2A> <xref:System.Windows.Forms.DataGridViewComboBoxColumn.ValueMember%2A> . Weitere Informationen finden Sie unter [ComboBox-Steuer](combobox-control-windows-forms.md)Element.  
  
 Sie können die eigentlichen Zellwerte an die Datenquelle binden, die vom-Steuerelement verwendet wird, <xref:System.Windows.Forms.DataGridView> indem Sie die- <xref:System.Windows.Forms.DataGridViewColumn.DataPropertyName%2A> Eigenschaft von festlegen <xref:System.Windows.Forms.DataGridViewComboBoxColumn?displayProperty=nameWithType> .  
  
 Kombinations Feld-Spalten werden nicht automatisch generiert, wenn ein Steuerelement an Daten gebunden wird <xref:System.Windows.Forms.DataGridView> . Wenn Sie Kombinations Feld Spalten verwenden möchten, müssen Sie diese manuell erstellen und der Auflistung hinzufügen, die von der-Eigenschaft zurückgegeben wird <xref:System.Windows.Forms.DataGridView.Columns%2A> .  
  
## <a name="datagridviewlinkcolumn"></a>DataGridViewLinkColumn  
 Mit dem <xref:System.Windows.Forms.DataGridViewLinkColumn> können Sie eine Spalte mit Zellen anzeigen, die Hyperlinks enthalten. Dies ist nützlich für URL-Werte in der Datenquelle oder als Alternative zur Schaltflächen Spalte, um besondere Verhaltensweisen wie das Öffnen eines Fensters mit untergeordneten Datensätzen zu untersuchen.  
  
 Link Spalten werden bei der Datenbindung an ein Steuerelement nicht automatisch generiert <xref:System.Windows.Forms.DataGridView> . Wenn Sie Link Spalten verwenden möchten, müssen Sie diese manuell erstellen und der Auflistung hinzufügen, die von der-Eigenschaft zurückgegeben wird <xref:System.Windows.Forms.DataGridView.Columns%2A> .  
  
 Sie können auf Benutzer Klicks auf Links reagieren, indem Sie das- <xref:System.Windows.Forms.DataGridView.CellContentClick> Ereignis behandeln. Dieses Ereignis unterscheidet sich von <xref:System.Windows.Forms.DataGridView.CellClick> den <xref:System.Windows.Forms.DataGridView.CellMouseClick> Ereignissen und, die auftreten, wenn ein Benutzer auf eine beliebige Stelle in einer Zelle klickt.  
  
 Die- <xref:System.Windows.Forms.DataGridViewLinkColumn> Klasse stellt mehrere Eigenschaften zum Ändern der Darstellung von Verknüpfungen vor, während und nach dem Klicken auf Sie bereit.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn>
- <xref:System.Windows.Forms.DataGridViewButtonColumn>
- <xref:System.Windows.Forms.DataGridViewCheckBoxColumn>
- <xref:System.Windows.Forms.DataGridViewComboBoxColumn>
- <xref:System.Windows.Forms.DataGridViewImageColumn>
- <xref:System.Windows.Forms.DataGridViewTextBoxColumn>
- <xref:System.Windows.Forms.DataGridViewLinkColumn>
- [DataGridView-Steuerelement](datagridview-control-windows-forms.md)
- [Vorgehensweise: Anzeigen von Bildern in Zellen des DataGridView-Steuerelements in Windows Forms](how-to-display-images-in-cells-of-the-windows-forms-datagridview-control.md)
- [Vorgehensweise: Arbeiten mit Bildspalten im DataGridView-Steuerelement in Windows Forms](how-to-work-with-image-columns-in-the-windows-forms-datagridview-control.md)
- [Anpassen des DataGridView-Steuerelements von Windows Forms](customizing-the-windows-forms-datagridview-control.md)
