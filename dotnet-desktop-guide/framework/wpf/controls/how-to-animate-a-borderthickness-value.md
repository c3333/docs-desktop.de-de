---
title: 'Gewusst wie: Animieren eines BorderThickness-Werts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- border thickness [WPF], animating changes to
- animation [WPF], changes to border thickness
ms.assetid: fd021978-f74b-4e7b-a7f7-3987dcad9e0f
ms.openlocfilehash: 4533ce6f2a1fe7243267ee8d638e2ad0a4f9cf3a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978095"
---
# <a name="how-to-animate-a-borderthickness-value"></a>Gewusst wie: Animieren eines BorderThickness-Werts
Dieses Beispiel zeigt, wie Sie mithilfe der-Klasse Änderungen an der Stärke eines Rahmens animieren <xref:System.Windows.Media.Animation.ThicknessAnimation> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die Stärke eines Rahmens mithilfe von animiert <xref:System.Windows.Media.Animation.ThicknessAnimation> . Im Beispiel wird die- <xref:System.Windows.Controls.Border.BorderThickness%2A> Eigenschaft von verwendet <xref:System.Windows.Controls.Border> .  
  
 [!code-csharp[BasicAnimations_snip#ThicknessAnimationWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/ThicknessAnimationExample.cs#thicknessanimationwholepage)]
 [!code-vb[BasicAnimations_snip#ThicknessAnimationWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/ThicknessAnimationExample.vb#thicknessanimationwholepage)]  
  
 Das komplette Beispiel finden Sie unter [Animation Example Gallery](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/AnimationExamples).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.ThicknessAnimation>
- <xref:System.Windows.Controls.Border.BorderThickness%2A>
- <xref:System.Windows.Controls.Border>
- [Übersicht über Animationen](../graphics-multimedia/animation-overview.md)
- [Gewusst-wie-Themen zu Animation und Zeitsteuerung](../graphics-multimedia/animation-and-timing-how-to-topics.md)
- [Animieren der Breite eines Rahmens mithilfe von Keyframes](../graphics-multimedia/how-to-animate-the-thickness-of-a-border-by-using-key-frames.md)
