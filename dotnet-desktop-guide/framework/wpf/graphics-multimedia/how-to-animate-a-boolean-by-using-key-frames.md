---
title: 'Gewusst wie: Animieren eines booleschen Werts mithilfe von Keyframes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Booleans [WPF], animating with key frames
- animation [WPF], Booleans with key frames
- key frames [WPF], animating Booleans with
ms.assetid: 4b0fac96-6231-4fcf-9775-4dd673ddc785
ms.openlocfilehash: 35704996dcf21fe463169dc13572941bcd8fbad1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977316"
---
# <a name="how-to-animate-a-boolean-by-using-key-frames"></a>Gewusst wie: Animieren eines booleschen Werts mithilfe von Keyframes
Dieses Beispiel zeigt, wie Sie den booleschen Eigenschafts Wert eines <xref:System.Windows.Controls.Button> Steuer Elements mithilfe von Keyframes animieren.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.BooleanAnimationUsingKeyFrames> Klasse verwendet, um die-Eigenschaft eines-Steuer Elements zu animieren <xref:System.Windows.UIElement.IsEnabled%2A> <xref:System.Windows.Controls.Button> . Alle Keyframes in diesem Beispiel verwenden eine Instanz der- <xref:System.Windows.Media.Animation.DiscreteBooleanKeyFrame> Klasse. Diskrete Keyframes wie z <xref:System.Windows.Media.Animation.DiscreteBooleanKeyFrame> . b. plötzliche Sprünge zwischen Werten, d. h. die Bewegung der Animation ist ruckartig.  
  
 [!code-csharp[keyframes_snip#BooleanAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/BooleanAnimationUsingKeyFramesExample.cs#booleananimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#BooleanAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/booleananimationusingkeyframesexample.vb#booleananimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#BooleanAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/BooleanAnimationUsingKeyFramesExample.xaml#booleananimationusingkeyframeswholepage)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.BooleanAnimationUsingKeyFrames>
- <xref:System.Windows.UIElement.IsEnabled%2A>
- <xref:System.Windows.Controls.Button>
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Themen zur Vorgehensweise mit Keyframes](key-frame-animation-how-to-topics.md)
