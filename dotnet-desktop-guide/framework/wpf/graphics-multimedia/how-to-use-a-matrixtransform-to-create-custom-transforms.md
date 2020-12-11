---
title: 'Gewusst wie: Verwenden von MatrixTransform zum Erstellen benutzerdefinierter Transformationen'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], custom Transforms
ms.assetid: 919381ca-989f-47cf-86b4-1094060236e4
ms.openlocfilehash: 1971d5fe9422c5138f140517e6fd4c9f9b2cf48b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977513"
---
# <a name="how-to-use-a-matrixtransform-to-create-custom-transforms"></a><span data-ttu-id="feec2-102">Gewusst wie: Verwenden von MatrixTransform zum Erstellen benutzerdefinierter Transformationen</span><span class="sxs-lookup"><span data-stu-id="feec2-102">How to: Use a MatrixTransform to Create Custom Transforms</span></span>
<span data-ttu-id="feec2-103">Dieses Beispiel zeigt, wie Sie mit einem <xref:System.Windows.Media.MatrixTransform> die Position, die Streckung und die Schiefe eines übersetzen (verschieben) <xref:System.Windows.Controls.Button> .</span><span class="sxs-lookup"><span data-stu-id="feec2-103">This example shows how to use a <xref:System.Windows.Media.MatrixTransform> to translate (move) the position, stretch, and skew of a <xref:System.Windows.Controls.Button>.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="feec2-104">Verwenden Sie die- <xref:System.Windows.Media.MatrixTransform> Klasse, um benutzerdefinierte Transformationen zu erstellen, die nicht von den <xref:System.Windows.Media.RotateTransform> <xref:System.Windows.Media.SkewTransform> Klassen,, oder bereitgestellt werden <xref:System.Windows.Media.ScaleTransform> <xref:System.Windows.Media.TranslateTransform> .</span><span class="sxs-lookup"><span data-stu-id="feec2-104">Use the <xref:System.Windows.Media.MatrixTransform> class to create custom transformations that are not provided by the <xref:System.Windows.Media.RotateTransform>, <xref:System.Windows.Media.SkewTransform>, <xref:System.Windows.Media.ScaleTransform>, or <xref:System.Windows.Media.TranslateTransform> classes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="feec2-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="feec2-105">Example</span></span>  
 [!code-xaml[Transforms_snip#MatrixTransform](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MatrixTransformExample.xaml#matrixtransform)]  
  
## <a name="see-also"></a><span data-ttu-id="feec2-106">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="feec2-106">See also</span></span>

- <xref:System.Windows.Media.MatrixTransform>
- <xref:System.Windows.Media.Transform>
- [<span data-ttu-id="feec2-107">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="feec2-107">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="feec2-108">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="feec2-108">How-to Topics</span></span>](transformations-how-to-topics.md)
- [<span data-ttu-id="feec2-109">Übersicht über Formen und die grundlegenden Funktionen zum Zeichnen in WPF</span><span class="sxs-lookup"><span data-stu-id="feec2-109">Shapes and Basic Drawing in WPF Overview</span></span>](shapes-and-basic-drawing-in-wpf-overview.md)
