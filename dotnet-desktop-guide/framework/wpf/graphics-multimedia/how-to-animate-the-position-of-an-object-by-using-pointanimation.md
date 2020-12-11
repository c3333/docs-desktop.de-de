---
title: 'Gewusst wie: Animieren der Position eines Objekts mit PointAnimation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], animation
- animation [WPF], PointAnimation
ms.assetid: 42310977-cc90-438a-8a47-0345898e01be
ms.openlocfilehash: 1ef3f77e551affaa7e61d2aabf95f10c29275417
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975331"
---
# <a name="how-to-animate-the-position-of-an-object-by-using-pointanimation"></a>Gewusst wie: Animieren der Position eines Objekts mit PointAnimation
In diesem Beispiel wird gezeigt, wie die-Klasse verwendet wird <xref:System.Windows.Media.Animation.PointAnimation> , um ein Objekt entlang eines zu animieren <xref:System.Windows.Shapes.Path> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine Ellipse entlang eines <xref:System.Windows.Shapes.Path> von einem Punkt auf dem Bildschirm zu einem anderen verschoben. Im Beispiel wird die Position eines animiert <xref:System.Windows.Media.EllipseGeometry> <xref:System.Windows.Media.Animation.PointAnimation> , indem zum Animieren der Eigenschaft verwendet wird <xref:System.Windows.Media.EllipseGeometry.Center%2A> .  
  
 [!code-csharp[BasicAnimations_snip#PointAnimationWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/PointAnimationExample.cs#pointanimationwholepage)]
 [!code-vb[BasicAnimations_snip#PointAnimationWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/PointAnimationExample.vb#pointanimationwholepage)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Animation.PointAnimation>
- <xref:System.Windows.Shapes.Path>
- <xref:System.Windows.Media.EllipseGeometry>
- <xref:System.Windows.Media.EllipseGeometry.Center%2A>
- [Übersicht über Animationen](animation-overview.md)
- [Grafiken und Multimedia](index.md)
- [Gewusst-wie-Themen zu Grafiken](graphics-how-to-topics.md)
- [Gewusst-wie-Themen zu Animation und Zeitsteuerung](animation-and-timing-how-to-topics.md)
