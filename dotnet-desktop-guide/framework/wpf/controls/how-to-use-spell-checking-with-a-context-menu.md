---
title: 'Gewusst wie: Verwenden der Rechtschreibprüfung mit einem Kontextmenü'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- enabling spell checking in a text box [WPF]
- reenabling spell checking in a text box [WPF]
- spell checking with a context menu [WPF]
ms.assetid: 61f69a20-2ff3-4056-9060-e32f4483ec5e
ms.openlocfilehash: 0c2ceb3e4091ee1d98bd0c786f51b3596cdedd08
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974660"
---
# <a name="how-to-use-spell-checking-with-a-context-menu"></a>Gewusst wie: Verwenden der Rechtschreibprüfung mit einem Kontextmenü
Wenn Sie die Rechtschreibprüfung in einem Bearbeitungs Steuerelement wie oder aktivieren <xref:System.Windows.Controls.TextBox> <xref:System.Windows.Controls.RichTextBox> , erhalten Sie standardmäßig im Kontextmenü die Optionen für die Rechtschreibprüfung. Wenn Benutzer z. b. mit der rechten Maustaste auf ein falsch geschriebenes Wort klicken, erhalten Sie einen Satz von Rechtschreib Vorschlägen oder die Option **Alle ignorieren**. Wenn Sie jedoch das Standardkontext Menü mit Ihrem eigenen benutzerdefinierten Kontextmenü außer Kraft setzen, gehen diese Funktionen verloren, und Sie müssen Code schreiben, um die Funktion zur Rechtschreibprüfung erneut im Kontextmenü zu aktivieren. Im folgenden Beispiel wird gezeigt, wie dies für eine aktiviert wird <xref:System.Windows.Controls.TextBox> .  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] , dass ein <xref:System.Windows.Controls.TextBox> mit einigen Ereignissen erstellt, die zum Implementieren des Kontextmenüs verwendet werden.  
  
 [!code-xaml[TextBoxMiscSnippets_snip#SpellerCustomContextMenuExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/speller_custom_context_menu.xaml#spellercustomcontextmenuexamplewholepage)]  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt den Code, der das Kontextmenü implementiert.  
  
 [!code-csharp[TextBoxMiscSnippets_snip#SpellerCustomContextMenuCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/speller_custom_context_menu.xaml.cs#spellercustomcontextmenucodeexamplewholepage)]
 [!code-vb[TextBoxMiscSnippets_snip#SpellerCustomContextMenuCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/visualbasic/speller_custom_context_menu.xaml.vb#spellercustomcontextmenucodeexamplewholepage)]  
  
 Der Code, der dazu verwendet wird, <xref:System.Windows.Controls.RichTextBox> ist ähnlich. Der Hauptunterschied besteht im-Parameter, der an die-Methode übergeben wird `GetSpellingError` . Übergeben Sie für einen <xref:System.Windows.Controls.TextBox> den ganzzahligen Index der Position der Einfügemarke:  
  
 `spellingError = myTextBox.GetSpellingError(caretIndex);`  
  
 Übergeben Sie für eine den, der die Position der Einfügemarke <xref:System.Windows.Controls.RichTextBox> <xref:System.Windows.Documents.TextPointer> angibt:  
  
 `spellingError = myRichTextBox.GetSpellingError(myRichTextBox.CaretPosition);`  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über TextBox](textbox-overview.md)
- [Übersicht über RichTextBox](richtextbox-overview.md)
- [Aktivieren der Rechtschreibprüfung in einem Textbearbeitungssteuerelement](how-to-enable-spell-checking-in-a-text-editing-control.md)
- [Verwenden eines benutzerdefinierten Kontextmenüs mit einem TextBox-Objekt](how-to-use-a-custom-context-menu-with-a-textbox.md)
