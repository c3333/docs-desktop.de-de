---
title: 'Gewusst wie: Animieren eines Point mithilfe von Keyframes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- key frames [WPF], animating Points with
- Points [WPF], animating with key frames
- animation [WPF], Points with key frames
ms.assetid: d2e2ef10-0773-4133-856e-d41c09f60ded
ms.openlocfilehash: edcba36644cf78d6e98f934d9bd8b593af38b328
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977313"
---
# <a name="how-to-animate-a-point-by-using-key-frames"></a>Gewusst wie: Animieren eines Point mithilfe von Keyframes
In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames> Klasse zum Animieren eines verwendet wird <xref:System.Windows.Point> .  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird eine Ellipse entlang eines dreieckigen Pfads verschoben. Im Beispiel wird die- <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Media.EllipseGeometry.Center%2A> Eigenschaft eines zu animieren <xref:System.Windows.Media.EllipseGeometry> . In dieser Animation werden drei Keyframes folgendermaßen verwendet:  
  
1. In der ersten halben Sekunde wird von eine Instanz der- <xref:System.Windows.Media.Animation.LinearPointKeyFrame> Klasse verwendet, um die Ellipse auf einem Pfad mit konstanter Geschwindigkeit von der Anfangsposition zu verschieben. Lineare Keyframes, wie z <xref:System.Windows.Media.Animation.LinearPointKeyFrame> . b. eine glatte lineare interpolung zwischen Werten.  
  
2. Am Ende der nächsten halben Sekunde wird von eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.DiscretePointKeyFrame> um die Ellipse entlang des Pfads an die nächste Position zu verschieben. Diskrete Keyframes wie z <xref:System.Windows.Media.Animation.DiscretePointKeyFrame> . b. plötzliche Sprünge zwischen Werten.  
  
3. In den letzten zwei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.SplinePointKeyFrame> um die Ellipse zurück an ihre Anfangsposition zu verschieben. Spline-Keyframes wie <xref:System.Windows.Media.Animation.SplinePointKeyFrame> das Erstellen eines Variablen Übergangs zwischen Werten gemäß den Werten der- <xref:System.Windows.Media.Animation.SplinePointKeyFrame.KeySpline%2A> Eigenschaft. In diesem Beispiel beginnt die Animation zunächst langsam und beschleunigt dann exponentiell im letzten Bereich des Zeitabschnitts.  
  
 [!code-csharp[keyframes_snip#PointAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/PointAnimationUsingKeyFramesExample.cs#pointanimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#PointAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/pointanimationusingkeyframesexample.vb#pointanimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#PointAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/PointAnimationUsingKeyFramesExample.xaml#pointanimationusingkeyframeswholepage)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).  
  
 Aus Gründen der Konsistenz mit anderen Animations Beispielen wird in den Code Versionen dieses Beispiels ein-Objekt verwendet, <xref:System.Windows.Media.Animation.Storyboard> um das anzuwenden <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames> . Beim Anwenden einer einzelnen Animation im Code ist es jedoch einfacher, die-Methode zu verwenden, <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> anstatt eine zu verwenden <xref:System.Windows.Media.Animation.Storyboard> . Ein Beispiel finden Sie unter [Animieren einer Eigenschaft ohne Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames>
- <xref:System.Windows.Media.EllipseGeometry.Center%2A?displayProperty=nameWithType>
- <xref:System.Windows.Media.EllipseGeometry>
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Themen zur Vorgehensweise mit Keyframes](key-frame-animation-how-to-topics.md)
