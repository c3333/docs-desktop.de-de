---
title: 'Gewusst wie: Auflisten des Zeichnungsinhalts eines visuellen Objekts'
ms.date: 03/30/2017
helpviewer_keywords:
- retrieving the DrawingGroup value of a Visual [WPF]
- enumerating the contents of a Visual [WPF]
ms.assetid: 2974ddb3-2997-4713-8fd2-e93d549c58a8
ms.openlocfilehash: 25aa0c3706005c1e16cedd7e06914db764545ebb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977854"
---
# <a name="how-to-enumerate-drawing-content-of-a-visual"></a><span data-ttu-id="15888-102">Gewusst wie: Auflisten des Zeichnungsinhalts eines visuellen Objekts</span><span class="sxs-lookup"><span data-stu-id="15888-102">How to: Enumerate Drawing Content of a Visual</span></span>
<span data-ttu-id="15888-103">Das- <xref:System.Windows.Media.Drawing> Objekt stellt ein Objektmodell für das Auflisten des Inhalts eines bereit <xref:System.Windows.Media.Visual> .</span><span class="sxs-lookup"><span data-stu-id="15888-103">The <xref:System.Windows.Media.Drawing> object provide an object model for enumerating the contents of a <xref:System.Windows.Media.Visual>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="15888-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="15888-104">Example</span></span>  
 <span data-ttu-id="15888-105">Im folgenden Beispiel wird die <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> -Methode verwendet, um den <xref:System.Windows.Media.DrawingGroup> Wert eines abzurufen <xref:System.Windows.Media.Visual> und ihn aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="15888-105">The following example uses the <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> method to retrieve the <xref:System.Windows.Media.DrawingGroup> value of a <xref:System.Windows.Media.Visual> and enumerate it.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="15888-106">Wenn Sie den Inhalt der Visualisierung auflisten, rufen Sie <xref:System.Windows.Media.Drawing> Objekte ab, und nicht die zugrunde liegende Darstellung der Renderingdaten als Liste von Vektorgrafik Anweisungs Listen.</span><span class="sxs-lookup"><span data-stu-id="15888-106">When you are enumerating the contents of the visual, you are retrieving <xref:System.Windows.Media.Drawing> objects, and not the underlying representation of the render data as a vector graphics instruction list.</span></span> <span data-ttu-id="15888-107">Weitere Informationen finden Sie unter [Übersicht über das WPF-Grafikenrendering](wpf-graphics-rendering-overview.md).</span><span class="sxs-lookup"><span data-stu-id="15888-107">For more information, see [WPF Graphics Rendering Overview](wpf-graphics-rendering-overview.md).</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMRetrieveDrawings](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/EnumerateDrawingsExample.xaml.cs#graphicsmmretrievedrawings)]  
  
## <a name="see-also"></a><span data-ttu-id="15888-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15888-108">See also</span></span>

- <xref:System.Windows.Media.Drawing>
- <xref:System.Windows.Media.DrawingGroup>
- <xref:System.Windows.Media.VisualTreeHelper>
- [<span data-ttu-id="15888-109">Übersicht über Zeichnungsobjekte</span><span class="sxs-lookup"><span data-stu-id="15888-109">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="15888-110">Übersicht über das WPF-Grafikrendering</span><span class="sxs-lookup"><span data-stu-id="15888-110">WPF Graphics Rendering Overview</span></span>](wpf-graphics-rendering-overview.md)
