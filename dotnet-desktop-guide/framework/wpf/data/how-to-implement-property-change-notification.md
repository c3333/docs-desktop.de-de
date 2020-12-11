---
title: 'Gewusst wie: Implementieren von Benachrichtigungen bei Eigenschaftenänderungen'
description: Aktivieren Sie Ihre Eigenschaften, um eine Bindungs Quelle automatisch zu benachrichtigen, wenn sich der Eigenschafts Wert in Windows Presentation Foundation (WPF) ändert.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- notifications of change [WPF]
- data binding [WPF], property change notifications
- change notifications [WPF]
- properties [WPF], change notifications
ms.assetid: 30b59d9e-8c3a-4349-aa82-4be837e841cf
ms.openlocfilehash: f3cf3fe211e852fccaa605623820ebbde7e62917
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977695"
---
# <a name="how-to-implement-property-change-notification"></a><span data-ttu-id="678c8-103">Gewusst wie: Implementieren von Benachrichtigungen bei Eigenschaftenänderungen</span><span class="sxs-lookup"><span data-stu-id="678c8-103">How to: Implement Property Change Notification</span></span>
<span data-ttu-id="678c8-104">Um die <xref:System.Windows.Data.BindingMode.OneWay> <xref:System.Windows.Data.BindingMode.TwoWay> dynamischen Änderungen der Bindungs Quelle automatisch widerzuspiegeln (z. b. wenn der Vorschaubereich automatisch aktualisiert werden soll, wenn der Benutzer ein Formular bearbeitet), muss die Klasse die richtigen Benachrichtigungen über geänderte Eigenschaften bereitstellen, damit die Bindungs Zieleigenschaften die dynamischen Änderungen der Bindungs Quelle automatisch widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="678c8-104">To support <xref:System.Windows.Data.BindingMode.OneWay> or <xref:System.Windows.Data.BindingMode.TwoWay> binding to enable your binding target properties to automatically reflect the dynamic changes of the binding source (for example, to have the preview pane updated automatically when the user edits a form), your class needs to provide the proper property changed notifications.</span></span> <span data-ttu-id="678c8-105">Dieses Beispiel zeigt, wie eine Klasse erstellt wird, die implementiert <xref:System.ComponentModel.INotifyPropertyChanged> .</span><span class="sxs-lookup"><span data-stu-id="678c8-105">This example shows how to create a class that implements <xref:System.ComponentModel.INotifyPropertyChanged>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="678c8-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="678c8-106">Example</span></span>  
 <span data-ttu-id="678c8-107">Zum Implementieren von <xref:System.ComponentModel.INotifyPropertyChanged> müssen Sie das <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> -Ereignis deklarieren und die-Methode erstellen `OnPropertyChanged` .</span><span class="sxs-lookup"><span data-stu-id="678c8-107">To implement <xref:System.ComponentModel.INotifyPropertyChanged> you need to declare the <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> event and create the `OnPropertyChanged` method.</span></span> <span data-ttu-id="678c8-108">Dann rufen Sie für jede Eigenschaft, für die Sie Änderungsbenachrichtigungen erhalten möchten, `OnPropertyChanged` auf, wenn die Eigenschaft aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="678c8-108">Then for each property you want change notifications for, you call `OnPropertyChanged` whenever the property is updated.</span></span>  
  
 [!code-csharp[SimpleBinding#PersonClass](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleBinding/CSharp/Person.cs#personclass)]
 [!code-vb[SimpleBinding#PersonClass](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleBinding/VisualBasic/Person.vb#personclass)]  
  
 <span data-ttu-id="678c8-109">Ein Beispiel für die Verwendung der- `Person` Klasse zur Unterstützung von Bindungen finden Sie unter <xref:System.Windows.Data.BindingMode.TwoWay> [Steuern, wann der TextBox-Text die Quelle aktualisiert](how-to-control-when-the-textbox-text-updates-the-source.md).</span><span class="sxs-lookup"><span data-stu-id="678c8-109">To see an example of how the `Person` class can be used to support <xref:System.Windows.Data.BindingMode.TwoWay> binding, see [Control When the TextBox Text Updates the Source](how-to-control-when-the-textbox-text-updates-the-source.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="678c8-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="678c8-110">See also</span></span>

- [<span data-ttu-id="678c8-111">Übersicht über Bindungsquellen</span><span class="sxs-lookup"><span data-stu-id="678c8-111">Binding Sources Overview</span></span>](binding-sources-overview.md)
- [<span data-ttu-id="678c8-112">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="678c8-112">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="678c8-113">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="678c8-113">How-to Topics</span></span>](data-binding-how-to-topics.md)
