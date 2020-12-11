---
title: 'Vorgehensweise: Überspannen von Zeilen und Spalten in einem TableLayoutPanel-Steuerelement'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.SpanRowsColumns
helpviewer_keywords:
- columns [Windows Forms], spanning
- merging cells
- TableLayoutPanel control [Windows Forms], spanning rows and columns
- rows [Windows Forms], spanning
- cells [Windows Forms], merging
ms.assetid: a8a2fdd3-a848-48b0-a4cd-4e85ebded87e
ms.openlocfilehash: a215b2b4e05bab5c81d2779d4b67d5b9d57b6ba5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976745"
---
# <a name="how-to-span-rows-and-columns-in-a-tablelayoutpanel-control"></a>Vorgehensweise: Überspannen von Zeilen und Spalten in einem TableLayoutPanel-Steuerelement
Steuerelemente in einem <xref:System.Windows.Forms.TableLayoutPanel> -Steuerelement können angrenzende Zeilen und Spalten umfassen.

## <a name="to-span-columns-and-rows"></a>Zum Spannen von Spalten und Zeilen

1. Ziehen Sie ein <xref:System.Windows.Forms.TableLayoutPanel> -Steuerelement aus der **Toolbox** auf das Formular.

2. Ziehen Sie ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** in die linke obere Zelle des- <xref:System.Windows.Forms.TableLayoutPanel> Steuer Elements.

3. Legen <xref:System.Windows.Forms.Button> Sie die **ColumnSpan** -Eigenschaft des Steuer Elements auf **2** fest. Beachten Sie, dass das <xref:System.Windows.Forms.Button> -Steuerelement die erste und die zweite Spalte umfasst.

4. Legen <xref:System.Windows.Forms.Button> Sie die **RowSpan** -Eigenschaft des Steuer Elements auf **2** fest. Beachten Sie, dass das <xref:System.Windows.Forms.Button> -Steuerelement die erste und die zweite Zeile umfasst.

5. Legen <xref:System.Windows.Forms.Button> Sie die **ColumnSpan** -Eigenschaft des Steuer Elements auf **1** fest. Beachten Sie, dass das <xref:System.Windows.Forms.Button> -Steuerelement in die erste Spalte wechselt und die erste und zweite Zeile umfasst.

## <a name="see-also"></a>Siehe auch

- [TableLayoutPanel-Steuerelement](tablelayoutpanel-control-windows-forms.md)
