---
title: 'Gewusst wie: Zeichnen eines Bereichs mit einem Systempinsel'
ms.date: 03/30/2017
helpviewer_keywords:
- system brushes [WPF], painting with
- painting [WPF], with system brushes
- brushes [WPF], painting with system brushes [WPF]
ms.assetid: 5141a763-9235-42cb-a6bb-afc75513eac7
ms.openlocfilehash: 26511c577bf06b016dfc69cedc7fce2bafb35f32
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976871"
---
# <a name="how-to-paint-an-area-with-a-system-brush"></a>Gewusst wie: Zeichnen eines Bereichs mit einem Systempinsel
Die <xref:System.Windows.SystemColors> -Klasse ermöglicht den Zugriff auf System Pinsel und Farben, wie z <xref:System.Windows.SystemColors.ControlBrush%2A> <xref:System.Windows.SystemColors.ControlBrushKey%2A> . b., und <xref:System.Windows.SystemColors.DesktopBrush%2A> . Ein System Pinsel ist ein- <xref:System.Windows.Media.SolidColorBrush> Objekt, das einen Bereich mit der angegebenen System Farbe zeichnet. Ein Systempinsel erzeugt immer eine Volltonfüllung und kann nicht zur Erstellung eines Farbverlaufs verwendet werden.  
  
 Sie können Systempinsel als statische oder dynamische Ressource verwenden. Verwenden Sie eine dynamische Ressource, wenn der Pinsel automatisch aktualisiert werden soll, wenn der Benutzer den Systempinsel bei laufender Anwendung ändert. Verwenden Sie andernfalls eine statische Ressource. Die SystemColors-Klasse enthält eine Vielzahl von statischen Eigenschaften, die einer strengen Namenskonvention folgen:  
  
- *\<SystemColor>* Zahn  
  
     Ruft einen statischen Verweis auf eine <xref:System.Windows.Media.SolidColorBrush> der angegebenen System Farbe ab.  
  
- *\<SystemColor>* Brushkey  
  
     Ruft einen dynamischen Verweis auf einen <xref:System.Windows.Media.SolidColorBrush> der angegebenen System Farbe ab.  
  
- *\<SystemColor>* Farbe  
  
     Ruft einen statischen Verweis auf eine <xref:System.Windows.Media.Color> Struktur der angegebenen System Farbe ab.  
  
- *\<SystemColor>* Colorkey  
  
     Ruft einen dynamischen Verweis auf die <xref:System.Windows.Media.Color> Struktur der angegebenen System Farbe ab.  
  
 Eine System Farbe ist eine <xref:System.Windows.Media.Color> Struktur, die verwendet werden kann, um einen Pinsel zu konfigurieren. Beispielsweise können Sie einen Farbverlauf mithilfe von Systemfarben erstellen, indem Sie die <xref:System.Windows.Media.GradientStop.Color%2A> Eigenschaften der <xref:System.Windows.Media.LinearGradientBrush> Farbverlaufs Stopps eines Objekts mit Systemfarben festlegen. Ein Beispiel finden Sie unter [Verwenden von System Farben in einem Farbverlauf](how-to-use-system-colors-in-a-gradient.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein dynamischer Verweis auf einen Systempinsel verwendet, um den Hintergrund einer Schaltfläche festzulegen.  
  
 [!code-xaml[brushsamples_snip#GraphicsMMDynamicSystemColorDesktopBrushKeyExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/DynamicSystemBrushExample.xaml#graphicsmmdynamicsystemcolordesktopbrushkeyexamplewholepage)]  
  
 Im nächsten Beispiel wird ein statischer Verweis auf einen Systempinsel verwendet, um den Hintergrund einer Schaltfläche festzulegen.  
  
 [!code-xaml[brushsamples_snip#GraphicsMMStaticSystemColorDesktopBrushExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/StaticSystemBrushExample.xaml#graphicsmmstaticsystemcolordesktopbrushexamplewholepage)]  
  
 Ein Beispiel für die Verwendung einer System Farbe in einem Farbverlauf finden Sie unter [Verwenden von Systemfarben in einem Farbverlauf](how-to-use-system-colors-in-a-gradient.md).  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von Systemfarben in einem Farbverlauf](how-to-use-system-colors-in-a-gradient.md)
- [Übersicht über das Zeichnen mit Volltonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md)
