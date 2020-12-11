---
title: 'Gewusst wie: Positionieren von untergeordneten Elementen mithilfe der angefügten Eigenschaften von Canvas'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- attached properties [WPF Designer]
- Canvas control [WPF], attached properties
ms.assetid: 48f1d25d-3820-4107-a4cc-d6c1e5664a44
ms.openlocfilehash: 347c8502bd4c5fafcde7a142327f85bfb75b9954
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974656"
---
# <a name="how-to-use-the-attached-properties-of-canvas-to-position-child-elements"></a><span data-ttu-id="8209a-102">Gewusst wie: Positionieren von untergeordneten Elementen mithilfe der angefügten Eigenschaften von Canvas</span><span class="sxs-lookup"><span data-stu-id="8209a-102">How to: Use the Attached Properties of Canvas to Position Child Elements</span></span>
<span data-ttu-id="8209a-103">In diesem Beispiel wird gezeigt, wie die angefügten Eigenschaften von verwendet werden <xref:System.Windows.Controls.Canvas> , um untergeordnete Elemente zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="8209a-103">This example shows how to use the attached properties of <xref:System.Windows.Controls.Canvas> to position child elements.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8209a-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8209a-104">Example</span></span>  
 <span data-ttu-id="8209a-105">Im folgenden Beispiel werden vier- <xref:System.Windows.Controls.Button> Elemente als untergeordnete Elemente eines übergeordneten Elements hinzugefügt <xref:System.Windows.Controls.Canvas> .</span><span class="sxs-lookup"><span data-stu-id="8209a-105">The following example adds four <xref:System.Windows.Controls.Button> elements as child elements of a parent <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="8209a-106">Jedes Element wird durch <xref:System.Windows.Controls.Canvas.Bottom%2A> , <xref:System.Windows.Controls.Canvas.Left%2A> , und dargestellt <xref:System.Windows.Controls.Canvas.Right%2A> <xref:System.Windows.Controls.Canvas.Top%2A> .</span><span class="sxs-lookup"><span data-stu-id="8209a-106">Each element is represented by a <xref:System.Windows.Controls.Canvas.Bottom%2A>, <xref:System.Windows.Controls.Canvas.Left%2A>, <xref:System.Windows.Controls.Canvas.Right%2A>, and <xref:System.Windows.Controls.Canvas.Top%2A>.</span></span>
<span data-ttu-id="8209a-107">Beide werden <xref:System.Windows.Controls.Button> relativ zum übergeordneten Element <xref:System.Windows.Controls.Canvas> und entsprechend dem zugewiesenen Eigenschafts Wert positioniert.</span><span class="sxs-lookup"><span data-stu-id="8209a-107">Each <xref:System.Windows.Controls.Button> is positioned relative to the parent <xref:System.Windows.Controls.Canvas> and according to its assigned property value.</span></span>  
  
 [!code-cpp[CanvasAttachedProperties#1](~/samples/snippets/cpp/VS_Snippets_Wpf/CanvasAttachedProperties/CPP/CanvasAttachedProps.cpp#1)]
 [!code-csharp[CanvasAttachedProperties#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasAttachedProperties/CSharp/CanvasAttachedProps.cs#1)]
 [!code-vb[CanvasAttachedProperties#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasAttachedProperties/VisualBasic/CanvasAttachedProps.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="8209a-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8209a-108">See also</span></span>

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.Canvas.Bottom%2A>
- <xref:System.Windows.Controls.Canvas.Left%2A>
- <xref:System.Windows.Controls.Canvas.Right%2A>
- <xref:System.Windows.Controls.Canvas.Top%2A>
- <xref:System.Windows.Controls.Button>
- [<span data-ttu-id="8209a-109">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="8209a-109">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="8209a-110">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="8209a-110">How-to Topics</span></span>](canvas-how-to-topics.md)
- [<span data-ttu-id="8209a-111">Übersicht über angefügte Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8209a-111">Attached Properties Overview</span></span>](../advanced/attached-properties-overview.md)
