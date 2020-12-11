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
# <a name="how-to-iterate-through-all-nodes-of-a-windows-forms-treeview-control"></a><span data-ttu-id="59079-102">Vorgehensweise: Durchlaufen aller Knoten eines TreeView-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="59079-102">How to: Iterate Through All Nodes of a Windows Forms TreeView Control</span></span>

<span data-ttu-id="59079-103">Es ist manchmal hilfreich, jeden Knoten in einem Windows Forms-Steuerelement zu untersuchen <xref:System.Windows.Forms.TreeView> , um eine Berechnung der Knotenwerte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="59079-103">It is sometimes useful to examine every node in a Windows Forms <xref:System.Windows.Forms.TreeView> control in order to perform some calculation on the node values.</span></span> <span data-ttu-id="59079-104">Dieser Vorgang kann über eine rekursive Prozedur (rekursive Methode in C# und C++) ausgeführt werden, die jeden Knoten in jeder Auflistung der Struktur durchläuft.</span><span class="sxs-lookup"><span data-stu-id="59079-104">This operation can be done using a recursive procedure (recursive method in C# and C++) that iterates through each node in each collection of the tree.</span></span>  
  
 <span data-ttu-id="59079-105">Jedes <xref:System.Windows.Forms.TreeNode> Objekt in einer Strukturansicht verfügt über Eigenschaften, mit denen Sie in der Strukturansicht navigieren können: <xref:System.Windows.Forms.TreeNode.FirstNode%2A> , <xref:System.Windows.Forms.TreeNode.LastNode%2A> , <xref:System.Windows.Forms.TreeNode.NextNode%2A> , <xref:System.Windows.Forms.TreeNode.PrevNode%2A> und <xref:System.Windows.Forms.TreeNode.Parent%2A> .</span><span class="sxs-lookup"><span data-stu-id="59079-105">Each <xref:System.Windows.Forms.TreeNode> object in a tree view has properties that you can use to navigate the tree view: <xref:System.Windows.Forms.TreeNode.FirstNode%2A>, <xref:System.Windows.Forms.TreeNode.LastNode%2A>, <xref:System.Windows.Forms.TreeNode.NextNode%2A>, <xref:System.Windows.Forms.TreeNode.PrevNode%2A>, and <xref:System.Windows.Forms.TreeNode.Parent%2A>.</span></span> <span data-ttu-id="59079-106">Der Wert der- <xref:System.Windows.Forms.TreeNode.Parent%2A> Eigenschaft ist der übergeordnete Knoten des aktuellen Knotens.</span><span class="sxs-lookup"><span data-stu-id="59079-106">The value of the <xref:System.Windows.Forms.TreeNode.Parent%2A> property is the parent node of the current node.</span></span> <span data-ttu-id="59079-107">Die untergeordneten Knoten des aktuellen Knotens (sofern vorhanden) werden in der- <xref:System.Windows.Forms.TreeNode.Nodes%2A> Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="59079-107">The child nodes of the current node, if there are any, are listed in its <xref:System.Windows.Forms.TreeNode.Nodes%2A> property.</span></span> <span data-ttu-id="59079-108">Das- <xref:System.Windows.Forms.TreeView> Steuerelement verfügt über die- <xref:System.Windows.Forms.TreeView.TopNode%2A> Eigenschaft, die den Stamm Knoten der gesamten Strukturansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="59079-108">The <xref:System.Windows.Forms.TreeView> control itself has the <xref:System.Windows.Forms.TreeView.TopNode%2A> property, which is the root node of the entire tree view.</span></span>  
  
### <a name="to-iterate-through-all-nodes-of-the-treeview-control"></a><span data-ttu-id="59079-109">So durchlaufen Sie alle Knoten des TreeView-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="59079-109">To iterate through all nodes of the TreeView control</span></span>  
  
1. <span data-ttu-id="59079-110">Erstellen Sie eine rekursive Prozedur (rekursive Methode in C# und C++), die jeden einzelnen Knoten testet.</span><span class="sxs-lookup"><span data-stu-id="59079-110">Create a recursive procedure (recursive method in C# and C++) that tests each node.</span></span>  
  
2. <span data-ttu-id="59079-111">Rufen Sie die Prozedur auf.</span><span class="sxs-lookup"><span data-stu-id="59079-111">Call the procedure.</span></span>  
  
     <span data-ttu-id="59079-112">Im folgenden Beispiel wird gezeigt, wie die <xref:System.Windows.Forms.TreeNode> -Eigenschaft jedes-Objekts gedruckt wird <xref:System.Windows.Forms.TreeNode.Text%2A> :</span><span class="sxs-lookup"><span data-stu-id="59079-112">The following example shows how to print each <xref:System.Windows.Forms.TreeNode> object's <xref:System.Windows.Forms.TreeNode.Text%2A> property:</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="59079-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59079-113">See also</span></span>

- [<span data-ttu-id="59079-114">TreeView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="59079-114">TreeView Control</span></span>](treeview-control-windows-forms.md)
- [<span data-ttu-id="59079-115">Rekursive Prozeduren</span><span class="sxs-lookup"><span data-stu-id="59079-115">Recursive Procedures</span></span>](/dotnet/visual-basic/programming-guide/language-features/procedures/recursive-procedures)
