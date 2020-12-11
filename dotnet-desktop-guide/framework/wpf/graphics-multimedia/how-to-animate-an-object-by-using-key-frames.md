---
title: 'Gewusst wie: Animieren eines Objekts mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], objects with key frames
- key frames [WPF], animating objects with
ms.assetid: b1f15ba9-cac7-4cea-8699-5c6b55c05c5e
ms.openlocfilehash: 0bc33b189fd856dbe8106c1db35bc18e27ea131e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977274"
---
# <a name="how-to-animate-an-object-by-using-key-frames"></a>Gewusst wie: Animieren eines Objekts mithilfe von Keyframes
In diesem Beispiel wird gezeigt, wie ein Objekt, das in diesem Beispiel die- <xref:System.Windows.Controls.Page.Background%2A> Eigenschaft eines-Steuer Elements ist <xref:System.Windows.Controls.Page> , mithilfe von Keyframes animiert wird.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames> Klasse verwendet, um Farbänderungen für die-Eigenschaft eines-Steuer Elements zu animieren <xref:System.Windows.Controls.Page.Background%2A> <xref:System.Windows.Controls.Page> . Die Beispiel Animation ändert sich in regelmäßigen Abständen in einen anderen Hintergrund Pinsel. Diese Animation verwendet die- <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> Klasse, um drei verschiedene Keyframes zu erstellen. Die Animation verwendet Keyframes wie folgt:  
  
1. Am Ende der ersten Sekunde animiert eine Instanz der- <xref:System.Windows.Media.LinearGradientBrush> Klasse. In diesem Abschnitt des Beispiels wird ein linearer Farbverlauf auf die Hintergrundfarbe angewendet, sodass die Farbe von Gelb in Orange in rot übergeht.  
  
2. Am Ende der nächsten Sekunde animiert eine Instanz der- <xref:System.Windows.Media.RadialGradientBrush> Klasse. In diesem Abschnitt des Beispiels wird ein Radialer Farbverlauf auf die Hintergrundfarbe angewendet, sodass die Farbe von weiß zu blau in schwarz übergeht.  
  
3. Am Ende der dritten Sekunde animiert eine Instanz der- <xref:System.Windows.Media.DrawingBrush> Klasse. In diesem Abschnitt des Beispiels wird ein checkboard-Muster auf den Hintergrund angewendet.  
  
4. Die Animation beginnt wieder und wird unbegrenzt wiederholt.  
  
> [!NOTE]
> <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> ist der einzige schlüsselframe, den Sie mit der-Klasse verwenden können <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames> . Keyframes wie z <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> . b. eine plötzliche Änderung von Werten, d. h. die Farbänderungen in diesem Beispiel treten plötzlich auf.  
  
 [!code-xaml[keyframes_snip#ObjectAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ObjectAnimationUsingKeyFramesExample.xaml#objectanimationusingkeyframeswholepage)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames>
- <xref:System.Windows.Controls.Page.Background%2A>
- <xref:System.Windows.Controls.Page>
- <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame>
- <xref:System.Windows.Media.LinearGradientBrush>
- <xref:System.Windows.Media.RadialGradientBrush>
- <xref:System.Windows.Media.DrawingBrush>
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Themen zur Vorgehensweise mit Keyframes](key-frame-animation-how-to-topics.md)
