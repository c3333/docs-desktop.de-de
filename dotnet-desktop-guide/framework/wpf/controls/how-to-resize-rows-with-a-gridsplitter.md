---
title: 'Gewusst wie: Änderung der Zeilengröße mit einem GridSplitter'
ms.date: 03/30/2017
helpviewer_keywords:
- resizing grid rows [WPF]
- grid rows [WPF], resizing
- GridSplitter control [WPF], resizing grid rows
ms.assetid: 2413a9f2-1d81-46ed-95cb-95ec8233eea2
ms.openlocfilehash: 6760a7a691af4f666294556cae3bc95a4299730a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977029"
---
# <a name="how-to-resize-rows-with-a-gridsplitter"></a>Gewusst wie: Änderung der Zeilengröße mit einem GridSplitter
In diesem Beispiel wird gezeigt, wie Sie mit einem horizontalen <xref:System.Windows.Controls.GridSplitter> den Leerraum zwischen zwei Zeilen in einem neu verteilen, <xref:System.Windows.Controls.Grid> ohne die Abmessungen des zu ändern <xref:System.Windows.Controls.Grid> .  
  
## <a name="example"></a>Beispiel  
 **Erstellen eines GridSplitter-Elements, das den Rand einer Zeile überlagert**  
  
 <xref:System.Windows.Controls.GridSplitter> <xref:System.Windows.Controls.Grid> Legen <xref:System.Windows.Controls.Grid.Row%2A> Sie die angefügte-Eigenschaft auf eine der Zeilen fest, dessen Größe Sie ändern möchten, um einen anzugeben, der die Größe der angrenzenden Zeilen in einem ändert. Wenn Ihr <xref:System.Windows.Controls.Grid> mehr als eine Spalte enthält, legen Sie die <xref:System.Windows.Controls.Grid.ColumnSpan%2A> angefügte-Eigenschaft fest, um die Anzahl der Spalten anzugeben. Legen Sie dann <xref:System.Windows.FrameworkElement.VerticalAlignment%2A> auf <xref:System.Windows.VerticalAlignment.Top> oder fest <xref:System.Windows.VerticalAlignment.Bottom> (welche Ausrichtung Sie festlegen, hängt davon ab, welche beiden Zeilen Sie ändern möchten). Legen Sie abschließend die- <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> Eigenschaft auf fest <xref:System.Windows.HorizontalAlignment.Stretch> .  
  
 Im folgenden Beispiel wird gezeigt, wie Sie eine horizontale definieren <xref:System.Windows.Controls.GridSplitter> , die die Größe angrenzender Zeilen ändert.  
  
 [!code-xaml[GridSplitterRowColumn#GridSplitterRowOverlay](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterRowColumn/CS/Window1.xaml#gridsplitterrowoverlay)]  
  
 Eine <xref:System.Windows.Controls.GridSplitter> , die keine eigene Zeile einnimmt, kann von anderen Steuerelementen in der verdeckt werden <xref:System.Windows.Controls.Grid> . Weitere Informationen zum Vermeiden dieses Problems finden Sie unter [Sicherstellen, dass ein GridSplitter sichtbar ist](how-to-make-sure-that-a-gridsplitter-is-visible.md).  
  
 **Erstellen eines GridSplitter-Elements, das eine Zeile einnimmt**  
  
 <xref:System.Windows.Controls.GridSplitter> <xref:System.Windows.Controls.Grid> Legen <xref:System.Windows.Controls.Grid.Row%2A> Sie die angefügte-Eigenschaft auf eine der Zeilen fest, für die die Größe geändert werden soll, um ein-Objekt anzugeben, das eine Zeile in einer einnimmt. Wenn Ihr <xref:System.Windows.Controls.Grid> mehr als eine Spalte enthält, legen Sie die <xref:System.Windows.Controls.Grid.ColumnSpan%2A> angefügte-Eigenschaft auf die Anzahl der Spalten fest. Legen Sie dann den <xref:System.Windows.FrameworkElement.VerticalAlignment%2A> auf fest <xref:System.Windows.VerticalAlignment.Center> , legen <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> Sie die-Eigenschaft auf fest <xref:System.Windows.HorizontalAlignment.Stretch> , und legen Sie die <xref:System.Windows.Controls.RowDefinition.Height%2A> der Zeile, die die enthält, auf fest <xref:System.Windows.Controls.GridSplitter> <xref:System.Windows.GridLength.Auto%2A> .  
  
 Im folgenden Beispiel wird gezeigt, wie Sie eine horizontale definieren <xref:System.Windows.Controls.GridSplitter> , die eine Zeile einnimmt und die Größe der Zeilen auf beiden Seiten der Zeile ändert.  
  
 [!code-xaml[GridSplitterRowColumn#GridSplitterEntireRowPart1](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterRowColumn/CS/Window1.xaml#gridsplitterentirerowpart1)]  
[!code-xaml[GridSplitterRowColumn#GridSplitterEntireRowPart2](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterRowColumn/CS/Window1.xaml#gridsplitterentirerowpart2)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.GridSplitter>
- [Artikel zu Vorgehensweisen](gridsplitter-how-to-topics.md)
