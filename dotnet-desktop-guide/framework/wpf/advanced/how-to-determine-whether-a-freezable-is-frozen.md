---
title: 'Gewusst wie: Bestimmen, ob ein Freezable-Objekt fixiert ist'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], determining if frozen
ms.assetid: 92e58baa-ee12-4a9e-ac3a-ca458807a8b2
ms.openlocfilehash: 6a63862d35f2c40289ea6445eb3dab8a2abe4a61
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976682"
---
# <a name="how-to-determine-whether-a-freezable-is-frozen"></a><span data-ttu-id="97842-102">Gewusst wie: Bestimmen, ob ein Freezable-Objekt fixiert ist</span><span class="sxs-lookup"><span data-stu-id="97842-102">How to: Determine Whether a Freezable Is Frozen</span></span>
<span data-ttu-id="97842-103">Dieses Beispiel zeigt, wie Sie bestimmen können, ob ein- <xref:System.Windows.Freezable> Objekt eingefroren ist.</span><span class="sxs-lookup"><span data-stu-id="97842-103">This example shows how to determine whether a <xref:System.Windows.Freezable> object is frozen.</span></span> <span data-ttu-id="97842-104">Wenn Sie versuchen, ein fixierte <xref:System.Windows.Freezable> Objekt zu ändern, wird eine ausgelöst <xref:System.InvalidOperationException> .</span><span class="sxs-lookup"><span data-stu-id="97842-104">If you try to modify a frozen <xref:System.Windows.Freezable> object, it throws an <xref:System.InvalidOperationException>.</span></span> <span data-ttu-id="97842-105">Um das Auslösen dieser Ausnahme zu vermeiden, verwenden Sie die- <xref:System.Windows.Freezable.IsFrozen%2A> Eigenschaft des- <xref:System.Windows.Freezable> Objekts, um zu bestimmen, ob es eingefroren ist.</span><span class="sxs-lookup"><span data-stu-id="97842-105">To avoid throwing this exception, use the <xref:System.Windows.Freezable.IsFrozen%2A> property of the <xref:System.Windows.Freezable> object to determine whether it is frozen.</span></span>  
  
## <a name="example"></a><span data-ttu-id="97842-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="97842-106">Example</span></span>  
 <span data-ttu-id="97842-107">Im folgenden Beispiel wird ein-Objekt einfriert <xref:System.Windows.Media.SolidColorBrush> und dann mit der- <xref:System.Windows.Freezable.IsFrozen%2A> Eigenschaft getestet, um zu bestimmen, ob es eingefroren ist.</span><span class="sxs-lookup"><span data-stu-id="97842-107">The following example freezes a <xref:System.Windows.Media.SolidColorBrush> and then tests it by using the <xref:System.Windows.Freezable.IsFrozen%2A> property to determine whether it is frozen.</span></span>  
  
 [!code-csharp[freezablesample_procedural#CheckIsFrozenExample](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#checkisfrozenexample)]
 [!code-vb[freezablesample_procedural#CheckIsFrozenExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#checkisfrozenexample)]  
  
 <span data-ttu-id="97842-108">Weitere Informationen zu Objekten finden Sie in der Übersicht über frei wählbare <xref:System.Windows.Freezable> [Objekte](freezable-objects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="97842-108">For more information about <xref:System.Windows.Freezable> objects, see the [Freezable Objects Overview](freezable-objects-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97842-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97842-109">See also</span></span>

- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.IsFrozen%2A>
- [<span data-ttu-id="97842-110">Übersicht über Freezable-Objekte</span><span class="sxs-lookup"><span data-stu-id="97842-110">Freezable Objects Overview</span></span>](freezable-objects-overview.md)
- [<span data-ttu-id="97842-111">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="97842-111">How-to Topics</span></span>](base-elements-how-to-topics.md)
