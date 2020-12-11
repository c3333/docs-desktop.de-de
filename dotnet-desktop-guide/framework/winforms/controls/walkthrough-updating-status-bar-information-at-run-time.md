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
# <a name="walkthrough-updating-status-bar-information-at-run-time"></a><span data-ttu-id="dc3b3-102">Exemplarische Vorgehensweise: Aktualisieren von Statusleisteninformationen zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="dc3b3-102">Walkthrough: Updating Status Bar Information at Run Time</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc3b3-103">Das-Steuerelement und das-Steuerelement <xref:System.Windows.Forms.StatusStrip> <xref:System.Windows.Forms.ToolStripStatusLabel> ersetzen und fügen Funktionen zu den <xref:System.Windows.Forms.StatusBar> -und-Steuer <xref:System.Windows.Forms.StatusBarPanel> Elementen hinzu. die Steuerelemente <xref:System.Windows.Forms.StatusBar> und werden jedoch sowohl für die abwärts <xref:System.Windows.Forms.StatusBarPanel> Kompatibilität als auch für die zukünftige Verwendung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-103">The <xref:System.Windows.Forms.StatusStrip> and <xref:System.Windows.Forms.ToolStripStatusLabel> controls replace and add functionality to the <xref:System.Windows.Forms.StatusBar> and <xref:System.Windows.Forms.StatusBarPanel> controls; however, the <xref:System.Windows.Forms.StatusBar> and <xref:System.Windows.Forms.StatusBarPanel> controls are retained for both backward compatibility and future use, if you choose.</span></span>  
  
 <span data-ttu-id="dc3b3-104">Ein Programm wird Sie häufig auffordern, die Inhalte von Bereichen der Statusleiste basierend auf Änderungen am Anwendungszustand oder anderen Benutzerinteraktionen dynamisch zur Laufzeit zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-104">Often, a program will call for you to update the contents of status bar panels dynamically at run time, based on changes to application state or other user interaction.</span></span> <span data-ttu-id="dc3b3-105">Dies ist eine gängige Methode, Benutzern mitzuteilen, dass Tasten wie die FESTSTELLTASTE, NUM- oder ROLLEN-TASTE aktiviert sind oder um das Datum oder eine Uhr als praktische Referenz zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-105">This is a common way to signal users that keys such as the CAPS LOCK, NUM LOCK, or SCROLL LOCK are enabled, or to provide the date or a clock as a convenient reference.</span></span>  
  
 <span data-ttu-id="dc3b3-106">Im folgenden Beispiel verwenden Sie eine Instanz der- <xref:System.Windows.Forms.StatusBarPanel> Klasse, um eine Uhr zu hosten.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-106">In the following example, you will use an instance of the <xref:System.Windows.Forms.StatusBarPanel> class to host a clock.</span></span>  
  
### <a name="to-get-the-status-bar-ready-for-updating"></a><span data-ttu-id="dc3b3-107">So bereiten Sie die Statusleiste für die Aktualisierung vor</span><span class="sxs-lookup"><span data-stu-id="dc3b3-107">To get the status bar ready for updating</span></span>  
  
1. <span data-ttu-id="dc3b3-108">Erstellen Sie ein neues Windows-Formular.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-108">Create a new Windows form.</span></span>  
  
2. <span data-ttu-id="dc3b3-109">Fügen Sie Ihrem Formular ein <xref:System.Windows.Forms.StatusBar>-Steuerelement hinzu.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-109">Add a <xref:System.Windows.Forms.StatusBar> control to your form.</span></span> <span data-ttu-id="dc3b3-110">Weitere Informationen finden Sie unter [Vorgehensweise: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="dc3b3-110">For details, see [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>  
  
3. <span data-ttu-id="dc3b3-111">Fügen Sie dem Steuerelement einen Status Leistenbereich hinzu <xref:System.Windows.Forms.StatusBar> .</span><span class="sxs-lookup"><span data-stu-id="dc3b3-111">Add a status bar panel to your <xref:System.Windows.Forms.StatusBar> control.</span></span> <span data-ttu-id="dc3b3-112">Weitere Informationen finden Sie unter [Vorgehensweise: Hinzufügen von Bereichen zu einem StatusBar-Steuerelement](how-to-add-panels-to-a-statusbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="dc3b3-112">For details, see [How to: Add Panels to a StatusBar Control](how-to-add-panels-to-a-statusbar-control.md).</span></span>  
  
4. <span data-ttu-id="dc3b3-113"><xref:System.Windows.Forms.StatusBar>Legen Sie für das Steuerelement, das Sie dem Formular hinzugefügt haben, die- <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> Eigenschaft auf fest `true`</span><span class="sxs-lookup"><span data-stu-id="dc3b3-113">For the <xref:System.Windows.Forms.StatusBar> control you added to your form, set the <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> property to `true`.</span></span>  
  
5. <span data-ttu-id="dc3b3-114">Fügen Sie <xref:System.Windows.Forms.Timer> dem Formular eine Windows Forms Komponente hinzu.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-114">Add a Windows Forms <xref:System.Windows.Forms.Timer> component to the form.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="dc3b3-115">Die Windows Forms <xref:System.Windows.Forms.Timer?displayProperty=nameWithType> Komponente ist für eine Windows Forms Umgebung konzipiert.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-115">The Windows Forms <xref:System.Windows.Forms.Timer?displayProperty=nameWithType> component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="dc3b3-116">Wenn Sie einen für eine Serverumgebung geeigneten Timer benötigen, lesen Sie die Informationen unter [Introduction to Server-Based Timers (Einführung in serverbasierte Timer)](/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="dc3b3-116">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).</span></span>  
  
6. <span data-ttu-id="dc3b3-117">Legen Sie die <xref:System.Windows.Forms.Timer.Enabled%2A> -Eigenschaft auf `true`fest.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-117">Set the <xref:System.Windows.Forms.Timer.Enabled%2A> property to `true`.</span></span>  
  
7. <span data-ttu-id="dc3b3-118">Legen Sie die- <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft von <xref:System.Windows.Forms.Timer> auf 30000 fest.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-118">Set the <xref:System.Windows.Forms.Timer.Interval%2A> property of the <xref:System.Windows.Forms.Timer> to 30000.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="dc3b3-119">Die- <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft der- <xref:System.Windows.Forms.Timer> Komponente ist auf 30 Sekunden (30.000 Millisekunden) festgelegt, um sicherzustellen, dass eine genaue Zeit in der angezeigten Zeit angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-119">The <xref:System.Windows.Forms.Timer.Interval%2A> property of the <xref:System.Windows.Forms.Timer> component is set to 30 seconds (30,000 milliseconds) to ensure that an accurate time is reflected in the time displayed.</span></span>  
  
### <a name="to-implement-the-timer-to-update-the-status-bar"></a><span data-ttu-id="dc3b3-120">So Implementieren Sie den Zeitgeber zum Aktualisieren der Statusleiste</span><span class="sxs-lookup"><span data-stu-id="dc3b3-120">To implement the timer to update the status bar</span></span>  
  
1. <span data-ttu-id="dc3b3-121">Fügen Sie den folgenden Code in den-Ereignishandler der- <xref:System.Windows.Forms.Timer> Komponente ein, um den Bereich des-Steuer Elements zu aktualisieren <xref:System.Windows.Forms.StatusBar> .</span><span class="sxs-lookup"><span data-stu-id="dc3b3-121">Insert the following code into the event handler of the <xref:System.Windows.Forms.Timer> component to update the panel of the <xref:System.Windows.Forms.StatusBar> control.</span></span>  
  
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
  
     <span data-ttu-id="dc3b3-122">An diesem Punkt sind Sie bereit, die Anwendung auszuführen und zu sehen, wie die Uhr im Statusleistenbereich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-122">At this point, you are ready to run the application and observe the clock running in the status bar panel.</span></span>  
  
### <a name="to-test-the-application"></a><span data-ttu-id="dc3b3-123">So testen Sie die Anwendung</span><span class="sxs-lookup"><span data-stu-id="dc3b3-123">To test the application</span></span>  
  
1. <span data-ttu-id="dc3b3-124">Debuggen Sie die Anwendung und drücken Sie F5, um die Anwendung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-124">Debug the application and press F5 to run it.</span></span> <span data-ttu-id="dc3b3-125">Weitere Informationen zum Debugging finden Sie unter [Debuggen in Visual Studio](/visualstudio/debugger/debugger-feature-tour).</span><span class="sxs-lookup"><span data-stu-id="dc3b3-125">For details about debugging, see [Debugging in Visual Studio](/visualstudio/debugger/debugger-feature-tour).</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="dc3b3-126">Es dauert ungefähr 30 Sekunden, bis die Uhr in der Statusleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-126">It will take approximately 30 seconds for the clock to appear in the status bar.</span></span> <span data-ttu-id="dc3b3-127">Dies ist die akkurateste mögliche Zeit.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-127">This is to get the most accurate time possible.</span></span> <span data-ttu-id="dc3b3-128">Umgekehrt können Sie den Wert der Eigenschaft verringern, die <xref:System.Windows.Forms.Timer.Interval%2A> Sie in Schritt 7 des vorherigen Verfahrens festgelegt haben, um die Uhr früher anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dc3b3-128">Conversely, to make the clock appear sooner, you can reduce the value of the <xref:System.Windows.Forms.Timer.Interval%2A> property you set in step 7 in the previous procedure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc3b3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc3b3-129">See also</span></span>

- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [<span data-ttu-id="dc3b3-130">Vorgehensweise: Hinzufügen von Bereichen zu einem StatusBar-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="dc3b3-130">How to: Add Panels to a StatusBar Control</span></span>](how-to-add-panels-to-a-statusbar-control.md)
- [<span data-ttu-id="dc3b3-131">Vorgehensweise: Bestimmen, auf welchen Bereich im StatusBar-Steuerelement in Windows Forms geklickt wurde</span><span class="sxs-lookup"><span data-stu-id="dc3b3-131">How to: Determine Which Panel in the Windows Forms StatusBar Control Was Clicked</span></span>](determine-which-panel-wf-statusbar-control-was-clicked.md)
- [<span data-ttu-id="dc3b3-132">Übersicht über das StatusBar-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="dc3b3-132">StatusBar Control Overview</span></span>](statusbar-control-overview-windows-forms.md)
