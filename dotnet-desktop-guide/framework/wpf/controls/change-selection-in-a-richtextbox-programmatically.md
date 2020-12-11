---
title: Programmgesteuertes Ändern der Auswahl in einem RichTextBox-Element
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- changing selections in a text box [WPF]
- changing selections in a RichTextBox [WPF]
ms.assetid: f1213205-1ad7-4cd2-b115-460173cc5aa3
ms.openlocfilehash: e3c76bd244e567857ebf132db5cc19c2d51139bd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977355"
---
# <a name="change-selection-in-a-richtextbox-programmatically"></a><span data-ttu-id="22c7c-102">Programmgesteuertes Ändern der Auswahl in einem RichTextBox-Element</span><span class="sxs-lookup"><span data-stu-id="22c7c-102">Change Selection in a RichTextBox Programmatically</span></span>
<span data-ttu-id="22c7c-103">Dieses Beispiel zeigt, wie Sie die aktuelle Auswahl in einer Programm gesteuert ändern können <xref:System.Windows.Controls.RichTextBox> .</span><span class="sxs-lookup"><span data-stu-id="22c7c-103">This example shows how to programmatically change the current selection in a <xref:System.Windows.Controls.RichTextBox>.</span></span> <span data-ttu-id="22c7c-104">Diese Auswahl ist identisch mit der Option, wenn der Benutzer den Inhalt mithilfe der Benutzeroberfläche ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="22c7c-104">This selection is the same as if the user had selected the content by using the user interface.</span></span>  
  
## <a name="example"></a><span data-ttu-id="22c7c-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="22c7c-105">Example</span></span>  
 <span data-ttu-id="22c7c-106">Der folgende [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Code beschreibt ein benanntes <xref:System.Windows.Controls.RichTextBox> Steuerelement mit einfachem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="22c7c-106">The following [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] code describes a named <xref:System.Windows.Controls.RichTextBox> control with simple content.</span></span>  
  
 [!code-xaml[RichTextBoxMiscSnippets_snip#ChangeSelectionProgrammaticalyExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxMiscSnippets_snip/CSharp/ChangeSelectionProgrammaticaly.xaml#changeselectionprogrammaticalyexamplewholepage)]  
  
## <a name="example"></a><span data-ttu-id="22c7c-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="22c7c-107">Example</span></span>  
 <span data-ttu-id="22c7c-108">Mit dem folgenden Code wird ein beliebiger Textprogramm gesteuert ausgewählt, wenn der Benutzer in den klickt <xref:System.Windows.Controls.RichTextBox> .</span><span class="sxs-lookup"><span data-stu-id="22c7c-108">The following code programmatically selects some arbitrary text when the user clicks inside the <xref:System.Windows.Controls.RichTextBox>.</span></span>  
  
 [!code-csharp[RichTextBoxMiscSnippets_snip#ChangeSelectionProgrammaticalyCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxMiscSnippets_snip/CSharp/ChangeSelectionProgrammaticaly.xaml.cs#changeselectionprogrammaticalycodeexamplewholepage)]
 [!code-vb[RichTextBoxMiscSnippets_snip#ChangeSelectionProgrammaticalyCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBoxMiscSnippets_snip/VisualBasic/ChangeSelectionProgrammaticaly.xaml.vb#changeselectionprogrammaticalycodeexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="22c7c-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22c7c-109">See also</span></span>

- [<span data-ttu-id="22c7c-110">Übersicht über RichTextBox</span><span class="sxs-lookup"><span data-stu-id="22c7c-110">RichTextBox Overview</span></span>](richtextbox-overview.md)
- [<span data-ttu-id="22c7c-111">Übersicht über TextBox</span><span class="sxs-lookup"><span data-stu-id="22c7c-111">TextBox Overview</span></span>](textbox-overview.md)
