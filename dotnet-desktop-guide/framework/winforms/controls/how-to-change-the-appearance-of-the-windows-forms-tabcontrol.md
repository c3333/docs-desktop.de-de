---
title: Ändern der Darstellung von TabControl
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- icons [Windows Forms], displaying on tabs
- TabControl control [Windows Forms], changing page appearance
- tabs [Windows Forms], controlling appearance
- buttons [Windows Forms], displaying tabs as
ms.assetid: 7c6cc443-ed62-4d26-b94d-b8913b44f773
ms.openlocfilehash: 056070177e6bbaba0c93c7b94f5adfd7887be6a8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976352"
---
# <a name="how-to-change-the-appearance-of-the-windows-forms-tabcontrol"></a>Vorgehensweise: Ändern der Darstellung der TabControl-Komponente in Windows Forms
Sie können die Darstellung von Registerkarten in Windows Forms ändern, indem Sie die Eigenschaften des <xref:System.Windows.Forms.TabControl> -Objekts und das- <xref:System.Windows.Forms.TabPage> Objekt verwenden, die die einzelnen Registerkarten des Steuer Elements bilden. Durch Festlegen dieser Eigenschaften können Sie Bilder auf Registerkarten anzeigen, Registerkarten vertikal anstatt horizontal anzeigen, mehrere Zeilen von Registerkarten anzeigen und Registerkarten Programm gesteuert aktivieren oder deaktivieren.  
  
### <a name="to-display-an-icon-on-the-label-part-of-a-tab"></a>So zeigen Sie ein Symbol auf dem Bezeichnungs Teil einer Registerkarte an  
  
1. Fügen Sie <xref:System.Windows.Forms.ImageList> dem Formular ein-Steuerelement hinzu.  
  
2. Fügen Sie der Bildliste Bilder hinzu.  
  
     Weitere Informationen zu Bildlisten finden Sie unter [ImageList-Komponente](imagelist-component-windows-forms.md) und Gewusst [wie: Hinzufügen oder Entfernen von Bildern mit der Windows Forms ImageList-Komponente](how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).  
  
3. Legen Sie die- <xref:System.Windows.Forms.TabControl.ImageList%2A> Eigenschaft von <xref:System.Windows.Forms.TabControl> auf das-Steuerelement fest <xref:System.Windows.Forms.ImageList> .  
  
4. Legen Sie die- <xref:System.Windows.Forms.TabPage.ImageIndex%2A> Eigenschaft des-Objekts <xref:System.Windows.Forms.TabPage> auf den Index eines entsprechenden Bilds in der Liste fest.  
  
### <a name="to-create-multiple-rows-of-tabs"></a>So erstellen Sie mehrere Zeilen von Registerkarten  
  
1. Fügen Sie die gewünschte Anzahl von Registerkarten hinzu.  
  
2. Legen Sie die <xref:System.Windows.Forms.TabControl.Multiline%2A>-Eigenschaft von <xref:System.Windows.Forms.TabControl> auf `true` fest.  
  
3. Wenn die Registerkarten nicht bereits in mehreren Zeilen angezeigt werden, legen <xref:System.Windows.Forms.Control.Width%2A> Sie die-Eigenschaft von auf einen engeren Wert fest <xref:System.Windows.Forms.TabControl> als alle Registerkarten.  
  
### <a name="to-arrange-tabs-on-the-side-of-the-control"></a>So ordnen Sie Registerkarten auf der Seite des Steuer Elements an  
  
- Legen Sie die- <xref:System.Windows.Forms.TabControl.Alignment%2A> Eigenschaft von <xref:System.Windows.Forms.TabControl> auf <xref:System.Windows.Forms.TabAlignment.Left> oder fest <xref:System.Windows.Forms.TabAlignment.Right> .  
  
### <a name="to-programmatically-enable-or-disable-all-controls-on-a-tab"></a>So aktivieren oder deaktivieren Sie alle Steuerelemente auf einer Registerkarte Programm gesteuert  
  
1. Legen Sie die- <xref:System.Windows.Forms.TabPage.Enabled%2A> Eigenschaft von <xref:System.Windows.Forms.TabPage> auf `true` oder fest `false` .  
  
    ```vb  
    TabPage1.Enabled = False  
    ```  
  
    ```csharp  
    tabPage1.Enabled = false;  
    ```  
  
    ```cpp  
    tabPage1->Enabled = false;  
    ```  
  
### <a name="to-display-tabs-as-buttons"></a>Anzeigen von Registerkarten als Schaltflächen  
  
- Legen Sie die- <xref:System.Windows.Forms.TabControl.Appearance%2A> Eigenschaft von <xref:System.Windows.Forms.TabControl> auf <xref:System.Windows.Forms.TabAppearance.Buttons> oder fest <xref:System.Windows.Forms.TabAppearance.FlatButtons> .  
  
## <a name="see-also"></a>Siehe auch

- [TabControl-Steuerelement](tabcontrol-control-windows-forms.md)
- [Übersicht über das TabControl-Steuerelement](tabcontrol-control-overview-windows-forms.md)
- [Vorgehensweise: Hinzufügen eines Steuerelements zu einer Registerkarte](how-to-add-a-control-to-a-tab-page.md)
- [Vorgehensweise: Deaktivieren von Registerkartenseiten](how-to-disable-tab-pages.md)
- [Vorgehensweise: Hinzufügen und Entfernen von Registerkarten mit dem TabControl-Steuerelement in Windows Forms](how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
