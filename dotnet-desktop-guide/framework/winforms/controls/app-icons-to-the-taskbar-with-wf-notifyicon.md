---
title: Hinzufügen von Anwendungssymbolen zur Taskleiste mit der NotifyIcon-Komponente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- TrayIcon
helpviewer_keywords:
- status area icons
- icons [Windows Forms], adding to taskbar
- NotifyIcon component
- taskbar [Windows Forms], adding icons
ms.assetid: d28c0fe6-aaf2-4df7-ad74-928d861a8510
ms.openlocfilehash: 46b50ecaabe75dba08fea922d7b5639031692269
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975790"
---
# <a name="how-to-add-application-icons-to-the-taskbar-with-the-windows-forms-notifyicon-component"></a><span data-ttu-id="70362-102">Vorgehensweise: Hinzufügen von Anwendungssymbolen zur Taskleiste mit der NotifyIcon-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="70362-102">How to: Add Application Icons to the TaskBar with the Windows Forms NotifyIcon Component</span></span>

<span data-ttu-id="70362-103">Die Windows Forms <xref:System.Windows.Forms.NotifyIcon> Komponente zeigt ein einzelnes Symbol im Status Benachrichtigungsbereich der Taskleiste an.</span><span class="sxs-lookup"><span data-stu-id="70362-103">The Windows Forms <xref:System.Windows.Forms.NotifyIcon> component displays a single icon in the status notification area of the taskbar.</span></span> <span data-ttu-id="70362-104">Um mehrere Symbole im Statusbereich anzuzeigen, müssen Sie <xref:System.Windows.Forms.NotifyIcon> über mehrere Komponenten im Formular verfügen.</span><span class="sxs-lookup"><span data-stu-id="70362-104">To display multiple icons in the status area, you must have multiple <xref:System.Windows.Forms.NotifyIcon> components on your form.</span></span> <span data-ttu-id="70362-105">Um das für ein Steuerelement angezeigte Symbol festzulegen, verwenden Sie die- <xref:System.Windows.Forms.NotifyIcon.Icon%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="70362-105">To set the icon displayed for a control, use the <xref:System.Windows.Forms.NotifyIcon.Icon%2A> property.</span></span> <span data-ttu-id="70362-106">Sie können auch Code im- <xref:System.Windows.Forms.NotifyIcon.DoubleClick> Ereignishandler schreiben, sodass etwas passiert, wenn der Benutzer auf das Symbol doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="70362-106">You can also write code in the <xref:System.Windows.Forms.NotifyIcon.DoubleClick> event handler so that something happens when the user double-clicks the icon.</span></span> <span data-ttu-id="70362-107">Beispielsweise können Sie festlegen, dass ein Dialogfeld angezeigt wird, in dem der Benutzer den durch das Symbol dargestellten Hintergrundprozess konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="70362-107">For example, you could make a dialog box appear for the user to configure the background process represented by the icon.</span></span>

> [!NOTE]
> <span data-ttu-id="70362-108">Die <xref:System.Windows.Forms.NotifyIcon> Komponente wird nur zu Benachrichtigungs Zwecken verwendet, um Benutzer darauf aufmerksam zu machen, dass eine Aktion oder ein Ereignis aufgetreten ist oder eine Änderung des Status einer bestimmten Art vorliegt.</span><span class="sxs-lookup"><span data-stu-id="70362-108">The <xref:System.Windows.Forms.NotifyIcon> component is used for notification purposes only, to alert users that an action or event has occurred or there has been a change in status of some sort.</span></span> <span data-ttu-id="70362-109">Sie sollten Menüs, Symbolleisten und andere Elemente der Benutzeroberfläche für die Standard Interaktion mit-Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="70362-109">You should use menus, toolbars, and other user-interface elements for standard interaction with applications.</span></span>

### <a name="to-set-the-icon"></a><span data-ttu-id="70362-110">So legen Sie das Symbol fest</span><span class="sxs-lookup"><span data-stu-id="70362-110">To set the icon</span></span>

1. <span data-ttu-id="70362-111">Weisen Sie der-Eigenschaft einen Wert zu <xref:System.Windows.Forms.NotifyIcon.Icon%2A> .</span><span class="sxs-lookup"><span data-stu-id="70362-111">Assign a value to the <xref:System.Windows.Forms.NotifyIcon.Icon%2A> property.</span></span> <span data-ttu-id="70362-112">Der Wert muss vom Typ sein `System.Drawing.Icon` und kann aus einer ICO-Datei geladen werden.</span><span class="sxs-lookup"><span data-stu-id="70362-112">The value must be of type `System.Drawing.Icon` and can be loaded from an .ico file.</span></span> <span data-ttu-id="70362-113">Sie können die Symbol Datei im Code oder durch Klicken auf die Schaltfläche mit den Auslassungs Zeichen ( ![ ...) im Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ) neben der <xref:System.Windows.Forms.NotifyIcon.Icon%2A> -Eigenschaft im **Eigenschaften** Fenster angeben und dann die Datei im **geöffneten** Dialogfeld öffnen.</span><span class="sxs-lookup"><span data-stu-id="70362-113">You can specify the icon file in code or by clicking the ellipsis button (![The Ellipsis button (...) in the Properties window of Visual Studio.](./media/visual-studio-ellipsis-button.png)) next to the <xref:System.Windows.Forms.NotifyIcon.Icon%2A> property in the **Properties** window, and then selecting the file in the **Open** dialog box that appears.</span></span>

2. <span data-ttu-id="70362-114">Legen Sie die <xref:System.Windows.Forms.NotifyIcon.Visible%2A> -Eigenschaft auf `true`fest.</span><span class="sxs-lookup"><span data-stu-id="70362-114">Set the <xref:System.Windows.Forms.NotifyIcon.Visible%2A> property to `true`.</span></span>

3. <span data-ttu-id="70362-115">Legen <xref:System.Windows.Forms.NotifyIcon.Text%2A> Sie die Eigenschaft auf eine entsprechende QuickInfo-Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="70362-115">Set the <xref:System.Windows.Forms.NotifyIcon.Text%2A> property to an appropriate ToolTip string.</span></span>

     <span data-ttu-id="70362-116">Im folgenden Codebeispiel ist der Pfad, der für den Speicherort des Symbols festgelegt wurde, der Ordner " **eigene** Dateien".</span><span class="sxs-lookup"><span data-stu-id="70362-116">In the following code example, the path set for the location of the icon is the **My Documents** folder.</span></span> <span data-ttu-id="70362-117">Dieser Speicherort wird verwendet, da Sie davon ausgehen können, dass die meisten Computer unter dem Windows-Betriebssystem diesen Ordner enthalten.</span><span class="sxs-lookup"><span data-stu-id="70362-117">This location is used because you can assume that most computers running the Windows operating system will include this folder.</span></span> <span data-ttu-id="70362-118">Wenn Sie diesen Speicherort auswählen, können Benutzer mit minimalen System Zugriffsebenen die Anwendung sicher ausführen.</span><span class="sxs-lookup"><span data-stu-id="70362-118">Choosing this location also enables users with minimal system access levels to safely run the application.</span></span> <span data-ttu-id="70362-119">Das folgende Beispiel erfordert ein Formular mit einem <xref:System.Windows.Forms.NotifyIcon> bereits hinzugefügten-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="70362-119">The following example requires a form with a <xref:System.Windows.Forms.NotifyIcon> control already added.</span></span> <span data-ttu-id="70362-120">Außerdem ist eine Symbol Datei mit dem Namen erforderlich `Icon.ico` .</span><span class="sxs-lookup"><span data-stu-id="70362-120">It also requires an icon file named `Icon.ico`.</span></span>

    ```vb
    ' You should replace the bold icon in the sample below
    ' with an icon of your own choosing.
    NotifyIcon1.Icon = New _
       System.Drawing.Icon(System.Environment.GetFolderPath _
       (System.Environment.SpecialFolder.Personal) _
       & "\Icon.ico")
    NotifyIcon1.Visible = True
    NotifyIcon1.Text = "Antivirus program"
    ```

    ```csharp
    // You should replace the bold icon in the sample below
    // with an icon of your own choosing.
    // Note the escape character used (@) when specifying the path.
    notifyIcon1.Icon =
       new System.Drawing.Icon (System.Environment.GetFolderPath
       (System.Environment.SpecialFolder.Personal)
       + @"\Icon.ico");
    notifyIcon1.Visible = true;
    notifyIcon1.Text = "Antivirus program";
    ```

    ```cpp
    // You should replace the bold icon in the sample below
    // with an icon of your own choosing.
    notifyIcon1->Icon = gcnew
       System::Drawing::Icon(String::Concat
       (System::Environment::GetFolderPath
       (System::Environment::SpecialFolder::Personal),
       "\\Icon.ico"));
    notifyIcon1->Visible = true;
    notifyIcon1->Text = "Antivirus program";
    ```

## <a name="see-also"></a><span data-ttu-id="70362-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70362-121">See also</span></span>

- <xref:System.Windows.Forms.NotifyIcon>
- <xref:System.Windows.Forms.NotifyIcon.Icon%2A>
- [<span data-ttu-id="70362-122">Vorgehensweise: Zuordnen eines Kontextmenüs zu einer NotifyIcon-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="70362-122">How to: Associate a Shortcut Menu with a Windows Forms NotifyIcon Component</span></span>](how-to-associate-a-shortcut-menu-with-a-windows-forms-notifyicon-component.md)
- [<span data-ttu-id="70362-123">NotifyIcon-Komponente</span><span class="sxs-lookup"><span data-stu-id="70362-123">NotifyIcon Component</span></span>](notifyicon-component-windows-forms.md)
- [<span data-ttu-id="70362-124">Übersicht über die NotifyIcon-Komponente</span><span class="sxs-lookup"><span data-stu-id="70362-124">NotifyIcon Component Overview</span></span>](notifyicon-component-overview-windows-forms.md)
