---
title: 'Vorgehensweise: Aktivieren von AutoComplete in ToolStrip-Steuerelementen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- AutoComplete [Windows Forms], examples
- toolbars [Windows Forms], AutoComplete
- examples [Windows Forms], toolbars
- AutoComplete [Windows Forms], enabling in toolbars
- ToolStripComboBox class [Windows Forms], examples
- ToolStrip control [Windows Forms], AutoComplete
ms.assetid: fd66d085-1af1-45d4-930a-cde944da2e16
ms.openlocfilehash: 18b17aaea9d2354c03bb43f3fdd8d3779697cf58
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975645"
---
# <a name="how-to-enable-autocomplete-in-toolstrip-controls-in-windows-forms"></a><span data-ttu-id="8ed5c-102">Gewusst wie: Aktivieren von AutoComplete in ToolStrip-Steuerelementen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8ed5c-102">How to: Enable AutoComplete in ToolStrip Controls in Windows Forms</span></span>
<span data-ttu-id="8ed5c-103">Im folgenden Verfahren wird ein <xref:System.Windows.Forms.ToolStripLabel> mit einem kombiniert, <xref:System.Windows.Forms.ToolStripComboBox> das zum Anzeigen einer Liste von Elementen (z. b. zuletzt besuchte Websites) gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ed5c-103">The following procedure combines a <xref:System.Windows.Forms.ToolStripLabel> with a <xref:System.Windows.Forms.ToolStripComboBox> that can be dropped down to show a list of items, such as recently visited Web sites.</span></span> <span data-ttu-id="8ed5c-104">Wenn der Benutzer ein Zeichen eingibt, das mit dem ersten Zeichen eines der Elemente in der Liste übereinstimmt, wird das Element sofort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8ed5c-104">If the user types a character that matches the first character of one of the items in the list, the item is immediately displayed.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="8ed5c-105">Die automatische Vervollständigung funktioniert mit Steuer `ToolStrip` Elementen auf die gleiche Weise wie mit herkömmlichen Steuerelementen wie <xref:System.Windows.Forms.ComboBox> und <xref:System.Windows.Forms.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="8ed5c-105">Automatic completion works with `ToolStrip` controls in the same way that it works with traditional controls such as <xref:System.Windows.Forms.ComboBox> and <xref:System.Windows.Forms.TextBox>.</span></span>  
  
### <a name="to-enable-autocomplete-in-a-toolstrip-control"></a><span data-ttu-id="8ed5c-106">So aktivieren Sie AutoComplete in einem ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="8ed5c-106">To enable AutoComplete in a ToolStrip control</span></span>  
  
1. <span data-ttu-id="8ed5c-107">Erstellen <xref:System.Windows.Forms.ToolStrip> Sie ein-Steuerelement, und fügen Sie ihm Elemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="8ed5c-107">Create a <xref:System.Windows.Forms.ToolStrip> control and add items to it.</span></span>  
  
    ```vb  
    ToolStrip1 = New System.Windows.Forms.ToolStrip  
    ToolStrip1.Items.AddRange(New System.Windows.Forms.ToolStripItem()_  
        {ToolStripLabel1, ToolStripComboBox1})  
    ```  
  
    ```csharp  
    toolStrip1 = new System.Windows.Forms.ToolStrip();  
    toolStrip1.Items.AddRange(new System.Windows.Forms.ToolStripItem[]
        {toolStripLabel1, toolStripComboBox1});  
    ```  
  
2. <span data-ttu-id="8ed5c-108">Legen <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> Sie die-Eigenschaft der Bezeichnung und das Kombinations Feld auf fest, <xref:System.Windows.Forms.ToolStripItemOverflow.Never> damit die Liste unabhängig von der Größe des Formulars immer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8ed5c-108">Set the <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> property of the label and the combo box to <xref:System.Windows.Forms.ToolStripItemOverflow.Never> so that the list is always available regardless of the form's size.</span></span>  
  
    ```vb  
    ToolStripLabel1.Overflow = _  
        System.Windows.Forms.ToolStripItemOverflow.Never  
    ToolStripComboBox1.Overflow = _  
        System.Windows.Forms.ToolStripItemOverflow.Never  
    ```  
  
    ```csharp  
    toolStripLabel1.Overflow = _  
        System.Windows.Forms.ToolStripItemOverflow.Never  
    toolStripComboBox1.Overflow = System.Windows.Forms.ToolStripItemOverflow.Never  
    ```  
  
3. <span data-ttu-id="8ed5c-109">Fügen Sie der Items-Auflistung des-Steuer Elements Wörter hinzu <xref:System.Windows.Forms.ToolStripComboBox> .</span><span class="sxs-lookup"><span data-stu-id="8ed5c-109">Add words to the Items collection of the <xref:System.Windows.Forms.ToolStripComboBox> control.</span></span>  
  
    ```vb  
    ToolStripComboBox1.Items.AddRange(New Object() {"First Item", _  
        "Second Item", "Third Item"})  
    ```  
  
    ```csharp  
    toolStripComboBox1.Items.AddRange(new object[] {"First item", "Second item", "Third item"});  
    ```  
  
4. <span data-ttu-id="8ed5c-110">Legen Sie die- <xref:System.Windows.Forms.ComboBox.AutoCompleteMode%2A> Eigenschaft des Kombinations Felds auf fest <xref:System.Windows.Forms.AutoCompleteMode.Append> .</span><span class="sxs-lookup"><span data-stu-id="8ed5c-110">Set the <xref:System.Windows.Forms.ComboBox.AutoCompleteMode%2A> property of the combo box to <xref:System.Windows.Forms.AutoCompleteMode.Append>.</span></span>  
  
    ```vb  
    ToolStripComboBox1.AutoCompleteMode = _  
        System.Windows.Forms.AutoCompleteMode.Append  
    ```  
  
    ```csharp  
    toolStripComboBox1.AutoCompleteMode = System.Windows.Forms.AutoCompleteMode.Append;  
    ```  
  
5. <span data-ttu-id="8ed5c-111">Legen Sie die- <xref:System.Windows.Forms.ComboBox.AutoCompleteSource%2A> Eigenschaft des Kombinations Felds auf fest <xref:System.Windows.Forms.AutoCompleteSource.ListItems> .</span><span class="sxs-lookup"><span data-stu-id="8ed5c-111">Set the <xref:System.Windows.Forms.ComboBox.AutoCompleteSource%2A> property of the combo box to <xref:System.Windows.Forms.AutoCompleteSource.ListItems>.</span></span>  
  
    ```vb  
    ToolStripComboBox1.AutoCompleteSource = _  
        System.Windows.Forms.AutoCompleteSource.ListItems  
    ```  
  
    ```csharp  
    toolStripComboBox1.AutoCompleteSource = System.Windows.Forms.AutoCompleteSource.ListItems;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="8ed5c-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ed5c-112">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripLabel>
- <xref:System.Windows.Forms.ToolStripComboBox>
- <xref:System.Windows.Forms.ToolStripComboBox.AutoCompleteMode%2A>
- <xref:System.Windows.Forms.ToolStripComboBox.AutoCompleteSource%2A>
- [<span data-ttu-id="8ed5c-113">Übersicht über das ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="8ed5c-113">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
- [<span data-ttu-id="8ed5c-114">Architektur des ToolStrip-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="8ed5c-114">ToolStrip Control Architecture</span></span>](toolstrip-control-architecture.md)
- [<span data-ttu-id="8ed5c-115">Zusammenfassung der ToolStrip-Technologie</span><span class="sxs-lookup"><span data-stu-id="8ed5c-115">ToolStrip Technology Summary</span></span>](toolstrip-technology-summary.md)
