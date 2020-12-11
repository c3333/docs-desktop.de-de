---
title: Bild Lauf leisten im RichTextBox-Steuerelement anzeigen
ms.date: 03/30/2017
helpviewer_keywords:
- text boxes [Windows Forms], displaying scroll bars
- scroll bars [Windows Forms], displaying in controls
- RichTextBox control [Windows Forms], displaying scroll bars
ms.assetid: cdeb42e1-86e8-410c-ba46-18aec264ef5f
ms.openlocfilehash: 2185b572ef20765043d3df3dbfd8bf5b21cfac28
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976516"
---
# <a name="how-to-display-scroll-bars-in-the-windows-forms-richtextbox-control"></a>Vorgehensweise: Anzeigen von Scrollleisten im RichTextBox-Steuerelement von Windows Forms
Standardmäßig werden im Windows Forms <xref:System.Windows.Forms.RichTextBox> Steuerelement bei Bedarf horizontale und vertikale Schiebe leisten angezeigt. Es gibt sieben mögliche Werte für die- <xref:System.Windows.Forms.RichTextBox.ScrollBars%2A> Eigenschaft des- <xref:System.Windows.Forms.RichTextBox> Steuer Elements, die in der folgenden Tabelle beschrieben werden.  
  
### <a name="to-display-scroll-bars-in-a-richtextbox-control"></a>So zeigen Sie Bild Lauf leisten in einem RichTextBox-Steuerelement an  
  
1. Legen Sie die <xref:System.Windows.Forms.RichTextBox.Multiline%2A> -Eigenschaft auf `true`fest. Wenn die- <xref:System.Windows.Forms.RichTextBox.Multiline%2A> Eigenschaft auf festgelegt ist, wird kein Typ der Bild Lauf Leiste angezeigt, einschließlich der horizontalen `false` .  
  
2. Legen Sie die- <xref:System.Windows.Forms.RichTextBox.ScrollBars%2A> Eigenschaft auf einen geeigneten Wert der- <xref:System.Windows.Forms.RichTextBoxScrollBars> Enumeration fest.  
  
    |Wert|Beschreibung|  
    |-----------|-----------------|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.Both> (Standardwert)|Zeigt horizontale oder vertikale Schiebe leisten (oder beides) nur an, wenn Text die Breite oder Länge des Steuer Elements überschreitet.|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.None>|Zeigt nie eine beliebige Bild Lauf Leiste an.|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.Horizontal>|Zeigt eine horizontale Schiebe Leiste nur an, wenn der Text die Breite des Steuer Elements überschreitet. (Damit dies geschehen kann, muss die- <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A> Eigenschaft auf festgelegt werden `false` .)|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.Vertical>|Zeigt eine vertikale Schiebe Leiste nur an, wenn der Text die Höhe des Steuer Elements überschreitet.|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.ForcedHorizontal>|Zeigt eine horizontale Schiebe Leiste an, wenn die- <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A> Eigenschaft auf festgelegt ist `false` . Die Bild Lauf Leiste wird abgeblendet angezeigt, wenn der Text nicht die Breite des Steuer Elements überschreitet.|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.ForcedVertical>|Zeigt immer eine vertikale Bild Lauf Leiste an. Die Bild Lauf Leiste wird abgeblendet angezeigt, wenn der Text die Länge des Steuer Elements nicht überschreitet.|  
    |<xref:System.Windows.Forms.RichTextBoxScrollBars.ForcedBoth>|Zeigt immer eine vertikale Bild Lauf Leiste an. Zeigt eine horizontale Schiebe Leiste an, wenn die- <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A> Eigenschaft auf festgelegt ist `false` . Die Bild Lauf leisten werden ausgegraut angezeigt, wenn Text die Breite oder Länge des Steuer Elements nicht überschreitet.|  
  
3. Legen Sie für die <xref:System.Windows.Forms.TextBoxBase.WordWrap%2A>-Eigenschaft einen geeigneten Wert fest.  
  
    |Wert|BESCHREIBUNG|  
    |-----------|-----------------|  
    |`false`|Der Text im Steuerelement wird nicht automatisch an die Breite des Steuer Elements angepasst, sodass er nach rechts verschoben wird, bis ein Zeilenumbruch erreicht ist. Verwenden Sie diesen Wert, wenn Sie oben horizontale Schiebe leisten oder beides ausgewählt haben.|  
    |`true` (Standard)|Der Text im-Steuerelement wird automatisch an die Breite des-Steuer Elements angepasst. Die horizontale Scrollleiste wird nicht angezeigt. Verwenden Sie diesen Wert, wenn Sie vertikale Bild Lauf leisten ausgewählt haben oder oben, um einen oder mehrere Absätze anzuzeigen.|  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.RichTextBoxScrollBars>
- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox-Steuerelement](richtextbox-control-windows-forms.md)
- [Steuerelemente für Windows Forms](controls-to-use-on-windows-forms.md)
