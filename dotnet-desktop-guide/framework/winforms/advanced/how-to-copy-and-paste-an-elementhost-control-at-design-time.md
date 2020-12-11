---
title: 'Vorgehensweise: Kopieren und Einfügen eines ElementHost-Steuerelements zur Entwurfszeit'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, content copying and pasting
- interoperability [WPF]
- ElementHost control [Windows Forms], copying and pasting at design time
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: e570375d-2a68-44ba-b4f7-c781af2d20e8
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: bde599dd8f2f592e9cd361c37572da240f710e2f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972376"
---
# <a name="how-to-copy-and-paste-an-elementhost-control"></a><span data-ttu-id="1a420-102">Gewusst wie: Kopieren und Einfügen eines Element Host-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="1a420-102">How to: Copy and paste an ElementHost control</span></span>

<span data-ttu-id="1a420-103">In diesem Verfahren wird gezeigt, wie ein Windows Presentation Foundation (WPF)-Steuerelement in ein Windows Form in Visual Studio kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="1a420-103">This procedure shows you how to copy a Windows Presentation Foundation (WPF) control on a Windows Form in Visual Studio.</span></span>

1. <span data-ttu-id="1a420-104">Fügen Sie in Visual Studio ein neues WPF <xref:System.Windows.Controls.UserControl> zu einem Windows Forms Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="1a420-104">In Visual Studio, add a new WPF <xref:System.Windows.Controls.UserControl> to a Windows Forms project.</span></span> <span data-ttu-id="1a420-105">Verwenden Sie den Standardnamen, `UserControl1.xaml`, für den Steuerelementtyp.</span><span class="sxs-lookup"><span data-stu-id="1a420-105">Use the default name for the control type, `UserControl1.xaml`.</span></span> <span data-ttu-id="1a420-106">Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Erstellen eines neuen WPF-Inhalts auf Windows Forms zur Entwurfszeit](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="1a420-106">For more information, see [Walkthrough: Creating New WPF Content on Windows Forms at Design Time](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span></span>

2. <span data-ttu-id="1a420-107">Legen Sie im Fenster **Eigenschaften** den Wert der-Eigenschaft <xref:System.Windows.FrameworkElement.Width%2A> und <xref:System.Windows.FrameworkElement.Height%2A> der-Eigenschaft von `UserControl1` auf **200** fest.</span><span class="sxs-lookup"><span data-stu-id="1a420-107">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties of `UserControl1` to **200**.</span></span>

3. <span data-ttu-id="1a420-108">Legen Sie den Wert der- <xref:System.Windows.Controls.Control.Background%2A> Eigenschaft auf **Blue** fest.</span><span class="sxs-lookup"><span data-stu-id="1a420-108">Set the value of the <xref:System.Windows.Controls.Control.Background%2A> property to **Blue**.</span></span>

4. <span data-ttu-id="1a420-109">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="1a420-109">Build the project.</span></span>

5. <span data-ttu-id="1a420-110">Öffnen Sie `Form1` im Windows Forms-Designer.</span><span class="sxs-lookup"><span data-stu-id="1a420-110">Open `Form1` in the Windows Forms Designer.</span></span>

6. <span data-ttu-id="1a420-111">Ziehen Sie aus der **Toolbox** eine Instanz von `UserControl1` auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="1a420-111">From the **Toolbox**, drag an instance of `UserControl1` onto the form.</span></span>

   <span data-ttu-id="1a420-112">Eine Instanz von `UserControl1` wird in einem neuen <xref:System.Windows.Forms.Integration.ElementHost>-Steuerelement namens `elementHost1` gehostet.</span><span class="sxs-lookup"><span data-stu-id="1a420-112">An instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost1`.</span></span>

7. <span data-ttu-id="1a420-113">Wenn `elementHost1` Sie ausgewählt haben, drücken Sie **STRG** + **C** , um Sie in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="1a420-113">With `elementHost1` selected, press **Ctrl**+**C** to copy it to the clipboard.</span></span>

8. <span data-ttu-id="1a420-114">Drücken Sie **STRG** + **V** , um das kopierte Steuerelement in das Formular einzufügen.</span><span class="sxs-lookup"><span data-stu-id="1a420-114">Press **Ctrl**+**V** to paste the copied control onto the form.</span></span>

   <span data-ttu-id="1a420-115"><xref:System.Windows.Forms.Integration.ElementHost>Im Formular wird ein neues Steuerelement `elementHost2` mit dem Namen erstellt.</span><span class="sxs-lookup"><span data-stu-id="1a420-115">A new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost2` is created on the form.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a420-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a420-116">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="1a420-117">Migration und Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="1a420-117">Migration and Interoperability</span></span>](/dotnet/framework/wpf/advanced/migration-and-interoperability)
- [<span data-ttu-id="1a420-118">Verwenden von WPF-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="1a420-118">Using WPF Controls</span></span>](using-wpf-controls.md)
- [<span data-ttu-id="1a420-119">Entwerfen von XAML-Code in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1a420-119">Design XAML in Visual Studio</span></span>](/visualstudio/xaml-tools/designing-xaml-in-visual-studio)
