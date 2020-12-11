---
title: 'Gewusst wie: Erstellen eines schreibgeschützten Freezable-Objekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], making read-only
ms.assetid: 6c544b7d-d3c9-4736-aa90-4b8728234ccb
ms.openlocfilehash: b8dcbec18977d46bd47b82f528deb2eeccc4e441
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976879"
---
# <a name="how-to-make-a-freezable-read-only"></a><span data-ttu-id="1f6c0-102">Gewusst wie: Erstellen eines schreibgeschützten Freezable-Objekts</span><span class="sxs-lookup"><span data-stu-id="1f6c0-102">How to: Make a Freezable Read-Only</span></span>
<span data-ttu-id="1f6c0-103">Dieses Beispiel zeigt, wie Sie einen schreibgeschützten Vorgang <xref:System.Windows.Freezable> durch Aufrufen seiner-Methode durchführen <xref:System.Windows.Freezable.Freeze%2A> .</span><span class="sxs-lookup"><span data-stu-id="1f6c0-103">This example shows how to make a <xref:System.Windows.Freezable> read-only by calling its <xref:System.Windows.Freezable.Freeze%2A> method.</span></span>  
  
 <span data-ttu-id="1f6c0-104">Ein-Objekt kann nicht fixiert <xref:System.Windows.Freezable> werden, wenn eine der folgenden Bedingungen `true` dem-Objekt entspricht:</span><span class="sxs-lookup"><span data-stu-id="1f6c0-104">You cannot freeze a <xref:System.Windows.Freezable> object if any one of the following conditions is `true` about the object:</span></span>  
  
- <span data-ttu-id="1f6c0-105">Sie verfügt über animierte oder Daten gebundene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1f6c0-105">It has animated or data bound properties.</span></span>  
  
- <span data-ttu-id="1f6c0-106">Sie verfügt über Eigenschaften, die durch eine dynamische Ressource festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1f6c0-106">It has properties that are set by a dynamic resource.</span></span> <span data-ttu-id="1f6c0-107">Weitere Informationen zu dynamischen Ressourcen finden Sie in den [XAML-Ressourcen](/dotnet/desktop-wpf/fundamentals/xaml-resources-define).</span><span class="sxs-lookup"><span data-stu-id="1f6c0-107">For more information about dynamic resources, see the [XAML Resources](/dotnet/desktop-wpf/fundamentals/xaml-resources-define).</span></span>  
  
- <span data-ttu-id="1f6c0-108">Sie enthält <xref:System.Windows.Freezable> untergeordnete Objekte, die nicht eingefroren werden können.</span><span class="sxs-lookup"><span data-stu-id="1f6c0-108">It contains <xref:System.Windows.Freezable> sub-objects that cannot be frozen.</span></span>  
  
 <span data-ttu-id="1f6c0-109">Wenn diese Bedingungen `false` für Ihr <xref:System.Windows.Freezable> Objekt gelten und Sie diese nicht ändern möchten, sollten Sie es in Erwägung gezogen, um Leistungsvorteile zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="1f6c0-109">If these conditions are `false` for your <xref:System.Windows.Freezable> object and you do not intend to modify it, consider freezing it to gain performance benefits.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1f6c0-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1f6c0-110">Example</span></span>  
 <span data-ttu-id="1f6c0-111">Im folgenden Beispiel wird ein- <xref:System.Windows.Media.SolidColorBrush> Objekt, das einen Objekttyp ist, eingefroren <xref:System.Windows.Freezable> .</span><span class="sxs-lookup"><span data-stu-id="1f6c0-111">The following example freezes a <xref:System.Windows.Media.SolidColorBrush>, which is a type of <xref:System.Windows.Freezable> object.</span></span>  
  
 [!code-csharp[freezablesample_procedural#FreezeExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#freezeexample1)]
 [!code-vb[freezablesample_procedural#FreezeExample1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#freezeexample1)]  
  
 <span data-ttu-id="1f6c0-112">Weitere Informationen zu Objekten finden Sie in der Übersicht über frei wählbare <xref:System.Windows.Freezable> [Objekte](freezable-objects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1f6c0-112">For more information about <xref:System.Windows.Freezable> objects, see the [Freezable Objects Overview](freezable-objects-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f6c0-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f6c0-113">See also</span></span>

- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CanFreeze%2A>
- <xref:System.Windows.Freezable.Freeze%2A>
- [<span data-ttu-id="1f6c0-114">Übersicht über Freezable-Objekte</span><span class="sxs-lookup"><span data-stu-id="1f6c0-114">Freezable Objects Overview</span></span>](freezable-objects-overview.md)
- [<span data-ttu-id="1f6c0-115">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="1f6c0-115">How-to Topics</span></span>](base-elements-how-to-topics.md)
