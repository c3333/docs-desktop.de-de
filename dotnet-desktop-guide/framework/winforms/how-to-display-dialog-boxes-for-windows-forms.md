---
title: 'Vorgehensweise: Anzeigen von Dialog Feldern'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, displaying
- Windows Forms dialog boxes [Windows Forms], displaying
- Windows Forms, calling one form from another
- dialog boxes [Windows Forms], displaying for Windows Forms
ms.assetid: aaac1b38-c651-495a-8d3d-5a9bfb32fee3
ms.openlocfilehash: 3625080c7c322e297a9de92e4f95a40c0caf3e72
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972297"
---
# <a name="how-to-display-dialog-boxes-for-windows-forms"></a><span data-ttu-id="4346c-102">Vorgehensweise: Anzeigen von Dialogfeldern für Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4346c-102">How to: Display Dialog Boxes for Windows Forms</span></span>
<span data-ttu-id="4346c-103">Sie können ein Dialogfeld auf die gleiche Weise wie andere Formulare in einer Anwendung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4346c-103">You display a dialog box in the same way you display any other form in an application.</span></span> <span data-ttu-id="4346c-104">Das Start Formular wird automatisch geladen, wenn die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4346c-104">The startup form loads automatically when the application is run.</span></span> <span data-ttu-id="4346c-105">Damit ein zweites Formular oder Dialogfeld in der Anwendung angezeigt wird, schreiben Sie Code, um ihn zu laden und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4346c-105">To make a second form or dialog box appear in the application, write code to load and display it.</span></span> <span data-ttu-id="4346c-106">Wenn Sie das Formular oder Dialogfeld ausblenden möchten, schreiben Sie den Code, um ihn zu entladen oder auszublenden.</span><span class="sxs-lookup"><span data-stu-id="4346c-106">Similarly, to make the form or dialog box disappear, write code to unload or hide it.</span></span>  
  
### <a name="to-display-a-dialog-box"></a><span data-ttu-id="4346c-107">So zeigen Sie ein Dialogfeld an</span><span class="sxs-lookup"><span data-stu-id="4346c-107">To display a dialog box</span></span>  
  
1. <span data-ttu-id="4346c-108">Navigieren Sie zu dem Ereignishandler, mit dem Sie das Dialogfeld öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="4346c-108">Navigate to the event handler with which you want to open the dialog box.</span></span> <span data-ttu-id="4346c-109">Dies kann vorkommen, wenn ein Menübefehl ausgewählt wird, wenn auf eine Schaltfläche geklickt wird oder wenn ein beliebiges anderes Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="4346c-109">This can happen when a menu command is selected, when a button is clicked, or when any other event occurs.</span></span>  
  
2. <span data-ttu-id="4346c-110">Fügen Sie im-Ereignishandler Code hinzu, um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4346c-110">In the event handler, add code to open the dialog box.</span></span> <span data-ttu-id="4346c-111">In diesem Beispiel wird ein Button-Click-Ereignis verwendet, um das Dialogfeld anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="4346c-111">In this example, a button-click event is used to show the dialog box:</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
       Dim dlg1 as new Form()  
       dlg1.ShowDialog()  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)
    {  
       Form dlg1 = new Form();  
       dlg1.ShowDialog();  
    }  
    ```  
  
    ```cpp  
    private:
      void button1_Click(System::Object ^ sender,  
        System::EventArgs ^ e)  
      {  
        Form ^ dlg1 = gcnew Form();  
        dlg1->ShowDialog();  
      }  
    ```
