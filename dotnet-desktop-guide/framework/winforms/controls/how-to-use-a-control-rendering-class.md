---
title: 'Vorgehensweise: Verwenden einer Steuerelementwiedergabeklasse'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- professional appearance [Windows Forms], rendering Windows Forms controls
- visual themes [Windows Forms], applying to Windows Forms controls
- visual styles [Windows Forms], rendering Windows Forms controls
ms.assetid: c0125e34-cd74-4c35-818c-3e40f462b0a3
ms.openlocfilehash: a0f450ff5f169026007002a0d2907ee35e79b29d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976637"
---
# <a name="how-to-use-a-control-rendering-class"></a><span data-ttu-id="c670b-102">Vorgehensweise: Verwenden einer Steuerelementwiedergabeklasse</span><span class="sxs-lookup"><span data-stu-id="c670b-102">How to: Use a Control Rendering Class</span></span>
<span data-ttu-id="c670b-103">In diesem Beispiel wird veranschaulicht, wie die <xref:System.Windows.Forms.ComboBoxRenderer> -Klasse zum Rendering des Dropdown Pfeils eines Kombinations Feld-Steuer Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c670b-103">This example demonstrates how to use the <xref:System.Windows.Forms.ComboBoxRenderer> class to render the drop-down arrow of a combo box control.</span></span> <span data-ttu-id="c670b-104">Das Beispiel besteht aus der- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode eines einfachen benutzerdefinierten Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c670b-104">The example consists of the <xref:System.Windows.Forms.Control.OnPaint%2A> method of a simple custom control.</span></span> <span data-ttu-id="c670b-105">Die- <xref:System.Windows.Forms.ComboBoxRenderer.IsSupported%2A?displayProperty=nameWithType> Eigenschaft wird verwendet, um zu bestimmen, ob visuelle Stile im Client Bereich von Anwendungs Fenstern aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c670b-105">The <xref:System.Windows.Forms.ComboBoxRenderer.IsSupported%2A?displayProperty=nameWithType> property is used to determine whether visual styles are enabled in the client area of application windows.</span></span> <span data-ttu-id="c670b-106">Wenn visuelle Stile aktiviert sind, wird der <xref:System.Windows.Forms.ComboBoxRenderer.DrawDropDownButton%2A?displayProperty=nameWithType> Dropdown Pfeil von der Methode mit visuellen Stilen dargestellt <xref:System.Windows.Forms.ControlPaint.DrawComboButton%2A?displayProperty=nameWithType> . andernfalls wird die Methode den Dropdown Pfeil im klassischen Windows-Stil Rendering.</span><span class="sxs-lookup"><span data-stu-id="c670b-106">If visual styles are active, then the <xref:System.Windows.Forms.ComboBoxRenderer.DrawDropDownButton%2A?displayProperty=nameWithType> method will render the drop-down arrow with visual styles; otherwise, the <xref:System.Windows.Forms.ControlPaint.DrawComboButton%2A?displayProperty=nameWithType> method will render the drop-down arrow in the classic Windows style.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c670b-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c670b-107">Example</span></span>  
 [!code-cpp[System.Windows.Forms_ControlRenderer#10](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/cpp/form1.cpp#10)]
 [!code-csharp[System.Windows.Forms_ControlRenderer#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/CS/form1.cs#10)]
 [!code-vb[System.Windows.Forms_ControlRenderer#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/VB/form1.vb#10)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c670b-108">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="c670b-108">Compiling the Code</span></span>  
 <span data-ttu-id="c670b-109">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c670b-109">This example requires:</span></span>  
  
- <span data-ttu-id="c670b-110">Ein benutzerdefiniertes, von der-Klasse abgeleitetes <xref:System.Windows.Forms.Control></span><span class="sxs-lookup"><span data-stu-id="c670b-110">A custom control derived from the <xref:System.Windows.Forms.Control> class.</span></span>  
  
- <span data-ttu-id="c670b-111">Ein <xref:System.Windows.Forms.Form> , der das benutzerdefinierte Steuerelement hostet.</span><span class="sxs-lookup"><span data-stu-id="c670b-111">A <xref:System.Windows.Forms.Form> that hosts the custom control.</span></span>  
  
- <span data-ttu-id="c670b-112">Verweise auf die <xref:System?displayProperty=nameWithType> <xref:System.Drawing?displayProperty=nameWithType> <xref:System.Windows.Forms?displayProperty=nameWithType> <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> Namespaces,, und.</span><span class="sxs-lookup"><span data-stu-id="c670b-112">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, and <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> namespaces.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c670b-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c670b-113">See also</span></span>

- [<span data-ttu-id="c670b-114">Rendering von Steuerelementen mit visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="c670b-114">Rendering Controls with Visual Styles</span></span>](rendering-controls-with-visual-styles.md)
