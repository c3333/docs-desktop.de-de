---
title: 'Gewusst wie: Animieren der Breite eines Rahmens mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], border thickness with key frames
- key frames [WPF], animating border thickness with
- border thickness [WPF], animating with key frames
ms.assetid: 3a9cb463-0a63-407d-aae7-3fbb1a559947
ms.openlocfilehash: 884b62e88c347449ae39caa9c028d09db39b9f4b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975326"
---
# <a name="how-to-animate-the-thickness-of-a-border-by-using-key-frames"></a>Gewusst wie: Animieren der Breite eines Rahmens mithilfe von Keyframes
Dieses Beispiel zeigt, wie Sie die- <xref:System.Windows.Controls.Control.BorderThickness%2A> Eigenschaft eines animieren <xref:System.Windows.Controls.Border> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.ThicknessAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Controls.Control.BorderThickness%2A> Eigenschaft eines zu animieren <xref:System.Windows.Controls.Border> . In dieser Animation werden drei Keyframes folgendermaßen verwendet:  
  
1. In der ersten halben Sekunde wird von eine Instanz der- <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> Klasse verwendet, um die Stärke des Rahmens allmählich zu erhöhen. Im Beispiel wird verwendet <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> , um eine glatte lineare Zunahme zwischen Werten zu erstellen.  
  
2. Am Ende der nächsten halben Sekunde wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> um die Stärke des Rahmens plötzlich zu erhöhen. Diskrete Keyframes wie diejenigen, die von abgeleitet <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> werden, erzeugen plötzliche Sprünge zwischen Werten, d. h., die Animation der Animation ist ruckartig.  
  
3. In den letzten zwei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> um die Stärke des Rahmens zu verringern. Spline-Keyframes wie die, die von abgeleitet werden <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> , erstellen einen variablen Übergang zwischen Werten gemäß den Werten der- <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame.KeySpline%2A> Eigenschaft. In diesem Keyframe ist die Animation zunächst langsam und beschleunigt dann exponentiell im letzten Bereich des Zeitabschnitts.  
  
 [!code-xaml[keyframes_snip#ThicknessAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ThicknessAnimationUsingKeyFramesExample.xaml#thicknessanimationusingkeyframeswholepage)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame>
- <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame>
- <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame>
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Themen zur Vorgehensweise mit Keyframes](key-frame-animation-how-to-topics.md)
- [Animieren eines BorderThickness-Werts](../controls/how-to-animate-a-borderthickness-value.md)
