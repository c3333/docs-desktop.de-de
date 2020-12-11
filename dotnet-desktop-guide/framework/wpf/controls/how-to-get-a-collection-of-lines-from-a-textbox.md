---
title: 'Gewusst wie: Abrufen einer Auflistung der Zeilen aus einem "TextBox"-Element'
ms.date: 03/30/2017
helpviewer_keywords:
- lines [WPF], getting collection of
- TextBox control [WPF], getting collection of lines
ms.assetid: a12f529d-b926-47f6-92bf-cad5f17b532a
ms.openlocfilehash: b7b2f1c2e071388635fb50b1e3573fd7f44334dd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977411"
---
# <a name="how-to-get-a-collection-of-lines-from-a-textbox"></a><span data-ttu-id="2c8c3-102">Gewusst wie: Abrufen einer Auflistung der Zeilen aus einem "TextBox"-Element</span><span class="sxs-lookup"><span data-stu-id="2c8c3-102">How to: Get a Collection of Lines from a TextBox</span></span>
<span data-ttu-id="2c8c3-103">In diesem Beispiel wird gezeigt, wie Sie eine Auflistung von Textzeilen aus einer-Auflistung erhalten <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="2c8c3-103">This example shows how to get a collection of lines of text from a <xref:System.Windows.Controls.TextBox>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2c8c3-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2c8c3-104">Example</span></span>  
 <span data-ttu-id="2c8c3-105">Das folgende Beispiel zeigt eine einfache Methode, die eine <xref:System.Windows.Controls.TextBox> als-Argument annimmt und eine zurückgibt, <xref:System.Collections.Specialized.StringCollection> die die Textzeilen im **Textfeld** enthält.</span><span class="sxs-lookup"><span data-stu-id="2c8c3-105">The following example shows a simple method that takes a <xref:System.Windows.Controls.TextBox> as the argument, and returns a <xref:System.Collections.Specialized.StringCollection> containing the lines of text in the **TextBox**.</span></span>  <span data-ttu-id="2c8c3-106">Die <xref:System.Windows.Controls.TextBox.LineCount%2A> -Eigenschaft wird verwendet, um zu bestimmen, wie viele Zeilen derzeit im **Textfeld** sind, und <xref:System.Windows.Controls.TextBox.GetLineText%2A> anschließend wird die-Methode verwendet, um jede Zeile zu extrahieren und Sie der Zeilen Auflistung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2c8c3-106">The <xref:System.Windows.Controls.TextBox.LineCount%2A> property is used to determine how many lines are currently in the **TextBox**, and the <xref:System.Windows.Controls.TextBox.GetLineText%2A> method is then used to extract each line and add it to the collection of lines.</span></span>  
  
 [!code-csharp[TextBox_MiscCode#_TextBox_GetLines](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textbox_getlines)]  
  
## <a name="see-also"></a><span data-ttu-id="2c8c3-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c8c3-107">See also</span></span>

- [<span data-ttu-id="2c8c3-108">Übersicht über TextBox</span><span class="sxs-lookup"><span data-stu-id="2c8c3-108">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="2c8c3-109">Übersicht über RichTextBox</span><span class="sxs-lookup"><span data-stu-id="2c8c3-109">RichTextBox Overview</span></span>](richtextbox-overview.md)
