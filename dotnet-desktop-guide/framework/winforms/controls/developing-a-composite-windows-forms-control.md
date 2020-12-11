---
title: Entwickeln eines zusammengesetzten Steuer Elements
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], composite controls
- composite controls [Windows Forms]
- composite controls [Windows Forms], Windows Forms
- controls [Windows Forms], composite
ms.assetid: d086f2a3-baa3-4e09-b40c-a5bb3cfc51a6
ms.openlocfilehash: 6887de62857fc260fb53e33f462b07af80658178
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972126"
---
# <a name="develop-a-composite-windows-forms-control"></a><span data-ttu-id="49d8d-102">Entwickeln eines zusammengesetzten Windows Forms-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="49d8d-102">Develop a composite Windows Forms control</span></span>

<span data-ttu-id="49d8d-103">Sie können ein zusammengesetztes Windows Forms-Steuerelement entwickeln, indem Sie andere Windows Forms-Steuerelemente kombinieren.</span><span class="sxs-lookup"><span data-stu-id="49d8d-103">You can develop a composite Windows Forms control by combining other Windows Forms controls.</span></span> <span data-ttu-id="49d8d-104">Zusammengesetzte Steuerelemente, die von abgeleitet <xref:System.Web.UI.UserControl> werden, sind Benutzer Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="49d8d-104">Composite controls that derive from <xref:System.Web.UI.UserControl> are called user controls.</span></span> <span data-ttu-id="49d8d-105">Die Basisklasse, <xref:System.Windows.Forms.UserControl>, ermöglicht Tastaturrouting für die untergeordneten Steuerelemente und stellt damit sicher, dass untergeordnete Steuerelemente den Fokus erhalten können.</span><span class="sxs-lookup"><span data-stu-id="49d8d-105">The base class, <xref:System.Windows.Forms.UserControl>, provides keyboard routing for the child controls, thus ensuring that child controls can receive focus.</span></span> <span data-ttu-id="49d8d-106">Ein Beispiel für ein Benutzer Steuerelement finden Sie im Beispiel <xref:System.Windows.Forms.UserControl> unter Gewusst [wie: Anwenden von Attributen in Windows Forms](how-to-apply-attributes-in-windows-forms-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="49d8d-106">For an example of a user control, see the <xref:System.Windows.Forms.UserControl> sample in [How to: Apply Attributes in Windows Forms Controls](how-to-apply-attributes-in-windows-forms-controls.md).</span></span>

<span data-ttu-id="49d8d-107">Der Windows Forms-Designer in Visual Studio bietet umfangreiche Entwurfszeit Unterstützung für die Erstellung von Benutzer Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="49d8d-107">The Windows Forms designer in Visual Studio provides rich design-time support for authoring user controls.</span></span>

- [<span data-ttu-id="49d8d-108">Gewusst wie: Anzeigen eines Steuerelements im Dialogfeld "Toolboxelemente auswählen"</span><span class="sxs-lookup"><span data-stu-id="49d8d-108">How to: Display a Control in the Choose Toolbox Items Dialog Box</span></span>](how-to-display-a-control-in-the-choose-toolbox-items-dialog-box.md)

- [<span data-ttu-id="49d8d-109">Exemplarische Vorgehensweise: Serialisieren der Auflistungen von Standardtypen mit dem DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="49d8d-109">Walkthrough: Serializing Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>](serializing-collections-designerserializationvisibilityattribute.md)

- [<span data-ttu-id="49d8d-110">Exemplarische Vorgehensweise: Vererben von einem Windows Forms-Steuerelement mit Visual C #</span><span class="sxs-lookup"><span data-stu-id="49d8d-110">Walkthrough: Inheriting from a Windows Forms Control with Visual C#</span></span>](walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)

- [<span data-ttu-id="49d8d-111">Vorgehensweise: Bereitstellen einer Toolboxbitmap für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="49d8d-111">How to: Provide a Toolbox Bitmap for a Control</span></span>](how-to-provide-a-toolbox-bitmap-for-a-control.md)

- [<span data-ttu-id="49d8d-112">Vorgehensweise: Erben von vorhandenen Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="49d8d-112">How to: Inherit from Existing Windows Forms Controls</span></span>](how-to-inherit-from-existing-windows-forms-controls.md)

- [<span data-ttu-id="49d8d-113">Exemplarische Vorgehensweise: Debuggen von benutzerdefinierten Windows Forms-Steuerelementen zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="49d8d-113">Walkthrough: Debugging Custom Windows Forms Controls at Design Time</span></span>](walkthrough-debugging-custom-windows-forms-controls-at-design-time.md)

- [<span data-ttu-id="49d8d-114">Vorgehensweise: Erben von der Control-Klasse</span><span class="sxs-lookup"><span data-stu-id="49d8d-114">How to: Inherit from the Control Class</span></span>](how-to-inherit-from-the-control-class.md)

- [<span data-ttu-id="49d8d-115">Vorgehensweise: Testen des Laufzeitverhaltens eines UserControl</span><span class="sxs-lookup"><span data-stu-id="49d8d-115">How to: Test the Run-Time Behavior of a UserControl</span></span>](how-to-test-the-run-time-behavior-of-a-usercontrol.md)

- [<span data-ttu-id="49d8d-116">Gewusst wie: Ausrichten eines Steuerelements an den Rändern eines Formulars zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="49d8d-116">How to: Align a Control to the Edges of Forms at Design Time</span></span>](how-to-align-a-control-to-the-edges-of-forms-at-design-time.md)

- [<span data-ttu-id="49d8d-117">How to: Erben von der UserControl-Klasse</span><span class="sxs-lookup"><span data-stu-id="49d8d-117">How to: Inherit from the UserControl Class</span></span>](how-to-inherit-from-the-usercontrol-class.md)

- [<span data-ttu-id="49d8d-118">Vorgehensweise: Erstellen von Steuerelementen für Windows Forms</span><span class="sxs-lookup"><span data-stu-id="49d8d-118">How to: Author Controls for Windows Forms</span></span>](how-to-author-controls-for-windows-forms.md)

- [<span data-ttu-id="49d8d-119">Vorgehensweise: Erstellen von zusammengesetzten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="49d8d-119">How to: Author Composite Controls</span></span>](how-to-author-composite-controls.md)

- [<span data-ttu-id="49d8d-120">Exemplarische Vorgehensweise: Erstellen eines zusammengesetzten Steuer Elements mit Visual C #</span><span class="sxs-lookup"><span data-stu-id="49d8d-120">Walkthrough: Authoring a Composite Control with Visual C#</span></span>](walkthrough-authoring-a-composite-control-with-visual-csharp.md)

- [<span data-ttu-id="49d8d-121">Exemplarische Vorgehensweise: Erstellen eines Windows Forms-Steuer Elements, das Visual Studio-Design-Time Features nutzt</span><span class="sxs-lookup"><span data-stu-id="49d8d-121">Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features</span></span>](creating-a-wf-control-design-time-features.md)

- <span data-ttu-id="49d8d-122">[Vorgehensweise: Erstellen eines Windows Forms-Steuerelements, das Entwurfszeitfeatures nutzt](/previous-versions/visualstudio/visual-studio-2013/307hck25(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="49d8d-122">[How to: Create a Windows Forms Control That Takes Advantage of Design-Time Features](/previous-versions/visualstudio/visual-studio-2013/307hck25(v=vs.120))</span></span>

## <a name="see-also"></a><span data-ttu-id="49d8d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49d8d-123">See also</span></span>

- [<span data-ttu-id="49d8d-124">Vorgehensweise: Anwenden von Attributen auf Windows Forms-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="49d8d-124">How to: Apply Attributes in Windows Forms Controls</span></span>](how-to-apply-attributes-in-windows-forms-controls.md)
- [<span data-ttu-id="49d8d-125">Entwickeln benutzerdefinierter Windows Forms-Steuerelemente mit .NET Framework</span><span class="sxs-lookup"><span data-stu-id="49d8d-125">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="49d8d-126">Arten von benutzerdefinierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="49d8d-126">Varieties of Custom Controls</span></span>](varieties-of-custom-controls.md)
