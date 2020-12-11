---
title: 'Gewusst wie: Verwenden eines ThicknessConverter-Objekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- border thickness [WPF]
- ThicknessConverter objects [WPF]
ms.assetid: 52682194-d7fd-499c-8005-73fcc84e7b2c
ms.openlocfilehash: 7420824ad939012d12f61ecbb72f2d00ce483e8b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976274"
---
# <a name="how-to-use-a-thicknessconverter-object"></a>Gewusst wie: Verwenden eines ThicknessConverter-Objekts

## <a name="example"></a>Beispiel  

 In diesem Beispiel wird gezeigt, wie eine Instanz von erstellt <xref:System.Windows.ThicknessConverter> und verwendet wird, um die Stärke eines Rahmens zu ändern.  
  
 Im Beispiel wird eine benutzerdefinierte Methode mit dem Namen definiert `changeThickness` . diese Methode konvertiert zuerst den Inhalt einer <xref:System.Windows.Controls.ListBoxItem> , die in einer separaten [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Datei definiert ist, in eine Instanz von <xref:System.Windows.Thickness> und konvertiert den Inhalt später in einen <xref:System.String> . Diese Methode übergibt das <xref:System.Windows.Controls.ListBoxItem> an ein- <xref:System.Windows.ThicknessConverter> Objekt, das den einer <xref:System.Windows.Controls.ContentControl.Content%2A> <xref:System.Windows.Controls.ListBoxItem> in eine Instanz von konvertiert <xref:System.Windows.Thickness> . Dieser Wert wird dann als Wert der- <xref:System.Windows.Controls.Border.BorderThickness%2A> Eigenschaft von zurückgegeben <xref:System.Windows.Controls.Border> .  
  
 Dieses Beispiel wird nicht ausgeführt.  
  
 [!code-csharp[ThicknessConverter#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ThicknessConverter/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ThicknessConverter#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ThicknessConverter/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Thickness>
- <xref:System.Windows.ThicknessConverter>
- <xref:System.Windows.Controls.Border>
- [Vorgehensweise: Ändern der Margin-Eigenschaft](/previous-versions/dotnet/netframework-3.5/ms750561(v=vs.90))
- [Gewusst wie: Konvertieren eines ListBoxItem in einen neuen Datentyp](/previous-versions/dotnet/netframework-3.5/ms749147(v=vs.90))
- [Übersicht über Panel-Elemente](../controls/panels-overview.md)
