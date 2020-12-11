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
# <a name="how-to-determine-which-treeview-node-was-clicked-windows-forms"></a>Gewusst wie: Ermitteln des per Mausklick ausgewählten TreeView-Knotens (Windows Forms)
Beim Arbeiten mit dem Windows Forms- <xref:System.Windows.Forms.TreeView> Steuerelement besteht eine gängige Aufgabe darin, zu ermitteln, auf welchen Knoten geklickt wurde, und entsprechend zu reagieren.  
  
### <a name="to-determine-which-treeview-node-was-clicked"></a>So bestimmen Sie, auf welchen TreeView-Knoten geklickt wurde  
  
1. Verwenden Sie das- <xref:System.EventArgs> Objekt, um einen Verweis auf das angeklickte Knoten Objekt zurückzugeben.  
  
2. Bestimmen Sie, auf welchen Knoten geklickt wurde, indem Sie die-Klasse überprüfen <xref:System.Windows.Forms.TreeViewEventArgs> , die auf das ereignisbezogene Daten enthält.  
  
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
    > Als Alternative können Sie den <xref:System.Windows.Forms.MouseEventArgs> des <xref:System.Windows.Forms.Control.MouseDown> <xref:System.Windows.Forms.Control.MouseUp> -Ereignisses oder das-Ereignis verwenden, um die <xref:System.Drawing.Point.X%2A> -und-Koordinaten Werte des-Werts zu erhalten, <xref:System.Drawing.Point.Y%2A> in dem <xref:System.Drawing.Point> der Klick aufgetreten ist. Verwenden Sie dann die <xref:System.Windows.Forms.TreeView> -Methode des Steuer Elements <xref:System.Windows.Forms.TreeView.GetNodeAt%2A> , um zu ermitteln, auf welchen Knoten geklickt wurde.  
  
## <a name="see-also"></a>Siehe auch

- [TreeView-Steuerelement](treeview-control-windows-forms.md)
