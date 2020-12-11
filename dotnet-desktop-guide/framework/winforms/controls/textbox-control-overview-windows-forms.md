---
title: Übersicht über das TextBox-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- TextBox
helpviewer_keywords:
- TextBox control [Windows Forms], about TextBox controls
- text boxes [Windows Forms], adding
ms.assetid: d1a9c7f5-fa53-480a-a75c-158f8649ea2f
ms.openlocfilehash: 06ab460d720d17331881b5ba653263160eaf3cb3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975354"
---
# <a name="textbox-control-overview-windows-forms"></a><span data-ttu-id="c1d8c-102">Übersicht über das TextBox-Steuerelement (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="c1d8c-102">TextBox Control Overview (Windows Forms)</span></span>
<span data-ttu-id="c1d8c-103">Windows Forms Textfelder werden verwendet, um Eingaben vom Benutzer zu erhalten oder Text anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-103">Windows Forms text boxes are used to get input from the user or to display text.</span></span> <span data-ttu-id="c1d8c-104">Das <xref:System.Windows.Forms.TextBox> Steuerelement wird im Allgemeinen für bearbeitbaren Text verwendet, obwohl es auch als schreibgeschützt festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-104">The <xref:System.Windows.Forms.TextBox> control is generally used for editable text, although it can also be made read-only.</span></span> <span data-ttu-id="c1d8c-105">Textfelder können mehrere Zeilen anzeigen, Text in die Größe des Steuer Elements umschließen und grundlegende Formatierung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-105">Text boxes can display multiple lines, wrap text to the size of the control, and add basic formatting.</span></span> <span data-ttu-id="c1d8c-106">Das- <xref:System.Windows.Forms.TextBox> Steuerelement stellt einen einzelnen Formatierungs Stil für Text bereit, der im Steuerelement angezeigt oder eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-106">The <xref:System.Windows.Forms.TextBox> control provides a single format style for text displayed or entered into the control.</span></span> <span data-ttu-id="c1d8c-107">Verwenden Sie das-Steuerelement, um mehrere formatierte Text Typen anzuzeigen <xref:System.Windows.Forms.RichTextBox> .</span><span class="sxs-lookup"><span data-stu-id="c1d8c-107">To display multiple types of formatted text, use the <xref:System.Windows.Forms.RichTextBox> control.</span></span> <span data-ttu-id="c1d8c-108">Weitere Informationen finden Sie unter [Übersicht über das RichTextBox-Steuer](richtextbox-control-overview-windows-forms.md)Element.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-108">For more information, see [RichTextBox Control Overview](richtextbox-control-overview-windows-forms.md).</span></span>  
  
## <a name="working-with-the-textbox-control"></a><span data-ttu-id="c1d8c-109">Arbeiten mit dem TextBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c1d8c-109">Working with the TextBox Control</span></span>  
 <span data-ttu-id="c1d8c-110">Der Text, der vom-Steuerelement angezeigt wird, ist in der- <xref:System.Windows.Forms.TextBox.Text%2A> Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-110">The text displayed by the control is contained in the <xref:System.Windows.Forms.TextBox.Text%2A> property.</span></span> <span data-ttu-id="c1d8c-111">Standardmäßig können Sie bis zu 2048 Zeichen in einem Textfeld eingeben.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-111">By default, you can enter up to 2048 characters in a text box.</span></span> <span data-ttu-id="c1d8c-112">Wenn Sie die- <xref:System.Windows.Forms.TextBox.Multiline%2A> Eigenschaft auf festlegen `true` , können Sie bis zu 32 KB Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-112">If you set the <xref:System.Windows.Forms.TextBox.Multiline%2A> property to `true`, you can enter up to 32 KB of text.</span></span> <span data-ttu-id="c1d8c-113">Die- <xref:System.Windows.Forms.TextBox.Text%2A> Eigenschaft kann zur Entwurfszeit mit dem Eigenschaften Fenster, zur Laufzeit im Code oder durch Benutzereingaben zur Laufzeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-113">The <xref:System.Windows.Forms.TextBox.Text%2A> property can be set at design time with the Properties Window, at run time in code, or by user input at run time.</span></span> <span data-ttu-id="c1d8c-114">Der aktuelle Inhalt eines Textfelds kann zur Laufzeit abgerufen werden, indem die-Eigenschaft gelesen wird <xref:System.Windows.Forms.TextBox.Text%2A> .</span><span class="sxs-lookup"><span data-stu-id="c1d8c-114">The current contents of a text box can be retrieved at run time by reading the <xref:System.Windows.Forms.TextBox.Text%2A> property.</span></span>  
  
 <span data-ttu-id="c1d8c-115">Im folgenden Codebeispiel wird der Text im-Steuerelement zur Laufzeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-115">The following code example sets text in the control at run time.</span></span> <span data-ttu-id="c1d8c-116">Die `InitializeMyControl` Prozedur wird nicht automatisch ausgeführt. Sie muss aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c1d8c-116">The `InitializeMyControl` procedure will not execute automatically; it must be called.</span></span>  
  
```vb  
Private Sub InitializeMyControl()  
   ' Put some text into the control first.  
   TextBox1.Text = "This is a TextBox control."  
End Sub  
```  
  
```csharp  
private void InitializeMyControl() {  
   // Put some text into the control first.  
   textBox1.Text = "This is a TextBox control.";  
}  
```  
  
```cpp  
private:  
   void InitializeMyControl()  
   {  
      // Put some text into the control first.  
      textBox1->Text = "This is a TextBox control.";  
   }  
```  
  
## <a name="see-also"></a><span data-ttu-id="c1d8c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1d8c-117">See also</span></span>

- <xref:System.Windows.Forms.TextBox>
- [<span data-ttu-id="c1d8c-118">Vorgehensweise: Steuern der Einfügemarke in einem TextBox-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c1d8c-118">How to: Control the Insertion Point in a Windows Forms TextBox Control</span></span>](how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [<span data-ttu-id="c1d8c-119">Vorgehensweise: Erstellen eines Kennwort-Textfelds mit dem TextBox-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c1d8c-119">How to: Create a Password Text Box with the Windows Forms TextBox Control</span></span>](how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)
- [<span data-ttu-id="c1d8c-120">Vorgehensweise: Erstellen eines schreibgeschützten Textfelds</span><span class="sxs-lookup"><span data-stu-id="c1d8c-120">How to: Create a Read-Only Text Box</span></span>](how-to-create-a-read-only-text-box-windows-forms.md)
- [<span data-ttu-id="c1d8c-121">Vorgehensweise: Setzen von Anführungszeichen in Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="c1d8c-121">How to: Put Quotation Marks in a String</span></span>](how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [<span data-ttu-id="c1d8c-122">Vorgehensweise: Programmgesteuertes Auswählen von Text im TextBox-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c1d8c-122">How to: Select Text in the Windows Forms TextBox Control</span></span>](how-to-select-text-in-the-windows-forms-textbox-control.md)
- [<span data-ttu-id="c1d8c-123">Vorgehensweise: Anzeigen mehrerer Zeilen im TextBox-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c1d8c-123">How to: View Multiple Lines in the Windows Forms TextBox Control</span></span>](how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [<span data-ttu-id="c1d8c-124">TextBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c1d8c-124">TextBox Control</span></span>](textbox-control-windows-forms.md)
