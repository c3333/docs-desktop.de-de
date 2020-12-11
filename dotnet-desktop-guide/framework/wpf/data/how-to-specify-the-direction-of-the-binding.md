---
title: 'Gewusst wie: Angeben der Bindungsrichtung'
ms.date: 03/30/2017
helpviewer_keywords:
- direction of binding [WPF]
- binding direction [WPF]
- data binding [WPF], direction of binding
ms.assetid: 37334478-028b-4514-86c9-1420709f4818
ms.openlocfilehash: 6b3c6afde5e9fa1b778905b1a278bb295b6cbf11
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976551"
---
# <a name="how-to-specify-the-direction-of-the-binding"></a><span data-ttu-id="5ab29-102">Gewusst wie: Angeben der Bindungs Richtung</span><span class="sxs-lookup"><span data-stu-id="5ab29-102">How to: Specify the direction of the binding</span></span>

<span data-ttu-id="5ab29-103">In diesem Beispiel wird erläutert, wie sich angeben lässt, ob die Bindung nur die Eigenschaft „Bindungsziel (Ziel)“, „Bindungsquelle (Quelle)“ oder sowohl die Ziel- als auch die Quelleigenschaft aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5ab29-103">This example shows how to specify whether the binding updates only the binding target (target) property, the binding source (source) property, or both the target property and the source property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5ab29-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5ab29-104">Example</span></span>  
 <span data-ttu-id="5ab29-105">Verwenden Sie die- <xref:System.Windows.Data.Binding.Mode%2A?displayProperty=nameWithType> Eigenschaft, um die Bindungs Richtung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5ab29-105">You use the <xref:System.Windows.Data.Binding.Mode%2A?displayProperty=nameWithType> property to specify the direction of the binding.</span></span> <span data-ttu-id="5ab29-106">Im folgenden finden Sie die verfügbaren Optionen für das Binden von Updates:</span><span class="sxs-lookup"><span data-stu-id="5ab29-106">The following are the available options for binding updates:</span></span>  
  
- <span data-ttu-id="5ab29-107"><xref:System.Windows.Data.BindingMode.TwoWay?displayProperty=nameWithType> Aktualisiert die Ziel Eigenschaft oder die-Eigenschaft, wenn sich entweder die Ziel Eigenschaft oder die Quell Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="5ab29-107"><xref:System.Windows.Data.BindingMode.TwoWay?displayProperty=nameWithType> updates the target property or the property whenever either the target property or the source property changes.</span></span>  
  
- <span data-ttu-id="5ab29-108"><xref:System.Windows.Data.BindingMode.OneWay?displayProperty=nameWithType> Aktualisiert die Ziel Eigenschaft nur, wenn sich die Quell Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="5ab29-108"><xref:System.Windows.Data.BindingMode.OneWay?displayProperty=nameWithType> updates the target property only when the source property changes.</span></span>  
  
- <span data-ttu-id="5ab29-109"><xref:System.Windows.Data.BindingMode.OneTime?displayProperty=nameWithType> Aktualisiert die Ziel Eigenschaft nur, wenn die Anwendung gestartet wird oder wenn <xref:System.Windows.FrameworkElement.DataContext%2A> eine Änderung durchläuft.</span><span class="sxs-lookup"><span data-stu-id="5ab29-109"><xref:System.Windows.Data.BindingMode.OneTime?displayProperty=nameWithType> updates the target property only when the application starts or when the <xref:System.Windows.FrameworkElement.DataContext%2A> undergoes a change.</span></span>  
  
- <span data-ttu-id="5ab29-110"><xref:System.Windows.Data.BindingMode.OneWayToSource?displayProperty=nameWithType> Aktualisiert die Quell Eigenschaft, wenn die Ziel Eigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5ab29-110"><xref:System.Windows.Data.BindingMode.OneWayToSource?displayProperty=nameWithType> updates the source property when the target property changes.</span></span>  
  
- <span data-ttu-id="5ab29-111"><xref:System.Windows.Data.BindingMode.Default?displayProperty=nameWithType> bewirkt <xref:System.Windows.Data.Binding.Mode%2A> , dass der Standardwert der Ziel Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ab29-111"><xref:System.Windows.Data.BindingMode.Default?displayProperty=nameWithType> causes the default <xref:System.Windows.Data.Binding.Mode%2A> value of target property to be used.</span></span>  
  
 <span data-ttu-id="5ab29-112">Weitere Informationen finden Sie unter der <xref:System.Windows.Data.BindingMode>-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="5ab29-112">For more information, see the <xref:System.Windows.Data.BindingMode> enumeration.</span></span>  
  
 <span data-ttu-id="5ab29-113">Im folgenden Beispiel wird das Festlegen der <xref:System.Windows.Data.Binding.Mode%2A>-Eigenschaft veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5ab29-113">The following example shows how to set the <xref:System.Windows.Data.Binding.Mode%2A> property.</span></span>  
  
 [!code-xaml[DirectionalBinding#4](~/samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml#4)]  
  
 <span data-ttu-id="5ab29-114">Zum Erkennen von Quelländerungen (das gilt für die <xref:System.Windows.Data.BindingMode.OneWay>-Bindung und die <xref:System.Windows.Data.BindingMode.TwoWay>-Bindung) muss die Quelle einen geeigneten Mechanismus für Benachrichtigungen bei Eigenschaftenänderungen implementieren, z. B. <xref:System.ComponentModel.INotifyPropertyChanged>.</span><span class="sxs-lookup"><span data-stu-id="5ab29-114">To detect source changes (applicable to <xref:System.Windows.Data.BindingMode.OneWay> and <xref:System.Windows.Data.BindingMode.TwoWay> bindings), the source must implement a suitable property change notification mechanism such as <xref:System.ComponentModel.INotifyPropertyChanged>.</span></span> <span data-ttu-id="5ab29-115">Ein Beispiel für eine-Implementierung finden Sie unter [Implementieren von Benachrichtigungen über Eigenschafts Änderungen](how-to-implement-property-change-notification.md) <xref:System.ComponentModel.INotifyPropertyChanged> .</span><span class="sxs-lookup"><span data-stu-id="5ab29-115">See [Implement Property Change Notification](how-to-implement-property-change-notification.md) for an example of an <xref:System.ComponentModel.INotifyPropertyChanged> implementation.</span></span>  
  
 <span data-ttu-id="5ab29-116">Für- <xref:System.Windows.Data.BindingMode.TwoWay> oder- <xref:System.Windows.Data.BindingMode.OneWayToSource> Bindungen können Sie die zeitliche Steuerung der Quell Aktualisierungen steuern, indem Sie die- <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5ab29-116">For <xref:System.Windows.Data.BindingMode.TwoWay> or <xref:System.Windows.Data.BindingMode.OneWayToSource> bindings, you can control the timing of the source updates by setting the <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> property.</span></span> <span data-ttu-id="5ab29-117">Weitere Informationen finden Sie unter <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A>.</span><span class="sxs-lookup"><span data-stu-id="5ab29-117">See <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> for more information.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ab29-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ab29-118">See also</span></span>

- <xref:System.Windows.Data.Binding>
- [<span data-ttu-id="5ab29-119">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="5ab29-119">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="5ab29-120">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="5ab29-120">How-to Topics</span></span>](data-binding-how-to-topics.md)
