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
# <a name="how-to-change-the-appearance-of-the-windows-forms-linklabel-control"></a>Vorgehensweise: Ändern der Darstellung des LinkLabel-Steuerelements in Windows Forms
Sie können den vom Steuerelement angezeigten Text so ändern, dass er <xref:System.Windows.Forms.LinkLabel> zu einer Vielzahl von Zwecken passt. Es ist z. b. üblich, dem Benutzer anzuzeigen, dass auf Text geklickt werden kann, indem der Text auf eine bestimmte Farbe mit einer Unterstreichung festgelegt wird. Nachdem der Benutzer auf den Text geklickt hat, ändert sich die Farbe in eine andere Farbe. Um dieses Verhalten zu steuern, können Sie fünf verschiedene Eigenschaften festlegen: <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A> die <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> Eigenschaften,, <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> , <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> und <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> .  
  
### <a name="to-change-the-appearance-of-a-linklabel-control"></a>So ändern Sie die Darstellung eines LinkLabel-Steuer Elements  
  
1. Legen <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> Sie die-Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> auf die gewünschten Farben fest.  
  
     Dies kann entweder Programm gesteuert oder zur Entwurfszeit im **Eigenschaften** Fenster erfolgen.  
  
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
  
2. Legen Sie die- <xref:System.Windows.Forms.LinkLabel.Text%2A> Eigenschaft auf eine entsprechende Beschriftung fest.  
  
     Dies kann entweder Programm gesteuert oder zur Entwurfszeit im **Eigenschaften** Fenster erfolgen.  
  
    ```vb  
    LinkLabel1.Text = "Click here to see more."  
    ```  
  
    ```csharp  
    linkLabel1.Text = "Click here to see more.";  
    ```  
  
    ```cpp  
    linkLabel1->Text = "Click here to see more.";  
    ```  
  
3. Legen Sie die- <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> Eigenschaft fest, um zu bestimmen, welcher Teil der Beschriftung als Link angegeben wird.  
  
     Der- <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> Wert wird mit <xref:System.Windows.Forms.LinkArea> zwei Zahlen dargestellt, der Anfangs Zeichenposition und der Anzahl der Zeichen. Dies kann entweder Programm gesteuert oder zur Entwurfszeit im **Eigenschaften** Fenster erfolgen.  
  
    ```vb  
    LinkLabel1.LinkArea = new LinkArea(6,4)  
    ```  
  
    ```csharp  
    linkLabel1.LinkArea = new LinkArea(6,4);  
    ```  
  
    ```cpp  
    linkLabel1->LinkArea = LinkArea(6,4);  
    ```  
  
4. Legen Sie die- <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A> Eigenschaft auf <xref:System.Windows.Forms.LinkBehavior.AlwaysUnderline> , <xref:System.Windows.Forms.LinkBehavior.HoverUnderline> oder fest <xref:System.Windows.Forms.LinkBehavior.NeverUnderline> .  
  
     Wenn Sie auf festgelegt ist <xref:System.Windows.Forms.LinkBehavior.HoverUnderline> , wird der von festgelegte Teil der Beschriftung <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> nur unterstrichen, wenn der Zeiger darauf liegt.  
  
5. <xref:System.Windows.Forms.LinkLabel.LinkClicked>Legen Sie im-Ereignishandler die- <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> Eigenschaft auf fest `true` .  
  
     Wenn ein Link geöffnet wurde, ist es üblich, seine Darstellung in gewisser Weise zu ändern, üblicherweise nach Farbe. Der Text wird in die von der-Eigenschaft angegebene Farbe geändert <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> .  
  
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
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.LinkLabel.LinkArea%2A>
- <xref:System.Windows.Forms.LinkLabel.LinkColor%2A>
- <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A>
- <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A>
- [Übersicht über das LinkLabel-Steuerelement](linklabel-control-overview-windows-forms.md)
- [Vorgehensweise: Verknüpfen eines Objekts oder einer Webseite mit dem LinkLabel-Steuerelement in Windows Forms](link-to-an-object-or-web-page-with-wf-linklabel-control.md)
- [LinkLabel-Steuerelement](linklabel-control-windows-forms.md)
