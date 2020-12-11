---
title: 'Gewusst wie: Verwenden von Systemfarben in einem Farbverlauf'
ms.date: 03/30/2017
helpviewer_keywords:
- gradients [WPF], system colors in
- system colors in gradients [WPF]
ms.assetid: 11942e7e-6300-4b50-8ed1-f50e8d20e7d2
ms.openlocfilehash: 55c99640907a0c372f8c7bbc50b9b45c9f15ef3c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976923"
---
# <a name="how-to-use-system-colors-in-a-gradient"></a>Gewusst wie: Verwenden von Systemfarben in einem Farbverlauf
Um eine System Farbe in einem Farbverlauf zu verwenden, verwenden Sie die *\<SystemColor>* statischen Farb-und *\<SystemColor>* Colorkey-Eigenschaften der- <xref:System.Windows.SystemColors> Klasse, um einen Verweis auf die Farbe zu erhalten, wobei *\<SystemColor>* der Name der gewünschten System Farbe ist. Verwenden *\<SystemColor>* Sie die Colorkey-Eigenschaften, wenn Sie einen dynamischen Verweis erstellen möchten, der automatisch aktualisiert wird, wenn das Systemdesign geändert wird. Andernfalls sollten Sie die *\<SystemColor>* Farbeigenschaften verwenden.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Farbverlauf mithilfe dynamischer Systemfarbressourcen erstellt.  
  
 [!code-xaml[brushsamples_snip#GraphicsMMDynamicSystemColorGradientExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/DynamicSystemColorExample.xaml#graphicsmmdynamicsystemcolorgradientexamplewholepage)]  
  
 Im nächsten Beispiel wird ein Farbverlauf mithilfe statischer Systemfarbressourcen erstellt.  
  
 [!code-xaml[brushsamples_snip#GraphicsMMStaticSystemColorGradientExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/StaticSystemColorExample.xaml#graphicsmmstaticsystemcolorgradientexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.SystemColors>
- [Zeichnen eines Bereichs mit einem Systempinsel](how-to-paint-an-area-with-a-system-brush.md)
- [Übersicht über das Zeichnen mit Volltonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md)
