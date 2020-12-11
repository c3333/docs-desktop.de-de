---
title: 'Vorgehensweise: Ausführen von Drag & Drop-Operationen zwischen Anwendungen'
ms.date: 03/30/2017
helpviewer_keywords:
- drag and drop [Windows Forms], between applications
ms.assetid: fa347436-2b12-4dd6-8507-59d7241f6a06
ms.openlocfilehash: 9aac3a0efd6359c25a6972f0e0b52dd489ec31db
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975894"
---
# <a name="how-to-perform-drag-and-drop-operations-between-applications"></a>Vorgehensweise: Ausführen von Drag & Drop-Operationen zwischen Anwendungen
Das Ausführen von Drag &amp; Drop-Vorgängen zwischen Anwendungen unterscheidet sich nicht vom Aktivieren dieser Aktion innerhalb einer Anwendung, so lange sich die beiden betroffenen Anwendungen gemäß dem „Vertrag“ verhalten, der zwischen den Eigenschaften <xref:System.Windows.Forms.DragEventArgs.AllowedEffect%2A> und <xref:System.Windows.Forms.DragEventArgs.Effect%2A> eingerichtet wurde.  
  
 Im folgenden Verfahren verwenden Sie eine von Ihnen erstellte Windows-basierte Anwendung und das im Windows-Betriebssystem enthaltene Textverarbeitungsprogramm WordPad, um Drag &amp; Drop-Vorgänge zwischen Anwendungen auszuführen. WordPad verfügt über einen bestimmten Satz an zulässigen Effekte für Drag & Drop-Text. Die Windows-basierte Anwendung, für die Sie Code schreiben, arbeitet mit diesen Effekten, damit die Drag &amp;amp; Drop-Vorgänge erfolgreich ausgeführt werden können.  
  
### <a name="to-perform-a-drag-and-drop-procedure-between-applications"></a>So führen Sie ein Drag &amp; Drop-Verfahren zwischen Anwendungen aus  
  
1. Erstellen Sie eine neue Windows Forms-Anwendung.  
  
2. Fügen Sie Ihrem Formular ein <xref:System.Windows.Forms.TextBox>-Steuerelement hinzu.  
  
3. Konfigurieren Sie das <xref:System.Windows.Forms.TextBox>-Steuerelement, um abgelegte Daten zu empfangen.  
  
     Weitere Informationen finden Sie unter Exemplarische Vorgehens [Weise: Ausführen eines Drag & Drop-Vorgangs in Windows Forms](walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md).  
  
4. Führen Sie die Windows-basierte Anwendung aus. Während die Anwendung aktiv ist, führen Sie WordPad aus.  
  
     WordPad ist ein Text-Editor von Windows, der Drag & Drop-Vorgänge ermöglicht. Sie können darauf zugreifen, indem Sie auf die Schaltfläche **Start** klicken, **Ausführen** auswählen und dann `WordPad` in das Textfeld des Dialog Felds **Ausführen** eingeben und auf **OK** klicken.  
  
5. Sobald WordPad geöffnet ist, geben Sie eine Textzeichenfolge ein.  
  
6. Mit der Maus markieren Sie den Text, und ziehen Sie den markierten Text dann zum <xref:System.Windows.Forms.TextBox>-Steuerelement in der Windows-basierten Anwendung.  
  
     Wenn sich die Maus über dem <xref:System.Windows.Forms.TextBox>-Steuerelement befindet (und damit folglich das <xref:System.Windows.Forms.Control.DragEnter>-Ereignis ausgelöst wird), können Sie erkennen, dass sich der Cursor geändert hat. Sie können den markierten Text dann im <xref:System.Windows.Forms.TextBox>-Steuerelement ablegen.  
  
     Darüber hinaus können Sie das <xref:System.Windows.Forms.TextBox>-Steuerelement konfigurieren, damit Textzeichenfolgen per Drag &amp; Drop in WordPad eingefügt werden können. Weitere Informationen finden Sie unter Exemplarische Vorgehens [Weise: Ausführen eines Drag & Drop-Vorgangs in Windows Forms](walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md).  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Hinzufügen von Daten zur Zwischenablage](how-to-add-data-to-the-clipboard.md)
- [Vorgehensweise: Abrufen von Daten aus der Zwischenablage](how-to-retrieve-data-from-the-clipboard.md)
- [Drag &amp;amp; Drop-Operationen und Unterstützung der Zwischenablage](drag-and-drop-operations-and-clipboard-support.md)
