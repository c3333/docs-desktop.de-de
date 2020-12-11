---
title: 'Gewusst wie: Animieren von Color mithilfe von Keyframes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [WPF], animating with key frames
- animation [WPF], colors with key frames
- key frames [WPF], animating colors with
ms.assetid: ab04ffa6-4de9-4d5b-a3b4-4e35d5b2ef35
ms.openlocfilehash: 8a444706f7541b52722ab8257a88e76c3e1b0938
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977641"
---
# <a name="how-to-animate-color-by-using-key-frames"></a>Gewusst wie: Animieren von Color mithilfe von Keyframes
In diesem Beispiel wird gezeigt, wie die <xref:System.Windows.Media.SolidColorBrush.Color%2A> eines <xref:System.Windows.Media.SolidColorBrush> mithilfe von Keyframes animiert wird.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.ColorAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Media.SolidColorBrush.Color%2A> Eigenschaft eines zu animieren <xref:System.Windows.Media.SolidColorBrush> . In dieser Animation werden drei Keyframes folgendermaßen verwendet:  
  
1. In den ersten zwei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.LinearColorKeyFrame> um die Farbe allmählich von Grün in rot zu ändern. Lineare Keyframes, wie z <xref:System.Windows.Media.Animation.LinearColorKeyFrame> . b. eine glatte lineare Umstellung zwischen Werten.  
  
2. Am Ende der nächsten halben Sekunde wird von eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.DiscreteColorKeyFrame> um die Farbe von rot in gelb zu ändern. Diskrete Keyframes wie <xref:System.Windows.Media.Animation.DiscreteColorKeyFrame> das Erstellen von plötzlichen Änderungen zwischen Werten, d. h. die Farbänderung in diesem Teil der Animation tritt schnell auf und ist nicht fein.  
  
3. In den letzten zwei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.SplineColorKeyFrame> um die Farbe erneut zu ändern – diesmal von gelb zurück zu grün. Spline-Keyframes wie <xref:System.Windows.Media.Animation.SplineColorKeyFrame> das Erstellen eines Variablen Übergangs zwischen Werten gemäß den Werten der- <xref:System.Windows.Media.Animation.SplineColorKeyFrame.KeySpline%2A> Eigenschaft. In diesem Beispiel beginnt die Farbveränderung zunächst langsam und beschleunigt dann exponentiell im letzten Bereich des Zeitabschnitts.  
  
 [!code-csharp[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/ColorAnimationUsingKeyFramesExample.cs#coloranimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/coloranimationusingkeyframesexample.vb#coloranimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ColorAnimationUsingKeyFramesExample.xaml#coloranimationusingkeyframeswholepage)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.SolidColorBrush.Color%2A>
- <xref:System.Windows.Media.SolidColorBrush>
- <xref:System.Windows.Media.Animation.ColorAnimationUsingKeyFrames>
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Themen zur Vorgehensweise mit Keyframes](key-frame-animation-how-to-topics.md)
