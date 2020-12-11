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
# <a name="how-to-add-a-watermark-to-a-textbox"></a>Gewusst wie: Hinzufügen eines Wasserzeichens zu einer TextBox
Im folgenden Beispiel wird gezeigt, wie Sie die Verwendbarkeit eines <xref:System.Windows.Controls.TextBox> unterstützen können, indem Sie ein erklärendes Hintergrundbild innerhalb von anzeigen <xref:System.Windows.Controls.TextBox> , bis der Benutzer Text eingibt. an diesem Punkt wird das Bild entfernt. Außerdem wird das Hintergrundbild wieder hergestellt, wenn der Benutzer seine Eingabe entfernt. Siehe Abbildung unten.  
  
 ![Eine TextBox mit einem Hintergrundbild](./media/editing-textbox-using-background-image.png "Editing_TextBox_using_background_image")  
  
> [!NOTE]
> Der Grund, warum ein Hintergrundbild in diesem Beispiel verwendet wird, anstatt einfach die- <xref:System.Windows.Controls.TextBox.Text%2A> Eigenschaft von <xref:System.Windows.Controls.TextBox> zu bearbeiten, besteht darin, dass ein Hintergrundbild die Datenbindung nicht beeinträchtigt.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[TextBoxMiscSnippets_snip#TextBoxBackgroundExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/textbox_with_background_image.xaml#textboxbackgroundexamplewholepage)]  
  
 [!code-csharp[TextBoxMiscSnippets_snip#TextBoxBackgroundCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/textbox_with_background_image.xaml.cs#textboxbackgroundcodeexamplewholepage)]
 [!code-vb[TextBoxMiscSnippets_snip#TextBoxBackgroundCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/visualbasic/textbox_with_background_image.xaml.vb#textboxbackgroundcodeexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über TextBox](textbox-overview.md)
- [Übersicht über RichTextBox](richtextbox-overview.md)
