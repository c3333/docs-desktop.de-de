---
title: 'Gewusst wie: Entfernen aller Adorner aus einem Element'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: fe5303a3-b76e-4643-aafb-51419032b47b
ms.openlocfilehash: 8504bb1ec70de188033b2b092bbb66cf9da3dc11
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978149"
---
# <a name="how-to-remove-all-adorners-from-an-element"></a><span data-ttu-id="5f938-102">Gewusst wie: Entfernen aller Adorner aus einem Element</span><span class="sxs-lookup"><span data-stu-id="5f938-102">How to: Remove all Adorners from an Element</span></span>
<span data-ttu-id="5f938-103">In diesem Beispiel wird gezeigt, wie alle Adorner aus einem angegebenen Programm gesteuert entfernt werden <xref:System.Windows.UIElement> .</span><span class="sxs-lookup"><span data-stu-id="5f938-103">This example shows how to programmatically remove all adorners from a specified <xref:System.Windows.UIElement>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5f938-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5f938-104">Example</span></span>  
 <span data-ttu-id="5f938-105">Dieses ausführliche Codebeispiel entfernt alle Adorner in dem Array von Adornern, die von zurückgegeben werden <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> .</span><span class="sxs-lookup"><span data-stu-id="5f938-105">This verbose code example removes all of the adorners in the array of adorners returned by <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span></span>  <span data-ttu-id="5f938-106">In diesem Beispiel werden die Adorner für ein <xref:System.Windows.UIElement> benanntes *MyTextBox*-Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5f938-106">This example happens to retrieve the adorners on a <xref:System.Windows.UIElement> named *myTextBox*.</span></span>  <span data-ttu-id="5f938-107">Wenn das im-aufrufelement angegebene Element <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> keine Adorner hat, `null` wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f938-107">If the element specified in the call to <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> has no adorners, `null` is returned.</span></span>  <span data-ttu-id="5f938-108">Dieser Code prüft explizit nach einem NULL-Array und eignet sich am besten für Anwendungen, bei denen erwartet wird, dass ein NULL-Array relativ häufig ist.</span><span class="sxs-lookup"><span data-stu-id="5f938-108">This code explicitly checks for a null array, and is best suited for applications where a null array is expected to be relatively common.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersLong](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornerslong)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersLong](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornerslong)]  
  
## <a name="example"></a><span data-ttu-id="5f938-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5f938-109">Example</span></span>  
 <span data-ttu-id="5f938-110">Dieses komprimierte Codebeispiel ist funktional äquivalent zu dem oben gezeigten ausführlichen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="5f938-110">This condensed code example is functionally equivalent to the verbose example shown above.</span></span> <span data-ttu-id="5f938-111">In diesem Code wird nicht explizit nach einem NULL-Array gesucht, daher ist es möglich, dass eine- <xref:System.NullReferenceException> Ausnahme ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="5f938-111">This code does not explicitly check for a null array, so it is possible that a <xref:System.NullReferenceException> exception may be raised.</span></span>  <span data-ttu-id="5f938-112">Dieser Code eignet sich am besten für Anwendungen, bei denen erwartet wird, dass ein NULL-Array selten vorkommt.</span><span class="sxs-lookup"><span data-stu-id="5f938-112">This code is best suited for applications where a null array is expected to be rare.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersShort](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornersshort)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersShort](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornersshort)]  
  
## <a name="see-also"></a><span data-ttu-id="5f938-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f938-113">See also</span></span>

- [<span data-ttu-id="5f938-114">Übersicht über Adorner</span><span class="sxs-lookup"><span data-stu-id="5f938-114">Adorners Overview</span></span>](adorners-overview.md)
