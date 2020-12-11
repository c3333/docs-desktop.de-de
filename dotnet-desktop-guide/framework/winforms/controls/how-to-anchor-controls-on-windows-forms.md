---
title: Verankern von Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- Anchor property [Windows Forms], enabling resizable forms
- Windows Forms controls, screen resolutions
- resizing forms [Windows Forms]
- Windows Forms controls, size
- screen resolution and control display
- controls [Windows Forms], anchoring
- forms [Windows Forms], resizing
- Windows Forms, resizing
- controls [Windows Forms], positioning
ms.assetid: 59ea914f-fbd3-427a-80fe-decd02f7ae6d
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 7c307d8c5b3bc32e15e6de048c434854ef1bbc65
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975732"
---
# <a name="how-to-anchor-controls-on-windows-forms"></a>Gewusst wie: Verankern von Steuerelementen auf Windows Forms

Wenn Sie ein Formular entwerfen, in dem der Benutzer zur Laufzeit die Größe ändern kann, sollten die Steuerelemente auf dem Formular die Größe ändern und die Position ordnungsgemäß ändern. Um die Größe der Steuerelemente dynamisch mit dem Formular zu ändern, können Sie die- <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaft von Windows Forms-Steuerelementen verwenden. Die- <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaft definiert eine Ankerposition für das-Steuerelement. Wenn ein Steuerelement in einem Formular verankert ist und die Größe des Formulars geändert wird, behält das Steuerelement den Abstand zwischen dem Steuerelement und den Anker Positionen. Wenn Sie z. b. ein Steuerelement haben, <xref:System.Windows.Forms.TextBox> das am linken, rechten und unteren Rand des Formulars verankert ist, während die Größe des Formulars geändert wird, <xref:System.Windows.Forms.TextBox> ändert sich das Steuerelement horizontal, sodass es die gleiche Entfernung von der rechten und linken Seite des Formulars erhält. Außerdem positioniert sich das Steuerelement selbst vertikal, sodass seine Position immer die gleiche Entfernung vom unteren Rand des Formulars ist. Wenn ein Steuerelement nicht verankert ist und die Größe des Formulars geändert wird, wird die Position des Steuer Elements relativ zu den Rändern des Formulars geändert.

Die- <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaft interagiert mit der- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft. Weitere Informationen finden Sie unter [Übersicht über die AutoSize-Eigenschaft](autosize-property-overview.md).

## <a name="anchor-a-control-on-a-form"></a>Verankern eines Steuer Elements in einem Formular

1. Wählen Sie in Visual Studio das Steuerelement aus, das Sie verankern möchten.

    > [!NOTE]
    > Sie können mehrere Steuerelemente gleichzeitig verankern, indem Sie die STRG-Taste drücken, auf jedes Steuerelement klicken, um es auszuwählen, und dann die restlichen Schritte dieses Verfahrens ausführen.

2. Klicken Sie im **Eigenschaften** Fenster auf den Pfeil rechts neben der- <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaft.

     Es wird ein Editor angezeigt, der eine Kreuz Darstellung anzeigt.

3. Um einen Anker festzulegen, klicken Sie auf den oberen, linken, rechten oder unteren Abschnitt des Kreuz-.

     Steuerelemente werden standardmäßig oben und Links verankert.

4. Um eine Seite des verankerten Steuer Elements zu löschen, klicken Sie auf den Arm des Kreuz-.

5. <xref:System.Windows.Forms.Control.Anchor%2A>Klicken Sie erneut auf den Eigenschaften Namen, um den Eigenschaften-Editor zu schließen <xref:System.Windows.Forms.Control.Anchor%2A> .

Wenn das Formular zur Laufzeit angezeigt wird, wird die Größe des Steuer Elements so geändert, dass es in der gleichen Entfernung vom Rand des Formulars positioniert bleibt. Der Abstand vom verankerten Rand bleibt immer identisch mit dem Abstand, der definiert wird, wenn das Steuerelement im Windows Forms-Designer positioniert ist.

> [!NOTE]
> Bestimmte Steuerelemente, z. b. das- <xref:System.Windows.Forms.ComboBox> Steuerelement, haben eine Beschränkung auf Ihre Höhe. Wenn das Steuerelement am unteren Rand des Formulars oder Containers verankert wird, kann das Steuerelement das Höhen Limit nicht überschreiten.

Geerbte Steuerelemente müssen in der Lage sein, verankert zu werden `Protected` . Um die Zugriffsebene eines Steuer Elements zu ändern, legen Sie die zugehörige- `Modifiers` Eigenschaft im **Eigenschaften** Fenster fest.

## <a name="see-also"></a>Siehe auch

- [Windows Forms Steuerelemente](index.md)
- [Übersicht über die AutoSize-Eigenschaft](autosize-property-overview.md)
- [Gewusst wie: Andocken von Steuerelementen in Windows Forms](how-to-dock-controls-on-windows-forms.md)
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [Exemplarische Vorgehensweise: Anordnen von Windows Forms-Steuerelementen mithilfe von Abständen, Rändern und der AutoSize-Eigenschaft](windows-forms-controls-padding-autosize.md)
