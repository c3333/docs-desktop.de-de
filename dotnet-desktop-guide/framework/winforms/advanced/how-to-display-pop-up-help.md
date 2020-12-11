---
title: 'Vorgehensweise: Anzeigen der kontextbezogenen Hilfe'
ms.date: 03/30/2017
helpviewer_keywords:
- pop-up Help
- Help [Windows Forms], pop-up Help
- Windows Forms, displaying Help
- forms [Windows Forms], displaying Help
- modal dialog boxes [Windows Forms], pop-up Help
- F1 Help [Windows Forms], in dialog boxes
- HelpProvider component [Windows Forms]
- Help [Windows Forms], adding to dialog boxes
ms.assetid: 218aa81e-e87e-4d67-af05-11627bbdce3b
ms.openlocfilehash: a3b40f49119fcf7900f1f0c8b77c5d83fe81144c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972358"
---
# <a name="how-to-display-pop-up-help"></a><span data-ttu-id="2702b-102">Gewusst wie: Anzeigen der Popup Hilfe</span><span class="sxs-lookup"><span data-stu-id="2702b-102">How to: Display pop-up Help</span></span>

<span data-ttu-id="2702b-103">Eine Möglichkeit zum Anzeigen der Hilfe Windows Forms finden Sie über die Schaltfläche " **Hilfe** ", die sich auf der rechten Seite der Titelleiste befindet, auf die über die-Eigenschaft zugegriffen werden kann <xref:System.Windows.Forms.Form.HelpButton%2A> .</span><span class="sxs-lookup"><span data-stu-id="2702b-103">One way to display Help on Windows Forms is through the **Help** button, located on the right side of the title bar, accessible through the <xref:System.Windows.Forms.Form.HelpButton%2A> property.</span></span> <span data-ttu-id="2702b-104">Diese Art, die Hilfe aufzurufen, eignet sich besonders für Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="2702b-104">This type of Help display is well-suited for use with dialog boxes.</span></span> <span data-ttu-id="2702b-105">In modal (mit der <xref:System.Windows.Forms.Form.ShowDialog%2A>-Methode) angezeigten Dialogfeldern ist das Aufrufen externer Hilfesysteme problematisch, da modale Dialogfelder zuerst geschlossen werden müssen, ehe der Fokus auf ein anderes Fenster gerichtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2702b-105">Dialog boxes shown modally (with the <xref:System.Windows.Forms.Form.ShowDialog%2A> method) have trouble bringing up external Help systems, because modal dialog boxes need to be closed before focus can shift to another window.</span></span> <span data-ttu-id="2702b-106">Außerdem erfordert die Verwendung der Schaltfläche **Hilfe** , dass in der Titelleiste keine Schaltfläche **minimieren** oder **maximieren** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2702b-106">Additionally, using the **Help** button requires that there is no **Minimize** button or **Maximize** button shown in the title bar.</span></span> <span data-ttu-id="2702b-107">Dabei handelt es sich um eine standardmäßige Dialogfeld Konvention, während Formulare normalerweise die Schaltflächen **minimieren** und **maximieren** .</span><span class="sxs-lookup"><span data-stu-id="2702b-107">This is a standard dialog-box convention, whereas forms usually have **Minimize** and **Maximize** buttons.</span></span>

<span data-ttu-id="2702b-108">Sie können die-Komponente auch verwenden, <xref:System.Windows.Forms.HelpProvider> um Steuerelemente mit Dateien in einem Hilfesystem zu verknüpfen, auch wenn Sie die Popup Hilfe implementiert haben.</span><span class="sxs-lookup"><span data-stu-id="2702b-108">You can also use the <xref:System.Windows.Forms.HelpProvider> component to link controls to files in a Help system, even if you have implemented pop-up Help.</span></span> <span data-ttu-id="2702b-109">Weitere Informationen finden Sie unter [Bereitstellen von Hilfe in einer Windows-Anwendung](how-to-provide-help-in-a-windows-application.md).</span><span class="sxs-lookup"><span data-stu-id="2702b-109">For more information, see [Providing Help in a Windows Application](how-to-provide-help-in-a-windows-application.md).</span></span>

## <a name="display-pop-up-help"></a><span data-ttu-id="2702b-110">Popup Hilfe anzeigen</span><span class="sxs-lookup"><span data-stu-id="2702b-110">Display pop-up Help</span></span>

1. <span data-ttu-id="2702b-111">Ziehen Sie in Visual Studio eine [HelpProvider](../controls/helpprovider-component-windows-forms.md) -Komponente aus der Toolbox auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="2702b-111">In Visual Studio, drag a [HelpProvider](../controls/helpprovider-component-windows-forms.md) component from the Toolbox to your form.</span></span>

   <span data-ttu-id="2702b-112">Sie befindet sich in der Komponentenleiste im unteren Bereich des Windows Forms Designer.</span><span class="sxs-lookup"><span data-stu-id="2702b-112">It will sit in the tray at the bottom of the Windows Forms Designer.</span></span>

2. <span data-ttu-id="2702b-113">Legen Sie im Fenster "Eigenschaften" die Eigenschaft <xref:System.Windows.Forms.Form.HelpButton%2A> auf `true` fest.</span><span class="sxs-lookup"><span data-stu-id="2702b-113">In the Properties window, set the <xref:System.Windows.Forms.Form.HelpButton%2A> property to `true`.</span></span> <span data-ttu-id="2702b-114">Dadurch wird in der Titelleiste des Formulars auf der rechten Seite eine Schaltfläche mit einem Fragezeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2702b-114">This will display a button with a question mark in it on the right side of the title bar of the form.</span></span>

3. <span data-ttu-id="2702b-115">Damit die Hilfeschaltfläche <xref:System.Windows.Forms.Form.HelpButton%2A> angezeigt werden kann, müssen Sie die Eigenschaften <xref:System.Windows.Forms.Form.MinimizeBox%2A> und <xref:System.Windows.Forms.Form.MaximizeBox%2A> des Formulars auf `false`, die Eigenschaft <xref:System.Windows.Forms.Form.ControlBox%2A> auf `true` und die Eigenschaft <xref:System.Windows.Forms.Form.FormBorderStyle%2A> auf einen der folgenden Werte festlegen: <xref:System.Windows.Forms.FormBorderStyle.FixedSingle>, <xref:System.Windows.Forms.FormBorderStyle.Fixed3D>, <xref:System.Windows.Forms.FormBorderStyle.FixedDialog> oder <xref:System.Windows.Forms.FormBorderStyle.Sizable>.</span><span class="sxs-lookup"><span data-stu-id="2702b-115">In order for the <xref:System.Windows.Forms.Form.HelpButton%2A> to display, the form's <xref:System.Windows.Forms.Form.MinimizeBox%2A> and <xref:System.Windows.Forms.Form.MaximizeBox%2A> properties must be set to `false`, the <xref:System.Windows.Forms.Form.ControlBox%2A> property set to `true`, and the <xref:System.Windows.Forms.Form.FormBorderStyle%2A> property to one of the following values: <xref:System.Windows.Forms.FormBorderStyle.FixedSingle>, <xref:System.Windows.Forms.FormBorderStyle.Fixed3D>, <xref:System.Windows.Forms.FormBorderStyle.FixedDialog> or <xref:System.Windows.Forms.FormBorderStyle.Sizable>.</span></span>

4. <span data-ttu-id="2702b-116">Wählen Sie das Steuerelement aus, für das Sie Hilfeinformationen in Ihrem Formular anzeigen möchten, und legen Sie im Fenster "Eigenschaften" den Hilfetext fest.</span><span class="sxs-lookup"><span data-stu-id="2702b-116">Select the control for which you want to show help on your form and set the Help string in the Properties window.</span></span> <span data-ttu-id="2702b-117">Dies ist die Text Zeichenfolge, die [in einem Fenster](../controls/tooltip-component-windows-forms.md)angezeigt wird, das einer QuickInfo ähnelt.</span><span class="sxs-lookup"><span data-stu-id="2702b-117">This is the string of text that will be displayed in a window similar to a [ToolTip](../controls/tooltip-component-windows-forms.md).</span></span>

5. <span data-ttu-id="2702b-118">Drücken Sie **F5**.</span><span class="sxs-lookup"><span data-stu-id="2702b-118">Press **F5**.</span></span>

6. <span data-ttu-id="2702b-119">Klicken Sie in der Titelleiste auf die Schaltfläche **Hilfe** , und klicken Sie auf das Steuerelement, für das Sie die Hilfe Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2702b-119">Press the **Help** button on the title bar and click the control on which you set the Help string.</span></span>

## <a name="see-also"></a><span data-ttu-id="2702b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2702b-120">See also</span></span>

- [<span data-ttu-id="2702b-121">Benutzerführung mithilfe von QuickInfos</span><span class="sxs-lookup"><span data-stu-id="2702b-121">Control Help Using ToolTips</span></span>](control-help-using-tooltips.md)
- [<span data-ttu-id="2702b-122">Integrieren von Benutzerhilfe in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2702b-122">Integrating User Help in Windows Forms</span></span>](integrating-user-help-in-windows-forms.md)
- [<span data-ttu-id="2702b-123">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2702b-123">Windows Forms</span></span>](../index.yml)
