---
title: 'Vorgehensweise: Anwenden einer Zeichnung auf ein 3D-Modell'
ms.date: 03/30/2017
helpviewer_keywords:
- drawings [WPF], applying to 3D models
- 3D models [WPF], applying drawings to
ms.assetid: 68357577-b7fc-446e-8be9-a8cc7df3a350
ms.openlocfilehash: 794ca9a48bcec42c3eee4d8da143f3ae9d27fcf2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977272"
---
# <a name="how-to-apply-a-drawing-to-a-3d-model"></a><span data-ttu-id="f435c-102">Vorgehensweise: Anwenden einer Zeichnung auf ein 3D-Modell</span><span class="sxs-lookup"><span data-stu-id="f435c-102">How to: Apply a Drawing to a 3D Model</span></span>

<span data-ttu-id="f435c-103">In diesem Beispiel wird gezeigt, wie Sie <xref:System.Windows.Media.DrawingBrush> als <xref:System.Windows.Media.Media3D.Material> auf ein 3D-Modell angewendetes verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f435c-103">This example shows how to use a <xref:System.Windows.Media.DrawingBrush> as the <xref:System.Windows.Media.Media3D.Material> applied to a 3D model.</span></span>

<span data-ttu-id="f435c-104">Im folgenden Code wird ein <xref:System.Windows.Media.DrawingGroup> als Inhalt eines definiert <xref:System.Windows.Media.DrawingBrush> .</span><span class="sxs-lookup"><span data-stu-id="f435c-104">The following code defines a <xref:System.Windows.Media.DrawingGroup> as the content of a <xref:System.Windows.Media.DrawingBrush>.</span></span>  <span data-ttu-id="f435c-105">Der <xref:System.Windows.Media.DrawingBrush> wird als <xref:System.Windows.Media.Media3D.DiffuseMaterial.Brush%2A> -Eigenschaft des festgelegt <xref:System.Windows.Media.Media3D.DiffuseMaterial> , der auf eine 3D-Ebene angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f435c-105">The <xref:System.Windows.Media.DrawingBrush> is set as the <xref:System.Windows.Media.Media3D.DiffuseMaterial.Brush%2A> property of the <xref:System.Windows.Media.Media3D.DiffuseMaterial> applied to a 3D plane.</span></span>

> [!NOTE]
> <span data-ttu-id="f435c-106">Es ist häufig wünschenswert, komplexe Objekte und Werte wie die nachfolgende Zeichnung als Ressourcen zu definieren, die wieder verwendet werden können, und den Code zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="f435c-106">It is often desirable to define complex objects and values like the drawing below as resources which can be reused and simplify your code.</span></span> <span data-ttu-id="f435c-107">Weitere Informationen finden Sie unter [XAML-Ressourcen](/dotnet/desktop-wpf/fundamentals/xaml-resources-define) .</span><span class="sxs-lookup"><span data-stu-id="f435c-107">See [XAML Resources](/dotnet/desktop-wpf/fundamentals/xaml-resources-define) for more information.</span></span>

[!code-xaml[3DGallery_snip#ApplyDrawingToMaterialInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ApplyDrawingToMaterialExample.xaml#applydrawingtomaterialinline1)]

## <a name="example"></a><span data-ttu-id="f435c-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f435c-108">Example</span></span>

<span data-ttu-id="f435c-109">Der folgende Code zeigt das gesamte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f435c-109">The following code shows the entire sample.</span></span>

[!code-xaml[3DGallery_snip#ApplyDrawingToMaterialExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ApplyDrawingToMaterialExample.xaml#applydrawingtomaterialexamplewholepage)]

## <a name="see-also"></a><span data-ttu-id="f435c-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f435c-110">See also</span></span>

- [<span data-ttu-id="f435c-111">XAML-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f435c-111">XAML Resources</span></span>](/dotnet/desktop-wpf/fundamentals/xaml-resources-define)
- [<span data-ttu-id="f435c-112">Erstellen einer 3D-Szene</span><span class="sxs-lookup"><span data-stu-id="f435c-112">Create a 3D Scene</span></span>](how-to-create-a-3-d-scene.md)
- [<span data-ttu-id="f435c-113">Übersicht über Zeichnungsobjekte</span><span class="sxs-lookup"><span data-stu-id="f435c-113">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="f435c-114">Übersicht über 3D-Grafiken</span><span class="sxs-lookup"><span data-stu-id="f435c-114">3D Graphics Overview</span></span>](3-d-graphics-overview.md)
