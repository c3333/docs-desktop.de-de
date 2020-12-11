---
title: 'Gewusst wie: Binden eines Adorners an ein Element'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UIElements [WPF], binding adorners to
- adorners [WPF], binding to specified UIElements
ms.assetid: b2101611-a0ee-4137-bdb8-9b3673d2e6b9
ms.openlocfilehash: 951643602b09a522d23a6449aefa4be41e051a40
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976990"
---
# <a name="how-to-bind-an-adorner-to-an-element"></a><span data-ttu-id="c40d4-102">Gewusst wie: Binden eines Adorners an ein Element</span><span class="sxs-lookup"><span data-stu-id="c40d4-102">How to: Bind an Adorner to an Element</span></span>
<span data-ttu-id="c40d4-103">In diesem Beispiel wird gezeigt, wie ein Funktions Indikator Programm gesteuert an eine angegebene gebunden wird <xref:System.Windows.UIElement> .</span><span class="sxs-lookup"><span data-stu-id="c40d4-103">This example shows how to programmatically bind an adorner to a specified <xref:System.Windows.UIElement>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c40d4-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c40d4-104">Example</span></span>  
 <span data-ttu-id="c40d4-105">Führen Sie die folgenden Schritte aus, um einen Funktions Indikator an einen bestimmten zu binden <xref:System.Windows.UIElement> :</span><span class="sxs-lookup"><span data-stu-id="c40d4-105">To bind an adorner to a particular <xref:System.Windows.UIElement>, follow these steps:</span></span>  
  
1. <span data-ttu-id="c40d4-106">Ruft die- `static` Methode <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> auf, um ein-Objekt zu erhalten, <xref:System.Windows.Documents.AdornerLayer> das <xref:System.Windows.UIElement> zu schmücken ist.</span><span class="sxs-lookup"><span data-stu-id="c40d4-106">Call the `static` method <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> to get an <xref:System.Windows.Documents.AdornerLayer> object for the <xref:System.Windows.UIElement> to be adorned.</span></span> <span data-ttu-id="c40d4-107"><xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> durchläuft die visuelle Struktur, beginnend beim angegebenen **UIElement**, und gibt die erste gefundene Adornerebene zurück.</span><span class="sxs-lookup"><span data-stu-id="c40d4-107"><xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> walks up the visual tree, starting at the specified **UIElement**, and returns the first adorner layer it finds.</span></span> <span data-ttu-id="c40d4-108">(Falls keine Adorner-Ebenen gefunden werden, gibt die Methode NULL zurück.)</span><span class="sxs-lookup"><span data-stu-id="c40d4-108">(If no adorner layers are found, the method returns null.)</span></span>  
  
2. <span data-ttu-id="c40d4-109">Ruft die- <xref:System.Windows.Documents.AdornerLayer.Add%2A> Methode auf, um den Funktions Indikator an das **UIElement**-Ziel zu binden.</span><span class="sxs-lookup"><span data-stu-id="c40d4-109">Call the <xref:System.Windows.Documents.AdornerLayer.Add%2A> method to bind the adorner to the target **UIElement**.</span></span>  
  
 <span data-ttu-id="c40d4-110">Im folgenden Beispiel wird ein SimpleCircleAdorner (siehe oben) an ein <xref:System.Windows.Controls.TextBox> benanntes *MyTextBox*-Element gebunden.</span><span class="sxs-lookup"><span data-stu-id="c40d4-110">The following example binds a SimpleCircleAdorner (shown above) to a <xref:System.Windows.Controls.TextBox> named *myTextBox*.</span></span>  
  
 [!code-csharp[Adorners_SimpleCircleAdorner#_AdornSingleElement](~/samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_adornsingleelement)]
 [!code-vb[Adorners_SimpleCircleAdorner#_AdornSingleElement](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_adornsingleelement)]  
  
> [!NOTE]
> <span data-ttu-id="c40d4-111">Das Binden von Adornern an andere Elemente mit [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c40d4-111">Using [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] to bind an adorner to another element is currently not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c40d4-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c40d4-112">See also</span></span>

- [<span data-ttu-id="c40d4-113">Übersicht über Adorner</span><span class="sxs-lookup"><span data-stu-id="c40d4-113">Adorners Overview</span></span>](adorners-overview.md)
