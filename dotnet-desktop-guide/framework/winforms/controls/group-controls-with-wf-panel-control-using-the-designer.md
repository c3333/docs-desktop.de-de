---
title: Gruppieren von Steuerelementen mit Panel-Steuerelement mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- Panel control [Windows Forms], grouping controls
- controls [Windows Forms], grouping
- Windows Forms controls, grouping
ms.assetid: 7e1cd708-fdb1-49d8-9ca2-5640b276bf2e
ms.openlocfilehash: 927aeb5b51bc1ac4e22a45e487b49424b4e67b71
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972104"
---
# <a name="how-to-group-controls-with-the-windows-forms-panel-control-using-the-designer"></a>Vorgehensweise: Gruppieren von Steuerelementen mit dem Windows Forms-Bereichssteuerelement im Designer
Windows Forms-Steuer <xref:System.Windows.Forms.Panel> Elemente werden verwendet, um andere Steuerelemente zu gruppieren. Es gibt drei Gründe für das Gruppieren von Steuerelementen. Eine ist die visuelle Gruppierung verwandter Formularelemente für eine eindeutige Benutzeroberfläche. eine andere ist die programmatische Gruppierung von Options Feldern, z. b.. die letzte dient zum Verschieben der Steuerelemente als Einheit zur Entwurfszeit.

## <a name="to-create-a-group-of-controls"></a>So erstellen Sie eine Gruppe von Steuerelementen

1. Ziehen Sie ein- <xref:System.Windows.Forms.Panel> Steuerelement von der Registerkarte **Windows Forms** der Toolbox auf ein Formular.

2. Fügen Sie dem Panel weitere Steuerelemente hinzu, und zeichnen Sie die einzelnen Elemente innerhalb des Panels.

     Wenn Sie über vorhandene Steuerelemente verfügen, die Sie in einem Panel einschließen möchten, können Sie alle Steuerelemente auswählen, Sie in die Zwischenablage Ausschneiden, das Steuerelement auswählen <xref:System.Windows.Forms.Panel> und dann in das Panel einfügen. Sie können Sie auch in das Panel ziehen.

3. Optionale Wenn Sie einem Panel einen Rahmen hinzufügen möchten, legen Sie dessen- <xref:System.Windows.Forms.BorderStyle> Eigenschaft fest. Es gibt drei Optionen: <xref:System.Windows.Forms.BorderStyle.Fixed3D> , <xref:System.Windows.Forms.BorderStyle.FixedSingle> und <xref:System.Windows.Forms.BorderStyle.None> .

## <a name="see-also"></a>Siehe auch

- [Panelsteuerelement](panel-control-windows-forms.md)
- [Übersicht über das Panel-Steuerelement](panel-control-overview-windows-forms.md)
- [Vorgehensweise: Festlegen des Hintergrunds eines Bereichs](how-to-set-the-background-of-a-windows-forms-panel.md)
