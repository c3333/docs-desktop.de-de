---
title: Festlegen von Layoutoptionen
description: Hier erfahren Sie mehr über die verschiedenen Einstellungen für ein Steuerelement, die sich auf Layout und Positionierung in Windows Forms für .NET auswirken. Hier lernen Sie die verschiedenen Steuerelementcontainer kennen, die sich auf das Layout auswirken.
ms.date: 10/26/2020
ms.topic: overview
helpviewer_keywords:
- forms [Windows Forms], aligning controls
- Windows Forms, aligning controls
- controls [Windows Forms], positioning
- controls [Windows Forms], aligning
- TabControl control [Windows Forms], about TabControl control
- SplitContainer control [Windows Forms], about SplitContainer control
- Panel control [Windows Forms], about Panel control
- GroupBox control [Windows Forms], about GroupBox control
- FlowLayoutPanel control [Windows Forms], about FlowLayoutPanel control
- TableLayoutPanel control [Windows Forms], about TableLayoutPanel control
- sizing [Windows Forms], automatic
- layout [Windows Forms], AutoSize
- automatic sizing
- AutoSizeMode property
ms.openlocfilehash: 542decdf2555dcc01ff544a370f59ac73269ab6c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942053"
---
# <a name="position-and-layout-of-controls-windows-forms-net"></a>Position und Layout von Steuerelementen (Windows Forms .NET)

Die Platzierung von Steuerelementen in Windows Forms wird nicht nur durch das Steuerelement bestimmt, sondern auch durch das übergeordnete Element des Steuerelements. In diesem Artikel werden die durch Steuerelemente bereitgestellten Einstellungen und die übergeordneten Container beschrieben, die sich auf das Layout auswirken.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="fixed-position-and-size"></a>Feste Position und Größe

Die Position, an der ein Steuerelement auf einem übergeordneten Element angezeigt wird, wird durch den Wert der <xref:System.Windows.Forms.Control.Location>-Eigenschaft relativ zum oberen linken Rand der übergeordneten Oberfläche bestimmt. `(x0,y0)` ist die obere linke Positionskoordinate im übergeordneten Element. Die Größe des Steuerelements wird durch die <xref:System.Windows.Forms.Control.Size>-Eigenschaft bestimmt. Sie gibt die Breite und Höhe des Steuerelements an.

:::image type="content" source="media/layout/location+container.png" alt-text="Position des Steuerelements relativ zum Container":::

Wenn einem übergeordneten Element ein Steuerelement hinzugefügt wird, das die automatische Platzierung erzwingt, ändern sich Position und Größe des Steuerelements. In diesem Fall können Position und Größe des Steuerelements je nach übergeordnetem Element möglicherweise nicht manuell angepasst werden.

Mit den Eigenschaften <xref:System.Windows.Forms.Control.MaximumSize%2A> und <xref:System.Windows.Forms.Control.MinimumSize%2A> können der mindestens erforderliche und der maximal zulässige Bereich für das Steuerelement festgelegt werden.

## <a name="automatic-placement-and-size"></a>Automatische Platzierung und Größenanpassung

Steuerelemente können automatisch im übergeordneten Element platziert werden. Von einigen übergeordneten Containern wird die Platzierung erzwungen, während von anderen die Platzierungseinstellungen des Steuerelements übernommen wird. Es gibt zwei Eigenschaften für ein Steuerelement, mit denen die automatische Platzierung und Größenanpassung innerhalb eines übergeordneten Elements unterstützt wird: <xref:System.Windows.Forms.Control.Dock%2A> und <xref:System.Windows.Forms.Control.Anchor>.

Die automatische Platzierung kann durch die Zeichnungsreihenfolge beeinflusst werden. Dabei geht es um die Reihenfolge, in der ein Steuerelement gezeichnet und die durch den Index des Steuerelements in der <xref:System.Windows.Forms.Control.Controls>-Sammlung des übergeordneten Elements bestimmt wird. Dieser Index wird als **:::no-loc text="Z-order":::** bezeichnet. Die einzelnen Steuerelemente werden in der umgekehrten Reihenfolge gezeichnet, in der sie in der Sammlung angezeigt werden. Das bedeutet, dass es sich bei der Sammlung um eine First-In-Last-Drawn- und eine Last-In-First-Drawn-Sammlung handelt.

Mit den Eigenschaften <xref:System.Windows.Forms.Control.MinimumSize%2A> und <xref:System.Windows.Forms.Control.MaximumSize%2A> können der mindestens erforderliche und der maximal zulässige Bereich für das Steuerelement festgelegt werden.

### <a name="dock"></a>Dock

Mit der `Dock`-Eigenschaft wird festgelegt, welcher Rahmen des Steuerelements an der entsprechenden Seite des übergeordneten Elements ausgerichtet und wie die Größe des Steuerelements innerhalb des übergeordneten Elements geändert wird.

:::image type="content" source="media/layout/dock-modes.png" alt-text="Windows-Formular mit Schaltflächen mit Andockeinstellungen":::

Bei einem angedockten Element wird der Bereich, der durch das Steuerelement belegt wird, durch den Container bestimmt. Zudem wird durch den Container die Größe des Steuerelements geändert und das Steuerelement platziert. Breite und Höhe des Steuerelements werden weiterhin basierend auf dem Andockstil übernommen. Wenn das Steuerelement beispielsweise am oberen Rand angedockt wird, wird die <xref:System.Windows.Forms.Control.Height> des Steuerelements übernommen, die <xref:System.Windows.Forms.Control.Width> wird jedoch automatisch angepasst. Wenn das Steuerelement am linken Rand angedockt wird, wird die <xref:System.Windows.Forms.Control.Width> des Steuerelements übernommen, die <xref:System.Windows.Forms.Control.Height> wird jedoch automatisch angepasst.

Die <xref:System.Windows.Forms.Control.Location> des Steuerelements kann nicht manuell festgelegt werden, da die Position eines Steuerelements durch das Andocken automatisch festgelegt wird.

Die **:::no-loc text="Z-order":::** des Steuerelements wirkt sich auf das Andocken aus. Da angedockte Steuerelemente angeordnet sind, belegen sie den für sie verfügbaren Bereich. Wenn beispielsweise ein Steuerelement gezeichnet und am oberen Rand angedockt wird, nimmt es die gesamte Breite des Containers ein. Wenn dann ein weiteres Steuerelement am linken Rand angedockt wird, ist der vertikal verfügbare Bereich kleiner.

:::image type="content" source="media/layout/dock-top-then-left.png" alt-text="Windows-Formular mit links und oben angedockten Schaltflächen, wobei die obere größer ist":::

Wenn die **:::no-loc text="Z-order":::** der Steuerelemente umgekehrt wird, steht dem am linken Rand angedockten Steuerelement zunächst ein größerer Bereich zur Verfügung. Vom Steuerelement wird die gesamte Höhe des Containers belegt. Dem Steuerelement, das am oberen Rand angedockt wird, bleibt ein kleinerer horizontaler Bereich.

:::image type="content" source="media/layout/dock-left-then-top.png" alt-text="Windows-Formular mit links und oben angedockten Schaltflächen, wobei die linke größer ist":::

Wenn sich die Größe des Containers ändert, werden Position und Größe der an den Container angedockten Steuerelemente geändert, sodass die jeweiligen Positionen und Größen erhalten bleiben.

:::image type="content" source="media/layout/dock-resize.gif" alt-text="Animation zur Darstellung, wie sich die Größe eines Windows-Formulars mit an allen Positionen angedockten Schaltflächen ändert":::

Wenn mehrere Steuerelemente an derselben Seite des Containers angedockt werden, werden sie entsprechend der **:::no-loc text="Z-order":::** gestapelt.

:::image type="content" source="media/layout/dock-left-left.png" alt-text="Windows-Formular mit zwei am linken Rand angedockten Schaltflächen":::

### <a name="anchor"></a>Anchor

Durch das Verankern eines Steuerelements können Sie das Steuerelement an eine oder mehrere Seiten des übergeordneten Container binden. Wenn sich die Größe des Containers ändert, bleibt für alle untergeordneten Steuerelemente der Abstand zur verankerten Seite erhalten.

Ein Steuerelement kann ohne Einschränkung an einer oder mehreren Seiten verankert werden. Der Anker wird mit der <xref:System.Windows.Forms.Control.Anchor>-Eigenschaft festgelegt.

:::image type="content" source="media/layout/anchor-resize.gif" alt-text="Animation zur Darstellung, wie sich die Größe eines Windows-Formulars mit an allen Positionen verankerten Schaltflächen ändert":::

### <a name="automatic-sizing"></a>Automatische Größenanpassung

Mit der <xref:System.Windows.Forms.Control.AutoSize>-Eigenschaft lässt sich die Größe eines Steuerelements bei Bedarf ändern, sodass es der durch die <xref:System.Windows.Forms.Control.PreferredSize>-Eigenschaft angegebenen Größe entspricht. Das Verhalten bei der Größenanpassung können Sie durch Festlegen der `AutoSizeMode`-Eigenschaft für bestimmte Steuerelemente anpassen.

Die <xref:System.Windows.Forms.Control.AutoSize%2A>-Eigenschaft wird nicht von allen Steuerelementen unterstützt. Einige Steuerelemente, mit denen die <xref:System.Windows.Forms.Control.AutoSize%2A>-Eigenschaft unterstützt wird, wird auch die `AutoSizeMode`-Eigenschaft unterstützt.

| Verhalten: immer TRUE | BESCHREIBUNG |
|--|--|
| Bei der automatischen Größenanpassung handelt es sich um ein Laufzeitfeature. | Das bedeutet, dass eine Größenänderung für ein Steuerelement immer weitere Auswirkungen hat. |
| Wenn sich die Größe eines Steuerelements ändert, bleibt der Wert der <xref:System.Windows.Forms.Control.Location%2A>-Eigenschaft immer konstant. | Wenn ein Steuerelement aufgrund des Inhalts größer wird, nimmt die Größe des Steuerelements nach rechts und nach unten zu. Nach links werden Steuerelemente nicht vergrößert. |
| Die Eigenschaften <xref:System.Windows.Forms.Control.Dock%2A> und <xref:System.Windows.Forms.Control.Anchor%2A> werden berücksichtigt, wenn <xref:System.Windows.Forms.Control.AutoSize%2A> `true` ist. | Der Wert der <xref:System.Windows.Forms.Control.Location%2A>-Eigenschaft des Steuerelements wird an den entsprechenden Wert angepasst.<br /><br /> Das Steuerelement <xref:System.Windows.Forms.Label> ist die Ausnahme von dieser Regel. Wenn Sie den Wert der <xref:System.Windows.Forms.Control.AutoSize%2A>-Eigenschaft eines angedockten <xref:System.Windows.Forms.Label>-Steuerelements auf `true` festlegen, wird das <xref:System.Windows.Forms.Label>-Steuerelement nicht gestreckt. |
| Die Eigenschaften <xref:System.Windows.Forms.Control.MaximumSize%2A> und <xref:System.Windows.Forms.Control.MinimumSize%2A> eines Steuerelements werden immer berücksichtigt. Der Wert der <xref:System.Windows.Forms.Control.AutoSize%2A>-Eigenschaft spielt dabei keine Rolle. | Die Eigenschaften <xref:System.Windows.Forms.Control.MaximumSize%2A> und <xref:System.Windows.Forms.Control.MinimumSize%2A> werden durch die <xref:System.Windows.Forms.Control.AutoSize%2A>-Eigenschaft nicht beeinflusst. |
| Standardmäßig ist keine Mindestgröße festgelegt. | Das bedeutet, dass der Wert der <xref:System.Windows.Forms.Control.Size%2A>-Eigenschaft eines Steuerelements `(0x,0y)` lautet, wenn für das Steuerelement unter <xref:System.Windows.Forms.Control.AutoSize%2A> eine Verkleinerung festgelegt ist und das Steuerelement keine Inhalte aufweist. In diesem Fall wird das Steuerelement auf die Größe eines Punkts verkleinert und ist nicht mehr ohne Weiteres sichtbar. |
| Wenn die <xref:System.Windows.Forms.Control.GetPreferredSize%2A>-Methode für ein Steuerelement nicht implementiert wird, wird mit der <xref:System.Windows.Forms.Control.GetPreferredSize%2A>-Methode der Wert zurückgegeben, der der <xref:System.Windows.Forms.Control.Size%2A>-Eigenschaft zuletzt zugewiesen wurde. | Das bedeutet, dass es keine Auswirkungen hat, wenn <xref:System.Windows.Forms.Control.AutoSize%2A> auf `true` festgelegt wird. |
| Ein Steuerelement in einer <xref:System.Windows.Forms.TableLayoutPanel>-Zelle wird immer verkleinert, sodass es in die Zelle passt, bis die <xref:System.Windows.Forms.Control.MinimumSize%2A> erreicht ist. | Diese Größe wird als maximale Größe erzwungen. Dies ist nicht der Fall, wenn die Zelle Teil einer <xref:System.Windows.Forms.SizeType.AutoSize>-Zeile oder -Spalte ist. |

## <a name="container-form"></a>Container: Formular

Das <xref:System.Windows.Forms.Form> ist das Hauptobjekt von Windows Forms. In einer Windows Forms-Anwendung wird normalerweise immer ein Formular angezeigt. In einem Formular sind Steuerelemente enthalten und bei der manuellen Platzierung werden die Eigenschaften <xref:System.Windows.Forms.Control.Location> und <xref:System.Windows.Forms.Control.Size> des Steuerelements berücksichtigt. Zudem wird in einem Formular bei der automatischen Platzierung die [Dock](#dock)-Eigenschaft berücksichtigt.

Bei den meisten Formularen befinden sich an den Kanten Ziehpunkte, mit denen der Benutzer die Größe eines Formulars ändern kann. Mit der <xref:System.Windows.Forms.Control.Anchor>-Eigenschaft eines Steuerelements wird beim Ändern der Formulargröße die Größe des Steuerelements geändert.

## <a name="container-panel"></a>Container: Bereich

Das <xref:System.Windows.Forms.Panel>-Steuerelement gleicht insofern einem Formular, als dass sich damit Steuerelemente einfach gruppieren lassen. Dabei werden dieselben manuellen und automatischen Platzierungsstile wie bei einem Formular unterstützt. Weitere Informationen finden Sie im Abschnitt [Container: Formular](#container-form).

Ein Bereich wird nahtlos mit dem übergeordneten Element eingeblendet. Dabei werden alle Bereiche eines Steuerelements außerhalb der Grenzen des Bereichs abgeschnitten. Wenn ein Steuerelement außerhalb der Bereichsgrenzen liegt und <xref:System.Windows.Forms.Form.AutoScroll> auf `true` festgelegt ist, werden Scrollleisten angezeigt und der Benutzer kann den Bereich scrollen.

Im Gegensatz zum [Gruppenfeld](#container-group-box)-Steuerelement enthält ein Bereich keinen Beschriftungstext und keinen Rahmen.

:::image type="content" source="media/layout/panel-groupbox.png" alt-text="Ein Windows-Formular mit einem Bereich und einem Gruppenfeld":::

Auf der obigen Abbildung ist ein Bereich dargestellt, für den die <xref:System.Windows.Forms.Panel.BorderStyle%2A>-Eigenschaft zur Darstellung der Bereichsgrenzen festgelegt wurde.

## <a name="container-group-box"></a>Container: Gruppenfeld

Das <xref:System.Windows.Forms.GroupBox>-Steuerelement stellt eine erkennbare Gruppierung für andere Steuerelemente zur Verfügung. In der Regel wird ein Gruppenfeld verwendet, um ein Formular nach Funktionen zu unterteilen. So können beispielsweise in einem Formular mit persönlichen Daten die Felder für die Adresse in einer Gruppe zusammengefasst werden. Das Gruppenfeld mit den enthaltenen Steuerelementen lässt sich zur Entwurfszeit leichter verschieben.

Bei einem Gruppenfeld werden dieselben manuellen und automatischen Platzierungsstile wie bei einem Formular unterstützt. Weitere Informationen finden Sie im Abschnitt [Container: Formular](#container-form). Bei einem Gruppenfeld werden ebenfalls Bereiche eines Steuerelements abgeschnitten, die sich außerhalb der Bereichsgrenzen befinden.

Im Gegensatz zum [panel](#container-panel)-Steuerelement gibt es bei einem Gruppenfeld keine Möglichkeit, den Inhalt zu scrollen und Scrollleisten anzuzeigen.

:::image type="content" source="media/layout/panel-groupbox.png" alt-text="Ein Windows-Formular mit einem Bereich und einem Gruppenfeld":::

## <a name="container-flow-layout"></a>Container: Flusslayout

Das <xref:System.Windows.Forms.FlowLayoutPanel>-Steuerelement ordnet seinen Inhalt in horizontaler oder vertikaler Flussrichtung an. Dieser Inhalt kann von einer Zeile zur nächsten oder von einer Spalte zur nächsten umgebrochen werden. Wahlweise können Sie den Inhalt auch abschneiden statt ihn umzubrechen.  
  
Sie können die Flussrichtung angeben, indem Sie den Wert der <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A>-Eigenschaft festlegen. Das <xref:System.Windows.Forms.FlowLayoutPanel>-Steuerelement kehrt seine Flussrichtung in Layouts mit Leserichtung von rechts nach links (RTL) entsprechend um. Darüber hinaus können Sie angeben, ob der Inhalt des <xref:System.Windows.Forms.FlowLayoutPanel>-Steuerelements umgebrochen oder abgeschnitten wird, indem Sie den Wert der <xref:System.Windows.Forms.FlowLayoutPanel.WrapContents%2A>-Eigenschaft festlegen.  

Das <xref:System.Windows.Forms.FlowLayoutPanel>-Steuerelement wird automatisch an seinen Inhalt angepasst, wenn Sie die <xref:System.Windows.Forms.Control.AutoSize%2A>-Eigenschaft auf `true` festlegen. Zudem stellt es für seine untergeordneten Steuerelemente eine `FlowBreak`-Eigenschaft bereit. Wenn Sie den Wert der `FlowBreak`-Eigenschaft auf `true` festlegen, ordnet das <xref:System.Windows.Forms.FlowLayoutPanel>-Steuerelement andere Steuerelemente nicht mehr in der aktuellen Flussrichtung an und bricht diese auch nicht mehr in die nächste Zeile oder Spalte um.  

:::image type="content" source="media/layout/flow.png" alt-text="Ein Windows-Formular mit zwei Bereichssteuerelementen":::

Auf der obigen Abbildung sind zwei `FlowLayoutPanel`-Steuerelemente dargestellt, für die die <xref:System.Windows.Forms.Panel.BorderStyle>-Eigenschaft zur Darstellung der Grenzen des Steuerelements festgelegt wurde.

## <a name="container-table-layout"></a>Container: Tabellenlayout

Das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement ordnet seinen Inhalt in einem Raster an. Da das Layout sowohl zur Entwurfszeit als auch zur Laufzeit ausgeführt wird, kann es sich dynamisch ändern, wenn sich die Anwendungsumgebung ändert. Dadurch können sich die Steuerelemente im Bereich proportional in der Größe anpassen, sodass sie auf Änderungen wie die Größenanpassung des übergeordneten Steuerelements oder eine durch Lokalisierung veränderte Textlänge reagieren.

Jedes Windows Forms-Steuerelement kann ein untergeordnetes Element des <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelements sein, einschließlich anderer Instanzen von <xref:System.Windows.Forms.TableLayoutPanel>. Dadurch können Sie anspruchsvolle Layouts erstellen, die sich zur Laufzeit an Änderungen anpassen.

Außerdem können Sie festlegen, in welche Richtung (horizontal oder vertikal) das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement erweitert wird, wenn es bereits mit untergeordneten Steuerelementen gefüllt ist. Standardmäßig wird das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement nach unten erweitert, indem Zeilen hinzufügt werden.

Größe und Stil der Zeilen und Spalten können mithilfe der Eigenschaften <xref:System.Windows.Forms.TableLayoutPanel.RowStyles%2A> und <xref:System.Windows.Forms.TableLayoutPanel.ColumnStyles%2A> festgelegt werden. Sie können die Eigenschaften von Zeilen oder Spalten individuell festlegen.

Das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement fügt seinen untergeordneten Steuerelementen folgende Eigenschaften hinzu: `Cell`, `Column`, `Row`, `ColumnSpan` und `RowSpan`.

:::image type="content" source="media/layout/table.png" alt-text="Ein Windows-Formular mit einem Steuerelement für Tabellenlayout":::

Auf der obigen Abbildung ist eine Tabelle dargestellt, für die die <xref:System.Windows.Forms.TableLayoutPanel.CellBorderStyle>-Eigenschaft zur Darstellung der Grenzen der einzelnen Zellen festgelegt wurde.

## <a name="container-split-container"></a>Container: Geteilter Container

Das <xref:System.Windows.Forms.SplitContainer>-Steuerelement in Windows Forms kann als zusammengesetztes Steuerelement betrachtet werden. Es setzt sich aus zwei Bereichen zusammen, die durch eine verschiebbare Leiste getrennt sind. Wenn sich der Mauszeiger über der Leiste befindet, ändert sich seine Form und zeigt an, dass die Leiste verschiebbar ist.  

Mit dem <xref:System.Windows.Forms.SplitContainer>-Steuerelement können Sie komplexe Benutzeroberflächen erstellen. Häufig bestimmt die Auswahl in einem Fensterbereich, welche Objekte im anderen Fensterbereich angezeigt werden. Diese Anordnung eignet sich gut für die Anzeige und das Durchsuchen von Informationen. Die beiden Fensterbereiche ermöglichen Ihnen, Informationen in getrennten Bereichen anzuordnen, und mithilfe der Leiste, die auch als „Splitter“ bezeichnet wird, können Benutzer die Größe der Fensterbereiche leicht anpassen.

:::image type="content" source="media/layout/splitcontainer.png" alt-text="Ein Windows-Formular mit einem geschachtelten geteilten Container":::

Auf der obigen Abbildung ist ein geteilter Container zum Erstellen eines linken und rechten Fensterbereichs dargestellt. Der rechte Fensterbereich enthält einen zweiten geteilten Container, wobei für <xref:System.Windows.Forms.SplitContainer.Orientation> <xref:System.Windows.Forms.Orientation.Vertical> festgelegt ist. Die <xref:System.Windows.Forms.SplitContainer.BorderStyle>-Eigenschaft wurde zur Darstellung der Grenzen der einzelnen Fensterbereich festgelegt.

## <a name="container-tab-control"></a>Container: Registersteuerelement

Mit <xref:System.Windows.Forms.TabControl> werden mehrere Registerkarten wie Karteireiter in einem Notizbuch oder Reiter in Ordnern in einem Aktenschrank angezeigt. Die Registerkarten können Bilder und weitere Steuerelemente enthalten. Verwenden Sie das Registersteuerelement, um eine Art von Dialogfeld mit mehreren Seiten zu erstellen, die im Betriebssystem Windows an verschiedenen Stellen angezeigt wird, z. B. in der Systemsteuerung und in den Anzeigeeigenschaften. Zudem können Sie mit <xref:System.Windows.Forms.TabControl> Eigenschaftenseiten erstellen, mit denen eine Gruppe verwandter Eigenschaften festgelegt werden kann.

Die wichtigste Eigenschaft von <xref:System.Windows.Forms.TabControl> ist die Eigenschaft <xref:System.Windows.Forms.TabControl.TabPages%2A>. Sie enthält die einzelnen Registerkarten. Jede einzelne Registerkarte ist ein <xref:System.Windows.Forms.TabPage>-Objekt.

:::image type="content" source="media/layout/tabcontrol.png" alt-text="Ein Windows-Formular mit einem Registersteuerelement mit zwei Registerkartenseiten":::
