---
title: Rendering eines Steuer Elements
ms.date: 03/30/2017
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], rendering
- OnPaintBackground method [Windows Forms], invoking in Windows Forms custom controls
- custom controls [Windows Forms], graphics resources
- custom controls [Windows Forms], invalidation and painting
ms.assetid: aae8e1e6-4786-432b-a15e-f4c44760d302
ms.openlocfilehash: 86e219723dde8c10a8cc0d4ee7bdf149cde399bf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976477"
---
# <a name="rendering-a-windows-forms-control"></a>Wiedergeben eines Windows Forms-Steuerelements

Rendering bezieht sich auf den Prozess der Erstellung einer visuellen Darstellung auf dem Bildschirm eines Benutzers. Windows Forms verwendet GDI (die neue Windows-Grafikbibliothek) zum Rendern. Die verwalteten Klassen, die Zugriff auf GDI bereitstellen, befinden sich im <xref:System.Drawing?displayProperty=nameWithType> -Namespace und den zugehörigen Subnamespaces.  
  
 Die folgenden Elemente sind am Steuerelement Rendering beteiligt:  
  
- Die von der Basisklasse bereitgestellte Zeichnungs Funktionalität <xref:System.Windows.Forms.Control?displayProperty=nameWithType> .  
  
- Die wesentlichen Elemente der GDI-Grafikbibliothek.  
  
- Die Geometrie des Zeichnungs Bereichs.  
  
- Die Vorgehensweise zum Freigeben von Grafik Ressourcen.  
  
## <a name="drawing-functionality-provided-by-control"></a>Von Steuerelement bereitgestellte Zeichnungsfunktionen  

 Die-Basisklasse <xref:System.Windows.Forms.Control> stellt Zeichnungsfunktionen über das- <xref:System.Windows.Forms.Control.Paint> Ereignis bereit. Ein-Steuerelement löst das- <xref:System.Windows.Forms.Control.Paint> Ereignis aus, wenn es seine Anzeige aktualisieren muss. Weitere Informationen zu Ereignissen in der .NET Framework finden Sie unter [behandeln und Auswerfen von Ereignissen](/dotnet/standard/events/index).  
  
 Die Ereignisdaten Klasse für das <xref:System.Windows.Forms.Control.Paint> Ereignis, <xref:System.Windows.Forms.PaintEventArgs> , enthält die Daten, die zum Zeichnen eines Steuer Elements erforderlich sind – ein Handle für ein Grafik Objekt und ein Rechteck Objekt, das den Bereich darstellt, in dem gezeichnet werden soll. Diese Objekte werden im folgenden Code Fragment in Fett Schrift angezeigt.  
  
```vb  
Public Class PaintEventArgs  
   Inherits EventArgs  
   Implements IDisposable  
  
   Public ReadOnly Property ClipRectangle() As System.Drawing.Rectangle  
      ...  
   End Property  
  
   Public ReadOnly Property Graphics() As System.Drawing.Graphics  
      ...  
   End Property  
   ' Other properties and methods.  
   ...  
End Class  
```  
  
```csharp  
public class PaintEventArgs : EventArgs, IDisposable {  
public System.Drawing.Rectangle ClipRectangle {get;}  
public System.Drawing.Graphics Graphics {get;}  
// Other properties and methods.  
...  
}  
```  
  
 <xref:System.Drawing.Graphics> ist eine verwaltete Klasse, die Zeichnungsfunktionen kapselt, wie in der Erörterung von GDI weiter unten in diesem Thema beschrieben. <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A>Bei handelt es sich um eine Instanz der <xref:System.Drawing.Rectangle> -Struktur, die den verfügbaren Bereich definiert, in dem ein Steuerelement gezeichnet werden kann. Ein Steuerelement Entwickler kann das <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> mithilfe der- <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> Eigenschaft eines-Steuer Elements berechnen, wie in der Erläuterung der Geometrie weiter unten in diesem Thema beschrieben.  
  
 Ein Steuerelement muss Renderinglogik bereitstellen, indem die Methode überschrieben wird <xref:System.Windows.Forms.Control.OnPaint%2A> , von der geerbt wird <xref:System.Windows.Forms.Control> . <xref:System.Windows.Forms.Control.OnPaint%2A> Ruft den Zugriff auf ein Grafik Objekt und ein Rechteck ab, das durch die <xref:System.Drawing.Design.PaintValueEventArgs.Graphics%2A> -Eigenschaft und die-Eigenschaft der-Instanz gezeichnet werden soll <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> <xref:System.Windows.Forms.PaintEventArgs> .  
  
```vb  
Protected Overridable Sub OnPaint(pe As PaintEventArgs)  
```  
  
```csharp  
protected virtual void OnPaint(PaintEventArgs pe);  
```  
  
 Die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode der-Basis <xref:System.Windows.Forms.Control> Klasse implementiert keine Zeichnungsfunktionen, sondern ruft lediglich die Ereignis Delegaten auf, die beim-Ereignis registriert sind <xref:System.Windows.Forms.Control.Paint> . Wenn Sie <xref:System.Windows.Forms.Control.OnPaint%2A> überschreiben, sollten Sie in der Regel die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode der Basisklasse aufrufen, damit registrierte Delegaten das <xref:System.Windows.Forms.Control.Paint> Ereignis empfangen. Allerdings sollten Steuerelemente, die ihre gesamte Oberfläche zeichnen, nicht die Basisklasse aufrufen <xref:System.Windows.Forms.Control.OnPaint%2A> , da dadurch Flicker eingeführt wird. Ein Beispiel für das Überschreiben des <xref:System.Windows.Forms.Control.OnPaint%2A> Ereignisses finden Sie unter Gewusst [wie: Erstellen eines Windows Forms Steuer Elements, das den Fortschritt anzeigt](how-to-create-a-windows-forms-control-that-shows-progress.md).  
  
> [!NOTE]
> Rufen Sie nicht <xref:System.Windows.Forms.Control.OnPaint%2A> direkt aus dem Steuerelement auf. Rufen Sie stattdessen die- <xref:System.Windows.Forms.Control.Invalidate%2A> Methode (geerbt von <xref:System.Windows.Forms.Control> ) oder eine andere Methode auf, die aufruft <xref:System.Windows.Forms.Control.Invalidate%2A> . Die- <xref:System.Windows.Forms.Control.Invalidate%2A> Methode ruft wiederum auf <xref:System.Windows.Forms.Control.OnPaint%2A> . Die <xref:System.Windows.Forms.Control.Invalidate%2A> -Methode ist überladen, und abhängig von den Argumenten, die für bereitgestellt werden <xref:System.Windows.Forms.Control.Invalidate%2A> `e` , zeichnet ein-Steuerelement entweder einen Teil oder den gesamten Bildschirmbereich neu.  
  
 Die-Basis <xref:System.Windows.Forms.Control> Klasse definiert eine andere Methode, die zum Zeichnen von – die-Methode nützlich ist <xref:System.Windows.Forms.Control.OnPaintBackground%2A> .  
  
```vb  
Protected Overridable Sub OnPaintBackground(pevent As PaintEventArgs)  
```  
  
```csharp  
protected virtual void OnPaintBackground(PaintEventArgs pevent);  
```  
  
 <xref:System.Windows.Forms.Control.OnPaintBackground%2A> zeichnet den Hintergrund (und damit die Form) des Fensters und ist garantiert schnell, während <xref:System.Windows.Forms.Control.OnPaint%2A> die Details zeichnet und langsamer sein können, da einzelne Zeichnungs Anforderungen in einem Ereignis kombiniert werden, <xref:System.Windows.Forms.Control.Paint> das alle Bereiche abdeckt, die neu gezeichnet werden müssen. Möglicherweise möchten Sie den aufrufen, <xref:System.Windows.Forms.Control.OnPaintBackground%2A> Wenn Sie beispielsweise einen Hintergrund Hintergrund für das Steuerelement zeichnen möchten.  
  
 Obwohl <xref:System.Windows.Forms.Control.OnPaintBackground%2A> eine Ereignis ähnliche Nomenklatur aufweist und dasselbe Argument wie die- `OnPaint` Methode annimmt, <xref:System.Windows.Forms.Control.OnPaintBackground%2A> ist keine echte Ereignismethode. Es ist kein Ereignis vorhanden, und es werden keine Ereignis Delegaten aufgerufen `PaintBackground` <xref:System.Windows.Forms.Control.OnPaintBackground%2A> . Wenn die- <xref:System.Windows.Forms.Control.OnPaintBackground%2A> Methode überschrieben wird, ist es nicht erforderlich, dass eine abgeleitete Klasse die- <xref:System.Windows.Forms.Control.OnPaintBackground%2A> Methode der Basisklasse aufruft.  
  
## <a name="gdi-basics"></a>GDI+-Grundlagen  

 Die- <xref:System.Drawing.Graphics> Klasse stellt Methoden zum Zeichnen verschiedener Formen (z. b. Kreise, Dreiecke, Arcs und Ellipsen) sowie Methoden zum Anzeigen von Text bereit. Der <xref:System.Drawing?displayProperty=nameWithType> -Namespace und seine Subnamespaces enthalten Klassen, die Grafikelemente wie Formen (Kreise, Rechtecke, Arcs usw.), Farben, Schriftarten, Pinsel usw. Kapseln. Weitere Informationen zu GDI finden Sie unter [Verwenden von verwalteten Grafik Klassen](../advanced/using-managed-graphics-classes.md). Die Grundlagen von GDI werden auch im Abschnitt Gewusst [wie: Erstellen eines Windows Forms Steuer Elements beschrieben, das den Fortschritt anzeigt](how-to-create-a-windows-forms-control-that-shows-progress.md).  
  
## <a name="geometry-of-the-drawing-region"></a>Geometrie des Zeichnungs Bereichs  

 Die- <xref:System.Windows.Forms.Control.ClientRectangle%2A> Eigenschaft eines Steuer Elements gibt den rechteckigen Bereich an, der für das Steuerelement auf dem Bildschirm des Benutzers verfügbar ist, während die- <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> Eigenschaft von <xref:System.Windows.Forms.PaintEventArgs> den Bereich angibt, der tatsächlich gezeichnet wird. (Beachten Sie, dass das Zeichnen in der <xref:System.Windows.Forms.Control.Paint> Ereignismethode erfolgt, die eine- <xref:System.Windows.Forms.PaintEventArgs> Instanz als Argument annimmt). Ein Steuerelement muss möglicherweise nur einen Teil des verfügbaren Bereichs zeichnen, wie es auch der Fall ist, wenn sich ein kleiner Abschnitt der Anzeige des Steuer Elements ändert. In diesen Fällen muss ein Steuerelement Entwickler das eigentliche Rechteck berechnen, um es zu zeichnen und dieses an zu übergeben <xref:System.Windows.Forms.Control.Invalidate%2A> . Die überladenen Versionen von <xref:System.Windows.Forms.Control.Invalidate%2A> , die einen <xref:System.Drawing.Rectangle> oder <xref:System.Drawing.Region> als Argument akzeptieren, verwenden dieses Argument, um die- <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> Eigenschaft von zu generieren <xref:System.Windows.Forms.PaintEventArgs> .  
  
 Das folgende Code Fragment zeigt, wie das `FlashTrackBar` benutzerdefinierte Steuerelement den rechteckigen Bereich berechnet, in dem gezeichnet werden soll. Die- `client` Variable bezeichnet die- <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> Eigenschaft. Ein umfassendes Beispiel finden Sie unter Gewusst [wie: Erstellen eines Windows Forms Steuer Elements, das den Fortschritt anzeigt](how-to-create-a-windows-forms-control-that-shows-progress.md).  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#6)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#6)]  
  
## <a name="freeing-graphics-resources"></a>Freigeben von Grafik Ressourcen  

 Grafik Objekte sind aufwendig, da Sie Systemressourcen verwenden. Zu diesen Objekten zählen Instanzen der <xref:System.Drawing.Graphics?displayProperty=nameWithType> -Klasse sowie Instanzen von <xref:System.Drawing.Brush?displayProperty=nameWithType> , <xref:System.Drawing.Pen?displayProperty=nameWithType> und anderen Grafik Klassen. Es ist wichtig, dass Sie nur dann eine Grafik Ressource erstellen, wenn Sie Sie benötigen, und Sie nach der Verwendung sofort freigeben. Wenn Sie einen Typ erstellen, der die-Schnittstelle implementiert, rufen Sie die zugehörige- <xref:System.IDisposable> Methode auf, <xref:System.IDisposable.Dispose%2A> Wenn Sie damit fertig sind, um Ressourcen freizugeben.  
  
 Das folgende Code Fragment zeigt, wie das `FlashTrackBar` benutzerdefinierte Steuerelement eine Ressource erstellt und freigibt <xref:System.Drawing.Brush> . Den gesamten Quellcode finden Sie unter Gewusst [wie: Erstellen eines Windows Forms Steuer Elements, das den Fortschritt anzeigt](how-to-create-a-windows-forms-control-that-shows-progress.md).  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#5)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#5)]  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#4)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#4)]  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#3)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#3)]  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Erstellen eines Windows Forms-Steuerelements, das den Fortschritt anzeigt](how-to-create-a-windows-forms-control-that-shows-progress.md)
