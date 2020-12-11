---
title: 'Gewusst wie: Festlegen von horizontaler und vertikaler Ausrichtung bei einem TileBrush'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TileBrush [WPF], alignment of
- vertical alignment of TileBrushes [WPF]
- aligning [WPF], TileBrushes
- horizontal alignment of Tilebrushes [WPF]
ms.assetid: 65ae89bd-9246-4c9e-bde4-2fb991d4060d
ms.openlocfilehash: e3bfb2b209e40c435c3a321c874dfbd7a9a2fd50
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975478"
---
# <a name="how-to-set-the-horizontal-and-vertical-alignment-of-a-tilebrush"></a>Gewusst wie: Festlegen von horizontaler und vertikaler Ausrichtung bei einem TileBrush
In diesem Beispiel wird gezeigt, wie die horizontale und die vertikale Ausrichtung des Inhalts in einer Fläche gesteuert werden. Um die horizontale und vertikale Ausrichtung eines-Steuer Elements zu steuern <xref:System.Windows.Media.TileBrush> , verwenden Sie dessen <xref:System.Windows.Media.TileBrush.AlignmentX%2A> -Eigenschaft und-Eigenschaft <xref:System.Windows.Media.TileBrush.AlignmentY%2A> .  
  
 Die <xref:System.Windows.Media.TileBrush.AlignmentX%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.TileBrush.AlignmentY%2A> eines <xref:System.Windows.Media.TileBrush> werden verwendet, wenn eine der folgenden Bedingungen zutrifft:  
  
- Die <xref:System.Windows.Media.TileBrush.Stretch%2A> -Eigenschaft ist <xref:System.Windows.Media.Stretch.Uniform> oder, <xref:System.Windows.Media.Stretch.UniformToFill> und die <xref:System.Windows.Media.TileBrush.Viewbox%2A> und weisen <xref:System.Windows.Media.TileBrush.Viewport%2A> unterschiedliche Seitenverhältnisse auf.  
  
- Die- <xref:System.Windows.Media.TileBrush.Stretch%2A> Eigenschaft ist, <xref:System.Windows.Media.Stretch.None> und <xref:System.Windows.Media.TileBrush.Viewbox%2A> und <xref:System.Windows.Media.TileBrush.Viewport%2A> sind unterschiedlich groß.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird der Inhalt eines- <xref:System.Windows.Media.DrawingBrush> Typs, der ein Typ von ist, <xref:System.Windows.Media.TileBrush> in der linken oberen Ecke der zugehörigen Kachel ausgerichtet. Um den Inhalt auszurichten, wird im Beispiel die <xref:System.Windows.Media.TileBrush.AlignmentX%2A> -Eigenschaft von <xref:System.Windows.Media.DrawingBrush> auf <xref:System.Windows.Media.AlignmentX.Left> und die- <xref:System.Windows.Media.TileBrush.AlignmentY%2A> Eigenschaft auf <xref:System.Windows.Media.AlignmentY.Top> festgelegt. Folgende Ergebnisse werden zurückgegeben:  
  
 ![TileBrush mit an der linken oberen Ecke ausgerichtetem Inhalt](./media/graphicsmm-tilebrushalignmentexampletopleft.png "graphicsmm_TileBrushAlignmentExampleTopLeft")  
TileBrush mit an der linken oberen Ecke ausgerichtetem Inhalt  
  
 [!code-csharp[brushoverviewexamples_snip#TileBrushTopLeftAlignmentInline](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_snip/CSharp/TileBrushAlignmentExample.cs#tilebrushtopleftalignmentinline)]
 [!code-vb[brushoverviewexamples_snip#TileBrushTopLeftAlignmentInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_snip/visualbasic/tilebrushalignmentexample.vb#tilebrushtopleftalignmentinline)]
 [!code-xaml[brushoverviewexamples_snip#TileBrushTopLeftAlignmentInline](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TileBrushAlignmentExample.xaml#tilebrushtopleftalignmentinline)]  
  
## <a name="example"></a>Beispiel  
 Im nächsten Beispiel wird der Inhalt eines in der <xref:System.Windows.Media.DrawingBrush> rechten unteren Ecke der Kachel ausgerichtet, indem die <xref:System.Windows.Media.TileBrush.AlignmentX%2A> -Eigenschaft auf <xref:System.Windows.Media.AlignmentX.Right> und die- <xref:System.Windows.Media.TileBrush.AlignmentY%2A> Eigenschaft auf festgelegt wird <xref:System.Windows.Media.AlignmentY.Bottom> . Das Beispiel erzeugt folgende Ausgabe.  
  
 ![TileBrush mit an der rechten unteren Ecke ausgerichtetem Inhalt](./media/graphicsmm-tilebrushalignmentexamplebottomright.png "graphicsmm_TileBrushAlignmentExampleBottomRight")  
TileBrush mit an der rechten unteren Ecke ausgerichtetem Inhalt  
  
 [!code-csharp[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_snip/CSharp/TileBrushAlignmentExample.cs#tilebrushbottomrightalignmentinline)]
 [!code-vb[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_snip/visualbasic/tilebrushalignmentexample.vb#tilebrushbottomrightalignmentinline)]
 [!code-xaml[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TileBrushAlignmentExample.xaml#tilebrushbottomrightalignmentinline)]  
  
## <a name="example"></a>Beispiel  
 Im nächsten Beispiel wird der Inhalt eines <xref:System.Windows.Media.DrawingBrush> -Objekts auf die obere linke Ecke der Kachel ausgerichtet, indem die <xref:System.Windows.Media.TileBrush.AlignmentX%2A> -Eigenschaft auf <xref:System.Windows.Media.AlignmentX.Left> und die- <xref:System.Windows.Media.TileBrush.AlignmentY%2A> Eigenschaft auf <xref:System.Windows.Media.AlignmentY.Top> festgelegt wird. Außerdem wird der <xref:System.Windows.Media.TileBrush.Viewport%2A> und der von so festgelegt <xref:System.Windows.Media.TileBrush.TileMode%2A> , dass <xref:System.Windows.Media.DrawingBrush> ein Kachel Muster erzeugt wird. Das Beispiel erzeugt folgende Ausgabe.  
  
 ![Flächenmuster mit in der Basisfläche oben links ausgerichtetem Inhalt](./media/graphicsmm-tilebrushalignmentexampletoplefttiled.png "graphicsmm_TileBrushAlignmentExampleTopLeftTiled")  
Flächenmuster mit in der Basisfläche oben links ausgerichtetem Inhalt  
  
 In der Abbildung ist eine Basisfläche hervorgehoben, damit Sie sehen können, wie der Inhalt ausgerichtet ist. Beachten Sie, dass die- <xref:System.Windows.Media.TileBrush.AlignmentX%2A> Einstellung keine Auswirkung hat, da der Inhalt von die <xref:System.Windows.Media.DrawingBrush> Basis Kachel vollständig horizontal füllt.  
  
 [!code-csharp[brushoverviewexamples_snip#TileBrushTopLeftAlignmentTiledInline](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_snip/CSharp/TileBrushAlignmentExample.cs#tilebrushtopleftalignmenttiledinline)]
 [!code-vb[brushoverviewexamples_snip#TileBrushTopLeftAlignmentTiledInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_snip/visualbasic/tilebrushalignmentexample.vb#tilebrushtopleftalignmenttiledinline)]
 [!code-xaml[brushoverviewexamples_snip#TileBrushTopLeftAlignmentTiledInline](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TileBrushAlignmentExample.xaml#tilebrushtopleftalignmenttiledinline)]  
  
## <a name="example"></a>Beispiel  
 Im letzten Beispiel wird der Inhalt einer gekachelten <xref:System.Windows.Media.DrawingBrush> an der unteren rechten Seite der zugehörigen Basis Kachel ausgerichtet, indem die <xref:System.Windows.Media.TileBrush.AlignmentX%2A> -Eigenschaft auf <xref:System.Windows.Media.AlignmentX.Right> und die- <xref:System.Windows.Media.TileBrush.AlignmentY%2A> Eigenschaft auf festgelegt wird <xref:System.Windows.Media.AlignmentY.Bottom> . Das Beispiel erzeugt folgende Ausgabe.  
  
 ![Flächenmuster mit in der Basisfläche oben rechts ausgerichtetem Inhalt](./media/graphicsmm-tilebrushalignmentexamplebottomrighttiled.png "graphicsmm_TileBrushAlignmentExampleBottomRightTiled")  
Flächenmuster mit in der Basisfläche oben rechts ausgerichtetem Inhalt  
  
 Auch diese <xref:System.Windows.Media.TileBrush.AlignmentX%2A> Einstellung hat keine Auswirkung, da der Inhalt von die <xref:System.Windows.Media.DrawingBrush> Basis Kachel vollständig horizontal füllt.  
  
 [!code-csharp[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_snip/CSharp/TileBrushAlignmentExample.cs#tilebrushbottomrightalignmentinline)]
 [!code-vb[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_snip/visualbasic/tilebrushalignmentexample.vb#tilebrushbottomrightalignmentinline)]
 [!code-xaml[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TileBrushAlignmentExample.xaml#tilebrushbottomrightalignmentinline)]  
  
 In den Beispielen <xref:System.Windows.Media.DrawingBrush> werden-Objekte verwendet, um zu veranschaulichen, wie die <xref:System.Windows.Media.TileBrush.AlignmentX%2A> <xref:System.Windows.Media.TileBrush.AlignmentY%2A> Eigenschaften und verwendet werden. Diese Eigenschaften verhalten sich für alle Kachel Pinsel identisch: <xref:System.Windows.Media.DrawingBrush> , <xref:System.Windows.Media.ImageBrush> und <xref:System.Windows.Media.VisualBrush> . Weitere Informationen zu TileBrush-Objekten finden Sie unter [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](painting-with-images-drawings-and-visuals.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.DrawingBrush>
- <xref:System.Windows.Media.ImageBrush>
- <xref:System.Windows.Media.VisualBrush>
- [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](painting-with-images-drawings-and-visuals.md)
