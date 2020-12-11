---
title: 'Gewusst wie: Anwenden mehrerer Transformationen auf ein Objekt'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- grouping Transform objects [WPF]
- Transform objects [WPF], grouping
- graphics [WPF], grouping Transform objects
- TransformGroup [WPF]
ms.assetid: 98cd1921-12bc-4bf5-8193-529228fb7402
ms.openlocfilehash: 3ef11104b2a4fc775d29d2a388c9a70a69a3f10f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977764"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a><span data-ttu-id="b7e14-102">Gewusst wie: Anwenden mehrerer Transformationen auf ein Objekt</span><span class="sxs-lookup"><span data-stu-id="b7e14-102">How to: Apply Multiple Transforms to an Object</span></span>
<span data-ttu-id="b7e14-103">In diesem Beispiel wird gezeigt, wie ein-Objekt verwendet wird <xref:System.Windows.Media.TransformGroup> , um zwei oder mehr <xref:System.Windows.Media.Transform> Objekte in einem einzelnen zusammengesetzten zu gruppieren <xref:System.Windows.Media.Transform></span><span class="sxs-lookup"><span data-stu-id="b7e14-103">This example shows how to use a <xref:System.Windows.Media.TransformGroup> to group two or more <xref:System.Windows.Media.Transform> objects into a single composite <xref:System.Windows.Media.Transform>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b7e14-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b7e14-104">Example</span></span>  
 <span data-ttu-id="b7e14-105">Im folgenden Beispiel wird verwendet <xref:System.Windows.Media.TransformGroup> , um ein <xref:System.Windows.Media.ScaleTransform> und ein <xref:System.Windows.Media.RotateTransform> auf eine anzuwenden <xref:System.Windows.Controls.Button> .</span><span class="sxs-lookup"><span data-stu-id="b7e14-105">The following example uses a <xref:System.Windows.Media.TransformGroup> to apply a <xref:System.Windows.Media.ScaleTransform> and a <xref:System.Windows.Media.RotateTransform> to a <xref:System.Windows.Controls.Button>.</span></span>  
  
 [!code-xaml[Transforms_snip#MultipleTransformExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MultipleTransformExample.xaml#multipletransformexamplewholepage)]  
  
 [!code-csharp[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/MultipleTransformsExample.cs#multipletransformscodeexamplewholepage)]
 [!code-vb[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/MultipleTransformsExample.vb#multipletransformscodeexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="b7e14-106">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7e14-106">See also</span></span>

- <xref:System.Windows.UIElement.RenderTransform%2A>
- <xref:System.Windows.Media.TransformGroup>
- [<span data-ttu-id="b7e14-107">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="b7e14-107">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="b7e14-108">Beispiel für 2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="b7e14-108">2D Transforms Sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms)
