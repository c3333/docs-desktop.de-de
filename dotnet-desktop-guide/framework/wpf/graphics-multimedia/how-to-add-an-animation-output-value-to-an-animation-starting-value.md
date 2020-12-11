---
title: 'Gewusst wie: Hinzufügen eines Animationsausgabewerts zu einem Animationsstartwert'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF]
ms.assetid: b89a82be-b03d-481e-a8d3-cc513d09ca00
ms.openlocfilehash: 945675d03a280e2394fdb0eab27c0978dc7cc320
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975333"
---
# <a name="how-to-add-an-animation-output-value-to-an-animation-starting-value"></a>Gewusst wie: Hinzufügen eines Animationsausgabewerts zu einem Animationsstartwert
In diesem Beispiel wird gezeigt, wie Sie einen Animations Ausgabewert zu einem Animations Start Wert hinzufügen.  
  
## <a name="example"></a>Beispiel  
 Die- <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A> Eigenschaft gibt an, ob der Ausgabewert einer Animation dem Startwert (Basiswert) einer animierten Eigenschaft hinzugefügt werden soll. Sie können die <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A> -Eigenschaft mit den meisten grundlegenden Animationen und den meisten Keyframe-Animationen verwenden. Weitere Informationen finden Sie unter Übersicht über [Animationen](animation-overview.md) und [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md).  
  
 Das folgende Beispiel zeigt die Auswirkung der Verwendung der <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A?displayProperty=nameWithType> -Eigenschaft mit <xref:System.Windows.Media.Animation.DoubleAnimation> und die Verwendung der- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsAdditive%2A?displayProperty=nameWithType> Eigenschaft mit <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> .  
  
 [!code-xaml[timingbehaviors_snip#IsAdditiveWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/IsAdditiveExample.xaml#isadditivewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Sammeln von Animationen während Wiederholungszyklen](how-to-accumulate-animation-values-during-repeat-cycles.md)
- [Übersicht über Animationen](animation-overview.md)
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Gewusst-wie-Themen zu Animation und Zeitsteuerung](animation-and-timing-how-to-topics.md)
