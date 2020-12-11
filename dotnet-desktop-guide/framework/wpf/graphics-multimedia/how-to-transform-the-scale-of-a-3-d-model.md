---
title: 'Gewusst wie: Transformieren der Skalierung eines 3D-Modells'
ms.date: 03/30/2017
helpviewer_keywords:
- scaling [WPF], 3D objects
- 3D objects [WPF], scaling
ms.assetid: f3fdfe33-f7dc-44b0-84a5-e43b89947f35
ms.openlocfilehash: be41a0e10929912c1b54bf7140d743d9453199bf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976859"
---
# <a name="how-to-transform-the-scale-of-a-3d-model"></a>Gewusst wie: Transformieren der Skalierung eines 3D-Modells
In diesem Beispiel wird gezeigt, wie ein 3D-Objekt skaliert wird. Verwenden Sie zum Skalieren eines 3D-Objekts einen <xref:System.Windows.Media.Media3D.ScaleTransform3D> . Die <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A> <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A> Eigenschaften, und <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleZ%2A> ändern die Größe des-Elements mit dem von Ihnen angegebenen Faktor. Beispielsweise wird ein <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A> Objekt mit dem Wert 1,5 auf 150 Prozent seiner ursprünglichen Breite gestreckt. <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A>Der Wert 0,5 verkleinert die Höhe eines Objekts um 50 Prozent. Der folgende Code zeigt die Verwendung <xref:System.Windows.Media.Media3D.ScaleTransform3D> von als Transformation für eine <xref:System.Windows.Media.Media3D.GeometryModel3D> .  
  
 [!code-xaml[3DGallery_snip#ScaleTransform3DExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ScaleTransform3DExample.xaml#scaletransform3dexampleinline1)]  
  
## <a name="example"></a>Beispiel  
 Der folgende Code zeigt das gesamte Beispiel.  
  
 [!code-xaml[3DGallery_snip#ScaleTransform3DExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ScaleTransform3DExample.xaml#scaletransform3dexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Animieren von 3D-Translationen](how-to-animate-3-d-translations.md)
- [Erstellen einer 3D-Szene](how-to-create-a-3-d-scene.md)
- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
