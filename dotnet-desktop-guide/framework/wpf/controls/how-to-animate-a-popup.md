---
title: 'Gewusst wie: Animieren eines Popups'
ms.date: 03/30/2017
helpviewer_keywords:
- Popup control [WPF], animating
- animation [WPF], Popup controls
ms.assetid: acaa2a0a-6137-4efd-9cd1-75ece222e390
ms.openlocfilehash: b70d9c4cb1bca26a6c77d3a7c50add517ca8ef92
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977469"
---
# <a name="how-to-animate-a-popup"></a>Gewusst wie: Animieren eines Popups
Dieses Beispiel zeigt zwei Möglichkeiten zum Animieren eines- <xref:System.Windows.Controls.Primitives.Popup> Steuer Elements.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Controls.Primitives.PopupAnimation> Eigenschaft auf den Wert festgelegt, der <xref:System.Windows.Controls.Primitives.PopupAnimation.Slide> bewirkt, dass das <xref:System.Windows.Controls.Primitives.Popup> -Objekt "Folie-in" angezeigt wird.  
  
 Um das zu drehen, wird in <xref:System.Windows.Controls.Primitives.Popup> diesem Beispiel ein der-Eigenschaft auf dem zugewiesen, bei dem es sich um <xref:System.Windows.Media.RotateTransform> <xref:System.Windows.UIElement.RenderTransform%2A> <xref:System.Windows.Controls.Canvas> das untergeordnete Element von handelt <xref:System.Windows.Controls.Primitives.Popup> .  
  
 Damit die Transformation ordnungsgemäß funktioniert, muss im Beispiel die- <xref:System.Windows.Controls.Primitives.Popup.AllowsTransparency%2A> Eigenschaft auf festgelegt werden `true` . Außerdem <xref:System.Windows.FrameworkElement.Margin%2A> muss der auf dem <xref:System.Windows.Controls.Canvas> Inhalt ausreichend Speicherplatz angeben, um <xref:System.Windows.Controls.Primitives.Popup> zu drehen.  
  
 [!code-xaml[AnimatedPopup#RotateTransform2](~/samples/snippets/csharp/VS_Snippets_Wpf/AnimatedPopup/CS/Window1.xaml#rotatetransform2)]  
  
 Im folgenden Beispiel wird gezeigt, wie ein- <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignis, das beim Klicken auf ein Auftritt <xref:System.Windows.Controls.Button> , den auslöst, der <xref:System.Windows.Media.Animation.Storyboard> die Animation startet.  
  
 [!code-xaml[AnimatedPopup#RotateTransform1](~/samples/snippets/csharp/VS_Snippets_Wpf/AnimatedPopup/CS/Window1.xaml#rotatetransform1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.UIElement.RenderTransform%2A>
- <xref:System.Windows.Controls.Primitives.BulletDecorator>
- <xref:System.Windows.Media.RotateTransform>
- <xref:System.Windows.Media.Animation.Storyboard>
- <xref:System.Windows.Controls.Primitives.Popup>
- [Artikel zu Vorgehensweisen](popup-how-to-topics.md)
- [Übersicht über Popups](popup-overview.md)
