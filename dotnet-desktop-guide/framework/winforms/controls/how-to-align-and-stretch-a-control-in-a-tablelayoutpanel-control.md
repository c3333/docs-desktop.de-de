---
title: 'Vorgehensweise: Ausrichten und Strecken eines Steuerelements in einem TableLayoutPanel-Steuerelement'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.AlignStretchCtrl
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms], stretching controls
- controls [Windows Forms], stretching
- controls [Windows Forms], aligning
ms.assetid: 7dc1a157-6fee-4995-8ebc-b65bdc0909a8
ms.openlocfilehash: fd32593bcad9e3f3ef93edee8aa2659d423f9feb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976367"
---
# <a name="how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control"></a>Vorgehensweise: Ausrichten und Strecken eines Steuerelements in einem TableLayoutPanel-Steuerelement

Sie können Steuerelemente in einem <xref:System.Windows.Forms.TableLayoutPanel> mit der-Eigenschaft und der-Eigenschaft ausrichten und erweitern <xref:System.Windows.Forms.Control.Anchor%2A> <xref:System.Windows.Forms.Control.Dock%2A> .

## <a name="align-and-stretch-a-control"></a>Ausrichten und Strecken eines Steuer Elements

1. Ziehen Sie in Visual Studio ein- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement aus der **Toolbox** auf das Formular.

2. Ziehen Sie ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** in die linke obere Zelle des- <xref:System.Windows.Forms.TableLayoutPanel> Steuer Elements. Das- <xref:System.Windows.Forms.Button> Steuerelement wird in der Zelle zentriert.

3. Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Anchor%2A> auf fest `Left,Right` . Das Steuerelement wird so <xref:System.Windows.Forms.Button> gestreckt, dass es der Breite der Zelle entspricht.

4. Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Anchor%2A> auf fest `Top,Bottom` . Das-Steuerelement wird so <xref:System.Windows.Forms.Button> gestreckt, dass es der Höhe der Zelle entspricht.

5. Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Dock%2A> auf fest <xref:System.Windows.Forms.DockStyle.Fill> . Das-Steuerelement wird <xref:System.Windows.Forms.Button> erweitert, um die Zelle auszufüllen.

6. Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Dock%2A> auf fest <xref:System.Windows.Forms.DockStyle.None> . Das <xref:System.Windows.Forms.Button> Steuerelement wird auf seine ursprüngliche Größe zurückgesetzt und wechselt zur linken oberen Ecke der Zelle. Der **Windows Forms-Designer** hat die- <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaft auf festgelegt `Top, Left` .

7. Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Anchor%2A> auf fest `Bottom,Right` . Das- <xref:System.Windows.Forms.Button> Steuerelement wechselt zur unteren rechten Ecke der Zelle.

8. Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Anchor%2A> auf fest <xref:System.Windows.Forms.AnchorStyles.None> . Das- <xref:System.Windows.Forms.Button> Steuerelement wechselt in den Mittelpunkt der Zelle.

## <a name="see-also"></a>Siehe auch

- [TableLayoutPanel-Steuerelement](tablelayoutpanel-control-windows-forms.md)
