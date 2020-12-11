---
title: Festlegen des Hintergrunds eines Panels mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- background colors [Windows Forms], Windows Forms Panel controls
- background images [Windows Forms], Windows Forms Panel controls
- Panel control [Windows Forms], background
- colors [Windows Forms], Windows Forms Panel controls
ms.assetid: db83cf54-3c69-4b08-ac6c-25b9b5abb1b0
ms.openlocfilehash: 8bdefba433632f7ba02f549a549c52c7aa56c2d7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976764"
---
# <a name="how-to-set-the-background-of-a-windows-forms-panel-using-the-designer"></a><span data-ttu-id="7fb46-102">Gewusst wie: Festlegen des Hintergrunds eines Windows Forms Panels mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="7fb46-102">How to: Set the background of a Windows Forms panel using the Designer</span></span>

<span data-ttu-id="7fb46-103">Ein Windows Forms <xref:System.Windows.Forms.Panel> -Steuerelement kann sowohl eine Hintergrundfarbe als auch ein Hintergrundbild anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7fb46-103">A Windows Forms <xref:System.Windows.Forms.Panel> control can display both a background color and a background image.</span></span> <span data-ttu-id="7fb46-104">Die- <xref:System.Windows.Forms.Control.BackColor%2A> Eigenschaft legt die Hintergrundfarbe für Steuerelemente fest, die im Bereich enthalten sind, z. b. Bezeichnungen und Options Felder.</span><span class="sxs-lookup"><span data-stu-id="7fb46-104">The <xref:System.Windows.Forms.Control.BackColor%2A> property sets the background color for controls that are contained in the panel, such as labels and radio buttons.</span></span> <span data-ttu-id="7fb46-105">Wenn die <xref:System.Windows.Forms.Control.BackgroundImage%2A> Eigenschaft nicht festgelegt ist, <xref:System.Windows.Forms.Control.BackColor%2A> wird der gesamte Bereich durch die Auswahl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="7fb46-105">If the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property is not set, the <xref:System.Windows.Forms.Control.BackColor%2A> selection will fill all of the panel.</span></span> <span data-ttu-id="7fb46-106">Wenn die- <xref:System.Windows.Forms.Control.BackgroundImage%2A> Eigenschaft festgelegt ist, wird das Bild hinter den Steuerelementen angezeigt, die im Bereich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7fb46-106">If the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property is set, the image will be displayed behind the controls that are contained in the panel.</span></span>

<span data-ttu-id="7fb46-107">Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein-Steuerelement enthält <xref:System.Windows.Forms.Panel> .</span><span class="sxs-lookup"><span data-stu-id="7fb46-107">The following procedure requires a **Windows Application** project with a form that contains a <xref:System.Windows.Forms.Panel> control.</span></span> <span data-ttu-id="7fb46-108">Weitere Informationen zum Einrichten eines solchen Projekts in Visual Studio finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="7fb46-108">For information about how to set up such a project in Visual Studio, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>

## <a name="set-the-background-in-the-windows-forms-designer"></a><span data-ttu-id="7fb46-109">Legen Sie den Hintergrund im Windows Forms-Designer</span><span class="sxs-lookup"><span data-stu-id="7fb46-109">Set the background in the Windows Forms Designer</span></span>

1. <span data-ttu-id="7fb46-110">Öffnen Sie das Projekt in Visual Studio, und wählen Sie das Steuerelement aus <xref:System.Windows.Forms.Panel> .</span><span class="sxs-lookup"><span data-stu-id="7fb46-110">Open the project in Visual Studio and select the <xref:System.Windows.Forms.Panel> control.</span></span>

2. <span data-ttu-id="7fb46-111">Klicken Sie im Fenster **Eigenschaften** neben der-Eigenschaft auf die Pfeil Schaltfläche, <xref:System.Windows.Forms.Control.BackColor%2A> um ein Fenster mit drei Registerkarten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7fb46-111">In the **Properties** window, click the arrow button next to the <xref:System.Windows.Forms.Control.BackColor%2A> property to display a window with three tabs.</span></span>

3. <span data-ttu-id="7fb46-112">Wählen Sie die Registerkarte **Benutzer** definiert aus, um eine Palette von Farben anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7fb46-112">Select the **Custom** tab to display a palette of colors.</span></span>

4. <span data-ttu-id="7fb46-113">Wählen Sie die Registerkarte **Web** oder **System** aus, um eine Liste vordefinierter Namen für Farben anzuzeigen, und wählen Sie dann eine Farbe aus.</span><span class="sxs-lookup"><span data-stu-id="7fb46-113">Select the **Web** or **System** tab to display a list of predefined names for colors, and then select a color.</span></span>

5. <span data-ttu-id="7fb46-114">Klicken Sie im Fenster **Eigenschaften** neben der-Eigenschaft auf die Pfeil Schaltfläche <xref:System.Windows.Forms.Control.BackgroundImage%2A> .</span><span class="sxs-lookup"><span data-stu-id="7fb46-114">In the **Properties** window, click the arrow button next to the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property.</span></span>

6. <span data-ttu-id="7fb46-115">Wählen Sie im Dialogfeld **Öffnen** die Datei aus, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="7fb46-115">In the **Open** dialog box, select the file that you want to display.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fb46-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fb46-116">See also</span></span>

- <xref:System.Windows.Forms.Control.BackColor%2A>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
- [<span data-ttu-id="7fb46-117">Panelsteuerelement</span><span class="sxs-lookup"><span data-stu-id="7fb46-117">Panel Control</span></span>](panel-control-windows-forms.md)
- [<span data-ttu-id="7fb46-118">Übersicht über das Panel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7fb46-118">Panel Control Overview</span></span>](panel-control-overview-windows-forms.md)
- [<span data-ttu-id="7fb46-119">Vorgehensweise: Gruppieren von Steuerelementen mit dem Windows Forms-Bereichssteuerelement im Designer</span><span class="sxs-lookup"><span data-stu-id="7fb46-119">How to: Group Controls with the Windows Forms Panel Control Using the Designer</span></span>](group-controls-with-wf-panel-control-using-the-designer.md)
