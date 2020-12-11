---
title: 'Vorgehensweise: Ausblenden von ToolStripMenuItems mithilfe des Designers'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], hiding menu items in designer
- MenuStrip control [Windows Forms], hiding menu items in designer
- menu items [Windows Forms], hiding
ms.assetid: 8f1b057e-3d8a-4f11-88df-935f7b29a836
ms.openlocfilehash: 0e1cd7d1868adabd4d3eec9510f6ee567ba3867d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975633"
---
# <a name="how-to-hide-toolstripmenuitems-using-the-designer"></a>Vorgehensweise: Ausblenden von ToolStripMenuItems mithilfe des Designers
Das Ausblenden von Menü Elementen ist eine Möglichkeit, die Benutzeroberfläche (UI) Ihrer Anwendung zu steuern und Benutzer Befehle einzuschränken. Häufig ist es ratsam, ein gesamtes Menü auszublenden, wenn alle Menü Elemente darin nicht verfügbar sind. Dies stellt weniger Ablenkungen für den Benutzer dar. Außerdem empfiehlt es sich, das Menü oder das Menü Element auszublenden und zu deaktivieren, da durch das Ausblenden allein nicht verhindert wird, dass der Benutzer über eine Tastenkombination auf einen Menübefehl zugreift. Weitere Informationen zum Deaktivieren von Menü Elementen finden Sie unter Gewusst [wie: Deaktivieren von ToolStripMenuItems mithilfe des Designers](how-to-disable-toolstripmenuitems-using-the-designer.md).

## <a name="to-hide-a-top-level-menu-and-its-submenu-items"></a>So blenden Sie ein Menü der obersten Ebene und seine unter Menü Elemente aus

1. Wählen Sie das Menü Element der obersten Ebene aus, und legen Sie die- <xref:System.Windows.Forms.ToolStripItem.Visible%2A> oder- <xref:System.Windows.Forms.ToolStripItem.Available%2A> Eigenschaft auf fest `false`

     Wenn Sie das Menü Element der obersten Ebene ausblenden, werden alle Menü Elemente in diesem Menü ebenfalls ausgeblendet. Wenn Sie auf eine andere Stelle als auf der nach-Einstellung auf klicken <xref:System.Windows.Forms.MenuStrip> <xref:System.Windows.Forms.ToolStripItem.Visible%2A> `false` , werden das gesamte Menü Element der obersten Ebene und seine unter Menü Elemente aus dem Formular entfernt, sodass Sie die Lauf Zeit Wirkung ihrer Aktion angezeigt werden. Um das ausgeblendete Menü Element der obersten Ebene zur Entwurfszeit anzuzeigen, klicken Sie <xref:System.Windows.Forms.MenuStrip> in der **Komponenten Leiste**, in der **Dokument** Gliederung oder am oberen Rand des Eigenschaften Rasters auf das.

> [!NOTE]
> Sie werden in einem Zusammenführungs Szenario selten ein gesamtes Menü mit Ausnahme von untergeordneten MDI-Menüs (Multiple Document Interface) ausblenden.

## <a name="to-hide-a-submenu-item"></a>So blenden Sie ein unter Menü Element aus

1. Wählen Sie das unter Menü Element, und legen Sie dessen- <xref:System.Windows.Forms.ToolStripItem.Visible%2A> Eigenschaft auf fest `false` .

     Wenn Sie ein unter Menü Element ausblenden, bleibt es zur Entwurfszeit auf dem Formular sichtbar, sodass Sie es für weitere Aufgaben problemlos auswählen können. Sie wird zur Laufzeit ausgeblendet.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStripItem.Visible%2A>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A>
- <xref:System.Windows.Forms.ToolStripItem.Available%2A>
- <xref:System.Windows.Forms.ToolStripMenuItem.Overflow%2A>
- [Übersicht über das MenuStrip-Steuerelement](menustrip-control-overview-windows-forms.md)
- [Vorgehensweise: Deaktivieren von ToolStripMenuItems mithilfe des Designers](how-to-disable-toolstripmenuitems-using-the-designer.md)
