---
title: 'Gewusst wie: Animieren von Größenänderungen mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- key frames [WPF], animating size changes with
- animation [WPF], size changes with key frames
- size changes [WPF], animating with key frames
ms.assetid: 86bd2950-d4c9-4ec4-aa8d-7dc3ccadded4
ms.openlocfilehash: 42cecfc9df4304be4033ea39edc0517016de4a92
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975413"
---
# <a name="how-to-animate-size-changes-by-using-key-frames"></a>Gewusst wie: Animieren von Größenänderungen mithilfe von Keyframes
In diesem Beispiel wird das Animieren von Größenänderungen mithilfe von Keyframes veranschaulicht.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.SizeAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Media.ArcSegment.Size%2A> Eigenschaft eines zu animieren <xref:System.Windows.Media.ArcSegment> . In dieser Animation werden drei Keyframes folgendermaßen verwendet:  
  
1. In der ersten halben Sekunde der Animation wird von eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.LinearSizeKeyFrame> um die Größe des Bogens allmählich zu vergrößern. Lineare Keyframes, wie z <xref:System.Windows.Media.Animation.LinearSizeKeyFrame> . b. eine glatte lineare Umstellung zwischen Werten.  
  
2. Am Ende der nächsten halben Sekunde wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame> um die Größe des Bogens plötzlich zu vergrößern. Diskrete Keyframes wie z. b. <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame> die Erstellung plötzlicher Sprünge zwischen Werten, d. h. die Größenänderungen treten plötzlich auf und sind nicht fein.  
  
3. In den letzten zwei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.SplineSizeKeyFrame> um die Größe des Bogens zu vergrößern. Spline-Keyframes wie <xref:System.Windows.Media.Animation.SplineSizeKeyFrame> das Erstellen eines Variablen Übergangs zwischen Werten gemäß den Werten der- <xref:System.Windows.Media.Animation.SplineSizeKeyFrame.KeySpline%2A> Eigenschaft. In diesem Beispiel wächst die Größe des Bogens zunächst nur langsam und steigt dann exponentiell zum Ende des Zeitabschnitts.  
  
 [!code-xaml[keyframes_snip#SizeAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/SizeAnimationUsingKeyFramesExample.xaml#sizeanimationusingkeyframeswholepage)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.SizeAnimationUsingKeyFrames>
- <xref:System.Windows.Media.ArcSegment.Size%2A>
- <xref:System.Windows.Media.ArcSegment>
- <xref:System.Windows.Media.Animation.LinearSizeKeyFrame>
- <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame>
- <xref:System.Windows.Media.Animation.SplineSizeKeyFrame>
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Themen zur Vorgehensweise mit Keyframes](key-frame-animation-how-to-topics.md)
