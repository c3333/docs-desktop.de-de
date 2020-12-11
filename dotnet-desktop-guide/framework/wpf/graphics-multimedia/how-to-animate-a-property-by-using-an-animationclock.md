---
title: 'Gewusst wie: Animieren einer Eigenschaft mit AnimationClock'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], properties [WPF], with AnimationClocks
- AnimationClocks [WPF]
ms.assetid: e6542021-714c-4675-9567-04f1c7380834
ms.openlocfilehash: 13d91e8589c40d84ba374ffc613388e24407796a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974931"
---
# <a name="how-to-animate-a-property-by-using-an-animationclock"></a>Gewusst wie: Animieren einer Eigenschaft mit AnimationClock
In diesem Beispiel wird gezeigt, wie- <xref:System.Windows.Media.Animation.Clock> Objekte zum Animieren einer Eigenschaft verwendet werden.  
  
 Es gibt drei Möglichkeiten, eine Abhängigkeitseigenschaft zu animieren:  
  
- Erstellen <xref:System.Windows.Media.Animation.AnimationTimeline> Sie ein-Objekt, und ordnen Sie es der Eigenschaft mithilfe von zu <xref:System.Windows.Media.Animation.Storyboard> .  
  
- Verwenden Sie die-Methode des-Objekts <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> , um eine einzelne <xref:System.Windows.Media.Animation.AnimationTimeline> auf eine Ziel Eigenschaft anzuwenden.  
  
- Erstellen <xref:System.Windows.Media.Animation.AnimationClock> Sie ein aus einem <xref:System.Windows.Media.Animation.AnimationTimeline> , und wenden Sie es auf eine Eigenschaft an.  
  
 <xref:System.Windows.Media.Animation.Storyboard> mithilfe von Objekten und der- <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> Methode können Sie Eigenschaften animieren, ohne Uhren direkt zu erstellen und zu verteilen (Beispiele finden Sie unter [Animieren einer Eigenschaft mithilfe eines Storyboards](how-to-animate-a-property-by-using-a-storyboard.md) und [Animieren einer Eigenschaft ohne Storyboard](how-to-animate-a-property-without-using-a-storyboard.md)); Uhren werden automatisch erstellt und verteilt.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie ein erstellt <xref:System.Windows.Media.Animation.AnimationClock> und auf zwei ähnliche Eigenschaften angewendet wird.  
  
 [!code-csharp[timingbehaviors_procedural_snip#GraphicsMMCreateAnimationClockWholeClass](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp/AnimationClockExample.cs#graphicsmmcreateanimationclockwholeclass)]
 [!code-vb[timingbehaviors_procedural_snip#GraphicsMMCreateAnimationClockWholeClass](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic/animationclockexample.vb#graphicsmmcreateanimationclockwholeclass)]  
  
 Ein Beispiel, das zeigt, wie ein nach dem Start interaktiv gesteuert <xref:System.Windows.Media.Animation.Clock> wird, finden Sie unter [interaktiv Steuern einer Uhr](how-to-interactively-control-a-clock.md).  
  
## <a name="see-also"></a>Siehe auch

- [Animieren einer Eigenschaft unter Verwendung eines Storyboards](how-to-animate-a-property-by-using-a-storyboard.md)
- [Animieren einer Eigenschaft ohne Storyboard](how-to-animate-a-property-without-using-a-storyboard.md)
- [Übersicht über die Verfahren zur Animation von Eigenschaften](property-animation-techniques-overview.md)
