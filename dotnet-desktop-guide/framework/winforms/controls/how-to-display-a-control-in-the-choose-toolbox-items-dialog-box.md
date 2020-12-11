---
title: 'Gewusst wie: Anzeigen eines Steuerelements im Dialogfeld "Toolboxelemente auswählen"'
ms.date: 08/23/2019
helpviewer_keywords:
- global assembly cache [Windows Forms], Choose Toolbox Items dialog box
- AssemblyFoldersEx [Windows Forms], Choose Toolbox Items dialog box
- controls [Windows Forms], display in Choose Toolbox Items dialog box
- assembly folder registration [Windows Forms], Choose Toolbox Items dialog box
- Choose Toolbox Items dialog box [Windows Forms], display control
ms.assetid: 01ef6eba-d044-40f0-951d-78eff7ebd9a9
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: b105c45e0d55417066c7f8658f0cb23a12c7f768
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975661"
---
# <a name="how-to-display-a-control-in-the-choose-toolbox-items-dialog-box"></a><span data-ttu-id="ee68d-102">Gewusst wie: Anzeigen eines Steuerelements im Dialogfeld "Toolboxelemente auswählen"</span><span class="sxs-lookup"><span data-stu-id="ee68d-102">How to: Display a Control in the Choose Toolbox Items Dialog Box</span></span>

<span data-ttu-id="ee68d-103">Wenn Sie Steuerelemente entwickeln und verteilen, möchten Sie möglicherweise, dass diese Steuerelemente im Dialogfeld **Toolbox Elemente auswählen** von Visual Studio angezeigt werden, das angezeigt wird, wenn Sie mit der rechten Maustaste auf die **Toolbox** klicken und **Elemente auswählen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="ee68d-103">As you develop and distribute controls, you may want those controls to appear in the **Choose Toolbox Items** dialog box of Visual Studio, which is displayed when you right-click the **Toolbox** and select **Choose Items**.</span></span> <span data-ttu-id="ee68d-104">Sie können das Steuerelement in diesem Dialogfeld mithilfe der AssemblyFoldersEx-Registrierungs Prozedur anzeigen lassen.</span><span class="sxs-lookup"><span data-stu-id="ee68d-104">You can enable your control to appear in this dialog box by using the AssemblyFoldersEx registration procedure.</span></span>

<span data-ttu-id="ee68d-105">So zeigen Sie das Steuerelement im Dialogfeld Toolbox Elemente auswählen an:</span><span class="sxs-lookup"><span data-stu-id="ee68d-105">To display your control in the Choose Toolbox Items dialog box:</span></span>

- <span data-ttu-id="ee68d-106">Installieren Sie die steuerungsassembly im globalen Assemblycache.</span><span class="sxs-lookup"><span data-stu-id="ee68d-106">Install your control assembly to the global assembly cache.</span></span> <span data-ttu-id="ee68d-107">Weitere Informationen finden Sie unter Gewusst [wie: Installieren einer Assembly in den globalen Assemblycache](/dotnet/framework/app-domains/install-assembly-into-gac).</span><span class="sxs-lookup"><span data-stu-id="ee68d-107">For more information, see [How to: Install an Assembly into the Global Assembly Cache](/dotnet/framework/app-domains/install-assembly-into-gac).</span></span>

  <span data-ttu-id="ee68d-108">Oder</span><span class="sxs-lookup"><span data-stu-id="ee68d-108">-or-</span></span>

- <span data-ttu-id="ee68d-109">Registrieren Sie das Steuerelement und die zugehörigen Entwurfszeit-Assemblys mithilfe der AssemblyFoldersEx-Registrierungs Prozedur.</span><span class="sxs-lookup"><span data-stu-id="ee68d-109">Register your control and its associated design-time assemblies by using the AssemblyFoldersEx registration procedure.</span></span> <span data-ttu-id="ee68d-110">AssemblyFoldersEx ist ein Registrierungs Speicherort, an dem Drittanbieter Pfade für jede Version des Frameworks speichern, das Sie unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ee68d-110">AssemblyFoldersEx is a registry location where third-party vendors store paths for each version of the framework that they support.</span></span> <span data-ttu-id="ee68d-111">Die Entwurfszeit Auflösung kann in diesem Registrierungs Speicherort nach Verweisassemblys suchen.</span><span class="sxs-lookup"><span data-stu-id="ee68d-111">Design-time resolution can look in this registry location to find reference assemblies.</span></span> <span data-ttu-id="ee68d-112">Das Registrierungs Skript kann die Steuerelemente angeben, die in der Toolbox angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ee68d-112">The registry script can specify the controls you want to appear in the Toolbox.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee68d-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee68d-113">See also</span></span>

- [<span data-ttu-id="ee68d-114">Entwickeln von Windows Forms-Steuerelementen zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="ee68d-114">Developing Windows Forms Controls at Design Time</span></span>](developing-windows-forms-controls-at-design-time.md)
- [<span data-ttu-id="ee68d-115">How to: Installieren einer Assembly im globalen Assemblycache</span><span class="sxs-lookup"><span data-stu-id="ee68d-115">How to: Install an Assembly into the Global Assembly Cache</span></span>](/dotnet/framework/app-domains/install-assembly-into-gac)
- [<span data-ttu-id="ee68d-116">Exemplarische Vorgehensweise: Automatisches Füllen der Toolbox mit benutzerdefinierten Komponenten</span><span class="sxs-lookup"><span data-stu-id="ee68d-116">Walkthrough: Automatically Populating the Toolbox with Custom Components</span></span>](walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
