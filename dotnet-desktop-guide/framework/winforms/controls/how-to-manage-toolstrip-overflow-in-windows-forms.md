---
title: 'Vorgehensweise: Umgang mit dem ToolStrip-Überlauf'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], managing overflow
- toolbars [Windows Forms], managing overflow
- examples [Windows Forms], toolbars
- CanOverflow property
ms.assetid: fa10e0ad-4cbf-4c0d-9082-359c2f855d4e
ms.openlocfilehash: 52cc02e626bee2d2457355028ecddc17e462d8fa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974803"
---
# <a name="how-to-manage-toolstrip-overflow-in-windows-forms"></a>Gewusst wie: Umgang mit dem ToolStrip-Überlauf in Windows Forms

Wenn alle Elemente in einem <xref:System.Windows.Forms.ToolStrip> -Steuerelement nicht in den zugewiesenen Speicherplatz passen, können Sie die Überlauf Funktion für die aktivieren <xref:System.Windows.Forms.ToolStrip> und das Überlauf Verhalten bestimmter <xref:System.Windows.Forms.ToolStripItem> s bestimmen.

Wenn Sie s hinzufügen <xref:System.Windows.Forms.ToolStripItem> , die mehr Speicherplatz benötigen, als für die <xref:System.Windows.Forms.ToolStrip> aktuelle Größe des Formulars zugewiesen ist, wird <xref:System.Windows.Forms.ToolStripOverflowButton> automatisch auf dem angezeigt <xref:System.Windows.Forms.ToolStrip> . Die <xref:System.Windows.Forms.ToolStripOverflowButton> angezeigten Elemente und Überlauf aktivierte Elemente werden in das Dropdown Menü Überlauf verschoben. Auf diese Weise können Sie anpassen und priorisieren, wie Ihre <xref:System.Windows.Forms.ToolStrip> Elemente ordnungsgemäß an verschiedene Formular Größen angepasst werden. Sie können auch die Darstellung Ihrer Elemente ändern, wenn Sie in den Überlauf geraten, indem Sie die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.ToolStripItem.Placement%2A> <xref:System.Windows.Forms.ToolStripOverflow.DisplayedItems%2A?displayProperty=nameWithType> sowie das- <xref:System.Windows.Forms.ToolStrip.LayoutCompleted> Ereignis verwenden. Wenn Sie das Formular entweder zur Entwurfszeit oder zur Laufzeit vergrößern, <xref:System.Windows.Forms.ToolStripItem> können weitere s auf dem Hauptfenster angezeigt werden, <xref:System.Windows.Forms.ToolStrip> und die wird <xref:System.Windows.Forms.ToolStripOverflowButton> möglicherweise sogar ausgeblendet, bis Sie die Größe des Formulars verringern.

## <a name="to-enable-overflow-on-a-toolstrip-control"></a>So aktivieren Sie den Überlauf für ein ToolStrip-Steuerelement

- Stellen Sie sicher, dass die- <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> Eigenschaft nicht auf für festgelegt ist `false` <xref:System.Windows.Forms.ToolStrip> . Der Standardwert ist `True`.

     Wenn <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> ist `True` (der Standardwert), <xref:System.Windows.Forms.ToolStripItem> wird eine an das Dropdown-Überlauf Menü gesendet, wenn der Inhalt von <xref:System.Windows.Forms.ToolStripItem> die Breite eines horizontalen <xref:System.Windows.Forms.ToolStrip> oder der Höhe eines vertikalen überschreitet <xref:System.Windows.Forms.ToolStrip> .

## <a name="to-specify-overflow-behavior-of-a-specific-toolstripitem"></a>So geben Sie das Überlauf Verhalten eines bestimmten Tool Strip Item an

- Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> Eigenschaft des <xref:System.Windows.Forms.ToolStripItem> auf den gewünschten Wert fest. Die Möglichkeiten sind `Always` , `Never` und `AsNeeded` . Der Standardwert ist `AsNeeded`.

    ```vb
    toolStripTextBox1.Overflow = _
    System.Windows.Forms.ToolStripItemOverflow.Never
    ```

    ```csharp
    toolStripTextBox1.Overflow = _
    System.Windows.Forms.ToolStripItemOverflow.Never;
    ```

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripOverflowButton>
- <xref:System.Windows.Forms.ToolStripItem.Overflow%2A>
- <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A>
- [Übersicht über das ToolStrip-Steuerelement](toolstrip-control-overview-windows-forms.md)
- [Architektur des ToolStrip-Steuerelements](toolstrip-control-architecture.md)
- [Zusammenfassung der ToolStrip-Technologie](toolstrip-technology-summary.md)
