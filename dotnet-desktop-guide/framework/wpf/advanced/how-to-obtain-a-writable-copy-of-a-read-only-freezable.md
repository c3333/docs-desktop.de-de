---
title: 'Gewusst wie: Erstellen einer überschreibbaren Kopie eines schreibgeschützten Freezable-Objekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cloning Freezable objects [WPF]
- Freezable objects [WPF], modifiable clones
ms.assetid: d028de61-bbe9-4d62-b656-8fe3b1b2ca24
ms.openlocfilehash: 910c5dada6ca82f68992722e4df6b35f9f7497c7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977752"
---
# <a name="how-to-obtain-a-writable-copy-of-a-read-only-freezable"></a><span data-ttu-id="d0629-102">Gewusst wie: Erstellen einer überschreibbaren Kopie eines schreibgeschützten Freezable-Objekts</span><span class="sxs-lookup"><span data-stu-id="d0629-102">How to: Obtain a Writable Copy of a Read-Only Freezable</span></span>
<span data-ttu-id="d0629-103">Dieses Beispiel zeigt, wie Sie die- <xref:System.Windows.Freezable.Clone%2A> Methode verwenden, um eine schreibgeschützte Kopie eines schreibgeschützten zu erstellen <xref:System.Windows.Freezable> .</span><span class="sxs-lookup"><span data-stu-id="d0629-103">This example shows how to use the <xref:System.Windows.Freezable.Clone%2A> method to create a writable copy of a read-only <xref:System.Windows.Freezable>.</span></span>  
  
 <span data-ttu-id="d0629-104">Nachdem ein- <xref:System.Windows.Freezable> Objekt als schreibgeschützt ("eingefroren") markiert wurde, kann es nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d0629-104">After a <xref:System.Windows.Freezable> object is marked as read-only ("frozen"), you cannot modify it.</span></span> <span data-ttu-id="d0629-105">Sie können jedoch die- <xref:System.Windows.Freezable.Clone%2A> Methode verwenden, um einen änderbaren Klon des fixierten Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d0629-105">However, you can use the <xref:System.Windows.Freezable.Clone%2A> method to create a modifiable clone of the frozen object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d0629-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d0629-106">Example</span></span>  
 <span data-ttu-id="d0629-107">Im folgenden Beispiel wird ein änderbarer Klon eines fixierten <xref:System.Windows.Media.SolidColorBrush> Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="d0629-107">The following example creates a modifiable clone of a frozen <xref:System.Windows.Media.SolidColorBrush> object.</span></span>  
  
 [!code-csharp[freezablesample_procedural#CloneExample](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#cloneexample)]
 [!code-vb[freezablesample_procedural#CloneExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#cloneexample)]  
  
 <span data-ttu-id="d0629-108">Weitere Informationen zu Objekten finden Sie in der Übersicht über frei wählbare <xref:System.Windows.Freezable> [Objekte](freezable-objects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d0629-108">For more information about <xref:System.Windows.Freezable> objects, see the [Freezable Objects Overview](freezable-objects-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0629-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0629-109">See also</span></span>

- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CloneCurrentValue%2A>
- [<span data-ttu-id="d0629-110">Übersicht über Freezable-Objekte</span><span class="sxs-lookup"><span data-stu-id="d0629-110">Freezable Objects Overview</span></span>](freezable-objects-overview.md)
- [<span data-ttu-id="d0629-111">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="d0629-111">How-to Topics</span></span>](base-elements-how-to-topics.md)
