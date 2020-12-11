---
title: 'Gewusst wie: Abrufen und Festlegen von Canvas-Positionierungseigenschaften'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Canvas control [WPF], setting positioning properties
ms.assetid: 1636b950-2b5a-4507-8a10-c5034cc58b1c
ms.openlocfilehash: 06508e1198736ccb1cbda41641dff4bc634ef82b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975498"
---
# <a name="how-to-get-or-set-canvas-positioning-properties"></a>Gewusst wie: Abrufen und Festlegen von Canvas-Positionierungseigenschaften
In diesem Beispiel wird gezeigt, wie die Positions Methoden des-Elements verwendet werden <xref:System.Windows.Controls.Canvas> , um untergeordneten Inhalt zu positionieren. In diesem Beispiel wird der Inhalt in einem verwendet <xref:System.Windows.Controls.ListBoxItem> , um Positionierungs Werte darzustellen, und die Werte werden in Instanzen von konvertiert <xref:System.Double> . Dies ist ein erforderliches Argument für die Positionierung. Die Werte werden dann wieder in Zeichen folgen konvertiert und als Text in einem- <xref:System.Windows.Controls.TextBlock> Element mithilfe der- <xref:System.Windows.Controls.Canvas.GetLeft%2A> Methode angezeigt.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Windows.Controls.ListBox> Element erstellt, das elf auswählbare <xref:System.Windows.Controls.ListBoxItem> Elemente aufweist. Das- <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> Ereignis löst die `ChangeLeft` benutzerdefinierte-Methode aus, die der nachfolgende Codeblock definiert.  
  
 Jeder <xref:System.Windows.Controls.ListBoxItem> stellt einen- <xref:System.Double> Wert dar, der eines der Argumente ist, die von der- <xref:System.Windows.Controls.Canvas.SetLeft%2A> Methode akzeptiert werden <xref:System.Windows.Controls.Canvas> . Um einen <xref:System.Windows.Controls.ListBoxItem> zur Darstellung einer Instanz von verwenden zu <xref:System.Double> können, müssen Sie zuerst den <xref:System.Windows.Controls.ListBoxItem> in den richtigen Datentyp konvertieren.  
  
 [!code-xaml[CanvasPositioningProperties#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml#1)]  
  
 Wenn ein Benutzer die <xref:System.Windows.Controls.ListBox> Auswahl ändert, wird die Benutzer `ChangeLeft` definierte Methode aufgerufen. Diese Methode übergibt das <xref:System.Windows.Controls.ListBoxItem> an ein- <xref:System.Windows.LengthConverter> Objekt, das den einer <xref:System.Windows.Controls.ContentControl.Content%2A> <xref:System.Windows.Controls.ListBoxItem> in eine-Instanz konvertiert <xref:System.Double> (Beachten Sie, dass dieser Wert bereits mit der-Methode in eine konvertiert wurde <xref:System.String> <xref:System.Windows.Controls.Control.ToString%2A> ). Dieser Wert wird dann an die <xref:System.Windows.Controls.Canvas.SetLeft%2A> -Methode und die- <xref:System.Windows.Controls.Canvas.GetLeft%2A> Methode von zurückgegeben, um <xref:System.Windows.Controls.Canvas> die Position des-Objekts zu ändern `text1` .  
  
 [!code-csharp[CanvasPositioningProperties#2](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml.cs#2)]
 [!code-vb[CanvasPositioningProperties#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasPositioningProperties/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.ListBoxItem>
- <xref:System.Windows.LengthConverter>
- [Übersicht über Panel-Elemente](panels-overview.md)
