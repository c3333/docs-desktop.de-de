---
title: Architektur der BindingSource-Komponente
ms.date: 03/30/2017
helpviewer_keywords:
- BindingSource component [Windows Forms], architecture
- Windows Forms, data binding
- BindingSource component [Windows Forms], about BindingSource component
- data binding [Windows Forms], BindingSource component
ms.assetid: 7bc69c90-8a11-48b1-9336-3adab5b41591
ms.openlocfilehash: 54a23ba899ceb05701fe3580aefbb723c6b3f0fd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975119"
---
# <a name="bindingsource-component-architecture"></a>Architektur der BindingSource-Komponente
Mit der- <xref:System.Windows.Forms.BindingSource> Komponente können Sie universell alle Windows Forms-Steuerelemente an Datenquellen binden.  
  
 Die <xref:System.Windows.Forms.BindingSource> Komponente vereinfacht das Binden von Steuerelementen an eine Datenquelle und bietet gegenüber herkömmlichen Daten Bindungen die folgenden Vorteile:  
  
- Aktiviert die Entwurfszeit Bindung an Geschäftsobjekte.  
  
- Kapselt <xref:System.Windows.Forms.CurrencyManager> Funktionen und macht <xref:System.Windows.Forms.CurrencyManager> Ereignisse zur Entwurfszeit verfügbar.  
  
- Vereinfacht das Erstellen einer Liste, die die-Schnittstelle unterstützt, <xref:System.ComponentModel.IBindingList> indem Listen Änderungs Benachrichtigungen für Datenquellen bereitgestellt werden, die keine systemeigene Unterstützung für Listen Änderungs Benachrichtigungen  
  
- Stellt einen Erweiterbarkeits Punkt für die- <xref:System.ComponentModel.IBindingList.AddNew%2A?displayProperty=nameWithType> Methode bereit.  
  
- Stellt eine Dereferenzierungsebene zwischen der Datenquelle und dem-Steuerelement bereit. Diese Dereferenzierung ist wichtig, wenn sich die Datenquelle zur Laufzeit ändern kann.  
  
- Interagiert mit anderen datenbezogenen Windows Forms Steuerelementen, insbesondere dem <xref:System.Windows.Forms.BindingNavigator> und den-Steuer <xref:System.Windows.Forms.DataGridView> Elementen.  
  
 Aus diesen Gründen ist die- <xref:System.Windows.Forms.BindingSource> Komponente die bevorzugte Methode, um Ihre Windows Forms-Steuerelemente an Datenquellen zu binden.  
  
## <a name="bindingsource-features"></a>BindingSource-Funktionen  
 Die <xref:System.Windows.Forms.BindingSource> Komponente stellt mehrere Funktionen zum Binden von Steuerelementen an Daten bereit. Mit diesen Features können Sie die meisten Daten Bindungs Szenarios implementieren, bei denen fast keine Codierung für Sie durchzuführen ist.  
  
 Die <xref:System.Windows.Forms.BindingSource> Komponente erreicht dies durch die Bereitstellung einer konsistenten Schnittstelle für den Zugriff auf viele verschiedene Arten von Datenquellen. Dies bedeutet, dass Sie dieselbe Prozedur für die Bindung an einen beliebigen Typ verwenden. Beispielsweise können Sie die <xref:System.Windows.Forms.BindingSource.DataSource%2A> -Eigenschaft an einen <xref:System.Data.DataSet> oder an ein Geschäftsobjekt anfügen. in beiden Fällen verwenden Sie denselben Satz von Eigenschaften, Methoden und Ereignissen, um die Datenquelle zu bearbeiten.  
  
 Die konsistente Schnittstelle, die von der Komponente bereitgestellt wird <xref:System.Windows.Forms.BindingSource> , vereinfacht das Binden von Daten an Steuerelemente erheblich. Bei Datenquellen Typen, die Änderungs Benachrichtigungen bereitstellen, <xref:System.Windows.Forms.BindingSource> kommuniziert die Komponente automatisch mit Änderungen zwischen dem Steuerelement und der Datenquelle. Für Datenquellen Typen, die keine Änderungs Benachrichtigung bereitstellen, werden Ereignisse bereitgestellt, mit denen Sie Änderungs Benachrichtigungen durchführen können. In der folgenden Liste sind die von der-Komponente unterstützten Funktionen aufgeführt <xref:System.Windows.Forms.BindingSource> :  
  
- Dereferenzierung.  
  
- Währungsverwaltung.  
  
- Datenquelle als Liste.  
  
- <xref:System.Windows.Forms.BindingSource> als <xref:System.ComponentModel.IBindingList> .  
  
- Erstellen eines benutzerdefinierten Elements.  
  
- Transaktions Element Erstellung.  
  
- <xref:System.Collections.IEnumerable> Förder.  
  
- Unterstützung für die Entwurfszeit.  
  
- Statische <xref:System.Windows.Forms.ListBindingHelper> Methoden.  
  
- Sortieren und Filtern mit der- <xref:System.ComponentModel.IBindingListView> Schnittstelle.  
  
- Integration in <xref:System.Windows.Forms.BindingNavigator> .  
  
### <a name="indirection"></a>Dereferenzierung  
 Die <xref:System.Windows.Forms.BindingSource> Komponente stellt eine Dereferenzierungsebene zwischen einem Steuerelement und einer Datenquelle bereit. Anstatt ein Steuerelement direkt an eine Datenquelle zu binden, binden Sie das Steuerelement an eine <xref:System.Windows.Forms.BindingSource> und fügen die Datenquelle an die <xref:System.Windows.Forms.BindingSource> -Eigenschaft der Komponente an <xref:System.Windows.Forms.BindingSource.DataSource%2A> .  
  
 Bei dieser Dereferenzierung können Sie die Datenquelle ohne Zurücksetzen der Steuerelement Bindung ändern. Dadurch haben Sie die folgenden Möglichkeiten:  
  
- Sie können das <xref:System.Windows.Forms.BindingSource> an verschiedene Datenquellen anfügen, während Sie die aktuellen Steuerelement Bindungen beibehalten.  
  
- Sie können Elemente in der Datenquelle ändern und gebundene Steuerelemente benachrichtigen. Weitere Informationen finden Sie unter Gewusst [wie: reflektieren von Datenquellen Aktualisierungen in einem Windows Forms-Steuerelement mit der BindingSource](reflect-data-source-updates-in-a-wf-control-with-the-bindingsource.md).  
  
- Sie können eine Bindung zu einem <xref:System.Type> anstelle eines Objekts im Arbeitsspeicher herstellen. Weitere Informationen finden Sie unter Gewusst [wie: Binden eines Windows Forms Steuer Elements an einen Typ](how-to-bind-a-windows-forms-control-to-a-type.md). Anschließend können Sie zur Laufzeit eine Bindung an ein Objekt herstellen.  
  
### <a name="currency-management"></a>Währungsverwaltung  
 Die- <xref:System.Windows.Forms.BindingSource> Komponente implementiert die- <xref:System.Windows.Forms.ICurrencyManagerProvider> Schnittstelle, um die Währungsverwaltung für Sie zu verarbeiten. Mit der- <xref:System.Windows.Forms.ICurrencyManagerProvider> Schnittstelle können Sie auch auf den Currency Manager für einen zugreifen <xref:System.Windows.Forms.BindingSource> , zusätzlich zum Currency Manager für einen anderen, <xref:System.Windows.Forms.BindingSource> der an denselben gebunden ist <xref:System.Windows.Forms.BindingSource.DataMember%2A> .  
  
 Die <xref:System.Windows.Forms.BindingSource> Komponente kapselt <xref:System.Windows.Forms.CurrencyManager> Funktionen und macht die gängigsten <xref:System.Windows.Forms.CurrencyManager> Eigenschaften und Ereignisse verfügbar. In der folgenden Tabelle werden einige der Mitglieder im Zusammenhang mit der Währungsverwaltung beschrieben.  
  
 <xref:System.Windows.Forms.ICurrencyManagerProvider.CurrencyManager%2A> -Eigenschaft  
 Ruft den Currency Manager ab, der dem zugeordnet ist <xref:System.Windows.Forms.BindingSource> .  
  
 <xref:System.Windows.Forms.ICurrencyManagerProvider.GetRelatedCurrencyManager%2A>-Methode  
 Wenn eine andere <xref:System.Windows.Forms.BindingSource> an den angegebenen Datenmember gebunden ist, wird der zugehörige Currency Manager abgerufen.  
  
 <xref:System.Windows.Forms.BindingSource.Current%2A> -Eigenschaft  
 Ruft das aktuelle Element der Datenquelle ab.  
  
 <xref:System.Windows.Forms.BindingSource.Position%2A> -Eigenschaft  
 Ruft die aktuelle Position in der zugrunde liegenden Liste ab oder legt diese fest.  
  
 <xref:System.Windows.Forms.BindingSource.EndEdit%2A>-Methode  
 Wendet anstehende Änderungen auf die zugrunde liegende Datenquelle an.  
  
 <xref:System.Windows.Forms.BindingSource.CancelEdit%2A>-Methode  
 Bricht den aktuellen Bearbeitungsvorgang ab.  
  
### <a name="data-source-as-a-list"></a>Datenquelle als Liste  
 Die <xref:System.Windows.Forms.BindingSource> -Komponente implementiert die <xref:System.ComponentModel.IBindingListView> -und- <xref:System.ComponentModel.ITypedList> Schnittstellen. Mit dieser Implementierung können Sie die <xref:System.Windows.Forms.BindingSource> Komponente selbst als Datenquelle ohne externen Speicher verwenden.  
  
 Wenn die <xref:System.Windows.Forms.BindingSource> Komponente an eine Datenquelle angefügt ist, wird die Datenquelle als Liste verfügbar gemacht.  
  
 Die- <xref:System.Windows.Forms.BindingSource.DataSource%2A> Eigenschaft kann auf mehrere Datenquellen festgelegt werden. Dazu zählen Typen, Objekte und Listen von Typen. Die resultierende Datenquelle wird als Liste verfügbar gemacht. In der folgenden Tabelle sind einige der allgemeinen Datenquellen und die resultierende Listen Auswertung aufgeführt.  
  
|DataSource-Eigenschaft|Ergebnisse auflisten|  
|-------------------------|------------------|  
|Ein NULL-Verweis (`Nothing` in Visual Basic).|Ein leeres <xref:System.ComponentModel.IBindingList> von-Objekten. Durch das Hinzufügen eines Elements wird die Liste auf den Typ des hinzugefügten Elements festgelegt.|  
|Ein NULL-Verweis ( `Nothing` in Visual Basic) mit <xref:System.Windows.Forms.BindingSource.DataMember%2A> Set|Nicht unterstützt. löst aus <xref:System.ArgumentException> .|  
|Non-List-Typ oder-Objekt vom Typ "T"|Ein leeres <xref:System.ComponentModel.IBindingList> vom Typ "T".|  
|Array Instanz|Ein, <xref:System.ComponentModel.IBindingList> das die Array Elemente enthält.|  
|<xref:System.Collections.IEnumerable> lichen|Eine, <xref:System.ComponentModel.IBindingList> die die Elemente enthält. <xref:System.Collections.IEnumerable>|  
|Listen Instanz mit dem Typ "T"|Eine-Instanz, die den <xref:System.ComponentModel.IBindingList> Typ "T" enthält.|  
  
 Außerdem <xref:System.Windows.Forms.BindingSource.DataSource%2A> kann auf andere Listen Typen, z. b. und, festgelegt werden <xref:System.ComponentModel.IListSource> <xref:System.ComponentModel.ITypedList> , und der <xref:System.Windows.Forms.BindingSource> verarbeitet sie entsprechend. In diesem Fall sollte der in der Liste enthaltene Typ über einen Parameter losen Konstruktor verfügen.  
  
### <a name="bindingsource-as-an-ibindinglist"></a>BindingSource als IBindingList  
 Die <xref:System.Windows.Forms.BindingSource> Komponente stellt Member für den Zugriff auf und die Bearbeitung der zugrunde liegenden Daten als dar <xref:System.ComponentModel.IBindingList> . In der folgenden Tabelle werden einige dieser Member beschrieben.  
  
|Member|BESCHREIBUNG|  
|------------|-----------------|  
|<xref:System.Windows.Forms.BindingSource.List%2A> -Eigenschaft|Ruft die Liste ab, die sich aus der Auswertung der-Eigenschaft oder der-Eigenschaft ergibt <xref:System.Windows.Forms.BindingSource.DataSource%2A> <xref:System.Windows.Forms.BindingSource.DataMember%2A> .|  
|<xref:System.Windows.Forms.BindingSource.AddNew%2A>-Methode|Fügt der zugrunde liegenden Liste ein neues Element hinzu. Gilt für Datenquellen, die die <xref:System.ComponentModel.IBindingList> -Schnittstelle implementieren und das Hinzufügen von Elementen zulassen (das heißt, die- <xref:System.Windows.Forms.BindingSource.AllowNew%2A> Eigenschaft ist auf festgelegt `true` ).|  
  
### <a name="custom-item-creation"></a>Erstellung benutzerdefinierter Elemente  
 Sie können das- <xref:System.Windows.Forms.BindingSource.AddingNew> Ereignis behandeln, um eine eigene Logik zur Element Erstellung bereitzustellen. Das- <xref:System.Windows.Forms.BindingSource.AddingNew> Ereignis tritt auf, bevor ein neues-Objekt hinzugefügt wird <xref:System.Windows.Forms.BindingSource> . Dieses Ereignis wird ausgelöst, nachdem die- <xref:System.Windows.Forms.BindingSource.AddNew%2A> Methode aufgerufen wurde, aber bevor das neue Element der zugrunde liegenden Liste hinzugefügt wird. Durch die Behandlung dieses Ereignisses können Sie benutzerdefiniertes Element Erstellungs Verhalten bereitstellen, ohne von der Klasse abgeleitet zu werden <xref:System.Windows.Forms.BindingSource> . Weitere Informationen finden Sie unter Gewusst [wie: Anpassen des Hinzufügens von Elementen mit dem Windows Forms BindingSource](how-to-customize-item-addition-with-the-windows-forms-bindingsource.md).  
  
### <a name="transactional-item-creation"></a>Transaktions Element Erstellung  
 Die- <xref:System.Windows.Forms.BindingSource> Komponente implementiert die- <xref:System.ComponentModel.ICancelAddNew> Schnittstelle, die das Erstellen von transaktionalen Elementen ermöglicht. Nachdem ein neues Element mithilfe eines Aufrufens von vorläufig erstellt wurde <xref:System.Windows.Forms.BindingSource.AddNew%2A> , kann auf folgende Weise ein Commit oder ein Rollback für die Addition ausgeführt werden:  
  
- Die- <xref:System.ComponentModel.ICancelAddNew.EndNew%2A> Methode führt einen expliziten Commit für die ausstehende Addition aus.  
  
- Durch das Ausführen eines weiteren Auflistungs Vorgangs (z. b. einfügen, entfernen oder verschieben) wird die ausstehende Addition implizit committ.  
  
- Die <xref:System.ComponentModel.ICancelAddNew.CancelNew%2A> Methode führt ein Rollback für die ausstehende Addition aus, wenn für die Methode nicht bereits ein Commit ausgeführt wurde.  
  
### <a name="ienumerable-support"></a>IEnumerable-Unterstützung  
 Die- <xref:System.Windows.Forms.BindingSource> Komponente ermöglicht das Binden von Steuerelementen an <xref:System.Collections.IEnumerable> Datenquellen. Mit dieser Komponente können Sie eine Bindung an eine Datenquelle, z. b. eine, herstellen <xref:System.Data.SqlClient.SqlDataReader?displayProperty=nameWithType> .  
  
 Wenn <xref:System.Collections.IEnumerable> der Komponente eine Datenquelle zugewiesen ist <xref:System.Windows.Forms.BindingSource> , wird von <xref:System.Windows.Forms.BindingSource> eine erstellt <xref:System.ComponentModel.IBindingList> und der Liste der Inhalt der <xref:System.Collections.IEnumerable> Datenquelle hinzugefügt.  
  
### <a name="design-time-support"></a>Design-Time Unterstützung  
 Einige Objekttypen können nicht zur Entwurfszeit erstellt werden, z. b. Objekte, die aus einer Factoryklasse erstellt wurden, oder von einem Webdienst zurückgegebene Objekte. Manchmal müssen Sie Ihre Steuerelemente zur Entwurfszeit an diese Typen binden, auch wenn kein Objekt im Speicher vorhanden ist, an das die Steuerelemente gebunden werden können. Sie können z. b. die Spaltenkopfzeilen eines <xref:System.Windows.Forms.DataGridView> -Steuer Elements mit den Namen der öffentlichen Eigenschaften des benutzerdefinierten Typs bezeichnen.  
  
 Zur Unterstützung dieses Szenarios <xref:System.Windows.Forms.BindingSource> unterstützt die-Komponente die Bindung an <xref:System.Type> . Wenn Sie der- <xref:System.Type> Eigenschaft ein- <xref:System.Windows.Forms.BindingSource.DataSource%2A> Objekt zuweisen, <xref:System.Windows.Forms.BindingSource> erstellt die Komponente eine leere <xref:System.ComponentModel.BindingList%601> von <xref:System.Type> Elementen. Alle Steuerelemente, die Sie anschließend an die <xref:System.Windows.Forms.BindingSource> Komponente binden, werden zur Entwurfszeit oder zur Laufzeit gewarnt, wenn die Eigenschaften oder das Schema Ihres Typs vorhanden sind. Weitere Informationen finden Sie unter Gewusst [wie: Binden eines Windows Forms Steuer Elements an einen Typ](how-to-bind-a-windows-forms-control-to-a-type.md).  
  
### <a name="static-listbindinghelper-methods"></a>Statische ListBindingHelper-Methoden  
 Die <xref:System.Windows.Forms.BindingContext?displayProperty=nameWithType> <xref:System.Windows.Forms.CurrencyManager?displayProperty=nameWithType> Typen, und <xref:System.Windows.Forms.BindingSource> haben alle gemeinsame Logik, um eine Liste aus einem Paar zu generieren `DataSource` / `DataMember` . Außerdem wird diese gängige Logik öffentlich zur Verwendung durch Autoren von Steuerelementen und anderen Drittanbietern in den folgenden `static` Methoden bereitgestellt:  
  
- <xref:System.Windows.Forms.ListBindingHelper.GetListItemProperties%2A>  
  
- <xref:System.Windows.Forms.ListBindingHelper.GetList%2A>.  
  
- <xref:System.Windows.Forms.ListBindingHelper.GetListName%2A>  
  
- <xref:System.Windows.Forms.ListBindingHelper.GetListItemType%2A>  
  
### <a name="sorting-and-filtering-with-the-ibindinglistview-interface"></a>Sortieren und Filtern mit der IBindingListView-Schnittstelle  
 Die- <xref:System.Windows.Forms.BindingSource> Komponente implementiert die- <xref:System.ComponentModel.IBindingListView> Schnittstelle, die die- <xref:System.ComponentModel.IBindingList> Schnittstelle erweitert. <xref:System.ComponentModel.IBindingList>Bietet eine Sortierung mit einer einzelnen Spalte und <xref:System.ComponentModel.IBindingListView> bietet erweiterte Sortier-und Filterfunktionen. Mit <xref:System.ComponentModel.IBindingListView> können Sie Elemente in der Datenquelle sortieren und Filtern, wenn die Datenquelle auch eine dieser Schnittstellen implementiert. Die <xref:System.Windows.Forms.BindingSource> Komponente stellt keine Verweis Implementierung dieser Member bereit. Stattdessen werden Aufrufe an die zugrunde liegende Liste weitergeleitet.  
  
 In der folgenden Tabelle werden die Eigenschaften beschrieben, die Sie zum Sortieren und Filtern verwenden.  
  
|Member|BESCHREIBUNG|  
|------------|-----------------|  
|<xref:System.Windows.Forms.BindingSource.Filter%2A> -Eigenschaft|Wenn die Datenquelle eine <xref:System.ComponentModel.IBindingListView> ist, wird der Ausdruck abgerufen, der zum Filtern der anzuzeigenden Zeilen verwendet wird, oder dieser Ausdruck wird festgelegt.|  
|<xref:System.Windows.Forms.BindingSource.Sort%2A> -Eigenschaft|Wenn die Datenquelle eine <xref:System.ComponentModel.IBindingList> ist, wird ein Spaltenname abgerufen oder festgelegt, der für das Sortieren und für Informationen zur Sortierreihenfolge verwendet wird.<br /><br /> Oder<br /><br /> Wenn die Datenquelle eine ist <xref:System.ComponentModel.IBindingListView> und erweiterte Sortierung unterstützt, werden mehrere Spaltennamen abgerufen, die für Sortierung und Sortierreihenfolge verwendet werden.|  
  
### <a name="integration-with-bindingnavigator"></a>Integration in BindingNavigator  
 Sie können die- <xref:System.Windows.Forms.BindingSource> Komponente verwenden, um beliebige Windows Forms Steuerelemente an eine Datenquelle zu binden, aber das- <xref:System.Windows.Forms.BindingNavigator> Steuerelement ist speziell für die Arbeit mit der- <xref:System.Windows.Forms.BindingSource> Komponente konzipiert. Das <xref:System.Windows.Forms.BindingNavigator> -Steuerelement stellt eine Benutzeroberfläche zum Steuern des <xref:System.Windows.Forms.BindingSource> aktuellen Elements der Komponente bereit. Standardmäßig stellt das <xref:System.Windows.Forms.BindingNavigator> Steuerelement Schaltflächen bereit, die den Navigationsmethoden der <xref:System.Windows.Forms.BindingSource> Komponente entsprechen. Weitere Informationen finden Sie unter Gewusst [wie: Navigieren in Daten mit dem Windows Forms BindingNavigator-Steuer](how-to-navigate-data-with-the-windows-forms-bindingnavigator-control.md)Element.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.BindingSource>
- <xref:System.Windows.Forms.BindingNavigator>
- [Übersicht über die BindingSource-Komponente](bindingsource-component-overview.md)
- [BindingNavigator-Steuerelement](bindingnavigator-control-windows-forms.md)
- [Datenbindung in Web Forms](../windows-forms-data-binding.md)
- [Steuerelemente für Windows Forms](controls-to-use-on-windows-forms.md)
- [Vorgehensweise: Binden eines Windows Forms-Steuerelements an einen Typ](how-to-bind-a-windows-forms-control-to-a-type.md)
- [Vorgehensweise: Kennzeichnen von Datenquellenaktualisierungen in einem Windows Forms-Steuerelement mithilfe der BindingSource](reflect-data-source-updates-in-a-wf-control-with-the-bindingsource.md)
