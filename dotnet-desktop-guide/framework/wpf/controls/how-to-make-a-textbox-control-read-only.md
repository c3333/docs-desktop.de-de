---
title: 'Gewusst wie: Erstellen eines schreibgeschützten TextBox-Steuerelements'
ms.date: 03/30/2017
helpviewer_keywords:
- read-only TextBox controls [WPF]
- TextBox control read-only
ms.assetid: e707ec59-8b22-473e-b77c-3060a237517a
ms.openlocfilehash: 45fda33b5840bd89dac8d9e99f7dd1a8dd065838
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977186"
---
# <a name="how-to-make-a-textbox-control-read-only"></a><span data-ttu-id="84ea0-102">Gewusst wie: Erstellen eines schreibgeschützten TextBox-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="84ea0-102">How to: Make a TextBox Control Read-Only</span></span>
<span data-ttu-id="84ea0-103">Dieses Beispiel zeigt, wie Sie ein Steuerelement so konfigurieren <xref:System.Windows.Controls.TextBox> , dass Benutzereingaben oder-Änderungen nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="84ea0-103">This example shows how to configure a <xref:System.Windows.Controls.TextBox> control to not allow user input or modification.</span></span>  
  
## <a name="example"></a><span data-ttu-id="84ea0-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="84ea0-104">Example</span></span>  
 <span data-ttu-id="84ea0-105">Um zu verhindern, dass Benutzer den Inhalt eines <xref:System.Windows.Controls.TextBox> Steuer Elements ändern, legen Sie das- <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> Attribut auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="84ea0-105">To prevent users from modifying the contents of a <xref:System.Windows.Controls.TextBox> control, set the <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribute to **true**.</span></span>  
  
 [!code-xaml[TextBox_MiscCode#_ReadOnlyTextBoxXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_readonlytextboxxaml)]  
  
 <span data-ttu-id="84ea0-106">Das <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> Attribut wirkt sich nur auf die Benutzereingaben aus. es wirkt sich nicht auf den Text aus, der in der [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beschreibung eines Steuer Elements festgelegt <xref:System.Windows.Controls.TextBox> wurde, oder Text, der Programm gesteuert über die <xref:System.Windows.Controls.TextBox.Text%2A></span><span class="sxs-lookup"><span data-stu-id="84ea0-106">The <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribute affects user input only; it does not affect text set in the [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] description of a <xref:System.Windows.Controls.TextBox> control, or text set programmatically through the <xref:System.Windows.Controls.TextBox.Text%2A> property.</span></span>  
  
 <span data-ttu-id="84ea0-107">Der Standardwert von <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> ist **false**.</span><span class="sxs-lookup"><span data-stu-id="84ea0-107">The default value of <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> is **false**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84ea0-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84ea0-108">See also</span></span>

- [<span data-ttu-id="84ea0-109">Übersicht über TextBox</span><span class="sxs-lookup"><span data-stu-id="84ea0-109">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="84ea0-110">Übersicht über RichTextBox</span><span class="sxs-lookup"><span data-stu-id="84ea0-110">RichTextBox Overview</span></span>](richtextbox-overview.md)
