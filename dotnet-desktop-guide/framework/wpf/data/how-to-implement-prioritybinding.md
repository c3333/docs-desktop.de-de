---
title: 'Gewusst wie: Implementieren von PriorityBinding'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], PriorityBinding class
ms.assetid: d63b65ab-b3e9-4322-9aa8-1450f8d89532
ms.openlocfilehash: 694679183f92c9737bbdb511b4ebd5a4bf2185f1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978136"
---
# <a name="how-to-implement-prioritybinding"></a><span data-ttu-id="e8072-102">Gewusst wie: Implementieren von PriorityBinding</span><span class="sxs-lookup"><span data-stu-id="e8072-102">How to: Implement PriorityBinding</span></span>

<span data-ttu-id="e8072-103"><xref:System.Windows.Data.PriorityBinding> in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] funktioniert durch Angeben einer Liste von Bindungen.</span><span class="sxs-lookup"><span data-stu-id="e8072-103"><xref:System.Windows.Data.PriorityBinding> in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] works by specifying a list of bindings.</span></span> <span data-ttu-id="e8072-104">Die Liste der Bindungen ist von der höchsten Priorität bis zur niedrigsten Priorität geordnet.</span><span class="sxs-lookup"><span data-stu-id="e8072-104">The list of bindings is ordered from highest priority to lowest priority.</span></span> <span data-ttu-id="e8072-105">Wenn die Bindung mit der höchsten Priorität bei der Verarbeitung einen Wert erfolgreich zurückgibt, ist es nicht erforderlich, die anderen Bindungen in der Liste zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e8072-105">If the highest priority binding returns a value successfully when it is processed then there is never a need to process the other bindings in the list.</span></span> <span data-ttu-id="e8072-106">Dies könnte der Fall sein, wenn die Bewertung mit der höchsten Priorität lange ausgewertet werden muss, wenn die nächsthöhere Priorität, die erfolgreich einen Wert zurückgibt, verwendet wird, bis eine Bindung einer höheren Priorität erfolgreich einen Wert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e8072-106">It could be the case that the highest priority binding takes a long time to be evaluated, the next highest priority that returns a value successfully will be used until a binding of a higher priority returns a value successfully.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e8072-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e8072-107">Example</span></span>  

 <span data-ttu-id="e8072-108">Um zu veranschaulichen <xref:System.Windows.Data.PriorityBinding> , wie funktioniert, wurde das- `AsyncDataSource` Objekt mit den folgenden drei Eigenschaften erstellt: `FastDP` , `SlowerDP` und `SlowestDP` .</span><span class="sxs-lookup"><span data-stu-id="e8072-108">To demonstrate how <xref:System.Windows.Data.PriorityBinding> works, the `AsyncDataSource` object has been created with the following three properties: `FastDP`, `SlowerDP`, and `SlowestDP`.</span></span>  
  
 <span data-ttu-id="e8072-109">Der Get-Accessor von `FastDP` gibt den Wert des `_fastDP` Datenmembers zurück.</span><span class="sxs-lookup"><span data-stu-id="e8072-109">The get accessor of `FastDP` returns the value of the `_fastDP` data member.</span></span>  
  
 <span data-ttu-id="e8072-110">Der Get-Accessor von `SlowerDP` wartet drei Sekunden, bevor er den Wert des `_slowerDP` Datenmembers zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e8072-110">The get accessor of `SlowerDP` waits for 3 seconds before returning the value of the `_slowerDP` data member.</span></span>  
  
 <span data-ttu-id="e8072-111">Der Get-Accessor von `SlowestDP` wartet 5 Sekunden, bevor er den Wert des `_slowestDP` Datenmembers zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e8072-111">The get accessor of `SlowestDP` waits for 5 seconds before returning the value of the `_slowestDP` data member.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e8072-112">Dieses Beispiel dient ausschließlich Demonstrationszwecken.</span><span class="sxs-lookup"><span data-stu-id="e8072-112">This example is for demonstration purposes only.</span></span> <span data-ttu-id="e8072-113">Die .NET-Richtlinien werden zum Definieren von Eigenschaften empfohlen, die in der Größenordnung langsamer sind als ein Feld Satz.</span><span class="sxs-lookup"><span data-stu-id="e8072-113">The .NET guidelines recommend against defining properties that are orders of magnitude slower than a field set would be.</span></span> <span data-ttu-id="e8072-114">Weitere Informationen finden Sie unter [auswählen zwischen Eigenschaften und Methoden](/previous-versions/dotnet/netframework-4.0/ms229054(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="e8072-114">For more information, see [Choosing Between Properties and Methods](/previous-versions/dotnet/netframework-4.0/ms229054(v=vs.100)).</span></span>  
  
 [!code-csharp[PriorityBinding#1](~/samples/snippets/csharp/VS_Snippets_Wpf/PriorityBinding/CSharp/Window1.xaml.cs#1)]
 [!code-vb[PriorityBinding#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PriorityBinding/VisualBasic/AsyncDataSource.vb#1)]  
  
 <span data-ttu-id="e8072-115">Die- <xref:System.Windows.Controls.TextBlock.Text%2A> Eigenschaft bindet an die oben genannte `AsyncDS` mithilfe von <xref:System.Windows.Data.PriorityBinding> :</span><span class="sxs-lookup"><span data-stu-id="e8072-115">The <xref:System.Windows.Controls.TextBlock.Text%2A> property binds to the above `AsyncDS` using <xref:System.Windows.Data.PriorityBinding>:</span></span>  
  
 [!code-xaml[PriorityBinding#2](~/samples/snippets/csharp/VS_Snippets_Wpf/PriorityBinding/CSharp/Window1.xaml#2)]  
  
 <span data-ttu-id="e8072-116">Wenn die Bindungs-Engine die- <xref:System.Windows.Data.Binding> Objekte verarbeitet, beginnt Sie mit dem ersten <xref:System.Windows.Data.Binding> , das an die-Eigenschaft gebunden ist `SlowestDP` .</span><span class="sxs-lookup"><span data-stu-id="e8072-116">When the binding engine processes the <xref:System.Windows.Data.Binding> objects, it starts with the first <xref:System.Windows.Data.Binding>, which is bound to the `SlowestDP` property.</span></span> <span data-ttu-id="e8072-117">Wenn dies <xref:System.Windows.Data.Binding> verarbeitet wird, wird ein Wert nicht erfolgreich zurückgegeben, da er 5 Sekunden lang im Ruhezustand ist, sodass das nächste <xref:System.Windows.Data.Binding> Element verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e8072-117">When this <xref:System.Windows.Data.Binding> is processed, it does not return a value successfully because it is sleeping for 5 seconds, so the next <xref:System.Windows.Data.Binding> element is processed.</span></span> <span data-ttu-id="e8072-118">Der nächste gibt <xref:System.Windows.Data.Binding> einen Wert nicht erfolgreich zurück, da er drei Sekunden lang im Ruhezustand ist.</span><span class="sxs-lookup"><span data-stu-id="e8072-118">The next <xref:System.Windows.Data.Binding> does not return a value successfully because it is sleeping for 3 seconds.</span></span> <span data-ttu-id="e8072-119">Die Bindungs-Engine wechselt dann auf das nächste <xref:System.Windows.Data.Binding> Element, das an die- `FastDP` Eigenschaft gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="e8072-119">The binding engine then moves onto the next <xref:System.Windows.Data.Binding> element, which is bound to the `FastDP` property.</span></span> <span data-ttu-id="e8072-120">Dadurch wird <xref:System.Windows.Data.Binding> der Wert "fast Value" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e8072-120">This <xref:System.Windows.Data.Binding> returns the value "Fast Value".</span></span> <span data-ttu-id="e8072-121">Der <xref:System.Windows.Controls.TextBlock> zeigt jetzt den Wert "schneller Wert" an.</span><span class="sxs-lookup"><span data-stu-id="e8072-121">The <xref:System.Windows.Controls.TextBlock> now displays the value "Fast Value".</span></span>  
  
 <span data-ttu-id="e8072-122">Nach 3 Sekunden gibt die- `SlowerDP` Eigenschaft den Wert "langsamerer Wert" zurück.</span><span class="sxs-lookup"><span data-stu-id="e8072-122">After 3 seconds elapses, the `SlowerDP` property returns the value "Slower Value".</span></span> <span data-ttu-id="e8072-123">Der <xref:System.Windows.Controls.TextBlock> zeigt dann den Wert "langsamerer Wert" an.</span><span class="sxs-lookup"><span data-stu-id="e8072-123">The <xref:System.Windows.Controls.TextBlock> then displays the value "Slower Value".</span></span>  
  
 <span data-ttu-id="e8072-124">Nach 5 Sekunden gibt die- `SlowestDP` Eigenschaft den Wert "Slowest Value" zurück.</span><span class="sxs-lookup"><span data-stu-id="e8072-124">After 5 seconds elapses, the `SlowestDP` property returns the value "Slowest Value".</span></span> <span data-ttu-id="e8072-125">Diese Bindung hat die höchste Priorität, da Sie zuerst aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8072-125">That binding has the highest priority because it is listed first.</span></span> <span data-ttu-id="e8072-126">Der <xref:System.Windows.Controls.TextBlock> zeigt jetzt den Wert "Langsamster Wert" an.</span><span class="sxs-lookup"><span data-stu-id="e8072-126">The <xref:System.Windows.Controls.TextBlock> now displays the value "Slowest Value".</span></span>  
  
 <span data-ttu-id="e8072-127"><xref:System.Windows.Data.PriorityBinding>Informationen dazu, was als erfolgreicher Rückgabewert einer Bindung angesehen wird, finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="e8072-127">See <xref:System.Windows.Data.PriorityBinding> for information about what is considered a successful return value from a binding.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8072-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8072-128">See also</span></span>

- <xref:System.Windows.Data.Binding.IsAsync%2A?displayProperty=nameWithType>
- [<span data-ttu-id="e8072-129">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="e8072-129">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="e8072-130">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="e8072-130">How-to Topics</span></span>](data-binding-how-to-topics.md)
