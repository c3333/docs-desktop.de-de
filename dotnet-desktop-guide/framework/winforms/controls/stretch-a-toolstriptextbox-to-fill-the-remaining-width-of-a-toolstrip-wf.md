---
title: 'Vorgehensweise: Strecken einer ToolStripTextBox zum Ausfüllen der verbleibenden Breite eines ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text boxes [Windows Forms], stretching in ToolStrip control [Windows Forms]
- ToolStrip control [Windows Forms], stretching a text box
ms.assetid: 0e610fbf-85fe-414c-900c-9704a5dd5cc6
ms.openlocfilehash: c60cc2a377f08a73159f25b2ab5f2812d41f0c10
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976455"
---
# <a name="how-to-stretch-a-toolstriptextbox-to-fill-the-remaining-width-of-a-toolstrip-windows-forms"></a><span data-ttu-id="dc5c2-102">Gewusst wie: Strecken einer ToolStripTextBox zum Ausfüllen der verbleibenden Breite eines ToolStrip (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="dc5c2-102">How to: Stretch a ToolStripTextBox to Fill the Remaining Width of a ToolStrip (Windows Forms)</span></span>
<span data-ttu-id="dc5c2-103">Wenn Sie die- <xref:System.Windows.Forms.ToolStrip.Stretch%2A> Eigenschaft eines- <xref:System.Windows.Forms.ToolStrip> Steuer Elements auf festlegen `true` , füllt das-Steuerelement seinen Container von End-to-End und ändert seine Größe, wenn die Größe des Containers geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dc5c2-103">When you set the <xref:System.Windows.Forms.ToolStrip.Stretch%2A> property of a <xref:System.Windows.Forms.ToolStrip> control to `true`, the control fills its container from end to end, and resizes when its container resizes.</span></span> <span data-ttu-id="dc5c2-104">In dieser Konfiguration ist es möglicherweise sinnvoll, ein Element im-Steuerelement, z. b. <xref:System.Windows.Forms.ToolStripTextBox> , zu Strecken, um den verfügbaren Platz auszufüllen und die Größe zu ändern, wenn die Größe des Steuer Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dc5c2-104">In this configuration, you may find it useful to stretch an item in the control, such as a <xref:System.Windows.Forms.ToolStripTextBox>, to fill the available space and to resize when the control resizes.</span></span> <span data-ttu-id="dc5c2-105">Diese Streckung ist beispielsweise nützlich, wenn Sie aussehen und Verhalten ähnlich der Adressleiste in Microsoft® Internet Explorer erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="dc5c2-105">This stretching is useful, for example, if you want to achieve appearance and behavior similar to the address bar in Microsoft® Internet Explorer.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dc5c2-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dc5c2-106">Example</span></span>  
 <span data-ttu-id="dc5c2-107">Das folgende Codebeispiel stellt eine von <xref:System.Windows.Forms.ToolStripTextBox> aufgeleitete Klasse bereit `ToolStripSpringTextBox` .</span><span class="sxs-lookup"><span data-stu-id="dc5c2-107">The following code example provides a class derived from <xref:System.Windows.Forms.ToolStripTextBox> called `ToolStripSpringTextBox`.</span></span> <span data-ttu-id="dc5c2-108">Diese Klasse überschreibt die- <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A> Methode, um die verfügbare Breite des übergeordneten Steuer Elements zu berechnen, <xref:System.Windows.Forms.ToolStrip> nachdem die kombinierte Breite aller anderen Elemente subtrahiert wurde.</span><span class="sxs-lookup"><span data-stu-id="dc5c2-108">This class overrides the <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A> method to calculate the available width of the parent <xref:System.Windows.Forms.ToolStrip> control after the combined width of all other items has been subtracted.</span></span> <span data-ttu-id="dc5c2-109">Dieses Codebeispiel stellt außerdem eine <xref:System.Windows.Forms.Form> -Klasse und eine- `Program` Klasse bereit, um das neue Verhalten zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="dc5c2-109">This code example also provides a <xref:System.Windows.Forms.Form> class and a `Program` class to demonstrate the new behavior.</span></span>  
  
 [!code-csharp[ToolStripSpringTextBox#00](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripSpringTextBox/cs/ToolStripSpringTextBox.cs#00)]
 [!code-vb[ToolStripSpringTextBox#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripSpringTextBox/vb/ToolStripSpringTextBox.vb#00)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="dc5c2-110">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="dc5c2-110">Compiling the Code</span></span>  
 <span data-ttu-id="dc5c2-111">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dc5c2-111">This example requires:</span></span>  
  
- <span data-ttu-id="dc5c2-112">Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="dc5c2-112">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc5c2-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc5c2-113">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.Stretch%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ToolStripTextBox>
- <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A?displayProperty=nameWithType>
- [<span data-ttu-id="dc5c2-114">Architektur des ToolStrip-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="dc5c2-114">ToolStrip Control Architecture</span></span>](toolstrip-control-architecture.md)
- [<span data-ttu-id="dc5c2-115">Vorgehensweise: Interaktive Verwendung der Spring-Eigenschaft in StatusStrip</span><span class="sxs-lookup"><span data-stu-id="dc5c2-115">How to: Use the Spring Property Interactively in a StatusStrip</span></span>](how-to-use-the-spring-property-interactively-in-a-statusstrip.md)
