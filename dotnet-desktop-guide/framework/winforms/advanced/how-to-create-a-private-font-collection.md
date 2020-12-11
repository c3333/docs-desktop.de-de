---
title: 'Vorgehensweise: Erstellen einer privaten Schriftartenauflistung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- private font collections [Windows Forms], creating
- fonts [Windows Forms], creating private collections
ms.assetid: 6533d5e5-a8dc-4b76-9fc4-3bf75c8b9212
ms.openlocfilehash: 0bb7293a5423004a13cf98b79bba0a6c411a7c97
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974839"
---
# <a name="how-to-create-a-private-font-collection"></a>Vorgehensweise: Erstellen einer privaten Schriftartenauflistung
Die <xref:System.Drawing.Text.PrivateFontCollection> Klasse erbt von der <xref:System.Drawing.Text.FontCollection> abstrakten Basisklasse. Sie können ein- <xref:System.Drawing.Text.PrivateFontCollection> Objekt verwenden, um eine Reihe von Schriftarten speziell für Ihre Anwendung beizubehalten. Eine private Schriftart Auflistung kann installierte System Schriftarten und Schriftarten enthalten, die nicht auf dem Computer installiert wurden. Um einer privaten Schriftart Auflistung eine Schriftart Datei hinzuzufügen, müssen Sie die- <xref:System.Drawing.Text.PrivateFontCollection.AddFontFile%2A> Methode eines-Objekts aufzurufen <xref:System.Drawing.Text.PrivateFontCollection> .  
  
 Die- <xref:System.Drawing.Text.FontCollection.Families%2A> Eigenschaft eines- <xref:System.Drawing.Text.PrivateFontCollection> Objekts enthält ein Array von- <xref:System.Drawing.FontFamily> Objekten.  
  
 Die Anzahl der Schriftart Familien in einer privaten Schriftart Auflistung ist nicht notwendigerweise identisch mit der Anzahl der Schriftart Dateien, die der Sammlung hinzugefügt wurden. Nehmen Sie beispielsweise an, dass Sie die Dateien ArialBd. tff, Times. tff und TimesBd. tff einer Auflistung hinzufügen. Es gibt drei Dateien, aber nur zwei Familien in der Sammlung, da times. tff und TimesBd. tff derselben Familie angehören.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden die folgenden drei Schriftart Dateien zu einem-Objekt hinzugefügt <xref:System.Drawing.Text.PrivateFontCollection> :  
  
- C: \\ *systemroot*\fonz\arial.tff (Arial, Regular)  
  
- C: \\ *systemroot*\fonung\courbi.tff (Courier New, Fett kursiv)  
  
- C: \\ *systemroot*\fonz\timesbd.tff (Times New Roman, Bold)  
  
 Der Code Ruft ein Array von- <xref:System.Drawing.FontFamily> Objekten aus der- <xref:System.Drawing.Text.FontCollection.Families%2A> Eigenschaft des- <xref:System.Drawing.Text.PrivateFontCollection> Objekts ab.  
  
 <xref:System.Drawing.FontFamily>Der Code Ruft die-Methode für jedes Objekt in der Auflistung <xref:System.Drawing.FontFamily.IsStyleAvailable%2A> auf, um zu bestimmen, ob verschiedene Stile (regulär, Fett, kursiv, Fett kursiv, unterstrichen und durchgestrichen) verfügbar sind. Die an die Methode über gebenden Argumente <xref:System.Drawing.FontFamily.IsStyleAvailable%2A> sind Member der- <xref:System.Drawing.FontStyle> Enumeration.  
  
 Wenn eine bestimmte Kombination aus Familie und Stil verfügbar ist, <xref:System.Drawing.Font> wird ein-Objekt mit dieser Familie und diesem Stil erstellt. Das erste Argument, das an den <xref:System.Drawing.Font.%23ctor%2A> Konstruktor übergeben wird, ist der Schriftfamilien Name (kein- <xref:System.Drawing.FontFamily> Objekt, wie es bei anderen Variationen des Konstruktors der Fall ist <xref:System.Drawing.Font.%23ctor%2A> ). Nachdem das <xref:System.Drawing.Font> Objekt erstellt wurde, wird es an die- <xref:System.Drawing.Graphics.DrawString%2A> Methode der-Klasse weitergegeben, <xref:System.Drawing.Graphics> um den Familiennamen zusammen mit dem Namen des Stils anzuzeigen.  
  
 Die Ausgabe des folgenden Codes ähnelt der Ausgabe in der folgenden Abbildung:  
  
 ![Screenshot, der Text in verschiedenen Schriftarten anzeigt.](./media/how-to-create-a-private-font-collection/various-fonts-text-output.png)  
  
 Arial. tff (der der privaten Schriftart Auflistung im folgenden Codebeispiel hinzugefügt wurde) ist die Schriftart Datei für den normalen Arial-Stil. Beachten Sie jedoch, dass die Programmausgabe für die Schriftart der Arial-Schriftart verschiedene andere andere Formate als regulär anzeigt. Dies liegt daran, dass GDI+ die fetten, kursiv und Fetten kursiv formatierten Stile aus dem regulären Stil simulieren kann. GDI+ kann auch Unterstriche und Striche aus dem regulären Stil ergeben.  
  
 Ebenso kann GDI+ den fett formatierten Stil entweder aus dem fett formatierten Stil oder dem kursiv formatierten Stil simulieren. Die Programmausgabe zeigt, dass der Fett formatierte Stil für die Zeit Familie verfügbar ist, auch wenn TimesBd. tff (Times New Roman, Bold) die einzige Datei in der Sammlung ist.  
  
 [!code-csharp[System.Drawing.FontsAndText#51](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#51)]
 [!code-vb[System.Drawing.FontsAndText#51](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#51)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Text.PrivateFontCollection>
- [Verwenden von Schriftarten und Text](using-fonts-and-text.md)
