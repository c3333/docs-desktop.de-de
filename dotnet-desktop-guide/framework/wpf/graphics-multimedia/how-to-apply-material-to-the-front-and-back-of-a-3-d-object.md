---
title: 'Gewusst wie: Anwenden von Material auf die Vorder-und Rückseite eines 3D-Objekts'
ms.date: 03/30/2017
helpviewer_keywords:
- 3D objects [WPF], applying Material class
- Material class [WPF], applying to both sides of 3D object
- classes [WPF], Material
ms.assetid: d93c8ad6-4939-4d29-9544-4d16d98093c1
ms.openlocfilehash: 5c24879d97e7857fb07fcef4a9ba8efa901e4a39
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975315"
---
# <a name="how-to-apply-material-to-the-front-and-back-of-a-3d-object"></a>Gewusst wie: Anwenden von Material auf die Vorder-und Rückseite eines 3D-Objekts
Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Media.Media3D.Material> auf die Vorder-und Rückseite eines 3D-Objekts angewendet und das-Objekt animiert wird, um beide Seiten des-Objekts anzuzeigen. Die <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> -Eigenschaft eines <xref:System.Windows.Media.Media3D.GeometryModel3D> -Objekts wird verwendet, um ein rotes <xref:System.Windows.Media.Brush> auf die Vorderseite des-Objekts anzuwenden, und die- <xref:System.Windows.Media.Media3D.GeometryModel3D.BackMaterial%2A> Eigenschaft von <xref:System.Windows.Media.Media3D.GeometryModel3D> wird verwendet, um einen blauen <xref:System.Windows.Media.Brush> auf die Rückseite des-Objekts anzuwenden. Der folgende Code zeigt die Anwendung der Materialien für das-Objekt:  
  
 [!code-xaml[Animation3DGallery_snip#BackMaterialAnimationExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/BackMaterialAnimationExample.xaml#backmaterialanimationexampleinline1)]  
  
## <a name="example"></a>Beispiel  
 Der folgende Code zeigt das gesamte Beispiel.  
  
 [!code-xaml[Animation3DGallery_snip#BackMaterialAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/BackMaterialAnimationExample.xaml#backmaterialanimationexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Erstellen einer 3D-Szene](how-to-create-a-3-d-scene.md)
- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
- [Animieren von Materialeigenschaften in einer 3D-Szene](how-to-animate-material-properties-in-a-3-d-scene.md)
- [Anwenden von selbstleuchtendem Material auf ein 3D-Objekt](how-to-apply-emissive-material-to-a-3-d-object.md)
