---
title: Durchlaufen aller Knoten des TreeView-Steuer Elements
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- TreeView control [Windows Forms], iterating through nodes
- tree nodes in TreeView control [Windows Forms], iterating through
ms.assetid: 427f8928-ebcf-4beb-887f-695b905d5134
ms.openlocfilehash: fd3d8c4659f0dad3b9566cc7946f35957a19f6f9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976613"
---
# <a name="how-to-iterate-through-all-nodes-of-a-windows-forms-treeview-control"></a>Vorgehensweise: Durchlaufen aller Knoten eines TreeView-Steuerelements in Windows Forms

Es ist manchmal hilfreich, jeden Knoten in einem Windows Forms-Steuerelement zu untersuchen <xref:System.Windows.Forms.TreeView> , um eine Berechnung der Knotenwerte auszuführen. Dieser Vorgang kann über eine rekursive Prozedur (rekursive Methode in C# und C++) ausgeführt werden, die jeden Knoten in jeder Auflistung der Struktur durchläuft.  
  
 Jedes <xref:System.Windows.Forms.TreeNode> Objekt in einer Strukturansicht verfügt über Eigenschaften, mit denen Sie in der Strukturansicht navigieren können: <xref:System.Windows.Forms.TreeNode.FirstNode%2A> , <xref:System.Windows.Forms.TreeNode.LastNode%2A> , <xref:System.Windows.Forms.TreeNode.NextNode%2A> , <xref:System.Windows.Forms.TreeNode.PrevNode%2A> und <xref:System.Windows.Forms.TreeNode.Parent%2A> . Der Wert der- <xref:System.Windows.Forms.TreeNode.Parent%2A> Eigenschaft ist der übergeordnete Knoten des aktuellen Knotens. Die untergeordneten Knoten des aktuellen Knotens (sofern vorhanden) werden in der- <xref:System.Windows.Forms.TreeNode.Nodes%2A> Eigenschaft aufgelistet. Das- <xref:System.Windows.Forms.TreeView> Steuerelement verfügt über die- <xref:System.Windows.Forms.TreeView.TopNode%2A> Eigenschaft, die den Stamm Knoten der gesamten Strukturansicht enthält.  
  
### <a name="to-iterate-through-all-nodes-of-the-treeview-control"></a>So durchlaufen Sie alle Knoten des TreeView-Steuerelements  
  
1. Erstellen Sie eine rekursive Prozedur (rekursive Methode in C# und C++), die jeden einzelnen Knoten testet.  
  
2. Rufen Sie die Prozedur auf.  
  
     Im folgenden Beispiel wird gezeigt, wie die <xref:System.Windows.Forms.TreeNode> -Eigenschaft jedes-Objekts gedruckt wird <xref:System.Windows.Forms.TreeNode.Text%2A> :  
  
    ```vb  
    Private Sub PrintRecursive(ByVal n As TreeNode)  
       System.Diagnostics.Debug.WriteLine(n.Text)  
       MessageBox.Show(n.Text)  
       Dim aNode As TreeNode  
       For Each aNode In n.Nodes  
          PrintRecursive(aNode)  
       Next  
    End Sub  
  
    ' Call the procedure using the top nodes of the treeview.  
    Private Sub CallRecursive(ByVal aTreeView As TreeView)  
       Dim n As TreeNode  
       For Each n In aTreeView.Nodes  
          PrintRecursive(n)  
       Next  
    End Sub  
    ```  
  
    ```csharp  
    private void PrintRecursive(TreeNode treeNode)  
    {  
       // Print the node.  
       System.Diagnostics.Debug.WriteLine(treeNode.Text);  
       MessageBox.Show(treeNode.Text);  
       // Print each node recursively.  
       foreach (TreeNode tn in treeNode.Nodes)  
       {  
          PrintRecursive(tn);  
       }  
    }  
  
    // Call the procedure using the TreeView.  
    private void CallRecursive(TreeView treeView)  
    {  
       // Print each node recursively.  
       TreeNodeCollection nodes = treeView.Nodes;  
       foreach (TreeNode n in nodes)  
       {  
          PrintRecursive(n);  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void PrintRecursive( TreeNode^ treeNode )  
       {  
          // Print the node.  
          System::Diagnostics::Debug::WriteLine( treeNode->Text );  
          MessageBox::Show( treeNode->Text );  
  
          // Print each node recursively.  
          System::Collections::IEnumerator^ myNodes = (safe_cast<System::Collections::IEnumerable^>(treeNode->Nodes))->GetEnumerator();  
          try  
          {  
             while ( myNodes->MoveNext() )  
             {  
                TreeNode^ tn = safe_cast<TreeNode^>(myNodes->Current);  
                PrintRecursive( tn );  
             }  
          }  
          finally  
          {  
             IDisposable^ disposable = dynamic_cast<System::IDisposable^>(myNodes);  
             if ( disposable != nullptr )  
                      disposable->Dispose();  
          }  
       }  
  
       // Call the procedure using the TreeView.  
       void CallRecursive( TreeView^ treeView )  
       {  
          // Print each node recursively.  
          TreeNodeCollection^ nodes = treeView->Nodes;  
          System::Collections::IEnumerator^ myNodes = (safe_cast<System::Collections::IEnumerable^>(nodes))->GetEnumerator();  
          try  
          {  
             while ( myNodes->MoveNext() )  
             {  
                TreeNode^ n = safe_cast<TreeNode^>(myNodes->Current);  
                PrintRecursive( n );  
             }  
          }  
          finally  
          {  
             IDisposable^ disposable = dynamic_cast<System::IDisposable^>(myNodes);  
             if ( disposable != nullptr )  
                      disposable->Dispose();  
          }  
       }  
    ```  
  
## <a name="see-also"></a>Siehe auch

- [TreeView-Steuerelement](treeview-control-windows-forms.md)
- [Rekursive Prozeduren](/dotnet/visual-basic/programming-guide/language-features/procedures/recursive-procedures)
