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
# <a name="how-to-position-and-size-a-form-windows-forms-net"></a>Festlegen der Position und Größe eines Formulars (Windows Forms .NET)

Wenn ein Formular erstellt wird, werden die Größe und Position zunächst auf einen Standardwert festgelegt. Die Standardgröße eines Formulars beträgt im Allgemeinen eine Höhe und Breite von _800 × 500_ Pixel. Die ursprüngliche Position beim Anzeigen des Formulars hängt von einigen unterschiedlichen Einstellungen ab.

Sie können die Größe eines Formulars zur Entwurfszeit mit Visual Studio und zur Laufzeit mit Code ändern.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="resize-with-the-designer"></a>Ändern der Größe mit dem Designer

Nachdem dem Projekt ein [neues Formular hinzugefügt wurde](how-to-add.md), kann die Größe eines Formulars auf zwei verschiedene Arten festgelegt werden. Erstens können Sie die Größe mithilfe der Größenziehpunkte im Designer anpassen. Durch Ziehen des rechten oder unteren Rands oder durch Ziehen der Ecke kann die Größe des Formulars geändert werden.

:::image type="content" source="media/how-to-position-and-resize/designer-grips.png" alt-text="Rechtsklick auf den Projektmappen-Explorer, um dem Windows Forms-Projekt ein neues Formular mit Größenziehpunkten hinzuzufügen":::

Die zweite Möglichkeit besteht darin, die Größe des Formulars bei geöffnetem Designer im Eigenschaftenbereich zu ändern. Klicken Sie dazu auf das Formular, und suchen Sie den Bereich **Eigenschaften** in Visual Studio. Scrollen Sie nach unten zu **Größe**, und erweitern Sie den Abschnitt. Sie können die **Breite** und **Höhe** manuell festlegen.

:::image type="content" source="media/how-to-position-and-resize/designer-properties-size.png" alt-text="Rechtsklick auf den Projektmappen-Explorer, um dem Windows Forms-Projekt ein neues Formular hinzuzufügen":::

## <a name="resize-in-code"></a>Ändern der Größe im Code

Obwohl der Designer die anfängliche Größe eines Formulars festlegt, können Sie diese im Code ändern. Es bietet sich an, die Größe eines Formulars im Code zu ändern, wenn die Anwendung feststellt, dass die Standardgröße des Formulars unzureichend ist.

Passen Sie zum Ändern der Größe eines Formulars die <xref:System.Windows.Forms.Form.Size%2A>-Eigenschaft an, die die Breite und Höhe des Formulars darstellt.

### <a name="resize-the-current-form"></a>Ändern der Größe des aktuellen Formulars

Sie können die Größe des aktuellen Formulars ändern, solange der Code im Kontext des Formulars ausgeführt wird. Beispiel: `Form1` enthält eine Schaltfläche, die den `Click`-Ereignishandler aufruft, wenn sie angeklickt wird, um die Größe des Formulars zu ändern:

```csharp
private void button1_Click(object sender, EventArgs e) =>
    Size = new Size(250, 200);
```

```vb
Private Sub Button1_Click(sender As Object, e As EventArgs)
    Size = New Drawing.Size(250, 200)
End Sub
```

### <a name="resize-a-different-form"></a>Ändern der Größe eines anderen Formulars

Sie können die Größe eines anderen Formulars nach dessen Erstellung mithilfe der Variablen ändern, die auf das Formular verweist. Beispiel: Sie verfügen über die beiden Formulare `Form1` (in diesem Beispiel das Startformular) und `Form2`. `Form1` weist eine Schaltfläche auf, die das `Click`-Ereignis aufruft, wenn sie angeklickt wird. Der Handler dieses Ereignisses erstellt eine neue Instanz des Formulars `Form2`, legt die Größe fest und zeigt das Formular dann an:

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

Wenn `Size` nicht manuell festgelegt wird, entspricht die Standardgröße des Formulars der zur Entwurfszeit festgelegten Größe.

## <a name="position-with-the-designer"></a>Positionieren mit dem Designer

Wenn eine Formularinstanz erstellt und angezeigt wird, wird die ursprüngliche Position des Formulars durch die <xref:System.Windows.Forms.Form.StartPosition%2A>-Eigenschaft bestimmt. Die <xref:System.Windows.Forms.Form.Location%2A>-Eigenschaft enthält die aktuelle Position des Formulars. Beide Eigenschaften können über den Designer festgelegt werden.

:::image type="content" source="media/how-to-position-and-resize/startposition.png" alt-text="Visual Studio-Eigenschaftenbereich mit hervorgehobener Startposition":::

| Enumeration „FormStartPosition“ | BESCHREIBUNG                                                                                                      |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| CenterParent           | Das Formular wird innerhalb des übergeordneten Formulars zentriert.                                                       |
| CenterScreen           | Das Formular wird bei der aktuellen Anzeige zentriert.                                                                     |
| Manuell                 | Die Position des Formulars wird durch die [Location](xref:System.Windows.Forms.Form.Location%2A)-Eigenschaft bestimmt.   |
| WindowsDefaultBounds   | Das Formular wird an der Windows-Standardposition positioniert, und seine Größe wird in die von Windows festgelegte Standardgröße geändert. |
| WindowsDefaultLocation | Das Formular wird an der Windows-Standardposition positioniert, und seine Größe wird nicht geändert.                                        |

Der [CenterParent](xref:System.Windows.Forms.FormStartPosition.CenterParent)-Wert funktioniert nur mit Formularen, bei denen es sich entweder um ein untergeordnetes MDI-Formular (Multiple Document Interface, Schnittstelle für mehrere Dokumente) oder um ein normales Formular handelt, das mit der Methode <xref:System.Windows.Window.ShowDialog%2A> angezeigt wird. `CenterParent` hat keine Auswirkung auf ein normales Formular, das mit der Methode <xref:System.Windows.Window.Show%2A> angezeigt wird. Verwenden Sie den folgenden Code, um ein Formular (`form`-Variable) in einem anderen Formular (`parentForm`-Variable) zu zentrieren:

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

## <a name="position-with-code"></a>Positionieren mit Code

Obwohl die Startposition eines Formulars mit dem Designer festgelegt werden kann, können Sie im Code entweder den Modus für die Startposition ändern oder die Position manuell festlegen. Das Positionieren eines Formulars mithilfe von Code ist hilfreich, wenn Sie ein Formular manuell in Relation zum Bildschirm oder anderen Formularen positionieren und in der Größe anpassen müssen.

### <a name="move-the-current-form"></a>Verschieben des aktuellen Formulars

Sie können das aktuelle Formular verschieben, solange der Code im Kontext des Formulars ausgeführt wird. Beispiel: `Form1` enthält eine Schaltfläche, die den `Click`-Ereignishandler aufruft, wenn sie angeklickt wird. Der Handler in diesem Beispiel ändert die Position des Formulars in den oberen linken Bildschirmbereich, indem er die <xref:System.Windows.Forms.Form.Location%2A>-Eigenschaft festlegt:

```csharp
private void button1_Click(object sender, EventArgs e) =>
    Location = new Point(0, 0);
```

```vb
Private Sub Button1_Click(sender As Object, e As EventArgs)
    Location = New Drawing.Point(0, 0)
End Sub
```

### <a name="position-a-different-form"></a>Positionieren eines anderen Formulars

Sie können die Position eines anderen Formulars nach dessen Erstellung mithilfe der Variablen ändern, die auf das Formular verweist. Beispiel: Sie verfügen über die beiden Formulare `Form1` (in diesem Beispiel das Startformular) und `Form2`. `Form1` weist eine Schaltfläche auf, die das `Click`-Ereignis aufruft, wenn sie angeklickt wird. Der Handler dieses Ereignisses erstellt eine neue Instanz des Formulars `Form2` und legt die Größe fest:

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

Wenn `Size` nicht festgelegt wird, entspricht die Standardgröße des Formulars der zur Entwurfszeit festgelegten Größe.

## <a name="see-also"></a>Siehe auch

- [Hinzufügen eines Formulars zu einem Projekt (Windows Forms .NET)](how-to-add.md)
- [Übersicht über Ereignisse (Windows Forms .NET)](events.md)
- [Position und Layout von Steuerelementen (Windows Forms .NET)](../controls/layout.md)
