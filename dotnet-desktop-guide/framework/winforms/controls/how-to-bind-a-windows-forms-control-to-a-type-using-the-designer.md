---
title: Binden des Steuer Elements an einen Typ mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], binding to a type
- BindingSource component [Windows Forms], binding to a type
- types [Windows Forms], binding controls to
ms.assetid: 5ab984b5-c2d0-4638-a572-1c84013e8746
ms.openlocfilehash: 2257489e123ceeea819ad3538952db51b726c7e5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975718"
---
# <a name="how-to-bind-a-windows-forms-control-to-a-type-using-the-designer"></a><span data-ttu-id="01d27-102">Vorgehensweise: Binden eines Windows Forms-Steuerelements an einen Typ mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="01d27-102">How to: Bind a Windows Forms Control to a Type Using the Designer</span></span>

<span data-ttu-id="01d27-103">Beim Erstellen von Steuerelementen, die mit Daten interagieren, ist es manchmal erforderlich, ein Steuerelement an einen Typ statt an ein Objekt zu binden.</span><span class="sxs-lookup"><span data-stu-id="01d27-103">When you are building controls that interact with data, you sometimes need to bind a control to a type, rather than an object.</span></span> <span data-ttu-id="01d27-104">Sie müssen normalerweise ein Steuerelement zur Entwurfszeit an einen Typ binden, wenn Daten möglicherweise nicht verfügbar sind, aber die datengebundenen Steuerelemente dennoch Daten von der öffentlichen Schnittstelle eines Typs anzeigen sollen.</span><span class="sxs-lookup"><span data-stu-id="01d27-104">You typically need to bind a control to a type at design time, when data may not be available, but you still want your data-bound controls to display data from a type's public interface.</span></span> <span data-ttu-id="01d27-105">Die folgenden Prozeduren veranschaulichen, wie ein neues erstellt <xref:System.Windows.Forms.BindingSource> wird, das an einen-Typ gebunden ist, und wie eine der-Eigenschaften des Typs an die- <xref:System.Windows.Forms.TextBox.Text%2A> Eigenschaft eines gebunden wird <xref:System.Windows.Forms.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="01d27-105">The following procedures demonstrate how to create a new <xref:System.Windows.Forms.BindingSource> that is bound to a type, and then how to bind one of the type's properties to the <xref:System.Windows.Forms.TextBox.Text%2A> property of a <xref:System.Windows.Forms.TextBox>.</span></span>

### <a name="to-bind-the-bindingsource-to-a-type"></a><span data-ttu-id="01d27-106">So binden Sie die BindingSource an einen Typen</span><span class="sxs-lookup"><span data-stu-id="01d27-106">To bind the BindingSource to a type</span></span>

1. <span data-ttu-id="01d27-107">Erstellen Sie ein Windows Forms Projekt (**Datei**  >  **neu**  >  **Projekt**  >  **Visual c#** oder **Visual Basic**  >  **klassische Desktop**  >  **Windows Forms Anwendung**).</span><span class="sxs-lookup"><span data-stu-id="01d27-107">Create a Windows Forms project (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>

2. <span data-ttu-id="01d27-108">Ziehen Sie eine Komponente in der **Entwurfs** Ansicht <xref:System.Windows.Forms.BindingSource> auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="01d27-108">In **Design** view, drag a <xref:System.Windows.Forms.BindingSource> component onto the form.</span></span>

3. <span data-ttu-id="01d27-109">Klicken Sie im **Eigenschaften** Fenster auf den Pfeil für die- <xref:System.Windows.Forms.BindingSource.DataSource%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="01d27-109">In the **Properties** window, click the arrow for the <xref:System.Windows.Forms.BindingSource.DataSource%2A> property.</span></span>

4. <span data-ttu-id="01d27-110">Klicken Sie im **DataSource-UI-Typ-Editor** auf **Projektdatenquelle hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="01d27-110">In the **DataSource UI Type Editor**, click **Add Project Data Source**.</span></span>

5. <span data-ttu-id="01d27-111">Wählen Sie auf der Seite **Datenquellentyp auswählen** die Option **Objekt** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="01d27-111">On the **Choose a Data Source Type** page, select **Object** and click **Next**.</span></span>

6. <span data-ttu-id="01d27-112">Wählen Sie den Typ aus, an den gebunden werden soll:</span><span class="sxs-lookup"><span data-stu-id="01d27-112">Select the type to bind to:</span></span>

    - <span data-ttu-id="01d27-113">Wenn sich der Typ, den Sie binden möchten, im aktuellen Projekt befindet oder die Assembly, die den Typ enthält, bereits als Verweis hinzugefügt ist, müssen Sie die Knoten erweitern, um den gewünschten Typ zu suchen. Wählen Sie ihn anschließend aus.</span><span class="sxs-lookup"><span data-stu-id="01d27-113">If the type you want to bind to is in the current project, or the assembly that contains the type is already added as a reference, expand the nodes to find the type you want, and then select it.</span></span>

      <span data-ttu-id="01d27-114">\- oder -</span><span class="sxs-lookup"><span data-stu-id="01d27-114">\-or-</span></span>

    - <span data-ttu-id="01d27-115">Wenn sich der Typ, an den Sie binden möchten, in einer anderen Assembly befindet, die derzeit nicht in der Liste der Verweise enthalten ist, klicken Sie auf **Verweis hinzufügen** und dann auf die Registerkarte **Projekte** . Wählen Sie das Projekt aus, das das gewünschte Geschäftsobjekt enthält, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="01d27-115">If the type you want to bind to is in another assembly, not currently in the list of references, click **Add Reference**, and then click the **Projects** tab. Select the project that contains the business object you want and click **OK**.</span></span> <span data-ttu-id="01d27-116">Dieses Projekt erscheint in der Liste der Assemblys. Dadurch können Sie die Knoten erweitern, um den gewünschten Typ zu suchen und ihn anschließend auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="01d27-116">This project will appear in the list of assemblies, so you can expand the nodes to find the type you want, and then select it.</span></span>

      > [!NOTE]
      > <span data-ttu-id="01d27-117">Deaktivieren Sie das Dialogfeld **Assemblys ausblenden, die mit „Microsoft“ oder „System“ beginnen**, wenn Sie an einen Typen in einem Framework oder einer Microsoft-Assembly binden möchten.</span><span class="sxs-lookup"><span data-stu-id="01d27-117">If you want to bind to a type in a framework or Microsoft assembly, clear the **Hide assemblies that begin with Microsoft or System** check box.</span></span>

7. <span data-ttu-id="01d27-118">Klicken Sie auf **Weiter** und dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="01d27-118">Click **Next**, and then click **Finish**.</span></span>

### <a name="to-bind-the-control-to-the-bindingsource"></a><span data-ttu-id="01d27-119">So binden Sie das Steuerelement an die BindingSource</span><span class="sxs-lookup"><span data-stu-id="01d27-119">To bind the control to the BindingSource</span></span>

1. <span data-ttu-id="01d27-120">Fügen Sie dem Formular eine <xref:System.Windows.Forms.TextBox> hinzu.</span><span class="sxs-lookup"><span data-stu-id="01d27-120">Add a <xref:System.Windows.Forms.TextBox> to the form.</span></span>

2. <span data-ttu-id="01d27-121">Erweitern Sie im Fenster **Eigenschaften** den Knoten **(DataBindings)**.</span><span class="sxs-lookup"><span data-stu-id="01d27-121">In the **Properties** window, expand the **(DataBindings)** node.</span></span>

3. <span data-ttu-id="01d27-122">Klicken Sie auf den Pfeil neben der- <xref:System.Windows.Forms.TextBox.Text%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="01d27-122">Click the arrow next to the <xref:System.Windows.Forms.TextBox.Text%2A> property.</span></span>

4. <span data-ttu-id="01d27-123">Erweitern Sie im **DataSource-Typ-Editor für die Benutzeroberfläche** den Knoten für das <xref:System.Windows.Forms.BindingSource> zuvor hinzugefügte, und wählen Sie die Eigenschaft des gebundenen Typs aus, die Sie an die- <xref:System.Windows.Forms.TextBox.Text%2A> Eigenschaft des binden möchten <xref:System.Windows.Forms.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="01d27-123">In the **DataSource UI Type Editor**, expand the node for the <xref:System.Windows.Forms.BindingSource> added previously, and select the property of the bound type you want to bind to the <xref:System.Windows.Forms.TextBox.Text%2A> property of the <xref:System.Windows.Forms.TextBox>.</span></span>

## <a name="see-also"></a><span data-ttu-id="01d27-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01d27-124">See also</span></span>

- [<span data-ttu-id="01d27-125">BindingSource-Komponente</span><span class="sxs-lookup"><span data-stu-id="01d27-125">BindingSource Component</span></span>](bindingsource-component.md)
- [<span data-ttu-id="01d27-126">Vorgehensweise: Binden eines Windows Forms-Steuerelements an einen Typ</span><span class="sxs-lookup"><span data-stu-id="01d27-126">How to: Bind a Windows Forms Control to a Type</span></span>](how-to-bind-a-windows-forms-control-to-a-type.md)
- [<span data-ttu-id="01d27-127">Binden von Steuerelementen an Daten in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="01d27-127">Bind controls to data in Visual Studio</span></span>](/visualstudio/data-tools/bind-controls-to-data-in-visual-studio)
