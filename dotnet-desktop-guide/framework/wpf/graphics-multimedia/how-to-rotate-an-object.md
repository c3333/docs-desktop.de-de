---
title: 'Gewusst wie: Drehen eines Objekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], rotating objects [WPF]
- rotating objects [WPF]
ms.assetid: ee3466cd-e66f-4e8f-8a5a-71d77bc1e390
ms.openlocfilehash: e17d3b7b9986b477df198480129edaf4c139c6bc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977270"
---
# <a name="how-to-rotate-an-object"></a>Gewusst wie: Drehen eines Objekts
Dieses Beispiel zeigt, wie ein Objekt gedreht wird. Im Beispiel wird zunächst ein erstellt <xref:System.Windows.Media.RotateTransform> und dann der <xref:System.Windows.Media.RotateTransform.Angle%2A> in Grad angegeben.  
  
 Im folgenden Beispiel wird ein- <xref:System.Windows.Shapes.Polyline> Objekt um 45 Grad um die linke obere Ecke gedreht.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[Transforms_snip#RotatePolylineAboutTopLeft](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/RotateTransformExample.xaml#rotatepolylineabouttopleft)]  
  
 [!code-csharp[Transforms_Procedural_snip#RotatePolylineAboutTopLeft](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/RotateTransformExample.cs#rotatepolylineabouttopleft)]
 [!code-vb[Transforms_Procedural_snip#RotatePolylineAboutTopLeft](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/RotateTransformExample.vb#rotatepolylineabouttopleft)]  
  
 Die <xref:System.Windows.Media.RotateTransform.CenterX%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.RotateTransform.CenterY%2A> des- <xref:System.Windows.Media.RotateTransform> Objekts geben den Punkt an, an dem das Objekt gedreht wird. Dieser Mittelpunkt wird im Koordinatenraum des Elements ausgedrückt, das transformiert wird. Standardmäßig wird die Drehung um den Punkt (0,0), die obere linke Ecke des zu transformierenden Objekts, vorgenommen.  
  
 Im nächsten Beispiel wird ein- <xref:System.Windows.Shapes.Polyline> Objekt um 45 Grad im Uhrzeigersinn um den Punkt gedreht (25, 50).  
  
 [!code-xaml[Transforms_snip#RotatePolylineAboutCenter](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/RotateTransformExample.xaml#rotatepolylineaboutcenter)]  
  
 [!code-csharp[Transforms_Procedural_snip#RotatePolylineAboutCenter](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/RotateTransformExample.cs#rotatepolylineaboutcenter)]
 [!code-vb[Transforms_Procedural_snip#RotatePolylineAboutCenter](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/RotateTransformExample.vb#rotatepolylineaboutcenter)]  
  
 Die folgende Abbildung zeigt die Ergebnisse der Anwendung eines <xref:System.Windows.Media.Transform> auf die beiden-Objekte.  
  
 ![45-Grad-Drehungen mit unterschiedlichen Mittelpunkten](./media/wcpsdk-graphicsmm-rotatetransform45degrees.gif "wcpsdk_graphicsmm_rotatetransform45degrees")  
Zwei Objekte, die um unterschiedliche Drehpunkte um 45 Grad gedreht werden  
  
 Das <xref:System.Windows.Shapes.Polyline> in den vorherigen Beispielen ist ein <xref:System.Windows.UIElement> . Wenn Sie <xref:System.Windows.Media.Transform> auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft eines anwenden <xref:System.Windows.UIElement> , können Sie die-Eigenschaft verwenden, <xref:System.Windows.UIElement.RenderTransformOrigin%2A> um einen Ursprung für jeden anzugeben, <xref:System.Windows.Media.Transform> den Sie auf das Element anwenden. Da die- <xref:System.Windows.UIElement.RenderTransformOrigin%2A> Eigenschaft relative Koordinaten verwendet, können Sie eine Transformation auf den Mittelpunkt des Elements anwenden, auch wenn Sie Ihre Größe nicht kennen. Weitere Informationen und ein Beispiel finden [Sie unter Angeben des Ursprungs einer Transformation mithilfe von relativen Werten](how-to-specify-the-origin-of-a-transform-by-using-relative-values.md).  
  
 Das komplette Beispiel finden Sie unter [Beispiel für 2D-Transformationen](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Transform>
- [Übersicht über Transformationen](transforms-overview.md)
- [Artikel zu Vorgehensweisen](transformations-how-to-topics.md)
