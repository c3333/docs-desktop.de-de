---
title: 'Gewusst wie: Sammeln von Animationswerten während Wiederholungszyklen'
ms.date: 03/30/2017
helpviewer_keywords:
- accumulating animation values across repeating cycles [WPF]
- animation [WPF], accumulating values across repeating cycles
ms.assetid: 548df369-c7cc-4dab-b569-08b95ced2e7e
ms.openlocfilehash: bccdc9b7bf2d5a0ea476e39e8d54107854db7ae3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977677"
---
# <a name="how-to-accumulate-animation-values-during-repeat-cycles"></a>Gewusst wie: Sammeln von Animationswerten während Wiederholungszyklen
In diesem Beispiel wird gezeigt, wie die-Eigenschaft verwendet wird <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> , um Animations Werte in wiederkehrenden Zyklen zu sammeln.  
  
## <a name="example"></a>Beispiel  
 Verwenden Sie die- <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> Eigenschaft, um Basiswerte einer Animation über sich wiederholende Zyklen hinweg zu sammeln. Wenn Sie z. b. eine Animation so festlegen, dass Sie 9-Mal wiederholt <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> wird (= "9X"), und Sie die-Eigenschaft auf animieren zwischen 10 und 15 festlegen (von = 10 bis = 15), wird die-Eigenschaft während des ersten Durchlaufs zwischen 10 und 15 animiert. Daher wird für jeden Animations Durchlauf der Wert "End Animation" aus dem vorherigen Animations Cycle als Basiswert verwendet.  
  
 Sie können die `IsCumulative` -Eigenschaft mit den meisten grundlegenden Animationen und den meisten Keyframe-Animationen verwenden. Weitere Informationen finden Sie unter Übersicht über [Animationen](animation-overview.md) und [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md).  
  
 Das folgende Beispiel zeigt dieses Verhalten, indem Sie die Breite von vier Rechtecke animieren. Beispiel:  
  
- Animiert das erste Rechteck mit <xref:System.Windows.Media.Animation.DoubleAnimation> und legt die- <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> Eigenschaft auf fest `true` .  
  
- Animiert das zweite Rechteck mit <xref:System.Windows.Media.Animation.DoubleAnimation> und legt die- <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> Eigenschaft auf den Standardwert von fest `false` .  
  
- Animiert das dritte Rechteck mit <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> und legt die- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsCumulative%2A> Eigenschaft auf fest `true` .  
  
- Animiert das letzte Rechteck mit <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> und legt die- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsCumulative%2A> Eigenschaft auf fest `false` .  
  
 [!code-xaml[timingbehaviors_snip#IsCumulativeWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/IsCumulativeExample.xaml#iscumulativewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Hinzufügen eines Animationsausgabewerts zu einem Animationsstartwert](how-to-add-an-animation-output-value-to-an-animation-starting-value.md)
- [Wiederholen einer Animation](how-to-repeat-an-animation.md)
- [Übersicht über Animationen](animation-overview.md)
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Artikel zu Vorgehensweisen](animation-and-timing-how-to-topics.md)
