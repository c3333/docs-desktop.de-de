---
title: 'Vorgehensweise: Verwenden von Treffertests mit einem Bereich'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [Windows Forms], using regions
- regions [Windows Forms], hit testing
ms.assetid: 3a4c07cb-a40a-4d14-ad35-008f531910a8
ms.openlocfilehash: 136f15f1364fb2aed791b4a61d0f11411b055967
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975854"
---
# <a name="how-to-use-hit-testing-with-a-region"></a><span data-ttu-id="ff087-102">Vorgehensweise: Verwenden von Treffertests mit einem Bereich</span><span class="sxs-lookup"><span data-stu-id="ff087-102">How to: Use Hit Testing with a Region</span></span>
<span data-ttu-id="ff087-103">Der Zweck von Treffer Tests besteht darin, zu bestimmen, ob sich der Cursor über einem bestimmten Objekt befindet, z. b. ein Symbol oder eine Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="ff087-103">The purpose of hit testing is to determine whether the cursor is over a given object, such as an icon or a button.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ff087-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ff087-104">Example</span></span>  
 <span data-ttu-id="ff087-105">Im folgenden Beispiel wird ein Plus förmiger Bereich erstellt, indem die Union zweier rechteckiger Bereiche gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="ff087-105">The following example creates a plus-shaped region by forming the union of two rectangular regions.</span></span> <span data-ttu-id="ff087-106">Angenommen, die Variable `point` enthält den Speicherort des letzten Click.</span><span class="sxs-lookup"><span data-stu-id="ff087-106">Assume that the variable `point` holds the location of the most recent click.</span></span> <span data-ttu-id="ff087-107">Der Code prüft, ob `point` im Plus-förmigen Bereich ist.</span><span class="sxs-lookup"><span data-stu-id="ff087-107">The code checks to see whether `point` is in the plus-shaped region.</span></span> <span data-ttu-id="ff087-108">Wenn sich der Punkt in der Region (einem Treffer) befindet, wird der Bereich mit einem nicht transparenten roten Pinsel gefüllt.</span><span class="sxs-lookup"><span data-stu-id="ff087-108">If the point is in the region (a hit), the region is filled with an opaque red brush.</span></span> <span data-ttu-id="ff087-109">Andernfalls wird der Bereich mit einem semitransparenten roten Pinsel gefüllt.</span><span class="sxs-lookup"><span data-stu-id="ff087-109">Otherwise, the region is filled with a semitransparent red brush.</span></span>  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.MiscLegacyTopics#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ff087-110">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="ff087-110">Compiling the Code</span></span>  
 <span data-ttu-id="ff087-111">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="ff087-111">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff087-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff087-112">See also</span></span>

- <xref:System.Drawing.Region>
- [<span data-ttu-id="ff087-113">Bereiche in GDI+</span><span class="sxs-lookup"><span data-stu-id="ff087-113">Regions in GDI+</span></span>](regions-in-gdi.md)
- [<span data-ttu-id="ff087-114">Vorgehensweise: Verwenden von Ausschneiden mit einem Bereich</span><span class="sxs-lookup"><span data-stu-id="ff087-114">How to: Use Clipping with a Region</span></span>](how-to-use-clipping-with-a-region.md)
