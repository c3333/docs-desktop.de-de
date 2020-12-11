---
title: 'Gewusst wie: Erstellen eines benutzerdefinierten Bereichselements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Panel control [WPF]
- custom Panel elements [WPF]
ms.assetid: e0df4f1e-8c07-4e86-89a3-e22acfffdc2a
ms.openlocfilehash: 31edc75114c5dad613e5b65e7d8b051e2c3713af
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978074"
---
# <a name="how-to-create-a-custom-panel-element"></a><span data-ttu-id="17b68-102">Gewusst wie: Erstellen eines benutzerdefinierten Bereichselements</span><span class="sxs-lookup"><span data-stu-id="17b68-102">How to: Create a Custom Panel Element</span></span>
## <a name="example"></a><span data-ttu-id="17b68-103">Beispiel</span><span class="sxs-lookup"><span data-stu-id="17b68-103">Example</span></span>  
 <span data-ttu-id="17b68-104">In diesem Beispiel wird gezeigt, wie das Standardlayoutverhalten des <xref:System.Windows.Controls.Panel> -Elements überschrieben und benutzerdefinierte Layoutelemente erstellt werden, die von abgeleitet werden <xref:System.Windows.Controls.Panel> .</span><span class="sxs-lookup"><span data-stu-id="17b68-104">This example shows how to override the default layout behavior of the <xref:System.Windows.Controls.Panel> element and create custom layout elements that are derived from <xref:System.Windows.Controls.Panel>.</span></span>  
  
 <span data-ttu-id="17b68-105">Im Beispiel wird ein einfaches benutzerdefiniertes <xref:System.Windows.Controls.Panel> Element namens definiert `PlotPanel` , das untergeordnete Elemente nach zwei hart codierten x-und y-Koordinaten positioniert.</span><span class="sxs-lookup"><span data-stu-id="17b68-105">The example defines a simple custom <xref:System.Windows.Controls.Panel> element called `PlotPanel`, which positions child elements according to two hard-coded x- and y-coordinates.</span></span> <span data-ttu-id="17b68-106">In diesem Beispiel `x` sind und auf `y` festgelegt `50` . Daher werden alle untergeordneten Elemente an dieser Stelle auf der x-und der y-Achse positioniert.</span><span class="sxs-lookup"><span data-stu-id="17b68-106">In this example, `x` and `y` are both set to `50`; therefore, all child elements are positioned at that location on the x and y axes.</span></span>  
  
 <span data-ttu-id="17b68-107">Zum Implementieren von benutzerdefiniertem <xref:System.Windows.Controls.Panel> Verhalten verwendet das Beispiel die <xref:System.Windows.FrameworkElement.MeasureOverride%2A> -Methode und die- <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="17b68-107">To implement custom <xref:System.Windows.Controls.Panel> behaviors, the example uses the <xref:System.Windows.FrameworkElement.MeasureOverride%2A> and <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> methods.</span></span> <span data-ttu-id="17b68-108">Jede Methode gibt die <xref:System.Windows.Size> Daten zurück, die erforderlich sind, um untergeordnete Elemente zu positionieren und zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="17b68-108">Each method returns the <xref:System.Windows.Size> data that is necessary to position and render child elements.</span></span>  
  
 [!code-cpp[PlotPanel#1](~/samples/snippets/cpp/VS_Snippets_Wpf/PlotPanel/CPP/PlotPanel.cpp#1)]
 [!code-csharp[PlotPanel#1](~/samples/snippets/csharp/VS_Snippets_Wpf/PlotPanel/CSharp/PlotPanel.cs#1)]
 [!code-vb[PlotPanel#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PlotPanel/VisualBasic/PlotPanel.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="17b68-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17b68-109">See also</span></span>

- <xref:System.Windows.Controls.Panel>
- [<span data-ttu-id="17b68-110">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="17b68-110">Panels Overview</span></span>](panels-overview.md)
