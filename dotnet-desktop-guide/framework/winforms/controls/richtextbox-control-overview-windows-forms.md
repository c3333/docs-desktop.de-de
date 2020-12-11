---
title: Übersicht über das RichTextBox-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- RichTextBox
helpviewer_keywords:
- RichTextBox control [Windows Forms], about RichTextBox control
- text boxes [Windows Forms], about text boxes
ms.assetid: 95081194-3dd4-4b84-9545-dd373e491eca
ms.openlocfilehash: 0d40967d97622b23e9dcb07e861f190327e6baba
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976464"
---
# <a name="richtextbox-control-overview-windows-forms"></a>Übersicht über das RichTextBox-Steuerelement (Windows Forms)
Das Windows Forms- <xref:System.Windows.Forms.RichTextBox> Steuerelement wird zum Anzeigen, eingeben und Bearbeiten von Text mit Formatierungen verwendet. Das- <xref:System.Windows.Forms.RichTextBox> Steuerelement erledigt alles, was das-Steuerelement bewirkt <xref:System.Windows.Forms.TextBox> , aber es kann auch Schriftarten, Farben und Verknüpfungen anzeigen, Text und eingebettete Bilder aus einer Datei laden und angegebene Zeichen suchen. Das <xref:System.Windows.Forms.RichTextBox> -Steuerelement wird normalerweise verwendet, um Textbearbeitung und Features anzuzeigen, ähnlich wie bei Textverarbeitungsanwendungen wie z. b. Microsoft Word. Ebenso wie das- <xref:System.Windows.Forms.TextBox> Steuerelement kann das Steuerelement Bild Lauf <xref:System.Windows.Forms.RichTextBox> leisten anzeigen, aber im Gegensatz zum- <xref:System.Windows.Forms.TextBox> Steuerelement ist die Standardeinstellung, bei Bedarf sowohl horizontale als auch vertikale Scrollleisten anzuzeigen, und Sie verfügt über zusätzliche Bild Lauf Leiste-Einstellungen.  
  
## <a name="working-with-the-richtextbox-control"></a>Arbeiten mit dem RichTextBox-Steuerelement  
 Wie beim- <xref:System.Windows.Forms.TextBox> Steuerelement wird der angezeigte Text durch die-Eigenschaft festgelegt <xref:System.Windows.Forms.RichTextBox.Text%2A> . Das <xref:System.Windows.Forms.RichTextBox> Steuerelement verfügt über zahlreiche Eigenschaften zum Formatieren von Text. Ausführliche Informationen zu diesen Eigenschaften finden Sie unter [Gewusst wie: Festlegen von Schriftartattributen für das RichTextBox-Steuerelement von Windows Forms](how-to-set-font-attributes-for-the-windows-forms-richtextbox-control.md) und [Gewusst wie: Festlegen von Einzügen, hängenden Einzügen und Absätzen mit Aufzählungszeichen mit dem RichTextBox-Steuerelement von Windows Forms](set-indents-hanging-indents-bulleted-paragraphs-with-wf-richtextbox.md). Um Dateien zu bearbeiten, <xref:System.Windows.Forms.RichTextBox.LoadFile%2A> können die-Methode und die- <xref:System.Windows.Forms.RichTextBox.SaveFile%2A> Methode mehrere Dateiformate anzeigen und schreiben, einschließlich nur-Text, Unicode-nur-Text und RTF (Rich Text Format). Die möglichen Dateiformate sind unter aufgeführt <xref:System.Windows.Forms.RichTextBoxStreamType> . Sie können die- <xref:System.Windows.Forms.RichTextBox.Find%2A> Methode verwenden, um Text Zeichenfolgen oder bestimmte Zeichen zu suchen.  
  
 Sie können auch ein <xref:System.Windows.Forms.RichTextBox> -Steuerelement für Webstil Verknüpfungen verwenden, indem Sie die <xref:System.Windows.Forms.RichTextBox.DetectUrls%2A> -Eigenschaft auf festlegen `true` und Code zur Behandlung des- <xref:System.Windows.Forms.RichTextBox.LinkClicked> Ereignisses schreiben. Weitere Informationen finden Sie unter [Gewusst wie: Anzeigen von Hyperlinks mit dem RichTextBox-Steuerelement von Windows Forms](how-to-display-web-style-links-with-the-windows-forms-richtextbox-control.md). Sie können verhindern, dass der Benutzer den Text im-Steuerelement bearbeitet, indem Sie die- <xref:System.Windows.Forms.RichTextBox.SelectionProtected%2A> Eigenschaft auf festlegen `true` .  
  
 <xref:System.Windows.Forms.RichTextBox>Durch Aufrufen der Methoden und können Sie die meisten Bearbeitungsvorgänge in einem-Steuerelement rückgängig machen und wiederholen <xref:System.Windows.Forms.TextBoxBase.Undo%2A> <xref:System.Windows.Forms.RichTextBox.Redo%2A> . Mit der- <xref:System.Windows.Forms.RichTextBox.CanRedo%2A> Methode können Sie feststellen, ob der letzte Vorgang, den der Benutzer rückgängig gemacht hat, erneut auf das-Steuerelement angewendet werden kann.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox-Steuerelement](richtextbox-control-windows-forms.md)
- [Übersicht über das TextBox-Steuerelement](textbox-control-overview-windows-forms.md)
