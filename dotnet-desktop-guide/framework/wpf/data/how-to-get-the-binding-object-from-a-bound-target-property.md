---
title: 'Gewusst wie: Abrufen des Bindungsobjekts aus einer gebundenen Zieleigenschaft'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], getting binding objects from bound target properties
- properties [WPF], getting binding objects from
ms.assetid: 87974c5f-136b-4de7-b07d-9285b62ab123
ms.openlocfilehash: c528515124898c7deb6114e620ce21766123ab3c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978143"
---
# <a name="how-to-get-the-binding-object-from-a-bound-target-property"></a><span data-ttu-id="bbe9e-102">Gewusst wie: Abrufen des Bindungsobjekts aus einer gebundenen Zieleigenschaft</span><span class="sxs-lookup"><span data-stu-id="bbe9e-102">How to: Get the Binding Object from a Bound Target Property</span></span>
<span data-ttu-id="bbe9e-103">Dieses Beispiel zeigt, wie das Bindungsobjekt aus einer datengebundenen Zieleigenschaft abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bbe9e-103">This example shows how to obtain the binding object from a data-bound target property.</span></span>

## <a name="example"></a><span data-ttu-id="bbe9e-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bbe9e-104">Example</span></span>
 <span data-ttu-id="bbe9e-105">Zum erhalten des-Objekts können Sie Folgendes ausführen <xref:System.Windows.Data.Binding> :</span><span class="sxs-lookup"><span data-stu-id="bbe9e-105">You can do the following to get the <xref:System.Windows.Data.Binding> object:</span></span>

 [!code-csharp[BindValidation#GetBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/BindValidation/CSharp/Window1.xaml.cs#getbinding)]

> [!NOTE]
> <span data-ttu-id="bbe9e-106">Sie müssen die Abhängigkeitseigenschaft für die abzurufende Bindung angeben, da eventuell mehrere Eigenschaften des Zielobjekts die Datenbindung verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbe9e-106">You must specify the dependency property for the binding you want because it is possible that more than one property of the target object is using data binding.</span></span>

 <span data-ttu-id="bbe9e-107">Alternativ können Sie das <xref:System.Windows.Data.BindingExpression> -Objekt und dann den Wert der- <xref:System.Windows.Data.BindingExpression.ParentBinding%2A> Eigenschaft erhalten.</span><span class="sxs-lookup"><span data-stu-id="bbe9e-107">Alternatively, you can get the <xref:System.Windows.Data.BindingExpression> and then get the value of the <xref:System.Windows.Data.BindingExpression.ParentBinding%2A> property.</span></span>

 <span data-ttu-id="bbe9e-108">Das komplette Beispiel finden Sie unter Beispiel für die [Bindungs Validierung](https://github.com/Microsoft/WPF-Samples/tree/master/Data%20Binding/BindValidation).</span><span class="sxs-lookup"><span data-stu-id="bbe9e-108">For the complete example see [Binding Validation Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Data%20Binding/BindValidation).</span></span>

> [!NOTE]
> <span data-ttu-id="bbe9e-109">Wenn die Bindung eine ist <xref:System.Windows.Data.MultiBinding> , verwenden Sie <xref:System.Windows.Data.BindingOperations.GetMultiBinding%2A?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="bbe9e-109">If your binding is a <xref:System.Windows.Data.MultiBinding>, use <xref:System.Windows.Data.BindingOperations.GetMultiBinding%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="bbe9e-110">Wenn es sich um eine handelt <xref:System.Windows.Data.PriorityBinding> , verwenden Sie <xref:System.Windows.Data.BindingOperations.GetPriorityBinding%2A?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="bbe9e-110">If it is a <xref:System.Windows.Data.PriorityBinding>, use <xref:System.Windows.Data.BindingOperations.GetPriorityBinding%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="bbe9e-111">Wenn Sie unsicher sind, ob die Ziel Eigenschaft mithilfe von,, oder gebunden ist <xref:System.Windows.Data.Binding> <xref:System.Windows.Data.MultiBinding> <xref:System.Windows.Data.PriorityBinding> , können Sie verwenden <xref:System.Windows.Data.BindingOperations.GetBindingBase%2A?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="bbe9e-111">If you are uncertain whether the target property is bound using a <xref:System.Windows.Data.Binding>, a <xref:System.Windows.Data.MultiBinding>, or a <xref:System.Windows.Data.PriorityBinding>, you can use <xref:System.Windows.Data.BindingOperations.GetBindingBase%2A?displayProperty=nameWithType>.</span></span>

## <a name="see-also"></a><span data-ttu-id="bbe9e-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbe9e-112">See also</span></span>

- [<span data-ttu-id="bbe9e-113">Erstellen einer Bindung in Code</span><span class="sxs-lookup"><span data-stu-id="bbe9e-113">Create a Binding in Code</span></span>](how-to-create-a-binding-in-code.md)
- [<span data-ttu-id="bbe9e-114">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="bbe9e-114">How-to Topics</span></span>](data-binding-how-to-topics.md)
