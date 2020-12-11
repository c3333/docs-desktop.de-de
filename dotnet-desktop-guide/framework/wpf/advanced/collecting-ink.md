---
title: Erfassen digitaler Freihand
ms.date: 08/15/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ink [WPF], collecting
- InkCanvas element [WPF]
- properties [WPF], DrawingAttributes
- collecting digital ink [WPF]
- digital ink [WPF], collecting
- properties [WPF], DefaultDrawingAttributes
- DefaultDrawingAttributes property [WPF]
ms.assetid: 66a3129d-9577-43eb-acbd-56c147282016
ms.openlocfilehash: 813a5313a6fbf83c36cdbed1f64ce69a217ad788
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976422"
---
# <a name="collect-ink"></a><span data-ttu-id="3d226-102">Frei Hand Eingaben erfassen</span><span class="sxs-lookup"><span data-stu-id="3d226-102">Collect Ink</span></span>

<span data-ttu-id="3d226-103">Als einen ihrer zentralen Funktionsbestandteile erfasst die [Windows Presentation Foundation](../index.md)-Plattform Freihandeingaben.</span><span class="sxs-lookup"><span data-stu-id="3d226-103">The [Windows Presentation Foundation](../index.md) platform collects digital ink as a core part of its functionality.</span></span> <span data-ttu-id="3d226-104">In diesem Thema werden die Methoden für die Sammlung von frei Hand Eingaben in Windows Presentation Foundation (WPF) erläutert.</span><span class="sxs-lookup"><span data-stu-id="3d226-104">This topic discusses methods for collection of ink in Windows Presentation Foundation (WPF).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3d226-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3d226-105">Prerequisites</span></span>

<span data-ttu-id="3d226-106">Um die folgenden Beispiele verwenden zu können, müssen Sie zuerst Visual Studio und den Windows SDK installieren.</span><span class="sxs-lookup"><span data-stu-id="3d226-106">To use the following examples, you must first install Visual Studio and the Windows SDK.</span></span> <span data-ttu-id="3d226-107">Außerdem sollten Sie wissen, wie Anwendungen für das WPF geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3d226-107">You should also understand how to write applications for the WPF.</span></span> <span data-ttu-id="3d226-108">Weitere Informationen zu den ersten Schritten mit WPF finden Sie unter Exemplarische Vorgehensweise [: meine erste WPF-Desktop Anwendung](../getting-started/walkthrough-my-first-wpf-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="3d226-108">For more information about getting started with WPF, see [Walkthrough: My first WPF desktop application](../getting-started/walkthrough-my-first-wpf-desktop-application.md).</span></span>

## <a name="use-the-inkcanvas-element"></a><span data-ttu-id="3d226-109">Verwenden des InkCanvas-Elements</span><span class="sxs-lookup"><span data-stu-id="3d226-109">Use the InkCanvas Element</span></span>

<span data-ttu-id="3d226-110">Das- <xref:System.Windows.Controls.InkCanvas?displayProperty=fullName> Element stellt die einfachste Möglichkeit zum Erfassen von frei Hand Eingaben in WPF bereit.</span><span class="sxs-lookup"><span data-stu-id="3d226-110">The <xref:System.Windows.Controls.InkCanvas?displayProperty=fullName> element provides the easiest way to collect ink in WPF.</span></span> <span data-ttu-id="3d226-111">Verwenden <xref:System.Windows.Controls.InkCanvas> Sie ein-Element, um frei Hand Eingaben zu empfangen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d226-111">Use an <xref:System.Windows.Controls.InkCanvas> element to receive and display ink input.</span></span> <span data-ttu-id="3d226-112">Freihandeingaben erfolgen im Allgemeinen mithilfe eines Tablettstifts, der über ein Digitalisierungsgerät Freihandstriche erzeugt.</span><span class="sxs-lookup"><span data-stu-id="3d226-112">You commonly input ink through the use of a stylus, which interacts with a digitizer to produce ink strokes.</span></span> <span data-ttu-id="3d226-113">Anstelle eines Tablettstifts kann auch eine Maus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d226-113">In addition, a mouse can be used in place of a stylus.</span></span> <span data-ttu-id="3d226-114">Die erstellten Striche werden als <xref:System.Windows.Ink.Stroke> -Objekte dargestellt und können sowohl Programm gesteuert als auch durch Benutzereingaben bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="3d226-114">The created strokes are represented as <xref:System.Windows.Ink.Stroke> objects, and they can be manipulated both programmatically and by user input.</span></span> <span data-ttu-id="3d226-115"><xref:System.Windows.Controls.InkCanvas>Ermöglicht es Benutzern, ein vorhandenes auszuwählen, zu ändern oder zu löschen <xref:System.Windows.Ink.Stroke> .</span><span class="sxs-lookup"><span data-stu-id="3d226-115">The <xref:System.Windows.Controls.InkCanvas> enables users to select, modify, or delete an existing <xref:System.Windows.Ink.Stroke>.</span></span>

<span data-ttu-id="3d226-116">Mithilfe von XAML können Sie die frei Hand Auflistung so einfach einrichten, wie Sie der Struktur ein **InkCanvas** -Element hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3d226-116">By using XAML, you can set up ink collection as easily as adding an **InkCanvas** element to your tree.</span></span> <span data-ttu-id="3d226-117">Im folgenden Beispiel wird ein einem <xref:System.Windows.Controls.InkCanvas> standardmäßigen WPF-Projekt hinzugefügt, das in Visual Studio erstellt wurde:</span><span class="sxs-lookup"><span data-stu-id="3d226-117">The following example adds an <xref:System.Windows.Controls.InkCanvas> to a default WPF project created in Visual Studio:</span></span>

[!code-xaml[DigitalInkTopics#6](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml#6)]

<span data-ttu-id="3d226-118">Das **InkCanvas** -Element kann auch untergeordnete Elemente enthalten, sodass Sie nahezu allen Typen von XAML-Elementen frei Hand Anmerkung-Funktionen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="3d226-118">The **InkCanvas** element can also contain child elements, making it possible to add ink annotation capabilities to almost any type of XAML element.</span></span> <span data-ttu-id="3d226-119">Wenn Sie z. b. einem Textelement eine Verknüpfung hinzufügen möchten, machen Sie es einfach zu einem untergeordneten Element <xref:System.Windows.Controls.InkCanvas> :</span><span class="sxs-lookup"><span data-stu-id="3d226-119">For example, to add inking capabilities to a text element, simply make it a child of an <xref:System.Windows.Controls.InkCanvas>:</span></span>

[!code-xaml[DigitalInkTopics#5](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml#5)]

<span data-ttu-id="3d226-120">Das Hinzufügen von Unterstützung für das Markieren eines Bilds mit frei Hand Eingaben ist ebenso einfach:</span><span class="sxs-lookup"><span data-stu-id="3d226-120">Adding support for marking up an image with ink is just as easy:</span></span>

[!code-xaml[DigitalInkTopics#7](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml#7)]

### <a name="inkcollection-modes"></a><span data-ttu-id="3d226-121">InkCollection-Modi</span><span class="sxs-lookup"><span data-stu-id="3d226-121">InkCollection Modes</span></span>

<span data-ttu-id="3d226-122">Der <xref:System.Windows.Controls.InkCanvas> bietet Unterstützung für verschiedene Eingabemodi durch seine- <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3d226-122">The <xref:System.Windows.Controls.InkCanvas> provides support for various input modes through its <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> property.</span></span>

### <a name="manipulate-ink"></a><span data-ttu-id="3d226-123">Freihand bearbeiten</span><span class="sxs-lookup"><span data-stu-id="3d226-123">Manipulate Ink</span></span>

<span data-ttu-id="3d226-124"><xref:System.Windows.Controls.InkCanvas>Bietet Unterstützung für viele Freihand Bearbeitungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="3d226-124">The <xref:System.Windows.Controls.InkCanvas> provides support for many ink editing operations.</span></span> <span data-ttu-id="3d226-125">Unterstützt z. b. die <xref:System.Windows.Controls.InkCanvas> Löschfunktion zum Löschen, und es ist kein zusätzlicher Code erforderlich, um dem-Element die Funktionalität hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3d226-125">For example, <xref:System.Windows.Controls.InkCanvas> supports back-of-pen erase, and no additional code is needed to add the functionality to the element.</span></span>

#### <a name="selection"></a><span data-ttu-id="3d226-126">Auswahl</span><span class="sxs-lookup"><span data-stu-id="3d226-126">Selection</span></span>

<span data-ttu-id="3d226-127">Das Festlegen des Auswahlmodus ist so einfach wie das Festlegen der- <xref:System.Windows.Controls.InkCanvasEditingMode> Eigenschaft auf **Select**.</span><span class="sxs-lookup"><span data-stu-id="3d226-127">Setting selection mode is as simple as setting the <xref:System.Windows.Controls.InkCanvasEditingMode> property to **Select**.</span></span>

<span data-ttu-id="3d226-128">Der folgende Code legt den Bearbeitungsmodus basierend auf dem Wert einer fest <xref:System.Windows.Forms.CheckBox> :</span><span class="sxs-lookup"><span data-stu-id="3d226-128">The following code sets the editing mode based on the value of a <xref:System.Windows.Forms.CheckBox>:</span></span>

[!code-csharp[DigitalInkTopics#8](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window1.xaml.cs#8)]
[!code-vb[DigitalInkTopics#8](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window1.xaml.vb#8)]

#### <a name="drawingattributes"></a><span data-ttu-id="3d226-129">DrawingAttributes</span><span class="sxs-lookup"><span data-stu-id="3d226-129">DrawingAttributes</span></span>

<span data-ttu-id="3d226-130">Verwenden Sie die- <xref:System.Windows.Ink.Stroke.DrawingAttributes%2A> Eigenschaft, um die Darstellung von Hand Strichen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3d226-130">Use the <xref:System.Windows.Ink.Stroke.DrawingAttributes%2A> property to change the appearance of ink strokes.</span></span> <span data-ttu-id="3d226-131">Beispielsweise legt der <xref:System.Windows.Ink.DrawingAttributes.Color%2A> Member von <xref:System.Windows.Ink.DrawingAttributes> die Farbe des gerenderten fest <xref:System.Windows.Ink.Stroke> .</span><span class="sxs-lookup"><span data-stu-id="3d226-131">For instance, the <xref:System.Windows.Ink.DrawingAttributes.Color%2A> member of <xref:System.Windows.Ink.DrawingAttributes> sets the color of the rendered <xref:System.Windows.Ink.Stroke>.</span></span>

<span data-ttu-id="3d226-132">Im folgenden Beispiel wird die Farbe der ausgewählten Striche in rot geändert:</span><span class="sxs-lookup"><span data-stu-id="3d226-132">The following example changes the color of the selected strokes to red:</span></span>

[!code-csharp[DigitalInkTopics#9](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window1.xaml.cs#9)]
[!code-vb[DigitalInkTopics#9](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window1.xaml.vb#9)]

### <a name="defaultdrawingattributes"></a><span data-ttu-id="3d226-133">DefaultDrawingAttributes</span><span class="sxs-lookup"><span data-stu-id="3d226-133">DefaultDrawingAttributes</span></span>

<span data-ttu-id="3d226-134">Die- <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> Eigenschaft ermöglicht den Zugriff auf Eigenschaften, z. b. Höhe, Breite und Farbe der Striche, die in einer erstellt werden sollen <xref:System.Windows.Controls.InkCanvas> .</span><span class="sxs-lookup"><span data-stu-id="3d226-134">The <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> property provides access to properties such as the height, width, and color of the strokes to be created in an <xref:System.Windows.Controls.InkCanvas>.</span></span> <span data-ttu-id="3d226-135">Nachdem Sie das geändert <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> haben, werden alle zukünftigen Striche, die in eingegeben <xref:System.Windows.Controls.InkCanvas> werden, mit den neuen Eigenschafts Werten gerendert.</span><span class="sxs-lookup"><span data-stu-id="3d226-135">Once you change the <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A>, all future strokes entered into the <xref:System.Windows.Controls.InkCanvas> are rendered with the new property values.</span></span>

<span data-ttu-id="3d226-136">Zusätzlich zum Ändern der <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> in der Code Behind-Datei können Sie die XAML-Syntax zum Angeben von <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> Eigenschaften verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d226-136">In addition to modifying the <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> in the code-behind file, you can use XAML syntax for specifying <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> properties.</span></span>

<span data-ttu-id="3d226-137">Im nächsten Beispiel wird veranschaulicht, wie die-Eigenschaft festgelegt wird <xref:System.Windows.Ink.DrawingAttributes.Color%2A> .</span><span class="sxs-lookup"><span data-stu-id="3d226-137">The next example demonstrates how to set the <xref:System.Windows.Ink.DrawingAttributes.Color%2A> property.</span></span> <span data-ttu-id="3d226-138">Um diesen Code zu verwenden, erstellen Sie in Visual Studio ein neues WPF-Projekt mit dem Namen "HelloInkCanvas".</span><span class="sxs-lookup"><span data-stu-id="3d226-138">To use this code, create a new WPF project called "HelloInkCanvas" in Visual Studio.</span></span> <span data-ttu-id="3d226-139">Ersetzen Sie den Code in der Datei " *MainWindow. XAML* " durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="3d226-139">Replace the code in the *MainWindow.xaml* file with the following code:</span></span>

[!code-xaml[HelloInkCanvas#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HelloInkCanvas/CSharp/Window1.xaml#1)]

<span data-ttu-id="3d226-140">Fügen Sie als nächstes die folgenden Ereignishandler für die Schaltfläche der Code-Behind-Datei innerhalb der MainWindow-Klasse hinzu:</span><span class="sxs-lookup"><span data-stu-id="3d226-140">Next, add the following button event handlers to the code behind file, inside the MainWindow class:</span></span>

[!code-csharp[HelloInkCanvas#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HelloInkCanvas/CSharp/Window1.xaml.cs#2)]

<span data-ttu-id="3d226-141">Nachdem Sie diesen Code kopiert haben, drücken Sie in Visual Studio **F5** , um das Programm im Debugger auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3d226-141">After copying this code, press **F5** in Visual Studio to run the program in the debugger.</span></span>

<span data-ttu-id="3d226-142">Beachten Sie, wie die <xref:System.Windows.Controls.StackPanel> Schaltflächen auf dem platziert <xref:System.Windows.Controls.InkCanvas> .</span><span class="sxs-lookup"><span data-stu-id="3d226-142">Notice how the <xref:System.Windows.Controls.StackPanel> places the buttons on top of the <xref:System.Windows.Controls.InkCanvas>.</span></span> <span data-ttu-id="3d226-143">Wenn Sie versuchen, über den oberen Rand der Schaltflächen zu übergeben, <xref:System.Windows.Controls.InkCanvas> sammelt und rendert die frei Hand Eingaben hinter den Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="3d226-143">If you try to ink over the top of the buttons, the <xref:System.Windows.Controls.InkCanvas> collects and renders the ink behind the buttons.</span></span> <span data-ttu-id="3d226-144">Dies liegt daran, dass die Schaltflächen gleich geordnete Elemente von sind und nicht untergeordnete Elemente <xref:System.Windows.Controls.InkCanvas> .</span><span class="sxs-lookup"><span data-stu-id="3d226-144">This is because the buttons are siblings of the <xref:System.Windows.Controls.InkCanvas> as opposed to children.</span></span> <span data-ttu-id="3d226-145">Außerdem sind die Schaltflächen in der Z-Reihenfolge weiter oben, weshalb die Freihandeingaben dahinter gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="3d226-145">Also, the buttons are higher in the z-order, so the ink is rendered behind them.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d226-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d226-146">See also</span></span>

- <xref:System.Windows.Ink.DrawingAttributes>
- <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A>
- <xref:System.Windows.Ink>
