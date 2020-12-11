---
title: Übersicht über 3D-Transformationen
ms.date: 03/30/2017
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- 3D transformations
- transformations [WPF], 3D
ms.assetid: e45e555d-ac1e-4b36-aced-e433afe7f27f
ms.openlocfilehash: fe6c7061b6cd2f57ace1765c898dac1d1f797cab
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977882"
---
# <a name="3d-transformations-overview"></a>Übersicht über 3D-Transformationen
In diesem Thema wird beschrieben, wie Sie Transformationen auf 3D-Modelle im [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Grafiksystem anwenden. Mit Transformationen können Entwickler die Position und Größe von Modellen ändern und sie neu ausrichten, ohne die Basiswerte zu verändern, die sie definieren.  

## <a name="3d-coordinate-space"></a>3D-Koordinaten Bereich  
 3D-Grafik Inhalte in werden [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] in einem Element <xref:System.Windows.Controls.Viewport3D> gekapselt,, das an der zweidimensionalen Elementstruktur teilnehmen kann. Das Grafiksystem behandelt Viewport3D als ein zweidimensionales visuelles Objekt, wie viele andere auch in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)]. Viewport3D fungiert als Fenster – ein Anzeigebereich – in eine dreidimensionale Szene. Genauer betrachtet ist es eine Oberfläche, auf der eine 3D-Szene projiziert wird.  Obwohl Sie Viewport3D mit anderen 2D-Zeichnungsobjekten im gleichen Szenen Diagramm verwenden können, ist es nicht möglich, 2D-und 3D-Objekte innerhalb einer Viewport3D zu interagieren. In der folgenden Erläuterung ist der beschriebene Koordinatenraum im Viewport3D-Element enthalten.  
  
 Das [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Koordinatensystem für 2D-Grafiken sucht den Ursprung in der oberen linken Ecke der Renderingoberfläche (in der Regel der Bildschirm). Im 2D-System werden die positiven Werte der x-Achse nach rechts und die positiven Werte der y-Achse nach unten fortgesetzt. Im 3D-Koordinatensystem befindet sich der Ursprung jedoch in der Mitte des Bildschirms, und die positiven Werte der x-Achse werden nach rechts fortgesetzt, aber die positiven Werte der y-Achse werden stattdessen weiter oben fortgesetzt, und positive z-Achsen Werte werden nach außen vom Ursprung an den Viewer weitergeführt.  
  
 ![Koordinatensysteme](./media/coordsystem-1.png "Coordsystem-1")  
Vergleich der Koordinatensysteme  
  
 Der von diesen Achsen definierte Raum ist der stationäre Frame des Verweises für 3D-Objekte in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] . Wenn Sie innerhalb dieses Raumes Modelle erstellen und Lichter und Kameras, um sie anzuzeigen, ist es hilfreich, diesen feststehenden Verweisrahmen oder „Weltenraum“ vom lokalen zu unterscheiden, den Sie beim Anwenden von Transformationen für jedes Modell erstellen. Beachten Sie außerdem, dass Objekte im Weltenraum je nach der Kamera und den Einstellungen völlig anders oder überhaupt nicht angezeigt werden können. Die Position der Kamera ändert aber nicht die Position von Objekten im Weltenraum.  
  
## <a name="transforming-models"></a>Transformieren von Modellen  
 Wenn Sie Modelle erstellen, verfügen diese über eine bestimmte Position in der Szene. Um die Position dieser Modelle in der Szene zu verändern, sie zu drehen oder ihre Größe zu ändern, sollten Sie nicht die Vertices ändern, die die Modelle selbst definieren. Stattdessen können Sie wie in 2D Transformationen auf Modelle anwenden.  
  
 Jedes Modell Objekt verfügt über eine- <xref:System.Windows.Media.Media3D.Model3D.Transform%2A> Eigenschaft, mit der Sie das Modell verschieben, neu ausrichten oder die Größe ändern können. Wenn Sie eine Transformation anwenden, versetzen Sie alle Punkte des Modells um den in der Transformation angegebenen Vektor oder Wert. Sie haben also den Koordinatenbereich transformiert, in dem das Modell definiert ist (Modellraum), aber Sie haben noch nicht die Werte geändert, die die Geometrie des Modells im Koordinatensystem der gesamten Szene („Weltenraum“) ausmachen.  
  
## <a name="translation-transformations"></a>Übersetzungstransformationen  
 3D-Transformationen erben von der abstrakten Basisklasse <xref:System.Windows.Media.Media3D.Transform3D> . dazu gehören die affinen Transformations Klassen <xref:System.Windows.Media.Media3D.TranslateTransform3D> , <xref:System.Windows.Media.Media3D.ScaleTransform3D> und <xref:System.Windows.Media.Media3D.RotateTransform3D> . Das [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] 3D-System bietet auch eine <xref:System.Windows.Media.Media3D.MatrixTransform3D> Klasse, mit der Sie dieselben Transformationen in präziseren Matrix Vorgängen angeben können.  
  
 <xref:System.Windows.Media.Media3D.TranslateTransform3D> Verschiebt alle Punkte in der Model3D in die Richtung des von Ihnen angegebenen Offset Vektors mit den <xref:System.Windows.Media.Media3D.TranslateTransform3D.OffsetX%2A> <xref:System.Windows.Media.Media3D.TranslateTransform3D.OffsetY%2A> Eigenschaften, und <xref:System.Windows.Media.Media3D.TranslateTransform3D.OffsetZ%2A> . Bei einem Vertex eines Würfels auf (2,2,2) würde ein Offsetvektor von (0,1.6,1) den Vertex (2,2,2) auf (2,3.6,3).) verschieben. Der Vertex des Würfels befindet sich noch immer auf (2,2,2) im Modellraum. Da sich nun aber die Beziehung des Modellraums zum Weltenraum geändert hat, entsprechen die Koordinaten (2,2,2) im Modellraum den Koordinaten (2,3.6,3) im Weltenraum.  
  
 ![Abbildung der Übersetzung](./media/transforms-translate.png "Transforms-Translate")  
Übersetzung mit Offset  
  
 In den folgenden Codebeispielen wird die Anwendung einer Übersetzung veranschaulicht.  
  
 [!code-xaml[animation3dgallery_snip#Translation3DAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationexamplewholepage)]  
  
## <a name="scale-transformations"></a>Skalierungstransformationen  
 <xref:System.Windows.Media.Media3D.ScaleTransform3D> ändert die Skalierung des Modells um einen angegebenen Skalierungs Vektor mit Verweis auf einen Mittelpunkt. Geben Sie eine einheitliche Skalierung an, die das Modell um den gleichen Wert auf den x-, y- und z-Achsen skaliert, um die Größe des Modells proportional zu ändern. Wenn Sie z. b. die-Eigenschaft, die-Eigenschaft und die-Eigenschaft auf 0,5 festlegen, wird <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleZ%2A> die Größe des Modells halbiert; das Festlegen der gleichen Eigenschaften auf 2 verdoppelt die Skalierung in allen drei Achsen.  
  
 ![Einheitliches ScaleTransform3D](./media/threecubes-uniformscale-1.png "threecubes_uniformscale_1")  
ScaleVector-Beispiel  
  
 Durch Angabe einer ungleichmäßigen Skalierungstransformation – eine Skalierungstransformation, deren x-, y- und z-Werte nicht alle identisch sind – kann ein Modell in einer oder zwei Dimensionen ohne Auswirkung auf die anderen gestreckt oder verkleinert werden. Wenn Sie z. b. <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> auf 1, <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> auf 2 und <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleZ%2A> auf 1 festlegen, bewirkt dies, dass das transformierte Modell die Höhe verdoppelt, aber an der X-und Z-Achse unverändert bleibt.  
  
 Aufgrund von ScaleTransform3D erweitern oder verkleinern sich Vertices standardmäßig um den Ursprung (0,0,0). Wenn das Modell, das Sie transformieren möchten, nicht vom Ursprung aus gezeichnet wurde, wird eine Skalierung vom Ursprung aus das Modell nicht „an Ort und Stelle“ skalieren. Stattdessen wird das Modell durch den Skalierungsvorgang sowohl übersetzt als auch skaliert, wenn die Vertices des Modells mit dem Skalierungsvektor multipliziert werden.  
  
 ![Drei mit einem angegebenen Mittelpunkt skalierte Würfel](./media/threecubes-scaledwithcenter-1.png "threecubes_scaledwithcenter_1")  
Beispiel für die Skalierung um den Mittelpunkt  
  
 Um ein Modell "an Ort und Stelle" zu skalieren, geben Sie den Mittelpunkt des Modells an, indem Sie die <xref:System.Windows.Media.ScaleTransform.CenterX%2A> Eigenschaften ScaleTransform3D's, <xref:System.Windows.Media.ScaleTransform.CenterY%2A> und festlegen <xref:System.Windows.Media.Media3D.ScaleTransform3D.CenterZ%2A> . Dadurch wird sichergestellt, dass das Grafiksystem den Modellbereich skaliert und dann in den Mittelpunkt des angegebenen übersetzt <xref:System.Windows.Media.Media3D.Point3D> . Wenn Sie das Modell umgekehrt um den Ursprung erstellt haben und geben einen anderen Mittelpunkt angeben, wird das Modell vom Ursprung weg übersetzt.  
  
## <a name="rotation-transformations"></a>Rotationstransformationen  
 Sie können ein Modell in 3D auf verschiedene Weise drehen. Eine normale Rotationstransformation gibt eine Achse und einen Drehwinkel um diese Achse an. Mit der- <xref:System.Windows.Media.Media3D.RotateTransform3D> Klasse können Sie eine <xref:System.Windows.Media.Media3D.Rotation3D> mit der- <xref:System.Windows.Media.Media3D.RotateTransform3D.Rotation%2A> Eigenschaft definieren. Anschließend geben Sie <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Axis%2A> die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Angle%2A> für Rotation3D, in diesem Fall <xref:System.Windows.Media.Media3D.AxisAngleRotation3D> , an, um die Transformation zu definieren. In den folgenden Beispielen wird ein Modell um 60 Grad um die y-Achse gedreht.  
  
 [!code-xaml[animation3dgallery_snip#Rotate3DUsingAxisAngleRotation3DExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Rotat3DUsingAxisAngleRotation3DExample.xaml#rotate3dusingaxisanglerotation3dexamplewholepage)]  
  
 Hinweis: [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] 3D ist ein rechts übergebenen System, was bedeutet, dass ein positiver Winkelwert für eine Drehung eine Drehung gegen den Uhrzeigersinn zur Achse ergibt.  
  
 Bei Achsen Spitzen Drehungen wird die Drehung über den Ursprung angenommen, wenn für die <xref:System.Windows.Media.Media3D.RotateTransform3D.CenterX%2A> <xref:System.Windows.Media.Media3D.RotateTransform3D.CenterY%2A> Eigenschaften, und <xref:System.Windows.Media.Media3D.RotateTransform3D.CenterZ%2A> auf RotateTransform3D kein Wert angegeben wurde. Wie bei der Skalierung ist es hilfreich zu wissen, dass die Rotation den gesamten Koordinatenraum des Modells transformiert. Wenn das Modell nicht um den Ursprung erstellt wurde oder bereits übersetzt wurde, könnte die Drehung um den Ursprung und nicht an Ort und Stelle erfolgen.  
  
 ![Drehung mit neuem Mittelpunkt](./media/threecubes-rotationwithcenter-1.png "threecubes_rotationwithcenter_1")  
Drehung mit neuem, angegebenen Mittelpunkt  
  
 Geben Sie zum Drehen des Modells „an Ort und Stelle“ den tatsächlichen Mittelpunkt des Modells als Mittelpunkt der Rotation an. Da die Geometrie in der Regel um den Ursprung modelliert wird, sollten Sie zuerst die Größe des Modells anpassen (skalieren), dann die Ausrichtung festlegen (drehen) und es anschließend an die gewünschte Position verschieben (übersetzen). So erzielen Sie bei einer Reihe von Transformationen normalerweise das erwünschte Ergebnis.  
  
 ![Drehung um 60 Grad auf der x&#45; und y&#45;Achse](./media/twocubes-rotation2axes-1.png "twocubes_rotation2axes_1")  
Rotationsbeispiele  
  
 Achsen-Winkel-Rotationen eignen sich für statische Transformationen und einige Animationen. Denken Sie jedoch daran, ein Cube-Modell um die X-Achse um 60 Grad zu drehen, und um die Z-Achse um 45 Grad. Sie können diese Transformation als zwei diskrete affine Transformationen oder als Matrix beschreiben. Die Animation der beschriebenen Rotation kann sich aber als problematisch herausstellen. Obwohl die Anfangs- und Endposition des Modells bei beiden Ansätzen identisch sind, sind die Zwischenpositionen des Modells rechnerisch nicht sicher. Quaternionen stellen eine alternative Möglichkeit zum Berechnen der Interpolation zwischen dem Start und dem Ende einer Rotation dar.  
  
 Eine Quaternion stellt eine Achse im 3D-Raum und eine Drehung um diese Achse dar. Eine Quaternion kann z.B. eine Achse (1,1,2) und eine Drehung um 50 Grad darstellen. Die Leistungsstärke von Quaternionen beim Definieren von Rotationen gründet in zwei Vorgängen, die Sie dafür ausführen können: die Zusammensetzung und die Interpolation. Die auf eine Geometrie angewendete Zusammensetzung von zwei Quaternionen bedeutet, dass die Geometrie um Achse2 um Rotation2 und anschließend um Achse1 um Rotation1 gedreht wird. Mithilfe der Zusammensetzung können Sie diese zwei Rotationen der Geometrie kombinieren, um eine einzelne Quaternion zu erstellen, die das Ergebnis darstellt. Da die Interpolation von Quaternionen einen eindeutigen Pfad von einer Achse und ihrer Ausrichtung zu einer anderen berechnen kann, können Sie vom Original zum zusammengesetzten Quaternion interpolieren, um einen reibungslosen Übergang von einem zum anderen zu erreichen und die Transformation dadurch zu animieren. Für Modelle, die Sie animieren möchten, können Sie ein Ziel <xref:System.Windows.Media.Media3D.Quaternion> für die Drehung angeben, indem Sie <xref:System.Windows.Media.Media3D.QuaternionRotation3D> für die- <xref:System.Windows.Media.Media3D.RotateTransform3D.Rotation%2A> Eigenschaft verwenden.  
  
## <a name="using-transformation-collections"></a>Verwenden von Auflistungstransformationen  
 Beim Erstellen einer Szene ist es üblich, mehr als eine Transformation auf ein Modell anzuwenden. Fügen Sie Transformationen zur-Auflistung <xref:System.Windows.Media.Media3D.Transform3DGroup.Children%2A> der- <xref:System.Windows.Media.Media3D.Transform3DGroup> Klasse hinzu, um Transformationen bequem zu gruppieren und auf verschiedene Modelle in der Szene anzuwenden. Häufig ist es sinnvoll, eine Transformation in mehreren verschiedenen Gruppen wiederzuverwenden, so wie Sie auch ein Modell durch Anwenden eines anderen Satzes von Transformationen auf jede Instanz wiederverwenden können. Beachten Sie, dass die Reihenfolge, in der die Transformationen der Auflistung hinzugefügt werden, relevant ist: Die ersten Transformationen in der Auflistung werden zuerst und die letzten zuletzt angewendet.  
  
## <a name="animating-transformations"></a>Animieren von Transformationen  
 Die [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] 3D-Implementierung ist an demselben Zeit-und Animationssystem beteiligt wie 2D-Grafiken. Das heißt, um eine 3D-Szene zu animieren, animieren Sie die Eigenschaften der Modelle. Es ist möglich, die Eigenschaften von primitiven Typen direkt zu animieren. In der Regel ist es aber einfacher, Transformationen zu animieren, die die Position oder die Darstellung von Modellen ändern. Da Transformationen <xref:System.Windows.Media.Media3D.Model3DGroup> sowohl auf Objekte als auch auf einzelne Modelle angewendet werden können, ist es möglich, einen Satz von Animationen auf die untergeordneten Elemente eines Model3DGroup und einen anderen Satz von Animationen auf eine Gruppe von Objekten anzuwenden.  Hintergrundinformationen zum Zeitsteuerungs- und Animationssystem von [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] finden Sie unter [Übersicht über Animationen](animation-overview.md) und [Übersicht über Storyboards](storyboards-overview.md).  
  
 Um ein Objekt in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] zu animieren, erstellen Sie eine Zeitachse, definieren Sie eine Animation (die im Zeitablauf eine tatsächliche Änderung einiger Eigenschaftswerte darstellt), und geben Sie die Eigenschaft an, auf die die Animation angewendet werden soll. Diese Eigenschaft muss eine Eigenschaft von FrameworkElement sein. Da alle Objekte in einer 3D-Szene untergeordnete Elemente von Viewport3D sind, sind die Eigenschaften, die für jede Animation gelten, die Sie auf die Szene anwenden möchten, Eigenschaften der Eigenschaften von Viewport3D. Es ist wichtig, den Eigenschaftenpfad für die Animation sorgfältig anzupassen, da die Syntax sehr ausführlich sein kann.  
  
 Angenommen Sie möchten ein Objekt an Ort und Stelle drehen und außerdem eine Schwingbewegung darauf anwenden, um mehr von dem anzuzeigenden Objekt darzustellen. Sie können dazu RotateTransform3D auf das Modell anwenden und dessen Rotationsachse von einem Vektor zu einem anderen animieren. Im folgenden Codebeispiel wird veranschaulicht, wie ein <xref:System.Windows.Media.Animation.Vector3DAnimation> auf die Axis-Eigenschaft des Rotation3D der Transformation angewendet wird, wobei angenommen wird, dass das RotateTransform3D eine von mehreren Transformationen ist, die auf das Modell mit einem angewendet werden <xref:System.Windows.Media.TransformGroup> .  
  
 [!code-csharp[3doverview#3DOverview3DN1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DOverview/CSharp/Window1.xaml.cs#3doverview3dn1)]
 [!code-vb[3doverview#3DOverview3DN1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/3DOverview/visualbasic/window1.xaml.vb#3doverview3dn1)]  
  
 [!code-csharp[3doverview#3DOverview3DN3](~/samples/snippets/csharp/VS_Snippets_Wpf/3DOverview/CSharp/Window1.xaml.cs#3doverview3dn3)]
 [!code-vb[3doverview#3DOverview3DN3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/3DOverview/visualbasic/window1.xaml.vb#3doverview3dn3)]  
  
 Verwenden Sie eine ähnliche Syntax, um auf andere zu verschiebende Transformationseigenschaften abzuzielen oder das Objekt zu skalieren.  Beispielsweise können Sie auf <xref:System.Windows.Media.Animation.Point3DAnimation> die ScaleCenter-Eigenschaft einer Skalierungs Transformation anwenden, um zu bewirken, dass die Form eines Modells reibungslos verzerrt wird.  
  
 Obwohl in den vorangehenden Beispielen die Eigenschaften von transformiert <xref:System.Windows.Media.Media3D.GeometryModel3D> werden, ist es auch möglich, die Eigenschaften anderer Modelle in der Szene zu transformieren.  Durch die Animation von Übersetzungen, die z.B. auf Lichtobjekte angewendet werden, können Sie wechselnde Licht- und Schatteneffekte erstellen, die die Darstellung eines Modells eindrucksvoll ändern.  
  
 Da Kameras auch Modelle sind, können Kameraeigenschaften ebenfalls transformiert werden.  Sie können zwar die Darstellung der Szene durch die Transformation der Kameraposition oder der Ebenenabstände (also die Projektion der gesamten Szene) ändern, allerdings ergeben viele der so erzielten Effekte als auf die Modellposition angewendete Transformationen optisch kaum Sinn für den Zuschauer.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
- [Übersicht über Transformationen](transforms-overview.md)
- [Beispiel für 2D-Transformationen](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms)
