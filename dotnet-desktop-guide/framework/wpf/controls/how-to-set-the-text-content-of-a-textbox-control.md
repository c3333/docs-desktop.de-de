---
title: 'Gewusst wie: Festlegen des Textinhalts eines TextBox-Steuerelements'
description: Erfahren Sie, wie Sie die Text-Eigenschaft verwenden, um den ursprünglichen Text Inhalt eines Windows Presentation Foundation TextBox-Steuer Elements festzulegen.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text content [WPF], setting
- TextBox control [WPF], setting text content
ms.assetid: bcd25fc7-a52f-4453-b802-2c8d2b335ab8
ms.openlocfilehash: 1e2ebdf2e66f4668b215767919c358ac34e5bd38
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977684"
---
# <a name="how-to-set-the-text-content-of-a-textbox-control"></a><span data-ttu-id="d591d-103">Gewusst wie: Festlegen des Textinhalts eines TextBox-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="d591d-103">How to: Set the Text Content of a TextBox Control</span></span>

<span data-ttu-id="d591d-104">In diesem Beispiel wird gezeigt, wie die-Eigenschaft verwendet wird <xref:System.Windows.Controls.TextBox.Text%2A> , um den ursprünglichen Text Inhalt eines-Steuer Elements festzulegen <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="d591d-104">This example shows how to use the <xref:System.Windows.Controls.TextBox.Text%2A> property to set the initial text contents of a <xref:System.Windows.Controls.TextBox> control.</span></span>

> [!NOTE]
> <span data-ttu-id="d591d-105">Obwohl die [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] -Version des Beispiels die `<TextBox.Text>` -Tags um den Text der einzelnen Schaltflächen Inhalte verwenden könnte <xref:System.Windows.Controls.TextBox> , ist dies nicht notwendig, da das- <xref:System.Windows.Controls.TextBox> <xref:System.Windows.Markup.ContentPropertyAttribute> Attribut auf die <xref:System.Windows.Controls.TextBox.Text%2A> Eigenschaft anwendet.</span><span class="sxs-lookup"><span data-stu-id="d591d-105">Although the [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] version of the example could use the `<TextBox.Text>` tags around the text of each button's <xref:System.Windows.Controls.TextBox> content, it is not necessary because the <xref:System.Windows.Controls.TextBox> applies the <xref:System.Windows.Markup.ContentPropertyAttribute> attribute to the <xref:System.Windows.Controls.TextBox.Text%2A> property.</span></span> <span data-ttu-id="d591d-106">Weitere Informationen finden Sie unter [Übersicht über XAML (WPF)](/dotnet/desktop-wpf/fundamentals/xaml).</span><span class="sxs-lookup"><span data-stu-id="d591d-106">For more information, see [XAML Overview (WPF)](/dotnet/desktop-wpf/fundamentals/xaml).</span></span>

## <a name="example"></a><span data-ttu-id="d591d-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d591d-107">Example</span></span>

[!code-xaml[TextBox_MiscCode#_TextBoxSetTextXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_textboxsettextxaml)]

## <a name="example"></a><span data-ttu-id="d591d-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d591d-108">Example</span></span>

[!code-csharp[TextBox_MiscCode#_TextBoxSetText](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textboxsettext)]
[!code-vb[TextBox_MiscCode#_TextBoxSetText](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_textboxsettext)]

## <a name="see-also"></a><span data-ttu-id="d591d-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d591d-109">See also</span></span>

- [<span data-ttu-id="d591d-110">Übersicht über TextBox</span><span class="sxs-lookup"><span data-stu-id="d591d-110">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="d591d-111">Übersicht über RichTextBox</span><span class="sxs-lookup"><span data-stu-id="d591d-111">RichTextBox Overview</span></span>](richtextbox-overview.md)
