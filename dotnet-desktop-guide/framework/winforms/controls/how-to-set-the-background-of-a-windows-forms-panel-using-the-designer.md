---
title: Festlegen des Hintergrunds eines Panels mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- background colors [Windows Forms], Windows Forms Panel controls
- background images [Windows Forms], Windows Forms Panel controls
- Panel control [Windows Forms], background
- colors [Windows Forms], Windows Forms Panel controls
ms.assetid: db83cf54-3c69-4b08-ac6c-25b9b5abb1b0
ms.openlocfilehash: 8bdefba433632f7ba02f549a549c52c7aa56c2d7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976764"
---
# <a name="how-to-set-the-background-of-a-windows-forms-panel-using-the-designer"></a>Gewusst wie: Festlegen des Hintergrunds eines Windows Forms Panels mithilfe des Designers

Ein Windows Forms <xref:System.Windows.Forms.Panel> -Steuerelement kann sowohl eine Hintergrundfarbe als auch ein Hintergrundbild anzeigen. Die- <xref:System.Windows.Forms.Control.BackColor%2A> Eigenschaft legt die Hintergrundfarbe für Steuerelemente fest, die im Bereich enthalten sind, z. b. Bezeichnungen und Options Felder. Wenn die <xref:System.Windows.Forms.Control.BackgroundImage%2A> Eigenschaft nicht festgelegt ist, <xref:System.Windows.Forms.Control.BackColor%2A> wird der gesamte Bereich durch die Auswahl ausgefüllt. Wenn die- <xref:System.Windows.Forms.Control.BackgroundImage%2A> Eigenschaft festgelegt ist, wird das Bild hinter den Steuerelementen angezeigt, die im Bereich enthalten sind.

Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein-Steuerelement enthält <xref:System.Windows.Forms.Panel> . Weitere Informationen zum Einrichten eines solchen Projekts in Visual Studio finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).

## <a name="set-the-background-in-the-windows-forms-designer"></a>Legen Sie den Hintergrund im Windows Forms-Designer

1. Öffnen Sie das Projekt in Visual Studio, und wählen Sie das Steuerelement aus <xref:System.Windows.Forms.Panel> .

2. Klicken Sie im Fenster **Eigenschaften** neben der-Eigenschaft auf die Pfeil Schaltfläche, <xref:System.Windows.Forms.Control.BackColor%2A> um ein Fenster mit drei Registerkarten anzuzeigen.

3. Wählen Sie die Registerkarte **Benutzer** definiert aus, um eine Palette von Farben anzuzeigen.

4. Wählen Sie die Registerkarte **Web** oder **System** aus, um eine Liste vordefinierter Namen für Farben anzuzeigen, und wählen Sie dann eine Farbe aus.

5. Klicken Sie im Fenster **Eigenschaften** neben der-Eigenschaft auf die Pfeil Schaltfläche <xref:System.Windows.Forms.Control.BackgroundImage%2A> .

6. Wählen Sie im Dialogfeld **Öffnen** die Datei aus, die Sie anzeigen möchten.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Control.BackColor%2A>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
- [Panelsteuerelement](panel-control-windows-forms.md)
- [Übersicht über das Panel-Steuerelement](panel-control-overview-windows-forms.md)
- [Vorgehensweise: Gruppieren von Steuerelementen mit dem Windows Forms-Bereichssteuerelement im Designer](group-controls-with-wf-panel-control-using-the-designer.md)
