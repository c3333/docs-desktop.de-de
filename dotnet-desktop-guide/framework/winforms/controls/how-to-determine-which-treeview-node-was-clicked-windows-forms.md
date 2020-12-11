---
title: 'Vorgehensweise: Ermitteln des per Mausklick ausgewählten TreeView-Knotens'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- TreeNode
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- tree nodes in TreeView control [Windows Forms], determining node clicked
- TreeView control [Windows Forms], determining node clicked
ms.assetid: 06a4a191-d918-42af-9f49-956c93eff261
ms.openlocfilehash: d960eaae2aa479e0be74e9a5e4fdbfec8ff411c1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976311"
---
# <a name="how-to-determine-which-treeview-node-was-clicked-windows-forms"></a><span data-ttu-id="3587c-102">Gewusst wie: Ermitteln des per Mausklick ausgewählten TreeView-Knotens (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="3587c-102">How to: Determine Which TreeView Node Was Clicked (Windows Forms)</span></span>
<span data-ttu-id="3587c-103">Beim Arbeiten mit dem Windows Forms- <xref:System.Windows.Forms.TreeView> Steuerelement besteht eine gängige Aufgabe darin, zu ermitteln, auf welchen Knoten geklickt wurde, und entsprechend zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="3587c-103">When working with the Windows Forms <xref:System.Windows.Forms.TreeView> control, a common task is to determine which node was clicked, and respond appropriately.</span></span>  
  
### <a name="to-determine-which-treeview-node-was-clicked"></a><span data-ttu-id="3587c-104">So bestimmen Sie, auf welchen TreeView-Knoten geklickt wurde</span><span class="sxs-lookup"><span data-stu-id="3587c-104">To determine which TreeView node was clicked</span></span>  
  
1. <span data-ttu-id="3587c-105">Verwenden Sie das- <xref:System.EventArgs> Objekt, um einen Verweis auf das angeklickte Knoten Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3587c-105">Use the <xref:System.EventArgs> object to return a reference to the clicked node object.</span></span>  
  
2. <span data-ttu-id="3587c-106">Bestimmen Sie, auf welchen Knoten geklickt wurde, indem Sie die-Klasse überprüfen <xref:System.Windows.Forms.TreeViewEventArgs> , die auf das ereignisbezogene Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="3587c-106">Determine which node was clicked by checking the <xref:System.Windows.Forms.TreeViewEventArgs> class, which contains data related to the event.</span></span>  
  
    ```vb  
    Private Sub TreeView1_AfterSelect(ByVal sender As System.Object, _  
    ByVal e As System.Windows.Forms.TreeViewEventArgs) Handles TreeView1.AfterSelect  
       ' Determine by checking the Node property of the TreeViewEventArgs.  
       MessageBox.Show(e.Node.Text)  
    End Sub  
    ```  
  
    ```csharp  
    protected void treeView1_AfterSelect (object sender,
    System.Windows.Forms.TreeViewEventArgs e)  
    {  
       // Determine by checking the Text property.  
       MessageBox.Show(e.Node.Text);  
    }  
    ```  
  
    ```cpp  
    private:  
       void treeView1_AfterSelect(System::Object ^  sender,  
          System::Windows::Forms::TreeViewEventArgs ^  e)  
       {  
          // Determine by checking the Text property.  
          MessageBox::Show(e->Node->Text);  
       }  
    ```  
  
    > [!NOTE]
    > <span data-ttu-id="3587c-107">Als Alternative können Sie den <xref:System.Windows.Forms.MouseEventArgs> des <xref:System.Windows.Forms.Control.MouseDown> <xref:System.Windows.Forms.Control.MouseUp> -Ereignisses oder das-Ereignis verwenden, um die <xref:System.Drawing.Point.X%2A> -und-Koordinaten Werte des-Werts zu erhalten, <xref:System.Drawing.Point.Y%2A> in dem <xref:System.Drawing.Point> der Klick aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3587c-107">As an alternative, you can use the <xref:System.Windows.Forms.MouseEventArgs> of the <xref:System.Windows.Forms.Control.MouseDown> or <xref:System.Windows.Forms.Control.MouseUp> event to get the <xref:System.Drawing.Point.X%2A> and <xref:System.Drawing.Point.Y%2A> coordinate values of the <xref:System.Drawing.Point> where the click occurred.</span></span> <span data-ttu-id="3587c-108">Verwenden Sie dann die <xref:System.Windows.Forms.TreeView> -Methode des Steuer Elements <xref:System.Windows.Forms.TreeView.GetNodeAt%2A> , um zu ermitteln, auf welchen Knoten geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="3587c-108">Then, use the <xref:System.Windows.Forms.TreeView> control's <xref:System.Windows.Forms.TreeView.GetNodeAt%2A> method to determine which node was clicked.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3587c-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3587c-109">See also</span></span>

- [<span data-ttu-id="3587c-110">TreeView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3587c-110">TreeView Control</span></span>](treeview-control-windows-forms.md)
