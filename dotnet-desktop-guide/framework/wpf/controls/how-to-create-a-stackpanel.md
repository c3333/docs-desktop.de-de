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
# <a name="how-to-create-a-stackpanel"></a><span data-ttu-id="c3b2f-102">Gewusst wie: Erstellen eines StackPanel</span><span class="sxs-lookup"><span data-stu-id="c3b2f-102">How to: Create a StackPanel</span></span>
<span data-ttu-id="c3b2f-103">In diesem Beispiel wird gezeigt, wie ein erstellt wird <xref:System.Windows.Controls.StackPanel> .</span><span class="sxs-lookup"><span data-stu-id="c3b2f-103">This example shows how to create a <xref:System.Windows.Controls.StackPanel>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c3b2f-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c3b2f-104">Example</span></span>  
 <span data-ttu-id="c3b2f-105"><xref:System.Windows.Controls.StackPanel>Mit einem können Sie Elemente in einer angegebenen Richtung stapeln.</span><span class="sxs-lookup"><span data-stu-id="c3b2f-105">A <xref:System.Windows.Controls.StackPanel> allows you to stack elements in a specified direction.</span></span> <span data-ttu-id="c3b2f-106">Durch die Verwendung von Eigenschaften, die für definiert sind, <xref:System.Windows.Controls.StackPanel> kann der Inhalt sowohl vertikal als auch als Standardeinstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3b2f-106">By using properties that are defined on <xref:System.Windows.Controls.StackPanel>, content can flow both vertically, which is the default setting, or horizontally.</span></span>  
  
 <span data-ttu-id="c3b2f-107">Im folgenden Beispiel werden <xref:System.Windows.Controls.TextBlock> mithilfe von vertikal fünf-Steuerelemente mit jeweils unterschiedlichen und mit einem-Element gestapelt <xref:System.Windows.Controls.Border> <xref:System.Windows.Controls.Border.Background%2A> <xref:System.Windows.Controls.StackPanel> .</span><span class="sxs-lookup"><span data-stu-id="c3b2f-107">The following example vertically stacks five <xref:System.Windows.Controls.TextBlock> controls, each with a different <xref:System.Windows.Controls.Border> and <xref:System.Windows.Controls.Border.Background%2A>, by using <xref:System.Windows.Controls.StackPanel>.</span></span> <span data-ttu-id="c3b2f-108">Die untergeordneten Elemente, die keine angegebene <xref:System.Windows.FrameworkElement.Width%2A> Streckung aufweisen, um das übergeordnete Fenster auszufüllen. allerdings werden die untergeordneten Elemente, die über eine angegebene verfügen <xref:System.Windows.FrameworkElement.Width%2A> , innerhalb des Fensters zentriert.</span><span class="sxs-lookup"><span data-stu-id="c3b2f-108">The child elements that have no specified <xref:System.Windows.FrameworkElement.Width%2A> stretch to fill the parent window; however, the child elements that have a specified <xref:System.Windows.FrameworkElement.Width%2A>, are centered within the window.</span></span>  
  
 <span data-ttu-id="c3b2f-109">Die Standard Stapel Richtung in einer <xref:System.Windows.Controls.StackPanel> ist vertikal.</span><span class="sxs-lookup"><span data-stu-id="c3b2f-109">The default stack direction in a <xref:System.Windows.Controls.StackPanel> is vertical.</span></span> <span data-ttu-id="c3b2f-110">Verwenden Sie zum Steuern des Inhalts Flusses in einem <xref:System.Windows.Controls.StackPanel> die- <xref:System.Windows.Controls.StackPanel.Orientation%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c3b2f-110">To control content flow in a <xref:System.Windows.Controls.StackPanel>, use the <xref:System.Windows.Controls.StackPanel.Orientation%2A> property.</span></span> <span data-ttu-id="c3b2f-111">Sie können die horizontale Ausrichtung mithilfe der- <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> Eigenschaft steuern.</span><span class="sxs-lookup"><span data-stu-id="c3b2f-111">You can control horizontal alignment by using the <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> property.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="c3b2f-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3b2f-112">See also</span></span>

- <xref:System.Windows.Controls.StackPanel>
- [<span data-ttu-id="c3b2f-113">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="c3b2f-113">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="c3b2f-114">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="c3b2f-114">How-to Topics</span></span>](stackpanel-how-to-topics.md)
