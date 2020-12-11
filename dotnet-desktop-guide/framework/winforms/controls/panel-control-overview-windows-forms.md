---
title: Übersicht über das Panel-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- Panel
helpviewer_keywords:
- grouping controls [Windows Forms], Panel control
- Panel control [Windows Forms], about Panel control
ms.assetid: b6b83636-2c39-4dad-89d6-f0fa41049a74
ms.openlocfilehash: 3ea86e898e8a3e1ca90ba8e0a6240414702a1a73
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976232"
---
# <a name="panel-control-overview-windows-forms"></a>Übersicht über das Panel-Steuerelement (Windows Forms)
Windows Forms Steuer <xref:System.Windows.Forms.Panel> Elemente werden verwendet, um eine identifizierbare Gruppierung für andere Steuerelemente bereitzustellen. In der Regel verwenden Sie Panels, um ein Formular nach Funktion zu unterteilen. Beispielsweise können Sie über ein Bestellformular verfügen, das Mailing Optionen angibt, z. b. den zu verwendenden Frachtunternehmen. Durch das Gruppieren aller Optionen in einem Panel erhält der Benutzer einen logischen visuellen Hinweis. Zur Entwurfszeit können alle Steuerelemente problemlos verschoben werden – wenn Sie das Steuerelement verschieben <xref:System.Windows.Forms.Panel> , werden auch alle darin enthaltenen Steuerelemente verschoben. Auf die in einem Panel gruppierten Steuerelemente kann über die-Eigenschaft zugegriffen werden <xref:System.Windows.Forms.Control.Controls%2A> . Diese Eigenschaft gibt eine Auflistung von- <xref:System.Windows.Forms.Control> Instanzen zurück, sodass Sie in der Regel ein Steuerelement, das auf diese Weise abgerufen wird, in den jeweiligen Typ umwandeln müssen.  
  
## <a name="panel-versus-groupbox"></a>Panel im Vergleich zu GroupBox  
 Das-Steuerelement <xref:System.Windows.Forms.Panel> ähnelt dem <xref:System.Windows.Forms.GroupBox> -Steuerelement. es kann jedoch nur das Steuerelement <xref:System.Windows.Forms.Panel> Scrollleisten aufweisen, und nur das <xref:System.Windows.Forms.GroupBox> Steuerelement zeigt eine Beschriftung an.  
  
## <a name="key-properties"></a>Schlüsseleigenschaften  
 Um Bild Lauf leisten anzuzeigen, legen <xref:System.Windows.Forms.ScrollableControl.AutoScroll%2A> Sie die-Eigenschaft auf fest `true` . Sie können die Darstellung des Panels auch anpassen, indem Sie die <xref:System.Windows.Forms.Control.BackColor%2A> <xref:System.Windows.Forms.Control.BackgroundImage%2A> Eigenschaften, und festlegen <xref:System.Windows.Forms.Panel.BorderStyle%2A> . Weitere Informationen zu den <xref:System.Windows.Forms.Control.BackColor%2A> Eigenschaften und <xref:System.Windows.Forms.Control.BackgroundImage%2A> finden Sie unter Gewusst [wie: Festlegen des Hintergrunds eines Panels](how-to-set-the-background-of-a-windows-forms-panel.md). Die- <xref:System.Windows.Forms.Panel.BorderStyle%2A> Eigenschaft bestimmt, ob der Bereich ohne sichtbaren Rahmen ( <xref:System.Windows.Forms.BorderStyle.None> ), eine einfache Linie ( <xref:System.Windows.Forms.BorderStyle.FixedSingle> ) oder eine Shadowing () angezeigt wird <xref:System.Windows.Forms.BorderStyle.Fixed3D> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Panel>
- [GroupBox-Steuerelement](groupbox-control-windows-forms.md)
- [Vorgehensweise: Gruppieren von Steuerelementen mit dem Windows Forms-Bereichssteuerelement im Designer](group-controls-with-wf-panel-control-using-the-designer.md)
- [Vorgehensweise: Festlegen des Hintergrunds eines Windows Forms-Bereichs mithilfe des Designers](how-to-set-the-background-of-a-windows-forms-panel-using-the-designer.md)
