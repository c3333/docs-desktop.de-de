---
title: 'Gewusst wie: Änderung der Spaltengröße mit einem GridSplitter'
ms.date: 03/30/2017
helpviewer_keywords:
- grid columns [WPF], resizing
- GridSplitter control [WPF], resizing grid columns
- resizing grid columns [WPF]
ms.assetid: 47b20fe6-7adc-4aa6-9693-b4e184eef74b
ms.openlocfilehash: f743e9ccf8a984a646a4b8f05ee99162e5bc73ad
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977031"
---
# <a name="how-to-resize-columns-with-a-gridsplitter"></a>Gewusst wie: Änderung der Spaltengröße mit einem GridSplitter
In diesem Beispiel wird gezeigt, wie eine vertikale erstellt wird <xref:System.Windows.Controls.GridSplitter> , um den Leerraum zwischen zwei Spalten in einer neu zu verteilen, <xref:System.Windows.Controls.Grid> ohne die Abmessungen von zu ändern <xref:System.Windows.Controls.Grid> .  
  
## <a name="example"></a>Beispiel  
 **Erstellen eines GridSplitter-Elements, das den Rand einer Spalte überlagert**  
  
 <xref:System.Windows.Controls.GridSplitter> <xref:System.Windows.Controls.Grid> Legen Sie für die <xref:System.Windows.Controls.Grid.Column%2A> angefügte-Eigenschaft eine der Spalten fest, die die Größe ändern möchten, um einen anzugeben, der die Größe der angrenzenden Spalten in einer ändert. Wenn Ihr <xref:System.Windows.Controls.Grid> mehr als eine Zeile enthält, legen Sie die <xref:System.Windows.Controls.Grid.RowSpan%2A> angefügte-Eigenschaft auf die Anzahl der Zeilen fest. Legen Sie dann die- <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> Eigenschaft auf <xref:System.Windows.HorizontalAlignment.Left> oder fest <xref:System.Windows.HorizontalAlignment.Right> (welche Ausrichtung Sie festlegen, hängt davon ab, für welche zwei Spalten die Größe geändert werden soll). Legen Sie abschließend die- <xref:System.Windows.FrameworkElement.VerticalAlignment%2A> Eigenschaft auf fest <xref:System.Windows.VerticalAlignment.Stretch> .  
  
 [!code-xaml[GridSplitterRowColumn#GridSplitterColumnOverlay](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterRowColumn/CS/Window1.xaml#gridsplittercolumnoverlay)]  
  
 Eine <xref:System.Windows.Controls.GridSplitter> , für die keine eigene Spalte vorhanden ist, kann von anderen Steuerelementen in der verdeckt werden <xref:System.Windows.Controls.Grid> . Weitere Informationen zum Vermeiden dieses Problems finden Sie unter [Sicherstellen, dass ein GridSplitter sichtbar ist](how-to-make-sure-that-a-gridsplitter-is-visible.md).  
  
 **Erstellen eines GridSplitter-Elements, das eine Spalte einnimmt**  
  
 Wenn Sie einen angeben möchten, <xref:System.Windows.Controls.GridSplitter> der eine Spalte in einer einnimmt <xref:System.Windows.Controls.Grid> , legen <xref:System.Windows.Controls.Grid.Column%2A> Sie die angefügte-Eigenschaft auf eine der Spalten fest, dessen Größe Sie ändern möchten. Wenn das Raster über mehr als eine Zeile verfügt, legen Sie die <xref:System.Windows.Controls.Grid.RowSpan%2A> angefügte-Eigenschaft auf die Anzahl der Zeilen fest. Legen Sie dann den <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> auf fest <xref:System.Windows.HorizontalAlignment.Center> , legen <xref:System.Windows.FrameworkElement.VerticalAlignment%2A> Sie die-Eigenschaft auf fest <xref:System.Windows.VerticalAlignment.Stretch> , und legen Sie die <xref:System.Windows.Controls.ColumnDefinition.Width%2A> der Spalte, die die enthält, auf fest <xref:System.Windows.Controls.GridSplitter> <xref:System.Windows.GridLength.Auto%2A> .  
  
 Im folgenden Beispiel wird gezeigt, wie ein vertikal definiert wird <xref:System.Windows.Controls.GridSplitter> , das eine Spalte einnimmt und die Größe der Spalten auf beiden Seiten der Spalte ändert.  
  
 [!code-xaml[GridSplitterRowColumn#GridSplitterEntireColumnPart1](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterRowColumn/CS/Window1.xaml#gridsplitterentirecolumnpart1)]  
[!code-xaml[GridSplitterRowColumn#GridSplitterEntireColumnPart2](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterRowColumn/CS/Window1.xaml#gridsplitterentirecolumnpart2)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.GridSplitter>
- [Artikel zu Vorgehensweisen](gridsplitter-how-to-topics.md)
