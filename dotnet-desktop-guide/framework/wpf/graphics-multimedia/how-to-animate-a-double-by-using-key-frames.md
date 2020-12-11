---
title: 'Gewusst wie: Animieren eines Doubles mithilfe von Keyframes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Doubles [WPF], animating with key frames
- animation [WPF], Doubles with key frames
- key frames [WPF], animating Doubles with
ms.assetid: 3a1a7dba-7694-4907-8a2f-3408baebfa82
ms.openlocfilehash: 9eab794cc8411230226cddc97beaa13c1bdd9405
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977315"
---
# <a name="how-to-animate-a-double-by-using-key-frames"></a>Gewusst wie: Animieren eines Doubles mithilfe von Keyframes
Dieses Beispiel zeigt, wie Sie den Wert einer Eigenschaft animieren, die <xref:System.Double> mithilfe von Keyframes einen annimmt.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Rechteck über den Bildschirm bewegt. Im Beispiel wird die- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Media.TranslateTransform.X%2A> Eigenschaft eines <xref:System.Windows.Media.TranslateTransform> zu animieren, das auf ein angewendet wird <xref:System.Windows.Shapes.Rectangle> . In dieser sich ständig wiederholenden Animation werden drei Keyframes folgendermaßen verwendet:  
  
1. In den ersten drei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.LinearDoubleKeyFrame> um das Rechteck entlang eines Pfads mit konstanter Geschwindigkeit von der Anfangsposition an die 500-Position zu verschieben. Lineare Keyframes, wie z <xref:System.Windows.Media.Animation.LinearDoubleKeyFrame> . b. eine glatte lineare Umstellung zwischen Werten.  
  
2. Am Ende der vierten Sekunde wird von eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.DiscreteDoubleKeyFrame> um das Rechteck plötzlich an die nächste Position zu verschieben. Diskrete Keyframes wie z <xref:System.Windows.Media.Animation.DiscreteDoubleKeyFrame> . b. plötzliche Sprünge zwischen Werten. In diesem Beispiel befindet sich das Rechteck an der Startposition und wird anschließend plötzlich an der Position 500 angezeigt.  
  
3. In den letzten zwei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame> um das Rechteck zurück an seine Anfangsposition zu verschieben. Spline-Keyframes wie das <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame> Erstellen eines Variablen Übergangs zwischen Werten gemäß dem Wert der- <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame.KeySpline%2A> Eigenschaft. In diesem Beispiel bewegt sich das Rechteck zunächst langsam und beschleunigt dann exponentiell im letzten Bereich des Zeitabschnitts.  
  
 [!code-csharp[keyframes_snip#AltDoubleAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/AltDoubleAnimationUsingKeyFramesExample.cs#altdoubleanimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#AltDoubleAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/altdoubleanimationusingkeyframesexample.vb#altdoubleanimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#AltDoubleAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/AltDoubleAnimationUsingKeyFramesExample.xaml#altdoubleanimationusingkeyframeswholepage)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).  
  
 Aus Gründen der Konsistenz mit anderen Animations Beispielen wird in den Code Versionen dieses Beispiels ein-Objekt verwendet, <xref:System.Windows.Media.Animation.Storyboard> um das anzuwenden <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> . Wenn Sie eine einzelne Animation im Code anwenden, ist es auch einfacher, die-Methode zu verwenden, <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> anstatt zu verwenden <xref:System.Windows.Media.Animation.Storyboard> . Ein Beispiel finden Sie unter [Animieren einer Eigenschaft ohne Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>
- <xref:System.Windows.Shapes.Rectangle>
- <xref:System.Windows.Media.Animation.LinearDoubleKeyFrame>
- <xref:System.Windows.Media.Animation.DiscreteDoubleKeyFrame>
- <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame>
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Themen zur Vorgehensweise mit Keyframes](key-frame-animation-how-to-topics.md)
