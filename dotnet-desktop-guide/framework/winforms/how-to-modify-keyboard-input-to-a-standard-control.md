---
title: 'Vorgehensweise: Ändern von Tastatureingaben in ein Standardsteuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- keyboard input [Windows Forms], modifying
- modifying keyboard input
- Windows Forms, modifying keyboard input
- keyboards [Windows Forms], keyboard input
ms.assetid: 626d3712-d866-4988-bcda-a2d5b36ec0ba
ms.openlocfilehash: 1aa22501eb3d15b30be4ea4918473cf5a48cfe94
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976830"
---
# <a name="how-to-modify-keyboard-input-to-a-standard-control"></a>Vorgehensweise: Ändern von Tastatureingaben in ein Standardsteuerelement
Windows Forms bietet die Möglichkeit, Tastatureingaben zu nutzen und zu ändern. Nutzen einer Taste bezieht sich auf die Behandlung einer Taste innerhalb einer Methode oder eines Ereignishandlers, sodass andere Methoden und Ereignisse weiter unten in der Meldungswarteschlange den Tastenwert nicht empfangen. Ändern einer Taste bezieht sich auf ein Ändern des Werts einer Taste, sodass Methoden und Ereignishandler weiter unten in der Meldungswarteschlange einen anderen Tastenwert empfangen. In diesem Thema wird gezeigt, wie Sie diese Aufgaben ausführen.  
  
### <a name="to-consume-a-key"></a>So nutzen Sie eine Taste  
  
- Legen Sie in einem <xref:System.Windows.Forms.Control.KeyPress>-Ereignishandler die <xref:System.Windows.Forms.KeyPressEventArgs.Handled%2A>-Eigenschaft der <xref:System.Windows.Forms.KeyPressEventArgs>-Klasse auf `true` fest.  
  
     Oder  
  
     Legen Sie in einem <xref:System.Windows.Forms.Control.KeyDown>-Ereignishandler die <xref:System.Windows.Forms.KeyEventArgs.Handled%2A>-Eigenschaft der <xref:System.Windows.Forms.KeyEventArgs>-Klasse auf `true` fest.  
  
    > [!NOTE]
    > Ein Festlegen der <xref:System.Windows.Forms.KeyEventArgs.Handled%2A>-Eigenschaft im <xref:System.Windows.Forms.Control.KeyDown>-Ereignishandler verhindert nicht, dass das <xref:System.Windows.Forms.Control.KeyPress>- und das <xref:System.Windows.Forms.Control.KeyUp>-Ereignis für die aktuelle Tastatureingabe ausgelöst werden. Verwenden Sie die <xref:System.Windows.Forms.KeyEventArgs.SuppressKeyPress%2A>-Eigenschaft für diesen Zweck.  
  
     Das folgende Beispiel ist ein Auszug aus einer `switch`-Anweisung, von der die <xref:System.Windows.Forms.KeyPressEventArgs.KeyChar%2A>-Eigenschaft der <xref:System.Windows.Forms.KeyPressEventArgs>-Klasse ausgewertet wird, die von einem <xref:System.Windows.Forms.Control.KeyPress>-Ereignishandler empfangen wurde. In diesem Code werden die Zeichentasten 'A' und 'a' genutzt.  
  
     [!code-csharp[System.Windows.Forms.KeyBoardInput#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInput/CS/form1.cs#6)]
     [!code-vb[System.Windows.Forms.KeyBoardInput#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInput/VB/form1.vb#6)]  
  
### <a name="to-modify-a-standard-character-key"></a>So ändern Sie eine Standardzeichentaste  
  
- Legen Sie in einem <xref:System.Windows.Forms.Control.KeyPress>-Ereignishandler die <xref:System.Windows.Forms.KeyPressEventArgs.KeyChar%2A>-Eigenschaft der <xref:System.Windows.Forms.KeyPressEventArgs>-Klasse auf den Wert der neuen Zeichentaste fest.  
  
     Das folgende Beispiel ist ein Auszug aus einer `switch`-Anweisung, in der 'B' in 'A' und 'b' in 'a' geändert wird. Beachten Sie, dass die <xref:System.Windows.Forms.KeyPressEventArgs.Handled%2A>-Eigenschaft des <xref:System.Windows.Forms.KeyPressEventArgs>-Parameters auf `false` festgelegt wird, sodass der neue Tastenwert an andere Methoden und Ereignisse in der Meldungswarteschlange weitergegeben wird.  
  
     [!code-csharp[System.Windows.Forms.KeyBoardInput#7](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInput/CS/form1.cs#7)]
     [!code-vb[System.Windows.Forms.KeyBoardInput#7](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInput/VB/form1.vb#7)]  
  
### <a name="to-modify-a-noncharacter-key"></a>So ändern Sie eine Nicht-Zeichentaste  
  
- Überschreiben Sie eine <xref:System.Windows.Forms.Control>-Methode, von der Windows-Meldungen verarbeitet werden, suchen Sie die Meldung WM_KEYDOWN oder WM_SYSKEYDOWN, und legen Sie die <xref:System.Windows.Forms.Message.WParam%2A>-Eigenschaft des <xref:System.Windows.Forms.Message>-Parameters auf den <xref:System.Windows.Forms.Keys>-Wert fest, der den neuen Wert der Nicht-Zeichentaste darstellt.  
  
     Im folgenden Codebeispiel wird veranschaulicht, wie Sie die <xref:System.Windows.Forms.Control.PreProcessMessage%2A>-Methode eines Steuerelements überschreiben, um die Tasten F1 bis F9 zu erkennen und jede Betätigung der Taste F3 in F1 zu ändern. Weitere Informationen <xref:System.Windows.Forms.Control> zu Methoden, die Sie zum Abfangen von Tastatur Meldungen außer Kraft setzen können, finden Sie unter [Benutzereingabe in einer Windows Forms Anwendung](user-input-in-a-windows-forms-application.md) und [Funktionsweise von Tastatureingaben](how-keyboard-input-works.md).  
  
     [!code-csharp[System.Windows.Forms.KeyBoardInput#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInput/CS/form1.cs#12)]
     [!code-vb[System.Windows.Forms.KeyBoardInput#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInput/VB/form1.vb#12)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird die vollständige Anwendung für die Codebeispiele aus den vorherigen Abschnitten dargestellt. In der Anwendung wird ein benutzerdefiniertes Steuerelement, das aus der <xref:System.Windows.Forms.TextBox>-Klasse abgeleitet wurde, dazu verwendet, Tastatureingaben zu nutzen und zu ändern.  
  
 [!code-csharp[System.Windows.Forms.KeyBoardInput#0](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInput/CS/form1.cs#0)]
 [!code-vb[System.Windows.Forms.KeyBoardInput#0](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInput/VB/form1.vb#0)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".  
  
## <a name="see-also"></a>Siehe auch

- [Tastatureingaben in einer Windows Forms-Anwendung](keyboard-input-in-a-windows-forms-application.md)
- [Benutzereingabe in einer Windows Forms-Anwendung](user-input-in-a-windows-forms-application.md)
- [Funktionsweise von Tastatureingaben](how-keyboard-input-works.md)
