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
# <a name="controls-with-built-in-owner-drawing-support"></a>Steuerelemente mit integrierter Ownerdrawing-Unterstützung
Ownerdrawing in Windows Forms, das auch als benutzerdefiniertes Zeichnen bezeichnet, ist ein Verfahren zum Ändern der Darstellung bestimmter Steuerelemente.  
  
> [!NOTE]
> Mit dem Wort "Steuerelement" in diesem Thema werden Klassen gemeint, die von oder abgeleitet werden <xref:System.Windows.Forms.Control> <xref:System.ComponentModel.Component> .  
  
 In der Regel verarbeitet Windows das Zeichnen automatisch mithilfe von Eigenschafts Einstellungen wie z <xref:System.Windows.Forms.Control.BackColor%2A> . b., um die Darstellung eines Steuer Elements zu bestimmen. Beim Ownerdrawing übernehmen Sie das Zeichnen und können Darstellungselemente ändern, die nicht mithilfe von Eigenschaften angepasst werden können. Beispielsweise kann bei zahlreichen Steuerelementen die Farbe des angezeigten Textes festgelegt werden. Dabei ist die Anzeige jedoch auf eine Farbe beschränkt. Das Ownerdrawing bietet beispielsweise die Möglichkeit, einen Teil des Textes schwarz und den anderen rot anzuzeigen.  
  
 In der Praxis ähnelt Ownerdrawing dem Zeichnen von Grafiken auf einem Formular. Sie können z. b. Grafik Methoden in einem Handler für das-Ereignis des Formulars verwenden, <xref:System.Windows.Forms.Control.Paint> um ein Steuerelement zu emulieren `ListBox` , aber Sie müssen eigenen Code schreiben, um die gesamte Benutzerinteraktion zu verarbeiten. Beim Ownerdrawing verwendet das Steuerelement den von Ihnen geschriebenen Code, um den Inhalt zu zeichnen, behält im Übrigen aber seine gesamte systeminterne Funktionalität bei. Sie können Grafikmethoden zum Zeichnen der einzelnen Elemente im Steuerelement oder zum Anpassen einiger Aspekte einzelner Elemente verwenden, während für andere Aspekte einzelner Elemente wiederum die Standarddarstellung übernommen werden kann.  
  
## <a name="owner-drawing-in-windows-forms-controls"></a>Ownerdrawing in Windows Forms-Steuerelementen  
 Um Ownerdrawing in Steuerelementen auszuführen, die diese Art des Zeichnens unterstützen, legen Sie normalerweise eine Eigenschaft fest und behandeln mindestens ein Ereignis.  
  
 Die meisten Steuerelemente mit Ownerdrawing-Unterstützung verfügen über die `OwnerDraw`-Eigenschaft oder `DrawMode`-Eigenschaft, die angibt, ob das Steuerelement eines oder mehrere zeichnungsbezogene Ereignisse auslöst, sobald es gezeichnet wird.  
  
 Zu den Steuerelementen, die keine `OwnerDraw`-Eigenschaft oder `DrawMode`-Eigenschaft aufweisen, gehört das `DataGridView`-Steuerelement, das automatisch ausgelöste Zeichnungsereignisse bereitstellt, sowie das `ToolStrip`-Steuerelement, das unter Verwendung einer externen Renderklasse gezeichnet wird, die eigene zeichnungsbezogene Ereignisse aufweist.  
  
 Es stehen viele verschiedene Arten von Zeichnungsereignissen zur Verfügung. Ein typisches Zeichnungsereignis tritt jedoch auf, wenn ein einzelnes Element innerhalb eines Steuerelements gezeichnet werden soll. Der Ereignishandler empfängt ein `EventArgs`-Objekt mit Informationen zum gezeichneten Element sowie zu den Tools, die zum Zeichnen verwendet werden können. Dieses Objekt enthält z. b. in der Regel die Indexnummer des Elements in der übergeordneten Auflistung, ein <xref:System.Drawing.Rectangle> -Objekt, das die Anzeige Grenzen des Elements angibt, und ein- <xref:System.Drawing.Graphics> Objekt zum Aufrufen von Paint-Methoden. Bei einigen Ereignissen umfasst das `EventArgs`-Objekt zusätzliche Informationen zum Element sowie zu den Methoden, die aufgerufen werden können, um einige Aspekte des Elements in der Standarddarstellung zu zeichnen, z. B. den Hintergrund oder ein Fokusrechteck.  
  
 Zum Erstellen eines wiederverwendbaren Steuerelements, das Ownerdrawing-Anpassungen enthält, erstellen Sie eine neue Klasse, die von einer Steuerelementklasse mit Ownerdrawing-Unterstützung abgeleitet ist. Anstatt Zeichnungsereignisse zu behandeln, sollten Sie Ownerdrawing-Code in Überschreibungen für mindestens eine geeignete `On`*EventName*-Methode in der neuen Klasse einfügen. Stellen Sie in diesem Fall sicher, dass die `On`*EventName*-Methoden der Basisklasse aufgerufen werden, damit Benutzer des Steuerelements Ownerdrawing-Ereignisse behandeln und weitere Anpassungen vornehmen können.  
  
 Die folgenden Windows Forms-Steuerelemente unterstützen Ownerdrawing in allen Versionen von .NET Framework:  
  
- <xref:System.Windows.Forms.ListBox>  
  
- <xref:System.Windows.Forms.ComboBox>  
  
- <xref:System.Windows.Forms.MenuItem> (verwendet von <xref:System.Windows.Forms.MainMenu> und <xref:System.Windows.Forms.ContextMenu> )  
  
- <xref:System.Windows.Forms.TabControl>  
  
 Die folgenden Steuerelemente unterstützen das Zeichnen von Besitzern nur in .NET Framework 2,0:  
  
- <xref:System.Windows.Forms.ToolTip>  
  
- <xref:System.Windows.Forms.ListView>  
  
- <xref:System.Windows.Forms.TreeView>  
  
 Die folgenden Steuerelemente unterstützen das Zeichnen von Besitzern und sind neu in .NET Framework 2,0:  
  
- <xref:System.Windows.Forms.DataGridView>  
  
- <xref:System.Windows.Forms.ToolStrip>  
  
 Die folgenden Abschnitte enthalten zusätzliche Details zu jedem dieser Steuerelemente.  
  
### <a name="listbox-and-combobox-controls"></a>Die Steuerelemente ListBox und ComboBox  
 Mit <xref:System.Windows.Forms.ListBox> den <xref:System.Windows.Forms.ComboBox> Steuerelementen und können Sie einzelne Elemente im Steuerelement entweder in einer Größe oder in unterschiedlichen Größen zeichnen.  
  
> [!NOTE]
> Obwohl das- <xref:System.Windows.Forms.CheckedListBox> Steuerelement vom-Steuerelement abgeleitet ist, wird das Zeichnen von <xref:System.Windows.Forms.ListBox> Besitzern nicht unterstützt.  
  
 Um jedes Element in derselben Größe zu zeichnen, legen `DrawMode` Sie die-Eigenschaft auf fest <xref:System.Windows.Forms.DrawMode.OwnerDrawFixed> und behandeln das- `DrawItem` Ereignis.  
  
 Um jedes Element mit einer anderen Größe zu zeichnen, legen Sie die `DrawMode` -Eigenschaft auf fest <xref:System.Windows.Forms.DrawMode.OwnerDrawVariable> und behandeln sowohl das `MeasureItem` -als auch das- `DrawItem` Ereignis. Mit dem `MeasureItem`-Ereignis können Sie die Größe eines Elements angeben, bevor das `DrawItem`-Ereignis für das jeweilige Element auftritt.  
  
 Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Themen:  
  
- <xref:System.Windows.Forms.ListBox.DrawMode%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ListBox.MeasureItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ListBox.DrawItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ComboBox.DrawMode%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ComboBox.MeasureItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ComboBox.DrawItem?displayProperty=nameWithType>  
  
- [Vorgehensweise: Erstellen von Text mit variabler Größe in einem ComboBox-Steuerelement](how-to-create-variable-sized-text-in-a-combobox-control.md)  
  
### <a name="menuitem-component"></a>MenuItem-Komponente  
 Die <xref:System.Windows.Forms.MenuItem> Komponente stellt ein einzelnes Menü Element in einer- <xref:System.Windows.Forms.MainMenu> oder- <xref:System.Windows.Forms.ContextMenu> Komponente dar.  
  
 Um einen zu zeichnen <xref:System.Windows.Forms.MenuItem> , legen `OwnerDraw` Sie seine-Eigenschaft auf fest `true` und behandeln das zugehörige- `DrawItem` Ereignis Um die Größe des Menüelements anzupassen, bevor das `DrawItem`-Ereignis auftritt, behandeln Sie das `MeasureItem`-Ereignis des Elements.  
  
 Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Referenzthemen:  
  
- <xref:System.Windows.Forms.MenuItem.OwnerDraw%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.MenuItem.DrawItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.MenuItem.MeasureItem?displayProperty=nameWithType>  
  
### <a name="tabcontrol-control"></a>TabControl-Steuerelement  
 Das- <xref:System.Windows.Forms.TabControl> Steuerelement ermöglicht es Ihnen, einzelne Registerkarten im-Steuerelement zu zeichnen. Besitzer Zeichnung wirkt sich nur auf die Registerkarten aus; der <xref:System.Windows.Forms.TabPage> Inhalt ist nicht betroffen.  
  
 Wenn Sie jede Registerkarte in einem zeichnen möchten <xref:System.Windows.Forms.TabControl> , legen `DrawMode` Sie die-Eigenschaft auf fest <xref:System.Windows.Forms.TabDrawMode.OwnerDrawFixed> und behandeln das- `DrawItem` Ereignis. Dieses Ereignis tritt jeweils einmal für jede Registerkarte auf, jedoch nur dann, wenn die Registerkarte im Steuerelement sichtbar ist.  
  
 Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Referenzthemen:  
  
- <xref:System.Windows.Forms.TabControl.DrawMode%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.TabControl.DrawItem?displayProperty=nameWithType>  
  
### <a name="tooltip-component"></a>ToolTip-Komponente  
 Mit der- <xref:System.Windows.Forms.ToolTip> Komponente können Sie die gesamte QuickInfo zeichnen, wenn Sie angezeigt wird.  
  
 Um einen zu zeichnen <xref:System.Windows.Forms.ToolTip> , legen `OwnerDraw` Sie seine-Eigenschaft auf fest `true` und behandeln das zugehörige- `Draw` Ereignis Um die Größe von <xref:System.Windows.Forms.ToolTip> vor dem Auftreten des `Draw` Ereignisses anzupassen, behandeln Sie das `Popup` -Ereignis, und legen Sie die- <xref:System.Windows.Forms.PopupEventArgs.ToolTipSize%2A> Eigenschaft im-Ereignishandler fest.  
  
 Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Referenzthemen:  
  
- <xref:System.Windows.Forms.ToolTip.OwnerDraw%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ToolTip.Draw?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ToolTip.Popup?displayProperty=nameWithType>  
  
### <a name="listview-control"></a>ListView-Steuerelement  
 Das- <xref:System.Windows.Forms.ListView> Steuerelement ermöglicht es Ihnen, einzelne Elemente, unter Elemente und Spaltenheader im-Steuerelement zu zeichnen.  
  
 Um Ownerdrawing im Steuerelement zu aktivieren, legen Sie die `OwnerDraw`-Eigenschaft `true` fest.  
  
 Um jedes Element im Steuerelement zu zeichnen, behandeln Sie das `DrawItem`-Ereignis.  
  
 Um jeden Unterelement-oder Spaltenheader im-Steuerelement zu zeichnen <xref:System.Windows.Forms.ListView.View%2A> , wenn die-Eigenschaft auf festgelegt ist <xref:System.Windows.Forms.View.Details> , behandeln Sie die `DrawSubItem` `DrawColumnHeader` Ereignisse und.  
  
 Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Referenzthemen:  
  
- <xref:System.Windows.Forms.ListView.OwnerDraw%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ListView.DrawItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ListView.DrawSubItem?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.ListView.DrawColumnHeader?displayProperty=nameWithType>  
  
### <a name="treeview-control"></a>TreeView-Steuerelement  
 Das- <xref:System.Windows.Forms.TreeView> Steuerelement ermöglicht es Ihnen, einzelne Knoten im-Steuerelement zu zeichnen.  
  
 Wenn Sie nur den in jedem Knoten angezeigten Text zeichnen möchten, legen Sie die `DrawMode` -Eigenschaft auf fest <xref:System.Windows.Forms.TreeViewDrawMode.OwnerDrawText> und behandeln das- `DrawNode` Ereignis, um den Text zu zeichnen.  
  
 Um alle Elemente der einzelnen Knoten zu zeichnen, legen `DrawMode` Sie die-Eigenschaft auf fest <xref:System.Windows.Forms.TreeViewDrawMode.OwnerDrawAll> und behandeln das- `DrawNode` Ereignis, um die Elemente zu zeichnen, die Sie benötigen, z. b. Text, Symbole, Kontrollkästchen, plus-und Minuszeichen sowie Zeilen, die die Knoten verbinden.  
  
 Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Referenzthemen:  
  
- <xref:System.Windows.Forms.TreeView.DrawMode%2A?displayProperty=nameWithType>  
  
- <xref:System.Windows.Forms.TreeView.DrawNode?displayProperty=nameWithType>  
  
### <a name="datagridview-control"></a>DataGridView-Steuerelement  
 Das <xref:System.Windows.Forms.DataGridView> -Steuerelement ermöglicht es Ihnen, einzelne Zellen und Zeilen im-Steuerelement zu zeichnen.  
  
 Um einzelne Zellen zu zeichnen, behandeln Sie das `CellPainting`-Ereignis.  
  
 Um einzelne Zeilen oder Zeilenelemente zu zeichnen, behandeln Sie das `RowPrePaint`- und/oder `RowPostPaint`-Ereignis. Das `RowPrePaint`-Ereignis tritt vor dem Zeichnen der Zellen in einer Zeile und das `RowPostPaint`-Ereignis danach auf. Sie können beide Ereignisse und das `CellPainting`-Ereignis behandeln, um den Zeilenhintergrund, einzelne Zellen sowie den Zeilenvordergrund separat zu zeichnen. Alternativ können Sie für bestimmte Elemente spezielle Anpassungen bereitstellen und für die übrigen Zeilenelemente die Standarddarstellung verwenden.  
  
 Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Themen:  
  
- <xref:System.Windows.Forms.DataGridView.CellPainting>  
  
- <xref:System.Windows.Forms.DataGridView.RowPrePaint>  
  
- <xref:System.Windows.Forms.DataGridView.RowPostPaint>  
  
- [Gewusst wie: Anpassen der Darstellung von Zellen im DataGridView-Steuerelement von Windows Forms](customize-the-appearance-of-cells-in-the-datagrid.md)  
  
- [Vorgehensweise: Anpassen der Darstellung von Zeilen im DataGridView-Steuerelement in Windows Forms](customize-the-appearance-of-rows-in-the-datagrid.md)  
  
### <a name="toolstrip-control"></a>ToolStrip-Steuerelement  
 <xref:System.Windows.Forms.ToolStrip> und abgeleitete Steuerelemente ermöglichen es Ihnen, beliebige Aspekte ihrer Darstellung anzupassen.  
  
 Wenn Sie benutzerdefiniertes Rendering für Steuerelemente bereitstellen möchten <xref:System.Windows.Forms.ToolStrip> , legen Sie die `Renderer` -Eigenschaft eines <xref:System.Windows.Forms.ToolStrip> , <xref:System.Windows.Forms.ToolStripManager> , <xref:System.Windows.Forms.ToolStripPanel> oder <xref:System.Windows.Forms.ToolStripContentPanel> auf ein `ToolStripRenderer` -Objekt fest, und behandeln Sie mindestens eines der vielen von der-Klasse bereitgestellten Zeichnungs Ereignisse `ToolStripRenderer` . Alternativ können Sie eine- `Renderer` Eigenschaft auf eine Instanz Ihrer eigenen Klasse festlegen, `ToolStripRenderer` die von, oder abgeleitet ist, <xref:System.Windows.Forms.ToolStripProfessionalRenderer> <xref:System.Windows.Forms.ToolStripSystemRenderer> die bestimmte `On` *EventName* -Methoden implementiert oder überschreibt.  
  
 Weitere Informationen, einschließlich Codebeispiele, finden Sie unter den folgenden Themen:  
  
- <xref:System.Windows.Forms.ToolStripRenderer>  
  
- [Gewusst wie: Erstellen und Festlegen eines benutzerdefinierten Renderers für das ToolStrip-Steuerelement in Windows Forms](create-and-set-a-custom-renderer-for-the-toolstrip-control-in-wf.md)  
  
- [Vorgehensweise: Benutzerdefiniertes Zeichnen eines ToolStrip-Steuerelements](how-to-custom-draw-a-toolstrip-control.md)  
  
## <a name="see-also"></a>Siehe auch

- [Steuerelemente für Windows Forms](controls-to-use-on-windows-forms.md)
