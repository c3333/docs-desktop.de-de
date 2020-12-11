---
title: 'Vorgehensweise: Erstellen eines Volltonpinsels'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- solid color brushes
- brushes [Windows Forms], examples
- brushes [Windows Forms], creating solid
ms.assetid: 85c3fe7d-fb1d-4591-8a9f-d75b556b90af
ms.openlocfilehash: ed9ec1f52b41c83b3cc6e36dedf97f1c00db42e6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974831"
---
# <a name="how-to-create-a-solid-brush"></a><span data-ttu-id="fbf87-102">Vorgehensweise: Erstellen eines Volltonpinsels</span><span class="sxs-lookup"><span data-stu-id="fbf87-102">How to: Create a Solid Brush</span></span>
<span data-ttu-id="fbf87-103">In diesem Beispiel wird ein- <xref:System.Drawing.SolidBrush> Objekt erstellt, das von einem- <xref:System.Drawing.Graphics> Objekt zum Auffüllen von Formen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fbf87-103">This example creates a <xref:System.Drawing.SolidBrush> object that can be used by a <xref:System.Drawing.Graphics> object for filling shapes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fbf87-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fbf87-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#1)]
 [!code-csharp[System.Drawing.ConceptualHowTos#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#1)]
 [!code-vb[System.Drawing.ConceptualHowTos#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#1)]  
  
## <a name="robust-programming"></a><span data-ttu-id="fbf87-105">Stabile Programmierung</span><span class="sxs-lookup"><span data-stu-id="fbf87-105">Robust Programming</span></span>  
 <span data-ttu-id="fbf87-106">Nachdem Sie die Verwendung abgeschlossen haben, sollten Sie <xref:System.IDisposable.Dispose%2A> für Objekte mit Systemressourcen (z. b. Pinsel Objekten) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="fbf87-106">After you have finished using them, you should call <xref:System.IDisposable.Dispose%2A> on objects that consume system resources, such as brush objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fbf87-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbf87-107">See also</span></span>

- <xref:System.Drawing.SolidBrush>
- <xref:System.Drawing.Brush>
- [<span data-ttu-id="fbf87-108">Erste Schritte mit Grafikprogrammierung</span><span class="sxs-lookup"><span data-stu-id="fbf87-108">Getting Started with Graphics Programming</span></span>](getting-started-with-graphics-programming.md)
- [<span data-ttu-id="fbf87-109">Pinsel und gefüllte Formen in GDI+</span><span class="sxs-lookup"><span data-stu-id="fbf87-109">Brushes and Filled Shapes in GDI+</span></span>](brushes-and-filled-shapes-in-gdi.md)
- [<span data-ttu-id="fbf87-110">Verwenden eines Pinsels zum Ausfüllen von Formen</span><span class="sxs-lookup"><span data-stu-id="fbf87-110">Using a Brush to Fill Shapes</span></span>](using-a-brush-to-fill-shapes.md)
