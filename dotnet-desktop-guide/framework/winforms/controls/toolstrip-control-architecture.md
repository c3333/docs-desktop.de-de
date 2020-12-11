---
title: Architektur des ToolStrip-Steuerelements
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStrip control [Windows Forms], architecture
ms.assetid: 71df2d18-862e-4701-9ff9-c1fe606f94f2
ms.openlocfilehash: d0a1441e9bae8d2c1f938e7399c11e736708da4d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977177"
---
# <a name="toolstrip-control-architecture"></a>Architektur des ToolStrip-Steuerelements

Die <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.ToolStripItem> Klassen und stellen ein flexibles, erweiterbares System zum Anzeigen von Symbolleisten-, Status-und Menü Elementen bereit. Diese Klassen sind alle im <xref:System.Windows.Forms> -Namespace enthalten. Sie werden in der Regel mit dem Präfix "ToolStrip" (z. b. <xref:System.Windows.Forms.ToolStripOverflow> ) oder mit dem Suffix "Strip" benannt (z <xref:System.Windows.Forms.MenuStrip> . b.).

## <a name="toolstrip"></a>ToolStrip

In den folgenden Themen werden <xref:System.Windows.Forms.ToolStrip> und die Steuerelemente beschrieben, die davon abgeleitet sind.

<xref:System.Windows.Forms.ToolStrip> ist die abstrakte Basisklasse für <xref:System.Windows.Forms.MenuStrip> , <xref:System.Windows.Forms.StatusStrip> und <xref:System.Windows.Forms.ContextMenuStrip> . Das folgende Objektmodell zeigt die <xref:System.Windows.Forms.ToolStrip> Vererbungs Hierarchie.

![Diagramm, das das ToolStrip-Objektmodell anzeigt.](./media/toolstrip-control-architecture/toolstrip-object-model.gif)

Sie können auf alle Elemente in einem über die-Auflistung zugreifen <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.ToolStrip.Items%2A> . Sie können auf alle Elemente in einem über die-Auflistung zugreifen <xref:System.Windows.Forms.ToolStripDropDownItem> <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItems%2A> . In einer von abgeleiteten Klasse <xref:System.Windows.Forms.ToolStrip> können Sie auch die- <xref:System.Windows.Forms.ToolStrip.DisplayedItems%2A> Eigenschaft verwenden, um nur auf die gegenwärtig angezeigten Elemente zuzugreifen. Dies sind die Elemente, die sich derzeit nicht in einem Überlauf Menü befinden.

Die folgenden Elemente sind speziell für die nahtlose Zusammenarbeit mit <xref:System.Windows.Forms.ToolStripSystemRenderer> und <xref:System.Windows.Forms.ToolStripProfessionalRenderer> in allen Ausrichtungen konzipiert. Sie sind standardmäßig zur Entwurfszeit für das- <xref:System.Windows.Forms.ToolStrip> Steuerelement verfügbar:

- <xref:System.Windows.Forms.ToolStripButton>

- <xref:System.Windows.Forms.ToolStripSeparator>

- <xref:System.Windows.Forms.ToolStripLabel>

- <xref:System.Windows.Forms.ToolStripDropDownButton>

- <xref:System.Windows.Forms.ToolStripSplitButton>

- <xref:System.Windows.Forms.ToolStripTextBox>

- <xref:System.Windows.Forms.ToolStripComboBox>

### <a name="menustrip"></a>MenuStrip

<xref:System.Windows.Forms.MenuStrip> ist der Container der obersten Ebene, der den ablöst <xref:System.Windows.Forms.MainMenu> . Außerdem werden Schlüssel Behandlung und MDI-Funktionen (Multiple Document Interface) bereitstellt. Funktional <xref:System.Windows.Forms.ToolStripDropDownItem> und <xref:System.Windows.Forms.ToolStripMenuItem> funktionieren zusammen mit <xref:System.Windows.Forms.MenuStrip> , obwohl Sie von abgeleitet sind <xref:System.Windows.Forms.ToolStripItem> .

Die folgenden Elemente sind speziell für die nahtlose Zusammenarbeit mit <xref:System.Windows.Forms.ToolStripSystemRenderer> und <xref:System.Windows.Forms.ToolStripProfessionalRenderer> in allen Ausrichtungen konzipiert. Sie sind standardmäßig zur Entwurfszeit für das- <xref:System.Windows.Forms.MenuStrip> Steuerelement verfügbar:

- <xref:System.Windows.Forms.ToolStripMenuItem>

- <xref:System.Windows.Forms.ToolStripTextBox>

- <xref:System.Windows.Forms.ToolStripComboBox>

### <a name="statusstrip"></a>StatusStrip

<xref:System.Windows.Forms.StatusStrip> ersetzt das- <xref:System.Windows.Forms.StatusBar> Steuerelement. Zu den besonderen Features von <xref:System.Windows.Forms.StatusStrip> gehören ein benutzerdefiniertes Tabellenlayout, Unterstützung für die Größenanpassung und das Verschieben des Formulars sowie die- `Spring` Eigenschaft, mit der ein <xref:System.Windows.Forms.ToolStripStatusLabel> verfügbarer Speicher automatisch aufgefüllt werden kann.

Die folgenden Elemente sind speziell für die nahtlose Zusammenarbeit mit <xref:System.Windows.Forms.ToolStripSystemRenderer> und <xref:System.Windows.Forms.ToolStripProfessionalRenderer> in allen Ausrichtungen konzipiert. Sie sind standardmäßig zur Entwurfszeit für das- <xref:System.Windows.Forms.StatusStrip> Steuerelement verfügbar:

- <xref:System.Windows.Forms.ToolStripStatusLabel>

- <xref:System.Windows.Forms.ToolStripDropDownButton>

- <xref:System.Windows.Forms.ToolStripSplitButton>

- <xref:System.Windows.Forms.ToolStripProgressBar>

### <a name="contextmenustrip"></a>ContextMenuStrip

<xref:System.Windows.Forms.ContextMenuStrip> ersetzt <xref:System.Windows.Forms.ContextMenu>. Sie können einem <xref:System.Windows.Forms.ContextMenuStrip> beliebiges Steuerelement einen zuordnen, und mit der rechten Maustaste wird automatisch das Kontextmenü (oder das Kontextmenü) angezeigt. Sie können einen <xref:System.Windows.Forms.ContextMenuStrip> Programm gesteuert mithilfe der- <xref:System.Windows.Forms.ToolStripDropDown.Show%2A> Methode anzeigen. <xref:System.Windows.Forms.ContextMenuStrip> unterstützt abgebrochen <xref:System.Windows.Forms.ToolStripDropDown.Opening> -und-Ereignisse zur Behandlung dynamischer auffüllungs-und <xref:System.Windows.Forms.ToolStripDropDown.Closing> multiclick-Szenarios. <xref:System.Windows.Forms.ContextMenuStrip> unterstützt Bilder, den Zustand der Menü Element Überprüfung, Text, Zugriffstasten, Verknüpfungen und Kaskadierende Menüs.

Die folgenden Elemente sind speziell für die nahtlose Zusammenarbeit mit <xref:System.Windows.Forms.ToolStripSystemRenderer> und <xref:System.Windows.Forms.ToolStripProfessionalRenderer> in allen Ausrichtungen konzipiert. Sie sind standardmäßig zur Entwurfszeit für das- <xref:System.Windows.Forms.ContextMenuStrip> Steuerelement verfügbar:

- <xref:System.Windows.Forms.ToolStripMenuItem>

- <xref:System.Windows.Forms.ToolStripSeparator>

- <xref:System.Windows.Forms.ToolStripTextBox>

- <xref:System.Windows.Forms.ToolStripComboBox>

### <a name="toolstrip-generic-features"></a>Generische Funktionen von ToolStrip

In den folgenden Themen werden Funktionen und das Verhalten beschrieben, die für die <xref:System.Windows.Forms.ToolStrip> abgeleiteten Steuerelemente und generisch sind.

#### <a name="painting"></a>Be

Es gibt mehrere Möglichkeiten, benutzerdefinierte Zeichen in Steuerelementen zu zeichnen <xref:System.Windows.Forms.ToolStrip> . Wie bei anderen Windows Forms-Steuerelementen <xref:System.Windows.Forms.ToolStrip> verfügen sowohl die-als auch die- <xref:System.Windows.Forms.ToolStripItem> Methode über schreibbare `OnPaint` Methoden und `Paint` Ereignisse. Wie bei der regulären Darstellung ist das Koordinatensystem relativ zum Client Bereich des Steuer Elements. Das heißt, die linke obere Ecke des Steuer Elements ist 0, 0. Das `Paint` Ereignis und die `OnPaint` Methode für ein <xref:System.Windows.Forms.ToolStripItem> Verhalten sich wie andere Steuerelemente zum Zeichnen von Steuerelementen.

Die-Steuer <xref:System.Windows.Forms.ToolStrip> Elemente bieten außerdem einen präziseteren Zugriff auf das Rendering der Elemente und des Containers über die- <xref:System.Windows.Forms.ToolStripRenderer> Klasse, die über schreibbare Methoden zum Zeichnen von Hintergrund, Element Hintergrund, Element Bild, Element Pfeil, Element Text und Rahmen des enthält <xref:System.Windows.Forms.ToolStrip> . Die Ereignis Argumente für diese Methoden machen verschiedene Eigenschaften verfügbar, z. b. Rechtecke, Farben und Textformate, die Sie nach Bedarf anpassen können.

Um nur einige Aspekte der Art und Weise anzupassen, wie ein Element gezeichnet wird, überschreiben Sie in der Regel den <xref:System.Windows.Forms.ToolStripRenderer> .

Wenn Sie ein neues Element schreiben und alle Aspekte des Bildes steuern möchten, überschreiben Sie die- `OnPaint` Methode. Innerhalb von `OnPaint` können Sie Methoden aus der verwenden <xref:System.Windows.Forms.ToolStripRenderer> .

Standardmäßig ist der <xref:System.Windows.Forms.ToolStrip> doppelt gepuffert und nutzt die- <xref:System.Windows.Forms.ControlStyles.OptimizedDoubleBuffer> Einstellung.

#### <a name="parenting"></a>Geordnet

Das Konzept von Container Besitz und-Verarbeitung ist in Steuer <xref:System.Windows.Forms.ToolStrip> Elementen komplexer als in anderen Windows Forms Container-Steuerelementen. Dies ist für die Unterstützung dynamischer Szenarien erforderlich, wie z. b. Überlauf, Freigabe von Dropdown Elementen über mehrere <xref:System.Windows.Forms.ToolStrip> Elemente hinweg und Unterstützung der Generierung eines <xref:System.Windows.Forms.ContextMenuStrip> von einem-Steuerelement.

In der folgenden Liste werden die Elemente beschrieben, die sich auf die über-und deren Verwendung beziehen.

- <xref:System.Windows.Forms.ToolStripDropDown.OwnerItem%2A> greift auf das Element zu, bei dem es sich um die Quelle des Dropdown Elements handelt. Dies ist vergleichbar mit <xref:System.Windows.Forms.ContextMenuStrip.SourceControl%2A> , aber anstelle eines-Steuer Elements wird ein zurückgegeben <xref:System.Windows.Forms.ToolStripItem> .

- <xref:System.Windows.Forms.ContextMenuStrip.SourceControl%2A> bestimmt, welches Steuerelement die Quelle von ist, <xref:System.Windows.Forms.ContextMenuStrip> Wenn mehrere Steuerelemente gleich sind <xref:System.Windows.Forms.ContextMenuStrip> .

- <xref:System.Windows.Forms.ToolStripItem.GetCurrentParent%2A> ist ein Schreib geschützter Accessor für die- <xref:System.Windows.Forms.ToolStripItem.Parent%2A> Eigenschaft. Ein übergeordnetes Element unterscheidet sich von einem Besitzer darin, dass ein übergeordnetes Element den zurückgegebenen aktuellen angibt <xref:System.Windows.Forms.ToolStrip> , in dem das Element angezeigt wird, das möglicherweise im Überlauf Bereich angezeigt wird.

- <xref:System.Windows.Forms.ToolStripItem.Owner%2A> Gibt das-Element zurück, <xref:System.Windows.Forms.ToolStrip> dessen Items-Auflistung den aktuellen enthält <xref:System.Windows.Forms.ToolStripItem> . Dies ist die beste Möglichkeit, auf <xref:System.Windows.Forms.ToolStrip.ImageList%2A> oder andere Eigenschaften in der obersten Ebene zu verweisen, <xref:System.Windows.Forms.ToolStrip> ohne speziellen Code zum Behandeln von Überlauf zu schreiben.

#### <a name="behavior-of-inherited-controls"></a>Verhalten von geerbten Steuerelementen

Die folgenden Steuerelemente werden gesperrt, wenn Sie in Vererbung verwendet werden:

- <xref:System.Windows.Forms.ToolStrip>

- <xref:System.Windows.Forms.MenuStrip>

- <xref:System.Windows.Forms.ContextMenuStrip>

- <xref:System.Windows.Forms.StatusStrip>

- <xref:System.Windows.Forms.ToolStripPanel> , die die Bereiche eines <xref:System.Windows.Forms.ToolStripContainer> und auch einzelner Steuer <xref:System.Windows.Forms.ToolStripPanel> Elemente enthält.

Erstellen Sie z. b. eine neue Windows Forms Anwendung, indem Sie eines oder mehrere der Steuerelemente in der vorherigen Liste verwenden. Legen Sie den Zugriffsmodifizierer für ein oder mehrere Steuerelemente auf `public` oder fest `protected` , und erstellen Sie dann das Projekt. Fügen Sie ein Formular hinzu, das vom ersten Formular erbt, und wählen Sie dann ein geerbtes Steuerelement aus. Das-Steuerelement wird als gesperrt angezeigt `private`

#### <a name="toolstripcontainer-support-of-inheritance"></a>ToolStripContainer-Unterstützung für Vererbung

Das- <xref:System.Windows.Forms.ToolStripContainer> Steuerelement unterstützt eingeschränkte geerbte Szenarien, ähnlich wie im folgenden Beispiel:

1. Erstellen Sie eine neue Windows Forms-Anwendung.

2. Fügen Sie dem Formular eine <xref:System.Windows.Forms.ToolStripContainer> hinzu.

3. Legen Sie den Zugriffsmodifizierer von <xref:System.Windows.Forms.ToolStripContainer> auf `public` oder fest `protected` .

4. Fügen Sie den Bereichen des eine beliebige Kombination von <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.MenuStrip> -,-und-Steuer <xref:System.Windows.Forms.ContextMenuStrip> Elementen hinzu <xref:System.Windows.Forms.ToolStripPanel> <xref:System.Windows.Forms.ToolStripContainer> .

5. Erstellen Sie das Projekt.

6. Fügen Sie ein Formular hinzu, das vom ersten Formular erbt.

7. Wählen Sie die geerbte <xref:System.Windows.Forms.ToolStripContainer> im Formular aus.

#### <a name="inherited-behavior-of-child-controls"></a>Vererbte Verhalten von untergeordneten Steuerelementen

Nachdem Sie die vorherigen Schritte ausgeführt haben, tritt das folgende geerbte Verhalten auf:

- Im Designer wird das-Steuerelement mit einem geerbten Symbol angezeigt.

- Die Steuer <xref:System.Windows.Forms.ToolStripPanel> Elemente sind gesperrt. Sie können ihren Inhalt nicht auswählen oder neu anordnen.

- Sie können der Steuerelemente hinzufügen <xref:System.Windows.Forms.ToolStripContentPanel> , die Steuerelemente verschieben und Sie als untergeordnete Steuerelemente des-Elements festlegen <xref:System.Windows.Forms.ToolStripContentPanel> .

- Die Änderungen bleiben nach dem Erstellen des Formulars erhalten.

  > [!NOTE]
  > Entfernen Sie die Zugriffsmodifizierer aus allen Steuer <xref:System.Windows.Forms.ToolStripPanel> Elementen, die Teil eines sind <xref:System.Windows.Forms.ToolStripContainer> . Der Zugriffsmodifizierer des <xref:System.Windows.Forms.ToolStripContainer> steuert das gesamte Steuerelement.

#### <a name="partial-trust"></a>Teilweise Vertrauenswürdigkeit

Die Einschränkungen von `ToolStrip` s bei teilweiser Vertrauenswürdigkeit sind so konzipiert, dass ein unbeabsichtigter Eintrag persönlicher Informationen vermieden wird, die möglicherweise von nicht autorisierten Personen oder Diensten verwendet werden. Die Schutzmaßnahmen lauten wie folgt:

- `ToolStripDropDown` -Steuerelemente erfordern <xref:System.Security.Permissions.UIPermissionWindow.AllWindows> , dass Elemente in einer angezeigt werden <xref:System.Windows.Forms.ToolStripControlHost> . Dies gilt sowohl für systeminterne Steuerelemente <xref:System.Windows.Forms.ToolStripTextBox> , wie z. b., und, als <xref:System.Windows.Forms.ToolStripComboBox> <xref:System.Windows.Forms.ToolStripProgressBar> auch für Benutzer erstellte Steuerelemente. Wenn diese Anforderung nicht erfüllt wird, werden diese Elemente nicht angezeigt. Es werden keine Ausnahmen ausgelöst.

- Das Festlegen der <xref:System.Windows.Forms.ToolStripDropDown.AutoClose%2A> -Eigenschaft auf `false` ist nicht zulässig, und der abgebrochen- <xref:System.Windows.Forms.ToolStripDropDown.Closing> Ereignis Parameter wird ignoriert. Dadurch ist es unmöglich, mehr als einen Tastatur Strich einzugeben, ohne das Dropdown Element zu verwerfen. Wenn diese Anforderung nicht erfüllt wird, werden diese Elemente nicht angezeigt. Es werden keine Ausnahmen ausgelöst.

- Viele Tastatur Schlag Ereignisse werden nicht ausgelöst, wenn Sie in teilweise vertrauenswürdigen Kontexten als auftreten <xref:System.Security.Permissions.UIPermissionWindow.AllWindows> .

- Zugriffsschlüssel werden nicht verarbeitet, wenn <xref:System.Security.Permissions.UIPermissionWindow.AllWindows> nicht gewährt wird.

#### <a name="usage"></a>Verwendung

Die folgenden Verwendungs Muster haben einen Einfluss auf <xref:System.Windows.Forms.ToolStrip> Layout, Tastatur Interaktion und Endbenutzer Verhalten:

- Verknüpft in <xref:System.Windows.Forms.ToolStripPanel>

  Der <xref:System.Windows.Forms.ToolStrip> kann innerhalb von <xref:System.Windows.Forms.ToolStripPanel> und über s neu positioniert werden <xref:System.Windows.Forms.ToolStripPanel> . Die `Dock` -Eigenschaft wird ignoriert, und wenn die-Eigenschaft den Wert <xref:System.Windows.Forms.ToolStrip.Stretch%2A> hat, wird die `false` Größe der Vergrößerung vergrößert <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.ToolStripPanel> . In der Regel ist der nicht an der Aktivier <xref:System.Windows.Forms.ToolStrip> Reihenfolge beteiligt.

- Angedockt

  Die <xref:System.Windows.Forms.ToolStrip> wird auf einer Seite eines Containers an einer festgelegten Position platziert, und die Größe wird über den gesamten Rand erweitert, an dem Sie angedockt ist. In der Regel ist der nicht an der Aktivier <xref:System.Windows.Forms.ToolStrip> Reihenfolge beteiligt.

- Absolut positioniert

  Die <xref:System.Windows.Forms.ToolStrip> ähnelt anderen Steuerelementen, da Sie von der-Eigenschaft platziert wird <xref:System.Windows.Forms.Control.Location%2A> , eine festgelegte Größe aufweist und in der Regel an der Aktivier Reihenfolge teilnimmt.

#### <a name="keyboard-interaction"></a>Tastatur Interaktion

##### <a name="access-keys"></a>Zugriffsschlüssel

In Kombination mit oder nach der Alt-Taste sind Zugriffstasten eine Möglichkeit zum Aktivieren eines Steuer Elements über die Tastatur. <xref:System.Windows.Forms.ToolStrip> unterstützt sowohl explizite als auch implizite Zugriffsschlüssel. Eine explizite Definition verwendet ein kaufmännisches und-Zeichen (&), das dem Buchstaben vorangestellt ist. Die implizite Definition verwendet einen Algorithmus, der versucht, ein übereinstimmendes Element auf Grundlage der Reihenfolge der Zeichen in einer bestimmten Eigenschaft zu finden `Text` .

##### <a name="shortcut-keys"></a>Tastenkombinationen

Die Tastenkombinationen, die von einem verwendet werden <xref:System.Windows.Forms.MenuStrip> , verwenden eine Kombination aus der- <xref:System.Windows.Forms.Keys> Enumeration (die nicht Reihen folgen spezifisch ist), um die Tastenkombination zu definieren. Sie können auch die- <xref:System.Windows.Forms.ToolStripMenuItem.ShortcutKeyDisplayString%2A> Eigenschaft verwenden, um eine Tastenkombination mit nur einem Text anzuzeigen, z. b. "del" anstelle von "Delete".

##### <a name="navigation"></a>Navigation

Die Alt-Taste aktiviert den <xref:System.Windows.Forms.MenuStrip> , auf den von gezeigt wird <xref:System.Windows.Forms.Form.MainMenuStrip%2A> . Von dort aus werden STRG + TAB zwischen Steuer <xref:System.Windows.Forms.ToolStrip> Elementen in `ToolStripPanel` s navigiert. Die Tab-Taste und die Pfeiltasten auf der numerischen Tastatur werden zwischen den Elementen in einem navigiert <xref:System.Windows.Forms.ToolStrip> . Ein spezieller Algorithmus behandelt die Navigation im Überlauf Bereich. Leertaste wählt <xref:System.Windows.Forms.ToolStripButton> , <xref:System.Windows.Forms.ToolStripDropDownButton> oder aus <xref:System.Windows.Forms.ToolStripSplitButton> .

##### <a name="focus-and-validation"></a>Fokus und Validierung

Bei Aktivierung durch die Alt-Taste wird <xref:System.Windows.Forms.MenuStrip> der <xref:System.Windows.Forms.ToolStrip> Fokus von oder in der Regel weder von dem Steuerelement entfernt, das derzeit den Fokus besitzt. Wenn ein-Steuerelement innerhalb <xref:System.Windows.Forms.MenuStrip> von oder in einem Dropdown Element von gehostet wird <xref:System.Windows.Forms.MenuStrip> , erhält das Steuerelement den Fokus, wenn der Benutzer die Tab-Taste drückt. Im Allgemeinen werden die <xref:System.Windows.Forms.Control.GotFocus> <xref:System.Windows.Forms.Control.LostFocus> -, <xref:System.Windows.Forms.Control.Enter> -,-und- <xref:System.Windows.Forms.Control.Leave> Ereignisse von <xref:System.Windows.Forms.MenuStrip> möglicherweise nicht ausgelöst, wenn Sie von der Tastatur aktiviert werden. Verwenden Sie in solchen Fällen <xref:System.Windows.Forms.MenuStrip.MenuActivate> stattdessen das-Ereignis und das- <xref:System.Windows.Forms.MenuStrip.MenuDeactivate> Ereignis.

Standardmäßig <xref:System.Windows.Forms.ToolStrip.CausesValidation%2A> ist `false` . Geben Sie <xref:System.Windows.Forms.ContainerControl.Validate%2A> explizit auf dem Formular ein, um die Validierung auszuführen.

#### <a name="layout"></a>Layout

Sie steuern das <xref:System.Windows.Forms.ToolStrip> Layout, indem Sie eines der Member von <xref:System.Windows.Forms.ToolStripLayoutStyle> mit der-Eigenschaft auswählen <xref:System.Windows.Forms.ToolStrip.LayoutStyle%2A> .

##### <a name="stack-layouts"></a>Stapel Layouts

Das Stapeln ist das Anordnen von Elementen an beiden Enden von nebeneinander <xref:System.Windows.Forms.ToolStrip> . In der folgenden Liste werden die Stapel Layouts beschrieben.

- <xref:System.Windows.Forms.ToolStripLayoutStyle.StackWithOverflow> ist die Standardoption. Diese Einstellung bewirkt, dass das <xref:System.Windows.Forms.ToolStrip> Layout automatisch in Übereinstimmung mit der- <xref:System.Windows.Forms.ToolStrip.Orientation%2A> Eigenschaft ändert, um Drag & amp; Andock Szenarios zu verarbeiten.

- <xref:System.Windows.Forms.ToolStripLayoutStyle.VerticalStackWithOverflow> Rendert die <xref:System.Windows.Forms.ToolStrip> Elemente nebeneinander nebeneinander.

- <xref:System.Windows.Forms.ToolStripLayoutStyle.HorizontalStackWithOverflow> Rendert die <xref:System.Windows.Forms.ToolStrip> Elemente nebeneinander nebeneinander.

##### <a name="other-features-of-stack-layouts"></a>Weitere Features von Stapel Layouts

<xref:System.Windows.Forms.ToolStripItem.Alignment%2A> bestimmt das Ende der <xref:System.Windows.Forms.ToolStrip> , an die das Element ausgerichtet wird.

Wenn Elemente nicht in passen <xref:System.Windows.Forms.ToolStrip> , wird automatisch eine Überlauf Schaltfläche angezeigt. Die- <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> Eigenschafts Einstellung bestimmt, ob ein Element immer, bei Bedarf im Überlauf Bereich angezeigt wird, oder nie.

Im- <xref:System.Windows.Forms.ToolStrip.LayoutCompleted> Ereignis können Sie die-Eigenschaft überprüfen, <xref:System.Windows.Forms.ToolStripItem.Placement%2A> um zu bestimmen, ob ein Element auf dem Haupt- <xref:System.Windows.Forms.ToolStrip> , dem Überlauf <xref:System.Windows.Forms.ToolStrip> oder derzeit überhaupt nicht angezeigt wird. Der typische Grund, warum ein Element nicht angezeigt wird, ist, dass das Element nicht in den Haupt <xref:System.Windows.Forms.ToolStrip> -und dessen- <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> Eigenschaft auf festgelegt wurde <xref:System.Windows.Forms.ToolStripItemOverflow.Never> .

<xref:System.Windows.Forms.ToolStrip>Verschieben Sie einen verschiebbaren Wert, indem Sie ihn in einem einfügen <xref:System.Windows.Forms.ToolStripPanel> und dessen <xref:System.Windows.Forms.ToolStrip.GripStyle%2A> auf festlegen <xref:System.Windows.Forms.ToolStripGripStyle.Visible> .

##### <a name="other-layout-options"></a>Weitere Layoutoptionen

Die anderen Layoutoptionen sind <xref:System.Windows.Forms.ToolStripLayoutStyle.Flow> und <xref:System.Windows.Forms.ToolStripLayoutStyle.Table> .

##### <a name="flow-layout"></a>Flusslayout

<xref:System.Windows.Forms.ToolStripLayoutStyle.Flow> Layout ist die Standardeinstellung für <xref:System.Windows.Forms.ContextMenuStrip> , <xref:System.Windows.Forms.ToolStripDropDownMenu> und <xref:System.Windows.Forms.ToolStripOverflow> . Sie ähnelt dem <xref:System.Windows.Forms.FlowLayoutPanel> . Die Merkmale des <xref:System.Windows.Forms.ToolStripLayoutStyle.Flow> Layouts lauten wie folgt:

- Alle Funktionen von <xref:System.Windows.Forms.FlowLayoutPanel> werden von der-Eigenschaft verfügbar gemacht <xref:System.Windows.Forms.ToolStrip.LayoutSettings%2A> . Sie müssen die <xref:System.Windows.Forms.LayoutSettings> Klasse in eine <xref:System.Windows.Forms.FlowLayoutSettings> Klasse umwandeln.

- Sie können die <xref:System.Windows.Forms.ToolStripItem.Dock%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.ToolStripItem.Anchor%2A> im Code verwenden, um die Elemente in der Zeile auszurichten.

- Die <xref:System.Windows.Forms.ToolStripItem.Alignment%2A>-Eigenschaft wird ignoriert.

- Im- <xref:System.Windows.Forms.ToolStrip.LayoutCompleted> Ereignis können Sie die- <xref:System.Windows.Forms.ToolStripItem.Placement%2A> Eigenschaft überprüfen, um zu bestimmen, ob ein Element in den Haupt- <xref:System.Windows.Forms.ToolStrip> oder nicht passt.

- Der Ziehpunkt wird nicht gerendert, <xref:System.Windows.Forms.ToolStrip> daher <xref:System.Windows.Forms.ToolStripLayoutStyle.Flow> kann ein im Layoutstil in einem nicht <xref:System.Windows.Forms.ToolStripPanel> verschoben werden.

- Die <xref:System.Windows.Forms.ToolStrip> Überlauf Schaltfläche wird nicht gerendert und <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> wird ignoriert.

##### <a name="table-layout"></a>Tabellenlayout

<xref:System.Windows.Forms.ToolStripLayoutStyle.Table> Layout ist die Standardeinstellung für <xref:System.Windows.Forms.StatusStrip> . Dies ist vergleichbar mit <xref:System.Windows.Forms.TableLayoutPanel> . Die Merkmale des <xref:System.Windows.Forms.ToolStripLayoutStyle.Flow> Layouts lauten wie folgt:

- Alle Funktionen von <xref:System.Windows.Forms.TableLayoutPanel> werden von der-Eigenschaft verfügbar gemacht <xref:System.Windows.Forms.ToolStrip.LayoutSettings%2A> . Sie müssen die <xref:System.Windows.Forms.LayoutSettings> Klasse in eine <xref:System.Windows.Forms.TableLayoutSettings> Klasse umwandeln.

- Sie können die <xref:System.Windows.Forms.ToolStripItem.Dock%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.ToolStripItem.Anchor%2A> im Code verwenden, um die Elemente in der Tabellenzelle auszurichten.

- Die <xref:System.Windows.Forms.ToolStripItem.Alignment%2A>-Eigenschaft wird ignoriert.

- Im- <xref:System.Windows.Forms.ToolStrip.LayoutCompleted> Ereignis können Sie die- <xref:System.Windows.Forms.ToolStripItem.Placement%2A> Eigenschaft überprüfen, um zu bestimmen, ob ein Element in den Haupt- <xref:System.Windows.Forms.ToolStrip> oder nicht passt.

- Der Ziehpunkt wird nicht gerendert, <xref:System.Windows.Forms.ToolStrip> daher <xref:System.Windows.Forms.ToolStripLayoutStyle.Table> kann ein im Layoutstil in einem nicht <xref:System.Windows.Forms.ToolStripPanel> verschoben werden.

- Die <xref:System.Windows.Forms.ToolStrip> Überlauf Schaltfläche wird nicht gerendert und <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> wird ignoriert.

## <a name="toolstripitem"></a>ToolStripItem

In den folgenden Themen werden <xref:System.Windows.Forms.ToolStripItem> und die Steuerelemente beschrieben, die davon abgeleitet sind.

<xref:System.Windows.Forms.ToolStripItem> ist die abstrakte Basisklasse für alle Elemente, die in ein-Element gelangen <xref:System.Windows.Forms.ToolStrip> . Das folgende Objektmodell zeigt die <xref:System.Windows.Forms.ToolStripItem> Vererbungs Hierarchie.

![Diagramm, das das ToolStripItem-Objektmodell zeigt.](./media/toolstrip-control-architecture/toolstripitem-object-model.gif)

<xref:System.Windows.Forms.ToolStripItem> Klassen erben entweder direkt von <xref:System.Windows.Forms.ToolStripItem> , oder Sie erben indirekt von <xref:System.Windows.Forms.ToolStripItem> durch <xref:System.Windows.Forms.ToolStripControlHost> oder <xref:System.Windows.Forms.ToolStripDropDownItem> .

<xref:System.Windows.Forms.ToolStripItem> Steuerelemente müssen in <xref:System.Windows.Forms.ToolStrip> , <xref:System.Windows.Forms.MenuStrip> , oder enthalten sein <xref:System.Windows.Forms.StatusStrip> <xref:System.Windows.Forms.ContextMenuStrip> und können nicht direkt zu einem Formular hinzugefügt werden. Die verschiedenen Containerklassen sind so konzipiert, dass Sie eine geeignete Teilmenge der Steuer <xref:System.Windows.Forms.ToolStripItem> Elemente enthalten.

In der folgenden Tabelle sind die Aktien Steuer <xref:System.Windows.Forms.ToolStripItem> Elemente und die Container aufgeführt, in denen Sie am besten aussehen. Obwohl ein beliebiges <xref:System.Windows.Forms.ToolStrip> Element in einem beliebigen von <xref:System.Windows.Forms.ToolStrip> abgeleiteten Container gehostet werden kann, wurden diese Elemente so entworfen, dass Sie am besten in den folgenden Containern aussehen:

> [!NOTE]
> <xref:System.Windows.Forms.ToolStripDropDown> wird nicht in der Designer-Toolbox angezeigt.

|Enthaltenes Element|ToolStrip|MenuStrip|ContextMenuStrip|StatusStrip|Tool Strip Dropdown|
|--------------------|---------------|---------------|----------------------|-----------------|-----------------------|
|<xref:System.Windows.Forms.ToolStripButton>|Ja|Nein|Nein|Nein|Ja|
|<xref:System.Windows.Forms.ToolStripComboBox>|Ja|Ja|Ja|Nein|Ja|
|<xref:System.Windows.Forms.ToolStripSplitButton>|Ja|Nein|Nein|Ja|Ja|
|<xref:System.Windows.Forms.ToolStripLabel>|Ja|Nein|Nein|Ja|Ja|
|<xref:System.Windows.Forms.ToolStripSeparator>|Ja|Ja|Ja|Nein|Ja|
|<xref:System.Windows.Forms.ToolStripDropDownButton>|Ja|Nein|Nein|Ja|Ja|
|<xref:System.Windows.Forms.ToolStripTextBox>|Ja|Ja|Ja|Nein|Ja|
|<xref:System.Windows.Forms.ToolStripMenuItem>|Nein|Ja|Ja|Nein|Nein|
|<xref:System.Windows.Forms.ToolStripStatusLabel>|Nein|Nein|Nein|Ja|Nein|
|<xref:System.Windows.Forms.ToolStripProgressBar>|Ja|Nein|Nein|Ja|Nein|
|<xref:System.Windows.Forms.ToolStripControlHost>|Ja|Ja|Nein|Ja|Ja|

### <a name="toolstripbutton"></a>ToolStripButton

<xref:System.Windows.Forms.ToolStripButton> ist das Schaltflächen Element für <xref:System.Windows.Forms.ToolStrip> . Sie können Sie mit verschiedenen Rahmen Formaten anzeigen, und Sie können Sie verwenden, um Betriebszustände darzustellen und zu aktivieren. Sie können auch festlegen, dass der Fokus standardmäßig festgelegt wird.

### <a name="toolstriplabel"></a>ToolStripLabel

Bietet Bezeichnungs <xref:System.Windows.Forms.ToolStripLabel> Funktionen in-Steuer <xref:System.Windows.Forms.ToolStrip> Elementen. Das <xref:System.Windows.Forms.ToolStripLabel> -ist wie ein <xref:System.Windows.Forms.ToolStripButton> , das nicht standardmäßig den Fokus erhält und nicht als per pushübertragung oder hervorgehoben dargestellt wird.

<xref:System.Windows.Forms.ToolStripLabel> als gehostete Elemente unterstützt Zugriffsschlüssel.

Verwenden <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> Sie die <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> Eigenschaften, und in <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A> einem <xref:System.Windows.Forms.ToolStripLabel> , um das Link Steuerelement in einem zu unterstützen <xref:System.Windows.Forms.ToolStrip> .

### <a name="toolstripstatuslabel"></a>ToolStripStatusLabel

<xref:System.Windows.Forms.ToolStripStatusLabel> ist eine Version von, die <xref:System.Windows.Forms.ToolStripLabel> speziell für die Verwendung in entworfen wurde <xref:System.Windows.Forms.StatusStrip> . Zu den besonderen Features zählen <xref:System.Windows.Forms.ToolStripStatusLabel.BorderStyle%2A> , <xref:System.Windows.Forms.ToolStripStatusLabel.BorderSides%2A> und <xref:System.Windows.Forms.ToolStripStatusLabel.Spring%2A> .

### <a name="toolstripseparator"></a>ToolStripSeparator

Der <xref:System.Windows.Forms.ToolStripSeparator> fügt einer Symbolleiste oder einem Menü abhängig von der Ausrichtung eine vertikale oder horizontale Linie hinzu. Sie ermöglicht das Gruppieren von oder unterschieden zwischen Elementen, z. b. in einem Menü.

Sie können ein <xref:System.Windows.Forms.ToolStripSeparator> zur Entwurfszeit hinzufügen, indem Sie es in einer Dropdown Liste auswählen. Sie können jedoch auch automatisch erstellen, <xref:System.Windows.Forms.ToolStripSeparator> indem Sie einen Bindestrich (-) entweder im Designer-Vorlagen Knoten oder in der- <xref:System.Windows.Forms.ToolStripItemCollection.Add%2A> Methode eingeben.

### <a name="toolstripcontrolhost"></a>ToolStripControlHost

<xref:System.Windows.Forms.ToolStripControlHost> ist die abstrakte Basisklasse für <xref:System.Windows.Forms.ToolStripComboBox> , <xref:System.Windows.Forms.ToolStripTextBox> und <xref:System.Windows.Forms.ToolStripProgressBar> . <xref:System.Windows.Forms.ToolStripControlHost> kann andere Steuerelemente, einschließlich benutzerdefinierter Steuerelemente, auf zwei Arten hosten:

- Erstellen Sie eine <xref:System.Windows.Forms.ToolStripControlHost> mit einer Klasse, die von abgeleitet wird <xref:System.Windows.Forms.Control> . Um vollständigen Zugriff auf das gehostete Steuerelement und die Eigenschaften zu erhalten, müssen Sie die <xref:System.Windows.Forms.ToolStripControlHost.Control%2A> Eigenschaft wieder in die tatsächliche Klasse umwandeln, die Sie repräsentiert

- Erweitern Sie <xref:System.Windows.Forms.ToolStripControlHost> und im Parameter losen Konstruktor der geerbten Klasse den Basisklassenkonstruktor, und übergeben Sie eine Klasse, die von abgeleitet wird <xref:System.Windows.Forms.Control> . Mit dieser Option können Sie allgemeine Steuerelement Methoden und-Eigenschaften für den einfachen Zugriff in einem einschließen <xref:System.Windows.Forms.ToolStrip> .

### <a name="toolstripcombobox"></a>ToolStripComboBox

<xref:System.Windows.Forms.ToolStripComboBox> ist das <xref:System.Windows.Forms.ComboBox> für das Hosting in einem optimierte <xref:System.Windows.Forms.ToolStrip> . Eine Teilmenge der Eigenschaften und Ereignisse des gehosteten Steuer Elements wird auf der- <xref:System.Windows.Forms.ToolStripComboBox> Ebene verfügbar gemacht, aber auf das zugrunde liegende Steuerelement kann <xref:System.Windows.Forms.ComboBox> über die-Eigenschaft vollständig zugegriffen werden <xref:System.Windows.Forms.ToolStripComboBox.ComboBox%2A> .

### <a name="toolstriptextbox"></a>Tool Strip TextBox

<xref:System.Windows.Forms.ToolStripTextBox> ist das <xref:System.Windows.Forms.TextBox> für das Hosting in einem optimierte <xref:System.Windows.Forms.ToolStrip> . Eine Teilmenge der Eigenschaften und Ereignisse des gehosteten Steuer Elements wird auf der- <xref:System.Windows.Forms.ToolStripTextBox> Ebene verfügbar gemacht, aber auf das zugrunde liegende Steuerelement kann <xref:System.Windows.Forms.TextBox> über die-Eigenschaft vollständig zugegriffen werden <xref:System.Windows.Forms.ToolStripTextBox.TextBox%2A> .

### <a name="toolstripprogressbar"></a>ToolStripProgressBar

<xref:System.Windows.Forms.ToolStripProgressBar> ist das <xref:System.Windows.Forms.ProgressBar> für das Hosting in einem optimierte <xref:System.Windows.Forms.ToolStrip> . Eine Teilmenge der Eigenschaften und Ereignisse des gehosteten Steuer Elements wird auf der- <xref:System.Windows.Forms.ToolStripProgressBar> Ebene verfügbar gemacht, aber auf das zugrunde liegende Steuerelement kann <xref:System.Windows.Forms.ProgressBar> über die-Eigenschaft vollständig zugegriffen werden <xref:System.Windows.Forms.ToolStripProgressBar.ProgressBar%2A> .

### <a name="toolstripdropdownitem"></a>ToolStripDropDownItem

<xref:System.Windows.Forms.ToolStripDropDownItem> ist die abstrakte Basisklasse für <xref:System.Windows.Forms.ToolStripMenuItem> , <xref:System.Windows.Forms.ToolStripDropDownButton> und <xref:System.Windows.Forms.ToolStripSplitButton> , die Elemente direkt hosten oder zusätzliche Elemente in einem Dropdown Container hosten kann. Hierzu legen Sie die <xref:System.Windows.Forms.ToolStripDropDownItem.DropDown%2A> -Eigenschaft auf fest <xref:System.Windows.Forms.ToolStripDropDown> und legen die- <xref:System.Windows.Forms.ToolStrip.Items%2A> Eigenschaft von fest <xref:System.Windows.Forms.ToolStripDropDown> . Greifen Sie direkt über die-Eigenschaft auf diese Dropdown Elemente zu <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItems%2A> .

### <a name="toolstripmenuitem"></a>ToolStripMenuItem

<xref:System.Windows.Forms.ToolStripMenuItem> ist eine <xref:System.Windows.Forms.ToolStripDropDownItem> , die mit und verwendet wird, <xref:System.Windows.Forms.ToolStripDropDownMenu> <xref:System.Windows.Forms.ContextMenuStrip> um die besondere Hervorhebung, das Layout und die Spalten Anordnung für Menüs zu verarbeiten.

### <a name="toolstripdropdownbutton"></a>ToolStripDropDownButton

<xref:System.Windows.Forms.ToolStripDropDownButton> sieht wie aus <xref:System.Windows.Forms.ToolStripButton> , aber es wird ein Dropdown Bereich angezeigt, wenn der Benutzer darauf klickt. Blenden Sie den Dropdown Pfeil durch Festlegen der-Eigenschaft aus, oder zeigen Sie ihn an <xref:System.Windows.Forms.ToolStripDropDownButton.ShowDropDownArrow%2A> . <xref:System.Windows.Forms.ToolStripDropDownButton> hostet einen <xref:System.Windows.Forms.ToolStripOverflowButton> , der Elemente anzeigt, die überlaufen <xref:System.Windows.Forms.ToolStrip> .

### <a name="toolstripsplitbutton"></a>ToolStripSplitButton

<xref:System.Windows.Forms.ToolStripSplitButton> kombiniert Schaltfläche und Dropdown-Schaltflächen Funktionalität.

Verwenden Sie die- <xref:System.Windows.Forms.ToolStripSplitButton.DefaultItem%2A> Eigenschaft, um das- <xref:System.Windows.Forms.Control.Click> Ereignis des ausgewählten Dropdown Elements mit dem Element zu synchronisieren, das auf der Schaltfläche angezeigt wird.

### <a name="toolstripitem-generic-features"></a>Generische Features von ToolStripItem

<xref:System.Windows.Forms.ToolStripItem> bietet die folgenden allgemeinen Features und Optionen zum Erben von Steuerelementen:

- Core-Ereignisse

- Bildverarbeitung

- Ausrichtung

- Text-und Bild Beziehung

- Anzeige Stil

#### <a name="core-events"></a>Core-Ereignisse

<xref:System.Windows.Forms.ToolStripItem> Steuerelemente empfangen eigene Click-, Maus-und Zeichnungs Ereignisse und können auch eine bestimmte Tastatur Vorverarbeitung durchführen.

#### <a name="image-handling"></a>Bildverarbeitung

Die <xref:System.Windows.Forms.ToolStripItem.Image%2A> <xref:System.Windows.Forms.ToolStripItem.ImageAlign%2A> Eigenschaften,, <xref:System.Windows.Forms.ToolStripItem.ImageIndex%2A> , und beziehen <xref:System.Windows.Forms.ToolStripItem.ImageKey%2A> <xref:System.Windows.Forms.ToolStripItem.ImageScaling%2A> sich auf verschiedene Aspekte der Bildverarbeitung. Verwenden Sie Bilder in Steuer <xref:System.Windows.Forms.ToolStrip> Elementen, indem Sie diese Eigenschaften direkt oder durch Festlegen der Eigenschaft Lauf Zeit – only festlegen <xref:System.Windows.Forms.ToolStrip.ImageList%2A> .

Die Bildskalierung wird durch die Interaktion von Eigenschaften sowohl in als auch in festgelegt <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.ToolStripItem> , wie im folgenden dargestellt:

- <xref:System.Windows.Forms.ToolStrip.ImageScalingSize%2A> die Skala des endgültigen Bilds, wie durch die Kombination der Image- <xref:System.Windows.Forms.ToolStripItem.ImageScaling%2A> Einstellung und der Einstellung des Containers bestimmt <xref:System.Windows.Forms.ToolStrip.AutoSize%2A> .

  - Wenn <xref:System.Windows.Forms.ToolStrip.AutoSize%2A> `true` (der Standardwert) ist und <xref:System.Windows.Forms.ToolStripItemImageScaling> ist, wird <xref:System.Windows.Forms.ToolStripItemImageScaling.SizeToFit> keine Bildskalierung durchgeführt, und die <xref:System.Windows.Forms.ToolStrip> Größe entspricht dem größten Element oder einer vorgeschriebenen Mindestgröße.

  - Wenn <xref:System.Windows.Forms.ToolStrip.AutoSize%2A> ist `false` und den Wert <xref:System.Windows.Forms.ToolStripItemImageScaling> <xref:System.Windows.Forms.ToolStripItemImageScaling.None> hat, erfolgt weder ein Bild noch eine <xref:System.Windows.Forms.ToolStrip> Skalierung.

#### <a name="alignment"></a>Ausrichtung

Der Wert der- <xref:System.Windows.Forms.ToolStripItem.Alignment%2A> Eigenschaft bestimmt das Ende der <xref:System.Windows.Forms.ToolStrip> , an der ein Element angezeigt wird. Die-Eigenschaft kann nur verwendet werden <xref:System.Windows.Forms.ToolStripItem.Alignment%2A> , wenn die layoutart des <xref:System.Windows.Forms.ToolStrip> auf einen der Stapelüberlauf Werte festgelegt ist.

Elemente werden in der <xref:System.Windows.Forms.ToolStrip> Reihenfolge platziert, in der die Elemente in der Items-Auflistung angezeigt werden. Um die Position eines Elements Programm gesteuert zu ändern, verwenden Sie die- <xref:System.Windows.Forms.ToolStripItemCollection.Insert%2A> Methode, um das Element in der Auflistung zu verschieben. Mit dieser Methode wird das Element verschoben, aber nicht dupliziert.

#### <a name="text-and-image-relationship"></a>Text-und Bild Beziehung

Die- <xref:System.Windows.Forms.ToolStripItem.TextImageRelation%2A> Eigenschaft definiert die relative Platzierung des Bilds in Bezug auf den Text auf einem <xref:System.Windows.Forms.ToolStripItem> . Elemente, die nicht über ein Bild, Text oder beides verfügen, werden als Sonderfälle behandelt, sodass <xref:System.Windows.Forms.ToolStripItem> für das fehlende Element oder die fehlenden Elemente keine leere Stelle anzeigt.

#### <a name="display-style"></a>Anzeige Stil

<xref:System.Windows.Forms.ToolStripItem.DisplayStyle%2A> ermöglicht das Festlegen der Werte für die Text-und Bildeigenschaften eines Elements, während nur die gewünschten Elemente angezeigt werden. Dies wird normalerweise verwendet, um nur den Anzeige Stil zu ändern, wenn das gleiche Element in einem anderen Kontext angezeigt wird.

## <a name="accessory-classes"></a>Zubehör Klassen

Zu den Klassen, die verschiedene andere Funktionen bieten, gehören:

- <xref:System.Windows.Forms.ToolStripManager> unterstützt <xref:System.Windows.Forms.ToolStrip> -bezogene Aufgaben für ganze Anwendungen, wie z. b. Zusammenführung, Einstellungen und rendereroptionen.

- <xref:System.Windows.Forms.ToolStripRenderer> ermöglicht es Ihnen, ein bestimmtes Format oder Design auf einfache Weise zu verwenden <xref:System.Windows.Forms.ToolStrip> .

- <xref:System.Windows.Forms.ToolStripProfessionalRenderer> erstellt Stifte und Pinsel auf der Grundlage einer ersetzbaren Farbtabelle ( <xref:System.Windows.Forms.ProfessionalColorTable> ).

- <xref:System.Windows.Forms.ToolStripSystemRenderer> wendet Systemfarben und einen flachen visuellen Stil auf <xref:System.Windows.Forms.ToolStrip> Anwendungen an.

- <xref:System.Windows.Forms.ToolStripContainer> ähnelt <xref:System.Windows.Forms.SplitContainer> . Er verwendet vier angedockte Seitenbereiche (Instanzen von <xref:System.Windows.Forms.ToolStripPanel> ) und einen zentralen Bereich (eine Instanz von <xref:System.Windows.Forms.ToolStripContentPanel> ), um eine typische Anordnung zu erstellen. Sie können die Seitenbereiche nicht entfernen, aber Sie können Sie ausblenden. Sie können den zentralen Bereich weder entfernen noch ausblenden. Sie können ein oder mehrere Steuer <xref:System.Windows.Forms.ToolStrip> <xref:System.Windows.Forms.MenuStrip> Elemente, oder <xref:System.Windows.Forms.StatusStrip> in den Seiten Bereichen anordnen, und Sie können den zentralen Bereich für andere Steuerelemente verwenden. <xref:System.Windows.Forms.ToolStripContentPanel>Bietet auch eine Möglichkeit, rendererunterstützung für eine konsistente Darstellung in den Hauptteil Ihres Formulars zu bringen. <xref:System.Windows.Forms.ToolStripContainer> bietet keine Unterstützung für Multiple Document Interface (MDI).

- <xref:System.Windows.Forms.ToolStripPanel> bietet Platz zum Verschieben und Anordnen von Steuer <xref:System.Windows.Forms.ToolStrip> Elementen. Sie können nur einen Panel verwenden, wenn Sie dies auswählen, und <xref:System.Windows.Forms.ToolStripPanel> in MDI-Szenarien gut funktionieren.

## <a name="see-also"></a>Siehe auch

- [Übersicht über das ToolStrip-Steuerelement](toolstrip-control-overview-windows-forms.md)
- [Zusammenfassung der ToolStrip-Technologie](toolstrip-technology-summary.md)
- [ToolStrip-Steuerelement](toolstrip-control-windows-forms.md)
- [MenuStrip-Steuerelement](menustrip-control-windows-forms.md)
- [StatusStrip-Steuerelement](statusstrip-control.md)
- [ContextMenuStrip-Steuerelement](contextmenustrip-control.md)
- [BindingNavigator-Steuerelement](bindingnavigator-control-windows-forms.md)
