---
title: Verhindern der Addition und Löschung von Zeilen im DataGridView-Steuerelement mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], preventing row addition or deletion
ms.assetid: a17722bd-9400-41e6-8dcc-c9c151f0a749
ms.openlocfilehash: cca497aeaedd0c9f988241092eed707ecc259859
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976214"
---
# <a name="how-to-prevent-row-addition-and-deletion-in-the-windows-forms-datagridview-control-using-the-designer"></a>Vorgehensweise: Verhindern des Hinzufügens und Löschens von Zeilen im DataGridView-Steuerelement in Windows Forms mithilfe des Designers
Gelegentlich möchten Sie Benutzer daran hindern, neue Zeilen von Daten einzugeben oder vorhandene Zeilen in Ihrem <xref:System.Windows.Forms.DataGridView>-Steuerelement zu löschen. Neue Zeilen werden in der speziellen Zeile für neue Datensätze am unteren Rand des Steuer Elements eingegeben. Wenn Sie die Zeilen Addition deaktivieren, wird die Zeile für neue Datensätze nicht angezeigt. Sie können das Steuerelement dann vollständig schreibgeschützt machen, indem Sie Zeilen Löschung und Zellen Bearbeitung deaktivieren.

 Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein-Steuerelement enthält <xref:System.Windows.Forms.DataGridView> . Weitere Informationen zum Einrichten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).

## <a name="to-prevent-row-addition-and-deletion"></a>So verhindern Sie das Hinzufügen und Löschen von Zeilen

- Klicken Sie ![ in der oberen rechten Ecke des Steuer Elements auf das Symbol Designer Aktionen (kleiner schwarzer Pfeil ](./media/designer-actions-glyph.gif) ) <xref:System.Windows.Forms.DataGridView> , und deaktivieren Sie dann die Kontrollkästchen **hinzufügen aktivieren** und **Löschen aktivieren** .

    > [!NOTE]
    > Deaktivieren Sie das Kontrollkästchen **Bearbeitung aktivieren** , damit das Steuerelement vollständig schreibgeschützt ist.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A?displayProperty=nameWithType>
- [Vorgehensweise: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [How to: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md)
