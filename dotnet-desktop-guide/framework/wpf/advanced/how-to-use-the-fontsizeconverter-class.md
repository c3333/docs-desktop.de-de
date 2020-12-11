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
# <a name="how-to-use-the-fontsizeconverter-class"></a><span data-ttu-id="60df5-102">Gewusst wie: Verwenden der FontSizeConverter-Klasse</span><span class="sxs-lookup"><span data-stu-id="60df5-102">How to: Use the FontSizeConverter Class</span></span>
## <a name="example"></a><span data-ttu-id="60df5-103">Beispiel</span><span class="sxs-lookup"><span data-stu-id="60df5-103">Example</span></span>  
 <span data-ttu-id="60df5-104">In diesem Beispiel wird gezeigt, wie eine Instanz von erstellt <xref:System.Windows.FontSizeConverter> und verwendet wird, um einen Schrift Grad zu ändern.</span><span class="sxs-lookup"><span data-stu-id="60df5-104">This example shows how to create an instance of <xref:System.Windows.FontSizeConverter> and use it to change a font size.</span></span>  
  
 <span data-ttu-id="60df5-105">Im Beispiel wird eine benutzerdefinierte Methode namens definiert `changeSize` , die den Inhalt einer <xref:System.Windows.Controls.ListBoxItem> , die in einer separaten Datei definiert ist, in eine [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Instanz von <xref:System.Double> und höher in eine konvertiert <xref:System.String> .</span><span class="sxs-lookup"><span data-stu-id="60df5-105">The example defines a custom method called `changeSize` that converts the contents of a <xref:System.Windows.Controls.ListBoxItem>, as defined in a separate [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] file, to an instance of <xref:System.Double>, and later into a <xref:System.String>.</span></span> <span data-ttu-id="60df5-106">Diese Methode übergibt das <xref:System.Windows.Controls.ListBoxItem> an ein- <xref:System.Windows.FontSizeConverter> Objekt, das den einer <xref:System.Windows.Controls.ContentControl.Content%2A> <xref:System.Windows.Controls.ListBoxItem> in eine Instanz von konvertiert <xref:System.Double> .</span><span class="sxs-lookup"><span data-stu-id="60df5-106">This method passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.FontSizeConverter> object, which converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Double>.</span></span> <span data-ttu-id="60df5-107">Dieser Wert wird dann als Wert der- <xref:System.Windows.Controls.TextBlock.FontSize%2A> Eigenschaft des-Elements zurückgegeben <xref:System.Windows.Controls.TextBlock> .</span><span class="sxs-lookup"><span data-stu-id="60df5-107">This value is then passed back as the value of the <xref:System.Windows.Controls.TextBlock.FontSize%2A> property of the <xref:System.Windows.Controls.TextBlock> element.</span></span>  
  
 <span data-ttu-id="60df5-108">In diesem Beispiel wird auch eine zweite benutzerdefinierte Methode mit dem Namen definiert `changeFamily` .</span><span class="sxs-lookup"><span data-stu-id="60df5-108">This example also defines a second custom method that is called `changeFamily`.</span></span> <span data-ttu-id="60df5-109">Diese Methode konvertiert den <xref:System.Windows.Controls.ContentControl.Content%2A> von <xref:System.Windows.Controls.ListBoxItem> in einen <xref:System.String> und übergibt diesen Wert dann an die- <xref:System.Windows.Controls.TextBlock.FontFamily%2A> Eigenschaft des- <xref:System.Windows.Controls.TextBlock> Elements.</span><span class="sxs-lookup"><span data-stu-id="60df5-109">This method converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.String>, and then passes that value to the <xref:System.Windows.Controls.TextBlock.FontFamily%2A> property of the <xref:System.Windows.Controls.TextBlock> element.</span></span>  
  
 <span data-ttu-id="60df5-110">Dieses Beispiel wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60df5-110">This example does not run.</span></span>  
  
 [!code-csharp[FontSizeConverter#1](~/samples/snippets/csharp/VS_Snippets_Wpf/FontSizeConverter/CSharp/Window1.xaml.cs#1)]  
  
## <a name="see-also"></a><span data-ttu-id="60df5-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60df5-111">See also</span></span>

- <xref:System.Windows.FontSizeConverter>
