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
# <a name="how-to-get-a-collection-of-lines-from-a-textbox"></a>Gewusst wie: Abrufen einer Auflistung der Zeilen aus einem "TextBox"-Element
In diesem Beispiel wird gezeigt, wie Sie eine Auflistung von Textzeilen aus einer-Auflistung erhalten <xref:System.Windows.Controls.TextBox> .  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt eine einfache Methode, die eine <xref:System.Windows.Controls.TextBox> als-Argument annimmt und eine zurückgibt, <xref:System.Collections.Specialized.StringCollection> die die Textzeilen im **Textfeld** enthält.  Die <xref:System.Windows.Controls.TextBox.LineCount%2A> -Eigenschaft wird verwendet, um zu bestimmen, wie viele Zeilen derzeit im **Textfeld** sind, und <xref:System.Windows.Controls.TextBox.GetLineText%2A> anschließend wird die-Methode verwendet, um jede Zeile zu extrahieren und Sie der Zeilen Auflistung hinzuzufügen.  
  
 [!code-csharp[TextBox_MiscCode#_TextBox_GetLines](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textbox_getlines)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über TextBox](textbox-overview.md)
- [Übersicht über RichTextBox](richtextbox-overview.md)
