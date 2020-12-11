---
title: 'Gewusst wie: Hinzufügen eines Wasserzeichens zu einer TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- displaying a background image inside a text box to aid user input [WPF]
- aid usability of a TextBox using a background image [WPF]
ms.assetid: df89bdd8-a0fb-45e0-b312-dd53332d01a8
ms.openlocfilehash: abe276c686d394ded13ec03f08deae65e4098d03
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977045"
---
# <a name="how-to-add-a-watermark-to-a-textbox"></a><span data-ttu-id="2a234-102">Gewusst wie: Hinzufügen eines Wasserzeichens zu einer TextBox</span><span class="sxs-lookup"><span data-stu-id="2a234-102">How to: Add a Watermark to a TextBox</span></span>
<span data-ttu-id="2a234-103">Im folgenden Beispiel wird gezeigt, wie Sie die Verwendbarkeit eines <xref:System.Windows.Controls.TextBox> unterstützen können, indem Sie ein erklärendes Hintergrundbild innerhalb von anzeigen <xref:System.Windows.Controls.TextBox> , bis der Benutzer Text eingibt. an diesem Punkt wird das Bild entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a234-103">The following example shows how to aid usability of a <xref:System.Windows.Controls.TextBox> by displaying an explanatory background image inside of the <xref:System.Windows.Controls.TextBox> until the user inputs text, at which point the image is removed.</span></span> <span data-ttu-id="2a234-104">Außerdem wird das Hintergrundbild wieder hergestellt, wenn der Benutzer seine Eingabe entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a234-104">In addition, the background image is restored again if the user removes their input.</span></span> <span data-ttu-id="2a234-105">Siehe Abbildung unten.</span><span class="sxs-lookup"><span data-stu-id="2a234-105">See illustration below.</span></span>  
  
 <span data-ttu-id="2a234-106">![Eine TextBox mit einem Hintergrundbild](./media/editing-textbox-using-background-image.png "Editing_TextBox_using_background_image")</span><span class="sxs-lookup"><span data-stu-id="2a234-106">![A TextBox with a background image](./media/editing-textbox-using-background-image.png "Editing_TextBox_using_background_image")</span></span>  
  
> [!NOTE]
> <span data-ttu-id="2a234-107">Der Grund, warum ein Hintergrundbild in diesem Beispiel verwendet wird, anstatt einfach die- <xref:System.Windows.Controls.TextBox.Text%2A> Eigenschaft von <xref:System.Windows.Controls.TextBox> zu bearbeiten, besteht darin, dass ein Hintergrundbild die Datenbindung nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="2a234-107">The reason a background image is used in this example rather then simply manipulating the <xref:System.Windows.Controls.TextBox.Text%2A> property of <xref:System.Windows.Controls.TextBox>, is that a background image will not interfere with data binding.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2a234-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2a234-108">Example</span></span>  
 [!code-xaml[TextBoxMiscSnippets_snip#TextBoxBackgroundExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/textbox_with_background_image.xaml#textboxbackgroundexamplewholepage)]  
  
 [!code-csharp[TextBoxMiscSnippets_snip#TextBoxBackgroundCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/textbox_with_background_image.xaml.cs#textboxbackgroundcodeexamplewholepage)]
 [!code-vb[TextBoxMiscSnippets_snip#TextBoxBackgroundCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/visualbasic/textbox_with_background_image.xaml.vb#textboxbackgroundcodeexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="2a234-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a234-109">See also</span></span>

- [<span data-ttu-id="2a234-110">Übersicht über TextBox</span><span class="sxs-lookup"><span data-stu-id="2a234-110">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="2a234-111">Übersicht über RichTextBox</span><span class="sxs-lookup"><span data-stu-id="2a234-111">RichTextBox Overview</span></span>](richtextbox-overview.md)
