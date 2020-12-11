---
title: Ermitteln, auf welchen Bereich im StatusBar-Steuerelement geklickt wurde
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- status bars [Windows Forms], determining panel clicked
- panels [Windows Forms], determining clicked
- StatusBar control [Windows Forms], coding panel click events
- StatusBar control [Windows Forms], determining panel clicked
- PanelClick event [Windows Forms], determining panel clicked
- Panel control [Windows Forms], determining click
ms.assetid: d14c6092-04b2-4a07-8ddf-0dd11277ff5f
ms.openlocfilehash: eb3b10d515ba5b62236594e063ca7f060b34b73e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972130"
---
# <a name="how-to-determine-which-panel-in-the-windows-forms-statusbar-control-was-clicked"></a><span data-ttu-id="216a6-102">Vorgehensweise: Bestimmen, auf welchen Bereich im StatusBar-Steuerelement in Windows Forms geklickt wurde</span><span class="sxs-lookup"><span data-stu-id="216a6-102">How to: Determine Which Panel in the Windows Forms StatusBar Control Was Clicked</span></span>
> [!IMPORTANT]
> <span data-ttu-id="216a6-103">Das-Steuerelement und das-Steuerelement <xref:System.Windows.Forms.StatusStrip> <xref:System.Windows.Forms.ToolStripStatusLabel> ersetzen und fügen Funktionen zu den <xref:System.Windows.Forms.StatusBar> -und-Steuer <xref:System.Windows.Forms.StatusBarPanel> Elementen hinzu. die Steuerelemente <xref:System.Windows.Forms.StatusBar> und werden jedoch sowohl für die abwärts <xref:System.Windows.Forms.StatusBarPanel> Kompatibilität als auch für die zukünftige Verwendung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="216a6-103">The <xref:System.Windows.Forms.StatusStrip> and <xref:System.Windows.Forms.ToolStripStatusLabel> controls replace and add functionality to the <xref:System.Windows.Forms.StatusBar> and <xref:System.Windows.Forms.StatusBarPanel> controls; however, the <xref:System.Windows.Forms.StatusBar> and <xref:System.Windows.Forms.StatusBarPanel> controls are retained for both backward compatibility and future use, if you choose.</span></span>  
  
 <span data-ttu-id="216a6-104">Um das [StatusBar-Steuer](statusbar-control-windows-forms.md) Element für die Reaktion auf Benutzer Klicks zu programmieren, verwenden Sie eine Case-Anweisung innerhalb des <xref:System.Windows.Forms.StatusBar.PanelClick> Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="216a6-104">To program the [StatusBar Control](statusbar-control-windows-forms.md) control to respond to user clicks, use a case statement within the <xref:System.Windows.Forms.StatusBar.PanelClick> event.</span></span> <span data-ttu-id="216a6-105">Das Ereignis enthält ein Argument (das Panel-Argument), das einen Verweis auf die angeklickte enthält <xref:System.Windows.Forms.StatusBarPanel> .</span><span class="sxs-lookup"><span data-stu-id="216a6-105">The event contains an argument (the panel argument), which contains a reference to the clicked <xref:System.Windows.Forms.StatusBarPanel>.</span></span> <span data-ttu-id="216a6-106">Mithilfe dieses Verweises können Sie den Index des angeklickten Panels ermitteln und entsprechend programmieren.</span><span class="sxs-lookup"><span data-stu-id="216a6-106">Using this reference, you can determine the index of the clicked panel, and program accordingly.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="216a6-107">Stellen Sie sicher, dass die <xref:System.Windows.Forms.StatusBar> -Eigenschaft des Steuer Elements <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> auf gesetzt ist `true` .</span><span class="sxs-lookup"><span data-stu-id="216a6-107">Ensure that the <xref:System.Windows.Forms.StatusBar> control's <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> property is set to `true`.</span></span>  
  
### <a name="to-determine-which-panel-was-clicked"></a><span data-ttu-id="216a6-108">So bestimmen Sie den Bereich, auf den geklickt wurde</span><span class="sxs-lookup"><span data-stu-id="216a6-108">To determine which panel was clicked</span></span>  
  
1. <span data-ttu-id="216a6-109"><xref:System.Windows.Forms.StatusBar.PanelClick>Verwenden Sie im-Ereignishandler eine- `Select Case` Anweisung (in Visual Basic) oder eine- `switch case` Anweisung (Visual c# oder Visual C++), um zu bestimmen, auf welche Fläche geklickt wurde, indem Sie den Index des angeklickten Panels in den Ereignis Argumenten untersuchen.</span><span class="sxs-lookup"><span data-stu-id="216a6-109">In the <xref:System.Windows.Forms.StatusBar.PanelClick> event handler, use a `Select Case` (in Visual Basic) or `switch case` (Visual C# or Visual C++) statement to determine which panel was clicked by examining the index of the clicked panel in the event arguments.</span></span>  
  
     <span data-ttu-id="216a6-110">Für das folgende Codebeispiel ist das vorhanden sein eines-Steuer Elements, des-Steuer Elements, des-Objekts und des-Objekts erforderlich <xref:System.Windows.Forms.StatusBar> `StatusBar1` <xref:System.Windows.Forms.StatusBarPanel> `StatusBarPanel1` `StatusBarPanel2` .</span><span class="sxs-lookup"><span data-stu-id="216a6-110">The following code example requires the presence, on the form, of a <xref:System.Windows.Forms.StatusBar> control, `StatusBar1`, and two <xref:System.Windows.Forms.StatusBarPanel> objects, `StatusBarPanel1` and `StatusBarPanel2`.</span></span>  
  
    ```vb  
    Private Sub StatusBar1_PanelClick(ByVal sender As System.Object, ByVal e As System.Windows.Forms.StatusBarPanelClickEventArgs) Handles StatusBar1.PanelClick  
       Select Case StatusBar1.Panels.IndexOf(e.StatusBarPanel)  
         Case 0  
           MessageBox.Show("You have clicked Panel One.")  
         Case 1  
           MessageBox.Show("You have clicked Panel Two.")  
       End Select  
    End Sub  
    ```  
  
    ```csharp  
    private void statusBar1_PanelClick(object sender,
    System.Windows.Forms.StatusBarPanelClickEventArgs e)  
    {  
       switch (statusBar1.Panels.IndexOf(e.StatusBarPanel))  
       {  
          case 0 :  
             MessageBox.Show("You have clicked Panel One.");  
             break;  
          case 1 :  
             MessageBox.Show("You have clicked Panel Two.");  
             break;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void statusBar1_PanelClick(System::Object ^  sender,  
          System::Windows::Forms::StatusBarPanelClickEventArgs ^  e)  
       {  
          switch (statusBar1->Panels->IndexOf(e->StatusBarPanel))  
          {  
             case 0 :  
                MessageBox::Show("You have clicked Panel One.");  
                break;  
             case 1 :  
                MessageBox::Show("You have clicked Panel Two.");  
                break;  
          }  
       }  
    ```  
  
     <span data-ttu-id="216a6-111">(Visual c#, Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="216a6-111">(Visual C#, Visual C++) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.statusBar1.PanelClick += new
       System.Windows.Forms.StatusBarPanelClickEventHandler
       (this.statusBar1_PanelClick);  
    ```  
  
    ```cpp  
    this->statusBar1->PanelClick += gcnew  
       System::Windows::Forms::StatusBarPanelClickEventHandler  
       (this, &Form1::statusBar1_PanelClick);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="216a6-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="216a6-112">See also</span></span>

- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [<span data-ttu-id="216a6-113">Vorgehensweise: Festlegen der Größe eines Statusleistenbereichs</span><span class="sxs-lookup"><span data-stu-id="216a6-113">How to: Set the Size of Status-Bar Panels</span></span>](how-to-set-the-size-of-status-bar-panels.md)
- [<span data-ttu-id="216a6-114">Exemplarische Vorgehensweise: Aktualisieren von Statusleisteninformationen zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="216a6-114">Walkthrough: Updating Status Bar Information at Run Time</span></span>](walkthrough-updating-status-bar-information-at-run-time.md)
- [<span data-ttu-id="216a6-115">Übersicht über das StatusBar-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="216a6-115">StatusBar Control Overview</span></span>](statusbar-control-overview-windows-forms.md)
