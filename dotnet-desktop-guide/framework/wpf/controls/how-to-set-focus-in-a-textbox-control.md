---
title: 'Gewusst wie: Setzen des Fokus in einem TextBox-Steuerelement'
description: Erfahren Sie, wie Sie die Fokus Methode verwenden, um den Fokus auf ein Windows Presentation Foundation TextBox-Steuerelement festzulegen.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- focus [WPF], setting
- TextBox control [WPF], setting focus
ms.assetid: 24b61b45-dc2d-425e-9839-b017af7ab86f
ms.openlocfilehash: e4c6a174ba0353b89225d2337f138f9feeac947c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976878"
---
# <a name="how-to-set-focus-in-a-textbox-control"></a><span data-ttu-id="ad37e-103">Gewusst wie: Setzen des Fokus in einem TextBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ad37e-103">How to: Set Focus in a TextBox Control</span></span>
<span data-ttu-id="ad37e-104">Dieses Beispiel zeigt, wie die- <xref:System.Windows.UIElement.Focus%2A> Methode verwendet wird, um den Fokus auf ein-Steuerelement festzulegen <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="ad37e-104">This example shows how to use the <xref:System.Windows.UIElement.Focus%2A> method to set focus on a <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ad37e-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ad37e-105">Example</span></span>  
 <span data-ttu-id="ad37e-106">Im folgenden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispiel wird ein einfaches Steuerelement mit dem <xref:System.Windows.Controls.TextBox> Namen " *tbfocus Me* " beschrieben</span><span class="sxs-lookup"><span data-stu-id="ad37e-106">The following [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] example describes a simple <xref:System.Windows.Controls.TextBox> control named *tbFocusMe*</span></span>  
  
 [!code-xaml[TextBox_MiscCode#_TextBoxFocusXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_textboxfocusxaml)]  
  
## <a name="example"></a><span data-ttu-id="ad37e-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ad37e-107">Example</span></span>  
 <span data-ttu-id="ad37e-108">Im folgenden Beispiel wird die- <xref:System.Windows.UIElement.Focus%2A> Methode aufgerufen, um den Fokus auf das- <xref:System.Windows.Controls.TextBox> Steuerelement mit dem Namen " *tbfocus Me*" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ad37e-108">The following example calls the <xref:System.Windows.UIElement.Focus%2A> method to set the focus on the <xref:System.Windows.Controls.TextBox> control with the Name *tbFocusMe*.</span></span>  
  
 [!code-csharp[TextBox_MiscCode#_FocusTextBox](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_focustextbox)]
 [!code-vb[TextBox_MiscCode#_FocusTextBox](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_focustextbox)]  
  
## <a name="see-also"></a><span data-ttu-id="ad37e-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad37e-109">See also</span></span>

- <xref:System.Windows.UIElement.Focusable%2A>
- <xref:System.Windows.UIElement.IsFocused%2A>
- [<span data-ttu-id="ad37e-110">Übersicht über TextBox</span><span class="sxs-lookup"><span data-stu-id="ad37e-110">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="ad37e-111">Übersicht über RichTextBox</span><span class="sxs-lookup"><span data-stu-id="ad37e-111">RichTextBox Overview</span></span>](richtextbox-overview.md)
