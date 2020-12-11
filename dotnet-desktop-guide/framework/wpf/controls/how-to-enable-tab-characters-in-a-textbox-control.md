---
title: 'Gewusst wie: Aktivieren von Tabstoppzeichen in einem TextBox-Steuerelement'
ms.date: 03/30/2017
helpviewer_keywords:
- TextBox control [WPF], enabling tab characters
- tab characters [WPF], enabling
ms.assetid: 14b1b064-61f7-4958-be63-88d85b868d03
ms.openlocfilehash: 9a01ae93d1b75c604fbe4f15f720e0a84086bd1a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977414"
---
# <a name="how-to-enable-tab-characters-in-a-textbox-control"></a>Gewusst wie: Aktivieren von Tabstoppzeichen in einem TextBox-Steuerelement
In diesem Beispiel wird gezeigt, wie die Annahme von Tabstopp Zeichen als normale Eingabe in einem-Steuerelement aktiviert wird <xref:System.Windows.Controls.TextBox> .  
  
## <a name="example"></a>Beispiel  
 Um die Annahme von Tabstopp Zeichen als Eingabe in einem-Steuerelement zu aktivieren <xref:System.Windows.Controls.TextBox> , legen Sie das- <xref:System.Windows.Controls.Primitives.TextBoxBase.AcceptsTab%2A> Attribut auf **true** fest.  
  
 [!code-xaml[TextBox_EnablingTab#_AcceptsTab](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_EnablingTab/CS/Window1.xaml#_acceptstab)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über TextBox](textbox-overview.md)
- [Übersicht über RichTextBox](richtextbox-overview.md)
