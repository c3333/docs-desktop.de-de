---
title: 'Gewusst wie: Erstellen eines Steuerelements, das über eine Tastenkombination und Textumbruch verfügt'
ms.date: 03/30/2017
helpviewer_keywords:
- access keys [WPF], control for
- controls [WPF], text wrapping
- wrapping text [WPF]
- keys [WPF], control for
- controls [WPF], access keys
- text wrapping [WPF]
ms.assetid: 205099d9-2551-4302-a25e-a15af9f67e04
ms.openlocfilehash: 86239374ca9cb3bd3d71415496e32d4a27fbae5a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978076"
---
# <a name="how-to-create-a-control-that-has-an-access-key-and-text-wrapping"></a>Gewusst wie: Erstellen eines Steuerelements, das über eine Tastenkombination und Textumbruch verfügt

Diese Beispiel veranschaulicht, wie Sie ein Steuerelement erstellen, das über eine Tastenkombination verfügt und das Umbrechen von Text unterstützt. Im Beispiel wird ein-Steuerelement verwendet <xref:System.Windows.Controls.Label> , um diese Konzepte zu veranschaulichen.  
  
## <a name="example"></a>Beispiel  

 **Umbrechen des Texts einer Bezeichnung**  
  
 Das- <xref:System.Windows.Controls.Label> Steuerelement unterstützt keine Text Umbrüchen. Wenn sich eine Bezeichnung über mehrere Zeilen erstrecken soll, können Sie ein anderes Element verschachteln, das das Umbrechen von Text unterstützt, und es innerhalb der Bezeichnung platzieren. Im folgenden Beispiel wird gezeigt, wie Sie mit einem <xref:System.Windows.Controls.TextBlock> eine Bezeichnung erstellen, die mehrere Textzeilen umschließt.  
  
 [!code-xaml[LabelSnippet#5](~/samples/snippets/csharp/VS_Snippets_Wpf/LabelSnippet/CS/Pane1.xaml#5)]  
  
 **Hinzufügen von Textumbruch und einer Tastenkombination zu einer Bezeichnung**  
  
 Wenn Sie ein- <xref:System.Windows.Controls.Label> Element benötigen, das über eine Zugriffstaste (mnetmonic) verfügt, verwenden Sie das-Element, das <xref:System.Windows.Controls.AccessText> sich in befindet <xref:System.Windows.Controls.Label> .  
  
 Steuerelemente wie <xref:System.Windows.Controls.Label> , <xref:System.Windows.Controls.Button> , <xref:System.Windows.Controls.RadioButton> , <xref:System.Windows.Controls.CheckBox> , <xref:System.Windows.Controls.MenuItem> , <xref:System.Windows.Controls.TabItem> , <xref:System.Windows.Controls.Expander> und <xref:System.Windows.Controls.GroupBox> verfügen über Standard Steuerelement Vorlagen. Diese Vorlagen enthalten einen <xref:System.Windows.Controls.ContentPresenter> . Eine der Eigenschaften, die Sie für das festlegen können <xref:System.Windows.Controls.ContentPresenter> <xref:System.Windows.Controls.ContentPresenter.RecognizesAccessKey%2A> , ist = "true", mit dem Sie einen Zugriffsschlüssel für das Steuerelement angeben können.  
  
 Im folgenden Beispiel wird gezeigt, wie ein erstellt wird <xref:System.Windows.Controls.Label> , das über eine Zugriffstaste verfügt und Text Umbrüchen unterstützt. Um das Umbenennen von Text zu aktivieren, wird im Beispiel die <xref:System.Windows.Controls.AccessText.TextWrapping%2A> -Eigenschaft festgelegt und ein Unterstrich verwendet, um die Zugriffstaste anzugeben. (Das Zeichen, das unmittelbar auf den Unterstrich folgt, ist die Tastenkombination.)  
  
 [!code-xaml[LabelSnippet#4](~/samples/snippets/csharp/VS_Snippets_Wpf/LabelSnippet/CS/Pane1.xaml#4)]  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Festlegen der Eigenschaft „Target“ einer Bezeichnung](/previous-versions/dotnet/netframework-3.5/ms752101(v=vs.90))
