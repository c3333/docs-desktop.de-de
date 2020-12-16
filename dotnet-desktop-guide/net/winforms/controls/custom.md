---
title: Arten von benutzerdefinierten Steuerelementen
description: In diesem Artikel erhalten Sie Informationen zu den verschiedenen Typen benutzerdefinierter Steuerelemente, die Sie in Windows Forms für .NET erstellen können.
ms.date: 10/26/2020
ms.topic: overview
f1_keywords:
- UserControl
helpviewer_keywords:
- controls [Windows Forms], user controls
- controls [Windows Forms], types of
- composite controls [Windows Forms]
- extended controls [Windows Forms]
- controls [Windows Forms], extended
- user controls [Windows Forms]
- custom controls [Windows Forms]
- controls [Windows Forms], composite
ms.openlocfilehash: 25430adf6efbb4c1f323496ce46cdea5aa0bb95c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942086"
---
# <a name="types-of-custom-controls-windows-forms-net"></a><span data-ttu-id="7c703-103">Arten von benutzerdefinierten Steuerelementen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="7c703-103">Types of custom controls (Windows Forms .NET)</span></span>

<span data-ttu-id="7c703-104">Mit Windows Forms können Sie neue Steuerelemente entwickeln und implementieren.</span><span class="sxs-lookup"><span data-stu-id="7c703-104">With Windows Forms, you can develop and implement new controls.</span></span> <span data-ttu-id="7c703-105">Sie können ein neues Benutzersteuerelement erstellen, vorhandene Steuerelemente über Vererbung ändern und ein benutzerdefiniertes Steuerelement schreiben, das sich selbst zeichnet.</span><span class="sxs-lookup"><span data-stu-id="7c703-105">You can create a new user control, modify existing controls through inheritance, and write a custom control that does its own painting.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

<span data-ttu-id="7c703-106">Es kann verwirrend sein, eine Entscheidung zu treffen, welche Art von Steuerelement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c703-106">Deciding which kind of control to create can be confusing.</span></span> <span data-ttu-id="7c703-107">Dieser Artikel behandelt die Unterschiede zwischen verschiedenen Arten von Steuerelementen, von denen geerbt werden kann, und bietet Informationen über die Auswahl einer bestimmten Art von Steuerelement für Ihr Projekt.</span><span class="sxs-lookup"><span data-stu-id="7c703-107">This article highlights the differences among the various kinds of controls from which you can inherit, and provides you with information about how to choose a particular type of control for your project.</span></span>

<table>
<thead>
  <tr>
    <th><span data-ttu-id="7c703-108">Szenario</span><span class="sxs-lookup"><span data-stu-id="7c703-108">If ...</span></span></th>
    <th><span data-ttu-id="7c703-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="7c703-109">Create a ...</span></span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>
        <ul>
            <li><span data-ttu-id="7c703-110">Sie möchten die Funktionalität mehrerer Windows Forms-Steuerelemente in einer einzigen wiederverwendbaren Einheit kombinieren.</span><span class="sxs-lookup"><span data-stu-id="7c703-110">You want to combine the functionality of several Windows Forms controls into a single reusable unit.</span></span></li>
        </ul>
    </td>
    <td><span data-ttu-id="7c703-111">Erstellen Sie ein <a href="#composite-controls">zusammengesetztes Steuerelement</a> durch Vererbung von <a href="/dotnet/api/system.windows.forms.usercontrol">System.Windows.Forms.UserControl</a>.</span><span class="sxs-lookup"><span data-stu-id="7c703-111"><a href="#composite-controls">Composite control</a> by inheriting from <a href="/dotnet/api/system.windows.forms.usercontrol">System.Windows.Forms.UserControl</a>.</span></span></td>
  </tr>
  <tr>
    <td>
        <ul>
            <li><span data-ttu-id="7c703-112">Ein Großteil der Funktionalität, die Sie benötigen, mit ist der Funktionalität eines vorhandenen Windows Forms-Steuerelements identisch.</span><span class="sxs-lookup"><span data-stu-id="7c703-112">Most of the functionality you need is already identical to an existing Windows Forms control.</span></span></li>
            <li><span data-ttu-id="7c703-113">Sie benötigen keine benutzerdefinierte grafische Benutzeroberfläche, oder Sie möchten eine neue grafische Benutzeroberfläche für ein vorhandenes Steuerelement entwerfen.</span><span class="sxs-lookup"><span data-stu-id="7c703-113">You don't need a custom graphical user interface, or you want to design a new graphical user interface for an existing control.</span></span></li>
        </ul>
    </td>
    <td><span data-ttu-id="7c703-114">Erstellen Sie ein <a href="#extended-controls">erweitertes Steuerelement</a> durch Vererbung von einem bestimmten Windows Forms-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="7c703-114"><a href="#extended-controls">Extended control</a> by inheriting from a specific Windows Forms control.</span></span></td>
  </tr>
  <tr>
    <td>
        <ul>
            <li><span data-ttu-id="7c703-115">Sie möchten eine benutzerdefinierte grafische Darstellung Ihres Steuerelements bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7c703-115">You want to provide a custom graphical representation of your control.</span></span></li>
            <li><span data-ttu-id="7c703-116">Sie müssen benutzerdefinierte Funktionalität implementieren, die über Standardsteuerelemente nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7c703-116">You need to implement custom functionality that isn't available through standard controls.</span></span></li>
        </ul>
    </td>
    <td><span data-ttu-id="7c703-117">Erstellen Sie ein <a href="#custom-controls">benutzerdefiniertes Steuerelement</a> durch Vererbung von <a href="/dotnet/api/system.windows.forms.control">System.Windows.Forms.Control</a>.</span><span class="sxs-lookup"><span data-stu-id="7c703-117"><a href="#custom-controls">Custom control</a> by inheriting from <a href="/dotnet/api/system.windows.forms.control">System.Windows.Forms.Control</a>.</span></span></td>
  </tr>
</tbody>
</table>

## <a name="base-control-class"></a><span data-ttu-id="7c703-118">Control-Basisklasse</span><span class="sxs-lookup"><span data-stu-id="7c703-118">Base Control Class</span></span>

<span data-ttu-id="7c703-119">Die <xref:System.Windows.Forms.Control>-Klasse ist die Basisklasse für Windows Forms-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="7c703-119">The <xref:System.Windows.Forms.Control> class is the base class for Windows Forms controls.</span></span> <span data-ttu-id="7c703-120">Sie bietet die Infrastruktur, die für die grafische Darstellung in Windows Forms-Anwendungen benötigt wird, und die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="7c703-120">It provides the infrastructure required for visual display in Windows Forms applications and provides the following capabilities:</span></span>

- <span data-ttu-id="7c703-121">Macht ein Fensterhandle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7c703-121">Exposes a window handle.</span></span>
- <span data-ttu-id="7c703-122">Verwaltet Meldungsrouting.</span><span class="sxs-lookup"><span data-stu-id="7c703-122">Manages message routing.</span></span>
- <span data-ttu-id="7c703-123">Bietet Maus- und Tastaturereignisse und viele weitere Ereignisse der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="7c703-123">Provides mouse and keyboard events, and many other user interface events.</span></span>
- <span data-ttu-id="7c703-124">Bietet erweiterte Layoutfunktionen.</span><span class="sxs-lookup"><span data-stu-id="7c703-124">Provides advanced layout features.</span></span>
- <span data-ttu-id="7c703-125">Die Klasse enthält viele für die grafische Darstellung spezifischen Eigenschaften wie <xref:System.Windows.Forms.Control.ForeColor%2A>, <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.Height%2A> und <xref:System.Windows.Forms.Control.Width%2A>.</span><span class="sxs-lookup"><span data-stu-id="7c703-125">Contains many properties specific to visual display, such as <xref:System.Windows.Forms.Control.ForeColor%2A>, <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.Height%2A>, and <xref:System.Windows.Forms.Control.Width%2A>.</span></span>
- <span data-ttu-id="7c703-126">Bietet die notwendige Unterstützung für Sicherheit und Threading für ein Windows Forms-Steuerelement, um als Microsoft® ActiveX®-Steuerelement zu fungieren.</span><span class="sxs-lookup"><span data-stu-id="7c703-126">Provides the security and threading support necessary for a Windows Forms control to act as a Microsoft® ActiveX® control.</span></span>

<span data-ttu-id="7c703-127">Da der Großteil der Infrastruktur von der Basisklasse bereitgestellt wird, ist es relativ einfach, Ihre eigenen Windows Forms-Steuerelemente zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="7c703-127">Because so much of the infrastructure is provided by the base class, it's relatively easy to develop your own Windows Forms controls.</span></span>

## <a name="composite-controls"></a><span data-ttu-id="7c703-128">Zusammengesetzte Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7c703-128">Composite Controls</span></span>

<span data-ttu-id="7c703-129">Ein zusammengesetztes Steuerelement ist eine Sammlung von Windows Forms-Steuerelementen, die in einem gemeinsamen Container gekapselt sind.</span><span class="sxs-lookup"><span data-stu-id="7c703-129">A composite control is a collection of Windows Forms controls encapsulated in a common container.</span></span> <span data-ttu-id="7c703-130">Diese Art von Steuerelement wird manchmal auch als *Benutzersteuerelement* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7c703-130">This kind of control is sometimes called a *user control*.</span></span> <span data-ttu-id="7c703-131">Die enthaltenen Steuerelemente werden *konstituierende Steuerelemente* genannt.</span><span class="sxs-lookup"><span data-stu-id="7c703-131">The contained controls are called *constituent controls*.</span></span>

<span data-ttu-id="7c703-132">Ein zusammengesetztes Steuerelement enthält die gesamte Funktionalität, die in jedem der enthaltenen Windows Forms-Steuerelemente implementiert ist, und ermöglicht es Ihnen, deren Eigenschaften selektiv verfügbar zu machen und zu binden.</span><span class="sxs-lookup"><span data-stu-id="7c703-132">A composite control holds all of the inherent functionality associated with each of the contained Windows Forms controls and enables you to selectively expose and bind their properties.</span></span> <span data-ttu-id="7c703-133">Ein zusammengesetztes Steuerelement bietet auch hohe Funktionalität für die standardmäßige Tastaturbehandlung, sodass Sie keinen zusätzlichen Entwicklungsaufwand betreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="7c703-133">A composite control also provides a great deal of default keyboard handling functionality with no extra development effort on your part.</span></span>

<span data-ttu-id="7c703-134">Ein zusammengesetztes Steuerelement kann z.B. erstellt werden, um die Adressdaten von Kunden aus einer Datenbank anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7c703-134">For example, a composite control could be built to display customer address data from a database.</span></span> <span data-ttu-id="7c703-135">Dieses Steuerelement würde ein <xref:System.Windows.Forms.DataGridView>-Steuerelement beinhalten, um die Datenbankfelder anzuzeigen, eine <xref:System.Windows.Forms.BindingSource>-Klasse zur Verarbeitung der Bindung an eine Datenquelle und ein <xref:System.Windows.Forms.BindingNavigator>-Steuerelement zur Navigation in den Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="7c703-135">This control would include a <xref:System.Windows.Forms.DataGridView> control to display the database fields, a <xref:System.Windows.Forms.BindingSource> to handle binding to a data source, and a <xref:System.Windows.Forms.BindingNavigator> control to move through the records.</span></span> <span data-ttu-id="7c703-136">Sie können Datenbindungseigenschaften selektiv verfügbar machen und das gesamte Steuerelement verpacken und von Anwendung zu Anwendung wiederverwenden.</span><span class="sxs-lookup"><span data-stu-id="7c703-136">You could selectively expose data binding properties, and you could package and reuse the entire control from application to application.</span></span><!-- TODO For an example of this kind of composite control, see [How to: Apply Attributes in Windows Forms Controls](how-to-apply-attributes-in-windows-forms-controls.md).-->

<span data-ttu-id="7c703-137">Leiten Sie von der Klasse <xref:System.Windows.Forms.UserControl> ab, um ein zusammengesetztes Steuerelement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7c703-137">To author a composite control, derive from the <xref:System.Windows.Forms.UserControl> class.</span></span> <span data-ttu-id="7c703-138">Die Basisklasse <xref:System.Windows.Forms.UserControl> ermöglicht Tastaturrouting für die untergeordneten Steuerelemente und stellt damit sicher, dass untergeordnete Steuerelemente als Gruppe arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="7c703-138">The <xref:System.Windows.Forms.UserControl> base class provides keyboard routing for child controls and enables child controls to work as a group.</span></span><!-- TODO For more information, see [Developing a Composite Windows Forms Control](developing-a-composite-windows-forms-control.md).-->

## <a name="extended-controls"></a><span data-ttu-id="7c703-139">Erweiterte Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7c703-139">Extended Controls</span></span>

<span data-ttu-id="7c703-140">Sie können ein geerbtes Steuerelement aus jedem vorhandenen Windows Forms-Steuerelement ableiten.</span><span class="sxs-lookup"><span data-stu-id="7c703-140">You can derive an inherited control from any existing Windows Forms control.</span></span> <span data-ttu-id="7c703-141">Diese Vorgehensweise ermöglicht es Ihnen, die in einem Windows Forms-Steuerelement implementierte Funktionalität zu übernehmen und diese Funktionalität dann durch Hinzufügen von benutzerdefinierten Eigenschaften, Methoden oder weiteren Features zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="7c703-141">With this approach, you can keep all of the inherent functionality of a Windows Forms control, and then extend that functionality by adding custom properties, methods, or other features.</span></span> <span data-ttu-id="7c703-142">Mit dieser Option können Sie die Farblogik des Basissteuerelements außer Kraft setzen und anschließend die Benutzeroberfläche durch Verändern des Aussehens erweitern.</span><span class="sxs-lookup"><span data-stu-id="7c703-142">With this option, you can override the base control's paint logic, and then extend its user interface by changing its appearance.</span></span>

<span data-ttu-id="7c703-143">Sie können z. B. ein von <xref:System.Windows.Forms.Button> abgeleitetes Steuerelement erstellen, das nachverfolgt, wie oft ein Benutzer darauf geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="7c703-143">For example, you can create a control derived from the <xref:System.Windows.Forms.Button> control that tracks how many times a user has clicked it.</span></span>

<span data-ttu-id="7c703-144">Bei einigen Steuerelementen können Sie auch eine benutzerdefinierte Darstellung der grafischen Benutzeroberfläche des Steuerelements hinzufügen, indem Sie die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode der Basisklasse überschreiben.</span><span class="sxs-lookup"><span data-stu-id="7c703-144">In some controls, you can also add a custom appearance to the graphical user interface of your control by overriding the <xref:System.Windows.Forms.Control.OnPaint%2A> method of the base class.</span></span> <span data-ttu-id="7c703-145">Für eine erweiterte Schaltfläche, die die Klicks nachverfolgt, können Sie die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode überschreiben, um die Basisimplementierung von <xref:System.Windows.Forms.Control.OnPaint%2A> aufzurufen, und dann den Klickzähler in einer Ecke des Clientbereichs des <xref:System.Windows.Forms.Button>-Steuerelements zeichnen.</span><span class="sxs-lookup"><span data-stu-id="7c703-145">For an extended button that tracks clicks, you can override the <xref:System.Windows.Forms.Control.OnPaint%2A> method to call the base implementation of <xref:System.Windows.Forms.Control.OnPaint%2A>, and then draw the click count in one corner of the <xref:System.Windows.Forms.Button> control's client area.</span></span>

## <a name="custom-controls"></a><span data-ttu-id="7c703-146">Benutzerdefinierte Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7c703-146">Custom Controls</span></span>

<span data-ttu-id="7c703-147">Eine weitere Möglichkeit zum Erstellen eines Steuerelements besteht darin, ein Steuerelement von Grund auf neu zu erstellen, indem es von <xref:System.Windows.Forms.Control> erbt.</span><span class="sxs-lookup"><span data-stu-id="7c703-147">Another way to create a control is to create one substantially from the beginning by inheriting from <xref:System.Windows.Forms.Control>.</span></span> <span data-ttu-id="7c703-148">Die Klasse <xref:System.Windows.Forms.Control> stellt die gesamte grundlegende Funktionalität bereit, die für Steuerelemente erforderlich ist, darunter Maus- und Tastaturbehandlungsereignisse, sie stellt aber weder für Steuerelemente spezifische Funktionalität noch eine grafische Oberfläche bereit.</span><span class="sxs-lookup"><span data-stu-id="7c703-148">The <xref:System.Windows.Forms.Control> class provides all of the basic functionality required by controls, including mouse and keyboard handling events, but no control-specific functionality or graphical interface.</span></span>

<span data-ttu-id="7c703-149">Das Erstellen eines Steuerelement durch Erben von der <xref:System.Windows.Forms.Control>-Klasse erfordert viel mehr Überlegungen und Aufwand als ein Erben von <xref:System.Windows.Forms.UserControl> oder von einem vorhandenen Windows Forms-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="7c703-149">Creating a control by inheriting from the <xref:System.Windows.Forms.Control> class requires much more thought and effort than inheriting from <xref:System.Windows.Forms.UserControl> or an existing Windows Forms control.</span></span> <span data-ttu-id="7c703-150">Da ein Großteil der Implementierung Ihnen überlassen ist, hat Ihr Steuerelement größere Flexibilität als ein zusammengesetztes oder erweitertes Steuerelement, und Sie können Ihr Steuerelement exakt an Ihre Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="7c703-150">Because a great deal of implementation is left for you, your control can have greater flexibility than a composite or extended control, and you can tailor your control to suit your exact needs.</span></span>

<span data-ttu-id="7c703-151">Sie müssen Code für das <xref:System.Windows.Forms.Control.OnPaint%2A>-Ereignis des Steuerelements sowie featurespezifischen Code schreiben, um ein benutzerdefiniertes Steuerelement zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="7c703-151">To implement a custom control, you must write code for the <xref:System.Windows.Forms.Control.OnPaint%2A> event of the control, as well as any feature-specific code you need.</span></span> <span data-ttu-id="7c703-152">Sie können auch die <xref:System.Windows.Forms.Control.WndProc%2A>-Methode überschreiben und Windows-Meldungen direkt verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7c703-152">You can also override the <xref:System.Windows.Forms.Control.WndProc%2A> method and handle windows messages directly.</span></span> <span data-ttu-id="7c703-153">Dies ist die beste Möglichkeit, ein Steuerelement zu erstellen. Sie müssen allerdings mit der Microsoft Win32-API vertraut sein, um diese Technik effektiv einsetzen zu können.</span><span class="sxs-lookup"><span data-stu-id="7c703-153">This is the most powerful way to create a control, but to use this technique effectively, you need to be familiar with the Microsoft Win32® API.</span></span>

<span data-ttu-id="7c703-154">Ein Beispiel für ein benutzerdefiniertes Steuerelement ist ein Uhren-Steuerelement, das das Erscheinungsbild und das Verhalten einer analogen Uhr dupliziert.</span><span class="sxs-lookup"><span data-stu-id="7c703-154">An example of a custom control is a clock control that duplicates the appearance and behavior of an analog clock.</span></span> <span data-ttu-id="7c703-155">Benutzerdefiniertes Zeichnen wird aufgerufen, um die Zeiger der Uhr als Reaktion auf <xref:System.Windows.Forms.Timer.Tick>-Ereignisse zu bewegen, die aus einer internen <xref:System.Windows.Forms.Timer>-Komponente stammen.</span><span class="sxs-lookup"><span data-stu-id="7c703-155">Custom painting is invoked to cause the hands of the clock to move in response to <xref:System.Windows.Forms.Timer.Tick> events from an internal <xref:System.Windows.Forms.Timer> component.</span></span><!-- TODO For more information, see [How to: Develop a Simple Windows Forms Control](how-to-develop-a-simple-windows-forms-control.md).-->

## <a name="activex-controls"></a><span data-ttu-id="7c703-156">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7c703-156">ActiveX Controls</span></span>

<span data-ttu-id="7c703-157">Obwohl die Windows Forms-Infrastruktur zum Hosten von Windows Forms-Steuerelementen optimiert wurde, können Sie weiterhin ActiveX-Steuerelemente verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c703-157">Although the Windows Forms infrastructure has been optimized to host Windows Forms controls, you can still use ActiveX controls.</span></span> <span data-ttu-id="7c703-158">Visual Studio bietet Unterstützung für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="7c703-158">There's support for this task in Visual Studio.</span></span><!-- TODO For more information, see [How to: Add ActiveX Controls to Windows Forms](how-to-add-activex-controls-to-windows-forms.md).-->

## <a name="windowless-controls"></a><span data-ttu-id="7c703-159">Fensterlose Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7c703-159">Windowless Controls</span></span>

<span data-ttu-id="7c703-160">Die Microsoft Visual Basic® 6.0- und ActiveX-Technologien unterstützen *fensterlose* Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="7c703-160">The Microsoft Visual Basic® 6.0 and ActiveX technologies support *windowless* controls.</span></span> <span data-ttu-id="7c703-161">Fensterlose Steuerelemente werden in Windows Forms nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c703-161">Windowless controls aren't supported in Windows Forms.</span></span>

## <a name="custom-design-experience"></a><span data-ttu-id="7c703-162">Benutzerdefiniertes Entwurfserlebnis</span><span class="sxs-lookup"><span data-stu-id="7c703-162">Custom Design Experience</span></span>

<span data-ttu-id="7c703-163">Wenn Sie eine benutzerdefinierte Handhabung zur Entwurfszeit implementieren müssen, können Sie Ihren eigenen Designer erstellen.</span><span class="sxs-lookup"><span data-stu-id="7c703-163">If you need to implement a custom design-time experience, you can author your own designer.</span></span> <span data-ttu-id="7c703-164">Leiten Sie für zusammengesetzte Steuerelemente Ihren benutzerdefinierten Designer von der Klasse <xref:System.Windows.Forms.Design.ParentControlDesigner> oder <xref:System.Windows.Forms.Design.DocumentDesigner> ab.</span><span class="sxs-lookup"><span data-stu-id="7c703-164">For composite controls, derive your custom designer class from the <xref:System.Windows.Forms.Design.ParentControlDesigner> or the <xref:System.Windows.Forms.Design.DocumentDesigner> classes.</span></span> <span data-ttu-id="7c703-165">Für erweiterte und benutzerdefinierte Steuerelemente leiten Sie Ihre benutzerdefinierte Designerklasse von der <xref:System.Windows.Forms.Design.ControlDesigner>-Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="7c703-165">For extended and custom controls, derive your custom designer class from the <xref:System.Windows.Forms.Design.ControlDesigner> class.</span></span>

<span data-ttu-id="7c703-166">Verwenden Sie die Klasse <xref:System.ComponentModel.DesignerAttribute>, um Ihr Steuerelement Ihrem Designer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="7c703-166">Use the <xref:System.ComponentModel.DesignerAttribute> to associate your control with your designer.</span></span>

<span data-ttu-id="7c703-167">Die folgenden Informationen sind zwar nicht mehr aktuell, helfen Ihnen möglicherweise jedoch trotzdem.</span><span class="sxs-lookup"><span data-stu-id="7c703-167">The following information is out of date but may help you.</span></span>

- <span data-ttu-id="7c703-168">[Erweitern der Entwurfszeitunterstützung](/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="7c703-168">[(Visual Studio 2013) Extending Design-Time Support](/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120)).</span></span>
- <span data-ttu-id="7c703-169">[Vorgehensweise: Erstellen eines Windows Forms-Steuerelements, das Entwurfszeitfeatures nutzt](/previous-versions/visualstudio/visual-studio-2013/307hck25(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="7c703-169">[(Visual Studio 2013) How to: Create a Windows Forms Control That Takes Advantage of Design-Time Features](/previous-versions/visualstudio/visual-studio-2013/307hck25(v=vs.120)).</span></span>

## <a name="see-also"></a><span data-ttu-id="7c703-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c703-170">See also</span></span>

- [<span data-ttu-id="7c703-171">Übersicht über die Verwendung von Steuerelementen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="7c703-171">Overview of Using Controls (Windows Forms .NET)</span></span>](overview.md)

<!-- TODO: link to the ..\custom-controls\ content 

- [Developing Custom Windows Forms Controls](developing-custom-windows-forms-controls.md)
- [How to: Develop a Simple Windows Forms Control](how-to-develop-a-simple-windows-forms-control.md)
- [Developing a Composite Windows Forms Control](developing-a-composite-windows-forms-control.md)
-->
