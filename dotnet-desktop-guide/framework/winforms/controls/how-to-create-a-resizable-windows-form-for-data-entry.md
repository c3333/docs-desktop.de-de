---
title: 'Vorgehensweise: Erstellen von in der Größe veränderbaren Windows Forms für die Dateneingabe'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- layout [Windows Forms], resizing
- forms [Windows Forms], creating resizable
- Windows Forms, resizable
ms.assetid: babdf198-404c-485d-a914-ed370c6ecd99
ms.openlocfilehash: c0cf79941a55f7412694b6ef9e8797e48aa069a1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976333"
---
# <a name="how-to-create-a-resizable-windows-form-for-data-entry"></a><span data-ttu-id="81e99-102">Vorgehensweise: Erstellen von in der Größe veränderbaren Windows Forms für die Dateneingabe</span><span class="sxs-lookup"><span data-stu-id="81e99-102">How to: Create a Resizable Windows Form for Data Entry</span></span>

<span data-ttu-id="81e99-103">Ein gutes Layout reagiert angemessen auf Änderungen in den Dimensionen des übergeordneten Formulars.</span><span class="sxs-lookup"><span data-stu-id="81e99-103">A good layout responds well to changes in the dimensions of its parent form.</span></span> <span data-ttu-id="81e99-104">Sie können das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement verwenden, um das Layout Ihres Formulars so zu gestalten, dass die Größe und die Position Ihrer Steuerelemente auf konsistente Weise geändert werden, wenn sich die Dimensionen des Formulars ändern.</span><span class="sxs-lookup"><span data-stu-id="81e99-104">You can use the <xref:System.Windows.Forms.TableLayoutPanel> control to arrange the layout of your form to resize and position your controls in a consistent way as the form's dimensions change.</span></span> <span data-ttu-id="81e99-105">Das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement ist auch nützlich, wenn Änderungen am Inhalt Ihrer Steuerelemente Änderungen im Layout verursachen.</span><span class="sxs-lookup"><span data-stu-id="81e99-105">The <xref:System.Windows.Forms.TableLayoutPanel> control is also useful when changes in the contents of your controls cause changes in the layout.</span></span> <span data-ttu-id="81e99-106">Der in diesem Verfahren beschriebene Vorgang kann innerhalb der Visual Studio-Umgebung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="81e99-106">The process covered in this procedure can be done within the Visual Studio environment.</span></span>  <span data-ttu-id="81e99-107">Siehe auch [Exemplarische Vorgehensweise: Erstellen eines in der Größe veränderbaren Windows Forms für die Dateneingabe](/previous-versions/visualstudio/visual-studio-2010/991eahec(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="81e99-107">Also see [Walkthrough: Creating a Resizable Windows Form for Data Entry](/previous-versions/visualstudio/visual-studio-2010/991eahec(v=vs.100)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="81e99-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="81e99-108">Example</span></span>  

 <span data-ttu-id="81e99-109">Im folgenden Beispiel wird veranschaulicht, wie ein <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement zum Erstellen eines Layouts verwendet wird, das angemessen reagiert, wenn der Benutzer die Größe des Formulars ändert.</span><span class="sxs-lookup"><span data-stu-id="81e99-109">The following example demonstrates how to use a <xref:System.Windows.Forms.TableLayoutPanel> control to build a layout that responds well when the user resizes the form.</span></span> <span data-ttu-id="81e99-110">Außerdem wird ein Layout gezeigt, das für Lokalisierung gut geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="81e99-110">It also demonstrates a layout that responds well to localization.</span></span>  
  
 [!code-cpp[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/cpp/basicdataentryform.cpp#1)]
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/CS/basicdataentryform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/VB/basicdataentryform.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="81e99-111">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="81e99-111">Compiling the Code</span></span>  

 <span data-ttu-id="81e99-112">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="81e99-112">This example requires:</span></span>  
  
- <span data-ttu-id="81e99-113">Verweise auf die Assemblys "System", "System.Data", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="81e99-113">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81e99-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81e99-114">See also</span></span>

- <xref:System.Windows.Forms.FlowLayoutPanel>
- <xref:System.Windows.Forms.TableLayoutPanel>
- [<span data-ttu-id="81e99-115">Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="81e99-115">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="81e99-116">Vorgehensweise: Entwerfen eines Windows Forms-Layouts, das zur Lokalisierung gut geeignet ist</span><span class="sxs-lookup"><span data-stu-id="81e99-116">How to: Design a Windows Forms Layout that Responds Well to Localization</span></span>](how-to-design-a-windows-forms-layout-that-responds-well-to-localization.md)
