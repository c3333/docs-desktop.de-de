---
title: 'Gewusst wie: Ausrichten eines Steuerelements an den Rändern eines Formulars zur Entwurfszeit'
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], docking using designer
- Dock property [Windows Forms], aligning controls (using designer)
ms.assetid: 51f08998-5e3b-4330-be58-a4edd0eb60f4
ms.openlocfilehash: b08e01eb9adb984a32a8fc435cf1f3b93b159a14
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976368"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms-at-design-time"></a>Gewusst wie: Ausrichten eines Steuerelements an den Rändern eines Formulars zur Entwurfszeit

Sie können das Steuerelement am Rand Ihrer Formulare ausrichten, indem Sie den Wert der- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft festlegen. Diese Eigenschaft legt fest, wo auf dem Formular das Steuerelement sich befindet. Die <xref:System.Windows.Forms.Control.Dock%2A>-Eigenschaft kann auf einen der folgenden Werte festgelegt werden:

|Einstellung|Auswirkung auf das Steuerelement|
|-------------|----------------------------|
|<xref:System.Windows.Forms.DockStyle.Bottom>|Wird im unteren Bereich des Formulars angedockt.|
|<xref:System.Windows.Forms.DockStyle.Fill>|Füllt den gesamten verbleibenden Platz im Formular aus.|
|<xref:System.Windows.Forms.DockStyle.Left>|Wird an der linken Seite des Formulars angedockt.|
|<xref:System.Windows.Forms.DockStyle.None>|Wird nicht an einer beliebigen Stelle andocken und wird an dem Speicherort angezeigt, der durch angegeben ist <xref:System.Windows.Forms.Control.Location%2A> .|
|<xref:System.Windows.Forms.DockStyle.Right>|Wird an der rechten Seite des Formulars angedockt.|
|<xref:System.Windows.Forms.DockStyle.Top>|Wird im oberen Bereich des Formulars angedockt.|

Diese Werte können auch im Code festgelegt werden. Weitere Informationen finden Sie unter Gewusst [wie: Ausrichten eines Steuer Elements an den Kanten von Formularen](how-to-align-a-control-to-the-edges-of-forms.md).

## <a name="set-the-dock-property-for-your-control-at-design-time"></a>Festlegen der Dock-Eigenschaft für das Steuerelement zur Entwurfszeit

1. Wählen Sie in der Windows Forms-Designer in Visual Studio das Steuerelement aus.

2. Klicken Sie im Fenster **Eigenschaften** auf das Dropdown Feld neben der- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft.

     Eine grafische Benutzeroberfläche, die die sechs möglichen Einstellungen darstellt, <xref:System.Windows.Forms.Control.Dock%2A> wird angezeigt.

3. Wählen Sie die entsprechende Einstellung aus.

4. Das Steuerelement wird nun in der durch die-Einstellung angegebenen Weise andocken.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>
- [Vorgehensweise: Ausrichten eines Steuerelements an Formularrändern](how-to-align-a-control-to-the-edges-of-forms.md)
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von Ausrichtungslinien](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
- [Gewusst wie: Verankern von Steuerelementen in Windows Forms](how-to-anchor-controls-on-windows-forms.md)
- [Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem TableLayoutPanel-Steuerelement](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem FlowLayoutPanel-Steuerelement](how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [Entwickeln von Windows Forms-Steuerelementen zur Entwurfszeit](developing-windows-forms-controls-at-design-time.md)
