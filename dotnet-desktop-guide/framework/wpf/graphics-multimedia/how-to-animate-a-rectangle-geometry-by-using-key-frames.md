---
title: 'Gewusst wie: Animieren einer Rechteckgeometrie mithilfe von Keyframes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- key frames [WPF], animating RectangleGeometry objects with
- RectangleGeometry objects [WPF], animating with key frames
- animation [WPF], RectangleGeometry objects with key frames
ms.assetid: a8b45ceb-0e32-4ba1-928f-df6d30db17c6
ms.openlocfilehash: bcc9e7f198b8a20ffe13daf6508fb8a735937652
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974928"
---
# <a name="how-to-animate-a-rectangle-geometry-by-using-key-frames"></a>Gewusst wie: Animieren einer Rechteckgeometrie mithilfe von Keyframes
In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.RectangleGeometry.Rect%2A> Eigenschaft eines <xref:System.Windows.Media.RectangleGeometry> mithilfe von Keyframes animiert wird.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.RectAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Media.RectangleGeometry.Rect%2A> Eigenschaft eines zu animieren <xref:System.Windows.Media.RectangleGeometry> . In dieser Animation werden drei Keyframes folgendermaßen verwendet:  
  
1. In den ersten zwei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.LinearRectKeyFrame> um eine schrittweise Änderung an Position, Breite und Höhe eines Rechtecks zu animieren. Lineare Keyframes, wie z <xref:System.Windows.Media.Animation.LinearRectKeyFrame> . b. eine glatte lineare Umstellung zwischen Werten.  
  
2. Am Ende der nächsten halben Sekunde wird von eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> um die Höhe des Rechtecks plötzlich zu verringern. Diskrete Keyframes, wie z. b. <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> plötzliche Änderungen zwischen Werten, d. h., die Abnahme der Höhe erfolgt schnell und ist nicht fein.  
  
3. In den letzten zwei Sekunden wird eine Instanz der <xref:System.Windows.Media.Animation.SplineRectKeyFrame> -Klasse verwendet, um das Rechteck wieder in seine ursprüngliche Größe und Position zu ändern. Spline-Keyframes wie <xref:System.Windows.Media.Animation.SplineRectKeyFrame> das Erstellen eines Variablen Übergangs zwischen Werten gemäß den Werten der- <xref:System.Windows.Media.Animation.SplineRectKeyFrame.KeySpline%2A> Eigenschaft. In diesem Beispiel beginnt die Veränderung zunächst langsam und beschleunigt dann exponentiell im letzten Bereich des Zeitabschnitts.  
  
 [!code-csharp[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/RectAnimationUsingKeyFramesExample.cs#rectanimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/rectanimationusingkeyframesexample.vb#rectanimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/RectAnimationUsingKeyFramesExample.xaml#rectanimationusingkeyframeswholepage)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.RectangleGeometry>
- <xref:System.Windows.Media.RectangleGeometry.Rect%2A>
- <xref:System.Windows.Media.Animation.RectAnimationUsingKeyFrames>
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Themen zur Vorgehensweise mit Keyframes](key-frame-animation-how-to-topics.md)
