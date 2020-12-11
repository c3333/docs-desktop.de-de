---
title: 'Gewusst wie: Abrufen des Offsets eines visuellen Objekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- getting offset values from visual objects [WPF]
- offset values [WPF], retrieving from visual objects [WPF]
- visual objects [WPF], retrieving offset values from
- retrieving offset values from visual objects [WPF]
ms.assetid: 889a1dd6-1b11-445a-b351-fbb04c53ee34
ms.openlocfilehash: 4787b771c7e59a8b033b9267079c068a5845a1e6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976782"
---
# <a name="how-to-get-the-offset-of-a-visual"></a>Gewusst wie: Abrufen des Offsets eines visuellen Objekts
In diesen Beispielen wird gezeigt, wie der Offset Wert eines visuellen Objekts abgerufen wird, das relativ zu seinem übergeordneten Element oder einem Vorgänger oder Nachfolger ist.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Markup Beispiel wird ein- <xref:System.Windows.Controls.TextBlock> Wert dargestellt, <xref:System.Windows.FrameworkElement.Margin%2A> der mit dem Wert 4 definiert ist.  
  
 [!code-xaml[VisualSnippets#VisualSnippet1](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window1.xaml#visualsnippet1)]  
  
 Im folgenden Codebeispiel wird gezeigt, wie die-Methode verwendet wird <xref:System.Windows.Media.VisualTreeHelper.GetOffset%2A> , um den Offset von abzurufen <xref:System.Windows.Controls.TextBlock> . Die Offset Werte sind im zurückgegebenen <xref:System.Windows.Vector> Wert enthalten.  
  
 [!code-csharp[VisualSnippets#VisualSnippet2](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window1.xaml.cs#visualsnippet2)]
 [!code-vb[VisualSnippets#VisualSnippet2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualSnippets/visualbasic/window1.xaml.vb#visualsnippet2)]  
  
 Der Offset berücksichtigt den <xref:System.Windows.FrameworkElement.Margin%2A> Wert. In diesem Fall <xref:System.Windows.Vector.X%2A> ist 4, und <xref:System.Windows.Vector.Y%2A> ist 4.  
  
 Der zurückgegebene Offset Wert ist relativ zum übergeordneten Element von <xref:System.Windows.Media.Visual> . Wenn Sie einen Offset Wert zurückgeben möchten, der nicht relativ zum übergeordneten Element eines ist <xref:System.Windows.Media.Visual> , verwenden Sie die- <xref:System.Windows.Media.Visual.TransformToAncestor%2A> Methode.  
  
## <a name="getting-the-offset-relative-to-an-ancestor"></a>Erzielen des Offsets in Relation zu einem Vorgänger  
 Im folgenden Markup Beispiel wird ein- <xref:System.Windows.Controls.TextBlock> Objekt gezeigt, das in zwei-Objekten geschachtelt ist <xref:System.Windows.Controls.StackPanel> .  
  
 [!code-xaml[VisualSnippets#VisualSnippet7](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window2.xaml#visualsnippet7)]  
  
 Die folgende Abbildung zeigt die Ergebnisse des Markups.  
  
 ![Versatzwerte für Objekte](./media/visualoffset-01.png "VisualOffset_01")  
TextBlock in zwei StackPanels geschachtelt  
  
 Im folgenden Codebeispiel wird gezeigt, wie die-Methode verwendet wird <xref:System.Windows.Media.Visual.TransformToAncestor%2A> , um den Offset des <xref:System.Windows.Controls.TextBlock> relativ zum enthaltenden abzurufen <xref:System.Windows.Window> . Die Offset Werte sind im zurückgegebenen <xref:System.Windows.Media.GeneralTransform> Wert enthalten.  
  
 [!code-csharp[VisualSnippets#VisualSnippet5](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window1.xaml.cs#visualsnippet5)]
 [!code-vb[VisualSnippets#VisualSnippet5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualSnippets/visualbasic/window1.xaml.vb#visualsnippet5)]  
  
 Der Offset berücksichtigt die <xref:System.Windows.FrameworkElement.Margin%2A> Werte für alle Objekte innerhalb der enthaltenden <xref:System.Windows.Window> . In diesem Fall <xref:System.Windows.Vector.X%2A> ist 28 (16 + 8 + 4), und <xref:System.Windows.Vector.Y%2A> ist 28.  
  
 Der zurückgegebene Offset Wert ist relativ zum Vorgänger von <xref:System.Windows.Media.Visual> . Wenn Sie einen Offset Wert zurückgeben möchten, der relativ zum Nachfolger eines ist <xref:System.Windows.Media.Visual> , verwenden Sie die- <xref:System.Windows.Media.Visual.TransformToDescendant%2A> Methode.  
  
## <a name="getting-the-offset-relative-to-a-descendant"></a>Erzielen des Offsets in Relation zu einem Nachfolger  
 Im folgenden Markup Beispiel wird ein- <xref:System.Windows.Controls.TextBlock> Objekt gezeigt, das in einem-Objekt enthalten ist <xref:System.Windows.Controls.StackPanel> .  
  
 [!code-xaml[VisualSnippets#VisualSnippet4](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window1.xaml#visualsnippet4)]  
  
 Im folgenden Codebeispiel wird gezeigt, wie die-Methode verwendet wird <xref:System.Windows.Media.Visual.TransformToDescendant%2A> , um den Offset des-Elements <xref:System.Windows.Controls.StackPanel> relativ zu seinem untergeordneten Element abzurufen <xref:System.Windows.Controls.TextBlock> . Die Offset Werte sind im zurückgegebenen <xref:System.Windows.Media.GeneralTransform> Wert enthalten.  
  
 [!code-csharp[VisualSnippets#VisualSnippet9](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window1.xaml.cs#visualsnippet9)]
 [!code-vb[VisualSnippets#VisualSnippet9](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualSnippets/visualbasic/window1.xaml.vb#visualsnippet9)]  
  
 Der Offset berücksichtigt die <xref:System.Windows.FrameworkElement.Margin%2A> Werte für alle-Objekte. In diesem Fall <xref:System.Windows.Vector.X%2A> ist-4, und <xref:System.Windows.Vector.Y%2A> ist-4. Die Offset Werte sind negative Werte, da das übergeordnete Objekt relativ zum untergeordneten Objekt negativ versetzt wird.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Visual>
- <xref:System.Windows.Media.VisualTreeHelper>
- [Übersicht über das WPF-Grafikrendering](wpf-graphics-rendering-overview.md)
