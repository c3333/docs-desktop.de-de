---
title: 'Gewusst wie: Animieren von 3D-Übersetzungen'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], 3D translations
- 3D translations [WPF], animating
ms.assetid: d4eece1f-0cd2-4a2c-8370-293354c380e4
ms.openlocfilehash: 7d4fff9c74663bd220ad5d15a983bcb639621afd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975332"
---
# <a name="how-to-animate-3d-translations"></a>Gewusst wie: Animieren von 3D-Übersetzungen
In diesem Thema wird veranschaulicht, wie Sie eine Übersetzungs Transformation für ein 3D-Modell animieren.  
  
 Der folgende Code zeigt die Anwendung eines- <xref:System.Windows.Media.Media3D.TranslateTransform3D> Objekts für die- <xref:System.Windows.Media.Media3D.Model3D.Transform%2A> Eigenschaft eines <xref:System.Windows.Media.Media3D.GeometryModel3D> .  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationinline1)]  
  
 Die- <xref:System.Windows.Media.Media3D.TranslateTransform3D.OffsetX%2A> Eigenschaft dieses- <xref:System.Windows.Media.Media3D.TranslateTransform3D> Objekts wird mithilfe des folgenden Codes animiert.  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationInline2](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationinline2)]  
  
## <a name="example"></a>Beispiel  
 Der folgende Code zeigt das gesamte Beispiel.  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Animationen](animation-overview.md)
- [Erstellen einer 3D-Szene](how-to-create-a-3-d-scene.md)
- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
- [Übersicht über Transformationen](transforms-overview.md)
