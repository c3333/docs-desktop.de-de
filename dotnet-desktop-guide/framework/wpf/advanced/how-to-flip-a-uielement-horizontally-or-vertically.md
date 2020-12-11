---
title: 'Gewusst wie: Horizontales oder vertikales Kippen eines UIElement'
ms.date: 03/30/2017
helpviewer_keywords:
- flipping UIElements [WPF]
- UIElements [WPF], flipping
ms.assetid: 02c6730f-65c0-40d5-a553-4cb663721882
ms.openlocfilehash: 6b3da322493d17e4f8e36a35b9a0e40fdc9dc685
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977570"
---
# <a name="how-to-flip-a-uielement-horizontally-or-vertically"></a>Gewusst wie: Horizontales oder vertikales Kippen eines UIElement
Dieses Beispiel zeigt, wie Sie einen <xref:System.Windows.Media.ScaleTransform> <xref:System.Windows.UIElement> horizontal oder vertikal mit einem kippen. In diesem Beispiel wird ein- <xref:System.Windows.Controls.Button> Steuerelement (ein Typ von <xref:System.Windows.UIElement> ) durch Anwenden eines <xref:System.Windows.Media.ScaleTransform> auf seine- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft gekippt.  
  
## <a name="example"></a>Beispiel  
 Die folgende Abbildung zeigt die Schaltfläche zum kippen.  
  
 ![Eine Schaltfläche ohne Transformierung](./media/graphicsmm-buttonflipbeforeflip.gif "graphicsmm_buttonflipbeforeflip")  
Das zu kippen UIElement.  
  
 Der folgende Code zeigt den Code, mit dem die Schaltfläche erstellt wird.  
  
 [!code-xaml[Transforms_snip#GraphicsMMButtonWithoutFlip](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmbuttonwithoutflip)]  
  
## <a name="example"></a>Beispiel  
 Um die Schaltfläche horizontal zu kippen, erstellen Sie einen, <xref:System.Windows.Media.ScaleTransform> und legen <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> Sie dessen-Eigenschaft auf-1 fest. Wenden <xref:System.Windows.Media.ScaleTransform> Sie auf die-Eigenschaft der Schaltfläche an <xref:System.Windows.UIElement.RenderTransform%2A> .  
  
 [!code-xaml[Transforms_snip#GraphicsMMFlipButtonExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmflipbuttonexample1)]  
  
 ![Eine mit horizontaler Umschaltfläche &#40;0,0&#41;](./media/graphicsmm-buttonfliphorizontalflip-displaced.gif "graphicsmm_buttonfliphorizontalflip_displaced")  
Die Schaltfläche nach dem Anwenden von ScaleTransform  
  
## <a name="example"></a>Beispiel  
 Wie Sie in der vorherigen Abbildung sehen können, wurde die Schaltfläche gekippt, aber auch verschoben. Das liegt daran, dass die Schaltfläche von der oberen linken Ecke aus gekippt wurde. Um die Schaltfläche zu kippen, sollten Sie den <xref:System.Windows.Media.ScaleTransform> auf seine Mitte, nicht auf seine Ecke anwenden. Eine einfache Möglichkeit, das <xref:System.Windows.Media.ScaleTransform> auf das Schaltflächen-Center anzuwenden, besteht darin, die-Eigenschaft der Schaltfläche <xref:System.Windows.UIElement.RenderTransformOrigin%2A> auf 0,5, 0,5 festzulegen.  
  
 [!code-xaml[Transforms_snip#GraphicsMMFlipButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmflipbuttonexample2)]  
  
 ![Eine horizontal um ihren Mittelpunkt gekippte Schaltfläche](./media/graphicsmm-buttonfliphorizontalflip-inplace.gif "graphicsmm_buttonfliphorizontalflip_inplace")  
Die Schaltfläche mit einem RenderTransformOrigin von 0,5, 0,5  
  
## <a name="example"></a>Beispiel  
 Wenn Sie die Schaltfläche vertikal kippen möchten, legen Sie die <xref:System.Windows.Media.ScaleTransform> -Eigenschaft des-Objekts <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> anstelle der- <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> Eigenschaft fest.  
  
 [!code-xaml[Transforms_snip#GraphicsMMVerticalFlipButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmverticalflipbuttonexample2)]  
  
 ![Eine vertikal um ihren Mittelpunkt gekippte Schaltfläche](./media/graphicsmm-buttonflipverticalflip-inplace.gif "graphicsmm_buttonflipverticalflip_inplace")  
Die vertikal geflickte Schaltfläche  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Transformationen](../graphics-multimedia/transforms-overview.md)
