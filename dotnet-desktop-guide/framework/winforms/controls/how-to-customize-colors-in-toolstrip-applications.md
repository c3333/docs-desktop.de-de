---
title: 'Vorgehensweise: Anpassen von Farben in ToolStrip-Anwendungen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], customizing colors
- colors [Windows Forms], customizing in ToolStrip controls [Windows Forms]
- ToolStrip control [Windows Forms], custom colors
ms.assetid: e2752fe2-1afb-489e-ab96-b7805acd96bc
ms.openlocfilehash: 6719156d0ab6d1e53cd0bd8f16f306577589fb40
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975681"
---
# <a name="how-to-customize-colors-in-toolstrip-applications"></a><span data-ttu-id="c15b7-102">Vorgehensweise: Anpassen von Farben in ToolStrip-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c15b7-102">How to: Customize Colors in ToolStrip Applications</span></span>
<span data-ttu-id="c15b7-103">Sie können die Darstellung von <xref:System.Windows.Forms.ToolStrip> mithilfe der <xref:System.Windows.Forms.ToolStripProfessionalRenderer>-Klasse anpassen, um benutzerdefinierte Farben zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c15b7-103">You can customize the appearance of your <xref:System.Windows.Forms.ToolStrip> by using the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> class to use customized colors.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c15b7-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c15b7-104">Example</span></span>  
 <span data-ttu-id="c15b7-105">Das folgende Codebeispiel zeigt, wie Sie <xref:System.Windows.Forms.ToolStripProfessionalRenderer> zum Definieren benutzerdefinierter Farben zur Laufzeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="c15b7-105">The following code example demonstrates how to use a <xref:System.Windows.Forms.ToolStripProfessionalRenderer> to define custom colors at run time.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#20)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#20)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c15b7-106">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="c15b7-106">Compiling the Code</span></span>  
 <span data-ttu-id="c15b7-107">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c15b7-107">This example requires:</span></span>  
  
- <span data-ttu-id="c15b7-108">Verweise auf die Assemblys "System.Design", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="c15b7-108">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c15b7-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c15b7-109">See also</span></span>

- <xref:System.Windows.Forms.ToolStripManager>
- <xref:System.Windows.Forms.ProfessionalColorTable>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripProfessionalRenderer>
