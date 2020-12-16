---
title: Festlegen der Position und Ändern der Größe eines Formulars
description: Hier erfahren Sie, wie Sie die Größe und Position eines Formulars in .NET Windows Forms und Visual Studio festlegen. Die Größe und Position können entweder im Visual Studio-Designer oder direkt im Code festgelegt werden.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- positioning Windows Forms
- resizing Windows Forms
- Windows Forms, location
- Windows Forms, size
ms.openlocfilehash: 4fdaff7589669ae2e216d08feda5368835b50b5b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942135"
---
# <a name="how-to-position-and-size-a-form-windows-forms-net"></a><span data-ttu-id="070a3-104">Festlegen der Position und Größe eines Formulars (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="070a3-104">How to position and size a form (Windows Forms .NET)</span></span>

<span data-ttu-id="070a3-105">Wenn ein Formular erstellt wird, werden die Größe und Position zunächst auf einen Standardwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="070a3-105">When a form is created, the size and location is initially set to a default value.</span></span> <span data-ttu-id="070a3-106">Die Standardgröße eines Formulars beträgt im Allgemeinen eine Höhe und Breite von _800 × 500_ Pixel.</span><span class="sxs-lookup"><span data-stu-id="070a3-106">The default size of a form is generally a width and height of _800x500_ pixels.</span></span> <span data-ttu-id="070a3-107">Die ursprüngliche Position beim Anzeigen des Formulars hängt von einigen unterschiedlichen Einstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="070a3-107">The initial location, when the form is displayed, depends on a few different settings.</span></span>

<span data-ttu-id="070a3-108">Sie können die Größe eines Formulars zur Entwurfszeit mit Visual Studio und zur Laufzeit mit Code ändern.</span><span class="sxs-lookup"><span data-stu-id="070a3-108">You can change the size of a form at design time with Visual Studio, and at run time with code.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="resize-with-the-designer"></a><span data-ttu-id="070a3-109">Ändern der Größe mit dem Designer</span><span class="sxs-lookup"><span data-stu-id="070a3-109">Resize with the designer</span></span>

<span data-ttu-id="070a3-110">Nachdem dem Projekt ein [neues Formular hinzugefügt wurde](how-to-add.md), kann die Größe eines Formulars auf zwei verschiedene Arten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="070a3-110">After [adding a new form](how-to-add.md) to the project, the size of a form is set in two different ways.</span></span> <span data-ttu-id="070a3-111">Erstens können Sie die Größe mithilfe der Größenziehpunkte im Designer anpassen.</span><span class="sxs-lookup"><span data-stu-id="070a3-111">First, you can set it is with the size grips in the designer.</span></span> <span data-ttu-id="070a3-112">Durch Ziehen des rechten oder unteren Rands oder durch Ziehen der Ecke kann die Größe des Formulars geändert werden.</span><span class="sxs-lookup"><span data-stu-id="070a3-112">By dragging either the right edge, bottom edge, or the corner, you can resize the form.</span></span>

:::image type="content" source="media/how-to-position-and-resize/designer-grips.png" alt-text="Rechtsklick auf den Projektmappen-Explorer, um dem Windows Forms-Projekt ein neues Formular mit Größenziehpunkten hinzuzufügen":::

<span data-ttu-id="070a3-114">Die zweite Möglichkeit besteht darin, die Größe des Formulars bei geöffnetem Designer im Eigenschaftenbereich zu ändern.</span><span class="sxs-lookup"><span data-stu-id="070a3-114">The second way you can resize the form while the designer is open, is through the properties pane.</span></span> <span data-ttu-id="070a3-115">Klicken Sie dazu auf das Formular, und suchen Sie den Bereich **Eigenschaften** in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="070a3-115">Select the form, then find the **Properties** pane in Visual Studio.</span></span> <span data-ttu-id="070a3-116">Scrollen Sie nach unten zu **Größe**, und erweitern Sie den Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="070a3-116">Scroll down to **size** and expand it.</span></span> <span data-ttu-id="070a3-117">Sie können die **Breite** und **Höhe** manuell festlegen.</span><span class="sxs-lookup"><span data-stu-id="070a3-117">You can set the **Width** and **Height** manually.</span></span>

:::image type="content" source="media/how-to-position-and-resize/designer-properties-size.png" alt-text="Rechtsklick auf den Projektmappen-Explorer, um dem Windows Forms-Projekt ein neues Formular hinzuzufügen":::

## <a name="resize-in-code"></a><span data-ttu-id="070a3-119">Ändern der Größe im Code</span><span class="sxs-lookup"><span data-stu-id="070a3-119">Resize in code</span></span>

<span data-ttu-id="070a3-120">Obwohl der Designer die anfängliche Größe eines Formulars festlegt, können Sie diese im Code ändern.</span><span class="sxs-lookup"><span data-stu-id="070a3-120">Even though the designer sets the starting size of a form, you can resize it through code.</span></span> <span data-ttu-id="070a3-121">Es bietet sich an, die Größe eines Formulars im Code zu ändern, wenn die Anwendung feststellt, dass die Standardgröße des Formulars unzureichend ist.</span><span class="sxs-lookup"><span data-stu-id="070a3-121">Using code to resize a form is useful when something about your application determines that the default size of the form is insufficient.</span></span>

<span data-ttu-id="070a3-122">Passen Sie zum Ändern der Größe eines Formulars die <xref:System.Windows.Forms.Form.Size%2A>-Eigenschaft an, die die Breite und Höhe des Formulars darstellt.</span><span class="sxs-lookup"><span data-stu-id="070a3-122">To resize a form, change the <xref:System.Windows.Forms.Form.Size%2A>, which represents the width and height of the form.</span></span>

### <a name="resize-the-current-form"></a><span data-ttu-id="070a3-123">Ändern der Größe des aktuellen Formulars</span><span class="sxs-lookup"><span data-stu-id="070a3-123">Resize the current form</span></span>

<span data-ttu-id="070a3-124">Sie können die Größe des aktuellen Formulars ändern, solange der Code im Kontext des Formulars ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="070a3-124">You can change the size of the current form as long as the code is running within the context of the form.</span></span> <span data-ttu-id="070a3-125">Beispiel: `Form1` enthält eine Schaltfläche, die den `Click`-Ereignishandler aufruft, wenn sie angeklickt wird, um die Größe des Formulars zu ändern:</span><span class="sxs-lookup"><span data-stu-id="070a3-125">For example, if you have `Form1` with a button on it, that when clicked invokes the `Click` event handler to resize the form:</span></span>

```csharp
private void button1_Click(object sender, EventArgs e) =>
    Size = new Size(250, 200);
```

```vb
Private Sub Button1_Click(sender As Object, e As EventArgs)
    Size = New Drawing.Size(250, 200)
End Sub
```

### <a name="resize-a-different-form"></a><span data-ttu-id="070a3-126">Ändern der Größe eines anderen Formulars</span><span class="sxs-lookup"><span data-stu-id="070a3-126">Resize a different form</span></span>

<span data-ttu-id="070a3-127">Sie können die Größe eines anderen Formulars nach dessen Erstellung mithilfe der Variablen ändern, die auf das Formular verweist.</span><span class="sxs-lookup"><span data-stu-id="070a3-127">You can change the size of another form after it's created by using the variable referencing the form.</span></span> <span data-ttu-id="070a3-128">Beispiel: Sie verfügen über die beiden Formulare `Form1` (in diesem Beispiel das Startformular) und `Form2`.</span><span class="sxs-lookup"><span data-stu-id="070a3-128">For example, let's say you have two forms, `Form1` (the startup form in this example) and `Form2`.</span></span> <span data-ttu-id="070a3-129">`Form1` weist eine Schaltfläche auf, die das `Click`-Ereignis aufruft, wenn sie angeklickt wird.</span><span class="sxs-lookup"><span data-stu-id="070a3-129">`Form1` has a button that when clicked, invokes the `Click` event.</span></span> <span data-ttu-id="070a3-130">Der Handler dieses Ereignisses erstellt eine neue Instanz des Formulars `Form2`, legt die Größe fest und zeigt das Formular dann an:</span><span class="sxs-lookup"><span data-stu-id="070a3-130">The handler of this event creates a new instance of the `Form2` form, sets the size, and then displays it:</span></span>

```csharp
private void button1_Click(object sender, EventArgs e)
{
    Form2 form = new Form2();
    form.Size = new Size(250, 200);
    form.Show();
}
```

```vb
Private Sub Button1_Click(sender As Object, e As EventArgs)
    Dim form = New Form2 With {
        .Size = New Drawing.Size(250, 200)
    }
    form.Show()
End Sub
```

<span data-ttu-id="070a3-131">Wenn `Size` nicht manuell festgelegt wird, entspricht die Standardgröße des Formulars der zur Entwurfszeit festgelegten Größe.</span><span class="sxs-lookup"><span data-stu-id="070a3-131">If the `Size` isn't manually set, the form's default size is what it was set to during design-time.</span></span>

## <a name="position-with-the-designer"></a><span data-ttu-id="070a3-132">Positionieren mit dem Designer</span><span class="sxs-lookup"><span data-stu-id="070a3-132">Position with the designer</span></span>

<span data-ttu-id="070a3-133">Wenn eine Formularinstanz erstellt und angezeigt wird, wird die ursprüngliche Position des Formulars durch die <xref:System.Windows.Forms.Form.StartPosition%2A>-Eigenschaft bestimmt.</span><span class="sxs-lookup"><span data-stu-id="070a3-133">When a form instance is created and displayed, the initial location of the form is determined by the <xref:System.Windows.Forms.Form.StartPosition%2A> property.</span></span> <span data-ttu-id="070a3-134">Die <xref:System.Windows.Forms.Form.Location%2A>-Eigenschaft enthält die aktuelle Position des Formulars.</span><span class="sxs-lookup"><span data-stu-id="070a3-134">The <xref:System.Windows.Forms.Form.Location%2A> property holds the current location the form.</span></span> <span data-ttu-id="070a3-135">Beide Eigenschaften können über den Designer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="070a3-135">Both properties can be set through the designer.</span></span>

:::image type="content" source="media/how-to-position-and-resize/startposition.png" alt-text="Visual Studio-Eigenschaftenbereich mit hervorgehobener Startposition":::

| <span data-ttu-id="070a3-137">Enumeration „FormStartPosition“</span><span class="sxs-lookup"><span data-stu-id="070a3-137">FormStartPosition Enum</span></span> | <span data-ttu-id="070a3-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="070a3-138">Description</span></span>                                                                                                      |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070a3-139">CenterParent</span><span class="sxs-lookup"><span data-stu-id="070a3-139">CenterParent</span></span>           | <span data-ttu-id="070a3-140">Das Formular wird innerhalb des übergeordneten Formulars zentriert.</span><span class="sxs-lookup"><span data-stu-id="070a3-140">The form is centered within the bounds of its parent form.</span></span>                                                       |
| <span data-ttu-id="070a3-141">CenterScreen</span><span class="sxs-lookup"><span data-stu-id="070a3-141">CenterScreen</span></span>           | <span data-ttu-id="070a3-142">Das Formular wird bei der aktuellen Anzeige zentriert.</span><span class="sxs-lookup"><span data-stu-id="070a3-142">The form is centered on the current display.</span></span>                                                                     |
| <span data-ttu-id="070a3-143">Manuell</span><span class="sxs-lookup"><span data-stu-id="070a3-143">Manual</span></span>                 | <span data-ttu-id="070a3-144">Die Position des Formulars wird durch die [Location](xref:System.Windows.Forms.Form.Location%2A)-Eigenschaft bestimmt.</span><span class="sxs-lookup"><span data-stu-id="070a3-144">The position of the form is determined by the [Location](xref:System.Windows.Forms.Form.Location%2A) property.</span></span>   |
| <span data-ttu-id="070a3-145">WindowsDefaultBounds</span><span class="sxs-lookup"><span data-stu-id="070a3-145">WindowsDefaultBounds</span></span>   | <span data-ttu-id="070a3-146">Das Formular wird an der Windows-Standardposition positioniert, und seine Größe wird in die von Windows festgelegte Standardgröße geändert.</span><span class="sxs-lookup"><span data-stu-id="070a3-146">The form is positioned at the Windows default location and is resized to the default size determined by Windows.</span></span> |
| <span data-ttu-id="070a3-147">WindowsDefaultLocation</span><span class="sxs-lookup"><span data-stu-id="070a3-147">WindowsDefaultLocation</span></span> | <span data-ttu-id="070a3-148">Das Formular wird an der Windows-Standardposition positioniert, und seine Größe wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="070a3-148">The form is positioned at the Windows default location and isn't resized.</span></span>                                        |

<span data-ttu-id="070a3-149">Der [CenterParent](xref:System.Windows.Forms.FormStartPosition.CenterParent)-Wert funktioniert nur mit Formularen, bei denen es sich entweder um ein untergeordnetes MDI-Formular (Multiple Document Interface, Schnittstelle für mehrere Dokumente) oder um ein normales Formular handelt, das mit der Methode <xref:System.Windows.Window.ShowDialog%2A> angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="070a3-149">The [CenterParent](xref:System.Windows.Forms.FormStartPosition.CenterParent) value only works with forms that are either a multiple document interface (MDI) child form, or a normal form that is displayed with the <xref:System.Windows.Window.ShowDialog%2A> method.</span></span> <span data-ttu-id="070a3-150">`CenterParent` hat keine Auswirkung auf ein normales Formular, das mit der Methode <xref:System.Windows.Window.Show%2A> angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="070a3-150">`CenterParent` has no affect on a normal form that is displayed with the <xref:System.Windows.Window.Show%2A> method.</span></span> <span data-ttu-id="070a3-151">Verwenden Sie den folgenden Code, um ein Formular (`form`-Variable) in einem anderen Formular (`parentForm`-Variable) zu zentrieren:</span><span class="sxs-lookup"><span data-stu-id="070a3-151">To center a form (`form` variable) to another form (`parentForm` variable), use the following code:</span></span>

```csharp
form.StartPosition = FormStartPosition.Manual;
form.Location = new Point(parentForm.Width / 2 - form.Width / 2 + parentForm.Location.X,
                          parentForm.Height / 2 - form.Height / 2 + parentForm.Location.Y);
form.Show();
```

```vb
form.StartPosition = Windows.Forms.FormStartPosition.CenterParent.Manual
form.Location = New Drawing.Point(parentForm.Width / 2 - form.Width / 2 + parentForm.Location.X,
                                  parentForm.Height / 2 - form.Height / 2 + parentForm.Location.Y)

form.Show()
```

## <a name="position-with-code"></a><span data-ttu-id="070a3-152">Positionieren mit Code</span><span class="sxs-lookup"><span data-stu-id="070a3-152">Position with code</span></span>

<span data-ttu-id="070a3-153">Obwohl die Startposition eines Formulars mit dem Designer festgelegt werden kann, können Sie im Code entweder den Modus für die Startposition ändern oder die Position manuell festlegen.</span><span class="sxs-lookup"><span data-stu-id="070a3-153">Even though the designer can be used to set the starting location of a form, you can use code either change the starting position mode or set the location manually.</span></span> <span data-ttu-id="070a3-154">Das Positionieren eines Formulars mithilfe von Code ist hilfreich, wenn Sie ein Formular manuell in Relation zum Bildschirm oder anderen Formularen positionieren und in der Größe anpassen müssen.</span><span class="sxs-lookup"><span data-stu-id="070a3-154">Using code to position a form is useful if you need to manually position and size a form in relation to the screen or other forms.</span></span>

### <a name="move-the-current-form"></a><span data-ttu-id="070a3-155">Verschieben des aktuellen Formulars</span><span class="sxs-lookup"><span data-stu-id="070a3-155">Move the current form</span></span>

<span data-ttu-id="070a3-156">Sie können das aktuelle Formular verschieben, solange der Code im Kontext des Formulars ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="070a3-156">You can move the current form as long as the code is running within the context of the form.</span></span> <span data-ttu-id="070a3-157">Beispiel: `Form1` enthält eine Schaltfläche, die den `Click`-Ereignishandler aufruft, wenn sie angeklickt wird.</span><span class="sxs-lookup"><span data-stu-id="070a3-157">For example, if you have `Form1` with a button on it, that when clicked invokes the `Click` event handler.</span></span> <span data-ttu-id="070a3-158">Der Handler in diesem Beispiel ändert die Position des Formulars in den oberen linken Bildschirmbereich, indem er die <xref:System.Windows.Forms.Form.Location%2A>-Eigenschaft festlegt:</span><span class="sxs-lookup"><span data-stu-id="070a3-158">The handler in this example changes the location of the form to the top-left of the screen by setting the <xref:System.Windows.Forms.Form.Location%2A> property:</span></span>

```csharp
private void button1_Click(object sender, EventArgs e) =>
    Location = new Point(0, 0);
```

```vb
Private Sub Button1_Click(sender As Object, e As EventArgs)
    Location = New Drawing.Point(0, 0)
End Sub
```

### <a name="position-a-different-form"></a><span data-ttu-id="070a3-159">Positionieren eines anderen Formulars</span><span class="sxs-lookup"><span data-stu-id="070a3-159">Position a different form</span></span>

<span data-ttu-id="070a3-160">Sie können die Position eines anderen Formulars nach dessen Erstellung mithilfe der Variablen ändern, die auf das Formular verweist.</span><span class="sxs-lookup"><span data-stu-id="070a3-160">You can change the location of another form after it's created by using the variable referencing the form.</span></span> <span data-ttu-id="070a3-161">Beispiel: Sie verfügen über die beiden Formulare `Form1` (in diesem Beispiel das Startformular) und `Form2`.</span><span class="sxs-lookup"><span data-stu-id="070a3-161">For example, let's say you have two forms, `Form1` (the startup form in this example) and `Form2`.</span></span> <span data-ttu-id="070a3-162">`Form1` weist eine Schaltfläche auf, die das `Click`-Ereignis aufruft, wenn sie angeklickt wird.</span><span class="sxs-lookup"><span data-stu-id="070a3-162">`Form1` has a button that when clicked, invokes the `Click` event.</span></span> <span data-ttu-id="070a3-163">Der Handler dieses Ereignisses erstellt eine neue Instanz des Formulars `Form2` und legt die Größe fest:</span><span class="sxs-lookup"><span data-stu-id="070a3-163">The handler of this event creates a new instance of the `Form2` form and sets the size:</span></span>

```csharp
private void button1_Click(object sender, EventArgs e)
{
    Form2 form = new Form2();
    form.Size = new Size(250, 200);
    form.Show();
}
```

```vb
Private Sub Button1_Click(sender As Object, e As EventArgs)
    Dim form = New Form2 With {
        .Size = New Drawing.Size(250, 200)
    }
    form.Show()
End Sub
```

<span data-ttu-id="070a3-164">Wenn `Size` nicht festgelegt wird, entspricht die Standardgröße des Formulars der zur Entwurfszeit festgelegten Größe.</span><span class="sxs-lookup"><span data-stu-id="070a3-164">If the `Size` isn't set, the form's default size is what it was set to at design-time.</span></span>

## <a name="see-also"></a><span data-ttu-id="070a3-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="070a3-165">See also</span></span>

- [<span data-ttu-id="070a3-166">Hinzufügen eines Formulars zu einem Projekt (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="070a3-166">How to add a form to a project (Windows Forms .NET)</span></span>](how-to-add.md)
- [<span data-ttu-id="070a3-167">Übersicht über Ereignisse (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="070a3-167">Events overview (Windows Forms .NET)</span></span>](events.md)
- [<span data-ttu-id="070a3-168">Position und Layout von Steuerelementen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="070a3-168">Position and layout of controls (Windows Forms .NET)</span></span>](../controls/layout.md)
