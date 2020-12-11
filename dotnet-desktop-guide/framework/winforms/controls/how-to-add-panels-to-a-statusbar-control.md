---
title: 'Vorgehensweise: Hinzufügen von Bereichen zu einem StatusBar-Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- panels [Windows Forms], status bars
- status bars [Windows Forms], adding panels
- StatusBar control [Windows Forms], adding panels
ms.assetid: 835e3902-288c-4c38-9d69-0696d8695009
ms.openlocfilehash: ba5b89123c4198ed1aecc988a39de018bc1a1fbb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976247"
---
# <a name="how-to-add-panels-to-a-statusbar-control"></a>Vorgehensweise: Hinzufügen von Bereichen zu einem StatusBar-Steuerelement

> [!IMPORTANT]
> Das-Steuerelement und das-Steuerelement <xref:System.Windows.Forms.StatusStrip> <xref:System.Windows.Forms.ToolStripStatusLabel> ersetzen und fügen Funktionen zu den <xref:System.Windows.Forms.StatusBar> -und-Steuer <xref:System.Windows.Forms.StatusBarPanel> Elementen hinzu. die Steuerelemente <xref:System.Windows.Forms.StatusBar> und werden jedoch sowohl für die abwärts <xref:System.Windows.Forms.StatusBarPanel> Kompatibilität als auch für die zukünftige Verwendung beibehalten.  
  
 Der programmierbare Bereich in einem [StatusBar-Steuer](statusbar-control-windows-forms.md) Element besteht aus Instanzen der- <xref:System.Windows.Forms.StatusBarPanel> Klasse. Diese werden durch Ergänzungen zur-Klasse hinzugefügt <xref:System.Windows.Forms.StatusBar.StatusBarPanelCollection> .  
  
### <a name="to-add-panels-to-a-status-bar"></a>So fügen Sie einer Statusleiste Panels hinzu  
  
1. Erstellen Sie in einer-Prozedur Status leisten Panels, indem Sie Sie der hinzufügen <xref:System.Windows.Forms.StatusBar.StatusBarPanelCollection> . Geben Sie die Eigenschafts Einstellungen für einzelne Panels mithilfe des Indexes an, der durch die-Eigenschaft geleitet wird <xref:System.Windows.Forms.StatusBar.Panels%2A> .  
  
     Im folgenden Codebeispiel ist der Pfad, der für den Speicherort des Symbols festgelegt wurde, der Ordner " **eigene** Dateien". Dieser Speicherort wird verwendet, da Sie davon ausgehen können, dass die meisten Computer unter dem Windows-Betriebssystem diesen Ordner enthalten. Wenn Sie diesen Speicherort auswählen, können Benutzer mit minimalen System Zugriffsebenen die Anwendung sicher ausführen. Das folgende Beispiel erfordert ein Formular mit einem <xref:System.Windows.Forms.StatusBar> bereits hinzugefügten-Steuerelement.  
  
    > [!NOTE]
    > Bei <xref:System.Windows.Forms.StatusBar.StatusBarPanelCollection> handelt es sich um eine Null basierte Auflistung, daher sollte der Code entsprechend fortgesetzt werden.  
  
    ```vb  
    Public Sub CreateStatusBarPanels()  
    ' Create panels and set text property.  
       StatusBar1.Panels.Add("One")  
       StatusBar1.Panels.Add("Two")  
       StatusBar1.Panels.Add("Three")  
    ' Set properties of StatusBar panels.  
    ' Set AutoSize property of panels.  
       StatusBar1.Panels(0).AutoSize = StatusBarPanelAutoSize.Spring  
       StatusBar1.Panels(1).AutoSize = StatusBarPanelAutoSize.Contents  
       StatusBar1.Panels(2).AutoSize = StatusBarPanelAutoSize.Contents  
    ' Set BorderStyle property of panels.  
       StatusBar1.Panels(0).BorderStyle = StatusBarPanelBorderStyle.Raised  
       StatusBar1.Panels(1).BorderStyle = StatusBarPanelBorderStyle.Sunken  
       StatusBar1.Panels(2).BorderStyle = StatusBarPanelBorderStyle.Raised  
    ' Set Icon property of third panel. You should replace the bolded  
    ' icon in the sample below with an icon of your own choosing.  
       StatusBar1.Panels(2).Icon = New _
       System.Drawing.Icon(System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.Personal) _  
       & "\Icon.ico")  
       StatusBar1.ShowPanels = True  
    End Sub  
    ```  
  
    ```csharp  
    public void CreateStatusBarPanels()  
    {  
       // Create panels and set text property.  
       statusBar1.Panels.Add("One");  
       statusBar1.Panels.Add("Two");  
       statusBar1.Panels.Add("Three");  
       // Set properties of StatusBar panels.  
       // Set AutoSize property of panels.  
       statusBar1.Panels[0].AutoSize = StatusBarPanelAutoSize.Spring;  
       statusBar1.Panels[1].AutoSize = StatusBarPanelAutoSize.Contents;  
       statusBar1.Panels[2].AutoSize = StatusBarPanelAutoSize.Contents;  
       // Set BorderStyle property of panels.  
       statusBar1.Panels[0].BorderStyle =  
          StatusBarPanelBorderStyle.Raised;  
       statusBar1.Panels[1].BorderStyle = StatusBarPanelBorderStyle.Sunken;  
       statusBar1.Panels[2].BorderStyle = StatusBarPanelBorderStyle.Raised;  
       // Set Icon property of third panel. You should replace the bolded  
       // icon in the sample below with an icon of your own choosing.  
       // Note the escape character used (@) when specifying the path.  
       statusBar1.Panels[2].Icon =
          new System.Drawing.Icon (System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.Personal) _  
       + @"\Icon.ico");  
       statusBar1.ShowPanels = true;  
    }  
    ```  
  
    ```cpp  
    public:  
       void CreateStatusBarPanels()  
       {  
          // Create panels and set text property.  
          statusBar1->Panels->Add("One");  
          statusBar1->Panels->Add("Two");  
          statusBar1->Panels->Add("Three");  
          // Set properties of StatusBar panels.  
          // Set AutoSize property of panels.  
          statusBar1->Panels[0]->AutoSize =  
             StatusBarPanelAutoSize::Spring;  
          statusBar1->Panels[1]->AutoSize =  
             StatusBarPanelAutoSize::Contents;  
          statusBar1->Panels[2]->AutoSize =  
             StatusBarPanelAutoSize::Contents;  
          // Set BorderStyle property of panels.  
          statusBar1->Panels[0]->BorderStyle =  
             StatusBarPanelBorderStyle::Raised;  
          statusBar1->Panels[1]->BorderStyle =  
             StatusBarPanelBorderStyle::Sunken;  
          statusBar1->Panels[2]->BorderStyle =  
             StatusBarPanelBorderStyle::Raised;  
          // Set Icon property of third panel.  
          // You should replace the bolded image
          // in the sample below with an icon of your own choosing.  
          statusBar1->Panels[2]->Icon =  
             gcnew System::Drawing::Icon(String::Concat(  
             System::Environment::GetFolderPath(  
             System::Environment::SpecialFolder::Personal),  
             "\\Icon.ico"));  
          statusBar1->ShowPanels = true;  
       }  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [Dialogfeld "Auflistungs-Editor"](/previous-versions/visualstudio/visual-studio-2010/xc4yyekt(v=vs.100))
- [Vorgehensweise: Festlegen der Größe eines Statusleistenbereichs](how-to-set-the-size-of-status-bar-panels.md)
- [Exemplarische Vorgehensweise: Aktualisieren von Statusleisteninformationen zur Laufzeit](walkthrough-updating-status-bar-information-at-run-time.md)
- [Vorgehensweise: Bestimmen, auf welchen Bereich im StatusBar-Steuerelement in Windows Forms geklickt wurde](determine-which-panel-wf-statusbar-control-was-clicked.md)
- [Übersicht über das StatusBar-Steuerelement](statusbar-control-overview-windows-forms.md)
