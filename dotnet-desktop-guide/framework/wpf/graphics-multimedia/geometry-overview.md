---
title: Übersicht über die Geometrie
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- geometry classes [WPF]
- graphics [WPF], geometry classes
ms.assetid: 9fba8934-98b7-4af6-82f6-f4ef887f963a
ms.openlocfilehash: 289a4175652de78d414d7c1d7f4b0697fe4bf243
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977236"
---
# <a name="geometry-overview"></a>Übersicht über die Geometrie
In dieser Übersicht wird beschrieben, wie Sie die- [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] <xref:System.Windows.Media.Geometry> Klassen verwenden, um Formen zu beschreiben. In diesem Thema werden auch die Unterschiede zwischen <xref:System.Windows.Media.Geometry> Objekten und <xref:System.Windows.Shapes.Shape> Elementen erläutert.  

<a name="wcpsdk_graphics_geometry_introduction"></a>
## <a name="what-is-a-geometry"></a>Was ist eine Geometrie?  
 Die <xref:System.Windows.Media.Geometry> -Klasse und die Klassen, die davon abgeleitet werden, z. b., <xref:System.Windows.Media.EllipseGeometry> <xref:System.Windows.Media.PathGeometry> und <xref:System.Windows.Media.CombinedGeometry> , ermöglichen es Ihnen, die Geometrie einer 2D-Form zu beschreiben. Diese geometrischen Beschreibungen haben viele Verwendungszwecke, beispielsweise zum Definieren einer am Bildschirm zu zeichnenden Form oder zum Definieren von Treffertest- und Clipbereichen. Sie können mithilfe einer Geometrie sogar einen Animationspfad definieren.  
  
 <xref:System.Windows.Media.Geometry> Objekte können einfach sein, z. b. Rechtecke und Kreise oder zusammengesetzte, die aus zwei oder mehr Geometrie Objekten erstellt werden.  Komplexere Geometrien können mithilfe der <xref:System.Windows.Media.PathGeometry> -Klasse und der- <xref:System.Windows.Media.StreamGeometry> Klasse erstellt werden, die es Ihnen ermöglichen, Bögen und Kurven zu beschreiben.  
  
 Da ein <xref:System.Windows.Media.Geometry> Typ von ist <xref:System.Windows.Freezable> , <xref:System.Windows.Media.Geometry> stellen-Objekte mehrere spezielle Features bereit: Sie können als [Ressourcen](/dotnet/desktop-wpf/fundamentals/xaml-resources-define)deklariert, von mehreren Objekten gemeinsam genutzt und schreibgeschützt werden, um die Leistung zu verbessern, geklont und Thread sicher gemacht zu werden. Weitere Informationen zu den verschiedenen Funktionen, die von-Objekten bereitgestellt werden <xref:System.Windows.Freezable> , finden Sie unter [Übersicht über](../advanced/freezable-objects-overview.md)frei wählbare Objekte.  
  
<a name="wcpsdk_graphics_geometry_geometryandshapes"></a>
## <a name="geometries-vs-shapes"></a>Geometrien im Vergleich zu Formen  
 Die <xref:System.Windows.Media.Geometry> <xref:System.Windows.Shapes.Shape> Klassen und sind insofern ähnlich, als Sie beide 2D-Formen beschreiben (z. b. vergleichen <xref:System.Windows.Media.EllipseGeometry> <xref:System.Windows.Shapes.Ellipse> ), aber es gibt wichtige Unterschiede.  
  
 Für einen <xref:System.Windows.Media.Geometry> erbt die-Klasse von der- <xref:System.Windows.Freezable> Klasse, während die- <xref:System.Windows.Shapes.Shape> Klasse von erbt <xref:System.Windows.FrameworkElement> . Da es sich um-Elemente handelt, <xref:System.Windows.Shapes.Shape> können sich-Objekte selbst Rendering und am Layoutsystem teilnehmen, während- <xref:System.Windows.Media.Geometry> Objekte nicht.  
  
 Obwohl- <xref:System.Windows.Shapes.Shape> Objekte leichter verwendbar sind als- <xref:System.Windows.Media.Geometry> Objekte, <xref:System.Windows.Media.Geometry> sind-Objekte vielseitiger. Während ein- <xref:System.Windows.Shapes.Shape> Objekt zum rendering2d-Grafiken verwendet wird, kann ein- <xref:System.Windows.Media.Geometry> Objekt verwendet werden, um den geometrischen Bereich für 2D-Grafiken zu definieren, einen Bereich für das Abschneiden zu definieren oder eine Region für Treffer Tests zu definieren, z. b..  
  
### <a name="the-path-shape"></a>Die Path-Form  
 Eine <xref:System.Windows.Shapes.Shape> , die- <xref:System.Windows.Shapes.Path> Klasse, verwendet tatsächlich eine, <xref:System.Windows.Media.Geometry> um ihren Inhalt zu beschreiben. Wenn Sie die <xref:System.Windows.Shapes.Path.Data%2A> -Eigenschaft des-Objekts <xref:System.Windows.Shapes.Path> mit einem festlegen <xref:System.Windows.Media.Geometry> und dessen <xref:System.Windows.Shapes.Shape.Fill%2A> -Eigenschaft und-Eigenschaft festlegen <xref:System.Windows.Shapes.Shape.Stroke%2A> , können Sie einen Rendering <xref:System.Windows.Media.Geometry> .  
  
<a name="commonproperties"></a>
## <a name="common-properties-that-take-a-geometry"></a>Allgemeine Eigenschaften, die eine Geometrie übernehmen  
 In den vorherigen Abschnitten wurde erwähnt, dass Geometry-Objekte für eine Vielzahl von Zwecken mit anderen Objekten verwendet werden können, z.B. zum Zeichnen von Formen, zum Animieren und für das Clipping. In der folgenden Tabelle werden mehrere Klassen aufgelistet, die über Eigenschaften verfügen, die ein- <xref:System.Windows.Media.Geometry> Objekt akzeptieren.  
  
|type|Eigenschaft|  
|----------|--------------|  
|<xref:System.Windows.Media.Animation.DoubleAnimationUsingPath>|<xref:System.Windows.Media.Animation.DoubleAnimationUsingPath.PathGeometry%2A>|  
|<xref:System.Windows.Media.DrawingGroup>|<xref:System.Windows.Media.DrawingGroup.ClipGeometry%2A>|  
|<xref:System.Windows.Media.GeometryDrawing>|<xref:System.Windows.Media.GeometryDrawing.Geometry%2A>|  
|<xref:System.Windows.Shapes.Path>|<xref:System.Windows.Shapes.Path.Data%2A>|  
|<xref:System.Windows.UIElement>|<xref:System.Windows.UIElement.Clip%2A>|  
  
<a name="wcpsdk_graphics_geometry_geometrytypes"></a>
## <a name="simple-geometry-types"></a>Einfache geometrische Typen  
 Die Basisklasse für alle Geometrien ist die abstrakte Klasse <xref:System.Windows.Media.Geometry> .  Die Klassen, die von der- <xref:System.Windows.Media.Geometry> Klasse abgeleitet werden, können grob in drei Kategorien gruppiert werden: einfache Geometrien, Pfadgeometrien und zusammengesetzte Geometrien.  
  
 Einfache Geometrie Klassen enthalten <xref:System.Windows.Media.LineGeometry> , <xref:System.Windows.Media.RectangleGeometry> und, <xref:System.Windows.Media.EllipseGeometry> und werden verwendet, um grundlegende geometrische Formen, wie z. b. Linien, Rechtecke und Kreise, zu erstellen.  
  
- Eine <xref:System.Windows.Media.LineGeometry> wird durch Angabe des Anfangs Punkts der Linie und des Endpunkts definiert.  
  
- Ein <xref:System.Windows.Media.RectangleGeometry> wird mit einer <xref:System.Windows.Rect> -Struktur definiert, die seine relative Position und seine Höhe und Breite angibt. Sie können ein abgerundetes Rechteck erstellen, indem Sie die <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> Eigenschaften und festlegen <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> .  
  
- Ein <xref:System.Windows.Media.EllipseGeometry> wird von einem Mittelpunkt, einem x-Radius und einem y-Radius definiert.  Die folgenden Beispiele zeigen, wie einfache Geometrien für das Rendering und das Clipping erstellt werden können.  
  
 Diese Formen und komplexere Formen können mithilfe von oder erstellt werden, <xref:System.Windows.Media.PathGeometry> indem Geometry-Objekte kombiniert werden, aber diese Klassen bieten eine einfachere Möglichkeit zum Erstellen dieser grundlegenden geometrischen Formen.  
  
 Im folgenden Beispiel wird gezeigt, wie ein erstellt und dargestellt wird <xref:System.Windows.Media.LineGeometry> .  Wie bereits erwähnt, ist ein- <xref:System.Windows.Media.Geometry> Objekt nicht in der Lage, sich selbst zu zeichnen. das Beispiel verwendet eine <xref:System.Windows.Shapes.Path> Form, um die Zeile zu rentieren.  Da eine Linie keinen Bereich aufweist, hat das Festlegen der <xref:System.Windows.Shapes.Shape.Fill%2A> -Eigenschaft von <xref:System.Windows.Shapes.Path> keine Auswirkung; stattdessen werden nur die <xref:System.Windows.Shapes.Shape.Stroke%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> angegeben. Die folgende Abbildung zeigt die Ausgabe des Beispiels.  
  
 ![LineGeometry](./media/graphicsmm-line.gif "graphicsmm_line")  
Eine LineGeometry, gezeichnet von (10,20) bis (100,130)  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMLineGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmlinegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmlinegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmlinegeometryexample)]  
  
 Im nächsten Beispiel wird gezeigt, wie ein erstellt und dargestellt wird <xref:System.Windows.Media.EllipseGeometry> .  In den Beispielen <xref:System.Windows.Media.EllipseGeometry.Center%2A> <xref:System.Windows.Media.EllipseGeometry> wird festgelegt, dass auf den Punkt festgelegt ist `50,50` , und der x-Radius und der y-Radius sind auf festgelegt `50` , wodurch ein Kreis mit einem Durchmesser von 100 erstellt wird.  Das Innere der Ellipse wird gezeichnet, indem der Fill-Eigenschaft des Path-Elements ein Wert zugewiesen wird, in diesem Fall <xref:System.Windows.Media.Brushes.Gold%2A> . Die folgende Abbildung zeigt die Ausgabe des Beispiels.  
  
 ![EllipseGeometry](./media/graphicsmm-ellipse.gif "graphicsmm_ellipse")  
EllipseGeometry, gezeichnet bei (50,50)  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMEllipseGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmellipsegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMEllipseGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmellipsegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMEllipseGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmellipsegeometryexample)]  
  
 Im folgenden Beispiel wird gezeigt, wie ein erstellt und dargestellt wird <xref:System.Windows.Media.RectangleGeometry> .  Die Position und die Dimensionen des Rechtecks werden durch eine- <xref:System.Windows.Rect> Struktur definiert. Die Position ist `50,50` und die Höhe und Breite sind beide `25`, wodurch ein Quadrat erstellt wird. Die folgende Abbildung zeigt die Ausgabe des Beispiels.  
  
 ![RectangleGeometry](./media/graphicsmm-rectangle.gif "graphicsmm_rectangle")  
Eine RectangleGeometry, gezeichnet bei 50,50  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmrectanglegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmrectanglegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmrectanglegeometryexample)]  
  
 Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Media.EllipseGeometry> als Clip Bereich für ein Bild verwendet wird.  Ein <xref:System.Windows.Controls.Image> -Objekt wird mit dem Wert <xref:System.Windows.FrameworkElement.Width%2A> 200 und einem <xref:System.Windows.FrameworkElement.Height%2A> von 150 definiert.  Ein <xref:System.Windows.Media.EllipseGeometry> mit dem <xref:System.Windows.Media.EllipseGeometry.RadiusX%2A> Wert 100, dem <xref:System.Windows.Media.EllipseGeometry.RadiusY%2A> Wert 75 und dem <xref:System.Windows.Media.EllipseGeometry.Center%2A> Wert 100, der auf die- <xref:System.Windows.UIElement.Clip%2A> Eigenschaft des Bilds festgelegt ist.  Es wird nur der Teil des Bilds angezeigt, der innerhalb des Bereichs der Ellipse liegt. Die folgende Abbildung zeigt die Ausgabe des Beispiels.  
  
 ![Ein Bild mit und ohne Clipping](./media/graphicsmm-clipexample.png "graphicsmm_clipexample")  
Eine EllipseGeometry zum Beschneiden eines Image-Steuerelements  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMImageClipGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmimageclipgeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMImageClipGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmimageclipgeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMImageClipGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmimageclipgeometryexample)]  
  
<a name="wcpsdk_graphics_geometry_pathgeometry"></a>
## <a name="path-geometries"></a>Path-Geometrien  
 Die <xref:System.Windows.Media.PathGeometry> -Klasse und ihre Lightweight-Entsprechung, die- <xref:System.Windows.Media.StreamGeometry> Klasse, bieten die Möglichkeit, mehrere komplexe Abbildungen zu beschreiben, die aus Arcs, Kurven und Linien bestehen.  
  
 Das Herzstück eines <xref:System.Windows.Media.PathGeometry> ist eine Auflistung von- <xref:System.Windows.Media.PathFigure> Objekten, die so benannt werden, dass jede Abbildung eine diskrete Form in der beschreibt <xref:System.Windows.Media.PathGeometry> . Jede besteht aus <xref:System.Windows.Media.PathFigure> einem oder mehreren- <xref:System.Windows.Media.PathSegment> Objekten, von denen jedes ein Segment der Abbildung beschreibt.  
  
 Es gibt viele Arten von Segmenten.  
  
|Segmenttyp|BESCHREIBUNG|Beispiel|  
|------------------|-----------------|-------------|  
|<xref:System.Windows.Media.ArcSegment>|Erstellt einen elliptischen Bogen zwischen zwei Punkten.|[Erstellen Sie einen elliptischen Bogen](how-to-create-an-elliptical-arc.md).|  
|<xref:System.Windows.Media.BezierSegment>|Erstellt eine kubische Bezier-Kurve zwischen zwei Punkten.|[Erstellen Sie eine kubische Bezier-Kurve](how-to-create-a-cubic-bezier-curve.md).|  
|<xref:System.Windows.Media.LineSegment>|Erstellt eine Linie zwischen zwei Punkten.|[Erstellen eines LineSegment in einer PathGeometry](how-to-create-a-linesegment-in-a-pathgeometry.md)|  
|<xref:System.Windows.Media.PolyBezierSegment>|Erstellt eine Reihe von kubischen Bezier-Kurven.|Informationen finden Sie auf der <xref:System.Windows.Media.PolyBezierSegment> Seite Typ.|  
|<xref:System.Windows.Media.PolyLineSegment>|Erstellt eine Reihe von Zeilen.|Informationen finden Sie auf der <xref:System.Windows.Media.PolyLineSegment> Seite Typ.|  
|<xref:System.Windows.Media.PolyQuadraticBezierSegment>|Erstellt eine Reihe quadratischer Bezier-Kurven.|Siehe die <xref:System.Windows.Media.PolyQuadraticBezierSegment> Seite.|  
|<xref:System.Windows.Media.QuadraticBezierSegment>|Erstellt eine quadratische Bezier-Kurve.|[Erstellen Sie eine quadratische Bezier-Kurve](how-to-create-a-quadratic-bezier-curve.md).|  
  
 Die Segmente in einer <xref:System.Windows.Media.PathFigure> werden zu einer einzelnen geometrischen Form zusammengefasst, wobei der Endpunkt der einzelnen Segmente der Anfangspunkt des nächsten Segments ist. Die- <xref:System.Windows.Media.PathFigure.StartPoint%2A> Eigenschaft eines <xref:System.Windows.Media.PathFigure> gibt den Punkt an, von dem das erste Segment gezeichnet wird. Jedes nachfolgende Segment beginnt am Endpunkt des vorherigen Segments. Beispielsweise kann eine vertikale Linie von `10,50` zu `10,150` definiert werden, indem die <xref:System.Windows.Media.PathFigure.StartPoint%2A> -Eigenschaft auf festgelegt `10,50` und ein <xref:System.Windows.Media.LineSegment> mit <xref:System.Windows.Media.LineSegment.Point%2A> der-Eigenschaften Einstellung erstellt wird `10,150` .  
  
 Im folgenden Beispiel wird ein einfaches <xref:System.Windows.Media.PathGeometry> <xref:System.Windows.Media.PathFigure> -Element mit einem-Element mit einem erstellt <xref:System.Windows.Media.LineSegment> und mit einem- <xref:System.Windows.Shapes.Path> Element angezeigt. Der <xref:System.Windows.Media.PathFigure> -Wert des-Objekts <xref:System.Windows.Media.PathFigure.StartPoint%2A> wird auf festgelegt, `10,20` und <xref:System.Windows.Media.LineSegment> wird mit einem Endpunkt von definiert `100,130` . In der folgenden Abbildung wird die in <xref:System.Windows.Media.PathGeometry> diesem Beispiel erstellte gezeigt.  
  
 ![LineGeometry](./media/graphicsmm-line.gif "graphicsmm_line")  
Eine PathGeometry, die ein einzelnes LineSegment enthält  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMPathGeometryLineExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmpathgeometrylineexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMPathGeometryLineExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmpathgeometrylineexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMPathGeometryLineExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmpathgeometrylineexample)]  
  
 Es lohnt sich, dieses Beispiel mit dem vorangehenden Beispiel zu vergleichen <xref:System.Windows.Media.LineGeometry> .  Die Syntax, die für einen verwendet <xref:System.Windows.Media.PathGeometry> wird, ist viel ausführlicher als die, die für eine einfache verwendet wird <xref:System.Windows.Media.LineGeometry> , und es ist möglicherweise sinnvoller, die <xref:System.Windows.Media.LineGeometry> -Klasse in diesem Fall zu verwenden, aber die ausführliche Syntax von <xref:System.Windows.Media.PathGeometry> ermöglicht extrem komplizierte und komplexe geometrische Bereiche.  
  
 Komplexere Geometrien können mithilfe einer Kombination von-Objekten erstellt werden <xref:System.Windows.Media.PathSegment> .  
  
 Im nächsten Beispiel wird ein <xref:System.Windows.Media.BezierSegment> -, ein-und ein-Typ verwendet, <xref:System.Windows.Media.LineSegment> <xref:System.Windows.Media.ArcSegment> um Form zu erstellen. Im Beispiel wird zuerst eine kubische Bezier-Kurve erstellt, indem vier Punkte definiert werden: ein Startpunkt, der Endpunkt des vorherigen Segments, ein Endpunkt ( <xref:System.Windows.Media.BezierSegment.Point3%2A> ) und zwei Kontrollpunkte ( <xref:System.Windows.Media.BezierSegment.Point1%2A> und <xref:System.Windows.Media.BezierSegment.Point2%2A> ).  Die beiden Steuerungs Punkte einer kubischen Bezier-Kurve Verhalten sich wie Magnete und gewinnen Teile davon, was andernfalls eine gerade Linie ist, wodurch eine Kurve erzeugt wird. Der erste Kontrollpunkt, <xref:System.Windows.Media.BezierSegment.Point1%2A> , wirkt sich auf den Anfangs Abschnitt der Kurve aus. der zweite Kontrollpunkt, <xref:System.Windows.Media.BezierSegment.Point2%2A> , wirkt sich auf den Endabschnitt der Kurve aus.  
  
 Im Beispiel wird dann ein-Objekt hinzugefügt <xref:System.Windows.Media.LineSegment> , das zwischen dem Endpunkt des vorhergehenden, der <xref:System.Windows.Media.BezierSegment> dem durch die-Eigenschaft angegebenen Punkt vorangestellt wurde, gezeichnet wird <xref:System.Windows.Media.LineSegment> .  
  
 Im Beispiel wird dann ein-Objekt hinzugefügt <xref:System.Windows.Media.ArcSegment> , das vom Endpunkt der vorhergehenden <xref:System.Windows.Media.LineSegment> bis zu dem durch die-Eigenschaft angegebenen Punkt gezeichnet wird <xref:System.Windows.Media.ArcSegment.Point%2A> . Im Beispiel werden auch der x-und y-Radius () des Bogens angegeben, <xref:System.Windows.Media.ArcSegment.Size%2A> ein Drehungs Winkel ( <xref:System.Windows.Media.ArcSegment.RotationAngle%2A> ), ein Flag, das angibt, wie groß der Winkel des resultierenden Bogens sein soll ( <xref:System.Windows.Media.ArcSegment.IsLargeArc%2A> ), und ein Wert, der angibt, in welcher Richtung der Bogen gezeichnet wird ( <xref:System.Windows.Media.ArcSegment.SweepDirection%2A> ). Die folgende Abbildung zeigt die durch dieses Beispiel erstellte Form.  
  
 ![Eine PathGeometry](./media/graphicsmm-path2.gif "graphicsmm_path2")  
Eine PathGeometry  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMPathGeometryComplexExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmpathgeometrycomplexexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMPathGeometryComplexExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmpathgeometrycomplexexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMPathGeometryComplexExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmpathgeometrycomplexexample)]  
  
 Noch komplexere Geometrien können mithilfe mehrerer- <xref:System.Windows.Media.PathFigure> Objekte in einer erstellt werden <xref:System.Windows.Media.PathGeometry> .  
  
 Im folgenden Beispiel wird ein <xref:System.Windows.Media.PathGeometry> mit zwei- <xref:System.Windows.Media.PathFigure> Objekten erstellt, die jeweils mehrere- <xref:System.Windows.Media.PathSegment> Objekte enthalten.  Der <xref:System.Windows.Media.PathFigure> aus dem obigen Beispiel und ein <xref:System.Windows.Media.PathFigure> mit <xref:System.Windows.Media.PolyLineSegment> und <xref:System.Windows.Media.QuadraticBezierSegment> werden verwendet.  Ein <xref:System.Windows.Media.PolyLineSegment> -Element wird mit einem Array von Punkten definiert, und das <xref:System.Windows.Media.QuadraticBezierSegment> wird mit einem Kontrollpunkt und einem Endpunkt definiert. Die folgende Abbildung zeigt die durch dieses Beispiel erstellte Form.  
  
 ![Eine PathGeometry](./media/graphicsmm-path.gif "graphicsmm_path")  
Eine PathGeometry mit mehreren Figuren  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMPathGeometryComplexMultiExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmpathgeometrycomplexmultiexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMPathGeometryComplexMultiExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmpathgeometrycomplexmultiexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMPathGeometryComplexMultiExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmpathgeometrycomplexmultiexample)]  
  
### <a name="streamgeometry"></a>StreamGeometry  
 Wie die- <xref:System.Windows.Media.PathGeometry> Klasse definiert eine eine <xref:System.Windows.Media.StreamGeometry> komplexe geometrische Form, die Kurven, Arcs und Linien enthalten kann. Anders als bei einem <xref:System.Windows.Media.PathGeometry> unterstützt der Inhalt von  <xref:System.Windows.Media.StreamGeometry> keine Datenbindung, Animation oder Änderung. Verwenden <xref:System.Windows.Media.StreamGeometry> Sie, wenn Sie eine komplexe Geometrie beschreiben müssen, aber nicht den Aufwand für die Unterstützung von Datenbindung, Animation oder Änderung. Aufgrund der Effizienz ist die- <xref:System.Windows.Media.StreamGeometry> Klasse eine gute Wahl, um Adorner zu beschreiben.  
  
 Ein Beispiel finden Sie unter [Erstellen einer Form mithilfe von StreamGeometry](how-to-create-a-shape-using-a-streamgeometry.md).  
  
### <a name="path-markup-syntax"></a>Pfadmarkupsyntax  
 Die <xref:System.Windows.Media.PathGeometry> -und- <xref:System.Windows.Media.StreamGeometry> Typen unterstützen eine- [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Attribut Syntax mithilfe einer speziellen Reihe von Move-und Draw-Befehlen. Weitere Informationen finden Sie unter [Pfadmarkupsyntax](path-markup-syntax.md).  
  
<a name="wcpsdk_graphics_geometry_introduction2"></a>
## <a name="composite-geometries"></a>Zusammengesetzte Geometrien  
 Zusammengesetzte Geometry-Objekte können mit einem <xref:System.Windows.Media.GeometryGroup> , einem <xref:System.Windows.Media.CombinedGeometry> oder durch Aufrufen der statischen- <xref:System.Windows.Media.Geometry> Methode erstellt werden <xref:System.Windows.Media.Geometry.Combine%2A> .  
  
- Das <xref:System.Windows.Media.CombinedGeometry> -Objekt und die- <xref:System.Windows.Media.Geometry.Combine%2A> Methode führen einen booleschen Vorgang aus, um den durch zwei Geometrien definierten Bereich zu kombinieren. <xref:System.Windows.Media.Geometry> Objekte, die keinen Bereich aufweisen, werden verworfen. <xref:System.Windows.Media.Geometry>Es können nur zwei Objekte kombiniert werden (obwohl diese beiden Geometrien auch zusammengesetzte Geometrien sein können).  
  
- Die- <xref:System.Windows.Media.GeometryGroup> Klasse erstellt eine Zusammenführung der <xref:System.Windows.Media.Geometry> enthaltenen-Objekte, ohne ihren Bereich zu kombinieren. Einer kann eine beliebige Anzahl von- <xref:System.Windows.Media.Geometry> Objekten hinzugefügt werden <xref:System.Windows.Media.GeometryGroup> . Ein Beispiel finden Sie unter [Erstellen einer zusammengesetzten Form](how-to-create-a-composite-shape.md).  
  
 Da Sie keinen kombinierender Vorgang ausführen, bietet die Verwendung von- <xref:System.Windows.Media.GeometryGroup> Objekten Leistungsvorteile gegenüber der Verwendung von- <xref:System.Windows.Media.CombinedGeometry> Objekten oder der- <xref:System.Windows.Media.Geometry.Combine%2A> Methode.  
  
<a name="combindgeometriessection"></a>
## <a name="combined-geometries"></a>Kombinierte Geometrien  
 Im vorherigen Abschnitt wurde das <xref:System.Windows.Media.CombinedGeometry> -Objekt erwähnt, und die- <xref:System.Windows.Media.Geometry.Combine%2A> Methode kombiniert den Bereich, der durch die darin enthaltenen Geometrien definiert ist. Die- <xref:System.Windows.Media.GeometryCombineMode> Enumeration gibt an, wie die Geometrien kombiniert werden. Die möglichen Werte für die- <xref:System.Windows.Media.CombinedGeometry.GeometryCombineMode%2A> Eigenschaft sind: <xref:System.Windows.Media.GeometryCombineMode.Union> , <xref:System.Windows.Media.GeometryCombineMode.Intersect> , <xref:System.Windows.Media.GeometryCombineMode.Exclude> und <xref:System.Windows.Media.GeometryCombineMode.Xor> .  
  
 Im folgenden Beispiel <xref:System.Windows.Media.CombinedGeometry> wird ein mit einem kombinierungsmodus von Union definiert.  Sowohl als <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> auch <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> werden als Kreise desselben Radius definiert, wobei die zentriert durch 50 versetzt werden.  
  
 [!code-xaml[GeometrySample#23](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#23)]  
  
 ![Ergebnisse des Union-Kombinationsmodus](./media/mil-task-combined-geometry-union.PNG "mil_task_combined_geometry_union")  
  
 Im folgenden Beispiel <xref:System.Windows.Media.CombinedGeometry> wird ein mit einem kombinierungsmodus von definiert <xref:System.Windows.Media.GeometryCombineMode.Xor> .  Sowohl als <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> auch <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> werden als Kreise desselben Radius definiert, wobei die zentriert durch 50 versetzt werden.  
  
 [!code-xaml[GeometrySample#24](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#24)]  
  
 ![Ergebnisse des Xor-Kombinationsmodus](./media/mil-task-combined-geometry-xor.PNG "mil_task_combined_geometry_xor")  
  
 Weitere Beispiele finden Sie unter [Erstellen einer zusammengesetzten Form](how-to-create-a-composite-shape.md) und unter [Erstellen von kombinierten Geometrien](how-to-create-a-combined-geometry.md).  
  
<a name="freezable_features"></a>
## <a name="freezable-features"></a>Features von Freezable  
 Da es von der-Klasse erbt <xref:System.Windows.Freezable> , <xref:System.Windows.Media.Geometry> stellt die-Klasse mehrere besondere Features bereit: <xref:System.Windows.Media.Geometry> Objekte können als [XAML-Ressourcen](/dotnet/desktop-wpf/fundamentals/xaml-resources-define)deklariert, von mehreren Objekten gemeinsam genutzt, als schreibgeschützt festgestellt werden, um die Leistung zu verbessern, geklont und Thread sicher gemacht zu werden. Weitere Informationen zu den verschiedenen Funktionen, die von-Objekten bereitgestellt werden <xref:System.Windows.Freezable> , finden Sie unter [Übersicht über](../advanced/freezable-objects-overview.md)frei wählbare Objekte.  
  
<a name="othergeometryfeatures"></a>
## <a name="other-geometry-features"></a>Andere Geometriefeatures  
 Die- <xref:System.Windows.Media.Geometry> Klasse bietet auch nützliche Hilfsmethoden, wie z. b. die folgenden:  
  
- <xref:System.Windows.Media.Geometry.GetArea%2A> : Ruft den Bereich der ab <xref:System.Windows.Media.Geometry> .  
  
- <xref:System.Windows.Media.Geometry.FillContains%2A> : Bestimmt, ob die Geometrie eine andere enthält <xref:System.Windows.Media.Geometry> .  
  
- <xref:System.Windows.Media.Geometry.StrokeContains%2A> : Bestimmt, ob der Strich eines einen <xref:System.Windows.Media.Geometry> angegebenen Punkt enthält.  
  
 Eine komplette Liste der zugehörigen Methoden finden Sie unter der- <xref:System.Windows.Media.Geometry> Klasse.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Geometry>
- <xref:System.Windows.Media.PathGeometry>
- <xref:System.Windows.Shapes.Path>
- <xref:System.Windows.Media.GeometryDrawing>
- [2D-Grafiken und Bildverarbeitung](../advanced/optimizing-performance-2d-graphics-and-imaging.md)
- [Pfad Markup Syntax](path-markup-syntax.md)
- [Artikel zu Vorgehensweisen](geometries-how-to-topics.md)
- [Übersicht über Animationen](animation-overview.md)
- [Übersicht über Formen und die grundlegenden Funktionen zum Zeichnen in WPF](shapes-and-basic-drawing-in-wpf-overview.md)
- [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md)
