---
title: 'Gewusst wie: Animieren von Material-Eigenschaften in einer 3D-Szene'
ms.date: 03/30/2017
helpviewer_keywords:
- Material properties [WPF], animating in 3D scenes
- animation [WPF], Material properties in 3D scenes
- 3D scenes [WPF], animating Material properties
ms.assetid: 229fd6eb-7401-4992-b0c9-8b28de230c0f
ms.openlocfilehash: db59debcd7558cde52d8604cb04c8c4e68921825
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975409"
---
# <a name="how-to-animate-material-properties-in-a-3d-scene"></a>Gewusst wie: Animieren von Material-Eigenschaften in einer 3D-Szene
In diesem Beispiel wird gezeigt, wie die <xref:System.Windows.Media.Brush.Opacity%2A> -Eigenschaft des <xref:System.Windows.Media.Media3D.Material> auf ein 3D-Modell angewendeten animiert wird.  
  
 Im folgenden Codebeispiel wird das <xref:System.Windows.Media.LinearGradientBrush> -Element definiert, das als <xref:System.Windows.Media.Media3D.Material> auf das 3D-Objekt angewendet wird.  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexampleinline1)]  
  
 Die- <xref:System.Windows.Media.Brush.Opacity%2A> Eigenschaft dieses-Objekts <xref:System.Windows.Media.LinearGradientBrush> wird mithilfe des folgenden Code Beispiels animiert.  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleInline2](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexampleinline2)]  
  
## <a name="example"></a>Beispiel  
 Der folgende Code zeigt das gesamte Beispiel.  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Erstellen einer 3D-Szene](how-to-create-a-3-d-scene.md)
- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
