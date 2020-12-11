---
title: Steuerelemente mit integrierter Ownerdrawing-Unterstützung
ms.date: 03/30/2017
ms.topic: overview
helpviewer_keywords:
- drawing [Windows Forms], owner
- drawing [Windows Forms], custom
- controls [Windows Forms], changing appearance
- custom drawing
- owner drawing
ms.assetid: 3823d01e-9610-43e6-864d-99f9b7c2b351
ms.openlocfilehash: a3c7b9eb2b7b19c8fe57cc656df64d0d0fdc4fdb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972219"
---
# <a name="controls-with-built-in-owner-drawing-support"></a><span data-ttu-id="c3c8e-102">Steuerelemente mit integrierter Ownerdrawing-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="c3c8e-102">Controls with Built-In Owner-Drawing Support</span></span>
<span data-ttu-id="c3c8e-103">Ownerdrawing in Windows Forms, das auch als benutzerdefiniertes Zeichnen bezeichnet, ist ein Verfahren zum Ändern der Darstellung bestimmter Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-103">Owner drawing in Windows Forms, which is also known as custom drawing, is a technique for changing the visual appearance of certain controls.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c3c8e-104">Mit dem Wort "Steuerelement" in diesem Thema werden Klassen gemeint, die von oder abgeleitet werden <xref:System.Windows.Forms.Control> <xref:System.ComponentModel.Component> .</span><span class="sxs-lookup"><span data-stu-id="c3c8e-104">The word "control" in this topic is used to mean classes that derive from either <xref:System.Windows.Forms.Control> or <xref:System.ComponentModel.Component>.</span></span>  
  
 <span data-ttu-id="c3c8e-105">In der Regel verarbeitet Windows das Zeichnen automatisch mithilfe von Eigenschafts Einstellungen wie z <xref:System.Windows.Forms.Control.BackColor%2A> . b., um die Darstellung eines Steuer Elements zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-105">Typically, Windows handles painting automatically by using property settings such as <xref:System.Windows.Forms.Control.BackColor%2A> to determine the appearance of a control.</span></span> <span data-ttu-id="c3c8e-106">Beim Ownerdrawing übernehmen Sie das Zeichnen und können Darstellungselemente ändern, die nicht mithilfe von Eigenschaften angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-106">With owner drawing, you take over the painting process, changing elements of appearance that are not available by using properties.</span></span> <span data-ttu-id="c3c8e-107">Beispielsweise kann bei zahlreichen Steuerelementen die Farbe des angezeigten Textes festgelegt werden. Dabei ist die Anzeige jedoch auf eine Farbe beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-107">For example, many controls let you set the color of the text that is displayed, but you are limited to a single color.</span></span> <span data-ttu-id="c3c8e-108">Das Ownerdrawing bietet beispielsweise die Möglichkeit, einen Teil des Textes schwarz und den anderen rot anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-108">Owner drawing enables you to do things like display part of the text in black and part in red.</span></span>  
  
 <span data-ttu-id="c3c8e-109">In der Praxis ähnelt Ownerdrawing dem Zeichnen von Grafiken auf einem Formular.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-109">In practice, owner drawing is similar to drawing graphics on a form.</span></span> <span data-ttu-id="c3c8e-110">Sie können z. b. Grafik Methoden in einem Handler für das-Ereignis des Formulars verwenden, <xref:System.Windows.Forms.Control.Paint> um ein Steuerelement zu emulieren `ListBox` , aber Sie müssen eigenen Code schreiben, um die gesamte Benutzerinteraktion zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-110">For example, you could use graphics methods in a handler for the form's <xref:System.Windows.Forms.Control.Paint> event to emulate a `ListBox` control, but you would have to write your own code to handle all user interaction.</span></span> <span data-ttu-id="c3c8e-111">Beim Ownerdrawing verwendet das Steuerelement den von Ihnen geschriebenen Code, um den Inhalt zu zeichnen, behält im Übrigen aber seine gesamte systeminterne Funktionalität bei.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-111">With owner drawing, the control uses your code to draw its contents but otherwise retains all its intrinsic capabilities.</span></span> <span data-ttu-id="c3c8e-112">Sie können Grafikmethoden zum Zeichnen der einzelnen Elemente im Steuerelement oder zum Anpassen einiger Aspekte einzelner Elemente verwenden, während für andere Aspekte einzelner Elemente wiederum die Standarddarstellung übernommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-112">You can use graphics methods to draw each item in the control or to customize some aspects of each item while you use the default appearance for other aspects of each item.</span></span>  
  
## <a name="owner-drawing-in-windows-forms-controls"></a><span data-ttu-id="c3c8e-113">Ownerdrawing in Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="c3c8e-113">Owner Drawing in Windows Forms Controls</span></span>  
 <span data-ttu-id="c3c8e-114">Um Ownerdrawing in Steuerelementen auszuführen, die diese Art des Zeichnens unterstützen, legen Sie normalerweise eine Eigenschaft fest und behandeln mindestens ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-114">To perform owner drawing in controls that support it, you will typically set one property and handle one or more events.</span></span>  
  
 <span data-ttu-id="c3c8e-115">Die meisten Steuerelemente mit Ownerdrawing-Unterstützung verfügen über die `OwnerDraw`-Eigenschaft oder `DrawMode`-Eigenschaft, die angibt, ob das Steuerelement eines oder mehrere zeichnungsbezogene Ereignisse auslöst, sobald es gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-115">Most controls that support owner drawing have an `OwnerDraw` or `DrawMode` property that indicates whether the control will raise its drawing-related event or events when it paints itself.</span></span>  
  
 <span data-ttu-id="c3c8e-116">Zu den Steuerelementen, die keine `OwnerDraw`-Eigenschaft oder `DrawMode`-Eigenschaft aufweisen, gehört das `DataGridView`-Steuerelement, das automatisch ausgelöste Zeichnungsereignisse bereitstellt, sowie das `ToolStrip`-Steuerelement, das unter Verwendung einer externen Renderklasse gezeichnet wird, die eigene zeichnungsbezogene Ereignisse aufweist.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-116">Controls that do not have an `OwnerDraw` or `DrawMode` property include the `DataGridView` control, which provides drawing events that occur automatically, and the `ToolStrip` control, which is drawn using an external rendering class that has its own drawing-related events.</span></span>  
  
 <span data-ttu-id="c3c8e-117">Es stehen viele verschiedene Arten von Zeichnungsereignissen zur Verfügung. Ein typisches Zeichnungsereignis tritt jedoch auf, wenn ein einzelnes Element innerhalb eines Steuerelements gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-117">There are many different kinds of drawing events, but a typical drawing event occurs in order to draw a single item within a control.</span></span> <span data-ttu-id="c3c8e-118">Der Ereignishandler empfängt ein `EventArgs`-Objekt mit Informationen zum gezeichneten Element sowie zu den Tools, die zum Zeichnen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-118">The event handler receives an `EventArgs` object that contains information about the item being drawn and tools you can use to draw it.</span></span> <span data-ttu-id="c3c8e-119">Dieses Objekt enthält z. b. in der Regel die Indexnummer des Elements in der übergeordneten Auflistung, ein <xref:System.Drawing.Rectangle> -Objekt, das die Anzeige Grenzen des Elements angibt, und ein- <xref:System.Drawing.Graphics> Objekt zum Aufrufen von Paint-Methoden.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-119">For example, this object typically contains the item's index number within its parent collection, a <xref:System.Drawing.Rectangle> that indicates the item's display boundaries, and a <xref:System.Drawing.Graphics> object for calling paint methods.</span></span> <span data-ttu-id="c3c8e-120">Bei einigen Ereignissen umfasst das `EventArgs`-Objekt zusätzliche Informationen zum Element sowie zu den Methoden, die aufgerufen werden können, um einige Aspekte des Elements in der Standarddarstellung zu zeichnen, z. B. den Hintergrund oder ein Fokusrechteck.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-120">For some events, the `EventArgs` object provides additional information about the item and methods that you can call to paint some aspects of the item by default, such as the background or a focus rectangle.</span></span>  
  
 <span data-ttu-id="c3c8e-121">Zum Erstellen eines wiederverwendbaren Steuerelements, das Ownerdrawing-Anpassungen enthält, erstellen Sie eine neue Klasse, die von einer Steuerelementklasse mit Ownerdrawing-Unterstützung abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-121">To create a reusable control that contains your owner-drawn customizations, create a new class that derives from a control class that supports owner drawing.</span></span> <span data-ttu-id="c3c8e-122">Anstatt Zeichnungsereignisse zu behandeln, sollten Sie Ownerdrawing-Code in Überschreibungen für mindestens eine geeignete `On`*EventName*-Methode in der neuen Klasse einfügen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-122">Rather than handling drawing events, include your owner-drawing code in overrides for the appropriate `On`*EventName* method or methods in the new class.</span></span> <span data-ttu-id="c3c8e-123">Stellen Sie in diesem Fall sicher, dass die `On`*EventName*-Methoden der Basisklasse aufgerufen werden, damit Benutzer des Steuerelements Ownerdrawing-Ereignisse behandeln und weitere Anpassungen vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-123">Make sure that you call the base class `On`*EventName* method or methods in this case so that users of your control can handle owner-drawing events and provide additional customization.</span></span>  
  
 <span data-ttu-id="c3c8e-124">Die folgenden Windows Forms-Steuerelemente unterstützen Ownerdrawing in allen Versionen von .NET Framework:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-124">The following Windows Forms controls support owner drawing in all versions of the .NET Framework:</span></span>  
  
- <xref:System.Windows.Forms.ListBox>  
  
- <xref:System.Windows.Forms.ComboBox>  
  
- <span data-ttu-id="c3c8e-125"><xref:System.Windows.Forms.MenuItem> (verwendet von <xref:System.Windows.Forms.MainMenu> und <xref:System.Windows.Forms.ContextMenu> )</span><span class="sxs-lookup"><span data-stu-id="c3c8e-125"><xref:System.Windows.Forms.MenuItem> (used by <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu>)</span></span>  
  
- <xref:System.Windows.Forms.TabControl>  
  
 <span data-ttu-id="c3c8e-126">Die folgenden Steuerelemente unterstützen das Zeichnen von Besitzern nur in .NET Framework 2,0:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-126">The following controls support owner drawing only in .NET Framework 2.0:</span></span>  
  
- <xref:System.Windows.Forms.ToolTip>  
  
- <xref:System.Windows.Forms.ListView>  
  
- <xref:System.Windows.Forms.TreeView>  
  
 <span data-ttu-id="c3c8e-127">Die folgenden Steuerelemente unterstützen das Zeichnen von Besitzern und sind neu in .NET Framework 2,0:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-127">The following controls support owner drawing and are new in .NET Framework 2.0:</span></span>  
  
- <xref:System.Windows.Forms.DataGridView>  
  
- <xref:System.Windows.Forms.ToolStrip>  
  
 <span data-ttu-id="c3c8e-128">Die folgenden Abschnitte enthalten zusätzliche Details zu jedem dieser Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-128">The following sections provide additional details for each of these controls.</span></span>  
  
### <a name="listbox-and-combobox-controls"></a><span data-ttu-id="c3c8e-129">Die Steuerelemente ListBox und ComboBox</span><span class="sxs-lookup"><span data-stu-id="c3c8e-129">ListBox and ComboBox Controls</span></span>  
 <span data-ttu-id="c3c8e-130">Mit <xref:System.Windows.Forms.ListBox> den <xref:System.Windows.Forms.ComboBox> Steuerelementen und können Sie einzelne Elemente im Steuerelement entweder in einer Größe oder in unterschiedlichen Größen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-130">The <xref:System.Windows.Forms.ListBox> and <xref:System.Windows.Forms.ComboBox> controls enable you to draw individual items in the control either all in one size, or in varying sizes.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c3c8e-131">Obwohl das- <xref:System.Windows.Forms.CheckedListBox> Steuerelement vom-Steuerelement abgeleitet ist, wird das Zeichnen von <xref:System.Windows.Forms.ListBox> Besitzern nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-131">Although the <xref:System.Windows.Forms.CheckedListBox> control is derived from the <xref:System.Windows.Forms.ListBox> control, it does not support owner drawing.</span></span>  
  
 <span data-ttu-id="c3c8e-132">Um jedes Element in derselben Größe zu zeichnen, legen `DrawMode` Sie die-Eigenschaft auf fest <xref:System.Windows.Forms.DrawMode.OwnerDrawFixed> und behandeln das- `DrawItem` Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-132">To draw each item the same size, set the `DrawMode` property to <xref:System.Windows.Forms.DrawMode.OwnerDrawFixed> and handle the `DrawItem` event.</span></span>  
  
 <span data-ttu-id="c3c8e-133">Um jedes Element mit einer anderen Größe zu zeichnen, legen Sie die `DrawMode` -Eigenschaft auf fest <xref:System.Windows.Forms.DrawMode.OwnerDrawVariable> und behandeln sowohl das `MeasureItem` -als auch das- `DrawItem` Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-133">To draw each item using a different size, set the `DrawMode` property to <xref:System.Windows.Forms.DrawMode.OwnerDrawVariable> and handle both the `MeasureItem` and `DrawItem` events.</span></span> <span data-ttu-id="c3c8e-134">Mit dem `MeasureItem`-Ereignis können Sie die Größe eines Elements angeben, bevor das `DrawItem`-Ereignis für das jeweilige Element auftritt.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-134">The `MeasureItem` event lets you indicate the size of an item before the `DrawItem` event occurs for that item.</span></span>  
  
 <span data-ttu-id="c3c8e-135">Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-135">For more information, including code examples, see the following topics:</span></span>  
  
- <xref:System.Windows.Forms.ListBox.DrawMode%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ListBox.MeasureItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ListBox.DrawItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ComboBox.DrawMode%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ComboBox.MeasureItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ComboBox.DrawItem?displayProperty=nameWithType>  
  
- [<span data-ttu-id="c3c8e-136">Vorgehensweise: Erstellen von Text mit variabler Größe in einem ComboBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c3c8e-136">How to: Create Variable Sized Text in a ComboBox Control</span></span>](how-to-create-variable-sized-text-in-a-combobox-control.md)  
  
### <a name="menuitem-component"></a><span data-ttu-id="c3c8e-137">MenuItem-Komponente</span><span class="sxs-lookup"><span data-stu-id="c3c8e-137">MenuItem Component</span></span>  
 <span data-ttu-id="c3c8e-138">Die <xref:System.Windows.Forms.MenuItem> Komponente stellt ein einzelnes Menü Element in einer- <xref:System.Windows.Forms.MainMenu> oder- <xref:System.Windows.Forms.ContextMenu> Komponente dar.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-138">The <xref:System.Windows.Forms.MenuItem> component represents a single menu item in a <xref:System.Windows.Forms.MainMenu> or <xref:System.Windows.Forms.ContextMenu> component.</span></span>  
  
 <span data-ttu-id="c3c8e-139">Um einen zu zeichnen <xref:System.Windows.Forms.MenuItem> , legen `OwnerDraw` Sie seine-Eigenschaft auf fest `true` und behandeln das zugehörige- `DrawItem` Ereignis</span><span class="sxs-lookup"><span data-stu-id="c3c8e-139">To draw a <xref:System.Windows.Forms.MenuItem>, set its `OwnerDraw` property to `true` and handle its `DrawItem` event.</span></span> <span data-ttu-id="c3c8e-140">Um die Größe des Menüelements anzupassen, bevor das `DrawItem`-Ereignis auftritt, behandeln Sie das `MeasureItem`-Ereignis des Elements.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-140">To customize the size of the menu item before the `DrawItem` event occurs, handle the item's `MeasureItem` event.</span></span>  
  
 <span data-ttu-id="c3c8e-141">Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Referenzthemen:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-141">For more information, including code examples, see the following reference topics:</span></span>  
  
- <xref:System.Windows.Forms.MenuItem.OwnerDraw%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.MenuItem.DrawItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.MenuItem.MeasureItem?displayProperty=nameWithType>  
  
### <a name="tabcontrol-control"></a><span data-ttu-id="c3c8e-142">TabControl-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c3c8e-142">TabControl Control</span></span>  
 <span data-ttu-id="c3c8e-143">Das- <xref:System.Windows.Forms.TabControl> Steuerelement ermöglicht es Ihnen, einzelne Registerkarten im-Steuerelement zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-143">The <xref:System.Windows.Forms.TabControl> control enables you to draw individual tabs in the control.</span></span> <span data-ttu-id="c3c8e-144">Besitzer Zeichnung wirkt sich nur auf die Registerkarten aus; der <xref:System.Windows.Forms.TabPage> Inhalt ist nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-144">Owner drawing affects only the tabs; the <xref:System.Windows.Forms.TabPage> contents are not affected.</span></span>  
  
 <span data-ttu-id="c3c8e-145">Wenn Sie jede Registerkarte in einem zeichnen möchten <xref:System.Windows.Forms.TabControl> , legen `DrawMode` Sie die-Eigenschaft auf fest <xref:System.Windows.Forms.TabDrawMode.OwnerDrawFixed> und behandeln das- `DrawItem` Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-145">To draw each tab in a <xref:System.Windows.Forms.TabControl>, set the `DrawMode` property to <xref:System.Windows.Forms.TabDrawMode.OwnerDrawFixed> and handle the `DrawItem` event.</span></span> <span data-ttu-id="c3c8e-146">Dieses Ereignis tritt jeweils einmal für jede Registerkarte auf, jedoch nur dann, wenn die Registerkarte im Steuerelement sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-146">This event occurs once for each tab only when the tab is visible in the control.</span></span>  
  
 <span data-ttu-id="c3c8e-147">Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Referenzthemen:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-147">For more information, including code examples, see the following reference topics:</span></span>  
  
- <xref:System.Windows.Forms.TabControl.DrawMode%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.TabControl.DrawItem?displayProperty=nameWithType>  
  
### <a name="tooltip-component"></a><span data-ttu-id="c3c8e-148">ToolTip-Komponente</span><span class="sxs-lookup"><span data-stu-id="c3c8e-148">ToolTip Component</span></span>  
 <span data-ttu-id="c3c8e-149">Mit der- <xref:System.Windows.Forms.ToolTip> Komponente können Sie die gesamte QuickInfo zeichnen, wenn Sie angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-149">The <xref:System.Windows.Forms.ToolTip> component enables you to draw the entire ToolTip when it is displayed.</span></span>  
  
 <span data-ttu-id="c3c8e-150">Um einen zu zeichnen <xref:System.Windows.Forms.ToolTip> , legen `OwnerDraw` Sie seine-Eigenschaft auf fest `true` und behandeln das zugehörige- `Draw` Ereignis</span><span class="sxs-lookup"><span data-stu-id="c3c8e-150">To draw a <xref:System.Windows.Forms.ToolTip>, set its `OwnerDraw` property to `true` and handle its `Draw` event.</span></span> <span data-ttu-id="c3c8e-151">Um die Größe von <xref:System.Windows.Forms.ToolTip> vor dem Auftreten des `Draw` Ereignisses anzupassen, behandeln Sie das `Popup` -Ereignis, und legen Sie die- <xref:System.Windows.Forms.PopupEventArgs.ToolTipSize%2A> Eigenschaft im-Ereignishandler fest.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-151">To customize the size of the <xref:System.Windows.Forms.ToolTip> before the `Draw` event occurs, handle the `Popup` event and set the <xref:System.Windows.Forms.PopupEventArgs.ToolTipSize%2A> property in the event handler.</span></span>  
  
 <span data-ttu-id="c3c8e-152">Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Referenzthemen:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-152">For more information, including code examples, see the following reference topics:</span></span>  
  
- <xref:System.Windows.Forms.ToolTip.OwnerDraw%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ToolTip.Draw?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ToolTip.Popup?displayProperty=nameWithType>  
  
### <a name="listview-control"></a><span data-ttu-id="c3c8e-153">ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c3c8e-153">ListView Control</span></span>  
 <span data-ttu-id="c3c8e-154">Das- <xref:System.Windows.Forms.ListView> Steuerelement ermöglicht es Ihnen, einzelne Elemente, unter Elemente und Spaltenheader im-Steuerelement zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-154">The <xref:System.Windows.Forms.ListView> control enables you to draw individual items, subitems, and column headers in the control.</span></span>  
  
 <span data-ttu-id="c3c8e-155">Um Ownerdrawing im Steuerelement zu aktivieren, legen Sie die `OwnerDraw`-Eigenschaft `true` fest.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-155">To enable owner drawing in the control, set the `OwnerDraw` property to `true`.</span></span>  
  
 <span data-ttu-id="c3c8e-156">Um jedes Element im Steuerelement zu zeichnen, behandeln Sie das `DrawItem`-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-156">To draw each item in the control, handle the `DrawItem` event.</span></span>  
  
 <span data-ttu-id="c3c8e-157">Um jeden Unterelement-oder Spaltenheader im-Steuerelement zu zeichnen <xref:System.Windows.Forms.ListView.View%2A> , wenn die-Eigenschaft auf festgelegt ist <xref:System.Windows.Forms.View.Details> , behandeln Sie die `DrawSubItem` `DrawColumnHeader` Ereignisse und.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-157">To draw each subitem or column header in the control when the <xref:System.Windows.Forms.ListView.View%2A> property is set to <xref:System.Windows.Forms.View.Details>, handle the `DrawSubItem` and `DrawColumnHeader` events.</span></span>  
  
 <span data-ttu-id="c3c8e-158">Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Referenzthemen:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-158">For more information, including code examples, see the following reference topics:</span></span>  
  
- <xref:System.Windows.Forms.ListView.OwnerDraw%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ListView.DrawItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ListView.DrawSubItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ListView.DrawColumnHeader?displayProperty=nameWithType>  
  
### <a name="treeview-control"></a><span data-ttu-id="c3c8e-159">TreeView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c3c8e-159">TreeView Control</span></span>  
 <span data-ttu-id="c3c8e-160">Das- <xref:System.Windows.Forms.TreeView> Steuerelement ermöglicht es Ihnen, einzelne Knoten im-Steuerelement zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-160">The <xref:System.Windows.Forms.TreeView> control enables you to draw individual nodes in the control.</span></span>  
  
 <span data-ttu-id="c3c8e-161">Wenn Sie nur den in jedem Knoten angezeigten Text zeichnen möchten, legen Sie die `DrawMode` -Eigenschaft auf fest <xref:System.Windows.Forms.TreeViewDrawMode.OwnerDrawText> und behandeln das- `DrawNode` Ereignis, um den Text zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-161">To draw only the text displayed in each node, set the `DrawMode` property to <xref:System.Windows.Forms.TreeViewDrawMode.OwnerDrawText> and handle the `DrawNode` event to draw the text.</span></span>  
  
 <span data-ttu-id="c3c8e-162">Um alle Elemente der einzelnen Knoten zu zeichnen, legen `DrawMode` Sie die-Eigenschaft auf fest <xref:System.Windows.Forms.TreeViewDrawMode.OwnerDrawAll> und behandeln das- `DrawNode` Ereignis, um die Elemente zu zeichnen, die Sie benötigen, z. b. Text, Symbole, Kontrollkästchen, plus-und Minuszeichen sowie Zeilen, die die Knoten verbinden.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-162">To draw all elements of each node, set the `DrawMode` property to <xref:System.Windows.Forms.TreeViewDrawMode.OwnerDrawAll> and handle the `DrawNode` event to draw whichever elements you need, such as text, icons, check boxes, plus and minus signs, and lines connecting the nodes.</span></span>  
  
 <span data-ttu-id="c3c8e-163">Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Referenzthemen:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-163">For more information, including code examples, see the following reference topics:</span></span>  
  
- <xref:System.Windows.Forms.TreeView.DrawMode%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.TreeView.DrawNode?displayProperty=nameWithType>  
  
### <a name="datagridview-control"></a><span data-ttu-id="c3c8e-164">DataGridView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c3c8e-164">DataGridView Control</span></span>  
 <span data-ttu-id="c3c8e-165">Das <xref:System.Windows.Forms.DataGridView> -Steuerelement ermöglicht es Ihnen, einzelne Zellen und Zeilen im-Steuerelement zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-165">The <xref:System.Windows.Forms.DataGridView> control enables you to draw individual cells and rows in the control.</span></span>  
  
 <span data-ttu-id="c3c8e-166">Um einzelne Zellen zu zeichnen, behandeln Sie das `CellPainting`-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-166">To draw individual cells, handle the `CellPainting` event.</span></span>  
  
 <span data-ttu-id="c3c8e-167">Um einzelne Zeilen oder Zeilenelemente zu zeichnen, behandeln Sie das `RowPrePaint`- und/oder `RowPostPaint`-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-167">To draw individual rows or elements of rows, handle one or both of the `RowPrePaint` and `RowPostPaint` events.</span></span> <span data-ttu-id="c3c8e-168">Das `RowPrePaint`-Ereignis tritt vor dem Zeichnen der Zellen in einer Zeile und das `RowPostPaint`-Ereignis danach auf.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-168">The `RowPrePaint` event occurs before the cells in a row are painted, and the `RowPostPaint` event occurs after the cells are painted.</span></span> <span data-ttu-id="c3c8e-169">Sie können beide Ereignisse und das `CellPainting`-Ereignis behandeln, um den Zeilenhintergrund, einzelne Zellen sowie den Zeilenvordergrund separat zu zeichnen. Alternativ können Sie für bestimmte Elemente spezielle Anpassungen bereitstellen und für die übrigen Zeilenelemente die Standarddarstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-169">You can handle both events and the `CellPainting` event to paint row background, individual cells, and row foreground separately, or you can provide specific customizations where you need them and use the default display for other elements of the row.</span></span>  
  
 <span data-ttu-id="c3c8e-170">Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-170">For more information, including code examples, see the following topics:</span></span>  
  
- <xref:System.Windows.Forms.DataGridView.CellPainting>  
  
- <xref:System.Windows.Forms.DataGridView.RowPrePaint>  
  
- <xref:System.Windows.Forms.DataGridView.RowPostPaint>  
  
- [<span data-ttu-id="c3c8e-171">Gewusst wie: Anpassen der Darstellung von Zellen im DataGridView-Steuerelement von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c3c8e-171">How to: Customize the Appearance of Cells in the Windows Forms DataGridView Control</span></span>](customize-the-appearance-of-cells-in-the-datagrid.md)  
  
- [<span data-ttu-id="c3c8e-172">Vorgehensweise: Anpassen der Darstellung von Zeilen im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c3c8e-172">How to: Customize the Appearance of Rows in the Windows Forms DataGridView Control</span></span>](customize-the-appearance-of-rows-in-the-datagrid.md)  
  
### <a name="toolstrip-control"></a><span data-ttu-id="c3c8e-173">ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c3c8e-173">ToolStrip Control</span></span>  
 <span data-ttu-id="c3c8e-174"><xref:System.Windows.Forms.ToolStrip> und abgeleitete Steuerelemente ermöglichen es Ihnen, beliebige Aspekte ihrer Darstellung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-174"><xref:System.Windows.Forms.ToolStrip> and derived controls enable you to customize any aspect of their appearance.</span></span>  
  
 <span data-ttu-id="c3c8e-175">Wenn Sie benutzerdefiniertes Rendering für Steuerelemente bereitstellen möchten <xref:System.Windows.Forms.ToolStrip> , legen Sie die `Renderer` -Eigenschaft eines <xref:System.Windows.Forms.ToolStrip> , <xref:System.Windows.Forms.ToolStripManager> , <xref:System.Windows.Forms.ToolStripPanel> oder <xref:System.Windows.Forms.ToolStripContentPanel> auf ein `ToolStripRenderer` -Objekt fest, und behandeln Sie mindestens eines der vielen von der-Klasse bereitgestellten Zeichnungs Ereignisse `ToolStripRenderer` .</span><span class="sxs-lookup"><span data-stu-id="c3c8e-175">To provide custom rendering for <xref:System.Windows.Forms.ToolStrip> controls, set the `Renderer` property of a <xref:System.Windows.Forms.ToolStrip>, <xref:System.Windows.Forms.ToolStripManager>, <xref:System.Windows.Forms.ToolStripPanel>, or <xref:System.Windows.Forms.ToolStripContentPanel> to a `ToolStripRenderer` object and handle one or more of the many drawing events provided by the `ToolStripRenderer` class.</span></span> <span data-ttu-id="c3c8e-176">Alternativ können Sie eine- `Renderer` Eigenschaft auf eine Instanz Ihrer eigenen Klasse festlegen, `ToolStripRenderer` die von, oder abgeleitet ist, <xref:System.Windows.Forms.ToolStripProfessionalRenderer> <xref:System.Windows.Forms.ToolStripSystemRenderer> die bestimmte `On` *EventName* -Methoden implementiert oder überschreibt.</span><span class="sxs-lookup"><span data-stu-id="c3c8e-176">Alternatively, set a `Renderer` property to an instance of your own class derived from `ToolStripRenderer`, <xref:System.Windows.Forms.ToolStripProfessionalRenderer>, or <xref:System.Windows.Forms.ToolStripSystemRenderer> that implements or overrides specific `On`*EventName* methods.</span></span>  
  
 <span data-ttu-id="c3c8e-177">Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c3c8e-177">For more information, including code examples, see the following topics:</span></span>  
  
- <xref:System.Windows.Forms.ToolStripRenderer>  
  
- [<span data-ttu-id="c3c8e-178">Gewusst wie: Erstellen und Festlegen eines benutzerdefinierten Renderers für das ToolStrip-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c3c8e-178">How to: Create and Set a Custom Renderer for the ToolStrip Control in Windows Forms</span></span>](create-and-set-a-custom-renderer-for-the-toolstrip-control-in-wf.md)  
  
- [<span data-ttu-id="c3c8e-179">Vorgehensweise: Benutzerdefiniertes Zeichnen eines ToolStrip-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="c3c8e-179">How to: Custom Draw a ToolStrip Control</span></span>](how-to-custom-draw-a-toolstrip-control.md)  
  
## <a name="see-also"></a><span data-ttu-id="c3c8e-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3c8e-180">See also</span></span>

- [<span data-ttu-id="c3c8e-181">Steuerelemente für Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c3c8e-181">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
