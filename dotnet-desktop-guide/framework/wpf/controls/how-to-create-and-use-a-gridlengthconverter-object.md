---
title: 'Gewusst wie: Erstellen und Verwenden eines GridLengthConverter-Objekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Grid control [WPF], creating [WPF], GridLengthConverter objects
ms.assetid: 5ab75911-e36a-4825-80e4-081c57e8e182
ms.openlocfilehash: 7cf6e12c1f3f9530d4616f0cfdecff1f07820615
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977652"
---
# <a name="how-to-create-and-use-a-gridlengthconverter-object"></a>Gewusst wie: Erstellen und Verwenden eines GridLengthConverter-Objekts
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie eine Instanz von erstellt und verwendet wird <xref:System.Windows.GridLengthConverter> . Im Beispiel wird eine benutzerdefinierte Methode mit dem Namen definiert `changeCol` , die den an einen übergibt, der <xref:System.Windows.Controls.ListBoxItem> den einer <xref:System.Windows.GridLengthConverter> <xref:System.Windows.Controls.ContentControl.Content%2A> <xref:System.Windows.Controls.ListBoxItem> in eine Instanz von konvertiert <xref:System.Windows.GridLength> . Der konvertierte Wert wird dann als Wert der- <xref:System.Windows.Controls.ColumnDefinition.Width%2A> Eigenschaft des-Elements zurückgegeben <xref:System.Windows.Controls.ColumnDefinition> .  
  
 Das Beispiel definiert auch eine zweite benutzerdefinierte Methode mit dem Namen `changeColVal` . Diese benutzerdefinierte Methode konvertiert den einer <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> <xref:System.Windows.Controls.Slider> in einen <xref:System.String> und übergibt diesen Wert dann wieder an den <xref:System.Windows.Controls.ColumnDefinition> als <xref:System.Windows.Controls.ColumnDefinition.Width%2A> des-Elements.  
  
 Beachten Sie, dass eine separate [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Datei den Inhalt eines <xref:System.Windows.Controls.ListBoxItem> definiert.  
  
 [!code-csharp[gridlengthConverterGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/gridlengthConverterGrid/CSharp/Window1.xaml.cs#1)]
 [!code-vb[gridlengthConverterGrid#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/gridlengthConverterGrid/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.GridLengthConverter>
- <xref:System.Windows.GridLength>
