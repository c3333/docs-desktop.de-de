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
# <a name="painting-and-drawing-on-controls-windows-forms-net"></a>Zeichnen eines Steuerelements (Windows Forms .NET)

Das benutzerdefinierte Zeichnen von Steuerelementen ist eine der vielen komplizierten Aufgaben, die durch Windows Forms vereinfacht werden kann. Wenn ein benutzerdefiniertes Steuerelement erstellt wird, gibt es viele Optionen, wie Sie die grafische Darstellung Ihres Steuerelements beeinflussen können. Wenn Sie ein [benutzerdefiniertes Steuerelement](custom.md#custom-controls) erstellen, also ein Steuerelement, das von <xref:System.Windows.Forms.Control> erbt, müssen Sie Code bereitstellen, um seine grafische Darstellung zu rendern.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

Wenn Sie ein [zusammengesetztes Steuerelement](custom.md#composite-controls) erstellen, also ein Steuerelement, das von <xref:System.Windows.Forms.UserControl> oder einem der vorhandenen Windows Forms-Steuerelemente erbt, können Sie die grafische Standarddarstellung überschreiben und eigenen Grafikcode bereitstellen.

Wenn Sie benutzerdefiniertes Rendering für ein vorhandenes Steuerelement anwenden möchten, ohne ein neues Steuerelement zu erstellen, sind die verfügbaren Optionen eingeschränkter. Dennoch gibt es weiterhin ein große Bandbreite grafischer Möglichkeiten für Ihre Steuerelemente und Anwendungen.

Beim Rendern von Steuerelementen sind die folgenden Elemente beteiligt:

- Die von der Basisklasse <xref:System.Windows.Forms.Control?displayProperty=nameWithType> bereitgestellte Funktion zum Zeichnen
- Die essentiellen Elemente der GDI-Grafikbibliothek
- Die Geometrie der Zeichnungsregion
- Die Prozedur für das Freigeben von Grafikressourcen

## <a name="drawing-provided-by-control"></a>Vom Steuerelement bereitgestellte Funktionen zum Zeichnen

Die Basisklasse <xref:System.Windows.Forms.Control> stellt Funktionen zum Zeichnen über das dazugehörige <xref:System.Windows.Forms.Control.Paint>-Ereignis bereit. Ein Steuerelement löst das <xref:System.Windows.Forms.Control.Paint>-Ereignis aus, sobald die dazugehörige Anzeige aktualisiert werden muss. Weitere Informationen zu Ereignissen in .NET finden Sie unter [Behandeln und Auslösen von Ereignissen](/dotnet/standard/events/index).

Die Ereignisdatenklasse für das <xref:System.Windows.Forms.Control.Paint>-Ereignis, <xref:System.Windows.Forms.PaintEventArgs>, enthält die Daten, die für das Zeichnen eines Steuerelements erforderlich sind – ein Handle für ein Grafikobjekt und ein Rechteck, das die Region darstellt, in der gezeichnet wird.

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

<xref:System.Drawing.Graphics> ist eine verwaltete Klasse, die die Funktion zum Zeichnen kapselt. Weitere Informationen finden Sie in der GDI-Diskussion später in diesem Artikel. Bei <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> handelt es sich um eine Instanz der <xref:System.Drawing.Rectangle>-Struktur. Hierdurch wird der verfügbare Bereich definiert, in dem ein Steuerelement zeichnen kann. Der Entwickler eines Steuerelements kann <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> mit der <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A>-Eigenschaft eines Steuerelements berechnen. Weitere Informationen finde Sie in der Geometriediskussion später in diesem Artikel.

### <a name="onpaint"></a>OnPaint

Ein Steuerelement muss Renderinglogik bereitstellen, indem die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode überschrieben wird, die es von <xref:System.Windows.Forms.Control> erbt. <xref:System.Windows.Forms.Control.OnPaint%2A> erhält über die übergebenen Eigenschaften <xref:System.Drawing.Design.PaintValueEventArgs.Graphics%2A> und <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> der Instanz <xref:System.Windows.Forms.PaintEventArgs> Zugriff auf ein Grafikobjekt und ein Rechteck, in dem gezeichnet werden kann.

Im folgenden Code wird der `System.Drawing`-Namespace verwendet:

:::code language="csharp" source="./snippets/custom-painting-drawing/cs/UserControl1.cs" id="OnPaintMethod":::

:::code language="vb" source="./snippets/custom-painting-drawing/vb/UserControl1.vb" id="OnPaintMethod":::

Die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode der <xref:System.Windows.Forms.Control>-Basisklasse implementiert keine Zeichnungsfunktionen, ruft jedoch die Ereignisdelegaten auf, die für das <xref:System.Windows.Forms.Control.Paint>-Ereignis registriert sind. Wenn Sie <xref:System.Windows.Forms.Control.OnPaint%2A> überschreiben, sollten Sie in der Regel die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode der Basisklasse aufrufen, damit registrierte Delegaten das <xref:System.Windows.Forms.Control.Paint>-Ereignis empfangen. Steuerelemente, deren gesamte Oberfläche gezeichnet wird, sollten nicht die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode der Basisklasse aufrufen, da dies zu Flimmern führen kann.

> [!NOTE]
> Rufen Sie <xref:System.Windows.Forms.Control.OnPaint%2A> nicht direkt in Ihrem Steuerelement auf. Rufen Sie stattdessen die <xref:System.Windows.Forms.Control.Invalidate%2A>-Methode (von <xref:System.Windows.Forms.Control> geerbt) oder eine andere Methode auf, die <xref:System.Windows.Forms.Control.Invalidate%2A> aufruft. Die <xref:System.Windows.Forms.Control.Invalidate%2A>-Methode wiederum ruft <xref:System.Windows.Forms.Control.OnPaint%2A> auf. Die <xref:System.Windows.Forms.Control.Invalidate%2A>-Methode wird überladen und zeichnet je nach für <xref:System.Windows.Forms.Control.Invalidate%2A> `e` bereitgestellten Argumenten entweder Teile oder den gesamten Bildschirmbereich neu.

Der Code in der <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode Ihres Steuerelements wird ausgeführt, wenn das Steuerelement erstmalig gezeichnet wird, und bei jeder Aktualisierung. Damit Ihr Steuerelement bei jeder Größenanpassung neu gezeichnet wird, fügen Sie die folgende Zeile im Konstruktor Ihres Steuerelements hinzu:

```csharp
SetStyle(ControlStyles.ResizeRedraw, true);
```

```vb
SetStyle(ControlStyles.ResizeRedraw, True)
```

### <a name="onpaintbackground"></a>OnPaintBackground

Die <xref:System.Windows.Forms.Control>-Basisklasse definiert eine weitere Methode, die hilfreich für das Zeichnen ist: die <xref:System.Windows.Forms.Control.OnPaintBackground%2A>-Methode.

```csharp
protected virtual void OnPaintBackground(PaintEventArgs e);
```

```vb
Protected Overridable Sub OnPaintBackground(e As PaintEventArgs)
```

<xref:System.Windows.Forms.Control.OnPaintBackground%2A> zeichnet den Hintergrund (und so auch die Form) des Fensters. Dies erfolgt sehr schnell. <xref:System.Windows.Forms.Control.OnPaint%2A> hingegen zeichnet die Details und ist deshalb möglicherweise langsamer, da einzelne Zeichnungsanforderungen in ein <xref:System.Windows.Forms.Control.Paint>-Ereignis kombiniert werden, das alle Bereiche abdeckt, die neu gezeichnet werden müssen. Sie sollten <xref:System.Windows.Forms.Control.OnPaintBackground%2A> aufrufen, wenn Sie beispielsweise ein Hintergrund mit Farbverlauf für Ihr Steuerelement zeichnen möchten.

Während <xref:System.Windows.Forms.Control.OnPaintBackground%2A> eine ereignisähnliche Bezeichnung aufweist und dasselbe Argument wie die `OnPaint`-Methode annimmt, handelt es sich bei `OnPaintBackground` um keine tatsächliche Ereignismethode. Es gibt kein `PaintBackground`-Ereignis, und `OnPaintBackground` ruft keine Ereignisdelegaten auf. Wenn die `OnPaintBackground`-Methode überschrieben wird, ist keine abgeleitete Klasse erforderlich, um die `OnPaintBackground`-Methode der dazugehörigen Basisklasse aufzurufen.

## <a name="gdi-basics"></a>GDI+-Grundlagen

Die <xref:System.Drawing.Graphics>-Klasse bietet Methoden für das Zeichnen verschiedener Formen wie Kreise, Dreiecke, Bögen und Ellipsen sowie Methoden für das Anzeigen von Text. Der <xref:System.Drawing?displayProperty=nameWithType>-Namespace enthält Namespaces und Klassen, die grafische Elemente wie Formen (z. B. Kreise, Rechtecke und Bögen), Farben, Schriftarten und Pinsel kapseln.<!-- TODO  For more information about GDI, see [Using Managed Graphics Classes](../advanced/using-managed-graphics-classes.md).-->

## <a name="geometry-of-the-drawing-region"></a>Geometrie der Zeichnungsregion

Die <xref:System.Windows.Forms.Control.ClientRectangle%2A>-Eigenschaft eines Steuerelements gibt die rechteckige Region an, die für das Steuerelement auf der Anzeige für den Benutzer verfügbar ist. Die <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A>-Eigenschaft von <xref:System.Windows.Forms.PaintEventArgs> gibt dahingegen den Bereich an, der gezeichnet wird. Ein Steuerelement muss möglicherweise nur einen Teil des verfügbaren Bereichs zeichnen, z. B. wenn ein kleiner Bereich der Anzeige des Steuerelements geändert wird. In solchen Situationen muss der Entwickler eines Steuerelements das tatsächliche Rechteck berechnen, in dem gezeichnet werden soll, und dieses an <xref:System.Windows.Forms.Control.Invalidate%2A> übergeben. Die überladenen Versionen von <xref:System.Windows.Forms.Control.Invalidate%2A>, die <xref:System.Drawing.Rectangle> oder <xref:System.Drawing.Region> als Argument akzeptieren, verwenden dieses Argument, um die <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A>-Eigenschaft von <xref:System.Windows.Forms.PaintEventArgs> zu generieren.

## <a name="freeing-graphics-resources"></a>Freigeben von Grafikressourcen

Grafikobjekte sind teuer, da sie Systemressourcen verwenden. Zu solchen Objekten gehören Instanzen der <xref:System.Drawing.Graphics?displayProperty=nameWithType>-Klasse und Instanzen von <xref:System.Drawing.Brush?displayProperty=nameWithType>, <xref:System.Drawing.Pen?displayProperty=nameWithType> sowie weitere Grafikklassen. Es ist wichtig, dass Sie nur eine Grafikressource zeichnen, wenn Sie eine benötigen, und dass Sie sie freigeben, sobald Sie die Verwendung beendet haben. Wenn Sie eine Instanz eines Typs erstellen, der die <xref:System.IDisposable>-Schnittstelle implementiert, rufen Sie die dazugehörige <xref:System.IDisposable.Dispose%2A>-Methode auf, sobald Sie das Freigeben der Ressourcen abgeschlossen haben.

## <a name="see-also"></a>Siehe auch

- [Arten von benutzerdefinierten Steuerelementen](custom.md)
