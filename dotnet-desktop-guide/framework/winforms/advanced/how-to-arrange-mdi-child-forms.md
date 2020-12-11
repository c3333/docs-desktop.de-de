---
title: 'Vorgehensweise: Anordnen von untergeordneten MDI-Formularen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- child forms [Windows Forms], arranging
- MDI [Windows Forms], arranging child forms
ms.assetid: a0786378-3206-4ccc-898e-7d3b38cc5089
ms.openlocfilehash: 7e4d5a80961ae37951251dffa30cb8e75b20be27
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972382"
---
# <a name="how-to-arrange-mdi-child-forms"></a><span data-ttu-id="d728a-102">Vorgehensweise: Anordnen von untergeordneten MDI-Formularen</span><span class="sxs-lookup"><span data-stu-id="d728a-102">How to: Arrange MDI Child Forms</span></span>
<span data-ttu-id="d728a-103">Anwendungen verfügen häufig über Menübefehle für Aktionen wie z. B. Nebeneinander anordnen, Überlappend anordnen und Anordnen, über die das Layout des geöffneten untergeordneten MDI-Formulars gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="d728a-103">Often, applications will have menu commands for actions such as Tile, Cascade, and Arrange, which control the layout of the open MDI child forms.</span></span> <span data-ttu-id="d728a-104">Sie können die <xref:System.Windows.Forms.Form.LayoutMdi%2A> -Methode mit einem der <xref:System.Windows.Forms.MdiLayout>-Enumerationswerte anwenden, um die untergeordneten Formulare in einem übergeordneten MDI-Enumerationswerteformular neu anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d728a-104">You can use the <xref:System.Windows.Forms.Form.LayoutMdi%2A> method with one of the <xref:System.Windows.Forms.MdiLayout> enumeration values to rearrange the child forms in an MDI parent form.</span></span>  
  
 <span data-ttu-id="d728a-105">Mit <xref:System.Windows.Forms.MdiLayout>-Enumerationswerten werden untergeordnete Formulare als überlappend, nebeneinander oder untereinander bzw. in Form von untergeordneten Formularsymbolen im unteren Bereich des MDI-Formulars angeordnet.</span><span class="sxs-lookup"><span data-stu-id="d728a-105">The <xref:System.Windows.Forms.MdiLayout> enumeration values display child forms as cascading, as horizontally or vertically tiled, or as child form icons arranged along the lower portion of the MDI form.</span></span> <span data-ttu-id="d728a-106">Diese Werte haben dieselbe Auswirkung wie die Windows-Befehle, die Fenster **kaskadieren**, Fenster **nebeneinander anzeigen**, **gestapelte Fenster anzeigen** und **den Desktop anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="d728a-106">These values have the same effect as the Windows commands **Cascade windows**, **Show windows side by side**, **Show windows stacked**, and **Show the desktop**, respectively.</span></span>  
  
 <span data-ttu-id="d728a-107">Diese Methoden werden häufig als Ereignishandler aufgerufen, die vom <xref:System.Windows.Forms.Control.Click>-Ereignis eines Menüelements abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d728a-107">Often, these methods are used as the event handlers called by a menu item's <xref:System.Windows.Forms.Control.Click> event.</span></span> <span data-ttu-id="d728a-108">Auf diese Weise kann ein Menüelement mit dem Text "Fenster überlappend anzeigen" den gewünschten Effekt auf untergeordnete MDI-Fenster haben.</span><span class="sxs-lookup"><span data-stu-id="d728a-108">In this way, a menu item with the text "Cascade Windows" can have the desired effect on the MDI child windows.</span></span>  
  
### <a name="to-arrange-child-forms"></a><span data-ttu-id="d728a-109">So ordnen Sie untergeordnete Formulare an</span><span class="sxs-lookup"><span data-stu-id="d728a-109">To arrange child forms</span></span>  
  
1. <span data-ttu-id="d728a-110">Verwenden Sie in einer Methode die <xref:System.Windows.Forms.Form.LayoutMdi%2A> -Methode zum Festlegen der <xref:System.Windows.Forms.MdiLayout> -Enumeration für das übergeordnete MDI-Formular.</span><span class="sxs-lookup"><span data-stu-id="d728a-110">In a method, use the <xref:System.Windows.Forms.Form.LayoutMdi%2A> method to set the <xref:System.Windows.Forms.MdiLayout> enumeration for the MDI parent form.</span></span> <span data-ttu-id="d728a-111">Im folgenden Beispiel wird der <xref:System.Windows.Forms.MdiLayout.Cascade?displayProperty=nameWithType> -Enumerationswert für die untergeordneten Fenster des übergeordneten MDI-Formulars (`Form1`) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d728a-111">The following example uses the <xref:System.Windows.Forms.MdiLayout.Cascade?displayProperty=nameWithType> enumeration value for the child windows of the MDI parent form (`Form1`).</span></span> <span data-ttu-id="d728a-112">Die-Enumeration wird im Code während des-Ereignis Handlers für das- <xref:System.Windows.Forms.Control.Click> Ereignis des Menü Elements **Cascade Windows** verwendet.</span><span class="sxs-lookup"><span data-stu-id="d728a-112">The enumeration is used in code during the event handler for the <xref:System.Windows.Forms.Control.Click> event of the **Cascade Windows** menu item.</span></span>  
  
    ```vb  
    Protected Sub CascadeWindows_Click(ByVal sender As System.Object, ByVal e As System.EventArgs)  
       Me.LayoutMdi(System.Windows.Forms.MdiLayout.Cascade)  
    End Sub  
    ```  
  
    ```csharp  
    protected void CascadeWindows_Click(object sender, System.EventArgs e){  
       this.LayoutMdi(System.Windows.Forms.MdiLayout.Cascade);  
    }  
    ```  
  
    > [!NOTE]
    > <span data-ttu-id="d728a-113">Sie könne Fenster auch nebeneinander oder als Symbole anordnen, indem Sie den verwendeten <xref:System.Windows.Forms.MdiLayout> -Enumerationswert ändern.</span><span class="sxs-lookup"><span data-stu-id="d728a-113">You can also tile windows and arranging windows as icons by changing the <xref:System.Windows.Forms.MdiLayout> enumeration value used.</span></span>  
  
2. <span data-ttu-id="d728a-114">Wenn Sie Visual C# verwenden, fügen Sie folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d728a-114">If you’re using Visual C#, place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="d728a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d728a-115">See also</span></span>

- [<span data-ttu-id="d728a-116">MDI-Anwendungen (Multiple Document Interface)</span><span class="sxs-lookup"><span data-stu-id="d728a-116">Multiple-Document Interface (MDI) Applications</span></span>](multiple-document-interface-mdi-applications.md)
- [<span data-ttu-id="d728a-117">Vorgehensweise: Erstellen von übergeordneten MDI-Formularen</span><span class="sxs-lookup"><span data-stu-id="d728a-117">How to: Create MDI Parent Forms</span></span>](how-to-create-mdi-parent-forms.md)
- [<span data-ttu-id="d728a-118">Vorgehensweise: Erstellen von untergeordneten MDI-Formularen</span><span class="sxs-lookup"><span data-stu-id="d728a-118">How to: Create MDI Child Forms</span></span>](how-to-create-mdi-child-forms.md)
- [<span data-ttu-id="d728a-119">Vorgehensweise: Bestimmen des aktiven untergeordneten MDI-Elements</span><span class="sxs-lookup"><span data-stu-id="d728a-119">How to: Determine the Active MDI Child</span></span>](how-to-determine-the-active-mdi-child.md)
- [<span data-ttu-id="d728a-120">Vorgehensweise: Senden von Daten an das aktive untergeordnete MDI-Element</span><span class="sxs-lookup"><span data-stu-id="d728a-120">How to: Send Data to the Active MDI Child</span></span>](how-to-send-data-to-the-active-mdi-child.md)
