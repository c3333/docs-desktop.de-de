---
title: 'Gewusst wie: Positionieren des Cursors am Anfang oder Ende von Text in einem "TextBox"-Steuerelement'
description: Erfahren Sie, wie Sie den Cursor am Anfang oder Ende des Text Inhalts eines Windows Presentation Foundation TextBox-Steuer Elements positionieren.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- positioning cursor [WPF]
- TextBox control [WPF], positioning cursor
- cursor [WPF], positioning
ms.assetid: c771a0b8-c6b4-4240-aecd-a21d0ba51a2e
ms.openlocfilehash: 32a738c37bac07e660fe84e3707ba4352594928a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977700"
---
# <a name="how-to-position-the-cursor-at-the-beginning-or-end-of-text-in-a-textbox-control"></a><span data-ttu-id="2b920-103">Gewusst wie: Positionieren des Cursors am Anfang oder Ende von Text in einem "TextBox"-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="2b920-103">How to: Position the Cursor at the Beginning or End of Text in a TextBox Control</span></span>
<span data-ttu-id="2b920-104">In diesem Beispiel wird gezeigt, wie der Cursor am Anfang oder Ende des Text Inhalts eines-Steuer Elements positioniert wird <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="2b920-104">This example shows how to position the cursor at the beginning or end of the text contents of a <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2b920-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2b920-105">Example</span></span>  
 <span data-ttu-id="2b920-106">Der folgende [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Code beschreibt ein <xref:System.Windows.Controls.TextBox> -Steuerelement und weist ihm einen Namen zu.</span><span class="sxs-lookup"><span data-stu-id="2b920-106">The following [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] code describes a <xref:System.Windows.Controls.TextBox> control and assigns it a Name.</span></span>  
  
 [!code-xaml[TextBox_MiscCode#_MoveCursorXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_movecursorxaml)]  
  
## <a name="example"></a><span data-ttu-id="2b920-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2b920-107">Example</span></span>  
 <span data-ttu-id="2b920-108">Um den Cursor am Anfang des Inhalts eines-Steuer Elements zu positionieren, müssen Sie <xref:System.Windows.Controls.TextBox> die <xref:System.Windows.Controls.TextBox.Select%2A> -Methode und die Startposition der Auswahl 0 und eine Auswahl Länge von 0 (null) angeben.</span><span class="sxs-lookup"><span data-stu-id="2b920-108">To position the cursor at the beginning of the contents of a <xref:System.Windows.Controls.TextBox> control, call the <xref:System.Windows.Controls.TextBox.Select%2A> method and specify the selection start position of 0, and a selection length of 0.</span></span>  
  
 [!code-csharp[TextBox_MiscCode#_CursorToStart](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_cursortostart)]
 [!code-vb[TextBox_MiscCode#_CursorToStart](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_cursortostart)]  
  
## <a name="example"></a><span data-ttu-id="2b920-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2b920-109">Example</span></span>  
 <span data-ttu-id="2b920-110">Um den Cursor am Ende des Inhalts eines-Steuer Elements zu positionieren, müssen Sie <xref:System.Windows.Controls.TextBox> die <xref:System.Windows.Controls.TextBox.Select%2A> -Methode und die Startposition der Auswahl gleich der Länge des Text Inhalts und eine Auswahl Länge von 0 (null) angeben.</span><span class="sxs-lookup"><span data-stu-id="2b920-110">To position the cursor at the end of the contents of a <xref:System.Windows.Controls.TextBox> control, call the <xref:System.Windows.Controls.TextBox.Select%2A> method and specify the selection start position equal to the  length of the text content, and a selection length of 0.</span></span>  
  
 [!code-csharp[TextBox_MiscCode#_CursorToEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_cursortoend)]
 [!code-vb[TextBox_MiscCode#_CursorToEnd](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_cursortoend)]  
  
## <a name="see-also"></a><span data-ttu-id="2b920-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b920-111">See also</span></span>

- [<span data-ttu-id="2b920-112">Übersicht über TextBox</span><span class="sxs-lookup"><span data-stu-id="2b920-112">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="2b920-113">Übersicht über RichTextBox</span><span class="sxs-lookup"><span data-stu-id="2b920-113">RichTextBox Overview</span></span>](richtextbox-overview.md)
