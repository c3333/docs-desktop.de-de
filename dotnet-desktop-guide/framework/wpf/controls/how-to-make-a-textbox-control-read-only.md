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
# <a name="how-to-make-a-textbox-control-read-only"></a>Gewusst wie: Erstellen eines schreibgeschützten TextBox-Steuerelements
Dieses Beispiel zeigt, wie Sie ein Steuerelement so konfigurieren <xref:System.Windows.Controls.TextBox> , dass Benutzereingaben oder-Änderungen nicht zulässig sind.  
  
## <a name="example"></a>Beispiel  
 Um zu verhindern, dass Benutzer den Inhalt eines <xref:System.Windows.Controls.TextBox> Steuer Elements ändern, legen Sie das- <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> Attribut auf " **true**" fest.  
  
 [!code-xaml[TextBox_MiscCode#_ReadOnlyTextBoxXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_readonlytextboxxaml)]  
  
 Das <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> Attribut wirkt sich nur auf die Benutzereingaben aus. es wirkt sich nicht auf den Text aus, der in der [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beschreibung eines Steuer Elements festgelegt <xref:System.Windows.Controls.TextBox> wurde, oder Text, der Programm gesteuert über die <xref:System.Windows.Controls.TextBox.Text%2A>  
  
 Der Standardwert von <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> ist **false**.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über TextBox](textbox-overview.md)
- [Übersicht über RichTextBox](richtextbox-overview.md)
