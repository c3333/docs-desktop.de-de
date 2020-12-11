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
# <a name="how-to-create-and-use-a-gridlengthconverter-object"></a><span data-ttu-id="0b521-102">Gewusst wie: Erstellen und Verwenden eines GridLengthConverter-Objekts</span><span class="sxs-lookup"><span data-stu-id="0b521-102">How to: Create and Use a GridLengthConverter Object</span></span>
## <a name="example"></a><span data-ttu-id="0b521-103">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0b521-103">Example</span></span>  
 <span data-ttu-id="0b521-104">Im folgenden Beispiel wird gezeigt, wie eine Instanz von erstellt und verwendet wird <xref:System.Windows.GridLengthConverter> .</span><span class="sxs-lookup"><span data-stu-id="0b521-104">The following example shows how to create and use an instance of <xref:System.Windows.GridLengthConverter>.</span></span> <span data-ttu-id="0b521-105">Im Beispiel wird eine benutzerdefinierte Methode mit dem Namen definiert `changeCol` , die den an einen übergibt, der <xref:System.Windows.Controls.ListBoxItem> den einer <xref:System.Windows.GridLengthConverter> <xref:System.Windows.Controls.ContentControl.Content%2A> <xref:System.Windows.Controls.ListBoxItem> in eine Instanz von konvertiert <xref:System.Windows.GridLength> .</span><span class="sxs-lookup"><span data-stu-id="0b521-105">The example defines a custom method called `changeCol`, which passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.GridLengthConverter> that converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Windows.GridLength>.</span></span> <span data-ttu-id="0b521-106">Der konvertierte Wert wird dann als Wert der- <xref:System.Windows.Controls.ColumnDefinition.Width%2A> Eigenschaft des-Elements zurückgegeben <xref:System.Windows.Controls.ColumnDefinition> .</span><span class="sxs-lookup"><span data-stu-id="0b521-106">The converted value is then passed back as the value of the <xref:System.Windows.Controls.ColumnDefinition.Width%2A> property of the <xref:System.Windows.Controls.ColumnDefinition> element.</span></span>  
  
 <span data-ttu-id="0b521-107">Das Beispiel definiert auch eine zweite benutzerdefinierte Methode mit dem Namen `changeColVal` .</span><span class="sxs-lookup"><span data-stu-id="0b521-107">The example also defines a second custom method, called `changeColVal`.</span></span> <span data-ttu-id="0b521-108">Diese benutzerdefinierte Methode konvertiert den einer <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> <xref:System.Windows.Controls.Slider> in einen <xref:System.String> und übergibt diesen Wert dann wieder an den <xref:System.Windows.Controls.ColumnDefinition> als <xref:System.Windows.Controls.ColumnDefinition.Width%2A> des-Elements.</span><span class="sxs-lookup"><span data-stu-id="0b521-108">This custom method converts the <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> of a <xref:System.Windows.Controls.Slider> to a <xref:System.String> and then passes that value back to the <xref:System.Windows.Controls.ColumnDefinition> as the <xref:System.Windows.Controls.ColumnDefinition.Width%2A> of the element.</span></span>  
  
 <span data-ttu-id="0b521-109">Beachten Sie, dass eine separate [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Datei den Inhalt eines <xref:System.Windows.Controls.ListBoxItem> definiert.</span><span class="sxs-lookup"><span data-stu-id="0b521-109">Note that a separate [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] file defines the contents of a <xref:System.Windows.Controls.ListBoxItem>.</span></span>  
  
 [!code-csharp[gridlengthConverterGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/gridlengthConverterGrid/CSharp/Window1.xaml.cs#1)]
 [!code-vb[gridlengthConverterGrid#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/gridlengthConverterGrid/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="0b521-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b521-110">See also</span></span>

- <xref:System.Windows.GridLengthConverter>
- <xref:System.Windows.GridLength>
