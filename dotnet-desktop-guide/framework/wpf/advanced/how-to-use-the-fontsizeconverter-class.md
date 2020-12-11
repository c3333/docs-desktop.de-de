---
title: 'Gewusst wie: Verwenden der FontSizeConverter-Klasse'
ms.date: 03/30/2017
helpviewer_keywords:
- FontSizeConverter objects [WPF]
- typography [WPF], FontSizeConverter objects
ms.assetid: 3b0592bd-7223-4860-a108-a5d72f3a9178
ms.openlocfilehash: b4662ef60866150008d84f22de44852b65373282
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977837"
---
# <a name="how-to-use-the-fontsizeconverter-class"></a>Gewusst wie: Verwenden der FontSizeConverter-Klasse
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird gezeigt, wie eine Instanz von erstellt <xref:System.Windows.FontSizeConverter> und verwendet wird, um einen Schrift Grad zu ändern.  
  
 Im Beispiel wird eine benutzerdefinierte Methode namens definiert `changeSize` , die den Inhalt einer <xref:System.Windows.Controls.ListBoxItem> , die in einer separaten Datei definiert ist, in eine [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Instanz von <xref:System.Double> und höher in eine konvertiert <xref:System.String> . Diese Methode übergibt das <xref:System.Windows.Controls.ListBoxItem> an ein- <xref:System.Windows.FontSizeConverter> Objekt, das den einer <xref:System.Windows.Controls.ContentControl.Content%2A> <xref:System.Windows.Controls.ListBoxItem> in eine Instanz von konvertiert <xref:System.Double> . Dieser Wert wird dann als Wert der- <xref:System.Windows.Controls.TextBlock.FontSize%2A> Eigenschaft des-Elements zurückgegeben <xref:System.Windows.Controls.TextBlock> .  
  
 In diesem Beispiel wird auch eine zweite benutzerdefinierte Methode mit dem Namen definiert `changeFamily` . Diese Methode konvertiert den <xref:System.Windows.Controls.ContentControl.Content%2A> von <xref:System.Windows.Controls.ListBoxItem> in einen <xref:System.String> und übergibt diesen Wert dann an die- <xref:System.Windows.Controls.TextBlock.FontFamily%2A> Eigenschaft des- <xref:System.Windows.Controls.TextBlock> Elements.  
  
 Dieses Beispiel wird nicht ausgeführt.  
  
 [!code-csharp[FontSizeConverter#1](~/samples/snippets/csharp/VS_Snippets_Wpf/FontSizeConverter/CSharp/Window1.xaml.cs#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.FontSizeConverter>
