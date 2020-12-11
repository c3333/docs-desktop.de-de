---
title: 'Vorgehensweise: Erstellen eines professionellen ToolStrip-Steuerelements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStripRenderer class [Windows Forms]
- ToolStrip control [Windows Forms]
ms.assetid: c208b2f6-8105-474b-9075-d582e1792870
ms.openlocfilehash: 4e4e899d583eb87b3ced7161f1fd274c0bcc591c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976336"
---
# <a name="how-to-create-a-professionally-styled-toolstrip-control"></a><span data-ttu-id="95457-102">Vorgehensweise: Erstellen eines professionellen ToolStrip-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="95457-102">How to: Create a Professionally Styled ToolStrip Control</span></span>
<span data-ttu-id="95457-103">Sie können den <xref:System.Windows.Forms.ToolStrip>-Steuerelementen Ihrer Anwendung ein professionelles Aussehen und Verhalten ("Look and Feel") verleihen, indem Sie eine eigene Klasse schreiben, die vom Typ <xref:System.Windows.Forms.ToolStripProfessionalRenderer> abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="95457-103">You can give your application’s <xref:System.Windows.Forms.ToolStrip> controls a professional appearance and behavior (look and feel) by writing your own class derived from the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> type.</span></span>  
  
 <span data-ttu-id="95457-104">In Visual Studio wird dieses Feature umfassend unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95457-104">There is extensive support for this feature in Visual Studio.</span></span>  
  
 <span data-ttu-id="95457-105">Siehe [Exemplarische Vorgehensweise: Erstellen eines professionellen ToolStrip-Steuerelements](walkthrough-creating-a-professionally-styled-toolstrip-control.md).</span><span class="sxs-lookup"><span data-stu-id="95457-105">See [Walkthrough: Creating a Professionally Styled ToolStrip Control](walkthrough-creating-a-professionally-styled-toolstrip-control.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="95457-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="95457-106">Example</span></span>  
 <span data-ttu-id="95457-107">Im folgenden Codebeispiel wird veranschaulicht, wie <xref:System.Windows.Forms.ToolStrip> Steuerelemente verwendet werden, um ein zusammengesetztes Steuerelement zu erstellen, das den **Navigations** Bereich von Microsoft® Outlook-® imitiert.</span><span class="sxs-lookup"><span data-stu-id="95457-107">The following code example demonstrates how to use <xref:System.Windows.Forms.ToolStrip> controls to create a composite control that mimics the **Navigation Pane** provided by Microsoft® Outlook®.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.StackView#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.StackView#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="95457-108">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="95457-108">Compiling the Code</span></span>  
 <span data-ttu-id="95457-109">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="95457-109">This example requires:</span></span>  
  
- <span data-ttu-id="95457-110">Verweise auf die Assemblys ""System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="95457-110">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95457-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95457-111">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="95457-112">ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="95457-112">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
- [<span data-ttu-id="95457-113">Vorgehensweise: Bereitstellen von Standardmenüelementen für ein Formular</span><span class="sxs-lookup"><span data-stu-id="95457-113">How to: Provide Standard Menu Items to a Form</span></span>](how-to-provide-standard-menu-items-to-a-form.md)
