---
title: 'Exemplarische Vorgehensweise: Aktualisieren von Statusleisteninformationen zur Laufzeit'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- status bars [Windows Forms], updating at run time
- status bars [Windows Forms], refreshing panels
- StatusBar control [Windows Forms], refreshing panels
- panels [Windows Forms], refreshing status bar
ms.assetid: cc2abb06-c082-49f7-a5a3-2fd1bbcb58d1
ms.openlocfilehash: a58f8698af95810e4f716aa2b105bb86be3f55e6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976589"
---
# <a name="walkthrough-updating-status-bar-information-at-run-time"></a>Exemplarische Vorgehensweise: Aktualisieren von Statusleisteninformationen zur Laufzeit

> [!IMPORTANT]
> Das-Steuerelement und das-Steuerelement <xref:System.Windows.Forms.StatusStrip> <xref:System.Windows.Forms.ToolStripStatusLabel> ersetzen und fügen Funktionen zu den <xref:System.Windows.Forms.StatusBar> -und-Steuer <xref:System.Windows.Forms.StatusBarPanel> Elementen hinzu. die Steuerelemente <xref:System.Windows.Forms.StatusBar> und werden jedoch sowohl für die abwärts <xref:System.Windows.Forms.StatusBarPanel> Kompatibilität als auch für die zukünftige Verwendung beibehalten.  
  
 Ein Programm wird Sie häufig auffordern, die Inhalte von Bereichen der Statusleiste basierend auf Änderungen am Anwendungszustand oder anderen Benutzerinteraktionen dynamisch zur Laufzeit zu aktualisieren. Dies ist eine gängige Methode, Benutzern mitzuteilen, dass Tasten wie die FESTSTELLTASTE, NUM- oder ROLLEN-TASTE aktiviert sind oder um das Datum oder eine Uhr als praktische Referenz zur Verfügung zu stellen.  
  
 Im folgenden Beispiel verwenden Sie eine Instanz der- <xref:System.Windows.Forms.StatusBarPanel> Klasse, um eine Uhr zu hosten.  
  
### <a name="to-get-the-status-bar-ready-for-updating"></a>So bereiten Sie die Statusleiste für die Aktualisierung vor  
  
1. Erstellen Sie ein neues Windows-Formular.  
  
2. Fügen Sie Ihrem Formular ein <xref:System.Windows.Forms.StatusBar>-Steuerelement hinzu. Weitere Informationen finden Sie unter [Vorgehensweise: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).  
  
3. Fügen Sie dem Steuerelement einen Status Leistenbereich hinzu <xref:System.Windows.Forms.StatusBar> . Weitere Informationen finden Sie unter [Vorgehensweise: Hinzufügen von Bereichen zu einem StatusBar-Steuerelement](how-to-add-panels-to-a-statusbar-control.md).  
  
4. <xref:System.Windows.Forms.StatusBar>Legen Sie für das Steuerelement, das Sie dem Formular hinzugefügt haben, die- <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> Eigenschaft auf fest `true`  
  
5. Fügen Sie <xref:System.Windows.Forms.Timer> dem Formular eine Windows Forms Komponente hinzu.  
  
    > [!NOTE]
    > Die Windows Forms <xref:System.Windows.Forms.Timer?displayProperty=nameWithType> Komponente ist für eine Windows Forms Umgebung konzipiert. Wenn Sie einen für eine Serverumgebung geeigneten Timer benötigen, lesen Sie die Informationen unter [Introduction to Server-Based Timers (Einführung in serverbasierte Timer)](/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).  
  
6. Legen Sie die <xref:System.Windows.Forms.Timer.Enabled%2A> -Eigenschaft auf `true`fest.  
  
7. Legen Sie die- <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft von <xref:System.Windows.Forms.Timer> auf 30000 fest.  
  
    > [!NOTE]
    > Die- <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft der- <xref:System.Windows.Forms.Timer> Komponente ist auf 30 Sekunden (30.000 Millisekunden) festgelegt, um sicherzustellen, dass eine genaue Zeit in der angezeigten Zeit angezeigt wird.  
  
### <a name="to-implement-the-timer-to-update-the-status-bar"></a>So Implementieren Sie den Zeitgeber zum Aktualisieren der Statusleiste  
  
1. Fügen Sie den folgenden Code in den-Ereignishandler der- <xref:System.Windows.Forms.Timer> Komponente ein, um den Bereich des-Steuer Elements zu aktualisieren <xref:System.Windows.Forms.StatusBar> .  
  
    ```vb  
    Private Sub Timer1_Tick(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Timer1.Tick  
       StatusBar1.Panels(0).Text = Now.ToShortTimeString  
    End Sub  
    ```  
  
    ```csharp  
    private void timer1_Tick(object sender, System.EventArgs e)  
    {  
       statusBar1.Panels[0].Text = DateTime.Now.ToShortTimeString();  
    }  
    ```  
  
    ```cpp  
    private:  
      System::Void timer1_Tick(System::Object ^ sender,  
        System::EventArgs ^ e)  
      {  
        statusBar1->Panels[0]->Text =  
          DateTime::Now.ToShortTimeString();  
      }  
    ```  
  
     An diesem Punkt sind Sie bereit, die Anwendung auszuführen und zu sehen, wie die Uhr im Statusleistenbereich ausgeführt wird.  
  
### <a name="to-test-the-application"></a>So testen Sie die Anwendung  
  
1. Debuggen Sie die Anwendung und drücken Sie F5, um die Anwendung auszuführen. Weitere Informationen zum Debugging finden Sie unter [Debuggen in Visual Studio](/visualstudio/debugger/debugger-feature-tour).  
  
    > [!NOTE]
    > Es dauert ungefähr 30 Sekunden, bis die Uhr in der Statusleiste angezeigt wird. Dies ist die akkurateste mögliche Zeit. Umgekehrt können Sie den Wert der Eigenschaft verringern, die <xref:System.Windows.Forms.Timer.Interval%2A> Sie in Schritt 7 des vorherigen Verfahrens festgelegt haben, um die Uhr früher anzuzeigen.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [Vorgehensweise: Hinzufügen von Bereichen zu einem StatusBar-Steuerelement](how-to-add-panels-to-a-statusbar-control.md)
- [Vorgehensweise: Bestimmen, auf welchen Bereich im StatusBar-Steuerelement in Windows Forms geklickt wurde](determine-which-panel-wf-statusbar-control-was-clicked.md)
- [Übersicht über das StatusBar-Steuerelement](statusbar-control-overview-windows-forms.md)
