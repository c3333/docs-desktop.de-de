---
title: 'Vorgehensweise: Zeichnen von vertikalem Text in einem Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- StringFormat.FormatFlags
- Graphics.DrawString
helpviewer_keywords:
- text [Windows Forms], drawing vertical
- strings [Windows Forms], drawing vertical
- text [Windows Forms], drawing
- text [Windows Forms], vertical text
ms.assetid: 717a6131-00f6-4373-b574-9894e8317799
ms.openlocfilehash: 660d7abae5463c976e60b7d9caeae8a798d122ca
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975918"
---
# <a name="how-to-draw-vertical-text-on-a-windows-form"></a><span data-ttu-id="7e333-102">Vorgehensweise: Zeichnen von vertikalem Text in einem Windows Form</span><span class="sxs-lookup"><span data-stu-id="7e333-102">How to: Draw Vertical Text on a Windows Form</span></span>
<span data-ttu-id="7e333-103">Im folgenden Codebeispiel wird gezeigt, wie vertikaler Text in einem Formular mithilfe der- <xref:System.Drawing.Graphics.DrawString%2A> Methode von gezeichnet wird <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="7e333-103">The following code example shows how to draw vertical text on a form by using the <xref:System.Drawing.Graphics.DrawString%2A> method of <xref:System.Drawing.Graphics>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7e333-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7e333-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#8](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#8)]
 [!code-csharp[System.Drawing.ConceptualHowTos#8](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#8)]
 [!code-vb[System.Drawing.ConceptualHowTos#8](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#8)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="7e333-105">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="7e333-105">Compiling the Code</span></span>  
 <span data-ttu-id="7e333-106">Diese Methode kann nicht im- <xref:System.Windows.Forms.Form.Load> Ereignishandler aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7e333-106">You cannot call this method in the <xref:System.Windows.Forms.Form.Load> event handler.</span></span> <span data-ttu-id="7e333-107">Der gezeichnete Inhalt wird nicht neu gezeichnet, wenn die Größe des Formulars geändert oder durch ein anderes Formular verdeckt wird.</span><span class="sxs-lookup"><span data-stu-id="7e333-107">The drawn content will not be redrawn if the form is resized or obscured by another form.</span></span> <span data-ttu-id="7e333-108">Damit Ihre Inhalte automatisch neu gezeichnet werden, sollten Sie die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="7e333-108">To make your content automatically repaint, you should override the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="7e333-109">Stabile Programmierung</span><span class="sxs-lookup"><span data-stu-id="7e333-109">Robust Programming</span></span>  
 <span data-ttu-id="7e333-110">Die folgenden Bedingungen können einen Ausnahmefehler verursachen:</span><span class="sxs-lookup"><span data-stu-id="7e333-110">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="7e333-111">Die Schriftart "Arial" ist nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="7e333-111">The Arial font is not installed.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e333-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e333-112">See also</span></span>

- <xref:System.Drawing.Graphics.DrawString%2A>
- <xref:System.Drawing.StringFormat.FormatFlags%2A>
- <xref:System.Drawing.StringFormatFlags>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- [<span data-ttu-id="7e333-113">Erste Schritte mit Grafikprogrammierung</span><span class="sxs-lookup"><span data-stu-id="7e333-113">Getting Started with Graphics Programming</span></span>](getting-started-with-graphics-programming.md)
- [<span data-ttu-id="7e333-114">Verwenden von Schriftarten und Text</span><span class="sxs-lookup"><span data-stu-id="7e333-114">Using Fonts and Text</span></span>](using-fonts-and-text.md)
