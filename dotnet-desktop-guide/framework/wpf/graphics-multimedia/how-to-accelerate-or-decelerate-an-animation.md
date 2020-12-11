---
title: 'Gewusst wie: Beschleunigen oder Verlangsamen einer Animation'
ms.date: 03/30/2017
helpviewer_keywords:
- decelerating animation [WPF]
- accelerating animation [WPF]
- animation [WPF], accelerating
- animation [WPF], decelerating
ms.assetid: 4f383b2c-f94d-4a4e-9a06-f56f5dae95f9
ms.openlocfilehash: 7ab55ba44b866a992b9021284f170858f0108d15
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977221"
---
# <a name="how-to-accelerate-or-decelerate-an-animation"></a>Vorgehensweise: beschleunigen oder verlangsamen einer Animation

Dieses Beispiel zeigt, wie Sie eine Animation beschleunigen und im Laufe der Zeit verlangsamen können. Im folgenden Beispiel werden mehrere Rechtecke von Animationen mit unterschiedlichen <xref:System.Windows.Media.Animation.Timeline.AccelerationRatio%2A> -und- <xref:System.Windows.Media.Animation.Timeline.DecelerationRatio%2A> Einstellungen animiert.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[timingbehaviors_snip#1](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AccelDecelExample.xaml#1)]  
  
 Code wurde in diesem Beispiel ausgelassen. Den gesamten Code finden Sie unter [Animations Zeitverhalten (c#)](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp) oder [Animations Zeitverhalten (Visual Basic)](https://github.com/dotnet/docs/tree/master/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic).
