---
title: 'Gewusst wie: Zeitliche Steuerung einer Keyframe-Animation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- key frames [WPF], timing
- timing key-frame animation
ms.assetid: b059216f-7d4b-4ca8-a019-bc287ee7bf16
ms.openlocfilehash: 8cfd2be0bbc526ed92a5fb1b558a5a41dc9c3113
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977631"
---
# <a name="how-to-control-key-frame-animation-timing"></a>Gewusst wie: Zeitliche Steuerung einer Keyframe-Animation

In diesem Beispiel wird gezeigt, wie die zeitliche Steuerung von Keyframes innerhalb einer Keyframe-Animation gesteuert wird. Wie andere Animationen verfügen Keyframe-Animationen über eine- <xref:System.Windows.Media.Animation.Timeline.Duration%2A> Eigenschaft. Zusätzlich zur Angabe der Dauer einer Animation müssen Sie angeben, welcher Teil dieser Dauer den einzelnen Keyframes zugewiesen wird. Um die Zeit festzulegen, geben Sie <xref:System.Windows.Media.Animation.KeyTime> für jeden Keyframe in der Animation ein an.

Der <xref:System.Windows.Media.Animation.KeyTime> for each-Keyframe gibt an, wann ein Keyframe endet (er gibt nicht an, wie lange ein Keyframe wiedergegeben wird). Sie können als <xref:System.Windows.Media.Animation.KeyTime> <xref:System.TimeSpan> Wert, als Prozentsatz oder als <xref:System.Windows.Media.Animation.KeyTime.Uniform%2A> <xref:System.Windows.Media.Animation.KeyTime.Paced%2A> besonderen Wert angeben.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird verwendet <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> , um ein Rechteck auf dem Bildschirm zu animieren. Die Schlüssel Zeiten der Keyframes werden mit Werten festgelegt <xref:System.TimeSpan> .

[!code-csharp[keyframes_snip#KeyTimesTimeSpanExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimestimespanexample)]
[!code-vb[keyframes_snip#KeyTimesTimeSpanExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimestimespanexample)]
[!code-xaml[keyframes_snip#KeyTimesTimeSpanExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimestimespanexample)]

In der folgenden Abbildung wird gezeigt, wann der Wert jedes Keyframes erreicht wird.

![Schlüsselwerte werden nach 3, 4 und 10 Sekunden erreicht](./media/graphicsmm-keyframe-keytime1-timespan.png "graphicsmm_keyframe_keytime1_timespan")

Das nächste Beispiel zeigt eine identische Animation, mit der Ausnahme, dass die Schlüssel Zeiten der Keyframes mit Prozentwerten festgelegt werden.

[!code-csharp[keyframes_snip#KeyTimesPercentageExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimespercentageexample)]
[!code-vb[keyframes_snip#KeyTimesPercentageExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimespercentageexample)]
[!code-xaml[keyframes_snip#KeyTimesPercentageExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimespercentageexample)]

In der folgenden Abbildung wird gezeigt, wann der Wert jedes Keyframes erreicht wird.

![Schlüsselwerte werden nach 3, 4 und 10 Sekunden erreicht](./media/graphicsmm-keyframe-keytime2-percentage.png "graphicsmm_keyframe_keytime2_percentage")

Im nächsten Beispiel werden <xref:System.Windows.Media.Animation.KeyTime.Uniform%2A> Schlüssel Zeitwerte verwendet.

[!code-csharp[keyframes_snip#KeyTimesUniformExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimesuniformexample)]
[!code-vb[keyframes_snip#KeyTimesUniformExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimesuniformexample)]
[!code-xaml[keyframes_snip#KeyTimesUniformExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimesuniformexample)]

In der folgenden Abbildung wird gezeigt, wann der Wert jedes Keyframes erreicht wird.

![Schlüsselwerte werden nach 3,3, 6,6 und 9,9 Sekunden erreicht](./media/graphicsmm-keyframe-keytime3-uniform.png "graphicsmm_keyframe_keytime3_uniform")

Im letzten Beispiel werden <xref:System.Windows.Media.Animation.KeyTime.Paced%2A> Schlüssel Zeitwerte verwendet.

[!code-csharp[keyframes_snip#KeyTimesPacedExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimespacedexample)]
[!code-vb[keyframes_snip#KeyTimesPacedExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimespacedexample)]
[!code-xaml[keyframes_snip#KeyTimesPacedExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimespacedexample)]

In der folgenden Abbildung wird gezeigt, wann der Wert jedes Keyframes erreicht wird.

![Schlüsselwerte werden nach 0, 5 und 10 Sekunden erreicht](./media/graphicsmm-keyframe-keytime4-paced.png "graphicsmm_keyframe_keytime4_paced")

Der Einfachheit halber werden in den Code Versionen dieses Beispiels lokale Animationen verwendet, nicht Storyboards, da nur eine einzelne Animation auf eine einzelne Eigenschaft angewendet wird, die Beispiele jedoch möglicherweise so geändert werden, dass Storyboards verwendet werden. Ein Beispiel für das Deklarieren eines Storyboards im Code finden Sie unter [Animieren einer Eigenschaft mithilfe eines Storyboards](how-to-animate-a-property-by-using-a-storyboard.md).

Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation). Weitere Informationen zu Keyframe-Animationen finden Sie unter [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md).

## <a name="see-also"></a>Siehe auch

- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Übersicht über Animationen](animation-overview.md)
- [Artikel zu Vorgehensweisen](animation-and-timing-how-to-topics.md)
