---
title: Zusammenfassung der DataGridView-Steuerelementtechnologie
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], about DataGridView control
- data grids [Windows Forms], about data grids
ms.assetid: 094498c3-a126-4a3f-83fe-f69e96c7717b
ms.openlocfilehash: 1b620cabb756fadb8468fc75879025131e4bffd8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972160"
---
# <a name="datagridview-control-technology-summary-windows-forms"></a>Zusammenfassung der DataGridView-Steuerelementtechnologie (Windows Forms)

In diesem Thema sind Informationen zum `DataGridView`-Steuerelement und den Klassen zusammengefasst, die seine Verwendung unterstützen.  
  
 Das Anzeigen von Daten in einem tabellarischen Format ist eine Aufgabe, die Sie wahrscheinlich häufig ausführen. Das- `DataGridView` Steuerelement ist als umfassende Lösung für die Darstellung von Daten in einem Raster konzipiert.  
  
## <a name="keywords"></a>Keywords  

 DataGridView, BindingSource, Table, Cell, Data Binding, Virtual Mode  
  
## <a name="namespaces"></a>Namespaces  

 <xref:System.Windows.Forms?displayProperty=nameWithType>  
  
 <xref:System.Data?displayProperty=nameWithType>  
  
## <a name="related-technologies"></a>Verwandte Technologien  

 `BindingSource`  
  
## <a name="background"></a>Hintergrund  

 Benutzeroberflächen-Designer finden häufig die Notwendigkeit, Tabellendaten für Benutzer anzuzeigen. Der .NET Framework bietet mehrere Möglichkeiten zum Anzeigen von Daten in einer Tabelle oder einem Raster. Das- `DataGridView` Steuerelement stellt die neueste Entwicklung dieser Technologie für Windows Forms-Anwendungen dar.  
  
 Das- `DataGridView` Steuerelement kann Daten Zeilen aus einem Datenspeicher anzeigen. Viele Arten von Daten speichern werden unterstützt. Der Datenspeicher kann einfache, nicht typisierte Daten enthalten, z. b. ein eindimensionales Array, oder es kann typisierte Daten enthalten, z <xref:System.Data.DataSet> . b.. Weitere Informationen finden Sie unter Gewusst [wie: Binden von Daten an das Windows Forms DataGridView-Steuer](how-to-bind-data-to-the-windows-forms-datagridview-control.md)Element.  
  
 Das `DataGridView`-Steuerelement ermöglicht die flexible Anzeige von Daten in tabellarischer Form. Sie können das-Steuerelement verwenden, um schreibgeschützte oder bearbeitbare Sichten von kleinen bis sehr großen Datensätzen anzuzeigen.  
  
 Sie können das- `DataGridView` Steuerelement auf verschiedene Weise erweitern, um benutzerdefiniertes Verhalten in Ihren Anwendungen zu erstellen. So können Sie beispielsweise programmgesteuert Ihre eigenen Sortieralgorithmen angeben und eigene Zelltypen erstellen. Die Darstellung des `DataGridView`-Steuerelements kann mithilfe mehrerer Eigenschaften ganz einfach angepasst werden. Viele Typen von Daten speichern können als Datenquelle verwendet werden, oder das `DataGridView` Steuerelement kann ohne eine Datenquelle ausgeführt werden.  
  
## <a name="implementing-datagridview-classes"></a>Implementieren von DataGridView-Klassen  

 Es gibt mehrere Möglichkeiten, die `DataGridView` Erweiterbarkeits Funktionen des Steuer Elements zu nutzen. Sie können zahlreiche Aspekte des Steuer Elements durch Ereignisse und Eigenschaften anpassen, aber einige Anpassungen erfordern, dass Sie neue Klassen erstellen, die von vorhandenen Klassen abgeleitet werden `DataGridView` .  
  
 Die am häufigsten verwendeten Basisklassen sind `DataGridViewCell` und `DataGridViewColumn` . Sie können eine eigene Zellklasse von `DataGridViewCell` oder einer ihrer untergeordneten Klassen ableiten. Obwohl Sie jeder beliebigen Spalte einen beliebigen Zellentyp hinzufügen können, leiten Sie in der Regel auch eine begleitende Spalten Klasse von ab `DataGridViewColumn` , die standardmäßig Zellen Ihres benutzerdefinierten Zelltyps hostet.  
  
 Sie können die- `IDataGridViewEditingCell` Schnittstelle in der abgeleiteten Cell-Klasse implementieren, um einen Zelltyp zu erstellen, der über Bearbeitungsfunktionen verfügt, aber kein-Steuerelement im Bearbeitungsmodus hostet. Um ein Steuerelement zu erstellen, das Sie in einer Zelle im Bearbeitungsmodus hosten können, können Sie die- `IDataGridViewEditingControl` Schnittstelle in einer von abgeleiteten Klasse implementieren <xref:System.Windows.Forms.Control> .  
  
 Weitere Informationen finden Sie unter Gewusst [wie: Anpassen von Zellen und Spalten im Windows Forms DataGridView-Steuerelement durch Erweiterung ihres Verhaltens und ihrer](customize-cells-and-columns-in-the-datagrid-by-extending-behavior.md) Darstellung und Gewusst [wie: Hosten von Steuerelementen in Windows Forms DataGridView-Zellen](how-to-host-controls-in-windows-forms-datagridview-cells.md).  
  
## <a name="datagridview-classes-at-a-glance"></a>DataGridView-Klassen auf einen Blick  

 <xref:System.Windows.Forms>  
  
|Technologiebereich|Klassen/Schnittstellen/Konfigurationselemente|  
|---------------------|-------------------------------------------------|  
|Datenbindung|<xref:System.Windows.Forms.BindingSource>|  
|Datenpräsentation|<xref:System.Windows.Forms.DataGridView><br /><br /> <xref:System.Windows.Forms.DataGridViewCell> und abgeleitete Klassen<br /><br /> <xref:System.Windows.Forms.DataGridViewRow> und abgeleitete Klassen<br /><br /> <xref:System.Windows.Forms.DataGridViewColumn> und abgeleitete Klassen<br /><br /> <xref:System.Windows.Forms.DataGridViewCellStyle>|  
|<xref:System.Windows.Forms.DataGridView> Erweiterbarkeit|<xref:System.Windows.Forms.DataGridViewCell> und abgeleitete Klassen<br /><br /> <xref:System.Windows.Forms.DataGridViewColumn> und abgeleitete Klassen<br /><br /> <xref:System.Windows.Forms.IDataGridViewEditingCell><br /><br /> <xref:System.Windows.Forms.IDataGridViewEditingControl>|  
  
## <a name="whats-new"></a>Neuerungen  

 Das- <xref:System.Windows.Forms.DataGridView> Steuerelement ist als umfassende Lösung zum Anzeigen von Tabellendaten mit Windows Forms konzipiert. Sie sollten die Verwendung des- <xref:System.Windows.Forms.DataGridView> Steuer Elements vor anderen Lösungen in Erwägung gezogen werden, z <xref:System.Windows.Forms.DataGrid> . b. beim Erstellen einer neuen Anwendung. Weitere Informationen finden Sie unter [Unterschiede zwischen dem DataGridView-Steuerelement und dem DataGrid-Steuerelement in Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).  
  
 Das- <xref:System.Windows.Forms.DataGridView> Steuerelement kann in enger Verbindung mit der-Komponente verwendet werden <xref:System.Windows.Forms.BindingSource> . Diese Komponente ist als primäre Datenquelle eines Formulars konzipiert. Sie kann die Interaktion zwischen einem <xref:System.Windows.Forms.DataGridView> Steuerelement und seiner Datenquelle unabhängig vom Typ der Datenquelle verwalten.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über das DataGridView-Steuerelement](datagridview-control-overview-windows-forms.md)
- [Architektur des DataGridView-Steuerelements](datagridview-control-architecture-windows-forms.md)
- [Schützen von Verbindungsinformationen](/dotnet/framework/data/adonet/protecting-connection-information)
