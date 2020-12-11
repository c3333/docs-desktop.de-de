---
title: 'Gewusst wie: Löschen von Bindungen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bindings [WPF], clearing
- clearing bindings [WPF]
- data binding [WPF], clearing bindings
ms.assetid: 73962a93-32a9-4bcd-9240-bcfbb239093a
ms.openlocfilehash: ab89c185d1b45ab49e680135ca4c1d54395fe0f4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977187"
---
# <a name="how-to-clear-bindings"></a><span data-ttu-id="2b6b4-102">Gewusst wie: Löschen von Bindungen</span><span class="sxs-lookup"><span data-stu-id="2b6b4-102">How to: Clear Bindings</span></span>
<span data-ttu-id="2b6b4-103">Dieses Beispiel zeigt, wie Bindungen aus einem Objekt gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2b6b4-103">This example shows how to clear bindings from an object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2b6b4-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2b6b4-104">Example</span></span>  
 <span data-ttu-id="2b6b4-105">Um eine Bindung aus einer einzelnen Eigenschaft eines Objekts zu löschen, müssen Sie <xref:System.Windows.Data.BindingOperations.ClearBinding%2A> wie im folgenden Beispiel gezeigt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b6b4-105">To clear a binding from an individual property on an object, call <xref:System.Windows.Data.BindingOperations.ClearBinding%2A> as shown in the following example.</span></span> <span data-ttu-id="2b6b4-106">Im folgenden Beispiel wird die-Bindung aus dem <xref:System.Windows.Controls.TextBlock.TextProperty> von *MyText*, einem-Objekt, entfernt <xref:System.Windows.Controls.TextBlock> .</span><span class="sxs-lookup"><span data-stu-id="2b6b4-106">The following example removes the binding from the <xref:System.Windows.Controls.TextBlock.TextProperty> of *mytext*, a <xref:System.Windows.Controls.TextBlock> object.</span></span>  
  
 [!code-csharp[CodeOnlyBinding#ClearBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#clearbinding)]
 [!code-vb[CodeOnlyBinding#ClearBinding](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#clearbinding)]  
  
 <span data-ttu-id="2b6b4-107">Durch das Löschen einer Bindung wird diese entfernt, sodass die Abhängigkeitseigenschaft einen außerhalb der Bindung gültigen Wert annimmt.</span><span class="sxs-lookup"><span data-stu-id="2b6b4-107">Clearing the binding removes the binding so that the value of the dependency property is changed to whatever it would have been without the binding.</span></span> <span data-ttu-id="2b6b4-108">Dabei kann es sich um einen Standardwert, einen geerbten Wert oder um einen Wert aus einer Datenvorlagenbindung handeln.</span><span class="sxs-lookup"><span data-stu-id="2b6b4-108">This value could be a default value, an inherited value, or a value from a data template binding.</span></span>  
  
 <span data-ttu-id="2b6b4-109">Um Bindungen aus allen möglichen Eigenschaften eines Objekts zu löschen, verwenden Sie <xref:System.Windows.Data.BindingOperations.ClearAllBindings%2A> .</span><span class="sxs-lookup"><span data-stu-id="2b6b4-109">To clear bindings from all possible properties on an object, use <xref:System.Windows.Data.BindingOperations.ClearAllBindings%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b6b4-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b6b4-110">See also</span></span>

- <xref:System.Windows.Data.BindingOperations>
- [<span data-ttu-id="2b6b4-111">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="2b6b4-111">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="2b6b4-112">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="2b6b4-112">How-to Topics</span></span>](data-binding-how-to-topics.md)
