---
title: Unterstützte Datenquellen
ms.date: 03/30/2017
helpviewer_keywords:
- collections [Windows Forms], binding to
- OLE DB providers [Windows Forms], Windows Forms
- DataTable class [Windows Forms], binding and Windows Forms
- Windows Forms, data binding
- DataView class [Windows Forms], binding and Windows Forms
- DataViewManager class [Windows Forms], binding and Windows Forms
- Windows Forms, source data
- arrays [Windows Forms]
- data sources [Windows Forms]
- data providers [Windows Forms]
- DataSet class [Windows Forms], binding and Windows Forms
- data [Windows Forms], data providers
ms.assetid: 3d2c43f6-462b-4d35-9c86-13e9afe012e1
ms.openlocfilehash: b4c1c722790688ee638aa4de417664f697df3249
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976207"
---
# <a name="data-sources-supported-by-windows-forms"></a>Von Windows Forms unterstützte Datenquellen

In der Vergangenheit wurde die Datenbindung innerhalb von Anwendungen verwendet, um die in-Datenbanken gespeicherten Daten zu nutzen. Mit Windows Forms Datenbindung können Sie auf Daten aus Datenbanken sowie auf Daten in anderen Strukturen (z. b. Arrays und Sammlungen) zugreifen, solange bestimmte Mindestanforderungen erfüllt sind.  
  
## <a name="structures-to-bind-to"></a>Strukturen, an die gebunden werden soll  

 In Windows Forms können Sie eine Bindung an eine Vielzahl von Strukturen herstellen, von einfachen Objekten (einfache Bindung) bis hin zu komplexen Listen wie ADO.NET Data Tables (komplexe Bindung). Bei einer einfachen Bindung unterstützt Windows Forms das Binden an die öffentlichen Eigenschaften für das einfache Objekt. Windows Forms Listen basierte Bindung erfordert im Allgemeinen, dass das-Objekt die- <xref:System.Collections.IList> Schnittstelle oder die- <xref:System.ComponentModel.IListSource> Schnittstelle unterstützt. Außerdem können Sie, wenn Sie mit über eine- <xref:System.Windows.Forms.BindingSource> Komponente binden, eine Bindung an ein-Objekt durchlaufen, das die- <xref:System.Collections.IEnumerable> Schnittstelle unterstützt. Weitere Informationen zu Schnittstellen, die mit der Datenbindung verknüpft sind, finden [Sie Unterschnitt stellen für die Datenbindung](interfaces-related-to-data-binding.md).  
  
 In der folgenden Liste werden die Strukturen angezeigt, an die in Windows Forms gebunden werden kann.  
  
 <xref:System.Windows.Forms.BindingSource>  
 Eine <xref:System.Windows.Forms.BindingSource> ist die häufigste Windows Forms Datenquelle und fungiert als Proxy zwischen einer Datenquelle und Windows Forms Steuerelementen. Das allgemeine <xref:System.Windows.Forms.BindingSource> Verwendungs Muster besteht darin, die Steuerelemente an die zu binden <xref:System.Windows.Forms.BindingSource> und die <xref:System.Windows.Forms.BindingSource> an die Datenquelle zu binden (z. b. eine ADO.net-Datentabelle oder ein Geschäftsobjekt). <xref:System.Windows.Forms.BindingSource>Bietet Dienste, die die Ebene der Unterstützung der Datenbindung aktivieren und verbessern. Beispielsweise können Windows Forms Listen basierte Steuerelemente, wie z. b. und, die <xref:System.Windows.Forms.DataGridView> <xref:System.Windows.Forms.ComboBox> Bindung an Datenquellen nicht direkt unterstützen <xref:System.Collections.IEnumerable> , dieses Szenario durch Binden über eine aktivieren <xref:System.Windows.Forms.BindingSource> . In diesem Fall konvertiert die <xref:System.Windows.Forms.BindingSource> Datenquelle in eine <xref:System.Collections.IList> .  
  
 Einfache Objekte  
 Windows Forms unterstützt die Daten Bindungs Steuerelement-Eigenschaften für öffentliche Eigenschaften in der Instanz eines-Objekts, das den- <xref:System.Windows.Forms.Binding> Typ verwendet. Windows Forms unterstützt auch das Binden von Listen basierten Steuerelementen, z. b. <xref:System.Windows.Forms.ListControl> an eine Objektinstanz, wenn eine <xref:System.Windows.Forms.BindingSource> verwendet wird.  
  
 Array oder Sammlung  
 Eine Liste muss die-Schnittstelle implementieren, um als Datenquelle fungieren zu <xref:System.Collections.IList> können. ein Beispiel hierfür ist ein Array, bei dem es sich um eine Instanz der- <xref:System.Array> Klasse handelt. Weitere Informationen zu Arrays finden Sie unter Vorgehens [Weise: Erstellen eines Arrays von Objekten (Visual Basic)](/previous-versions/visualstudio/visual-studio-2010/487y7874(v=vs.100)).  
  
 Im Allgemeinen sollten Sie verwenden, <xref:System.ComponentModel.BindingList%601> Wenn Sie Listen von Objekten für die Datenbindung erstellen. <xref:System.ComponentModel.BindingList%601> ist eine generische Version der- <xref:System.ComponentModel.IBindingList> Schnittstelle. Die- <xref:System.ComponentModel.IBindingList> Schnittstelle erweitert die- <xref:System.Collections.IList> Schnittstelle durch Hinzufügen von Eigenschaften, Methoden und Ereignissen, die für die bidirektionale Datenbindung  
  
 <xref:System.Collections.IEnumerable>  
 Windows Forms Steuerelemente können an Datenquellen gebunden werden, die nur die-Schnittstelle unterstützen, <xref:System.Collections.IEnumerable> Wenn Sie durch eine Komponente gebunden werden <xref:System.Windows.Forms.BindingSource> .  
  
 ADO.net-Datenobjekte  
 ADO.NET stellt eine Reihe von Datenstrukturen bereit, die für die Bindung an geeignet sind. Jede hängt von ihrer Komplexität und Komplexität ab.  
  
- <xref:System.Data.DataColumn>. Ein <xref:System.Data.DataColumn> ist der wesentliche Baustein von <xref:System.Data.DataTable> , da eine Reihe von Spalten eine Tabelle bilden. Jede <xref:System.Data.DataColumn> verfügt über eine- <xref:System.Data.DataColumn.DataType%2A> Eigenschaft, die die Art der Daten bestimmt, die die Spalte enthält (z. b. das Erstellen eines Auto Fahrzeugs in einer Tabelle, die Autos beschreibt). Sie können ein Steuerelement (z. b. <xref:System.Windows.Forms.TextBox> die-Eigenschaft eines Steuer Elements) einfach <xref:System.Windows.Forms.Control.Text%2A> an eine Spalte in einer Datentabelle binden.  
  
- <xref:System.Data.DataTable>. Eine <xref:System.Data.DataTable> ist die Darstellung einer Tabelle mit Zeilen und Spalten in ADO.net. Eine Datentabelle enthält zwei Auflistungen: <xref:System.Data.DataColumn> , die die Spalten von Daten in einer bestimmten Tabelle darstellen (die letztendlich die Arten von Daten bestimmen, die in diese Tabelle eingegeben werden können), und <xref:System.Data.DataRow> , die die Daten Zeilen in einer bestimmten Tabelle darstellen. Sie können ein Steuerelement Komplex an die in einer Datentabelle enthaltenen Informationen binden (z. b. das Binden des <xref:System.Windows.Forms.DataGridView> Steuer Elements an eine Datentabelle). Wenn Sie jedoch eine Bindung an einen herstellen <xref:System.Data.DataTable> , stellen Sie tatsächlich eine Bindung an die Standardansicht der Tabelle her.  
  
- <xref:System.Data.DataView>. Ein <xref:System.Data.DataView> ist eine angepasste Ansicht einer einzelnen Datentabelle, die gefiltert oder sortiert werden kann. Eine Datenansicht ist die Daten "Snapshot", die von komplexen gebundenen Steuerelementen verwendet werden. Sie können eine einfache Bindung oder eine komplexe Bindung an die Daten innerhalb einer Datenansicht vornehmen, aber beachten Sie, dass Sie an ein festes "Bild" der Daten anstatt an eine saubere, aktualisierbare Datenquelle binden.  
  
- <xref:System.Data.DataSet>. Ein <xref:System.Data.DataSet> ist eine Auflistung von Tabellen, Beziehungen und Einschränkungen der Daten in einer Datenbank. Sie können eine einfache Bindung oder eine komplexe Bindung an die Daten innerhalb eines Datasets herstellen, aber beachten Sie, dass Sie die Bindung an den Standard <xref:System.Data.DataViewManager> Wert für das-Element <xref:System.Data.DataSet> (siehe nächster Aufzählungs Punkt) durchlaufen.  
  
- <xref:System.Data.DataViewManager>. Ein <xref:System.Data.DataViewManager> ist eine angepasste Ansicht des gesamten <xref:System.Data.DataSet> , analog zu einer <xref:System.Data.DataView> , aber mit der enthaltenen Beziehung. Mit einer <xref:System.Data.DataViewManager.DataViewSettings%2A> Sammlung können Sie Standardfilter und Sortieroptionen für alle Sichten festlegen, die <xref:System.Data.DataViewManager> für eine bestimmte Tabelle vorhanden sind.  
  
## <a name="see-also"></a>Siehe auch

- [Änderungsbenachrichtigung in der Windows Forms-Datenbindung](change-notification-in-windows-forms-data-binding.md)
- [Datenbindung und Windows Forms](data-binding-and-windows-forms.md)
- [Datenbindung in Web Forms](windows-forms-data-binding.md)
