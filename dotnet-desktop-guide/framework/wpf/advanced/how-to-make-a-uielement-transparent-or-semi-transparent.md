---
title: 'Gewusst wie: Formatieren von "UIElement" als transparent oder halbtransparent'
ms.date: 03/30/2017
helpviewer_keywords:
- UIElements [WPF], transparency
- opacity [WPF], of UIElements
- transparency of UIElements [WPF]
- UIElements [WPF], opacity
ms.assetid: a49fc8d6-7b32-4f28-9122-39b632a19b4b
ms.openlocfilehash: 1de9a7e11fee241ecb71242e9808e77b7e5e63b0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976281"
---
# <a name="how-to-make-a-uielement-transparent-or-semi-transparent"></a>Gewusst wie: Formatieren von "UIElement" als transparent oder halbtransparent
Dieses Beispiel zeigt, wie Sie <xref:System.Windows.UIElement> transparent oder halbtransparent machen. Wenn Sie ein Element transparent oder halbtransparent machen möchten, legen Sie dessen- <xref:System.Windows.UIElement.Opacity%2A> Eigenschaft fest. Mit einem Wert von `0.0` wird das-Element vollständig transparent, während ein-Wert `1.0` das-Element vollständig deckend macht. Mit dem Wert `0.5` wird das Element 50% nicht transparent, usw. Ein Element <xref:System.Windows.UIElement.Opacity%2A> ist standardmäßig auf festgelegt `1.0` .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die einer <xref:System.Windows.UIElement.Opacity%2A> Schaltfläche auf festgelegt `0.25` , sodass Sie und deren Inhalt (in diesem Fall der Text der Schaltfläche) 25% deckend ist.  
  
 [!code-xaml[brushsamples_snip#2](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/OpacityExample.xaml#2)]  
  
 [!code-csharp[brushsamples_procedural_snip#2](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/OpacityExample.cs#2)]  
  
 Wenn der Inhalt eines Elements über eigene <xref:System.Windows.UIElement.Opacity%2A> Einstellungen verfügt, werden diese Werte mit den enthaltenden Elementen multipliziert <xref:System.Windows.UIElement.Opacity%2A> .  
  
 Im folgenden Beispiel wird die Schaltfläche <xref:System.Windows.UIElement.Opacity%2A> auf `0.25` und die eines-Steuer Elements, das <xref:System.Windows.UIElement.Opacity%2A> <xref:System.Windows.Controls.Image> in der Schaltfläche enthalten `0.5` ist, auf festgelegt. Folglich wird das Image 12,5% deckend angezeigt: 0,25 * 0,5 = 0,125.  
  
 [!code-xaml[brushsamples_snip#3](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/OpacityExample.xaml#3)]  
  
 [!code-csharp[brushsamples_procedural_snip#3](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/OpacityExample.cs#3)]  
  
 Eine andere Möglichkeit, die Deckkraft eines Elements zu steuern, besteht darin, die Deckkraft des-Elements festzulegen <xref:System.Windows.Media.Brush> , das das Element zeichnet. Diese Vorgehensweise ermöglicht es Ihnen, die Deckkraft der Teile eines Elements selektiv zu ändern, und bietet Leistungsvorteile gegenüber der Verwendung der-Eigenschaft des-Elements <xref:System.Windows.UIElement.Opacity%2A> . Im folgenden Beispiel wird der <xref:System.Windows.Media.Brush.Opacity%2A> von einem <xref:System.Windows.Media.SolidColorBrush> -Wert festgelegt, der zum Zeichnen der Schaltfläche verwendet <xref:System.Windows.Controls.Control.Background%2A> wird `0.25` . Folglich ist der Hintergrund des Pinsels 25% deckend, aber sein Inhalt (der Text der Schaltfläche) bleibt 100% deckend.  
  
 [!code-xaml[brushsamples_snip#4](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/OpacityExample.xaml#4)]  
  
 [!code-csharp[brushsamples_procedural_snip#4](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/OpacityExample.cs#4)]  
  
 Sie können auch die Deckkraft einzelner Farben in einem Pinsel steuern. Weitere Informationen zu Farben und Pinsel finden Sie unter Übersicht über das Zeichnen [mit voll Tonfarben und Farbverläufen](../graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md). Ein Beispiel, das zeigt, wie Sie die Deckkraft eines Elements animieren, finden Sie unter [Animieren der Deckkraft eines Elements oder eines Pinsels](../graphics-multimedia/how-to-animate-the-opacity-of-an-element-or-brush.md).
