---
title: Hinzufügen von Steuerelementen ohne Benutzeroberfläche
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- NonVisualSelection
helpviewer_keywords:
- invisible controls [Windows Forms]
- Windows Forms controls, adding to form
- controls [Windows Forms], nonvisual
- Windows Forms controls, nonvisual
- nonvisual controls [Windows Forms]
ms.assetid: 52134d9c-cff6-4eed-8e2b-3d5eb3bd494e
ms.openlocfilehash: c1ab1ec848b4c7a19ed9a65b67e17679bac215cd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976251"
---
# <a name="how-to-add-controls-without-a-user-interface-to-windows-forms"></a><span data-ttu-id="76db0-102">Gewusst wie: Hinzufügen von Steuerelementen ohne Benutzeroberfläche zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="76db0-102">How to: Add Controls Without a User Interface to Windows Forms</span></span>

<span data-ttu-id="76db0-103">Ein nicht visuelles Steuerelement (oder eine Komponente) stellt Funktionen für Ihre Anwendung bereit.</span><span class="sxs-lookup"><span data-stu-id="76db0-103">A nonvisual control (or component) provides functionality to your application.</span></span> <span data-ttu-id="76db0-104">Im Gegensatz zu anderen Steuerelementen bieten Komponenten keine Benutzeroberfläche für den Benutzer und müssen daher nicht auf der Windows Forms-Designer Oberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="76db0-104">Unlike other controls, components do not provide a user interface to the user and thus do not need to be displayed on the Windows Forms Designer surface.</span></span> <span data-ttu-id="76db0-105">Wenn eine Komponente zu einem Formular hinzugefügt wird, zeigt der Windows Forms-Designer am unteren Rand des Formulars, in dem alle Komponenten angezeigt werden, eine Größe an, die geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="76db0-105">When a component is added to a form, the Windows Forms Designer displays a resizable tray at the bottom of the form where all components are displayed.</span></span> <span data-ttu-id="76db0-106">Nachdem ein Steuerelement der Komponenten Leiste hinzugefügt wurde, können Sie die Komponente auswählen und deren Eigenschaften wie jedes andere Steuerelement im Formular festlegen.</span><span class="sxs-lookup"><span data-stu-id="76db0-106">Once a control has been added to the component tray, you can select the component and set its properties as you would any other control on the form.</span></span>

## <a name="add-a-component-to-a-windows-form"></a><span data-ttu-id="76db0-107">Hinzufügen einer Komponente zu einem Windows Form</span><span class="sxs-lookup"><span data-stu-id="76db0-107">Add a component to a Windows Form</span></span>

1. <span data-ttu-id="76db0-108">Öffnen Sie das Formular in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="76db0-108">Open the form in Visual Studio.</span></span> <span data-ttu-id="76db0-109">Weitere Informationen finden Sie unter Gewusst [wie: Anzeigen von Windows Forms im Designer](/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="76db0-109">For details, see [How to: Display Windows Forms in the Designer](/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).</span></span>

2. <span data-ttu-id="76db0-110">Klicken Sie in der **Toolbox** auf eine Komponente, und ziehen Sie Sie in das Formular.</span><span class="sxs-lookup"><span data-stu-id="76db0-110">In the **Toolbox**, click a component and drag it to your form.</span></span>

     <span data-ttu-id="76db0-111">Die Komponente wird in der Komponenten Leiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76db0-111">Your component appears in the component tray.</span></span>

<span data-ttu-id="76db0-112">Darüber hinaus können Komponenten zur Laufzeit einem Formular hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="76db0-112">Furthermore, components can be added to a form at run time.</span></span> <span data-ttu-id="76db0-113">Dies ist ein häufiges Szenario, insbesondere, da Komponenten keinen visuellen Ausdruck aufweisen, anders als Steuerelemente mit einer Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="76db0-113">This is a common scenario, especially because components do not have a visual expression, unlike controls that have a user interface.</span></span> <span data-ttu-id="76db0-114">Im folgenden Beispiel <xref:System.Windows.Forms.Timer> wird eine Komponente zur Laufzeit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="76db0-114">In the example below, a <xref:System.Windows.Forms.Timer> component is added at run time.</span></span> <span data-ttu-id="76db0-115">(Beachten Sie, dass Visual Studio eine Reihe von unterschiedlichen Timern enthält. verwenden Sie in diesem Fall eine Windows Forms <xref:System.Windows.Forms.Timer> Komponente.</span><span class="sxs-lookup"><span data-stu-id="76db0-115">(Note that Visual Studio contains a number of different timers; in this case, use a Windows Forms <xref:System.Windows.Forms.Timer> component.</span></span> <span data-ttu-id="76db0-116">Weitere Informationen zu den verschiedenen Timern in Visual Studio finden [Sie unter Einführung in Server-Based Timer](/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).)</span><span class="sxs-lookup"><span data-stu-id="76db0-116">For more information about the different timers in Visual Studio, see [Introduction to Server-Based Timers](/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).)</span></span>

> [!CAUTION]
> <span data-ttu-id="76db0-117">Komponenten verfügen häufig über Steuerungs spezifische Eigenschaften, die für eine effektive Funktionsweise der Komponente festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="76db0-117">Components often have control-specific properties that must be set for the component to function effectively.</span></span> <span data-ttu-id="76db0-118">Im Fall der nachfolgenden <xref:System.Windows.Forms.Timer> Komponente legen Sie die- `Interval` Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="76db0-118">In the case of the <xref:System.Windows.Forms.Timer> component below, you set the `Interval` property.</span></span> <span data-ttu-id="76db0-119">Stellen Sie sicher, dass Sie beim Hinzufügen von Komponenten zu Ihrem Projekt die Eigenschaften festlegen, die für diese Komponente erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="76db0-119">Be sure, when adding components to your project, that you set the properties necessary for that component.</span></span>

## <a name="add-a-component-to-a-windows-form-programmatically"></a><span data-ttu-id="76db0-120">Programm gesteuertes Hinzufügen einer Komponente zu einem Windows Form</span><span class="sxs-lookup"><span data-stu-id="76db0-120">Add a component to a Windows Form programmatically</span></span>

1. <span data-ttu-id="76db0-121">Erstellen Sie im Code eine Instanz der- <xref:System.Windows.Forms.Timer> Klasse.</span><span class="sxs-lookup"><span data-stu-id="76db0-121">Create an instance of the <xref:System.Windows.Forms.Timer> class in code.</span></span>

2. <span data-ttu-id="76db0-122">Legen Sie die- `Interval` Eigenschaft fest, um die Zeit zwischen Ticks des Timers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="76db0-122">Set the `Interval` property to determine the time between ticks of the timer.</span></span>

3. <span data-ttu-id="76db0-123">Konfigurieren Sie alle anderen erforderlichen Eigenschaften für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="76db0-123">Configure any other necessary properties for your component.</span></span>

     <span data-ttu-id="76db0-124">Der folgende Code zeigt die Erstellung eines- <xref:System.Windows.Forms.Timer> Objekts, dessen- `Interval` Eigenschaft auf festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="76db0-124">The following code shows the creation of a <xref:System.Windows.Forms.Timer> with its `Interval` property set.</span></span>

    ```vb
    Public Sub CreateTimer()
       Dim timerKeepTrack As New System.Windows.Forms.Timer
       timerKeepTrack.Interval = 1000
    End Sub
    ```

    ```csharp
    public void createTimer()
    {
       System.Windows.Forms.Timer timerKeepTrack = new
           System.Windows.Forms.Timer();
       timerKeepTrack.Interval = 1000;
    }
    ```

    ```cpp
    public:
       void createTimer()
       {
          System::Windows::Forms::Timer^ timerKeepTrack = gcnew
             System::Windows::Forms::Timer();
          timerKeepTrack->Interval = 1000;
       }
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="76db0-125">Sie können den lokalen Computer mit einem Sicherheitsrisiko über das Netzwerk verfügbar machen, indem Sie auf ein schädliches UserControl-Steuerelement verweisen.</span><span class="sxs-lookup"><span data-stu-id="76db0-125">You might expose your local computer to a security risk through the network by referencing a malicious UserControl.</span></span> <span data-ttu-id="76db0-126">Dies wäre nur ein Problem, wenn eine böswillige Person ein schädliches benutzerdefiniertes Steuerelement erstellt, gefolgt von dem, das Sie versehentlich dem Projekt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="76db0-126">This would only be a concern in the case of a malicious person creating a damaging custom control, followed by you mistakenly adding it to your project.</span></span>

## <a name="see-also"></a><span data-ttu-id="76db0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76db0-127">See also</span></span>

- [<span data-ttu-id="76db0-128">Windows Forms Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="76db0-128">Windows Forms Controls</span></span>](index.md)
- [<span data-ttu-id="76db0-129">How to: Hinzufügen von Steuerelementen zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="76db0-129">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
- [<span data-ttu-id="76db0-130">Gewusst wie: Hinzufügen von ActiveX-Steuerelementen zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="76db0-130">How to: Add ActiveX Controls to Windows Forms</span></span>](how-to-add-activex-controls-to-windows-forms.md)
- [<span data-ttu-id="76db0-131">Einfügen von Steuerelementen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="76db0-131">Putting Controls on Windows Forms</span></span>](putting-controls-on-windows-forms.md)
- [<span data-ttu-id="76db0-132">Beschriften einzelner Steuerelemente für Windows Forms und Konfigurieren von Shortcuts für diese Elemente</span><span class="sxs-lookup"><span data-stu-id="76db0-132">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [<span data-ttu-id="76db0-133">Steuerelemente für Windows Forms</span><span class="sxs-lookup"><span data-stu-id="76db0-133">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
- [<span data-ttu-id="76db0-134">Windows Forms-Steuerelemente nach Funktion</span><span class="sxs-lookup"><span data-stu-id="76db0-134">Windows Forms Controls by Function</span></span>](windows-forms-controls-by-function.md)
