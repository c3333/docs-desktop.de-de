---
title: 'Gewusst wie: Übersetzen eines Elements'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], translations
ms.assetid: 461c8273-15df-42f6-8672-89ba22887cc0
ms.openlocfilehash: addff0e22fb3f27ea924887809c0635aeb3ad67d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976858"
---
# <a name="how-to-translate-an-element"></a>Gewusst wie: Übersetzen eines Elements
In diesem Beispiel wird gezeigt, wie ein Element mithilfe eines übersetzt (verschoben) werden kann <xref:System.Windows.Media.TranslateTransform> .  
  
 Die- <xref:System.Windows.Media.TranslateTransform> Klasse ist besonders nützlich zum Verschieben von Elementen in Bereichen, die keine absolute Positionierung unterstützen. Wenn Sie z. b. ein <xref:System.Windows.Media.TranslateTransform> auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft eines-Elements anwenden, können Sie ein Element innerhalb von <xref:System.Windows.Controls.StackPanel> oder verschieben <xref:System.Windows.Controls.DockPanel> .  
  
 Verwenden Sie die- <xref:System.Windows.Media.TranslateTransform.X%2A> Eigenschaft des, <xref:System.Windows.Media.TranslateTransform> um den Betrag in Pixel anzugeben, um das Element entlang der x-Achse zu verschieben. Verwenden Sie die- <xref:System.Windows.Media.TranslateTransform.Y%2A> Eigenschaft, um den Betrag in Pixel anzugeben, um das Element entlang der y-Achse zu verschieben. Wenden Sie schließlich das <xref:System.Windows.Media.TranslateTransform> auf die- <xref:System.Windows.UIElement.RenderTransform%2A> Eigenschaft des-Elements an.  
  
 Im folgenden Beispiel wird ein <xref:System.Windows.Media.TranslateTransform> -Element verwendet, um ein Element 50 Pixel nach rechts und 50 Pixel nach unten zu verschieben.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[transformsSample#53](~/samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/TranslateTransformExample.xaml#53)]  
  
 Das komplette Beispiel finden Sie unter [Beispiel für 2D-Transformationen](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/2DTransforms).  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Transformationen](transforms-overview.md)
