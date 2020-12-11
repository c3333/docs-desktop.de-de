---
title: 'Vorgehensweise: Erstellen einer MDI-Fensterliste mithilfe von MenuStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- MDI [Windows Forms], creating window lists
- MenuStrip control [Windows Forms], creating window lists
ms.assetid: 04fb414b-811f-4a83-aab6-b4a24646dec5
ms.openlocfilehash: f013c3df2ab5783a22fe2c34402dc53a328cafa2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975686"
---
# <a name="how-to-create-an-mdi-window-list-with-menustrip-windows-forms"></a><span data-ttu-id="6d63c-102">Gewusst wie: Erstellen einer MDI-Fensterliste mithilfe von MenuStrip (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="6d63c-102">How to: Create an MDI Window List with MenuStrip (Windows Forms)</span></span>
<span data-ttu-id="6d63c-103">Verwenden Sie die Multiple Document Interface (MDI), um Anwendungen zu erstellen, die mehrere Dokumente gleichzeitig öffnen und Inhalte aus einem Dokument kopieren und in das andere einfügen können.</span><span class="sxs-lookup"><span data-stu-id="6d63c-103">Use the multiple-document interface (MDI) to create applications that can open several documents at the same time and copy and paste content from one document to the other.</span></span>  
  
 <span data-ttu-id="6d63c-104">In diesem Verfahren wird gezeigt, wie Sie eine Liste aller aktiven untergeordneten Formulare im Fenstermenü des übergeordneten Fensters erstellen.</span><span class="sxs-lookup"><span data-stu-id="6d63c-104">This procedure shows you how to create a list of all the active child forms on the parent's Window menu.</span></span>  
  
### <a name="to-create-an-mdi-window-list-on-a-menustrip"></a><span data-ttu-id="6d63c-105">So erstellen Sie eine MDI-Fensterliste in einem MenuStrip</span><span class="sxs-lookup"><span data-stu-id="6d63c-105">To create an MDI Window list on a MenuStrip</span></span>  
  
1. <span data-ttu-id="6d63c-106">Erstellen Sie ein Formular, und legen Sie dessen <xref:System.Windows.Forms.Form.IsMdiContainer%2A>-Eigenschaft auf `true` fest.</span><span class="sxs-lookup"><span data-stu-id="6d63c-106">Create a form and set its <xref:System.Windows.Forms.Form.IsMdiContainer%2A> property to `true`.</span></span>  
  
2. <span data-ttu-id="6d63c-107">Fügen Sie dem Formular eine <xref:System.Windows.Forms.MenuStrip> hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d63c-107">Add a <xref:System.Windows.Forms.MenuStrip> to the form.</span></span>  
  
3. <span data-ttu-id="6d63c-108">Fügen Sie zwei Menü Elemente der obersten Ebene hinzu, <xref:System.Windows.Forms.MenuStrip> und legen Sie deren <xref:System.Windows.Forms.Control.Text%2A> Eigenschaften auf `&File` und fest `&Window` .</span><span class="sxs-lookup"><span data-stu-id="6d63c-108">Add two top-level menu items to the <xref:System.Windows.Forms.MenuStrip> and set their <xref:System.Windows.Forms.Control.Text%2A> properties to `&File` and `&Window`.</span></span>  
  
4. <span data-ttu-id="6d63c-109">Fügen Sie dem `&File`-Menüelement ein Untermenüelement hinzu, und legen Sie dessen <xref:System.Windows.Forms.ToolStripItem.Text%2A>-Eigenschaft auf `&Open` fest.</span><span class="sxs-lookup"><span data-stu-id="6d63c-109">Add a submenu item to the `&File` menu item and set its <xref:System.Windows.Forms.ToolStripItem.Text%2A> property to `&Open`.</span></span>  
  
5. <span data-ttu-id="6d63c-110">Legen Sie die- <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> Eigenschaft des-Objekts <xref:System.Windows.Forms.MenuStrip> auf fest `&Window` <xref:System.Windows.Forms.ToolStripMenuItem> .</span><span class="sxs-lookup"><span data-stu-id="6d63c-110">Set the <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> property of the <xref:System.Windows.Forms.MenuStrip> to the `&Window`<xref:System.Windows.Forms.ToolStripMenuItem>.</span></span>  
  
6. <span data-ttu-id="6d63c-111">Fügen Sie dem Projekt ein Formular hinzu, und fügen Sie das gewünschte Steuerelement hinzu, z <xref:System.Windows.Forms.MenuStrip> . b. ein anderes.</span><span class="sxs-lookup"><span data-stu-id="6d63c-111">Add a form to the project and add the control you want to it, such as another <xref:System.Windows.Forms.MenuStrip>.</span></span>  
  
7. <span data-ttu-id="6d63c-112">Erstellen Sie einen Ereignishandler für das <xref:System.Windows.Forms.Control.Click>-Ereignis von `&New`<xref:System.Windows.Forms.ToolStripMenuItem>.</span><span class="sxs-lookup"><span data-stu-id="6d63c-112">Create an event handler for the <xref:System.Windows.Forms.Control.Click> event of the `&New`<xref:System.Windows.Forms.ToolStripMenuItem>.</span></span>  
  
8. <span data-ttu-id="6d63c-113">Fügen Sie im-Ereignishandler Code ähnlich dem folgenden ein, um neue Instanzen von als untergeordnete MDI-Elemente von zu erstellen und anzuzeigen `Form2` `Form1` .</span><span class="sxs-lookup"><span data-stu-id="6d63c-113">Within the event handler, insert code similar to the following to create and display new instances of `Form2` as MDI children of `Form1`.</span></span>  
  
    ```vb  
    Private Sub openToolStripMenuItem_Click(ByVal sender As _  
    System.Object, ByVal e As System.EventArgs) Handles _  
    openToolStripMenuItem.Click  
        Dim NewMDIChild As New Form2()  
        'Set the parent form of the child window.  
            NewMDIChild.MdiParent = Me  
        'Display the new form.  
            NewMDIChild.Show()  
    End Sub  
    ```  
  
    ```csharp  
    private void newToolStripMenuItem_Click(object sender, EventArgs e)  
    {  
        Form2 newMDIChild = new Form2();  
        // Set the parent form of the child window.  
            newMDIChild.MdiParent = this;  
        // Display the new form.  
            newMDIChild.Show();  
    }  
    ```  
  
9. <span data-ttu-id="6d63c-114">Platzieren Sie Code wie den folgenden in der `&New` <xref:System.Windows.Forms.ToolStripMenuItem> , um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="6d63c-114">Place code like the following in the `&New`<xref:System.Windows.Forms.ToolStripMenuItem> to register the event handler.</span></span>  
  
    ```vb  
    Private Sub newToolStripMenuItem_Click(sender As Object, e As _  
    EventArgs) Handles newToolStripMenuItem.Click  
    ```  
  
    ```csharp  
    this.newToolStripMenuItem.Click += new System.EventHandler(this.newToolStripMenuItem_Click);  
    ```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="6d63c-115">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="6d63c-115">Compiling the Code</span></span>  
 <span data-ttu-id="6d63c-116">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6d63c-116">This example requires:</span></span>  
  
- <span data-ttu-id="6d63c-117">Zwei <xref:System.Windows.Forms.Form>-Steuerelemente namens `Form1` und `Form2`.</span><span class="sxs-lookup"><span data-stu-id="6d63c-117">Two <xref:System.Windows.Forms.Form> controls named `Form1` and `Form2`.</span></span>  
  
- <span data-ttu-id="6d63c-118">Ein <xref:System.Windows.Forms.MenuStrip>-Steuerelement auf `Form1`, das den Namen `menuStrip1` hat, und ein <xref:System.Windows.Forms.MenuStrip>-Steuerelement auf `Form2`, das den Namen `menuStrip2` hat.</span><span class="sxs-lookup"><span data-stu-id="6d63c-118">A <xref:System.Windows.Forms.MenuStrip> control on `Form1` named `menuStrip1`, and a <xref:System.Windows.Forms.MenuStrip> control on `Form2` named `menuStrip2`.</span></span>  
  
- <span data-ttu-id="6d63c-119">Verweise auf die Assemblys <xref:System?displayProperty=nameWithType> und <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="6d63c-119">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d63c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d63c-120">See also</span></span>

- [<span data-ttu-id="6d63c-121">Vorgehensweise: Erstellen von übergeordneten MDI-Formularen</span><span class="sxs-lookup"><span data-stu-id="6d63c-121">How to: Create MDI Parent Forms</span></span>](../advanced/how-to-create-mdi-parent-forms.md)
- [<span data-ttu-id="6d63c-122">Vorgehensweise: Erstellen von untergeordneten MDI-Formularen</span><span class="sxs-lookup"><span data-stu-id="6d63c-122">How to: Create MDI Child Forms</span></span>](../advanced/how-to-create-mdi-child-forms.md)
- [<span data-ttu-id="6d63c-123">MenuStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6d63c-123">MenuStrip Control</span></span>](menustrip-control-windows-forms.md)
