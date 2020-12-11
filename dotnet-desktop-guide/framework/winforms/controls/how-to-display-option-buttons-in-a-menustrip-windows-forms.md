---
title: 'Vorgehensweise: Anzeigen von Optionsfeldern in einem MenuStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- MenuStrip [Windows Forms], displaying option buttons
- displaying option buttons [Windows Forms], MenuStrip [Windows Forms]
- option buttons [Windows Forms], displaying in MenuStrip
ms.assetid: 8b596af2-9ff8-4f7b-93d7-cba830e167f4
ms.openlocfilehash: f3010e71396ce562e9dbdefd4b75b36f3a81ffb3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976518"
---
# <a name="how-to-display-option-buttons-in-a-menustrip-windows-forms"></a>Gewusst wie: Anzeigen von Optionsfeldern in einem MenuStrip (Windows Forms)

Options Felder, auch als Options Felder bezeichnet, ähneln Kontrollkästchen, mit dem Unterschied, dass Benutzer jeweils nur eine auswählen können. Obwohl die <xref:System.Windows.Forms.ToolStripMenuItem> -Klasse standardmäßig kein Optionsfeld Verhalten bereitstellt, stellt die-Klasse ein Kontrollkästchen Verhalten bereit, das Sie anpassen können, um das Optionsfeld Verhalten für Menü Elemente in einem-Steuerelement zu implementieren <xref:System.Windows.Forms.MenuStrip> .

Wenn die- <xref:System.Windows.Forms.ToolStripMenuItem.CheckOnClick%2A> Eigenschaft eines Menü Elements ist `true` , können Benutzer auf das Element klicken, um die Anzeige eines Häkchens ein-und auszuschalten. Die- <xref:System.Windows.Forms.ToolStripMenuItem.Checked%2A> Eigenschaft gibt den aktuellen Zustand des Elements an. Wenn Sie das grundlegende Optionsfeld Verhalten implementieren möchten, müssen Sie sicherstellen, dass die- <xref:System.Windows.Forms.ToolStripMenuItem.Checked%2A> Eigenschaft für das zuvor ausgewählte Element auf festgelegt ist, wenn ein Element ausgewählt ist `false` .

In den folgenden Prozeduren wird beschrieben, wie diese und zusätzliche Funktionen in einer Klasse implementiert werden, die die-Klasse erbt <xref:System.Windows.Forms.ToolStripMenuItem> . Die `ToolStripRadioButtonMenuItem` -Klasse überschreibt Member wie <xref:System.Windows.Forms.ToolStripMenuItem.OnCheckedChanged%2A> und <xref:System.Windows.Forms.ToolStripMenuItem.OnPaint%2A> , um das Auswahl Verhalten und die Darstellung von Options Schaltflächen bereitzustellen. Darüber hinaus überschreibt diese Klasse die- <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> Eigenschaft, sodass Optionen in einem Untermenü deaktiviert werden, es sei denn, das übergeordnete Element ist ausgewählt.

## <a name="to-implement-option-button-selection-behavior"></a>So implementieren Sie das Auswahl Verhalten für die Options Schaltfläche

1. Initialisieren Sie die- <xref:System.Windows.Forms.ToolStripMenuItem.CheckOnClick%2A> Eigenschaft, um die `true` Elementauswahl zu aktivieren.

     [!code-csharp[ToolStripRadioButtonMenuItem#110](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/cs/ToolStripRadioButtonMenuItem.cs#110)]
     [!code-vb[ToolStripRadioButtonMenuItem#110](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/vb/ToolStripRadioButtonMenuItem.vb#110)]

2. Überschreiben <xref:System.Windows.Forms.ToolStripMenuItem.OnCheckedChanged%2A> Sie die-Methode, um die Auswahl des zuvor ausgewählten Elements zu löschen, wenn ein neues Element ausgewählt wird.

     [!code-csharp[ToolStripRadioButtonMenuItem#120](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/cs/ToolStripRadioButtonMenuItem.cs#120)]
     [!code-vb[ToolStripRadioButtonMenuItem#120](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/vb/ToolStripRadioButtonMenuItem.vb#120)]

3. Überschreiben <xref:System.Windows.Forms.ToolStripMenuItem.OnClick%2A> Sie die-Methode, um sicherzustellen, dass das Klicken auf ein Element, das bereits ausgewählt wurde, die Auswahl nicht löscht.

     [!code-csharp[ToolStripRadioButtonMenuItem#130](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/cs/ToolStripRadioButtonMenuItem.cs#130)]
     [!code-vb[ToolStripRadioButtonMenuItem#130](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/vb/ToolStripRadioButtonMenuItem.vb#130)]

## <a name="to-modify-the-appearance-of-the-option-button-items"></a>So ändern Sie die Darstellung der Optionsfeld Elemente

1. Überschreiben Sie die- <xref:System.Windows.Forms.ToolStripMenuItem.OnPaint%2A> Methode, um das Standard Häkchen durch ein Optionsfeld zu ersetzen, indem Sie die- <xref:System.Windows.Forms.RadioButtonRenderer> Klasse verwenden.

     [!code-csharp[ToolStripRadioButtonMenuItem#140](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/cs/ToolStripRadioButtonMenuItem.cs#140)]
     [!code-vb[ToolStripRadioButtonMenuItem#140](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/vb/ToolStripRadioButtonMenuItem.vb#140)]

2. Überschreiben <xref:System.Windows.Forms.ToolStripMenuItem.OnMouseEnter%2A> <xref:System.Windows.Forms.ToolStripMenuItem.OnMouseLeave%2A> Sie die Methoden,, und, <xref:System.Windows.Forms.ToolStripMenuItem.OnMouseDown%2A> <xref:System.Windows.Forms.ToolStripMenuItem.OnMouseUp%2A> um den Zustand der Maus zu verfolgen und sicherzustellen, dass die <xref:System.Windows.Forms.ToolStripMenuItem.OnPaint%2A> -Methode den richtigen Optionsfeld Zustand zeichnet.

     [!code-csharp[ToolStripRadioButtonMenuItem#150](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/cs/ToolStripRadioButtonMenuItem.cs#150)]
     [!code-vb[ToolStripRadioButtonMenuItem#150](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/vb/ToolStripRadioButtonMenuItem.vb#150)]

## <a name="to-disable-options-on-a-submenu-when-the-parent-item-is-not-selected"></a>So deaktivieren Sie Optionen in einem Untermenü, wenn das übergeordnete Element nicht ausgewählt ist

1. Überschreiben <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> Sie die-Eigenschaft, sodass das Element deaktiviert ist, wenn es über ein übergeordnetes Element mit dem <xref:System.Windows.Forms.ToolStripMenuItem.CheckOnClick%2A> Wert `true` und dem Wert verfügt <xref:System.Windows.Forms.ToolStripMenuItem.Checked%2A> `false` .

     [!code-csharp[ToolStripRadioButtonMenuItem#160](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/cs/ToolStripRadioButtonMenuItem.cs#160)]
     [!code-vb[ToolStripRadioButtonMenuItem#160](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/vb/ToolStripRadioButtonMenuItem.vb#160)]

2. Überschreiben Sie die- <xref:System.Windows.Forms.ToolStripMenuItem.OnOwnerChanged%2A> Methode, um das- <xref:System.Windows.Forms.ToolStripMenuItem.CheckedChanged> Ereignis des übergeordneten Elements zu abonnieren.

     [!code-csharp[ToolStripRadioButtonMenuItem#170](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/cs/ToolStripRadioButtonMenuItem.cs#170)]
     [!code-vb[ToolStripRadioButtonMenuItem#170](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/vb/ToolStripRadioButtonMenuItem.vb#170)]

3. Im Handler für das übergeordnete Element- <xref:System.Windows.Forms.ToolStripMenuItem.CheckedChanged> Ereignis wird das Element für ungültig erklärt, um die Anzeige mit dem neuen aktivierten Zustand zu aktualisieren.

     [!code-csharp[ToolStripRadioButtonMenuItem#180](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/cs/ToolStripRadioButtonMenuItem.cs#180)]
     [!code-vb[ToolStripRadioButtonMenuItem#180](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/vb/ToolStripRadioButtonMenuItem.vb#180)]

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird die gesamte `ToolStripRadioButtonMenuItem` -Klasse und eine-Klasse und eine-Klasse bereitgestellt, <xref:System.Windows.Forms.Form> `Program` um das Optionsfeld Verhalten zu veranschaulichen.

[!code-csharp[ToolStripRadioButtonMenuItem#000](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/cs/ToolStripRadioButtonMenuItem.cs#000)]
[!code-vb[ToolStripRadioButtonMenuItem#000](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripRadioButtonMenuItem/vb/ToolStripRadioButtonMenuItem.vb#000)]

## <a name="compiling-the-code"></a>Kompilieren des Codes

Für dieses Beispiel benötigen Sie Folgendes:

- Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- <xref:System.Windows.Forms.ToolStripMenuItem.CheckOnClick%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ToolStripMenuItem.Checked%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ToolStripMenuItem.OnCheckedChanged%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ToolStripMenuItem.OnPaint%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.RadioButtonRenderer>
- [MenuStrip-Steuerelement](menustrip-control-windows-forms.md)
- [Vorgehensweise: Implementieren eines benutzerdefinierten ToolStripRenderer](how-to-implement-a-custom-toolstriprenderer.md)
