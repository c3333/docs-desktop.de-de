---
title: 'Gewusst wie: Animieren einer Zeichenfolge mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], strings with key frames
- strings [WPF], animating with key frames
- key frames [WPF], animating strings with
ms.assetid: c62bc9fd-c09a-4227-bce0-0a1ab82049dd
ms.openlocfilehash: c954806ca901bbfc3ab6d4bbcc237cd0e404f154
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977021"
---
# <a name="how-to-animate-a-string-by-using-key-frames"></a>Gewusst wie: Animieren einer Zeichenfolge mithilfe von Keyframes
Dieses Beispiel zeigt, wie eine Zeichenfolge, die in diesem Beispiel die- <xref:System.Windows.Controls.ContentControl.Content%2A> Eigenschaft eines- <xref:System.Windows.Controls.Button> Steuer Elements ist, mithilfe von Keyframes animiert wird.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Controls.ContentControl.Content%2A> Eigenschaft eines zu animieren <xref:System.Windows.Controls.Button> .  
  
 Alle Keyframes in diesem Beispiel verwenden eine Instanz der- <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> Klasse, da eine Zeichen folgen Animation, die mit Keyframes erstellt wird, nur diskrete Keyframes verwenden kann. Diskrete Keyframes wie z. b. <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> plötzliche Sprünge zwischen Werten, d. h. Änderungen an der Animation werden schnell ausgeführt und sind nicht fein.  
  
 [!code-xaml[keyframes_snip#StringAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/StringAnimationUsingKeyFramesExample.xaml#stringanimationusingkeyframeswholepage)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames>
- <xref:System.Windows.Controls.ContentControl.Content%2A>
- <xref:System.Windows.Controls.Button>
- <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame>
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Themen zur Vorgehensweise mit Keyframes](key-frame-animation-how-to-topics.md)
