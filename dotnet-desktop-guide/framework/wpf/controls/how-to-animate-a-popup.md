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
# <a name="how-to-animate-a-popup"></a><span data-ttu-id="8ab14-102">Gewusst wie: Animieren eines Popups</span><span class="sxs-lookup"><span data-stu-id="8ab14-102">How to: Animate a Popup</span></span>
<span data-ttu-id="8ab14-103">Dieses Beispiel zeigt zwei Möglichkeiten zum Animieren eines- <xref:System.Windows.Controls.Primitives.Popup> Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="8ab14-103">This example shows two ways to animate a <xref:System.Windows.Controls.Primitives.Popup> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8ab14-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8ab14-104">Example</span></span>  
 <span data-ttu-id="8ab14-105">Im folgenden Beispiel wird die- <xref:System.Windows.Controls.Primitives.PopupAnimation> Eigenschaft auf den Wert festgelegt, der <xref:System.Windows.Controls.Primitives.PopupAnimation.Slide> bewirkt, dass das <xref:System.Windows.Controls.Primitives.Popup> -Objekt "Folie-in" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8ab14-105">The following example sets the <xref:System.Windows.Controls.Primitives.PopupAnimation> property to a value of <xref:System.Windows.Controls.Primitives.PopupAnimation.Slide>, which causes the <xref:System.Windows.Controls.Primitives.Popup> to "slide-in" when it appears.</span></span>  
  
 <span data-ttu-id="8ab14-106">Um das zu drehen, wird in <xref:System.Windows.Controls.Primitives.Popup> diesem Beispiel ein der-Eigenschaft auf dem zugewiesen, bei dem es sich um <xref:System.Windows.Media.RotateTransform> <xref:System.Windows.UIElement.RenderTransform%2A> <xref:System.Windows.Controls.Canvas> das untergeordnete Element von handelt <xref:System.Windows.Controls.Primitives.Popup> .</span><span class="sxs-lookup"><span data-stu-id="8ab14-106">In order to rotate the <xref:System.Windows.Controls.Primitives.Popup>, this example assigns a <xref:System.Windows.Media.RotateTransform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property on the <xref:System.Windows.Controls.Canvas>, which is the child element of the <xref:System.Windows.Controls.Primitives.Popup>.</span></span>  
  
 <span data-ttu-id="8ab14-107">Damit die Transformation ordnungsgemäß funktioniert, muss im Beispiel die- <xref:System.Windows.Controls.Primitives.Popup.AllowsTransparency%2A> Eigenschaft auf festgelegt werden `true` .</span><span class="sxs-lookup"><span data-stu-id="8ab14-107">For the transform to work correctly, the example must set the <xref:System.Windows.Controls.Primitives.Popup.AllowsTransparency%2A> property to `true`.</span></span> <span data-ttu-id="8ab14-108">Außerdem <xref:System.Windows.FrameworkElement.Margin%2A> muss der auf dem <xref:System.Windows.Controls.Canvas> Inhalt ausreichend Speicherplatz angeben, um <xref:System.Windows.Controls.Primitives.Popup> zu drehen.</span><span class="sxs-lookup"><span data-stu-id="8ab14-108">In addition, the <xref:System.Windows.FrameworkElement.Margin%2A> on the <xref:System.Windows.Controls.Canvas> content must specify enough space for the <xref:System.Windows.Controls.Primitives.Popup> to rotate.</span></span>  
  
 [!code-xaml[AnimatedPopup#RotateTransform2](~/samples/snippets/csharp/VS_Snippets_Wpf/AnimatedPopup/CS/Window1.xaml#rotatetransform2)]  
  
 <span data-ttu-id="8ab14-109">Im folgenden Beispiel wird gezeigt, wie ein- <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignis, das beim Klicken auf ein Auftritt <xref:System.Windows.Controls.Button> , den auslöst, der <xref:System.Windows.Media.Animation.Storyboard> die Animation startet.</span><span class="sxs-lookup"><span data-stu-id="8ab14-109">The following example shows how a <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event, which occurs when a <xref:System.Windows.Controls.Button> is clicked, triggers the <xref:System.Windows.Media.Animation.Storyboard> that starts the animation.</span></span>  
  
 [!code-xaml[AnimatedPopup#RotateTransform1](~/samples/snippets/csharp/VS_Snippets_Wpf/AnimatedPopup/CS/Window1.xaml#rotatetransform1)]  
  
## <a name="see-also"></a><span data-ttu-id="8ab14-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ab14-110">See also</span></span>

- <xref:System.Windows.UIElement.RenderTransform%2A>
- <xref:System.Windows.Controls.Primitives.BulletDecorator>
- <xref:System.Windows.Media.RotateTransform>
- <xref:System.Windows.Media.Animation.Storyboard>
- <xref:System.Windows.Controls.Primitives.Popup>
- [<span data-ttu-id="8ab14-111">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="8ab14-111">How-to Topics</span></span>](popup-how-to-topics.md)
- [<span data-ttu-id="8ab14-112">Übersicht über Popups</span><span class="sxs-lookup"><span data-stu-id="8ab14-112">Popup Overview</span></span>](popup-overview.md)
