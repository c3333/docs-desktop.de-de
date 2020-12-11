---
title: 'Gewusst wie: Entfernen eines Adorners aus einem Element'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: 97cf4d9f-0596-429e-8526-32a30aa4ae99
ms.openlocfilehash: 256dd6fa0117f88aec2ef6b60c6dcd4c33b57855
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977035"
---
# <a name="how-to-remove-an-adorner-from-an-element"></a><span data-ttu-id="b51d8-102">Gewusst wie: Entfernen eines Adorners aus einem Element</span><span class="sxs-lookup"><span data-stu-id="b51d8-102">How to: Remove an Adorner from an Element</span></span>
<span data-ttu-id="b51d8-103">In diesem Beispiel wird gezeigt, wie ein bestimmter Funktions Indikator Programm gesteuert aus einem angegebenen entfernt wird <xref:System.Windows.UIElement> .</span><span class="sxs-lookup"><span data-stu-id="b51d8-103">This example shows how to programmatically remove a specific adorner from a specified <xref:System.Windows.UIElement>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b51d8-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b51d8-104">Example</span></span>  
 <span data-ttu-id="b51d8-105">In diesem ausführlichen Codebeispiel wird der erste Funktions Indikator in dem Array von Adornern entfernt, das von zurückgegeben wird <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> .</span><span class="sxs-lookup"><span data-stu-id="b51d8-105">This verbose code example removes the first adorner in the array of adorners returned by <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span></span>  <span data-ttu-id="b51d8-106">In diesem Beispiel werden die Adorner für ein <xref:System.Windows.UIElement> benanntes *MyTextBox*-Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b51d8-106">This example happens to retrieve the adorners on a <xref:System.Windows.UIElement> named *myTextBox*.</span></span>  <span data-ttu-id="b51d8-107">Wenn das im-aufrufelement angegebene Element <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> keine Adorner hat, `null` wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b51d8-107">If the element specified in the call to <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> has no adorners, `null` is returned.</span></span>  <span data-ttu-id="b51d8-108">Dieser Code prüft explizit nach einem NULL-Array und eignet sich am besten für Anwendungen, bei denen erwartet wird, dass ein NULL-Array relativ häufig ist.</span><span class="sxs-lookup"><span data-stu-id="b51d8-108">This code explicitly checks for a null array, and is best suited for applications where a null array is expected to be relatively common.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveSpecificAdornerLong](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removespecificadornerlong)]
 [!code-vb[AdornersMiscCode#_RemoveSpecificAdornerLong](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removespecificadornerlong)]  
  
## <a name="example"></a><span data-ttu-id="b51d8-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b51d8-109">Example</span></span>  
 <span data-ttu-id="b51d8-110">Dieses komprimierte Codebeispiel ist funktional äquivalent zu dem oben gezeigten ausführlichen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="b51d8-110">This condensed code example is functionally equivalent to the verbose example shown above.</span></span> <span data-ttu-id="b51d8-111">In diesem Code wird nicht explizit nach einem NULL-Array gesucht, daher ist es möglich, dass eine- <xref:System.NullReferenceException> Ausnahme ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="b51d8-111">This code does not explicitly check for a null array, so it is possible that a <xref:System.NullReferenceException> exception may be raised.</span></span>  <span data-ttu-id="b51d8-112">Dieser Code eignet sich am besten für Anwendungen, bei denen erwartet wird, dass ein NULL-Array selten vorkommt.</span><span class="sxs-lookup"><span data-stu-id="b51d8-112">This code is best suited for applications where a null array is expected to be rare.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveSpecificAdornerShort](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removespecificadornershort)]
 [!code-vb[AdornersMiscCode#_RemoveSpecificAdornerShort](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removespecificadornershort)]  
  
## <a name="see-also"></a><span data-ttu-id="b51d8-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b51d8-113">See also</span></span>

- [<span data-ttu-id="b51d8-114">Übersicht über Adorner</span><span class="sxs-lookup"><span data-stu-id="b51d8-114">Adorners Overview</span></span>](adorners-overview.md)
