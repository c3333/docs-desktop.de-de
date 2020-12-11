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
# <a name="how-to-use-a-thicknessconverter-object"></a><span data-ttu-id="88c81-102">Gewusst wie: Verwenden eines ThicknessConverter-Objekts</span><span class="sxs-lookup"><span data-stu-id="88c81-102">How to: Use a ThicknessConverter Object</span></span>

## <a name="example"></a><span data-ttu-id="88c81-103">Beispiel</span><span class="sxs-lookup"><span data-stu-id="88c81-103">Example</span></span>  

 <span data-ttu-id="88c81-104">In diesem Beispiel wird gezeigt, wie eine Instanz von erstellt <xref:System.Windows.ThicknessConverter> und verwendet wird, um die Stärke eines Rahmens zu ändern.</span><span class="sxs-lookup"><span data-stu-id="88c81-104">This example shows how to create an instance of <xref:System.Windows.ThicknessConverter> and use it to change the thickness of a border.</span></span>  
  
 <span data-ttu-id="88c81-105">Im Beispiel wird eine benutzerdefinierte Methode mit dem Namen definiert `changeThickness` . diese Methode konvertiert zuerst den Inhalt einer <xref:System.Windows.Controls.ListBoxItem> , die in einer separaten [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Datei definiert ist, in eine Instanz von <xref:System.Windows.Thickness> und konvertiert den Inhalt später in einen <xref:System.String> .</span><span class="sxs-lookup"><span data-stu-id="88c81-105">The example defines a custom method called `changeThickness`; this method first converts the contents of a <xref:System.Windows.Controls.ListBoxItem>, as defined in a separate [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] file, to an instance of <xref:System.Windows.Thickness>, and later converts the content into a <xref:System.String>.</span></span> <span data-ttu-id="88c81-106">Diese Methode übergibt das <xref:System.Windows.Controls.ListBoxItem> an ein- <xref:System.Windows.ThicknessConverter> Objekt, das den einer <xref:System.Windows.Controls.ContentControl.Content%2A> <xref:System.Windows.Controls.ListBoxItem> in eine Instanz von konvertiert <xref:System.Windows.Thickness> .</span><span class="sxs-lookup"><span data-stu-id="88c81-106">This method passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.ThicknessConverter> object, which converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Windows.Thickness>.</span></span> <span data-ttu-id="88c81-107">Dieser Wert wird dann als Wert der- <xref:System.Windows.Controls.Border.BorderThickness%2A> Eigenschaft von zurückgegeben <xref:System.Windows.Controls.Border> .</span><span class="sxs-lookup"><span data-stu-id="88c81-107">This value is then passed back as the value of the <xref:System.Windows.Controls.Border.BorderThickness%2A> property of the <xref:System.Windows.Controls.Border>.</span></span>  
  
 <span data-ttu-id="88c81-108">Dieses Beispiel wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88c81-108">This example does not run.</span></span>  
  
 [!code-csharp[ThicknessConverter#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ThicknessConverter/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ThicknessConverter#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ThicknessConverter/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="88c81-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88c81-109">See also</span></span>

- <xref:System.Windows.Thickness>
- <xref:System.Windows.ThicknessConverter>
- <xref:System.Windows.Controls.Border>
- <span data-ttu-id="88c81-110">[Vorgehensweise: Ändern der Margin-Eigenschaft](/previous-versions/dotnet/netframework-3.5/ms750561(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="88c81-110">[How to: Change the Margin Property](/previous-versions/dotnet/netframework-3.5/ms750561(v=vs.90))</span></span>
- <span data-ttu-id="88c81-111">[Gewusst wie: Konvertieren eines ListBoxItem in einen neuen Datentyp](/previous-versions/dotnet/netframework-3.5/ms749147(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="88c81-111">[How to: Convert a ListBoxItem to a new Data Type](/previous-versions/dotnet/netframework-3.5/ms749147(v=vs.90))</span></span>
- [<span data-ttu-id="88c81-112">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="88c81-112">Panels Overview</span></span>](../controls/panels-overview.md)
