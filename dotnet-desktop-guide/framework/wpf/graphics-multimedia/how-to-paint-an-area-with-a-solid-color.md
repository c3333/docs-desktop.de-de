---
title: 'Gewusst wie: Zeichnen eines Bereichs mit einer Volltonfarbe'
ms.date: 03/30/2017
helpviewer_keywords:
- solid colors [WPF], painting with
- brushes [WPF], painting with solid colors
- painting [WPF], with solid colors
ms.assetid: 5d27d8a7-4bd7-4063-bdf3-2c5c0f19f9d3
ms.openlocfilehash: be28a0af04c4e43cdf745a5429468aee99e34c40
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976539"
---
# <a name="how-to-paint-an-area-with-a-solid-color"></a>Gewusst wie: Zeichnen eines Bereichs mit einer Volltonfarbe
Um einen Bereich mit einer voll Tonfarbe zu zeichnen, können Sie einen vordefinierten System Pinsel verwenden, z. b. <xref:System.Windows.Media.Brushes.Red%2A> oder <xref:System.Windows.Media.Brushes.Blue%2A> , oder Sie können eine neue erstellen <xref:System.Windows.Media.SolidColorBrush> und deren <xref:System.Windows.Media.SolidColorBrush.Color%2A> mit Alpha-, rot-, grün-und blauen Werten beschreiben. In XAML können Sie einen Bereich mit einer Volltonfarbe auch mit der Hexadezimalschreibweise zeichnen.  
  
 In den folgenden Beispielen wird jede dieser Techniken zum Zeichnen eines <xref:System.Windows.Shapes.Rectangle> blauen verwendet.  
  
## <a name="example"></a>Beispiel  
 **Verwenden eines vordefinierten Pinsels**  
  
 Im folgenden Beispiel wird der vordefinierte Pinsel <xref:System.Windows.Media.Brushes.Blue%2A> zum Zeichnen eines blauen Rechtecks verwendet.  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_PredefinedBrush1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_predefinedbrush1)]  
  
 [!code-csharp[brushsamples_procedural_snip#_graphicsmm_PredefinedBrush1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/SolidColorBrushExample.cs#_graphicsmm_predefinedbrush1)]  
  
 **Hexadezimalnotation**  
  
 Im nächsten Beispiel wird die Hexadezimalschreibweise mit acht Ziffern verwendet.  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_HexNotation8Digit1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_hexnotation8digit1)]  
  
 **Verwenden der ARGB-Werte**  
  
 Im nächsten Beispiel wird eine erstellt <xref:System.Windows.Media.SolidColorBrush> und <xref:System.Windows.Media.SolidColorBrush.Color%2A> die mit den ARGB-Werten für die Farbe blau beschrieben.  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_RgbNotation1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_rgbnotation1)]  
  
 [!code-csharp[brushsamples_procedural_snip#_graphicsmm_RgbNotation1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/SolidColorBrushExample.cs#_graphicsmm_rgbnotation1)]  
  
 Weitere Methoden zum Beschreiben von Farben finden Sie in der <xref:System.Windows.Media.Color> Struktur.  
  
 **Verwandte Themen**  
  
 Weitere Informationen zu <xref:System.Windows.Media.SolidColorBrush> und zusätzlichen Beispielen finden Sie unter Übersicht über das Zeichnen [mit voll Tonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md) .  
  
 Dieses Codebeispiel ist Teil eines größeren Beispiels, das für die-Klasse bereitgestellt wird <xref:System.Windows.Media.SolidColorBrush> . Das vollständige Beispiel finden Sie unter der [Beispiel für Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Brushes>
