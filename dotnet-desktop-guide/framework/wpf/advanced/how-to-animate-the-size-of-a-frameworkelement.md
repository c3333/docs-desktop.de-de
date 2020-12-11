---
title: 'Gewusst wie: Animieren der Größe von FrameworkElement'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], FrameworkElement size
- FrameworkElement [WPF], animating size of
ms.assetid: d4cd5a13-c20d-4a6f-a2ba-14f2c9ce4cef
ms.openlocfilehash: d1995deec5ab2c9bf405911af43b4d242d599119
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976391"
---
# <a name="how-to-animate-the-size-of-a-frameworkelement"></a>Gewusst wie: Animieren der Größe von FrameworkElement
Um die Größe eines zu animieren <xref:System.Windows.FrameworkElement> , können Sie entweder seine-Eigenschaft und die-Eigenschaft animieren <xref:System.Windows.FrameworkElement.Width%2A> <xref:System.Windows.FrameworkElement.Height%2A> oder einen animierten verwenden <xref:System.Windows.Media.ScaleTransform> .  
  
 Im folgenden Beispiel wird die Größe von zwei Schaltflächen mit diesen beiden Ansätzen animiert. Die Größe einer Schaltfläche wird geändert, indem die zugehörige <xref:System.Windows.FrameworkElement.Width%2A> -Eigenschaft animiert wird und eine andere Größe geändert wird <xref:System.Windows.Media.ScaleTransform> <xref:System.Windows.UIElement.RenderTransform%2A> . Jede Schaltfläche enthält Text. Anfänglich wird der Text in beiden Schaltflächen gleich angezeigt, aber wenn die Größe der Schaltflächen geändert wird, wird der Text in der zweiten Schaltfläche verzerrt.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[transformanimations_snip#1](~/samples/snippets/xaml/VS_Snippets_Wpf/transformanimations_snip/XAML/AnimatingSizeExample.xaml#1)]  
  
 Wenn Sie ein Element transformieren, werden das gesamte Element und sein Inhalt transformiert. Wenn Sie die Größe eines Elements direkt ändern, wie im Fall der ersten Schaltfläche, wird der Inhalt des Elements nicht geändert, es sei denn, die Größe und Position hängen von der Größe des übergeordneten Elements ab.  
  
 Die Animation der Größe eines Elements durch Anwenden einer animierten Transformation auf seine <xref:System.Windows.UIElement.RenderTransform%2A> -Eigenschaft sorgt für eine bessere Leistung als bei der Animation seiner <xref:System.Windows.FrameworkElement.Width%2A> und <xref:System.Windows.FrameworkElement.Height%2A> direkt, da die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft keinen Layoutdurchlauf auslöst.  
  
 Weitere Informationen zum Animieren von Eigenschaften finden Sie unter [Übersicht über Animationen](../graphics-multimedia/animation-overview.md). Weitere Informationen zu Transformationen finden Sie in der [Übersicht über Transformationen](../graphics-multimedia/transforms-overview.md).
