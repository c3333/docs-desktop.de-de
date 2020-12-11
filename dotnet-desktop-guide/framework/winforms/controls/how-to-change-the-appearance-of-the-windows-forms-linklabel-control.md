---
title: Ändern der Darstellung des LinkLabel-Steuer Elements
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- LinkLabel properties
- LinkLabel control [Windows Forms], changing appearance of links
- links [Windows Forms], changing appearance
- examples [Windows Forms], LinkLabel control
- LinkLabel control [Windows Forms], examples
ms.assetid: fdc5854f-5162-4457-8cbe-1042feb2d132
ms.openlocfilehash: df66991289373a05fc7c27b7768a96643e3bbae0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975702"
---
# <a name="how-to-change-the-appearance-of-the-windows-forms-linklabel-control"></a><span data-ttu-id="d0277-102">Vorgehensweise: Ändern der Darstellung des LinkLabel-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d0277-102">How to: Change the Appearance of the Windows Forms LinkLabel Control</span></span>
<span data-ttu-id="d0277-103">Sie können den vom Steuerelement angezeigten Text so ändern, dass er <xref:System.Windows.Forms.LinkLabel> zu einer Vielzahl von Zwecken passt.</span><span class="sxs-lookup"><span data-stu-id="d0277-103">You can change the text displayed by the <xref:System.Windows.Forms.LinkLabel> control to suit a variety of purposes.</span></span> <span data-ttu-id="d0277-104">Es ist z. b. üblich, dem Benutzer anzuzeigen, dass auf Text geklickt werden kann, indem der Text auf eine bestimmte Farbe mit einer Unterstreichung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d0277-104">For example, it is common practice to indicate to the user that text can be clicked by setting the text to appear in a specific color with an underline.</span></span> <span data-ttu-id="d0277-105">Nachdem der Benutzer auf den Text geklickt hat, ändert sich die Farbe in eine andere Farbe.</span><span class="sxs-lookup"><span data-stu-id="d0277-105">After the user clicks the text, the color changes to a different color.</span></span> <span data-ttu-id="d0277-106">Um dieses Verhalten zu steuern, können Sie fünf verschiedene Eigenschaften festlegen: <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A> die <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> Eigenschaften,, <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> , <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> und <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> .</span><span class="sxs-lookup"><span data-stu-id="d0277-106">To control this behavior, you can set five different properties: the <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A>, <xref:System.Windows.Forms.LinkLabel.LinkArea%2A>, <xref:System.Windows.Forms.LinkLabel.LinkColor%2A>, <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A>, and <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> properties.</span></span>  
  
### <a name="to-change-the-appearance-of-a-linklabel-control"></a><span data-ttu-id="d0277-107">So ändern Sie die Darstellung eines LinkLabel-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="d0277-107">To change the appearance of a LinkLabel control</span></span>  
  
1. <span data-ttu-id="d0277-108">Legen <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> Sie die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> auf die gewünschten Farben fest.</span><span class="sxs-lookup"><span data-stu-id="d0277-108">Set the <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> and <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> properties to the colors you want.</span></span>  
  
     <span data-ttu-id="d0277-109">Dies kann entweder Programm gesteuert oder zur Entwurfszeit im **Eigenschaften** Fenster erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d0277-109">This can be done either programmatically or at design time in the **Properties** window.</span></span>  
  
    ```vb  
    ' You can set the color using decimal values for red, green, and blue  
    LinkLabel1.LinkColor = Color.FromArgb(0, 0, 255)  
    ' Or you can set the color using defined constants  
    LinkLabel1.VisitedLinkColor = Color.Purple  
    ```  
  
    ```csharp  
    // You can set the color using decimal values for red, green, and blue  
    linkLabel1.LinkColor = Color.FromArgb(0, 0, 255);  
    // Or you can set the color using defined constants  
    linkLabel1.VisitedLinkColor = Color.Purple;  
    ```  
  
    ```cpp  
    // You can set the color using decimal values for red, green, and blue  
    linkLabel1->LinkColor = Color::FromArgb(0, 0, 255);  
    // Or you can set the color using defined constants  
    linkLabel1->VisitedLinkColor = Color::Purple;  
    ```  
  
2. <span data-ttu-id="d0277-110">Legen Sie die- <xref:System.Windows.Forms.LinkLabel.Text%2A> Eigenschaft auf eine entsprechende Beschriftung fest.</span><span class="sxs-lookup"><span data-stu-id="d0277-110">Set the <xref:System.Windows.Forms.LinkLabel.Text%2A> property to an appropriate caption.</span></span>  
  
     <span data-ttu-id="d0277-111">Dies kann entweder Programm gesteuert oder zur Entwurfszeit im **Eigenschaften** Fenster erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d0277-111">This can be done either programmatically or at design time in the **Properties** window.</span></span>  
  
    ```vb  
    LinkLabel1.Text = "Click here to see more."  
    ```  
  
    ```csharp  
    linkLabel1.Text = "Click here to see more.";  
    ```  
  
    ```cpp  
    linkLabel1->Text = "Click here to see more.";  
    ```  
  
3. <span data-ttu-id="d0277-112">Legen Sie die- <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> Eigenschaft fest, um zu bestimmen, welcher Teil der Beschriftung als Link angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d0277-112">Set the <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> property to determine which part of the caption will be indicated as a link.</span></span>  
  
     <span data-ttu-id="d0277-113">Der- <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> Wert wird mit <xref:System.Windows.Forms.LinkArea> zwei Zahlen dargestellt, der Anfangs Zeichenposition und der Anzahl der Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d0277-113">The <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> value is represented with a <xref:System.Windows.Forms.LinkArea> containing two numbers, the starting character position and the number of characters.</span></span> <span data-ttu-id="d0277-114">Dies kann entweder Programm gesteuert oder zur Entwurfszeit im **Eigenschaften** Fenster erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d0277-114">This can be done either programmatically or at design time in the **Properties** window.</span></span>  
  
    ```vb  
    LinkLabel1.LinkArea = new LinkArea(6,4)  
    ```  
  
    ```csharp  
    linkLabel1.LinkArea = new LinkArea(6,4);  
    ```  
  
    ```cpp  
    linkLabel1->LinkArea = LinkArea(6,4);  
    ```  
  
4. <span data-ttu-id="d0277-115">Legen Sie die- <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A> Eigenschaft auf <xref:System.Windows.Forms.LinkBehavior.AlwaysUnderline> , <xref:System.Windows.Forms.LinkBehavior.HoverUnderline> oder fest <xref:System.Windows.Forms.LinkBehavior.NeverUnderline> .</span><span class="sxs-lookup"><span data-stu-id="d0277-115">Set the <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A> property to <xref:System.Windows.Forms.LinkBehavior.AlwaysUnderline>, <xref:System.Windows.Forms.LinkBehavior.HoverUnderline>, or <xref:System.Windows.Forms.LinkBehavior.NeverUnderline>.</span></span>  
  
     <span data-ttu-id="d0277-116">Wenn Sie auf festgelegt ist <xref:System.Windows.Forms.LinkBehavior.HoverUnderline> , wird der von festgelegte Teil der Beschriftung <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> nur unterstrichen, wenn der Zeiger darauf liegt.</span><span class="sxs-lookup"><span data-stu-id="d0277-116">If it is set to <xref:System.Windows.Forms.LinkBehavior.HoverUnderline>, the part of the caption determined by <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> will only be underlined when the pointer rests on it.</span></span>  
  
5. <span data-ttu-id="d0277-117"><xref:System.Windows.Forms.LinkLabel.LinkClicked>Legen Sie im-Ereignishandler die- <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> Eigenschaft auf fest `true` .</span><span class="sxs-lookup"><span data-stu-id="d0277-117">In the <xref:System.Windows.Forms.LinkLabel.LinkClicked> event handler, set the <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> property to `true`.</span></span>  
  
     <span data-ttu-id="d0277-118">Wenn ein Link geöffnet wurde, ist es üblich, seine Darstellung in gewisser Weise zu ändern, üblicherweise nach Farbe.</span><span class="sxs-lookup"><span data-stu-id="d0277-118">When a link has been visited, it is common practice to change its appearance in some way, usually by color.</span></span> <span data-ttu-id="d0277-119">Der Text wird in die von der-Eigenschaft angegebene Farbe geändert <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> .</span><span class="sxs-lookup"><span data-stu-id="d0277-119">The text will change to the color specified by the <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> property.</span></span>  
  
    ```vb  
    Protected Sub LinkLabel1_LinkClicked (ByVal sender As Object, _  
       ByVal e As EventArgs) Handles LinkLabel1.LinkClicked  
       ' Change the color of the link text  
       ' by setting LinkVisited to True.  
       LinkLabel1.LinkVisited = True  
       ' Then do whatever other action is appropriate  
    End Sub  
    ```  
  
    ```csharp  
    protected void LinkLabel1_LinkClicked(object sender, System.EventArgs e)  
    {  
       // Change the color of the link text by setting LinkVisited
       // to True.  
       linkLabel1.LinkVisited = true;  
       // Then do whatever other action is appropriate  
    }  
    ```  
  
    ```cpp  
    private:  
       System::Void linkLabel1_LinkClicked(System::Object ^  sender,  
          System::Windows::Forms::LinkLabelLinkClickedEventArgs ^  e)  
       {  
          // Change the color of the link text by setting LinkVisited
          // to True.  
          linkLabel1->LinkVisited = true;  
          // Then do whatever other action is appropriate  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="d0277-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0277-120">See also</span></span>

- <xref:System.Windows.Forms.LinkLabel.LinkArea%2A>
- <xref:System.Windows.Forms.LinkLabel.LinkColor%2A>
- <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A>
- <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A>
- [<span data-ttu-id="d0277-121">Übersicht über das LinkLabel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d0277-121">LinkLabel Control Overview</span></span>](linklabel-control-overview-windows-forms.md)
- [<span data-ttu-id="d0277-122">Vorgehensweise: Verknüpfen eines Objekts oder einer Webseite mit dem LinkLabel-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d0277-122">How to: Link to an Object or Web Page with the Windows Forms LinkLabel Control</span></span>](link-to-an-object-or-web-page-with-wf-linklabel-control.md)
- [<span data-ttu-id="d0277-123">LinkLabel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d0277-123">LinkLabel Control</span></span>](linklabel-control-windows-forms.md)
