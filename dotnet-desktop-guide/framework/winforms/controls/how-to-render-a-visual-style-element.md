---
title: 'Vorgehensweise: Rendern eines visuellen Stilelements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- visual themes [Windows Forms], applying to elements of Windows Forms applications
- professional appearance [Windows Forms], applying to elements of Windows Forms applications
- visual styles [Windows Forms], rendering Windows Forms controls
ms.assetid: a207781b-1baa-4ce9-b788-1e951bd4b5df
ms.openlocfilehash: a2b9524b6a3e3c77d3c68c4d9e138b8c0e2a9373
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975602"
---
# <a name="how-to-render-a-visual-style-element"></a><span data-ttu-id="93878-102">Vorgehensweise: Rendern eines visuellen Stilelements</span><span class="sxs-lookup"><span data-stu-id="93878-102">How to: Render a Visual Style Element</span></span>
<span data-ttu-id="93878-103">Der- <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> Namespace macht <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> Objekte verfügbar, die die von visuellen Stilen unterstützten Elemente der Windows-Benutzeroberfläche darstellen.</span><span class="sxs-lookup"><span data-stu-id="93878-103">The <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> namespace exposes <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> objects that represent the Windows user interface (UI) elements supported by visual styles.</span></span> <span data-ttu-id="93878-104">In diesem Thema wird veranschaulicht, wie die <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> -Klasse verwendet wird, um das zu Rendering <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> , das die Schaltflächen abmelden und **herunter** **fahren** im Startmenü darstellt.</span><span class="sxs-lookup"><span data-stu-id="93878-104">This topic demonstrates how to use the <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> class to render the <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> that represents the **Log Off** and **Shut Down** buttons of the Start menu.</span></span>  
  
### <a name="to-render-a-visual-style-element"></a><span data-ttu-id="93878-105">So Rendering Sie ein visuelles Stilelement</span><span class="sxs-lookup"><span data-stu-id="93878-105">To render a visual style element</span></span>  
  
1. <span data-ttu-id="93878-106">Erstellen <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> Sie ein, und legen Sie es auf das zu zeichnende Element fest.</span><span class="sxs-lookup"><span data-stu-id="93878-106">Create a <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> and set it to the element you want to draw.</span></span> <span data-ttu-id="93878-107">Beachten Sie die Verwendung der <xref:System.Windows.Forms.Application.RenderWithVisualStyles%2A?displayProperty=nameWithType> -Eigenschaft und der- <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.IsElementDefined%2A?displayProperty=nameWithType> Methode <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.%23ctor%2A> . der Konstruktor löst eine Ausnahme aus, wenn visuelle Stile deaktiviert sind oder ein Element nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="93878-107">Note the use of the <xref:System.Windows.Forms.Application.RenderWithVisualStyles%2A?displayProperty=nameWithType> property and the <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.IsElementDefined%2A?displayProperty=nameWithType> method; the <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.%23ctor%2A> constructor will throw an exception if visual styles are disabled or an element is undefined.</span></span>  
  
     [!code-cpp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/cpp/form1.cpp#4)]
     [!code-csharp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/CS/form1.cs#4)]
     [!code-vb[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/VB/form1.vb#4)]  
  
2. <span data-ttu-id="93878-108">Ruft die- <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.DrawBackground%2A> Methode auf, um das Element zu Rendering, das das <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> gegenwärtig darstellt.</span><span class="sxs-lookup"><span data-stu-id="93878-108">Call the <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.DrawBackground%2A> method to render the element that the <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> currently represents.</span></span>  
  
     [!code-cpp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/cpp/form1.cpp#6)]
     [!code-csharp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/CS/form1.cs#6)]
     [!code-vb[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/VB/form1.vb#6)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="93878-109">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="93878-109">Compiling the Code</span></span>  
 <span data-ttu-id="93878-110">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="93878-110">This example requires:</span></span>  
  
- <span data-ttu-id="93878-111">Ein benutzerdefiniertes, von der-Klasse abgeleitetes <xref:System.Windows.Forms.Control></span><span class="sxs-lookup"><span data-stu-id="93878-111">A custom control derived from the <xref:System.Windows.Forms.Control> class.</span></span>  
  
- <span data-ttu-id="93878-112">Ein <xref:System.Windows.Forms.Form> , der das benutzerdefinierte Steuerelement hostet.</span><span class="sxs-lookup"><span data-stu-id="93878-112">A <xref:System.Windows.Forms.Form> that hosts the custom control.</span></span>  
  
- <span data-ttu-id="93878-113">Verweise auf die <xref:System?displayProperty=nameWithType> <xref:System.Drawing?displayProperty=nameWithType> <xref:System.Windows.Forms?displayProperty=nameWithType> <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> Namespaces,, und.</span><span class="sxs-lookup"><span data-stu-id="93878-113">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, and <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> namespaces.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93878-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93878-114">See also</span></span>

- [<span data-ttu-id="93878-115">Rendering von Steuerelementen mit visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="93878-115">Rendering Controls with Visual Styles</span></span>](rendering-controls-with-visual-styles.md)
