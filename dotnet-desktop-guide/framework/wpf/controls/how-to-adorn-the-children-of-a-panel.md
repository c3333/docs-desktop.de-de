---
title: 'Gewusst wie: Verzieren der untergeordneten Elemente eines Bereichs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], binding to children of Panels
- Panel control [WPF], binding adorners to children
ms.assetid: 4cc9b972-b472-4e5c-bdf3-3702d7fbb1f5
ms.openlocfilehash: 4c5ac537bfd68e9c43583758047b2ec378d0bb57
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977040"
---
# <a name="how-to-adorn-the-children-of-a-panel"></a><span data-ttu-id="46e2b-102">Gewusst wie: Verzieren der untergeordneten Elemente eines Bereichs</span><span class="sxs-lookup"><span data-stu-id="46e2b-102">How to: Adorn the Children of a Panel</span></span>
<span data-ttu-id="46e2b-103">In diesem Beispiel wird gezeigt, wie ein Funktions Indikator Programm gesteuert an die untergeordneten Elemente eines angegebenen gebunden wird <xref:System.Windows.Controls.Panel> .</span><span class="sxs-lookup"><span data-stu-id="46e2b-103">This example shows how to programmatically bind an adorner to the children of a specified <xref:System.Windows.Controls.Panel>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="46e2b-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="46e2b-104">Example</span></span>  
 <span data-ttu-id="46e2b-105">Führen Sie die folgenden Schritte aus, um einen Funktions Indikator an die untergeordneten Elemente eines zu binden <xref:System.Windows.Controls.Panel> :</span><span class="sxs-lookup"><span data-stu-id="46e2b-105">To bind an adorner to the children of a <xref:System.Windows.Controls.Panel>, follow these steps:</span></span>  
  
1. <span data-ttu-id="46e2b-106">Deklarieren Sie ein neues <xref:System.Windows.Documents.AdornerLayer> -Objekt, und rufen Sie die- `static` <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> Methode auf, um eine Adornerebene für das Element zu finden, dessen untergeordnete Elemente geschmückt werden</span><span class="sxs-lookup"><span data-stu-id="46e2b-106">Declare a new <xref:System.Windows.Documents.AdornerLayer> object and call the `static`<xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> method to find an adorner layer for the element whose children are to be adorned.</span></span>  
  
2. <span data-ttu-id="46e2b-107">Listet die untergeordneten Elemente des übergeordneten Elements auf und ruft die- <xref:System.Windows.Documents.AdornerLayer.Add%2A> Methode auf, um einen Funktions Indikator an jedes untergeordnete Element zu binden.</span><span class="sxs-lookup"><span data-stu-id="46e2b-107">Enumerate through the children of the parent element and call the <xref:System.Windows.Documents.AdornerLayer.Add%2A> method to bind an adorner to each child element.</span></span>  
  
 <span data-ttu-id="46e2b-108">Im folgenden Beispiel wird ein SimpleCircleAdorner (siehe oben) an die untergeordneten Elemente eines <xref:System.Windows.Controls.StackPanel> namens *myStackPanel* gebunden.</span><span class="sxs-lookup"><span data-stu-id="46e2b-108">The following example binds a SimpleCircleAdorner (shown above) to the children of a <xref:System.Windows.Controls.StackPanel> named *myStackPanel*.</span></span>  
  
 [!code-csharp[Adorners_SimpleCircleAdorner#_AdornChildren](~/samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_adornchildren)]
 [!code-vb[Adorners_SimpleCircleAdorner#_AdornChildren](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_adornchildren)]  
  
> [!NOTE]
> <span data-ttu-id="46e2b-109">Das Binden von Adornern an andere Elemente mit [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46e2b-109">Using [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] to bind an adorner to another element is currently not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46e2b-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46e2b-110">See also</span></span>

- [<span data-ttu-id="46e2b-111">Übersicht über Adorner</span><span class="sxs-lookup"><span data-stu-id="46e2b-111">Adorners Overview</span></span>](adorners-overview.md)
