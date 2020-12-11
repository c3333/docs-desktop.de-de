---
title: 'Gewusst wie: Überschreiben der Panel.OnRender-Methode'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- overriding OnRender method
- Panel control, overriding OnRender method
- OnRender method
- controls, Panel, overriding OnRender method
helpviewer_keywords:
- overriding OnRender method of Panel control [WPF]
- OnRender method [WPF], overriding
- Panel control [WPF], overriding OnRender method
ms.assetid: 57397834-a085-4e36-90ab-416fad98f341
ms.openlocfilehash: 23c3353e130585ed83726816a467ca73f6aa9152
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978161"
---
# <a name="how-to-override-the-panel-onrender-method"></a><span data-ttu-id="d598c-102">Gewusst wie: Überschreiben der Panel.OnRender-Methode</span><span class="sxs-lookup"><span data-stu-id="d598c-102">How to: Override the Panel OnRender Method</span></span>
<span data-ttu-id="d598c-103">In diesem Beispiel wird gezeigt, wie die-Methode von überschrieben wird, um <xref:System.Windows.Controls.Panel.OnRender%2A> <xref:System.Windows.Controls.Panel> einem Layout-Element benutzerdefinierte grafische Effekte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d598c-103">This example shows how to override the <xref:System.Windows.Controls.Panel.OnRender%2A> method of <xref:System.Windows.Controls.Panel> in order to add custom graphical effects to a layout element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d598c-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d598c-104">Example</span></span>  
 <span data-ttu-id="d598c-105">Verwenden Sie die- <xref:System.Windows.Controls.Panel.OnRender%2A> Methode, um einem gerenderten Panel-Element grafische Effekte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d598c-105">Use the <xref:System.Windows.Controls.Panel.OnRender%2A> method in order to add graphical effects to a rendered panel element.</span></span> <span data-ttu-id="d598c-106">Beispielsweise können Sie mit dieser Methode benutzerdefinierte Rahmen-oder Hintergrundeffekte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d598c-106">For example, you can use this method to add custom border or background effects.</span></span> <span data-ttu-id="d598c-107">Ein- <xref:System.Windows.Media.DrawingContext> Objekt wird als Argument übermittelt, das Methoden zum Zeichnen von Formen, Text, Bildern oder Videos bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d598c-107">A <xref:System.Windows.Media.DrawingContext> object is passed as an argument, which provides methods for drawing shapes, text, images, or videos.</span></span> <span data-ttu-id="d598c-108">Folglich ist diese Methode nützlich für die Anpassung eines Panel-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d598c-108">As a result, this method is useful for customization of a panel object.</span></span>  
  
 [!code-csharp[LightWeightCustomPanel#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LightWeightCustomPanel/CSharp/OffsetPanel.cs#1)]
 [!code-vb[LightWeightCustomPanel#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/LightWeightCustomPanel/visualbasic/offsetpanel.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="d598c-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d598c-109">See also</span></span>

- <xref:System.Windows.Controls.Panel>
- [<span data-ttu-id="d598c-110">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="d598c-110">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="d598c-111">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="d598c-111">How-to Topics</span></span>](panel-how-to-topics.md)
