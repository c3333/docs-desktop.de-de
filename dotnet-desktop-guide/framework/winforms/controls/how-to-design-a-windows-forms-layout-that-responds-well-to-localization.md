---
title: Entwerfen eines lokalisierbaren Layouts
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- application design [Windows Forms], localization
- Windows Forms, localization
- localization [Windows Forms], Windows Forms layout
ms.assetid: d13eff2d-701c-4b6e-8838-3885cbfb7223
ms.openlocfilehash: ae52669d2547532fcdaabab9aeb2cf40a4a6fa2d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976316"
---
# <a name="how-to-design-a-windows-forms-layout-that-responds-well-to-localization"></a><span data-ttu-id="ad952-102">Vorgehensweise: Entwerfen eines Windows Forms-Layouts, das zur Lokalisierung gut geeignet ist</span><span class="sxs-lookup"><span data-stu-id="ad952-102">How to: Design a Windows Forms Layout that Responds Well to Localization</span></span>

<span data-ttu-id="ad952-103">Mit der Erstellung von Formularen, die bereit für die Lokalisierung sind, lässt sich die Entwicklung für internationale Märkte erheblich beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="ad952-103">Creating forms that are ready to be localized greatly speeds development for international markets.</span></span> <span data-ttu-id="ad952-104">Sie können das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement verwenden, um Layouts zu implementieren, die sich problemlos an die Größenänderung von Steuerelementen aufgrund von Änderungen der <xref:System.Windows.Forms.Control.Text%2A>-Eigenschaftswerte anpassen.</span><span class="sxs-lookup"><span data-stu-id="ad952-104">You can use the <xref:System.Windows.Forms.TableLayoutPanel> control to implement layouts that respond gracefully as controls resize due to changes in their <xref:System.Windows.Forms.Control.Text%2A> property values.</span></span>

## <a name="example"></a><span data-ttu-id="ad952-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ad952-105">Example</span></span>

 <span data-ttu-id="ad952-106">Dieses Formular zeigt, wie ein Layout erstellt wird, dass sich proportional anpasst, wenn Sie angezeigte Zeichenfolgenwerte in andere Sprachen übersetzen.</span><span class="sxs-lookup"><span data-stu-id="ad952-106">This form demonstrates how to create a layout that proportionally adjusts when you translate displayed string values into other languages.</span></span> <span data-ttu-id="ad952-107">Diese Art der Übersetzung wird als *Lokalisierung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ad952-107">This process of translation is called *localization*.</span></span> <span data-ttu-id="ad952-108">Weitere Informationen finden Sie unter [Lokalisierung](/dotnet/standard/globalization-localization/localization).</span><span class="sxs-lookup"><span data-stu-id="ad952-108">For more information, see [Localization](/dotnet/standard/globalization-localization/localization).</span></span>

 <span data-ttu-id="ad952-109">Visual Studio bietet umfassende Unterstützung für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ad952-109">There is extensive support for this task in Visual Studio.</span></span>  <span data-ttu-id="ad952-110">Siehe auch [Exemplarische Vorgehensweise: Erstellen eines Layouts, das sich proportional an die Lokalisierung anpasst](/previous-versions/visualstudio/visual-studio-2010/7k9fa71y(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="ad952-110">See also [Walkthrough: Creating a Layout That Adjusts Proportion for Localization](/previous-versions/visualstudio/visual-studio-2010/7k9fa71y(v=vs.100)).</span></span>

 [!code-csharp[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/CS/localizableform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/VB/localizableform.vb#1)]

## <a name="additional-resources"></a><span data-ttu-id="ad952-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ad952-111">Additional resources</span></span>

1. [<span data-ttu-id="ad952-112">Vorgehensweise: Ausrichten und Strecken eines Steuerelements in einem TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ad952-112">How to: Align and Stretch a Control in a TableLayoutPanel Control</span></span>](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)

2. [<span data-ttu-id="ad952-113">Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="ad952-113">Walkthrough: Arranging Controls on Windows Forms Using a FlowLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)

3. [<span data-ttu-id="ad952-114">Vorgehensweise: Überspannen von Zeilen und Spalten in einem TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ad952-114">How to: Span Rows and Columns in a TableLayoutPanel Control</span></span>](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)

4. [<span data-ttu-id="ad952-115">Vorgehensweise: Bearbeiten von Zeilen und Spalten in einem TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ad952-115">How to: Edit Columns and Rows in a TableLayoutPanel Control</span></span>](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)

5. [<span data-ttu-id="ad952-116">Exemplarische Vorgehensweise: Ausführen allgemeiner Aufgaben mit Designaktionen</span><span class="sxs-lookup"><span data-stu-id="ad952-116">Walkthrough: Perform common tasks using designer actions</span></span>](perform-common-tasks-design-actions.md)

6. [<span data-ttu-id="ad952-117">Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="ad952-117">Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)

7. [<span data-ttu-id="ad952-118">Exemplarische Vorgehensweise: Anordnen von Windows Forms-Steuerelementen mithilfe von Abständen, Rändern und der AutoSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ad952-118">Walkthrough: Laying Out Windows Forms Controls with Padding, Margins, and the AutoSize Property</span></span>](windows-forms-controls-padding-autosize.md)

8. <span data-ttu-id="ad952-119">[Vorgehensweise: Unterstützen der Lokalisierung in Windows Forms mithilfe von AutoSize und dem TableLayoutPanel-Steuerelement](/previous-versions/visualstudio/visual-studio-2010/1zkt8b33(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="ad952-119">[How to: Support Localization on Windows Forms Using AutoSize and the TableLayoutPanel Control](/previous-versions/visualstudio/visual-studio-2010/1zkt8b33(v=vs.100))</span></span>

9. <span data-ttu-id="ad952-120">[Exemplarische Vorgehensweise: Erstellen eines in der Größe veränderbaren Windows Forms für die Dateneingabe](/previous-versions/visualstudio/visual-studio-2010/991eahec(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="ad952-120">[Walkthrough: Creating a Resizable Windows Form for Data Entry](/previous-versions/visualstudio/visual-studio-2010/991eahec(v=vs.100))</span></span>

## <a name="compiling-the-code"></a><span data-ttu-id="ad952-121">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="ad952-121">Compiling the Code</span></span>

 <span data-ttu-id="ad952-122">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ad952-122">This example requires:</span></span>

- <span data-ttu-id="ad952-123">Verweise auf die Assemblys "System", "System.Data", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="ad952-123">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad952-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad952-124">See also</span></span>

- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
- [<span data-ttu-id="ad952-125">Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="ad952-125">Localization</span></span>](/dotnet/standard/globalization-localization/localization)
