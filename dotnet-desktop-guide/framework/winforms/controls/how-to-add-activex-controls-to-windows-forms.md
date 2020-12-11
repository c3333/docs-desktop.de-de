---
title: ActiveX-Steuerelemente zu Formularen hinzufügen
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, ActiveX controls
- forms [Windows Forms], adding ActiveX controls
- ActiveX controls [Windows Forms], adding
ms.assetid: 54a61e5b-555e-4887-b41e-6244fed271eb
ms.openlocfilehash: ebcaf984e3c64bae2988b5c2d1c94abac79ad36e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975749"
---
# <a name="how-to-add-activex-controls-to-windows-forms"></a><span data-ttu-id="6c6aa-102">Gewusst wie: Hinzufügen von ActiveX-Steuerelementen zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6c6aa-102">How to: Add ActiveX Controls to Windows Forms</span></span>

<span data-ttu-id="6c6aa-103">Während der Windows Forms-Designer in Visual Studio für das Hosten von Windows Forms Steuerelementen optimiert ist, können Sie auch ActiveX-Steuerelemente auf Windows Forms platzieren.</span><span class="sxs-lookup"><span data-stu-id="6c6aa-103">While the Windows Forms Designer in Visual Studio is optimized to host Windows Forms controls, you can also put ActiveX controls on Windows Forms.</span></span>

> [!CAUTION]
> <span data-ttu-id="6c6aa-104">Beim Hinzufügen von ActiveX-Steuerelementen sind Leistungseinschränkungen für Windows Forms vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c6aa-104">There are performance limitations for Windows Forms when ActiveX controls are added to them.</span></span>

<span data-ttu-id="6c6aa-105">Vor dem Hinzufügen von ActiveX-Steuerelementen zum Formular müssen Sie Sie der Toolbox hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c6aa-105">Before you add ActiveX controls to your form, you must add them to the Toolbox.</span></span> <span data-ttu-id="6c6aa-106">Weitere Informationen finden Sie unter [com-Komponenten, Dialog Feld "Toolbox anpassen](/previous-versions/visualstudio/visual-studio-2010/cby6tzh5(v=vs.100))".</span><span class="sxs-lookup"><span data-stu-id="6c6aa-106">For more information, see [COM Components, Customize Toolbox Dialog Box](/previous-versions/visualstudio/visual-studio-2010/cby6tzh5(v=vs.100)).</span></span>

## <a name="add-an-activex-control-to-your-windows-form"></a><span data-ttu-id="6c6aa-107">Hinzufügen eines ActiveX-Steuer Elements zu Windows Form</span><span class="sxs-lookup"><span data-stu-id="6c6aa-107">Add an ActiveX control to your Windows Form</span></span>

<span data-ttu-id="6c6aa-108">Um Ihrem Windows Form ein ActiveX-Steuerelement hinzuzufügen, doppelklicken Sie auf das-Steuerelement in der Toolbox.</span><span class="sxs-lookup"><span data-stu-id="6c6aa-108">To add an ActiveX control to your Windows Form, double-click the control on the Toolbox.</span></span>

<span data-ttu-id="6c6aa-109">Visual Studio fügt alle Verweise auf das-Steuerelement in Ihrem Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="6c6aa-109">Visual Studio adds all references to the control in your project.</span></span> <span data-ttu-id="6c6aa-110">Weitere Informationen zu den Punkten, die bei der Verwendung von ActiveX-Steuerelementen auf Windows Forms zu berücksichtigen sind, finden Sie unter [Überlegungen beim Hosting eines ActiveX-Steuer Elements in einem Windows Form](considerations-when-hosting-an-activex-control-on-a-windows-form.md).</span><span class="sxs-lookup"><span data-stu-id="6c6aa-110">For more information about things to keep in mind when using ActiveX controls on Windows Forms, see [Considerations When Hosting an ActiveX Control on a Windows Form](considerations-when-hosting-an-activex-control-on-a-windows-form.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6c6aa-111">Das Windows Forms ActiveX-Steuerelement-Import Programm (AxImp.exe) erstellt Ereignis Argumente eines anderen Typs als erwartet beim Importieren von ActiveX-Dynamic Link Libraries.</span><span class="sxs-lookup"><span data-stu-id="6c6aa-111">The Windows Forms ActiveX Control Importer (AxImp.exe) creates event arguments of a different type than expected upon importation of ActiveX dynamic link libraries.</span></span> <span data-ttu-id="6c6aa-112">Die von AxImp.exe erstellten Argumente ähneln den folgenden: `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEvent e)` , wenn `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEventArgs e)` erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="6c6aa-112">The arguments created by AxImp.exe are similar to the following: `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEvent e)`, when `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEventArgs e)` is expected.</span></span> <span data-ttu-id="6c6aa-113">Beachten Sie, dass diese Unregelmäßigkeiten nicht verhindern, dass Code normal funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6c6aa-113">Be aware that this irregularity does not prevent code from functioning normally.</span></span> <span data-ttu-id="6c6aa-114">Weitere Informationen finden Sie unter [Windows Forms ActiveX-Steuerelement-Import Programm (Aximp.exe)](/dotnet/framework/tools/aximp-exe-windows-forms-activex-control-importer).</span><span class="sxs-lookup"><span data-stu-id="6c6aa-114">For details, see [Windows Forms ActiveX Control Importer (Aximp.exe)](/dotnet/framework/tools/aximp-exe-windows-forms-activex-control-importer).</span></span>

## <a name="see-also"></a><span data-ttu-id="6c6aa-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c6aa-115">See also</span></span>

- [<span data-ttu-id="6c6aa-116">Windows Forms Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="6c6aa-116">Windows Forms Controls</span></span>](index.md)
- <span data-ttu-id="6c6aa-117">[In zahlreichen Sprachen und Bibliotheken verglichene Steuerelemente und programmierbare Objekte](/previous-versions/visualstudio/visual-studio-2010/0061wezk(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="6c6aa-117">[Controls and Programmable Objects Compared in Various Languages and Libraries](/previous-versions/visualstudio/visual-studio-2010/0061wezk(v=vs.100))</span></span>
- [<span data-ttu-id="6c6aa-118">How to: Hinzufügen von Steuerelementen zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6c6aa-118">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
- [<span data-ttu-id="6c6aa-119">Beschriften einzelner Steuerelemente für Windows Forms und Konfigurieren von Shortcuts für diese Elemente</span><span class="sxs-lookup"><span data-stu-id="6c6aa-119">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [<span data-ttu-id="6c6aa-120">Steuerelemente für Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6c6aa-120">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
- [<span data-ttu-id="6c6aa-121">Windows Forms-Steuerelemente nach Funktion</span><span class="sxs-lookup"><span data-stu-id="6c6aa-121">Windows Forms Controls by Function</span></span>](windows-forms-controls-by-function.md)
