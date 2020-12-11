---
title: 'Gewusst wie: Hinzufügen von benutzerdefinierten Informationen zu einem TreeView-oder ListView-Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- ListItem
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- examples [Windows Forms], ListView control
- ListView control [Windows Forms], adding custom information
- TreeView control [Windows Forms], adding custom information
ms.assetid: 68be11de-1d5b-430e-901f-cfbe48d14b19
ms.openlocfilehash: 284bd666d236b765821139a76decd8fedc29b760
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975156"
---
# <a name="how-to-add-custom-information-to-a-treeview-or-listview-control-windows-forms"></a>Vorgehensweise: Hinzufügen von benutzerdefinierten Daten zu einem TreeView- oder ListView-Steuerelement (Windows Forms)

Sie können einen abgeleiteten Knoten in einem Windows Forms- <xref:System.Windows.Forms.TreeView> Steuerelement oder in einem abgeleiteten Element in einem-Steuerelement erstellen <xref:System.Windows.Forms.ListView> . Durch Ableitung können Sie jegliche Felder, die Sie benötigen, sowie die benutzerdefinierten Methoden und Konstruktoren für deren Behandlung hinzufügen. Eine Verwendung dieser Funktion ist das Anfügen eines Customer-Objekts an jeden Strukturknoten oder jedes Listenelement. Die hier aufgeführten Beispiele gelten für ein <xref:System.Windows.Forms.TreeView> Steuerelement, aber der gleiche Ansatz kann für ein Steuerelement verwendet werden <xref:System.Windows.Forms.ListView> .  
  
### <a name="to-derive-a-tree-node"></a>So leiten Sie einen Strukturknoten ab  
  
- Erstellen Sie eine neue Knoten Klasse, die von der-Klasse abgeleitet wird <xref:System.Windows.Forms.TreeNode> , die über ein benutzerdefiniertes Feld zum Aufzeichnen eines Dateipfads verfügt.  
  
    ```vb  
    Class myTreeNode  
       Inherits TreeNode  
  
       Public FilePath As String  
  
       Sub New(ByVal fp As String)  
          MyBase.New()  
          FilePath = fp  
          Me.Text = fp.Substring(fp.LastIndexOf("\"))  
       End Sub  
    End Class  
    ```  
  
    ```csharp  
    class myTreeNode : TreeNode  
    {  
       public string FilePath;  
  
       public myTreeNode(string fp)  
       {  
          FilePath = fp;  
          this.Text = fp.Substring(fp.LastIndexOf("\\"));  
       }  
    }  
    ```  
  
    ```cpp  
    ref class myTreeNode : public TreeNode  
    {  
    public:  
       System::String ^ FilePath;  
  
       myTreeNode(System::String ^ fp)  
       {  
          FilePath = fp;  
          this->Text = fp->Substring(fp->LastIndexOf("\\"));  
       }  
    };  
    ```  
  
### <a name="to-use-a-derived-tree-node"></a>So verwenden Sie einen abgeleiteten Strukturknoten  
  
1. Sie können den neuen abgeleiteten Strukturknoten als Parameter für Funktionsaufrufe verwenden.  
  
     Im folgenden Beispiel ist der Pfad für den Speicherort der Textdatei der Ordner „Eigene Dateien“. Dies geschieht, da Sie davon ausgehen können, dass die meisten Computer, auf denen das Betriebssystem Windows ausgeführt wird, über dieses Verzeichnis verfügen. Dadurch können auch Benutzer mit minimalen Systemzugriffsebenen die Anwendung sicher ausführen.  
  
    ```vb  
    ' You should replace the bold text file
    ' in the sample below with a text file of your own choosing.  
    TreeView1.Nodes.Add(New myTreeNode (System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.Personal) _  
       & "\ TextFile.txt ") )  
    ```  
  
    ```csharp  
    // You should replace the bold text file
    // in the sample below with a text file of your own choosing.  
    // Note the escape character used (@) when specifying the path.  
    treeView1.Nodes.Add(new myTreeNode(System.Environment.GetFolderPath
       (System.Environment.SpecialFolder.Personal)
       + @"\TextFile.txt") );  
    ```  
  
    ```cpp  
    // You should replace the bold text file
    // in the sample below with a text file of your own choosing.  
    treeView1->Nodes->Add(new myTreeNode(String::Concat(  
       System::Environment::GetFolderPath  
       (System::Environment::SpecialFolder::Personal),  
       "\\TextFile.txt")));  
    ```  
  
2. Wenn Sie den Struktur Knoten und ihn als <xref:System.Windows.Forms.TreeNode> Klasse eingegeben haben, müssen Sie in die abgeleitete Klasse umwandeln. Die Umwandlung ist eine explizite Konvertierung von einem Objekt in ein anderes. Weitere Informationen zum Umwandeln finden Sie unter [implizite und explizite Konvertierungen](/dotnet/visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions) (Visual Basic), Umwandlung [und Typkonvertierungen](/dotnet/csharp/programming-guide/types/casting-and-type-conversions) (Visual c#) oder Umwandlungs [Operator: ()](/cpp/cpp/cast-operator-parens) (Visual C++).  
  
    ```vb  
    Public Sub TreeView1_AfterSelect(ByVal sender As Object, ByVal e As System.Windows.Forms.TreeViewEventArgs) Handles TreeView1.AfterSelect  
       Dim mynode As myTreeNode  
       mynode = CType(e.node, myTreeNode)  
       MessageBox.Show("Node selected is " & mynode.filepath)  
    End Sub  
    ```  
  
    ```csharp  
    protected void treeView1_AfterSelect (object sender,  
    System.Windows.Forms.TreeViewEventArgs e)  
    {  
       myTreeNode myNode = (myTreeNode)e.Node;  
       MessageBox.Show("Node selected is " + myNode.FilePath);  
    }  
    ```  
  
    ```cpp  
    private:  
       System::Void treeView1_AfterSelect(System::Object ^  sender,  
          System::Windows::Forms::TreeViewEventArgs ^  e)  
       {  
          myTreeNode ^ myNode = safe_cast<myTreeNode^>(e->Node);  
          MessageBox::Show(String::Concat("Node selected is ",
             myNode->FilePath));  
       }  
    ```  
  
## <a name="see-also"></a>Siehe auch

- [TreeView-Steuerelement](treeview-control-windows-forms.md)
- [ListView-Steuerelement](listview-control-windows-forms.md)
