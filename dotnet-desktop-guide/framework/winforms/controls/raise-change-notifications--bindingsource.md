---
title: 'Vorgehensweise: Auslösen von Änderungsbenachrichtigungen mithilfe von BindingSource und der INotifyPropertyChanged-Schnittstelle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- change notifications [Windows Forms], raising
- BindingSource component [Windows Forms], and IPropertyChange
- data sources [Windows Forms], detecting changes
- examples [Windows Forms], BindingSource component
- change notifications
- INotifyPropertyChanged interface [Windows Forms], using with BindingSource
- BindingSource component [Windows Forms], examples
ms.assetid: 7fa2cf51-c09f-4375-adf0-e36c5617f099
ms.openlocfilehash: cd8c3fba87fd5ab9acf9159fc1130ee28ed38497
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976964"
---
# <a name="how-to-raise-change-notifications-using-a-bindingsource-and-the-inotifypropertychanged-interface"></a>Vorgehensweise: Auslösen von Änderungsbenachrichtigungen mithilfe von BindingSource und der INotifyPropertyChanged-Schnittstelle

Die <xref:System.Windows.Forms.BindingSource> Komponente erkennt Änderungen in einer Datenquelle automatisch, wenn der in der Datenquelle enthaltene Typ implementiert <xref:System.ComponentModel.INotifyPropertyChanged> und <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> Ereignisse auslöst, wenn ein Eigenschafts Wert geändert wird. Diese Änderungs Erkennung ist nützlich, da Steuerelemente, die an die automatische Aktualisierung gebunden sind, bei einer <xref:System.Windows.Forms.BindingSource> Änderung der Datenquellen Werte.  
  
> [!NOTE]
> Wenn die Datenquelle <xref:System.ComponentModel.INotifyPropertyChanged> implementiert, sollten Sie beim Durchführen asynchroner Operationen keine Änderungen an der Datenquelle in einem Hintergrundthread vornehmen. Lesen Sie die Daten stattdessen in einem Hintergrundthread, und führen Sie sie in einer Liste auf dem UI-Thread zusammen.  
  
## <a name="example"></a>Beispiel  

 Das folgende Codebeispiel veranschaulicht eine einfache Implementierung der <xref:System.ComponentModel.INotifyPropertyChanged>-Schnittstelle. Darüber hinaus wird gezeigt, wie <xref:System.Windows.Forms.BindingSource> automatisch eine Datenquellenänderung an ein gebundenes Steuerelement übergibt, wenn <xref:System.Windows.Forms.BindingSource> an eine Liste des <xref:System.ComponentModel.INotifyPropertyChanged>-Typs gebunden ist.   
  
 Wenn Sie das `CallerMemberName`-Attribut verwenden, müssen Aufrufe der `NotifyPropertyChanged`-Methode den Eigenschaftennamen nicht als Zeichenfolgenargument angeben. Weitere Informationen finden Sie unter [Aufruferinformationen (c#)](/dotnet/csharp/language-reference/attributes/caller-information) oder [Aufruferinformationen (Visual Basic)](/dotnet/visual-basic/programming-guide/concepts/caller-information).  
  
 [!code-csharp[System.ComponentModel.IPropertyChangeExample#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.IPropertyChangeExample#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  

 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys "System", "System. Data", "System. Drawing" und "System. Windows. Forms"  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.ComponentModel.INotifyPropertyChanged>
- [BindingSource-Komponente](bindingsource-component.md)
- [Vorgehensweise: Auslösen von Änderungsbenachrichtigungen mithilfe der ResetItem-Methode einer BindingSource](how-to-raise-change-notifications-using-the-bindingsource-resetitem-method.md)
