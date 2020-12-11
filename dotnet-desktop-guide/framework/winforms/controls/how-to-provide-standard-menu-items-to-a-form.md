---
title: 'Vorgehensweise: Bereitstellen von Standardmenüelementen für ein Formular'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- menu items [Windows Forms], standard
- ToolStrip control [Windows Forms]
ms.assetid: 75db9126-e70c-4e81-921d-b83c0a4a9f50
ms.openlocfilehash: a95476ff3d182bf2a56e6527c9ee83c8c56af246
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975608"
---
# <a name="how-to-provide-standard-menu-items-to-a-form"></a><span data-ttu-id="d0417-102">Vorgehensweise: Bereitstellen von Standardmenüelementen für ein Formular</span><span class="sxs-lookup"><span data-stu-id="d0417-102">How to: Provide Standard Menu Items to a Form</span></span>
<span data-ttu-id="d0417-103">Mit dem <xref:System.Windows.Forms.MenuStrip>-Steuerelement können Sie ein Standardmenü für Formulare bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d0417-103">You can provide a standard menu for your forms with the <xref:System.Windows.Forms.MenuStrip> control.</span></span>  
  
 <span data-ttu-id="d0417-104">In Visual Studio wird dieses Feature umfassend unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0417-104">There is extensive support for this feature in Visual Studio.</span></span>  
  
 <span data-ttu-id="d0417-105">Siehe auch [Exemplarische Vorgehensweise: Bereitstellen von Standardmenüelementen für ein Formular](walkthrough-providing-standard-menu-items-to-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="d0417-105">Also see [Walkthrough: Providing Standard Menu Items to a Form](walkthrough-providing-standard-menu-items-to-a-form.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d0417-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d0417-106">Example</span></span>  
 <span data-ttu-id="d0417-107">Im folgenden Codebeispiel wird veranschaulicht, wie mit dem <xref:System.Windows.Forms.MenuStrip>-Steuerelement ein Formular mit Standardmenü erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d0417-107">The following code example demonstrates how to use a <xref:System.Windows.Forms.MenuStrip> control to create a form with a standard menu.</span></span> <span data-ttu-id="d0417-108">Menüelementauswahlen werden in einem <xref:System.Windows.Forms.StatusStrip>-Steuerelement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d0417-108">Menu item selections are displayed in a <xref:System.Windows.Forms.StatusStrip> control.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="d0417-109">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="d0417-109">Compiling the Code</span></span>  
 <span data-ttu-id="d0417-110">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d0417-110">This example requires:</span></span>  
  
- <span data-ttu-id="d0417-111">Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="d0417-111">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0417-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0417-112">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="d0417-113">MenuStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d0417-113">MenuStrip Control</span></span>](menustrip-control-windows-forms.md)
