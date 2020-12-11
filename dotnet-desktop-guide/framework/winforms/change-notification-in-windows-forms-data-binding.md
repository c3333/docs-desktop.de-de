---
title: Ändern der Benachrichtigung in der Datenbindung
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, data binding
- Windows Forms, adding change notification for data binding
ms.assetid: b5b10f90-0585-41d9-a377-409835262a92
ms.openlocfilehash: 2dffea46bf0db54d28ef55e507767d88bd29ebc2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975807"
---
# <a name="change-notification-in-windows-forms-data-binding"></a>Änderungsbenachrichtigung in der Windows Forms-Datenbindung
Eines der wichtigsten Konzepte von Windows Forms Datenbindung ist die *Änderungs Benachrichtigung*. Um sicherzustellen, dass Ihre Datenquelle und gebundene Steuerelemente immer über die aktuellsten Daten verfügen, müssen Sie eine Änderungs Benachrichtigung für die Datenbindung hinzufügen. Insbesondere sollten Sie sicherstellen, dass gebundene Steuerelemente über Änderungen benachrichtigt werden, die an der Datenquelle vorgenommen wurden, und dass die Datenquelle über Änderungen benachrichtigt wird, die an den gebundenen Eigenschaften eines Steuer Elements vorgenommen wurden.  
  
 Es gibt verschiedene Arten von Änderungs Benachrichtigungen, abhängig von der Art der Datenbindung:  
  
- Einfache Bindung, bei der eine einzelne Steuerelement Eigenschaft an eine einzelne Instanz eines Objekts gebunden ist.  
  
- Listen basierte Bindung, die eine einzelne Steuerelement Eigenschaft enthalten kann, die an die-Eigenschaft eines Elements in einer Liste gebunden ist, oder eine Steuerelement Eigenschaft, die an eine Liste von-Objekten gebunden ist.  
  
 Wenn Sie Windows Forms Steuerelemente erstellen, die Sie für die Datenbindung verwenden möchten, müssen Sie das Muster *propertyName* Changed auf die Steuerelemente anwenden, damit Änderungen an der gebundenen Eigenschaft eines Steuer Elements an die Datenquelle weitergegeben werden.  
  
## <a name="change-notification-for-simple-binding"></a>Änderungs Benachrichtigung für einfache Bindung  
 Bei einer einfachen Bindung müssen Geschäftsobjekte eine Änderungs Benachrichtigung bereitstellen, wenn der Wert einer gebundenen Eigenschaft geändert wird. Hierzu können Sie ein *propertyName* Changed-Ereignis für jede Eigenschaft Ihres Geschäftsobjekts verfügbar machen und das Geschäftsobjekt an Steuerelemente mit dem <xref:System.Windows.Forms.BindingSource> oder der bevorzugten Methode binden, in der das Geschäftsobjekt die <xref:System.ComponentModel.INotifyPropertyChanged> -Schnittstelle implementiert, und ein-Ereignis auslösen, <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> Wenn sich der Wert einer Eigenschaft ändert. Weitere Informationen finden Sie unter Gewusst [wie: Implementieren der INotifyPropertyChanged-Schnittstelle](how-to-implement-the-inotifypropertychanged-interface.md). Wenn Sie Objekte verwenden, die die- <xref:System.ComponentModel.INotifyPropertyChanged> Schnittstelle implementieren, müssen Sie nicht verwenden, <xref:System.Windows.Forms.BindingSource> um das Objekt an ein Steuerelement zu binden, aber die Verwendung von <xref:System.Windows.Forms.BindingSource> wird empfohlen.  
  
## <a name="change-notification-for-list-based-binding"></a>Änderungs Benachrichtigung für List-Based Bindung  
 Windows Forms hängt von einer gebundenen Liste ab, um Eigenschafts Änderungen (ein Listenelement-Eigenschafts Wertänderungen) und eine Liste geändert (ein Element wird gelöscht oder der Liste hinzugefügt) für gebundene Steuerelemente bereitzustellen. Daher müssen Listen, die für die Datenbindung verwendet werden <xref:System.ComponentModel.IBindingList> , implementieren, das beide Arten von Änderungs Benachrichtigungen bereitstellt. <xref:System.ComponentModel.BindingList%601>Ist eine generische Implementierung von <xref:System.ComponentModel.IBindingList> und ist für die Verwendung mit Windows Forms Datenbindung konzipiert. Sie können ein <xref:System.ComponentModel.BindingList%601> -Objekt erstellen, das einen Geschäfts Objekttyp enthält, der implementiert, <xref:System.ComponentModel.INotifyPropertyChanged> und die-Ereignisse werden automatisch <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> in-Ereignisse konvertiert <xref:System.ComponentModel.IBindingList.ListChanged> . Wenn es sich bei der gebundenen Liste nicht um eine handelt <xref:System.ComponentModel.IBindingList> , müssen Sie die Liste der Objekte mithilfe der-Komponente an Windows Forms-Steuerelemente binden <xref:System.Windows.Forms.BindingSource> . Die- <xref:System.Windows.Forms.BindingSource> Komponente stellt eine Eigenschaften-zu-Listen-Konvertierung ähnlich der von bereit <xref:System.ComponentModel.BindingList%601> . Weitere Informationen finden Sie unter Gewusst [wie: Aufrufen von Änderungs Benachrichtigungen mithilfe von BindingSource und der INotifyPropertyChanged-Schnittstelle](./controls/raise-change-notifications--bindingsource.md).  
  
## <a name="change-notification-for-custom-controls"></a>Änderungs Benachrichtigung für benutzerdefinierte Steuerelemente  
 Schließlich müssen Sie auf der Steuerungs Seite ein *propertyName* Changed-Ereignis für jede Eigenschaft verfügbar machen, die für die Datenbindung entworfen wurde. Die Änderungen an der Steuerelement Eigenschaft werden dann an die gebundene Datenquelle weitergegeben. Weitere Informationen finden Sie unter Vorgehens [Weise: Anwenden des PropertyNameChanged-Musters](how-to-apply-the-propertynamechanged-pattern.md) .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.BindingSource>
- <xref:System.ComponentModel.INotifyPropertyChanged>
- <xref:System.ComponentModel.BindingList%601>
- [Datenbindung in Web Forms](windows-forms-data-binding.md)
- [Von Windows Forms unterstützte Datenquellen](data-sources-supported-by-windows-forms.md)
- [Datenbindung und Windows Forms](data-binding-and-windows-forms.md)
