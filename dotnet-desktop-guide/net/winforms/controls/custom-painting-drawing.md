---
title: Benutzerdefinierte Darstellung für Steuerelemente
description: Hier erfahren Sie, wie Sie die Darstellung eines Steuerelements über die OnPaint-Methode und das Paint-Ereignis in Windows Forms für .NET anpassen.
ms.date: 10/26/2020
ms.topic: overview
dev_langs:
- csharp
- vb
f1_keywords:
- OnPaint
helpviewer_keywords:
- controls [Windows Forms], user controls
- controls [Windows Forms], types of
- composite controls [Windows Forms]
- extended controls [Windows Forms]
- controls [Windows Forms], extended
- user controls [Windows Forms]
- custom controls [Windows Forms]
- controls [Windows Forms], composite
ms.openlocfilehash: 8d9775c02addb68cc962cdc2e4bf2d1baa6ab2a1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942088"
---
# <a name="painting-and-drawing-on-controls-windows-forms-net"></a><span data-ttu-id="fd82b-103">Zeichnen eines Steuerelements (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="fd82b-103">Painting and drawing on controls (Windows Forms .NET)</span></span>

<span data-ttu-id="fd82b-104">Das benutzerdefinierte Zeichnen von Steuerelementen ist eine der vielen komplizierten Aufgaben, die durch Windows Forms vereinfacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd82b-104">Custom painting of controls is one of the many complicated tasks made easy by Windows Forms.</span></span> <span data-ttu-id="fd82b-105">Wenn ein benutzerdefiniertes Steuerelement erstellt wird, gibt es viele Optionen, wie Sie die grafische Darstellung Ihres Steuerelements beeinflussen können.</span><span class="sxs-lookup"><span data-stu-id="fd82b-105">When authoring a custom control, you have many options available to handle your control's graphical appearance.</span></span> <span data-ttu-id="fd82b-106">Wenn Sie ein [benutzerdefiniertes Steuerelement](custom.md#custom-controls) erstellen, also ein Steuerelement, das von <xref:System.Windows.Forms.Control> erbt, müssen Sie Code bereitstellen, um seine grafische Darstellung zu rendern.</span><span class="sxs-lookup"><span data-stu-id="fd82b-106">If you're authoring a [custom control](custom.md#custom-controls), that is, a control that inherits from <xref:System.Windows.Forms.Control>, you must provide code to render its graphical representation.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

<span data-ttu-id="fd82b-107">Wenn Sie ein [zusammengesetztes Steuerelement](custom.md#composite-controls) erstellen, also ein Steuerelement, das von <xref:System.Windows.Forms.UserControl> oder einem der vorhandenen Windows Forms-Steuerelemente erbt, können Sie die grafische Standarddarstellung überschreiben und eigenen Grafikcode bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fd82b-107">If you're creating a [composite control](custom.md#composite-controls), that is a control that inherits from <xref:System.Windows.Forms.UserControl> or one of the existing Windows Forms controls, you may override the standard graphical representation and provide your own graphics code.</span></span>

<span data-ttu-id="fd82b-108">Wenn Sie benutzerdefiniertes Rendering für ein vorhandenes Steuerelement anwenden möchten, ohne ein neues Steuerelement zu erstellen, sind die verfügbaren Optionen eingeschränkter.</span><span class="sxs-lookup"><span data-stu-id="fd82b-108">If you want to provide custom rendering for an existing control without creating a new control, your options become more limited.</span></span> <span data-ttu-id="fd82b-109">Dennoch gibt es weiterhin ein große Bandbreite grafischer Möglichkeiten für Ihre Steuerelemente und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="fd82b-109">However, there are still a wide range of graphical possibilities for your controls and applications.</span></span>

<span data-ttu-id="fd82b-110">Beim Rendern von Steuerelementen sind die folgenden Elemente beteiligt:</span><span class="sxs-lookup"><span data-stu-id="fd82b-110">The following elements are involved in control rendering:</span></span>

- <span data-ttu-id="fd82b-111">Die von der Basisklasse <xref:System.Windows.Forms.Control?displayProperty=nameWithType> bereitgestellte Funktion zum Zeichnen</span><span class="sxs-lookup"><span data-stu-id="fd82b-111">The drawing functionality provided by the base class <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span>
- <span data-ttu-id="fd82b-112">Die essentiellen Elemente der GDI-Grafikbibliothek</span><span class="sxs-lookup"><span data-stu-id="fd82b-112">The essential elements of the GDI graphics library.</span></span>
- <span data-ttu-id="fd82b-113">Die Geometrie der Zeichnungsregion</span><span class="sxs-lookup"><span data-stu-id="fd82b-113">The geometry of the drawing region.</span></span>
- <span data-ttu-id="fd82b-114">Die Prozedur für das Freigeben von Grafikressourcen</span><span class="sxs-lookup"><span data-stu-id="fd82b-114">The procedure for freeing graphics resources.</span></span>

## <a name="drawing-provided-by-control"></a><span data-ttu-id="fd82b-115">Vom Steuerelement bereitgestellte Funktionen zum Zeichnen</span><span class="sxs-lookup"><span data-stu-id="fd82b-115">Drawing provided by control</span></span>

<span data-ttu-id="fd82b-116">Die Basisklasse <xref:System.Windows.Forms.Control> stellt Funktionen zum Zeichnen über das dazugehörige <xref:System.Windows.Forms.Control.Paint>-Ereignis bereit.</span><span class="sxs-lookup"><span data-stu-id="fd82b-116">The base class <xref:System.Windows.Forms.Control> provides drawing functionality through its <xref:System.Windows.Forms.Control.Paint> event.</span></span> <span data-ttu-id="fd82b-117">Ein Steuerelement löst das <xref:System.Windows.Forms.Control.Paint>-Ereignis aus, sobald die dazugehörige Anzeige aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="fd82b-117">A control raises the <xref:System.Windows.Forms.Control.Paint> event whenever it needs to update its display.</span></span> <span data-ttu-id="fd82b-118">Weitere Informationen zu Ereignissen in .NET finden Sie unter [Behandeln und Auslösen von Ereignissen](/dotnet/standard/events/index).</span><span class="sxs-lookup"><span data-stu-id="fd82b-118">For more information about events in the .NET, see [Handling and raising events](/dotnet/standard/events/index).</span></span>

<span data-ttu-id="fd82b-119">Die Ereignisdatenklasse für das <xref:System.Windows.Forms.Control.Paint>-Ereignis, <xref:System.Windows.Forms.PaintEventArgs>, enthält die Daten, die für das Zeichnen eines Steuerelements erforderlich sind – ein Handle für ein Grafikobjekt und ein Rechteck, das die Region darstellt, in der gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="fd82b-119">The event data class for the <xref:System.Windows.Forms.Control.Paint> event, <xref:System.Windows.Forms.PaintEventArgs>, holds the data needed for drawing a control - a handle to a graphics object and a rectangle that represents the region to draw in.</span></span>

```csharp
public class PaintEventArgs : EventArgs, IDisposable
{

    public System.Drawing.Rectangle ClipRectangle {get;}
    public System.Drawing.Graphics Graphics {get;}

    // Other properties and methods.
}
```

```vb
Public Class PaintEventArgs
    Inherits EventArgs
    Implements IDisposable

    Public ReadOnly Property ClipRectangle As System.Drawing.Rectangle
    Public ReadOnly Property Graphics As System.Drawing.Graphics

    ' Other properties and methods.
End Class
```

<span data-ttu-id="fd82b-120"><xref:System.Drawing.Graphics> ist eine verwaltete Klasse, die die Funktion zum Zeichnen kapselt. Weitere Informationen finden Sie in der GDI-Diskussion später in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="fd82b-120"><xref:System.Drawing.Graphics> is a managed class that encapsulates drawing functionality, as described in the discussion of GDI later in this article.</span></span> <span data-ttu-id="fd82b-121">Bei <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> handelt es sich um eine Instanz der <xref:System.Drawing.Rectangle>-Struktur. Hierdurch wird der verfügbare Bereich definiert, in dem ein Steuerelement zeichnen kann.</span><span class="sxs-lookup"><span data-stu-id="fd82b-121">The <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> is an instance of the <xref:System.Drawing.Rectangle> structure and defines the available area in which a control can draw.</span></span> <span data-ttu-id="fd82b-122">Der Entwickler eines Steuerelements kann <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> mit der <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A>-Eigenschaft eines Steuerelements berechnen. Weitere Informationen finde Sie in der Geometriediskussion später in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="fd82b-122">A control developer can compute the <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> using the <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> property of a control, as described in the discussion of geometry later in this article.</span></span>

### <a name="onpaint"></a><span data-ttu-id="fd82b-123">OnPaint</span><span class="sxs-lookup"><span data-stu-id="fd82b-123">OnPaint</span></span>

<span data-ttu-id="fd82b-124">Ein Steuerelement muss Renderinglogik bereitstellen, indem die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode überschrieben wird, die es von <xref:System.Windows.Forms.Control> erbt.</span><span class="sxs-lookup"><span data-stu-id="fd82b-124">A control must provide rendering logic by overriding the <xref:System.Windows.Forms.Control.OnPaint%2A> method that it inherits from <xref:System.Windows.Forms.Control>.</span></span> <span data-ttu-id="fd82b-125"><xref:System.Windows.Forms.Control.OnPaint%2A> erhält über die übergebenen Eigenschaften <xref:System.Drawing.Design.PaintValueEventArgs.Graphics%2A> und <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> der Instanz <xref:System.Windows.Forms.PaintEventArgs> Zugriff auf ein Grafikobjekt und ein Rechteck, in dem gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd82b-125"><xref:System.Windows.Forms.Control.OnPaint%2A> gets access to a graphics object and a rectangle to draw in through the <xref:System.Drawing.Design.PaintValueEventArgs.Graphics%2A> and the <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> properties of the <xref:System.Windows.Forms.PaintEventArgs> instance passed to it.</span></span>

<span data-ttu-id="fd82b-126">Im folgenden Code wird der `System.Drawing`-Namespace verwendet:</span><span class="sxs-lookup"><span data-stu-id="fd82b-126">The following code uses the `System.Drawing` namespace:</span></span>

:::code language="csharp" source="./snippets/custom-painting-drawing/cs/UserControl1.cs" id="OnPaintMethod":::

:::code language="vb" source="./snippets/custom-painting-drawing/vb/UserControl1.vb" id="OnPaintMethod":::

<span data-ttu-id="fd82b-127">Die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode der <xref:System.Windows.Forms.Control>-Basisklasse implementiert keine Zeichnungsfunktionen, ruft jedoch die Ereignisdelegaten auf, die für das <xref:System.Windows.Forms.Control.Paint>-Ereignis registriert sind.</span><span class="sxs-lookup"><span data-stu-id="fd82b-127">The <xref:System.Windows.Forms.Control.OnPaint%2A> method of the base <xref:System.Windows.Forms.Control> class doesn't implement any drawing functionality but merely invokes the event delegates that are registered with the <xref:System.Windows.Forms.Control.Paint> event.</span></span> <span data-ttu-id="fd82b-128">Wenn Sie <xref:System.Windows.Forms.Control.OnPaint%2A> überschreiben, sollten Sie in der Regel die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode der Basisklasse aufrufen, damit registrierte Delegaten das <xref:System.Windows.Forms.Control.Paint>-Ereignis empfangen.</span><span class="sxs-lookup"><span data-stu-id="fd82b-128">When you override <xref:System.Windows.Forms.Control.OnPaint%2A>, you should typically invoke the <xref:System.Windows.Forms.Control.OnPaint%2A> method of the base class so that registered delegates receive the <xref:System.Windows.Forms.Control.Paint> event.</span></span> <span data-ttu-id="fd82b-129">Steuerelemente, deren gesamte Oberfläche gezeichnet wird, sollten nicht die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode der Basisklasse aufrufen, da dies zu Flimmern führen kann.</span><span class="sxs-lookup"><span data-stu-id="fd82b-129">However, controls that paint their entire surface shouldn't invoke the base class's <xref:System.Windows.Forms.Control.OnPaint%2A>, as this introduces flicker.</span></span>

> [!NOTE]
> <span data-ttu-id="fd82b-130">Rufen Sie <xref:System.Windows.Forms.Control.OnPaint%2A> nicht direkt in Ihrem Steuerelement auf. Rufen Sie stattdessen die <xref:System.Windows.Forms.Control.Invalidate%2A>-Methode (von <xref:System.Windows.Forms.Control> geerbt) oder eine andere Methode auf, die <xref:System.Windows.Forms.Control.Invalidate%2A> aufruft.</span><span class="sxs-lookup"><span data-stu-id="fd82b-130">Don't invoke <xref:System.Windows.Forms.Control.OnPaint%2A> directly from your control; instead, invoke the <xref:System.Windows.Forms.Control.Invalidate%2A> method (inherited from <xref:System.Windows.Forms.Control>) or some other method that invokes <xref:System.Windows.Forms.Control.Invalidate%2A>.</span></span> <span data-ttu-id="fd82b-131">Die <xref:System.Windows.Forms.Control.Invalidate%2A>-Methode wiederum ruft <xref:System.Windows.Forms.Control.OnPaint%2A> auf.</span><span class="sxs-lookup"><span data-stu-id="fd82b-131">The <xref:System.Windows.Forms.Control.Invalidate%2A> method in turn invokes <xref:System.Windows.Forms.Control.OnPaint%2A>.</span></span> <span data-ttu-id="fd82b-132">Die <xref:System.Windows.Forms.Control.Invalidate%2A>-Methode wird überladen und zeichnet je nach für <xref:System.Windows.Forms.Control.Invalidate%2A> `e` bereitgestellten Argumenten entweder Teile oder den gesamten Bildschirmbereich neu.</span><span class="sxs-lookup"><span data-stu-id="fd82b-132">The <xref:System.Windows.Forms.Control.Invalidate%2A> method is overloaded, and, depending on the arguments supplied to <xref:System.Windows.Forms.Control.Invalidate%2A> `e`, redraws either some or all of its screen area.</span></span>

<span data-ttu-id="fd82b-133">Der Code in der <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode Ihres Steuerelements wird ausgeführt, wenn das Steuerelement erstmalig gezeichnet wird, und bei jeder Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="fd82b-133">The code in the <xref:System.Windows.Forms.Control.OnPaint%2A> method of your control will execute when the control is first drawn, and whenever it is refreshed.</span></span> <span data-ttu-id="fd82b-134">Damit Ihr Steuerelement bei jeder Größenanpassung neu gezeichnet wird, fügen Sie die folgende Zeile im Konstruktor Ihres Steuerelements hinzu:</span><span class="sxs-lookup"><span data-stu-id="fd82b-134">To ensure that your control is redrawn every time it is resized, add the following line to the constructor of your control:</span></span>

```csharp
SetStyle(ControlStyles.ResizeRedraw, true);
```

```vb
SetStyle(ControlStyles.ResizeRedraw, True)
```

### <a name="onpaintbackground"></a><span data-ttu-id="fd82b-135">OnPaintBackground</span><span class="sxs-lookup"><span data-stu-id="fd82b-135">OnPaintBackground</span></span>

<span data-ttu-id="fd82b-136">Die <xref:System.Windows.Forms.Control>-Basisklasse definiert eine weitere Methode, die hilfreich für das Zeichnen ist: die <xref:System.Windows.Forms.Control.OnPaintBackground%2A>-Methode.</span><span class="sxs-lookup"><span data-stu-id="fd82b-136">The base <xref:System.Windows.Forms.Control> class defines another method that is useful for drawing, the <xref:System.Windows.Forms.Control.OnPaintBackground%2A> method.</span></span>

```csharp
protected virtual void OnPaintBackground(PaintEventArgs e);
```

```vb
Protected Overridable Sub OnPaintBackground(e As PaintEventArgs)
```

<span data-ttu-id="fd82b-137"><xref:System.Windows.Forms.Control.OnPaintBackground%2A> zeichnet den Hintergrund (und so auch die Form) des Fensters. Dies erfolgt sehr schnell. <xref:System.Windows.Forms.Control.OnPaint%2A> hingegen zeichnet die Details und ist deshalb möglicherweise langsamer, da einzelne Zeichnungsanforderungen in ein <xref:System.Windows.Forms.Control.Paint>-Ereignis kombiniert werden, das alle Bereiche abdeckt, die neu gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fd82b-137"><xref:System.Windows.Forms.Control.OnPaintBackground%2A> paints the background (and in that way, the shape) of the window and is guaranteed to be fast, while <xref:System.Windows.Forms.Control.OnPaint%2A> paints the details and might be slower because individual paint requests are combined into one <xref:System.Windows.Forms.Control.Paint> event that covers all areas that have to be redrawn.</span></span> <span data-ttu-id="fd82b-138">Sie sollten <xref:System.Windows.Forms.Control.OnPaintBackground%2A> aufrufen, wenn Sie beispielsweise ein Hintergrund mit Farbverlauf für Ihr Steuerelement zeichnen möchten.</span><span class="sxs-lookup"><span data-stu-id="fd82b-138">You might want to invoke the <xref:System.Windows.Forms.Control.OnPaintBackground%2A> if, for instance, you want to draw a gradient-colored background for your control.</span></span>

<span data-ttu-id="fd82b-139">Während <xref:System.Windows.Forms.Control.OnPaintBackground%2A> eine ereignisähnliche Bezeichnung aufweist und dasselbe Argument wie die `OnPaint`-Methode annimmt, handelt es sich bei `OnPaintBackground` um keine tatsächliche Ereignismethode.</span><span class="sxs-lookup"><span data-stu-id="fd82b-139">While <xref:System.Windows.Forms.Control.OnPaintBackground%2A> has an event-like nomenclature and takes the same argument as the `OnPaint` method, `OnPaintBackground` is not a true event method.</span></span> <span data-ttu-id="fd82b-140">Es gibt kein `PaintBackground`-Ereignis, und `OnPaintBackground` ruft keine Ereignisdelegaten auf.</span><span class="sxs-lookup"><span data-stu-id="fd82b-140">There is no `PaintBackground` event and `OnPaintBackground` doesn't invoke event delegates.</span></span> <span data-ttu-id="fd82b-141">Wenn die `OnPaintBackground`-Methode überschrieben wird, ist keine abgeleitete Klasse erforderlich, um die `OnPaintBackground`-Methode der dazugehörigen Basisklasse aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd82b-141">When overriding the `OnPaintBackground` method, a derived class is not required to invoke the `OnPaintBackground` method of its base class.</span></span>

## <a name="gdi-basics"></a><span data-ttu-id="fd82b-142">GDI+-Grundlagen</span><span class="sxs-lookup"><span data-stu-id="fd82b-142">GDI+ Basics</span></span>

<span data-ttu-id="fd82b-143">Die <xref:System.Drawing.Graphics>-Klasse bietet Methoden für das Zeichnen verschiedener Formen wie Kreise, Dreiecke, Bögen und Ellipsen sowie Methoden für das Anzeigen von Text.</span><span class="sxs-lookup"><span data-stu-id="fd82b-143">The <xref:System.Drawing.Graphics> class provides methods for drawing various shapes such as circles, triangles, arcs, and ellipses, and methods for displaying text.</span></span> <span data-ttu-id="fd82b-144">Der <xref:System.Drawing?displayProperty=nameWithType>-Namespace enthält Namespaces und Klassen, die grafische Elemente wie Formen (z. B. Kreise, Rechtecke und Bögen), Farben, Schriftarten und Pinsel kapseln.</span><span class="sxs-lookup"><span data-stu-id="fd82b-144">The <xref:System.Drawing?displayProperty=nameWithType> namespace contains namespaces and classes that encapsulate graphics elements such as shapes (circles, rectangles, arcs, and others), colors, fonts, brushes, and so on.</span></span><!-- TODO  For more information about GDI, see [Using Managed Graphics Classes](../advanced/using-managed-graphics-classes.md).-->

## <a name="geometry-of-the-drawing-region"></a><span data-ttu-id="fd82b-145">Geometrie der Zeichnungsregion</span><span class="sxs-lookup"><span data-stu-id="fd82b-145">Geometry of the Drawing Region</span></span>

<span data-ttu-id="fd82b-146">Die <xref:System.Windows.Forms.Control.ClientRectangle%2A>-Eigenschaft eines Steuerelements gibt die rechteckige Region an, die für das Steuerelement auf der Anzeige für den Benutzer verfügbar ist. Die <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A>-Eigenschaft von <xref:System.Windows.Forms.PaintEventArgs> gibt dahingegen den Bereich an, der gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="fd82b-146">The <xref:System.Windows.Forms.Control.ClientRectangle%2A> property of a control specifies the rectangular region available to the control on the user's screen, while the <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> property of <xref:System.Windows.Forms.PaintEventArgs> specifies the area that is painted.</span></span> <span data-ttu-id="fd82b-147">Ein Steuerelement muss möglicherweise nur einen Teil des verfügbaren Bereichs zeichnen, z. B. wenn ein kleiner Bereich der Anzeige des Steuerelements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fd82b-147">A control might need to paint only a portion of its available area, as is the case when a small section of the control's display changes.</span></span> <span data-ttu-id="fd82b-148">In solchen Situationen muss der Entwickler eines Steuerelements das tatsächliche Rechteck berechnen, in dem gezeichnet werden soll, und dieses an <xref:System.Windows.Forms.Control.Invalidate%2A> übergeben.</span><span class="sxs-lookup"><span data-stu-id="fd82b-148">In those situations, a control developer must compute the actual rectangle to draw in and pass that to <xref:System.Windows.Forms.Control.Invalidate%2A>.</span></span> <span data-ttu-id="fd82b-149">Die überladenen Versionen von <xref:System.Windows.Forms.Control.Invalidate%2A>, die <xref:System.Drawing.Rectangle> oder <xref:System.Drawing.Region> als Argument akzeptieren, verwenden dieses Argument, um die <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A>-Eigenschaft von <xref:System.Windows.Forms.PaintEventArgs> zu generieren.</span><span class="sxs-lookup"><span data-stu-id="fd82b-149">The overloaded versions of <xref:System.Windows.Forms.Control.Invalidate%2A> that take a <xref:System.Drawing.Rectangle> or <xref:System.Drawing.Region> as an argument use that argument to generate the <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> property of <xref:System.Windows.Forms.PaintEventArgs>.</span></span>

## <a name="freeing-graphics-resources"></a><span data-ttu-id="fd82b-150">Freigeben von Grafikressourcen</span><span class="sxs-lookup"><span data-stu-id="fd82b-150">Freeing Graphics Resources</span></span>

<span data-ttu-id="fd82b-151">Grafikobjekte sind teuer, da sie Systemressourcen verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd82b-151">Graphics objects are expensive because they use system resources.</span></span> <span data-ttu-id="fd82b-152">Zu solchen Objekten gehören Instanzen der <xref:System.Drawing.Graphics?displayProperty=nameWithType>-Klasse und Instanzen von <xref:System.Drawing.Brush?displayProperty=nameWithType>, <xref:System.Drawing.Pen?displayProperty=nameWithType> sowie weitere Grafikklassen.</span><span class="sxs-lookup"><span data-stu-id="fd82b-152">Such objects include instances of the <xref:System.Drawing.Graphics?displayProperty=nameWithType> class and instances of <xref:System.Drawing.Brush?displayProperty=nameWithType>, <xref:System.Drawing.Pen?displayProperty=nameWithType>, and other graphics classes.</span></span> <span data-ttu-id="fd82b-153">Es ist wichtig, dass Sie nur eine Grafikressource zeichnen, wenn Sie eine benötigen, und dass Sie sie freigeben, sobald Sie die Verwendung beendet haben.</span><span class="sxs-lookup"><span data-stu-id="fd82b-153">It's important that you create a graphics resource only when you need it and release it soon as you're finished using it.</span></span> <span data-ttu-id="fd82b-154">Wenn Sie eine Instanz eines Typs erstellen, der die <xref:System.IDisposable>-Schnittstelle implementiert, rufen Sie die dazugehörige <xref:System.IDisposable.Dispose%2A>-Methode auf, sobald Sie das Freigeben der Ressourcen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="fd82b-154">If you create an instance of a type that implements the <xref:System.IDisposable> interface, call its <xref:System.IDisposable.Dispose%2A> method when you're finished with it to free resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd82b-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd82b-155">See also</span></span>

- [<span data-ttu-id="fd82b-156">Arten von benutzerdefinierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="fd82b-156">Types of custom controls</span></span>](custom.md)
