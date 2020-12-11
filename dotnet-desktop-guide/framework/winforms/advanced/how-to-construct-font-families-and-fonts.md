---
title: 'Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- font families [Windows Forms], constructing
- fonts [Windows Forms], constructing
ms.assetid: d3a4a223-9492-4b54-9afd-db1c31c3cefd
ms.openlocfilehash: 2d609525858c7a8ff77c0b86900b4fc7d6b4e39a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972380"
---
# <a name="how-to-construct-font-families-and-fonts"></a>Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten
GDI+ gruppiert Schriftarten mit derselben Schriftart, aber unterschiedlichen Stilen in Schriftfamilien. Beispielsweise enthält die Familie "Arial Font" die folgenden Schriftarten:  
  
- Arial Normal  
  
- Arial Fett  
  
- Arial kursiv  
  
- Arial Fett kursiv  
  
 GDI+ verwendet vier Stile zum bilden von Familien: regulär, Fett, kursiv und fett formatiert. Adjektive, z. b. *schmale* und *abgerundete* , werden nicht als Stile betrachtet. Sie sind nicht Teil des Familiennamens. Beispielsweise ist Arial Narrow eine Schriftfamilie mit den folgenden Membern:  
  
- Arial schmale reguläre  
  
- Arial schmale Fett Formatierung  
  
- Arial, schmale kursiv  
  
- Arial schmale Fett kursiv  
  
 Bevor Sie Text mit GDI+ zeichnen können, müssen Sie ein <xref:System.Drawing.FontFamily> -Objekt und ein- <xref:System.Drawing.Font> Objekt erstellen. Das <xref:System.Drawing.FontFamily> -Objekt gibt die Schriftart (z. b. Arial) an, und das- <xref:System.Drawing.Font> Objekt gibt die Größe, den Stil und die Einheiten an.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine Schriftart mit einem regulären Stil mit einer Größe von 16 Pixeln erstellt. Im folgenden Code ist das erste Argument, das an den- <xref:System.Drawing.Font.%23ctor%2A> Konstruktor übergeben wird, das- <xref:System.Drawing.FontFamily> Objekt. Das zweite Argument gibt die Größe der Schriftart an, die in Einheiten gemessen wird, die durch das vierte Argument identifiziert werden. Das dritte Argument identifiziert den Stil.  
  
 <xref:System.Drawing.GraphicsUnit.Pixel> ist ein Member der <xref:System.Drawing.GraphicsUnit> -Enumeration und <xref:System.Drawing.FontStyle.Regular> ist ein Member der- <xref:System.Drawing.FontStyle> Enumeration.  
  
 [!code-csharp[System.Drawing.FontsAndText#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.FontsAndText#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von Schriftarten und Text](using-fonts-and-text.md)
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
