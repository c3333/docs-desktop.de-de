---
title: 'Gewusst wie: Festlegen einer Eigenschaft nach einer Storyboard-Animation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], changing property values after
ms.assetid: 79466556-4dbf-40bd-9c1e-a77613b07077
ms.openlocfilehash: 593d3fcefe3bb81518d0886afde82f9a172874ba
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976870"
---
# <a name="how-to-set-a-property-after-animating-it-with-a-storyboard"></a>Gewusst wie: Festlegen einer Eigenschaft nach einer Storyboard-Animation
In einigen Fällen kann es vorkommen, dass Sie den Wert einer Eigenschaft nach dem Animieren nicht ändern können.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel <xref:System.Windows.Media.Animation.Storyboard> wird ein verwendet, um die Farbe eines zu animieren <xref:System.Windows.Media.SolidColorBrush> . Das Storyboard wird ausgelöst, wenn auf die Schaltfläche geklickt wird. Das <xref:System.Windows.Media.Animation.Timeline.Completed> Ereignis wird behandelt, damit das Programm benachrichtigt wird, wenn <xref:System.Windows.Media.Animation.ColorAnimation> abgeschlossen wird.  
  
 [!code-xaml[timingbehaviors_snip#GraphicsMMButton1Declaration](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml#graphicsmmbutton1declaration)]  
  
## <a name="example"></a>Beispiel  
 Nachdem der <xref:System.Windows.Media.Animation.ColorAnimation> abgeschlossen ist, versucht das Programm, die Farbe des Pinsels in blau zu ändern.  
  
 [!code-csharp[timingbehaviors_snip#GraphicsMMButton1Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml.cs#graphicsmmbutton1handler)]
 [!code-vb[timingbehaviors_snip#GraphicsMMButton1Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_snip/visualbasic/animatethensetpropertyexample.xaml.vb#graphicsmmbutton1handler)]  
  
 Der vorherige Code scheint nichts zu tun: der Pinsel bleibt Gelb, d. h. der Wert, der von der bereitgestellt wird, die <xref:System.Windows.Media.Animation.ColorAnimation> den Pinsel animiert hat. Der zugrunde liegende Eigenschafts Wert (der Basiswert) wird tatsächlich in blau geändert. Der effektive oder aktuelle Wert bleibt jedoch gelb, da der <xref:System.Windows.Media.Animation.ColorAnimation> den Basiswert weiterhin überschreibt. Wenn der Basiswert wieder der effektive Wert werden soll, müssen Sie die Animation daran hindern, die Eigenschaft zu beeinflussen. Es gibt drei Möglichkeiten, um dies mit Storyboard-Animationen zu erreichen:  
  
- Legen Sie die-Eigenschaft der Animation auf fest. <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A><xref:System.Windows.Media.Animation.FillBehavior.Stop>  
  
- Entfernen Sie das gesamte Storyboard.  
  
- Entfernen Sie die Animation aus der einzelnen Eigenschaft.  
  
## <a name="set-the-animations-fillbehavior-property-to-stop"></a>Festlegen der FillBehavior-Eigenschaft der Animation auf "wird beendet"  
 Wenn <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> Sie auf festlegen <xref:System.Windows.Media.Animation.FillBehavior.Stop> , teilen Sie der Animation mit, dass die Ziel Eigenschaft nicht mehr beeinträchtigt wird, nachdem das Ende des aktiven Zeitraums erreicht wurde.  
  
 [!code-xaml[timingbehaviors_snip#GraphicsMMButton2Declaration](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml#graphicsmmbutton2declaration)]  
  
 [!code-csharp[timingbehaviors_snip#GraphicsMMButton2Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml.cs#graphicsmmbutton2handler)]
 [!code-vb[timingbehaviors_snip#GraphicsMMButton2Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_snip/visualbasic/animatethensetpropertyexample.xaml.vb#graphicsmmbutton2handler)]  
  
## <a name="remove-the-entire-storyboard"></a>Entfernen des gesamten Storyboards  
 Wenn Sie einen- <xref:System.Windows.Media.Animation.RemoveStoryboard> oder die- <xref:System.Windows.Media.Animation.Storyboard.Remove%2A?displayProperty=nameWithType> Methode verwenden, teilen Sie den Storyboard-Animationen mit, dass Ihre Zieleigenschaften nicht mehr beeinträchtigt werden. Der Unterschied zwischen diesem Ansatz und dem Festlegen der- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> Eigenschaft besteht darin, dass Sie das Storyboard jederzeit entfernen können, während die- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> Eigenschaft nur dann wirksam wird, wenn die Animation das Ende des aktiven Zeitraums erreicht.  
  
 [!code-xaml[timingbehaviors_snip#GraphicsMMButton3Declaration](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml#graphicsmmbutton3declaration)]  
  
 [!code-csharp[timingbehaviors_snip#GraphicsMMButton3Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml.cs#graphicsmmbutton3handler)]
 [!code-vb[timingbehaviors_snip#GraphicsMMButton3Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_snip/visualbasic/animatethensetpropertyexample.xaml.vb#graphicsmmbutton3handler)]  
  
## <a name="remove-an-animation-from-an-individual-property"></a>Entfernen einer Animation aus einer einzelnen Eigenschaft  
 Eine andere Möglichkeit, eine Animation daran zu hindern, eine Eigenschaft zu beeinflussen, ist die Verwendung der- <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%28System.Windows.DependencyProperty%2CSystem.Windows.Media.Animation.AnimationTimeline%29> Methode des zu animierenden Objekts. Geben Sie die zu animierende Eigenschaft als ersten Parameter und `null` als zweiten an.  
  
 [!code-xaml[timingbehaviors_snip#GraphicsMMButton4Declaration](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml#graphicsmmbutton4declaration)]  
  
 [!code-csharp[timingbehaviors_snip#GraphicsMMButton4Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AnimateThenSetPropertyExample.xaml.cs#graphicsmmbutton4handler)]
 [!code-vb[timingbehaviors_snip#GraphicsMMButton4Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_snip/visualbasic/animatethensetpropertyexample.xaml.vb#graphicsmmbutton4handler)]  
  
 Diese Technik funktioniert auch für nicht-Storyboard-Animationen.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A>
- <xref:System.Windows.Media.Animation.Storyboard.Remove%2A?displayProperty=nameWithType>
- <xref:System.Windows.Media.Animation.RemoveStoryboard>
- [Übersicht über Animationen](animation-overview.md)
- [Übersicht über die Verfahren zur Animation von Eigenschaften](property-animation-techniques-overview.md)
