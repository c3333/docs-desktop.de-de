---
title: 'Gewusst wie: Erstellen eines StackPanel'
ms.date: 03/30/2017
helpviewer_keywords:
- StackPanel control [WPF], creating
ms.assetid: e7ce65cb-720a-4bb6-95b6-286b74488a58
ms.openlocfilehash: bcf6decff2fbc012b5f8b62794f0d7b2cd9f29fc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977658"
---
# <a name="how-to-create-a-stackpanel"></a>Gewusst wie: Erstellen eines StackPanel
In diesem Beispiel wird gezeigt, wie ein erstellt wird <xref:System.Windows.Controls.StackPanel> .  
  
## <a name="example"></a>Beispiel  
 <xref:System.Windows.Controls.StackPanel>Mit einem können Sie Elemente in einer angegebenen Richtung stapeln. Durch die Verwendung von Eigenschaften, die für definiert sind, <xref:System.Windows.Controls.StackPanel> kann der Inhalt sowohl vertikal als auch als Standardeinstellung verwendet werden.  
  
 Im folgenden Beispiel werden <xref:System.Windows.Controls.TextBlock> mithilfe von vertikal fünf-Steuerelemente mit jeweils unterschiedlichen und mit einem-Element gestapelt <xref:System.Windows.Controls.Border> <xref:System.Windows.Controls.Border.Background%2A> <xref:System.Windows.Controls.StackPanel> . Die untergeordneten Elemente, die keine angegebene <xref:System.Windows.FrameworkElement.Width%2A> Streckung aufweisen, um das übergeordnete Fenster auszufüllen. allerdings werden die untergeordneten Elemente, die über eine angegebene verfügen <xref:System.Windows.FrameworkElement.Width%2A> , innerhalb des Fensters zentriert.  
  
 Die Standard Stapel Richtung in einer <xref:System.Windows.Controls.StackPanel> ist vertikal. Verwenden Sie zum Steuern des Inhalts Flusses in einem <xref:System.Windows.Controls.StackPanel> die- <xref:System.Windows.Controls.StackPanel.Orientation%2A> Eigenschaft. Sie können die horizontale Ausrichtung mithilfe der- <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> Eigenschaft steuern.  
  
```xaml  
<Page xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" WindowTitle="StackPanel Sample">  
  <StackPanel>  
    <Border Background="SkyBlue" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="12">Stacked Item #1</TextBlock>  
    </Border>  
    <Border Width="400" Background="CadetBlue" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="14">Stacked Item #2</TextBlock>  
    </Border>  
    <Border Background="LightGoldenRodYellow" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="16">Stacked Item #3</TextBlock>  
    </Border>  
    <Border Width="200" Background="PaleGreen" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="18">Stacked Item #4</TextBlock>  
    </Border>  
    <Border Background="White" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="20">Stacked Item #5</TextBlock>  
    </Border>  
  </StackPanel>  
</Page>  
```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.StackPanel>
- [Übersicht über Panel-Elemente](panels-overview.md)
- [Artikel zu Vorgehensweisen](stackpanel-how-to-topics.md)
