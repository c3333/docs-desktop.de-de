---
title: Auf Datenbindung bezogene Schnittstellen
ms.date: 03/30/2017
ms.topic: overview
helpviewer_keywords:
- data [Windows Forms], data-binding interfaces
- INotifyPropertyChanged interface
- IBindingListView interface
- IList interface [Windows Forms], Windows Forms data binding
- IBindingList interface [Windows Forms], Windows Forms data binding
- interfaces [Windows Forms], Windows Forms data binding
- IEditableObject interface [Windows Forms], Windows Forms data binding
- data binding [Windows Forms], interfaces
- IDataErrorInfo interface [Windows Forms], Windows Forms data binding
ms.assetid: 14e49a2e-3e46-47ca-b491-70d546333277
ms.openlocfilehash: 779b3f755d57014996af042d24236135293ce8ed
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976883"
---
# <a name="interfaces-related-to-data-binding"></a>Auf Datenbindung bezogene Schnittstellen

Mit ADO.net können Sie viele verschiedene Datenstrukturen erstellen, die den Bindungs Anforderungen Ihrer Anwendung und der Daten entsprechen, mit denen Sie arbeiten. Möglicherweise möchten Sie eigene Klassen erstellen, die Daten in Windows Forms bereitstellen oder verwenden. Diese Objekte können ein unterschiedliches Maß an Funktionalität und Komplexität bieten, von der Basisdatenbindung bis hin zur Bereitstellung der Unterstützung während der Entwurfszeit, Überprüfung von Fehlern, Benachrichtigung oder sogar Unterstützung für eine strukturierte Zurücksetzung der an den Daten selbst vorgenommenen Änderungen.

## <a name="consumers-of-data-binding-interfaces"></a>Consumer von Datenbindungsschnittstellen

In den folgenden Abschnitten werden zwei Gruppen von Schnittstellen Objekten beschrieben. Die erste Gruppe sind die Schnittstellen, die von Datenquellenautoren für Datenquellen implementiert werden. Diese Schnittstellen sollen von Datenquellenconsumern genutzt werden, die in den meisten Fällen Windows Forms-Steuerelemente oder Komponenten sind. Die zweite Gruppe bilden die Schnittstellen, die für die Verwendung durch Komponentenautoren vorgesehen sind. Komponentenautoren verwenden diese Schnittstellen, wenn sie eine Komponente erstellen, die die von der Windows Forms-Datenbindungs-Engine zu nutzende Datenbindung unterstützt. Sie können diese Schnittstellen in Klassen im Zusammenhang mit dem Formular implementieren, um die Datenbindung zu aktivieren. Jeder Fall stellt eine Klasse dar, die eine Schnittstelle implementiert, die die Interaktion mit Daten ermöglicht. Die Tools für die Entwicklung von Daten in Visual Studio (Rapid Application Development, Rad) nutzen diese Funktionen bereits.

### <a name="interfaces-for-implementation-by-data-source-authors"></a>Schnittstellen für die Implementierung von Datenquellenautoren

Die folgenden Schnittstellen sollen von Windows Forms-Steuerelementen genutzt werden:

- <xref:System.Collections.IList>-Schnittstelle

  Eine Klasse, die die- <xref:System.Collections.IList> Schnittstelle implementiert, kann <xref:System.Array> , oder sein <xref:System.Collections.ArrayList> <xref:System.Collections.CollectionBase> . Dabei handelt es sich um indizierte Listen von Elementen des Typs <xref:System.Object> . Diese Listen müssen homogene Typen enthalten, da das erste Element des Index den Typ bestimmt. <xref:System.Collections.IList> steht nur zur Laufzeit für die Bindung zur Verfügung.

  > [!NOTE]
  > Wenn Sie eine Liste von Geschäftsobjekten für die Bindung mit Windows Forms erstellen möchten, sollten Sie die Verwendung des-Objekts in Erwägung gezogen <xref:System.ComponentModel.BindingList%601> . <xref:System.ComponentModel.BindingList%601>Ist eine erweiterbare Klasse, die die primären Schnittstellen implementiert, die für die bidirektionale Windows Forms Datenbindung erforderlich sind.

- <xref:System.ComponentModel.IBindingList>-Schnittstelle

  Eine Klasse, die die <xref:System.ComponentModel.IBindingList> -Schnittstelle implementiert, bietet ein viel höheres Maß an Daten Bindungs Funktionalität. Diese Implementierung bietet Ihnen die grundlegenden Sortierfunktionen und Änderungsbenachrichtigung für Änderungen der Listenelemente (z.B. wenn das Feld Adresse des dritten Elements in einer Liste von Kunden geändert wurde) und für Änderungen der Liste selbst (z.B. wenn die Anzahl der Elemente in der Liste erhöht oder verringert wird). Änderungsbenachrichtigungen sind wichtig, wenn mehrere Steuerelemente an dieselben Daten gebunden und Datenänderungen in einem der Steuerelemente vorgenommen werden sollen, die an die anderen gebundenen Steuerelemente weitergegeben werden sollen.

  > [!NOTE]
  > Die Änderungs Benachrichtigung wird für die- <xref:System.ComponentModel.IBindingList> Schnittstelle durch die-Eigenschaft aktiviert, <xref:System.ComponentModel.IBindingList.SupportsChangeNotification%2A> die, wenn `true` , ein- <xref:System.ComponentModel.IBindingList.ListChanged> Ereignis auslöst, das angibt, dass die Liste geändert oder ein Element in der Liste geändert wurde.

  Der Typ der Änderung wird von der- <xref:System.ComponentModel.ListChangedType> Eigenschaft des- <xref:System.ComponentModel.ListChangedEventArgs> Parameters beschrieben. Wenn das Datenmodell aktualisiert wird, werden daher alle abhängigen Ansichten, wie z.B. andere Steuerelemente, die an die gleiche Datenquelle gebunden sind, ebenfalls aktualisiert. In der Liste enthaltene Objekte müssen die Liste jedoch Benachrichtigen, wenn Sie sich ändern, sodass die Liste das Ereignis ausgeben kann <xref:System.ComponentModel.IBindingList.ListChanged> .

  > [!NOTE]
  > <xref:System.ComponentModel.BindingList%601>Stellt eine generische Implementierung der- <xref:System.ComponentModel.IBindingList> Schnittstelle bereit.

- <xref:System.ComponentModel.IBindingListView>-Schnittstelle

  Eine Klasse, die die- <xref:System.ComponentModel.IBindingListView> Schnittstelle implementiert, bietet alle Funktionen einer Implementierung von <xref:System.ComponentModel.IBindingList> sowie Filter und erweiterte Sortierfunktionen. Diese Implementierung bietet zeichenfolgenbasierte Filterung und die mehrspaltige Sortierung mit Eigenschaftendeskriptor-Richtungspaaren.

- <xref:System.ComponentModel.IEditableObject>-Schnittstelle

  Eine Klasse, die die- <xref:System.ComponentModel.IEditableObject> Schnittstelle implementiert, ermöglicht einem Objekt, zu steuern, wann Änderungen an diesem Objekt dauerhaft gemacht werden. Diese Implementierung bietet Ihnen die <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> <xref:System.ComponentModel.IEditableObject.EndEdit%2A> Methoden, und <xref:System.ComponentModel.IEditableObject.CancelEdit%2A> , mit denen Sie die an dem Objekt vorgenommenen Änderungen zurücksetzen können. Im folgenden finden Sie eine kurze Erläuterung der Funktionsweise <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> der <xref:System.ComponentModel.IEditableObject.EndEdit%2A> Methoden, und <xref:System.ComponentModel.IEditableObject.CancelEdit%2A> und deren Funktionsweise in Verbindung mit einander, um ein mögliches Rollback der an den Daten vorgenommenen Änderungen zu ermöglichen:

  - Die- <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> Methode signalisiert den Anfang einer Bearbeitung für ein-Objekt. Ein Objekt, das diese Schnittstelle implementiert, muss alle Updates nach dem <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> Methodenaufruf so speichern, dass die Aktualisierungen verworfen werden können, wenn die- <xref:System.ComponentModel.IEditableObject.CancelEdit%2A> Methode aufgerufen wird. In Daten Bindungs Windows Forms können Sie mehrmals innerhalb des Gültigkeits <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> Bereichs einer einzelnen Bearbeitungs Transaktion (z. b., <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> , <xref:System.ComponentModel.IEditableObject.EndEdit%2A> ) aufgerufen werden. Implementierungen von <xref:System.ComponentModel.IEditableObject> sollten nachverfolgen, ob <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> bereits aufgerufen wurde, und nachfolgende Aufrufe von ignorieren <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> . Da diese Methode mehrmals aufgerufen werden kann, ist es wichtig, dass nachfolgende Aufrufe an diese nicht destruktiv sind. Das heißt, dass nachfolgende <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> Aufrufe die Updates, die durchgeführt wurden, nicht zerstören oder die beim ersten Aufruf gespeicherten Daten geändert haben <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> .

  - Die- <xref:System.ComponentModel.IEditableObject.EndEdit%2A> Methode überträgt alle Änderungen seit dem Aufruf <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> in das zugrunde liegende-Objekt, wenn sich das Objekt derzeit im Bearbeitungsmodus befindet.

  - Die- <xref:System.ComponentModel.IEditableObject.CancelEdit%2A> Methode verwirft alle an dem-Objekt vorgenommenen Änderungen.

  Weitere Informationen zur Funktionsweise der <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> <xref:System.ComponentModel.IEditableObject.EndEdit%2A> Methoden, und <xref:System.ComponentModel.IEditableObject.CancelEdit%2A> finden [Sie unter Speichern von Daten in der Datenbank](/visualstudio/data-tools/save-data-back-to-the-database).

  Dieses Transaktions Konzept der Daten Funktionalität wird vom-Steuerelement verwendet <xref:System.Windows.Forms.DataGridView> .

- <xref:System.ComponentModel.ICancelAddNew>-Schnittstelle

  Eine Klasse, die die- <xref:System.ComponentModel.ICancelAddNew> Schnittstelle implementiert, Implementiert in der Regel die <xref:System.ComponentModel.IBindingList> -Schnittstelle und ermöglicht es Ihnen, eine Addition für die Datenquelle mit der-Methode zurückzusetzen <xref:System.ComponentModel.IBindingList.AddNew%2A> . Wenn die Datenquelle die- <xref:System.ComponentModel.IBindingList> Schnittstelle implementiert, sollte Sie auch die- <xref:System.ComponentModel.ICancelAddNew> Schnittstelle implementieren.

- <xref:System.ComponentModel.IDataErrorInfo>-Schnittstelle

  Eine Klasse, die die- <xref:System.ComponentModel.IDataErrorInfo> Schnittstelle implementiert, ermöglicht es Objekten, gebundenen Steuerelementen benutzerdefinierte Fehlerinformationen bereitzustellen:

  - Die- <xref:System.ComponentModel.IDataErrorInfo.Error%2A> Eigenschaft gibt den allgemeinen Fehlermeldungs Text zurück (z. b. "ein Fehler ist aufgetreten").

  - Die- <xref:System.ComponentModel.IDataErrorInfo.Item%2A> Eigenschaft gibt eine Zeichenfolge mit der angegebenen Fehlermeldung aus der Spalte zurück (z. b. "der Wert in der `State` Spalte ist ungültig").

- <xref:System.Collections.IEnumerable>-Schnittstelle

  Eine Klasse, die die- <xref:System.Collections.IEnumerable> Schnittstelle implementiert, wird in der Regel von ASP.net genutzt. Windows Forms Unterstützung für diese Schnittstelle ist nur über die- <xref:System.Windows.Forms.BindingSource> Komponente verfügbar.

  > [!NOTE]
  > Die <xref:System.Windows.Forms.BindingSource> Komponente kopiert alle <xref:System.Collections.IEnumerable> Elemente zu Bindungs Zwecken in eine separate Liste.

- <xref:System.ComponentModel.ITypedList>-Schnittstelle

  Eine Auflistungs Klasse, die die- <xref:System.ComponentModel.ITypedList> Schnittstelle implementiert, bietet die Möglichkeit, die Reihenfolge und den Satz von Eigenschaften zu steuern, die für das gebundene Steuerelement

  > [!NOTE]
  > Wenn Sie die <xref:System.ComponentModel.ITypedList.GetItemProperties%2A> -Methode implementieren und das <xref:System.ComponentModel.PropertyDescriptor> Array nicht NULL ist, ist der letzte Eintrag im Array der Eigenschaften Deskriptor, der die Listen Eigenschaft beschreibt, bei der es sich um eine weitere Liste von Elementen handelt.

- <xref:System.ComponentModel.ICustomTypeDescriptor>-Schnittstelle

  Eine Klasse, die die- <xref:System.ComponentModel.ICustomTypeDescriptor> Schnittstelle implementiert, stellt dynamische Informationen über sich selbst bereit. Diese Schnittstelle ähnelt, <xref:System.ComponentModel.ITypedList> wird jedoch anstelle von Listen für-Objekte verwendet. Diese Schnittstelle wird von verwendet <xref:System.Data.DataRowView> , um das Schema der zugrunde liegenden Zeilen zu projizieren. Eine einfache Implementierung von <xref:System.ComponentModel.ICustomTypeDescriptor> wird von der- <xref:System.ComponentModel.CustomTypeDescriptor> Klasse bereitgestellt.

  > [!NOTE]
  > Zur Unterstützung der Entwurfszeit Bindung an Typen, die implementieren <xref:System.ComponentModel.ICustomTypeDescriptor> , muss der Typ auch implementieren <xref:System.ComponentModel.IComponent> und als-Instanz im Formular vorhanden sein.

- <xref:System.ComponentModel.IListSource>-Schnittstelle

  Eine Klasse, die die <xref:System.ComponentModel.IListSource> -Schnittstelle implementiert, ermöglicht eine Listen basierte Bindung für nicht-Listen Objekte. Die- <xref:System.ComponentModel.IListSource.GetList%2A> Methode von <xref:System.ComponentModel.IListSource> wird verwendet, um eine bindbare Liste von einem Objekt zurückzugeben, das nicht von erbt <xref:System.Collections.IList> . <xref:System.ComponentModel.IListSource> wird von der- <xref:System.Data.DataSet> Klasse verwendet.

- <xref:System.ComponentModel.IRaiseItemChangedEvents>-Schnittstelle

  Eine Klasse, die die- <xref:System.ComponentModel.IRaiseItemChangedEvents> Schnittstelle implementiert, ist eine bindbare Liste, die auch die- <xref:System.ComponentModel.IBindingList> Schnittstelle implementiert. Diese Schnittstelle wird verwendet, um anzugeben, ob der Typ <xref:System.ComponentModel.IBindingList.ListChanged> durch die-Eigenschaft Ereignisse vom Typ auslöst <xref:System.ComponentModel.ListChangedType.ItemChanged> <xref:System.ComponentModel.IRaiseItemChangedEvents.RaisesItemChangedEvents%2A> .

  > [!NOTE]
  > Sie sollten die implementieren <xref:System.ComponentModel.IRaiseItemChangedEvents> , wenn Ihre Datenquelle die-Eigenschaft bereitstellt, um die zuvor beschriebene Ereignis Konvertierung aufzulisten und mit der-Komponente zu interagieren <xref:System.Windows.Forms.BindingSource> . Andernfalls führt der <xref:System.Windows.Forms.BindingSource> auch die-Eigenschaft zum Auflisten der Ereignis Konvertierung aus, was zu einer langsameren Leistung führt.

- <xref:System.ComponentModel.ISupportInitialize>-Schnittstelle

  Eine Komponente, die die- <xref:System.ComponentModel.ISupportInitialize> Schnittstelle implementiert, nutzt die Vorteile von Batch Optimierungen zum Festlegen von Eigenschaften und zum Initialisieren von Co-abhängigen Eigenschaften. Der <xref:System.ComponentModel.ISupportInitialize> enthält zwei Methoden:

  - <xref:System.ComponentModel.ISupportInitialize.BeginInit%2A> signalisiert, dass die Objekt Initialisierung gestartet wird.

  - <xref:System.ComponentModel.ISupportInitialize.EndInit%2A> signalisiert, dass die Objekt Initialisierung abgeschlossen ist.

- <xref:System.ComponentModel.ISupportInitializeNotification>-Schnittstelle

  Eine Komponente, die die <xref:System.ComponentModel.ISupportInitializeNotification> Schnittstelle implementiert, implementiert auch die- <xref:System.ComponentModel.ISupportInitialize> Schnittstelle. Mit dieser Schnittstelle können Sie andere <xref:System.ComponentModel.ISupportInitialize> Komponenten Benachrichtigen, dass die Initialisierung beendet ist. Die- <xref:System.ComponentModel.ISupportInitializeNotification> Schnittstelle enthält zwei Member:

  - <xref:System.ComponentModel.ISupportInitializeNotification.IsInitialized%2A> Gibt einen `boolean` Wert zurück, der angibt, ob die Komponente initialisiert ist.

  - <xref:System.ComponentModel.ISupportInitializeNotification.Initialized> Tritt auf, wenn <xref:System.ComponentModel.ISupportInitialize.EndInit%2A> aufgerufen wird.

- <xref:System.ComponentModel.INotifyPropertyChanged>-Schnittstelle

  Eine Klasse, die diese Schnittstelle implementiert, ist ein Typ, der ein Ereignis auslöst, wenn sich einer der Eigenschaftswerte ändert. Diese Schnittstelle soll das Muster ersetzen, dass für jede Eigenschaft eines Steuerelements ein Änderungsereignis vorhanden ist. Wenn ein Geschäftsobjekt in einem verwendet wird <xref:System.ComponentModel.BindingList%601> , sollte die <xref:System.ComponentModel.INotifyPropertyChanged> -Schnittstelle implementiert werden, und die BindingList \` 1 konvertiert <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> Ereignisse in <xref:System.ComponentModel.BindingList%601.ListChanged> Ereignisse vom Typ <xref:System.ComponentModel.ListChangedType.ItemChanged> .

  > [!NOTE]
  > Damit die Änderungs Benachrichtigung in einer Bindung zwischen einem gebundenen Client und einer Datenquelle auftritt, muss der gebundene Daten Quellentyp entweder die- <xref:System.ComponentModel.INotifyPropertyChanged> Schnittstelle implementieren (bevorzugt), oder Sie können *propertyName* - `Changed` Ereignisse für den gebundenen Typ bereitstellen, aber Sie sollten nicht beides tun.

### <a name="interfaces-for-implementation-by-component-authors"></a>Schnittstellen für die Implementierung von Komponentenautoren

Die folgenden Schnittstellen sind für die Nutzung durch die Windows Forms-Datenbindungs-Engine ausgelegt:

- <xref:System.Windows.Forms.IBindableComponent>-Schnittstelle

  Eine Klasse, die diese Schnittstelle implementiert, ist eine Nichtsteuerungskomponente, die die Datenbindung unterstützt. Diese Klasse gibt die Daten Bindungen und den Bindungs Kontext der Komponente über die <xref:System.Windows.Forms.IBindableComponent.DataBindings%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.IBindableComponent.BindingContext%2A> dieser Schnittstelle zurück.

  > [!NOTE]
  > Wenn die Komponente von erbt <xref:System.Windows.Forms.Control> , müssen Sie die- <xref:System.Windows.Forms.IBindableComponent> Schnittstelle nicht implementieren.

- <xref:System.Windows.Forms.ICurrencyManagerProvider>-Schnittstelle

  Eine Klasse, die die- <xref:System.Windows.Forms.ICurrencyManagerProvider> Schnittstelle implementiert, ist eine Komponente, die eine eigene bereitstellt, <xref:System.Windows.Forms.CurrencyManager> um die dieser speziellen Komponente zugeordneten Bindungen zu verwalten. Der Zugriff auf die benutzerdefinierte <xref:System.Windows.Forms.CurrencyManager> wird von der-Eigenschaft bereitgestellt <xref:System.Windows.Forms.ICurrencyManagerProvider.CurrencyManager%2A> .

  > [!NOTE]
  > Eine Klasse, die von erbt <xref:System.Windows.Forms.Control> , verwaltet Bindungen automatisch über Ihre- <xref:System.Windows.Forms.Control.BindingContext%2A> Eigenschaft. Daher sind Fälle, in denen Sie implementieren müssen, <xref:System.Windows.Forms.ICurrencyManagerProvider> relativ selten.

## <a name="see-also"></a>Siehe auch

- [Datenbindung und Windows Forms](data-binding-and-windows-forms.md)
- [Vorgehensweise: Erstellen eines einfach gebundenen Steuerelements in einer Windows Forms-Instanz](how-to-create-a-simple-bound-control-on-a-windows-form.md)
- [Datenbindung in Web Forms](windows-forms-data-binding.md)
