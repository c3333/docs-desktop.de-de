---
title: Anordnen von Steuerelementen mithilfe von Richtungslinien
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], arranging with snaplines
- snaplines [Windows Forms], arranging Windows Forms controls
- SnapLine class [Windows Forms], walkthroughs
- Windows Forms controls, arranging
ms.assetid: d5c9edc7-cf30-4a97-8ebe-201d569340f8
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 0b68a70b55cbf03d480fd388a637a4caf78b6eaa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976949"
---
# <a name="walkthrough-arrange-controls-on-windows-forms-using-snaplines"></a>Exemplarische Vorgehensweise: Anordnen von Steuerelementen auf Windows Forms mithilfe von Richtungslinien

Die präzise Platzierung von Steuerelementen auf dem Formular hat für viele Anwendungen einen hohen Stellenwert. Die Windows Forms-Designer bietet Ihnen viele Layouttools, um dies zu erreichen. Eine der wichtigsten Funktionen ist die- <xref:System.Windows.Forms.Design.Behavior.SnapLine> Funktion.

Mithilfe von Richtungslinien zeigen Sie genau an, wo Sie Steuerelemente mit anderen Steuerelementen ausrichten. Außerdem zeigen Sie die empfohlenen Entfernungen für Ränder zwischen Steuerelementen gemäß den [Richtlinien der Windows-Benutzeroberfläche](/windows/win32/uxguide/guidelines)an.

Ausrichtungs Linien erleichtern Ihnen das Ausrichten ihrer Steuerelemente, um die Darstellung und das Verhalten zu optimieren.

## <a name="create-the-project"></a>Erstellen des Projekts

1. Erstellen Sie in Visual Studio ein Windows-basiertes Anwendungsprojekt mit dem Namen "SnaplineExample".

2. Wählen Sie das Formular im Forms-Designer aus.

## <a name="space-and-align-controls"></a>Leerzeichen und Ausrichten von Steuerelementen

Ausrichtungs Linien verfügen über eine präzise und intuitive Möglichkeit zum Ausrichten von Steuerelementen auf dem Formular. Sie werden angezeigt, wenn Sie ein ausgewähltes Steuerelement oder Steuerelemente in der Nähe einer Position verschieben, die an einem anderen Steuerelement oder einer Gruppe von Steuerelementen ausgerichtet Ihre Auswahl wird an der vorgeschlagenen Position "andocken", während Sie Sie nach den anderen Steuerelementen verschieben.

### <a name="to-arrange-controls-using-snaplines"></a>So ordnen Sie Steuerelemente mithilfe von Richtungslinien an

1. Ziehen Sie ein <xref:System.Windows.Forms.Button> -Steuerelement aus der **Toolbox** auf das Formular.

2. Verschieben <xref:System.Windows.Forms.Button> Sie das Steuerelement in die untere rechte Ecke des Formulars. Beachten Sie, dass die Richtungslinien, die als Steuerelement angezeigt werden, <xref:System.Windows.Forms.Button> den unteren und rechten Rand des Formulars nähern. Diese Richtungslinien zeigen den empfohlenen Abstand zwischen den Rändern des Steuer Elements und dem Formular an.

3. Verschieben <xref:System.Windows.Forms.Button> Sie das Steuerelement um die Rahmen des Formulars, und notieren Sie sich, wo die Richtungslinien angezeigt werden. Wenn Sie fertig sind, verschieben Sie das <xref:System.Windows.Forms.Button> Steuerelement in der Mitte des Formulars.

4. Ziehen Sie ein anderes <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** auf das Formular.

5. Verschieben Sie das zweite-Steuerelement, <xref:System.Windows.Forms.Button> bis es sich fast in der ersten befindet. Beachten Sie die Richtungslinie, die in der TextBaseline beider Schaltflächen angezeigt wird, und beachten Sie, dass das Steuerelement, das Sie verschieben, an eine Position mit dem anderen Steuerelement mit dem anderen Steuerelement bewegt wird.

6. Verschieben Sie das zweite-Steuerelement, <xref:System.Windows.Forms.Button> bis es direkt oberhalb des ersten positioniert ist. Beachten Sie die Ausrichtungs Linien, die am linken und rechten Rand beider Schaltflächen angezeigt werden, und beachten Sie, dass das Steuerelement, das Sie verschieben, an eine Position ausgerichtet wird, die exakt am anderen Steuerelement ausgerichtet ist.

7. Wählen Sie eines der Steuer <xref:System.Windows.Forms.Button> Elemente aus, und verschieben Sie es in die Nähe der anderen, bis Sie fast berührt werden. Beachten Sie die angezeigte schräschlange. Diese Distanz ist die empfohlene Entfernung zwischen den Rahmen der Steuerelemente. Beachten Sie auch, dass das Steuerelement, das Sie verschieben, an diese Position anspringt.

8. Ziehen Sie zwei-Steuer <xref:System.Windows.Forms.Panel> Elemente aus der **Toolbox** auf das Formular.

9. Verschieben Sie eines der-Steuer <xref:System.Windows.Forms.Panel> Elemente, bis es fast mit dem ersten-Element- Beachten Sie die Richtungslinien, die am oberen und unteren Rand beider Steuerelemente angezeigt werden, und beachten Sie, dass das Steuerelement, das Sie verschieben, an eine Position mit dem anderen Steuerelement mit dem anderen Steuerelement bewegt wird.

## <a name="align-to-form-and-container-margins"></a>An Form-und Container Ränder ausrichten

Ausrichtungs Linien unterstützen Sie bei der konsistenten Ausrichtung der Steuerelemente an Form-und Container Ränder.

1. Wählen Sie eines der Steuer <xref:System.Windows.Forms.Button> Elemente aus, und verschieben Sie es nahe an den rechten Rand des Formulars, bis eine Ausrichtungslinie angezeigt wird. Der Abstand der Richtungslinie vom rechten Rand aus ist die Summe aus der-Eigenschaft des Steuer Elements <xref:System.Windows.Forms.Control.Margin%2A> und den <xref:System.Windows.Forms.Control.Padding%2A> Eigenschafts Werten des Formulars.

   > [!NOTE]
   > Wenn die-Eigenschaft des Formulars <xref:System.Windows.Forms.Control.Padding%2A> auf 0, 0, 0, 0 (null) festgelegt ist, gibt die Windows Forms-Designer der Form einen Shadowing <xref:System.Windows.Forms.Control.Padding%2A> Wert von 9, 9, 9, 9 an. Um dieses Verhalten zu überschreiben, weisen Sie einen anderen Wert als 0, 0, 0, 0 zu.

2. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Margin%2A> <xref:System.Windows.Forms.Control.Margin%2A> , indem Sie im **Eigenschaften** Fenster den Eintrag erweitern und die- <xref:System.Windows.Forms.Padding.All%2A> Eigenschaft auf 0 festlegen. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise: Anordnen [von Windows Forms-Steuerelementen mit Auffüll Zeichen, Rändern und der AutoSize-Eigenschaft](windows-forms-controls-padding-autosize.md).

3. Verschieben <xref:System.Windows.Forms.Button> Sie das Steuerelement in der Nähe der rechten Ecke des Formulars, bis eine Linie angezeigt wird. Diese Entfernung wird jetzt durch den Wert der-Eigenschaft des Formulars angegeben <xref:System.Windows.Forms.Control.Padding%2A> .

4. Ziehen Sie ein <xref:System.Windows.Forms.GroupBox> -Steuerelement aus der **Toolbox** auf das Formular.

5. Ändern Sie den Wert der <xref:System.Windows.Forms.GroupBox> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Padding%2A> <xref:System.Windows.Forms.Control.Padding%2A> , indem Sie im **Eigenschaften** Fenster den Eintrag erweitern und die- <xref:System.Windows.Forms.Padding.All%2A> Eigenschaft auf 10 festlegen.

6. Ziehen Sie ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** in das- <xref:System.Windows.Forms.GroupBox> Steuerelement.

7. Verschieben <xref:System.Windows.Forms.Button> Sie das Steuerelement nahe an den rechten Rand des Steuer Elements, bis eine angezeigte Linie <xref:System.Windows.Forms.GroupBox> angezeigt wird. Verschieben <xref:System.Windows.Forms.Button> Sie das Steuerelement im-Steuerelement, <xref:System.Windows.Forms.GroupBox> und stellen Sie fest, wo die Richtungslinien angezeigt werden.

## <a name="align-to-grouped-controls"></a>An gruppierten Steuerelementen ausrichten

Sie können Ausrichtungs Linien verwenden, um gruppierte Steuerelemente und Steuerelemente in einem Steuerelement auszurichten <xref:System.Windows.Forms.GroupBox> .

1. Wählen Sie zwei der Steuerelemente auf dem Formular aus. Verschieben Sie die Auswahl, und notieren Sie sich die Ausrichtungs Linien, die zwischen Ihrer Auswahl und den anderen Steuerelementen angezeigt werden.

2. Ziehen Sie ein <xref:System.Windows.Forms.GroupBox> -Steuerelement aus der **Toolbox** auf das Formular.

3. Ziehen Sie ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** in das- <xref:System.Windows.Forms.GroupBox> Steuerelement.

4. Wählen Sie eines der <xref:System.Windows.Forms.Button> Steuerelemente aus, und verschieben Sie es um das <xref:System.Windows.Forms.GroupBox> Steuerelement. Beachten Sie die Richtungslinien, die an den Rändern des Steuer Elements angezeigt werden <xref:System.Windows.Forms.GroupBox> . Beachten Sie auch die Richtungslinien, die an den Rändern des Steuer Elements angezeigt werden, die im- <xref:System.Windows.Forms.Button> Steuerelement enthalten sind <xref:System.Windows.Forms.GroupBox> . Steuerelemente, die untergeordnete Elemente eines Container Steuer Elements sind, unterstützen auch Richtungslinien.

## <a name="use-snaplines-to-place-a-control-by-outlining-its-size"></a>Verwenden von Richtungslinien zum Platzieren eines Steuer Elements durch Gliederung der Größe

1. Klicken Sie in der **Toolbox** auf das Symbol des <xref:System.Windows.Forms.Button> -Steuerelements. Ziehen Sie es nicht auf das Formular.

2. Bewegen Sie den Mauszeiger über die Entwurfs Oberfläche des Formulars. Beachten Sie, dass der Mauszeiger die Form eines Fadenkreuzes annimmt, an das das Symbol des <xref:System.Windows.Forms.Button> -Steuerelements angefügt ist. Beachten Sie auch die Ausrichtungs Linien, die für das Steuerelement ausgerichtete Positionen vorschlagen <xref:System.Windows.Forms.Button> .

3. Klicken Sie, und halten Sie die Maustaste gedrückt.

4. Ziehen Sie den Mauszeiger auf das Formular. Beachten Sie, dass ein Umriss gezeichnet wird, der die Position und die Größe des Steuer Elements angibt.

5. Ziehen Sie den Zeiger, bis er sich mit einem anderen Steuerelement im Formular anpasst. Beachten Sie, dass eine Ausrichtungslinie angezeigt wird, die die Ausrichtung angibt.

6. Lassen Sie die Maustaste los. Das-Steuerelement wird an der Position und Größe erstellt, die durch die Kontur angegeben wird.

## <a name="use-snaplines-when-dragging-a-control-from-the-toolbox"></a>Verwenden von Richtungslinien beim Ziehen eines Steuer Elements aus der Toolbox

1. Ziehen Sie ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** auf das Formular, aber lassen Sie die Maustaste los.

2. Bewegen Sie den Mauszeiger über die Entwurfs Oberfläche des Formulars. Beachten Sie, dass der Zeiger geändert wird, um die Position anzugeben, an der das neue <xref:System.Windows.Forms.Button> Steuerelement erstellt wird.

3. Ziehen Sie den Mauszeiger auf das Formular. Beachten Sie die Ausrichtungs Linien, die für das Steuerelement ausgerichtete Positionen vorschlagen <xref:System.Windows.Forms.Button> . Suchen Sie eine Position, die an anderen Steuerelementen ausgerichtet ist.

4. Lassen Sie die Maustaste los. Das Steuerelement wird an der Position erstellt, die durch die Richtungslinien angegeben wird.

## <a name="resize-a-control-using-snaplines"></a>Ändern der Größe eines Steuer Elements mithilfe von Richtungslinien

1. Ziehen Sie ein <xref:System.Windows.Forms.Button> -Steuerelement aus der **Toolbox** auf das Formular.

2. Ändern Sie die Größe des Steuer Elements, <xref:System.Windows.Forms.Button> indem Sie eine der eckzieh Punkte der Ecke und ziehen. Weitere Informationen finden Sie unter Gewusst [wie: Ändern der Größe von Steuerelementen auf Windows Forms](how-to-resize-controls-on-windows-forms.md).

3. Ziehen Sie den Ziehpunkt, bis einer der Rahmen des <xref:System.Windows.Forms.Button> Steuer Elements an einem anderen Steuerelement ausgerichtet ist. Beachten Sie, dass eine Ausrichtungslinie angezeigt wird. Beachten Sie außerdem, dass das Größen Anpassungs Handle an die von der Einfügemarke festgelegten Position anspringt.

4. Ändern Sie die Größe des <xref:System.Windows.Forms.Button> Steuer Elements in verschiedene Richtungen, und richten Sie den Zieh Punkt an verschiedene Steuerelemente aus. Beachten Sie, dass die Ausrichtungs Linien in verschiedenen Ausrichtungen angezeigt werden, um die Ausrichtung anzugeben.

## <a name="align-a-label-to-a-controls-text"></a>Ausrichten einer Bezeichnung an einem Steuerelement Text

1. Ziehen Sie ein <xref:System.Windows.Forms.TextBox> -Steuerelement aus der **Toolbox** auf das Formular. Wenn Sie das <xref:System.Windows.Forms.TextBox> Steuerelement auf dem Formular ablegen, klicken Sie auf das Smarttagsymbol, und wählen Sie die Option **Text auf textBox1 festlegen** aus. Weitere Informationen finden Sie unter Exemplarische [Vorgehensweise: Ausführen allgemeiner Aufgaben mithilfe von Designer Aktionen](perform-common-tasks-design-actions.md).

2. Ziehen Sie ein <xref:System.Windows.Forms.Label> -Steuerelement aus der **Toolbox** auf das Formular.

3. Ändern Sie den Wert der <xref:System.Windows.Forms.Label> -Eigenschaft des <xref:System.Windows.Forms.Control.AutoSize%2A> -Steuerelements in `true`. Beachten Sie, dass die Rahmen des Steuer Elements an den Anzeige Text angepasst werden.

4. Verschieben Sie das- <xref:System.Windows.Forms.Label> Steuerelement auf die linke Seite des- <xref:System.Windows.Forms.TextBox> Steuer Elements, sodass es am unteren Rand des Steuer Elements ausgerichtet ist <xref:System.Windows.Forms.TextBox> . Beachten Sie die Richtungslinie, die an den unteren Rändern der beiden Steuerelemente angezeigt wird.

5. Verschieben Sie das <xref:System.Windows.Forms.Label> Steuerelement geringfügig nach oben, bis der <xref:System.Windows.Forms.Label> Text und der <xref:System.Windows.Forms.TextBox> Text ausgerichtet sind. Beachten Sie, dass die anders formatierte Ausrichtungslinie angezeigt wird, die anzeigt, wann die Textfelder beider Steuerelemente ausgerichtet werden.

## <a name="use-snaplines-with-keyboard-navigation"></a>Verwenden von Richtungslinien mit Tastaturnavigation

1. Ziehen Sie ein <xref:System.Windows.Forms.Button> -Steuerelement aus der **Toolbox** auf das Formular. Platzieren Sie ihn in der oberen linken Ecke des Formulars.

2. Drücken Sie die **STRG**-Taste + . Beachten Sie, dass das-Steuerelement das Formular bis zur ersten verfügbaren horizontalen Ausrichtungs Position verschiebt.

3. Drücken  + **Sie STRG nach-unten-Taste** , bis das Steuerelement den unteren Bereich des Formulars erreicht. Beachten Sie die Positionen, die Sie einnimmt, wenn Sie das Formular nach unten verschieben.

4. Drücken Sie **STRG** nach- + **Rechts**. Beachten Sie, dass das-Steuerelement über das Formular an die erste verfügbare vertikale Ausrichtungs Position verschoben wird.

5. Drücken Sie **STRG** nach- + **rechts-Taste** , bis das Steuerelement die Seite des Formulars erreicht. Beachten Sie die Positionen, die Sie einnimmt, wenn Sie über das Formular bewegt werden.

6. Verschieben Sie das Steuerelement um das Formular mit einer Kombination von Pfeiltasten. Beachten Sie, welche Positionen das Steuerelement einnimmt und welche Richtungslinien es begleitet.

7. Drücken  + Sie die UMSCHALT **Pfeiltaste** , um die Größe des Steuer Elements in <xref:System.Windows.Forms.Button> Schritten von einem Pixel zu ändern.

8. Drücken Sie die **STRG**-Taste +  +  , um die Größe des Steuer Elements in den Richtungslinien zu ändern <xref:System.Windows.Forms.Button> .

## <a name="selectively-disable-snaplines"></a>Selektiv deaktivieren von Richtungslinien

1. Ziehen Sie ein <xref:System.Windows.Forms.TableLayoutPanel> -Steuerelement aus der **Toolbox** auf das Formular.

2. Doppelklicken Sie auf das Symbol des <xref:System.Windows.Forms.Button> -Steuerelements in der **Toolbox**. Beachten Sie, dass ein neues Button-Steuerelement in der ersten Zelle des Steuer Elements angezeigt wird <xref:System.Windows.Forms.TableLayoutPanel> .

3. Doppelklicken Sie <xref:System.Windows.Forms.Button> zweimal auf das Symbol für das Steuerelement in der **Toolbox** . Dadurch bleibt eine leere Zelle im- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement.

4. Ziehen Sie ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** in die leere Zelle des- <xref:System.Windows.Forms.TableLayoutPanel> Steuer Elements. Beachten Sie, dass keine Schräglinien angezeigt werden.

5. Ziehen <xref:System.Windows.Forms.Button> Sie das Steuerelement aus dem <xref:System.Windows.Forms.TableLayoutPanel> -Steuerelement, und verschieben Sie es um das <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement. Beachten Sie, dass die Richtungslinien erneut angezeigt werden.

## <a name="disable-snaplines"></a>Deaktivieren von Schräglinien

Drücken Sie die **alt** -Taste, und verschieben Sie ein Steuerelement um das Formular.

Es werden keine Ausrichtungs Linien angezeigt, und das Steuerelement wird nicht an möglichen Ausrichtungs Positionen angedostet.

### <a name="to-disable-snaplines-in-the-design-environment"></a>So deaktivieren Sie die Richtungslinien in der Entwurfs Umgebung

1. Öffnen Sie **das Dialog** Feld **Optionen** im Menü Extras. Wählen Sie **Windows Forms-Designer** aus.

2. Wählen Sie den Knoten **Allgemein** aus. Ändern Sie im Abschnitt **Layoutmodus** die Auswahl von Ausrichtungs **Linien** in **snapchanraster**.

3. Wählen Sie **OK** aus, um die Einstellung zu übernehmen.

4. Wählen Sie ein Steuerelement auf dem Formular aus, und verschieben Sie es um die anderen Steuerelemente. Beachten Sie, dass keine Richtungslinien angezeigt werden.

## <a name="next-steps"></a>Nächste Schritte

Ausrichtungs Linien bieten eine intuitive Möglichkeit zum Ausrichten von Steuerelementen auf dem Formular. Mit folgenden Funktionen können Sie Ihre Fähigkeiten vertiefen:

- Schachteln Sie ein <xref:System.Windows.Forms.GroupBox> Steuerelement in einem anderen <xref:System.Windows.Forms.GroupBox> Steuerelement Platzieren Sie ein <xref:System.Windows.Forms.Button> Steuerelement innerhalb des unter <xref:System.Windows.Forms.GroupBox> geordneten Steuer Elements und ein anderes innerhalb des übergeordneten <xref:System.Windows.Forms.GroupBox> Steuer Elements. Verschieben Sie die Steuer <xref:System.Windows.Forms.Button> Elemente, um zu sehen, wie die Richtungslinien Container Grenzen überschreiten.

- Erstellen Sie eine Spalte mit Steuer <xref:System.Windows.Forms.TextBox> Elementen und eine entsprechende Spalte von Steuer <xref:System.Windows.Forms.Label> Elementen. Legen Sie den Wert der-Eigenschaft des Steuer Elements <xref:System.Windows.Forms.Label> <xref:System.Windows.Forms.Control.AutoSize%2A> auf fest `true` . Verwenden Sie Ausrichtungs Linien, um die Steuerelemente so zu verschieben, <xref:System.Windows.Forms.Label> dass der angezeigte Text an dem Text in den Steuerelementen ausgerichtet ist <xref:System.Windows.Forms.TextBox> .

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Design.Behavior.SnapLine>
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [Exemplarische Vorgehensweise: Anordnen von Windows Forms-Steuerelementen mithilfe von Abständen, Rändern und der AutoSize-Eigenschaft](windows-forms-controls-padding-autosize.md)
