---
title: 'Vorgehensweise: Verwenden von Ausschneiden mit einem Bereich'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- regions [Windows Forms], clipping
- regions [Windows Forms], restricting drawing surface
ms.assetid: 43d121b4-e14c-4901-b25c-2d6c25ba4e29
ms.openlocfilehash: e62be137b36a2f369c02151466154f6b3bab090b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975860"
---
# <a name="how-to-use-clipping-with-a-region"></a><span data-ttu-id="c818c-102">Vorgehensweise: Verwenden von Ausschneiden mit einem Bereich</span><span class="sxs-lookup"><span data-stu-id="c818c-102">How to: Use Clipping with a Region</span></span>
<span data-ttu-id="c818c-103">Eine der Eigenschaften der- <xref:System.Drawing.Graphics> Klasse ist der Clip Bereich.</span><span class="sxs-lookup"><span data-stu-id="c818c-103">One of the properties of the <xref:System.Drawing.Graphics> class is the clip region.</span></span> <span data-ttu-id="c818c-104">Alle Zeichnungen, die von einem bestimmten Objekt durchgeführt werden <xref:System.Drawing.Graphics> , sind auf den Ausschneide Bereich dieses <xref:System.Drawing.Graphics> Objekts beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c818c-104">All drawing done by a given <xref:System.Drawing.Graphics> object is restricted to the clip region of that <xref:System.Drawing.Graphics> object.</span></span> <span data-ttu-id="c818c-105">Sie können den Clip Bereich festlegen, indem Sie die- <xref:System.Drawing.Graphics.SetClip%2A> Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c818c-105">You can set the clip region by calling the <xref:System.Drawing.Graphics.SetClip%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c818c-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c818c-106">Example</span></span>  
 <span data-ttu-id="c818c-107">Im folgenden Beispiel wird ein Pfad erstellt, der aus einem einzelnen Polygon besteht.</span><span class="sxs-lookup"><span data-stu-id="c818c-107">The following example constructs a path that consists of a single polygon.</span></span> <span data-ttu-id="c818c-108">Anschließend erstellt der Code basierend auf diesem Pfad einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="c818c-108">Then the code constructs a region, based on that path.</span></span> <span data-ttu-id="c818c-109">Der Bereich wird an die <xref:System.Drawing.Graphics.SetClip%2A> -Methode eines <xref:System.Drawing.Graphics> -Objekts weitergegeben, und dann werden zwei Zeichen folgen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c818c-109">The region is passed to the <xref:System.Drawing.Graphics.SetClip%2A> method of a <xref:System.Drawing.Graphics> object, and then two strings are drawn.</span></span>  
  
 <span data-ttu-id="c818c-110">Die folgende Abbildung zeigt die ausgeschnittenen Zeichen folgen:</span><span class="sxs-lookup"><span data-stu-id="c818c-110">The following illustration shows the clipped strings:</span></span>  
  
 ![Screenshot, in dem abgeschnittene Zeichen folgen angezeigt werden.](./media/how-to-use-clipping-with-a-region/clipped-strings-polygon.png)  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.MiscLegacyTopics#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c818c-112">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="c818c-112">Compiling the Code</span></span>  
 <span data-ttu-id="c818c-113">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="c818c-113">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c818c-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c818c-114">See also</span></span>

- [<span data-ttu-id="c818c-115">Bereiche in GDI+</span><span class="sxs-lookup"><span data-stu-id="c818c-115">Regions in GDI+</span></span>](regions-in-gdi.md)
- [<span data-ttu-id="c818c-116">Verwenden von Bereichen</span><span class="sxs-lookup"><span data-stu-id="c818c-116">Using Regions</span></span>](using-regions.md)
