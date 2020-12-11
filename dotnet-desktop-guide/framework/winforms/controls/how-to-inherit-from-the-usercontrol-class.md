---
title: 'Vorgehensweise: Erben von der UserControl-Klasse'
ms.date: 03/30/2017
helpviewer_keywords:
- inheritance [Windows Forms], Windows Forms custom controls
- UserControl class [Windows Forms], inheriting from
- user controls [Windows Forms], creating
- composite controls [Windows Forms], creating
ms.assetid: 67713625-e2e4-4f6a-bce7-0855ee5043d9
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 5c278cfadd1bb0c9720718c08791a37f90d964d7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976617"
---
# <a name="how-to-inherit-from-the-usercontrol-class"></a><span data-ttu-id="31a7d-102">Vorgehensweise: Erben von der UserControl-Klasse</span><span class="sxs-lookup"><span data-stu-id="31a7d-102">How to: Inherit from the UserControl Class</span></span>

<span data-ttu-id="31a7d-103">Sie können ein *Benutzersteuerelement* erstellen, um die Funktionalität einer oder mehrerer Windows Forms-Steuerelemente mit benutzerdefiniertem Code zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="31a7d-103">To combine the functionality of one or more Windows Forms controls with custom code, you can create a *user control*.</span></span> <span data-ttu-id="31a7d-104">Benutzersteuerelemente kombinieren die schnelle Entwicklung von Steuerelementen, die standardmäßige Funktionalität von Windows Forms-Steuerelementen und die Vielseitigkeit von benutzerdefinierten Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="31a7d-104">User controls combine rapid control development, standard Windows Forms control functionality, and the versatility of custom properties and methods.</span></span> <span data-ttu-id="31a7d-105">Wenn Sie mit dem Erstellen eines Benutzersteuerelements beginnen, wird ein Designer angezeigt, auf dem Sie die standardmäßigen Windows Forms-Steuerelemente platzieren können.</span><span class="sxs-lookup"><span data-stu-id="31a7d-105">When you begin creating a user control, you are presented with a visible designer, upon which you can place standard Windows Forms controls.</span></span> <span data-ttu-id="31a7d-106">Diese Steuerelemente behalten ihre implementierte Funktionalität sowie das Aussehen und Verhalten der Standardsteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="31a7d-106">These controls retain all of their inherent functionality, as well as the appearance and behavior (look and feel) of standard controls.</span></span> <span data-ttu-id="31a7d-107">Sobald diese Steuerelemente in das Benutzersteuerelement integriert sind, stehen sie jedoch nicht mehr über Code zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="31a7d-107">Once these controls are built into the user control, however, they are no longer available to you through code.</span></span> <span data-ttu-id="31a7d-108">Das Benutzersteuerelement führt seine eigene Grafikausgabe aus und behandelt auch die gesamte grundlegende Funktionalität von Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="31a7d-108">The user control does its own painting and also handles all of the basic functionality associated with controls.</span></span>

## <a name="to-create-a-user-control"></a><span data-ttu-id="31a7d-109">So erstellen Sie ein benutzerdefiniertes Steuerelement</span><span class="sxs-lookup"><span data-stu-id="31a7d-109">To create a user control</span></span>

1. <span data-ttu-id="31a7d-110">Erstellen Sie in Visual Studio ein neues **Windows-Steuerelement Bibliothek** -Projekt.</span><span class="sxs-lookup"><span data-stu-id="31a7d-110">Create a new **Windows Control Library** project in Visual Studio.</span></span>

   <span data-ttu-id="31a7d-111">Ein neues Projekt mit einem leeren Benutzersteuerelement wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="31a7d-111">A new project is created with a blank user control.</span></span>

2. <span data-ttu-id="31a7d-112">Ziehen Sie Steuerelemente von der Registerkarte **Windows Forms** der **Toolbox** auf den Designer.</span><span class="sxs-lookup"><span data-stu-id="31a7d-112">Drag controls from the **Windows Forms** tab of the **Toolbox** onto your designer.</span></span>

3. <span data-ttu-id="31a7d-113">Diese Steuerelemente sollten so positioniert und entworfen werden, wie Sie im fertig gestellten Steuerelement angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31a7d-113">These controls should be positioned and designed as you want them to appear in the final user control.</span></span> <span data-ttu-id="31a7d-114">Wenn Sie möchten, dass Entwickler auf die konstituierenden Steuerelemente zugreifen können, müssen Sie diese als öffentlich deklarieren oder Eigenschaften des konstituierenden Steuerelements einzeln verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="31a7d-114">If you want to allow developers to access the constituent controls, you must declare them as public, or selectively expose properties of the constituent control.</span></span> <span data-ttu-id="31a7d-115">Einzelheiten finden Sie unter [Vorgehensweise: Verfügbarmachen der Eigenschaften konstituierender Steuerelemente](how-to-expose-properties-of-constituent-controls.md).</span><span class="sxs-lookup"><span data-stu-id="31a7d-115">For details, see [How to: Expose Properties of Constituent Controls](how-to-expose-properties-of-constituent-controls.md).</span></span>

4. <span data-ttu-id="31a7d-116">Implementieren Sie alle benutzerdefinierten Methoden oder Eigenschaften, die in das Steuerelement eingebunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31a7d-116">Implement any custom methods or properties that your control will incorporate.</span></span>

5. <span data-ttu-id="31a7d-117">Drücken Sie **F5** , um das Projekt zu erstellen, und führen Sie das Steuerelement im **UserControl-Test Container** aus.</span><span class="sxs-lookup"><span data-stu-id="31a7d-117">Press **F5** to build the project and run your control in the **UserControl Test Container**.</span></span> <span data-ttu-id="31a7d-118">Weitere Informationen finden Sie unter Gewusst [wie: Testen des Run-Time Verhaltens eines UserControl-Steuer](how-to-test-the-run-time-behavior-of-a-usercontrol.md)Elements.</span><span class="sxs-lookup"><span data-stu-id="31a7d-118">For more information, see [How to: Test the Run-Time Behavior of a UserControl](how-to-test-the-run-time-behavior-of-a-usercontrol.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="31a7d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31a7d-119">See also</span></span>

- [<span data-ttu-id="31a7d-120">Arten von benutzerdefinierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="31a7d-120">Varieties of Custom Controls</span></span>](varieties-of-custom-controls.md)
- [<span data-ttu-id="31a7d-121">Vorgehensweise: Erben von der Control-Klasse</span><span class="sxs-lookup"><span data-stu-id="31a7d-121">How to: Inherit from the Control Class</span></span>](how-to-inherit-from-the-control-class.md)
- [<span data-ttu-id="31a7d-122">Vorgehensweise: Erben von vorhandenen Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="31a7d-122">How to: Inherit from Existing Windows Forms Controls</span></span>](how-to-inherit-from-existing-windows-forms-controls.md)
- [<span data-ttu-id="31a7d-123">Vorgehensweise: Erstellen von Steuerelementen für Windows Forms</span><span class="sxs-lookup"><span data-stu-id="31a7d-123">How to: Author Controls for Windows Forms</span></span>](how-to-author-controls-for-windows-forms.md)
- [<span data-ttu-id="31a7d-124">Problembehandlung bei vererbten Ereignis Handlern in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="31a7d-124">Troubleshoot Inherited Event Handlers in Visual Basic</span></span>](/dotnet/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers)
- [<span data-ttu-id="31a7d-125">Vorgehensweise: Testen des Laufzeitverhaltens eines UserControl</span><span class="sxs-lookup"><span data-stu-id="31a7d-125">How to: Test the Run-Time Behavior of a UserControl</span></span>](how-to-test-the-run-time-behavior-of-a-usercontrol.md)
