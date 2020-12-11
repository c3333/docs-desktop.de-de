---
title: 'Vorgehensweise: Implementieren einer benutzerdefinierten Layout-Engine'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- layout engines [Windows Forms], custom
- TableLayoutPanel control [Windows Forms], layout engine
- layout engines [Windows Forms], implementing
- FlowLayoutPanel control [Windows Forms], layout engine
ms.assetid: f91aa91c-29f4-4089-95ca-5d48b774b00e
ms.openlocfilehash: 8e5043e2b42b1e7449c6dab51691b6d57e28cd53
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976481"
---
# <a name="how-to-implement-a-custom-layout-engine"></a><span data-ttu-id="3c69c-102">Vorgehensweise: Implementieren einer benutzerdefinierten Layout-Engine</span><span class="sxs-lookup"><span data-stu-id="3c69c-102">How to: Implement a Custom Layout Engine</span></span>
<span data-ttu-id="3c69c-103">Im folgenden Codebeispiel wird veranschaulicht, wie eine benutzerdefinierte LayoutEngine erstellt wird, die ein einfaches Fluss Layout ausführt.</span><span class="sxs-lookup"><span data-stu-id="3c69c-103">The following code example demonstrates how to create a custom layout engine that performs a simple flow layout.</span></span> <span data-ttu-id="3c69c-104">Es implementiert ein Panel-Steuerelement mit dem Namen `DemoFlowPanel` , das die-Eigenschaft überschreibt, <xref:System.Windows.Forms.Control.LayoutEngine%2A> um eine Instanz der-Klasse bereitzustellen `DemoFlowLayout` .</span><span class="sxs-lookup"><span data-stu-id="3c69c-104">It implements a panel control named `DemoFlowPanel`, which overrides the <xref:System.Windows.Forms.Control.LayoutEngine%2A> property to provide an instance of the `DemoFlowLayout` class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3c69c-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3c69c-105">Example</span></span>  
 [!code-cpp[System.Windows.Forms.Layout.LayoutEngine#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.Layout.LayoutEngine/cpp/DemoFlowLayout.cpp#1)]
 [!code-csharp[System.Windows.Forms.Layout.LayoutEngine#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Layout.LayoutEngine/CS/DemoFlowLayout.cs#1)]
 [!code-vb[System.Windows.Forms.Layout.LayoutEngine#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Layout.LayoutEngine/VB/DemoFlowLayout.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="3c69c-106">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c69c-106">See also</span></span>

- <xref:System.Windows.Forms.Layout.LayoutEngine>
- <xref:System.Windows.Forms.Control.LayoutEngine%2A?displayProperty=nameWithType>
