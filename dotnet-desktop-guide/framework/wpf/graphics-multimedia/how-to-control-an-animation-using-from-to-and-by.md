---
title: 'Gewusst wie: Steuern von Animationen mit From, To und By'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], From/to/by
- basic animation [WPF]
- animation [WPF], basic animation
- From/to/by animation
ms.assetid: 59afba57-6fc1-44c8-987e-8a5f4142adad
ms.openlocfilehash: b06df97dc57c58a01f30be2d70bfeebf104521ad
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977220"
---
# <a name="how-to-control-an-animation-using-from-to-and-by"></a>Gewusst wie: Steuern von Animationen mit From, To und By
Eine "from/to/by"-oder "Basic Animation"-Animation erstellt einen Übergang zwischen zwei Zielwerten (Weitere Informationen finden Sie unter [Übersicht über Animationen](animation-overview.md) ). Um die Zielwerte einer grundlegenden Animation festzulegen, verwenden Sie die <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A> Eigenschaften, und <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> .  In der folgenden Tabelle wird zusammengefasst, wie die <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A> -,-und <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> -Eigenschaften zusammen oder separat verwendet werden können, um die Zielwerte einer Animation zu bestimmen.  
  
|Angegebene Eigenschaften|Resultierendes Verhalten|  
|--------------------------|------------------------|  
|<xref:System.Windows.Media.Animation.DoubleAnimation.From%2A>|Die Animation wechselt von dem Wert, der von der- <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> Eigenschaft angegeben wird, zum Basiswert der zu animierenden Eigenschaft oder zum Ausgabewert einer vorherigen Animation, je nachdem, wie die vorherige Animation konfiguriert wurde.|  
|<xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> und <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A>|Die Animation verläuft von dem Wert, der von der-Eigenschaft angegeben wird <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> , mit dem von der-Eigenschaft angegebenen Wert <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A> .|  
|<xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> und <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A>|Die Animation wechselt von dem Wert, der von der <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> -Eigenschaft angegeben wird, zu dem Wert, der durch die Summe der <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> Eigenschaften und angegeben wird <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> .|  
|<xref:System.Windows.Media.Animation.DoubleAnimation.To%2A>|Die Animation verläuft vom Basiswert der animierten Eigenschaft oder vom Ausgabewert einer vorherigen Animation bis zu dem Wert, der von der-Eigenschaft angegeben wird <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A> .|  
|<xref:System.Windows.Media.Animation.DoubleAnimation.By%2A>|Die Animation verläuft vom Basiswert der zu animierenden Eigenschaft oder vom Ausgabewert einer vorherigen Animation bis zur Summe dieses Werts und des Werts, der von der-Eigenschaft angegeben wird <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> .|  
  
> [!NOTE]
> Legen Sie nicht sowohl die <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A> -Eigenschaft als auch die- <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> Eigenschaft für die gleiche Animation fest.  
  
 Um andere Interpolationsmethoden zu verwenden oder eine Animation zwischen mehr als zwei Zielwerten auszuführen, verwenden Sie eine Keyframe-Animation. Weitere Informationen finden Sie unter [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md) .  
  
 Informationen zum Anwenden mehrerer Animationen auf eine einzelne Eigenschaft finden Sie unter [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md).  
  
 Das folgende Beispiel zeigt die unterschiedlichen Auswirkungen der Einstellung der <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A> <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> Eigenschaften, und <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> für Animationen.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[BasicAnimations_snippet#AnimationTargetValuesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snippet/CS/AnimationTargetValuesExample.xaml#animationtargetvalueswholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Animationen](animation-overview.md)
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Beispiel für From-, To- und By-Animationszielwerte](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/TargetValues)
