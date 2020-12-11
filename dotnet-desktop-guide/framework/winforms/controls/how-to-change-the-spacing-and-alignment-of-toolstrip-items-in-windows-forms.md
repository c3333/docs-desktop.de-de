---
title: 'Gewusst wie: Ändern des Abstands und der Ausrichtung von ToolStrip-Elementen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], aligning items
- examples [Windows Forms], toolbars
- toolbars [Windows Forms], aligning items
ms.assetid: cd483466-0f49-43df-addf-e2b5fcd64027
ms.openlocfilehash: 550ac1660a077e8d766a01bfa8d102c07f0fbfeb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976348"
---
# <a name="how-to-change-the-spacing-and-alignment-of-toolstrip-items-in-windows-forms"></a>Vorgehensweise: Ändern der Abstände und der Ausrichtung der ToolStrip-Elemente in Windows Forms
Das- <xref:System.Windows.Forms.ToolStrip> Steuerelement unterstützt vollständige Layoutfunktionen, wie z. b. die Größe, den Abstand von Steuer <xref:System.Windows.Forms.ToolStripItem> Elementen relativ zueinander, die Anordnung der Steuerelemente auf dem <xref:System.Windows.Forms.ToolStrip> und den Abstand von Steuerelementen relativ zum <xref:System.Windows.Forms.ToolStrip> .  
  
 Da der Standardwert der- <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> Eigenschaft ist `true` , werden die Steuerelemente automatisch vergrößert, es sei denn, Sie legen die- <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> Eigenschaft auf fest `false` .  
  
### <a name="to-manually-size-a-toolstripitem"></a>So wird ein ToolStripItem-Element manuell Größe  
  
1. Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> Eigenschaft für das zugeordnete Steuerelement auf fest `false` .  
  
    ```vb  
    ToolStripButton1.AutoSize = False  
    ```  
  
    ```csharp  
    toolStripButton1.AutoSize = false;  
    ```  
  
2. Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.Size%2A> Eigenschaft auf die gewünschte Weise für die zugeordnete fest <xref:System.Windows.Forms.ToolStripItem> .  
  
### <a name="to-set-the-spacing-of-a-toolstripitem"></a>So legen Sie den Abstand eines ToolStripItem fest  
  
1. Fügen Sie die gewünschten Werte in Pixel in die- <xref:System.Windows.Forms.ToolStripItem.Margin%2A> Eigenschaft des zugeordneten Steuer Elements ein.  
  
     Die Werte der- <xref:System.Windows.Forms.ToolStripItem.Margin%2A> Eigenschaft geben den Abstand zwischen dem Element und angrenzenden Elementen in dieser Reihenfolge an: Links, oben, rechts und unten.  
  
    ```vb  
    ToolStripTextBox1.Margin = New System.Windows.Forms.Padding _  
        (3, 0, 3, 0)  
    ```  
  
    ```csharp  
    toolStripTextBox1.Margin = new System.Windows.Forms.Padding
        (3, 0, 3, 0);  
    ```  
  
### <a name="to-align-a-toolstripitem-to-the-right-side-of-the-toolstrip"></a>So richten Sie ein ToolStripItem rechts neben dem ToolStrip aus  
  
1. Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.Alignment%2A> Eigenschaft für das zugeordnete Steuerelement auf fest <xref:System.Windows.Forms.ToolStripItemAlignment.Right> . Standardmäßig <xref:System.Windows.Forms.ToolStripItem.Alignment%2A> ist auf festgelegt <xref:System.Windows.Forms.ToolStripItemAlignment.Left> , wodurch Steuerelemente auf der linken Seite des ausgerichtet werden <xref:System.Windows.Forms.ToolStrip> .  
  
    ```vb  
    ToolStripSplitButton1.Alignment = _  
        System.Windows.Forms.ToolStripItemAlignment.Right  
    ```  
  
    ```csharp  
    toolStripSplitButton1.Alignment =
        System.Windows.Forms.ToolStripItemAlignment.Right;  
    ```  
  
### <a name="to-arrange-toolstrip-items-on-the-toolstrip"></a>So ordnen Sie ToolStrip-Elemente auf dem ToolStrip an  
  
- Legen Sie die- <xref:System.Windows.Forms.ToolStrip.LayoutStyle%2A> Eigenschaft auf den <xref:System.Windows.Forms.ToolStripLayoutStyle> gewünschten Wert fest.  
  
    ```vb  
    ToolStripDropDown1.LayoutStyle = _  
        System.Windows.Forms.ToolStripLayoutStyle.Flow  
    ```  
  
    ```csharp  
    toolStripDropDown1.LayoutStyle =
        System.Windows.Forms.ToolStripLayoutStyle.Flow;  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.Control.Layout>
- <xref:System.Windows.Forms.ToolStrip.LayoutCompleted>
- <xref:System.Windows.Forms.ToolStrip.LayoutSettings%2A>
- <xref:System.Windows.Forms.ToolStripItem.TextImageRelation%2A>
- <xref:System.Windows.Forms.ToolStripItem.Placement%2A>
- <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A>
- [Übersicht über das ToolStrip-Steuerelement](toolstrip-control-overview-windows-forms.md)
- [Architektur des ToolStrip-Steuerelements](toolstrip-control-architecture.md)
- [Zusammenfassung der ToolStrip-Technologie](toolstrip-technology-summary.md)
