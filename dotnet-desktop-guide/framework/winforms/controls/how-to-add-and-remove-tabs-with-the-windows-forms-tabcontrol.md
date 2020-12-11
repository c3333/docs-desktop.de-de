---
title: Hinzufügen und Entfernen von Registerkarten mit TabControl
description: Erfahren Sie, wie Sie Registerkarten mit dem Windows Forms TabControl-Steuerelement hinzufügen und entfernen, das zwei TabPage-Steuerelemente enthält. Greifen Sie über die TabPages-Eigenschaft auf diese Registerkarten zu.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tabs [Windows Forms], removing from pages
- TabPage control
- TabControl control [Windows Forms], adding and removing tabs
- tabs [Windows Forms], adding to pages
- tab pages
ms.assetid: 66d4dfca-41e8-44e3-9c80-fb7ac4cb1619
ms.openlocfilehash: 7e67d0bbc13bd7d9c8835dc6fb9b9c5c9333b8bf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972092"
---
# <a name="how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol"></a>Vorgehensweise: Hinzufügen und Entfernen von Registerkarten mit dem TabControl-Steuerelement in Windows Forms
Standardmäßig enthält ein- <xref:System.Windows.Forms.TabControl> Steuerelement zwei-Steuer <xref:System.Windows.Forms.TabPage> Elemente. Sie können über die-Eigenschaft auf diese Registerkarten zugreifen <xref:System.Windows.Forms.TabControl.TabPages%2A> .  
  
### <a name="to-add-a-tab-programmatically"></a>So fügen Sie eine Registerkarte Programm gesteuert hinzu  
  
- Verwenden Sie die- <xref:System.Windows.Forms.TabControl.TabPageCollection.Add%2A> Methode der- <xref:System.Windows.Forms.TabControl.TabPages%2A> Eigenschaft.  
  
    ```vb  
    Dim myTabPage As New TabPage()  
    myTabPage.Text = "TabPage" & (TabControl1.TabPages.Count + 1)  
    TabControl1.TabPages.Add(myTabPage)  
    ```  
  
    ```csharp  
    string title = "TabPage " + (tabControl1.TabCount + 1).ToString();  
    TabPage myTabPage = new TabPage(title);  
    tabControl1.TabPages.Add(myTabPage);  
    ```  
  
    ```cpp  
    String^ title = String::Concat("TabPage ",  
       (tabControl1->TabCount + 1).ToString());  
    TabPage^ myTabPage = gcnew TabPage(title);  
    tabControl1->TabPages->Add(myTabPage);  
    ```  
  
### <a name="to-remove-a-tab-programmatically"></a>So entfernen Sie eine Registerkarte Programm gesteuert  
  
- Um die ausgewählten Registerkarten zu entfernen, verwenden Sie die- <xref:System.Windows.Forms.TabControl.TabPageCollection.Remove%2A> Methode der- <xref:System.Windows.Forms.TabControl.TabPages%2A> Eigenschaft.  
  
     Oder  
  
- Um alle Registerkarten zu entfernen, verwenden Sie die- <xref:System.Windows.Forms.TabControl.TabPageCollection.Clear%2A> Methode der- <xref:System.Windows.Forms.TabControl.TabPages%2A> Eigenschaft.  
  
    ```vb  
    ' Removes the selected tab:  
    TabControl1.TabPages.Remove(TabControl1.SelectedTab)  
    ' Removes all the tabs:  
    TabControl1.TabPages.Clear()  
    ```  
  
    ```csharp  
    // Removes the selected tab:  
    tabControl1.TabPages.Remove(tabControl1.SelectedTab);  
    // Removes all the tabs:  
    tabControl1.TabPages.Clear();  
    ```  
  
    ```cpp  
    // Removes the selected tab:  
    tabControl1->TabPages->Remove(tabControl1->SelectedTab);  
    // Removes all the tabs:  
    tabControl1->TabPages->Clear();  
    ```  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über das TabControl-Steuerelement](tabcontrol-control-overview-windows-forms.md)
- [Vorgehensweise: Hinzufügen eines Steuerelements zu einer Registerkarte](how-to-add-a-control-to-a-tab-page.md)
- [Vorgehensweise: Deaktivieren von Registerkartenseiten](how-to-disable-tab-pages.md)
- [Vorgehensweise: Ändern der Darstellung der TabControl-Komponente in Windows Forms](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
