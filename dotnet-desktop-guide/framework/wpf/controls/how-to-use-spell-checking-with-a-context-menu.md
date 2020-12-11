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
# <a name="how-to-use-spell-checking-with-a-context-menu"></a><span data-ttu-id="d5b8a-102">Gewusst wie: Verwenden der Rechtschreibprüfung mit einem Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="d5b8a-102">How to: Use Spell Checking with a Context Menu</span></span>
<span data-ttu-id="d5b8a-103">Wenn Sie die Rechtschreibprüfung in einem Bearbeitungs Steuerelement wie oder aktivieren <xref:System.Windows.Controls.TextBox> <xref:System.Windows.Controls.RichTextBox> , erhalten Sie standardmäßig im Kontextmenü die Optionen für die Rechtschreibprüfung.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-103">By default, when you enable spell checking in an editing control like <xref:System.Windows.Controls.TextBox> or <xref:System.Windows.Controls.RichTextBox>, you get spell-checking choices in the context menu.</span></span> <span data-ttu-id="d5b8a-104">Wenn Benutzer z. b. mit der rechten Maustaste auf ein falsch geschriebenes Wort klicken, erhalten Sie einen Satz von Rechtschreib Vorschlägen oder die Option **Alle ignorieren**.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-104">For example, when users right-click a misspelled word, they get a set of spelling suggestions or the option to **Ignore All**.</span></span> <span data-ttu-id="d5b8a-105">Wenn Sie jedoch das Standardkontext Menü mit Ihrem eigenen benutzerdefinierten Kontextmenü außer Kraft setzen, gehen diese Funktionen verloren, und Sie müssen Code schreiben, um die Funktion zur Rechtschreibprüfung erneut im Kontextmenü zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-105">However, when you override the default context menu with your own custom context menu, this functionality is lost, and you need to write code to reenable the spell-checking feature in the context menu.</span></span> <span data-ttu-id="d5b8a-106">Im folgenden Beispiel wird gezeigt, wie dies für eine aktiviert wird <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="d5b8a-106">The following example shows how to enable this on a <xref:System.Windows.Controls.TextBox>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d5b8a-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d5b8a-107">Example</span></span>  
 <span data-ttu-id="d5b8a-108">Das folgende Beispiel zeigt [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] , dass ein <xref:System.Windows.Controls.TextBox> mit einigen Ereignissen erstellt, die zum Implementieren des Kontextmenüs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-108">The following example shows the [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] that creates a <xref:System.Windows.Controls.TextBox> with some events that are used to implement the context menu.</span></span>  
  
 [!code-xaml[TextBoxMiscSnippets_snip#SpellerCustomContextMenuExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/speller_custom_context_menu.xaml#spellercustomcontextmenuexamplewholepage)]  
  
## <a name="example"></a><span data-ttu-id="d5b8a-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d5b8a-109">Example</span></span>  
 <span data-ttu-id="d5b8a-110">Das folgende Beispiel zeigt den Code, der das Kontextmenü implementiert.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-110">The following example shows the code that implements the context menu.</span></span>  
  
 [!code-csharp[TextBoxMiscSnippets_snip#SpellerCustomContextMenuCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/speller_custom_context_menu.xaml.cs#spellercustomcontextmenucodeexamplewholepage)]
 [!code-vb[TextBoxMiscSnippets_snip#SpellerCustomContextMenuCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/visualbasic/speller_custom_context_menu.xaml.vb#spellercustomcontextmenucodeexamplewholepage)]  
  
 <span data-ttu-id="d5b8a-111">Der Code, der dazu verwendet wird, <xref:System.Windows.Controls.RichTextBox> ist ähnlich.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-111">The code used for doing this with a <xref:System.Windows.Controls.RichTextBox> is similar.</span></span> <span data-ttu-id="d5b8a-112">Der Hauptunterschied besteht im-Parameter, der an die-Methode übergeben wird `GetSpellingError` .</span><span class="sxs-lookup"><span data-stu-id="d5b8a-112">The main difference is in the parameter passed to the `GetSpellingError` method.</span></span> <span data-ttu-id="d5b8a-113">Übergeben Sie für einen <xref:System.Windows.Controls.TextBox> den ganzzahligen Index der Position der Einfügemarke:</span><span class="sxs-lookup"><span data-stu-id="d5b8a-113">For a <xref:System.Windows.Controls.TextBox>, pass the integer index of the caret position:</span></span>  
  
 `spellingError = myTextBox.GetSpellingError(caretIndex);`  
  
 <span data-ttu-id="d5b8a-114">Übergeben Sie für eine den, der die Position der Einfügemarke <xref:System.Windows.Controls.RichTextBox> <xref:System.Windows.Documents.TextPointer> angibt:</span><span class="sxs-lookup"><span data-stu-id="d5b8a-114">For a <xref:System.Windows.Controls.RichTextBox>, pass the <xref:System.Windows.Documents.TextPointer> that specifies the caret position:</span></span>  
  
 `spellingError = myRichTextBox.GetSpellingError(myRichTextBox.CaretPosition);`  
  
## <a name="see-also"></a><span data-ttu-id="d5b8a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5b8a-115">See also</span></span>

- [<span data-ttu-id="d5b8a-116">Übersicht über TextBox</span><span class="sxs-lookup"><span data-stu-id="d5b8a-116">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="d5b8a-117">Übersicht über RichTextBox</span><span class="sxs-lookup"><span data-stu-id="d5b8a-117">RichTextBox Overview</span></span>](richtextbox-overview.md)
- [<span data-ttu-id="d5b8a-118">Aktivieren der Rechtschreibprüfung in einem Textbearbeitungssteuerelement</span><span class="sxs-lookup"><span data-stu-id="d5b8a-118">Enable Spell Checking in a Text Editing Control</span></span>](how-to-enable-spell-checking-in-a-text-editing-control.md)
- [<span data-ttu-id="d5b8a-119">Verwenden eines benutzerdefinierten Kontextmenüs mit einem TextBox-Objekt</span><span class="sxs-lookup"><span data-stu-id="d5b8a-119">Use a Custom Context Menu with a TextBox</span></span>](how-to-use-a-custom-context-menu-with-a-textbox.md)
