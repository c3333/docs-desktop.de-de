---
title: 'Vorgehensweise: Definieren eines Symbols für eine Symbolleistenschaltfläche mithilfe des Designers'
ms.date: 03/30/2017
helpviewer_keywords:
- toolbars [Windows Forms], adding icons to buttons
- examples [Windows Forms], toolbars
- images [Windows Forms], toolbar buttons
- buttons [Windows Forms], images
- icons [Windows Forms], toolbar buttons
- ToolBar control [Windows Forms], adding icons to buttons
ms.assetid: d848f38e-67f2-49d4-8e88-01c845c06c02
ms.openlocfilehash: 49e93f12bebbf409e6b3a06634556b9103c85f44
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975679"
---
# <a name="how-to-define-an-icon-for-a-toolbar-button-using-the-designer"></a><span data-ttu-id="f15da-102">Vorgehensweise: Definieren eines Symbols für eine Symbolleistenschaltfläche mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="f15da-102">How to: Define an Icon for a ToolBar Button Using the Designer</span></span>

> [!NOTE]
> <span data-ttu-id="f15da-103">Obwohl das <xref:System.Windows.Forms.ToolStrip>-Steuerelement das <xref:System.Windows.Forms.ToolBar>-Steuerelement ersetzt und funktionell erweitert, wird das <xref:System.Windows.Forms.ToolBar>-Steuerelement sowohl aus Gründen der Abwärtskompatibilität als auch, falls gewünscht, für die zukünftige Verwendung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f15da-103">The <xref:System.Windows.Forms.ToolStrip> control replaces and adds functionality to the <xref:System.Windows.Forms.ToolBar> control; however, the <xref:System.Windows.Forms.ToolBar> control is retained for both backward compatibility and future use, if you choose.</span></span>

<span data-ttu-id="f15da-104"><xref:System.Windows.Forms.ToolBar> mithilfe von Schaltflächen können darin Symbole angezeigt werden, die von Benutzern leichter identifiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="f15da-104"><xref:System.Windows.Forms.ToolBar> buttons are able to display icons within them for easy identification by users.</span></span> <span data-ttu-id="f15da-105">Dies wird erreicht, indem der Komponente Bilder hinzugefügt <xref:System.Windows.Forms.ImageList> und dem Steuerelement zugeordnet wird <xref:System.Windows.Forms.ToolBar> .</span><span class="sxs-lookup"><span data-stu-id="f15da-105">This is achieved through adding images to the <xref:System.Windows.Forms.ImageList> component and associating it with the <xref:System.Windows.Forms.ToolBar> control.</span></span>

<span data-ttu-id="f15da-106">Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein <xref:System.Windows.Forms.ToolBar> -Steuerelement und eine- <xref:System.Windows.Forms.ImageList> Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="f15da-106">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.ToolBar> control and an <xref:System.Windows.Forms.ImageList> component.</span></span> <span data-ttu-id="f15da-107">Weitere Informationen zum Einrichten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="f15da-107">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>

### <a name="to-set-an-icon-for-a-toolbar-button-at-design-time"></a><span data-ttu-id="f15da-108">So legen Sie ein Symbol für eine Symbolleisten-Schaltfläche zur Entwurfszeit fest</span><span class="sxs-lookup"><span data-stu-id="f15da-108">To set an icon for a toolbar button at design time</span></span>

1. <span data-ttu-id="f15da-109">Fügen Sie der Komponente Bilder hinzu <xref:System.Windows.Forms.ImageList> .</span><span class="sxs-lookup"><span data-stu-id="f15da-109">Add images to the <xref:System.Windows.Forms.ImageList> component.</span></span> <span data-ttu-id="f15da-110">Weitere Informationen finden Sie unter Gewusst [wie: Hinzufügen oder Entfernen von ImageList-Bildern mit dem Designer](how-to-add-or-remove-imagelist-images-with-the-designer.md).</span><span class="sxs-lookup"><span data-stu-id="f15da-110">For more information, see [How to: Add or Remove ImageList Images with the Designer](how-to-add-or-remove-imagelist-images-with-the-designer.md).</span></span>

2. <span data-ttu-id="f15da-111">Wählen Sie das <xref:System.Windows.Forms.ToolBar> Steuerelement auf dem Formular aus.</span><span class="sxs-lookup"><span data-stu-id="f15da-111">Select the <xref:System.Windows.Forms.ToolBar> control on your form.</span></span>

3. <span data-ttu-id="f15da-112">Legen Sie im Fenster **Eigenschaften** die <xref:System.Windows.Forms.ToolBar> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.ToolBar.ImageList%2A> auf die-Komponente fest <xref:System.Windows.Forms.ImageList> .</span><span class="sxs-lookup"><span data-stu-id="f15da-112">In the **Properties** window, set the <xref:System.Windows.Forms.ToolBar> control's <xref:System.Windows.Forms.ToolBar.ImageList%2A> property to the <xref:System.Windows.Forms.ImageList> component.</span></span>

4. <span data-ttu-id="f15da-113">Klicken Sie <xref:System.Windows.Forms.ToolBar> auf die-Eigenschaft des Steuer Elements, um es auszuwählen, und klicken Sie auf die Schaltfläche mit den Auslassungs Punkten ( <xref:System.Windows.Forms.ToolBar.Buttons%2A> ![ ...) in der Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ), um den **ToolBarButton**-Auflistungs-Editor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f15da-113">Click the <xref:System.Windows.Forms.ToolBar> control's <xref:System.Windows.Forms.ToolBar.Buttons%2A> property to select it, and click the ellipsis (![The Ellipsis button (...) in the Properties window of Visual Studio.](./media/visual-studio-ellipsis-button.png)) button to open the **ToolBarButton Collection Editor**.</span></span>

5. <span data-ttu-id="f15da-114">Mithilfe der Schaltfläche **Hinzufügen** können Sie dem Steuerelement Schaltflächen hinzufügen <xref:System.Windows.Forms.ToolBar> .</span><span class="sxs-lookup"><span data-stu-id="f15da-114">Use the **Add** button to add buttons to the <xref:System.Windows.Forms.ToolBar> control.</span></span>

6. <span data-ttu-id="f15da-115">Legen Sie im Fenster **Eigenschaften** , das im Bereich auf der rechten Seite des **ToolBarButton**-Auflistungs-Editors angezeigt wird, die- <xref:System.Windows.Forms.ToolBarButton.ImageIndex%2A> Eigenschaft jeder Symbolleisten-Schaltfläche auf einen der Werte in der Liste fest, der aus den Bildern gezeichnet wird, die Sie der Komponente hinzugefügt haben <xref:System.Windows.Forms.ImageList> .</span><span class="sxs-lookup"><span data-stu-id="f15da-115">In the **Properties** window that appears in the pane on the right side of the **ToolBarButton Collection Editor**, set the <xref:System.Windows.Forms.ToolBarButton.ImageIndex%2A> property of each toolbar button to one of the values in the list, which is drawn from the images you added to the <xref:System.Windows.Forms.ImageList> component.</span></span>

## <a name="see-also"></a><span data-ttu-id="f15da-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f15da-116">See also</span></span>

- <xref:System.Windows.Forms.ToolBar>
- [<span data-ttu-id="f15da-117">Vorgehensweise: Auslösen von Menüereignissen für Symbolleistenschaltflächen</span><span class="sxs-lookup"><span data-stu-id="f15da-117">How to: Trigger Menu Events for Toolbar Buttons</span></span>](how-to-trigger-menu-events-for-toolbar-buttons.md)
- [<span data-ttu-id="f15da-118">ToolBar-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="f15da-118">ToolBar Control</span></span>](toolbar-control-windows-forms.md)
- [<span data-ttu-id="f15da-119">ImageList-Komponente</span><span class="sxs-lookup"><span data-stu-id="f15da-119">ImageList Component</span></span>](imagelist-component-windows-forms.md)
