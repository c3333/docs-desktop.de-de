---
title: 'Gewusst wie: Steuern des Ausfüllens einer zusammengesetzten Form'
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], composite [WPF], controlling fill
- composite shapes [WPF], controlling fill
- graphics [WPF], composite shapes
- fill [WPF], controlling
ms.assetid: c1c94575-9eca-48a5-a49a-2ec65259f229
ms.openlocfilehash: 89f69d392e8838af99538c759a2f06453e1bcd60
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977626"
---
# <a name="how-to-control-the-fill-of-a-composite-shape"></a>Gewusst wie: Steuern des Ausfüllens einer zusammengesetzten Form

Die- <xref:System.Windows.Media.GeometryGroup.FillRule%2A> Eigenschaft eines-Objekts <xref:System.Windows.Media.GeometryGroup> oder eines-Objekts <xref:System.Windows.Media.PathGeometry> gibt eine "Rule" an, die von der zusammengesetzten Form verwendet wird, um zu bestimmen, ob ein bestimmter Punkt Teil der Geometrie ist. Es gibt zwei mögliche Werte für <xref:System.Windows.Media.FillRule> : <xref:System.Windows.Media.FillRule.EvenOdd> und <xref:System.Windows.Media.FillRule.Nonzero> . In den folgenden Abschnitten wird beschrieben, wie diese beiden Regeln verwendet werden.

**EvenOdd:** Diese Regel ermittelt, ob sich ein Punkt im Ausfüllbereich befindet, indem von diesem Punkt aus ein Strahl in beliebiger Richtung gegen Unendlich gezeichnet wird und die Anzahl der vom Strahl geschnittenen Pfadsegmente in der Form gezählt wird. Bei einer ungeraden Zahl liegt der Punkt innen, und bei einer geraden Zahl liegt er außen.

Beispielsweise wird mit dem folgenden XAML-Code eine zusammengesetzte Form erstellt, die aus einer Reihe von konzentrischen Ringen (Target) besteht, wobei <xref:System.Windows.Media.GeometryGroup.FillRule%2A> auf festgelegt ist <xref:System.Windows.Media.FillRule.EvenOdd> .

[!code-xaml[GeometriesMiscSnippets_snip#FillRuleEvenOddValue](~/samples/snippets/xaml/VS_Snippets_Wpf/GeometriesMiscSnippets_snip/XAML/FillRuleExample.xaml#fillruleevenoddvalue)]

Die folgende Abbildung zeigt die im vorherigen Beispiel erstellte Form.

![Ein Kreis, der aus einem konzentrischen Satz von Reihen mit wechselnden Farben besteht.](./media/how-to-control-the-fill-of-a-composite-shape/fillrule-evenodd-property.png)

Beachten Sie in der obigen Abbildung, dass der Mittelpunkt und der dritte Ring nicht gefüllt sind. Dies ist darauf zurückzuführen, dass ein Strahl, der von einem beliebigen Punkt innerhalb eines dieser beiden Ringe gezeichnet wird, eine gerade Anzahl von Segmenten schneidet. Sehen Sie sich die folgende Abbildung an:

![Diagramm, das die im Kreis gezeichneten EvenOdd-Strahlen anzeigt.](./media/how-to-control-the-fill-of-a-composite-shape/fillrule-evenodd-rays.png)

**NonZero:** Diese Regel bestimmt, ob sich ein Punkt im Ausfüllbereich im Pfad befindet, indem ein unendlicher Strahl von diesem Punkt in eine beliebige Richtung gezeichnet wird und anschließend die Stellen überprüft werden, an denen ein Segment der Form den Strahl schneidet. Beginnen Sie mit dem Wert 0 (null), und addieren Sie für jede Stelle, an der ein Segment den Strahl von links nach rechts schneidet, den Wert 1. Wenn das Ergebnis nach dem Zählen der Überschneidungen 0 (null) ist, liegt der Punkt außerhalb des Pfads. Andernfalls liegt er innerhalb des Pfads.

[!code-xaml[GeometriesMiscSnippets_snip#FillRuleNonZeroValueEllipseGeometry](~/samples/snippets/xaml/VS_Snippets_Wpf/GeometriesMiscSnippets_snip/XAML/FillRuleExample.xaml#fillrulenonzerovalueellipsegeometry)]

Mit dem vorherigen Beispiel <xref:System.Windows.Media.FillRule.Nonzero> <xref:System.Windows.Media.GeometryGroup.FillRule%2A> ergibt der Wert für die folgende Abbildung als Ergebnis:

![Ein Kreis, der aus einer Reihen konzentrischen Reihenfolge besteht, die alle mit derselben Farbe gefüllt ist.](./media/how-to-control-the-fill-of-a-composite-shape/fillrule-value-nonzero.png)

Wie Sie sehen können, sind alle Ringe ausgefüllt. Dies kommt daher, dass alle Segmente in die gleiche Richtung verlaufen und deshalb ein Strahl, der von einem beliebigen Punkt aus gezeichnet wird, ein oder mehrere Segmente schneidet, sodass die Summe der Schnitte ungleich 0 (null) ist. In der folgenden Abbildung stellen die roten Pfeile z. b. die Richtung dar, in der die Segmente gezeichnet werden, und der weiße Pfeil stellt einen beliebigen Strahl dar, der von einem Punkt im inneren Ring ausgeht. Ausgehend vom Wert 0 (null) wird für jedes Segment, das der Strahl schneidet, der Wert 1 addiert, da das Segment den Strahl von links nach rechts schneidet.

![Diagramm, das den FillRule-Eigenschafts Wert ungleich 0 (null) anzeigt.](./media/how-to-control-the-fill-of-a-composite-shape/fillrule-value-equal-nonzero.png)

Um das Verhalten einer Regel besser zu veranschaulichen, <xref:System.Windows.Media.FillRule.Nonzero> ist eine komplexere Form erforderlich, in der Segmente in verschiedenen Richtungen ausgeführt werden. Der folgende XAML-Code erstellt eine ähnliche Form wie das vorherige Beispiel, mit der Ausnahme, dass Sie mit einem anstelle von erstellt wird <xref:System.Windows.Media.PathGeometry> <xref:System.Windows.Media.EllipseGeometry> , das vier konzentrische Bögen erstellt, anstatt konzentrische Kreise vollständig geschlossen zu haben.

[!code-xaml[GeometriesMiscSnippets_snip#FillRuleNonZeroValuePathGeometry](~/samples/snippets/xaml/VS_Snippets_Wpf/GeometriesMiscSnippets_snip/XAML/FillRuleExample.xaml#fillrulenonzerovaluepathgeometry)]

Die folgende Abbildung zeigt die im vorherigen Beispiel erstellte Form.

![Ein Kreis, der aus einer Reihe von konzentrischen Ringen mit wechselnden Farben besteht, in denen der dritte Bogen nicht aufgefüllt ist.](./media/how-to-control-the-fill-of-a-composite-shape/pathgeometry-concentric-arcs.png)

Beachten Sie, dass der dritte Bogen ab der Mitte nicht ausgefüllt ist. In der folgenden Abbildung wird gezeigt, warum dies ist. In der Abbildung stellen die roten Pfeile die Richtung dar, in der die Segmente gezeichnet werden. Die beiden weißen Pfeile stellen zwei zufällige Strahlen dar, die von einem Punkt im „nicht ausgefüllten“ Bereich ausgehen. Wie aus der Abbildung ersichtlich, ist die Summe der Werte eines bestimmten Strahls, der die Segmente in seinem Pfad schneidet, gleich 0 (null). Wie oben bereits definiert, bedeutet eine Summe von null, dass der Punkt nicht Teil der Geometrie ist (kein Teil der Füllung), während eine Summe, die *ungleich* null oder negativ ist, Teil der Geometrie ist.

![Diagramm, das beliebige Strahlen Überschreitungen von Segmenten anzeigt.](./media/how-to-control-the-fill-of-a-composite-shape/arbitrary-ray-cross-segment.png)

> [!NOTE]
> Im Sinne von <xref:System.Windows.Media.FillRule> werden alle Formen als geschlossen betrachtet. Wenn in einem Segment eine Lücke vorhanden ist, zeichnen Sie eine gedachte Linie, um sie zu schließen. Im oben aufgeführten Beispiel weisen die Ringe kleine Lücken auf. Daher könnte man erwarten, dass ein Strahl durch die Lücke verläuft und ein anderes Ergebnis ergibt als ein Strahl, der in eine andere Richtung verläuft. Im folgenden finden Sie eine vergrößerte Abbildung einer dieser Lücken und des "imaginären Segments" (Segment, das zum Anwenden der gezeichnet wird <xref:System.Windows.Media.FillRule> ), das Sie schließt.

![Diagramm, das FillRule-Segmente anzeigt, die immer geschlossen sind.](./media/how-to-control-the-fill-of-a-composite-shape/fillrule-closed-segments.png)

## <a name="example"></a>Beispiel

## <a name="see-also"></a>Siehe auch

- [Erstellen einer zusammengesetzten Form](how-to-create-a-composite-shape.md)
- [Übersicht über die Geometrie](geometry-overview.md)
