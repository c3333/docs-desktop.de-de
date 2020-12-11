---
title: 'Gewusst wie: Anwenden einer Transformation auf ein Element beim Auftreten eines Ereignisses'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], transformations as event responses
- properties [WPF], LayoutTransform
- transformations as event responses [WPF]
- properties [WPF], RenderTransform
- LayoutTransform property [WPF]
ms.assetid: 71e4327e-ca57-444c-a3cf-09fb381491a0
ms.openlocfilehash: 8f04db274432c0e89c6839bef825976c8a2f853c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975318"
---
# <a name="how-to-apply-a-transform-to-an-element-when-an-event-occurs"></a>Gewusst wie: Anwenden einer Transformation auf ein Element beim Auftreten eines Ereignisses
Dieses Beispiel zeigt, wie ein-Ereignis angewendet wird, <xref:System.Windows.Media.ScaleTransform> Wenn ein Ereignis auftritt. Mithilfe des hier dargestellten Konzepts können Sie auch andere Transformationstypen anwenden. Weitere Informationen zu den verfügbaren Transformations Typen finden Sie in der <xref:System.Windows.Media.Transform> [Übersicht](transforms-overview.md)über Klassen oder Transformationen.  
  
 Sie können mit einem der folgenden beiden Verfahren eine Transformation auf ein Element anwenden:  
  
- Wenn sich die Transformation *nicht* auf das Layout auswirken soll, verwenden Sie die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft des-Elements.  
  
- Wenn sich die Transformation auf das Layout auswirken soll, verwenden Sie die- <xref:System.Windows.FrameworkElement.LayoutTransform%2A> Eigenschaft des-Elements.  
  
 Im folgenden Beispiel wird ein <xref:System.Windows.Media.ScaleTransform> auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft einer Schaltfläche angewendet. Wenn die Maus über die Schaltfläche bewegt wird, <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> werden die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> des <xref:System.Windows.Media.ScaleTransform> auf festgelegt `2` , wodurch die Schaltfläche vergrößert wird. Wenn der Mauszeiger von der Schaltfläche bewegt wird <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> und <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> auf festgelegt `1` ist, wird die Schaltfläche auf Ihre ursprüngliche Größe zurückgesetzt.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[ButtonTransform#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ButtonTransform/CSharp/ButtonTransformExample.xaml#1)]  
  
 [!code-csharp[ButtonTransform#1cb](~/samples/snippets/csharp/VS_Snippets_Wpf/ButtonTransform/CSharp/ButtonTransformExample.xaml.cs#1cb)]
 [!code-vb[ButtonTransform#1cb](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ButtonTransform/VisualBasic/ButtonTransformExample.xaml.vb#1cb)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Transform>
- <xref:System.Windows.Media.ScaleTransform>
- [Übersicht über Transformationen](transforms-overview.md)
- [Artikel zu Vorgehensweisen](transformations-how-to-topics.md)
- [Übersicht über Routingereignisse](../advanced/routed-events-overview.md)
