---
title: 'Gewusst wie: Einrichten von Benachrichtigungen über Bindungsaktualisierungen'
ms.date: 03/30/2017
helpviewer_keywords:
- notifications [WPF], binding updates
- data binding [WPF], notification of binding updates
- binding [WPF], updates [WPF], notifications of
ms.assetid: 5673073e-dbe1-49da-980a-484a88f9595a
ms.openlocfilehash: d6a27d0226abe1b67a92f76219be3a563fc26216
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977769"
---
# <a name="how-to-set-up-notification-of-binding-updates"></a><span data-ttu-id="5173b-102">Gewusst wie: Einrichten von Benachrichtigungen über Bindungsaktualisierungen</span><span class="sxs-lookup"><span data-stu-id="5173b-102">How to: Set Up Notification of Binding Updates</span></span>
<span data-ttu-id="5173b-103">In diesem Beispiel wird erläutert, wie Sie Benachrichtigungen einrichten können, die Sie darüber informieren, wenn die Eigenschaft „Bindungsziel (Ziel)“ oder „Bindungsquelle (Quelle)“ einer Bindung aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5173b-103">This example shows how to set up to be notified when the binding target (target) or the binding source (source) property of a binding has been updated.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5173b-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5173b-104">Example</span></span>  
 <span data-ttu-id="5173b-105">Bei jeder Aktualisierung der Bindungsquelle oder des Bindungsziels löst [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] ein Datenaktualisierungsereignis aus.</span><span class="sxs-lookup"><span data-stu-id="5173b-105">[!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] raises a data update event each time that the binding source or target has been updated.</span></span> <span data-ttu-id="5173b-106">Intern veranlasst dieses Ereignis die Benutzeroberfläche (User Interface, [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)]), eine Aktualisierung durchzuführen, weil sich die gebundenen Daten geändert haben.</span><span class="sxs-lookup"><span data-stu-id="5173b-106">Internally, this event is used to inform the [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] that it should update, because the bound data has changed.</span></span> <span data-ttu-id="5173b-107">Beachten Sie, dass Sie die Datenklasse mithilfe der-Schnittstelle implementieren müssen, damit diese Ereignisse funktionieren und auch für eine unidirektionale oder bidirektionale Bindung ordnungsgemäß funktionieren <xref:System.ComponentModel.INotifyPropertyChanged> .</span><span class="sxs-lookup"><span data-stu-id="5173b-107">Note that for these events to work, and also for one-way or two-way binding to work properly, you need to implement your data class using the <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span></span> <span data-ttu-id="5173b-108">Weitere Informationen finden Sie unter [Implementieren von Benachrichtigungen bei Eigenschaftenänderungen](how-to-implement-property-change-notification.md).</span><span class="sxs-lookup"><span data-stu-id="5173b-108">For more information, see [Implement Property Change Notification](how-to-implement-property-change-notification.md).</span></span>  
  
 <span data-ttu-id="5173b-109">Legen Sie die- <xref:System.Windows.Data.Binding.NotifyOnTargetUpdated%2A> Eigenschaft oder die- <xref:System.Windows.Data.Binding.NotifyOnSourceUpdated%2A> Eigenschaft (oder beides) `true` in der Bindung auf fest.</span><span class="sxs-lookup"><span data-stu-id="5173b-109">Set the <xref:System.Windows.Data.Binding.NotifyOnTargetUpdated%2A> or <xref:System.Windows.Data.Binding.NotifyOnSourceUpdated%2A> property (or both) to `true` in the binding.</span></span> <span data-ttu-id="5173b-110">Der Handler, den Sie zur Überwachung dieses Ereignisses bereitstellen, muss direkt an das Element angefügt werden, über dessen Änderungen Sie informiert werden möchten. Oder er muss an den Gesamtdatenkontext angefügt werden, wenn Sie über Änderungen am Kontext informiert werden möchten.</span><span class="sxs-lookup"><span data-stu-id="5173b-110">The handler you provide to listen for this event must be attached directly to the element where you want to be informed of changes, or to the overall data context if you want to be aware that anything in the context has changed.</span></span>  
  
 <span data-ttu-id="5173b-111">Im folgenden Beispiel wird erläutert, wie Sie Benachrichtigungen für die Aktualisierung einer Zieleigenschaft einrichten.</span><span class="sxs-lookup"><span data-stu-id="5173b-111">Here is an example that shows how to set up for notification when a target property has been updated.</span></span>  
  
 [!code-xaml[DirectionalBinding#2](~/samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml#2)]  
  
 <span data-ttu-id="5173b-112">Anschließend können Sie auf der Grundlage des EventHandler-Delegaten \<T> , *ontargetupdatiert* , in diesem Beispiel einen Handler zuweisen, um das-Ereignis zu behandeln:</span><span class="sxs-lookup"><span data-stu-id="5173b-112">You can then assign a handler based on the EventHandler\<T> delegate, *OnTargetUpdated* in this example, to handle the event:</span></span>  
  
 [!code-csharp[DirectionalBinding#3](~/samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml.cs#3)]  
[!code-csharp[DirectionalBinding#EndEvent](~/samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml.cs#endevent)]  
  
 <span data-ttu-id="5173b-113">Parameter des Ereignisses können zur Ermittlung von Details über die geänderte Eigenschaft (z. B. den Typ oder das jeweilige Element, wenn derselbe Handler an mehrere Elemente angefügt ist) verwendet werden. Diese Details können hilfreich sein, wenn es für ein einzelnes Element mehrere gebundene Eigenschaften gibt.</span><span class="sxs-lookup"><span data-stu-id="5173b-113">Parameters of the event can be used to determine details about the property that changed (such as the type or the specific element if the same handler is attached to more than one element), which can be useful if there are multiple bound properties on a single element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5173b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5173b-114">See also</span></span>

- [<span data-ttu-id="5173b-115">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="5173b-115">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="5173b-116">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="5173b-116">How-to Topics</span></span>](data-binding-how-to-topics.md)
