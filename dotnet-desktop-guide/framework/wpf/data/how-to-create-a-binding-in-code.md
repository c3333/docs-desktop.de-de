---
title: 'Gewusst wie: Erstellen einer Bindung in Code'
description: Erfahren Sie, wie Sie eine Bindung im Code in einer Windows Presentation Foundation Anwendung erstellen, indem Sie die SetBinding-Methode direkt aufrufen.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- binding data [WPF], creating
- data binding [WPF], creating
ms.assetid: 1a606db9-cf5f-42ed-a1c5-9e4722ec77a0
ms.openlocfilehash: ed94118123823b4904896ddfbf2d5b429fc1012b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977182"
---
# <a name="how-to-create-a-binding-in-code"></a><span data-ttu-id="0bc54-103">Gewusst wie: Erstellen einer Bindung in Code</span><span class="sxs-lookup"><span data-stu-id="0bc54-103">How to: Create a Binding in Code</span></span>

<span data-ttu-id="0bc54-104">In diesem Beispiel wird gezeigt, wie ein im Code erstellt und festgelegt wird <xref:System.Windows.Data.Binding> .</span><span class="sxs-lookup"><span data-stu-id="0bc54-104">This example shows how to create and set a <xref:System.Windows.Data.Binding> in code.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0bc54-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0bc54-105">Example</span></span>  

 <span data-ttu-id="0bc54-106">Die <xref:System.Windows.FrameworkElement> -Klasse und die- <xref:System.Windows.FrameworkContentElement> Klasse machen beide eine- `SetBinding` Methode verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0bc54-106">The <xref:System.Windows.FrameworkElement> class and the <xref:System.Windows.FrameworkContentElement> class both expose a `SetBinding` method.</span></span> <span data-ttu-id="0bc54-107">Wenn Sie ein Element binden, das eine dieser Klassen erbt, können Sie die <xref:System.Windows.FrameworkElement.SetBinding%2A> Methode direkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0bc54-107">If you are binding an element that inherits either of these classes, you can call the <xref:System.Windows.FrameworkElement.SetBinding%2A> method directly.</span></span>  
  
 <span data-ttu-id="0bc54-108">Im folgenden Beispiel wird eine Klasse namens erstellt, `MyData` die eine Eigenschaft mit dem Namen enthält `MyDataProperty` .</span><span class="sxs-lookup"><span data-stu-id="0bc54-108">The following example creates a class named, `MyData`, which contains a property named `MyDataProperty`.</span></span>  
  
 [!code-csharp[CodeOnlyBinding#DataObject](~/samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/MyData.cs#dataobject)]
 [!code-vb[CodeOnlyBinding#DataObject](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/MyData.vb#dataobject)]  
  
 <span data-ttu-id="0bc54-109">Im folgenden Beispiel wird gezeigt, wie ein Bindungs Objekt erstellt wird, um die Quelle der Bindung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0bc54-109">The following example shows how to create a binding object to set the source of the binding.</span></span>  <span data-ttu-id="0bc54-110">Im Beispiel wird verwendet, <xref:System.Windows.FrameworkElement.SetBinding%2A> um die- <xref:System.Windows.Controls.TextBlock.Text%2A> Eigenschaft von `myText` , die ein-Steuerelement ist <xref:System.Windows.Controls.TextBlock> , an zu binden `MyDataProperty` .</span><span class="sxs-lookup"><span data-stu-id="0bc54-110">The example uses <xref:System.Windows.FrameworkElement.SetBinding%2A> to bind the <xref:System.Windows.Controls.TextBlock.Text%2A> property of `myText`, which is a <xref:System.Windows.Controls.TextBlock> control, to `MyDataProperty`.</span></span>  
  
 [!code-csharp[CodeOnlyBinding#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#1)]
 [!code-vb[CodeOnlyBinding#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#1)]  
  
 <span data-ttu-id="0bc54-111">Das Codebeispiel für den gesamten Code finden Sie unter Beispiel für reine [Code Bindung](/previous-versions/dotnet/netframework-3.5/ms771500(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="0bc54-111">For the complete code sample, see [Code-only Binding Sample](/previous-versions/dotnet/netframework-3.5/ms771500(v=vs.90)).</span></span>  
  
 <span data-ttu-id="0bc54-112">Statt aufrufen <xref:System.Windows.FrameworkElement.SetBinding%2A> , können Sie die statische- <xref:System.Windows.Data.BindingOperations.SetBinding%2A> Methode der- <xref:System.Windows.Data.BindingOperations> Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="0bc54-112">Instead of calling <xref:System.Windows.FrameworkElement.SetBinding%2A>, you can use the <xref:System.Windows.Data.BindingOperations.SetBinding%2A> static method of the <xref:System.Windows.Data.BindingOperations> class.</span></span> <span data-ttu-id="0bc54-113">Im folgenden Beispiel wird <xref:System.Windows.Data.BindingOperations.SetBinding%2A?displayProperty=nameWithType> anstelle von aufgerufen, <xref:System.Windows.FrameworkElement.SetBinding%2A?displayProperty=nameWithType> um an zu binden `myText` `myDataProperty` .</span><span class="sxs-lookup"><span data-stu-id="0bc54-113">The following example, calls <xref:System.Windows.Data.BindingOperations.SetBinding%2A?displayProperty=nameWithType> instead of <xref:System.Windows.FrameworkElement.SetBinding%2A?displayProperty=nameWithType> to bind `myText` to `myDataProperty`.</span></span>  
  
 [!code-csharp[CodeOnlyBinding#BOSetBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#bosetbinding)]
 [!code-vb[CodeOnlyBinding#BOSetBinding](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#bosetbinding)]  
  
## <a name="see-also"></a><span data-ttu-id="0bc54-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bc54-114">See also</span></span>

- [<span data-ttu-id="0bc54-115">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="0bc54-115">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="0bc54-116">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="0bc54-116">How-to Topics</span></span>](data-binding-how-to-topics.md)
