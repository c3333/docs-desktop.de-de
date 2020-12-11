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
# <a name="how-to-get-the-binding-object-from-a-bound-target-property"></a>Gewusst wie: Abrufen des Bindungsobjekts aus einer gebundenen Zieleigenschaft
Dieses Beispiel zeigt, wie das Bindungsobjekt aus einer datengebundenen Zieleigenschaft abgerufen wird.

## <a name="example"></a>Beispiel
 Zum erhalten des-Objekts können Sie Folgendes ausführen <xref:System.Windows.Data.Binding> :

 [!code-csharp[BindValidation#GetBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/BindValidation/CSharp/Window1.xaml.cs#getbinding)]

> [!NOTE]
> Sie müssen die Abhängigkeitseigenschaft für die abzurufende Bindung angeben, da eventuell mehrere Eigenschaften des Zielobjekts die Datenbindung verwenden.

 Alternativ können Sie das <xref:System.Windows.Data.BindingExpression> -Objekt und dann den Wert der- <xref:System.Windows.Data.BindingExpression.ParentBinding%2A> Eigenschaft erhalten.

 Das komplette Beispiel finden Sie unter Beispiel für die [Bindungs Validierung](https://github.com/Microsoft/WPF-Samples/tree/master/Data%20Binding/BindValidation).

> [!NOTE]
> Wenn die Bindung eine ist <xref:System.Windows.Data.MultiBinding> , verwenden Sie <xref:System.Windows.Data.BindingOperations.GetMultiBinding%2A?displayProperty=nameWithType> . Wenn es sich um eine handelt <xref:System.Windows.Data.PriorityBinding> , verwenden Sie <xref:System.Windows.Data.BindingOperations.GetPriorityBinding%2A?displayProperty=nameWithType> . Wenn Sie unsicher sind, ob die Ziel Eigenschaft mithilfe von,, oder gebunden ist <xref:System.Windows.Data.Binding> <xref:System.Windows.Data.MultiBinding> <xref:System.Windows.Data.PriorityBinding> , können Sie verwenden <xref:System.Windows.Data.BindingOperations.GetBindingBase%2A?displayProperty=nameWithType> .

## <a name="see-also"></a>Siehe auch

- [Erstellen einer Bindung in Code](how-to-create-a-binding-in-code.md)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
