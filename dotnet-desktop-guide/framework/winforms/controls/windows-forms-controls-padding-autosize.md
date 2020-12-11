---
title: Layout von Steuerelementen mit Auffüll Zeichen, Rändern und der AutoSize-Eigenschaft
ms.date: 03/30/2017
f1_keywords:
- Margin.Bottom
- Margin.Left
- Margin.Top
- Margin.All
- Margin.Right
helpviewer_keywords:
- Margin property [Windows Forms], walkthroughs
- walkthroughs [Windows Forms], layout
- AutoSize property [Windows Forms], walkthroughs
- Padding property [Windows Forms], walkthroughs
- layout [Windows Forms], margins and padding
- Windows Forms, layout
ms.assetid: f8ae2a6b-db13-4630-8e25-d104091205c7
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: ca7942c04434592f2541252c47ac3dd17e03dbac
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975352"
---
# <a name="walkthrough-lay-out-controls-with-padding-margins-and-the-autosize-property"></a>Exemplarische Vorgehensweise: Anordnen von Steuerelementen mit Padding, Rändern und der AutoSize-Eigenschaft

Die präzise Platzierung von Steuerelementen auf dem Formular hat für viele Anwendungen einen hohen Stellenwert. Das **Windows Forms-Designer** in Visual Studio bietet Ihnen viele Layouttools, die Sie erreichen können. Drei der wichtigsten sind die <xref:System.Windows.Forms.Control.Margin%2A> <xref:System.Windows.Forms.Control.Padding%2A> Eigenschaften, und <xref:System.Windows.Forms.Control.AutoSize%2A> , die für alle Windows Forms-Steuerelemente vorhanden sind.

Die <xref:System.Windows.Forms.Control.Margin%2A>-Eigenschaft definiert den Bereich um das Steuerelement, durch den andere Steuerelemente einen bestimmten Abstand von den Rändern des Steuerelements einhalten müssen.

Die <xref:System.Windows.Forms.Control.Padding%2A>-Eigenschaft definiert den Bereich innerhalb eines Steuerelements, durch den der Inhalt des Steuerelements (z. B. der Wert seiner <xref:System.Windows.Forms.Control.Text%2A>-Eigenschaft) einen bestimmten Abstand von den Rändern des Steuerelements einhalten muss.

Die folgende Abbildung zeigt die <xref:System.Windows.Forms.Control.Padding%2A>-Eigenschaft und die <xref:System.Windows.Forms.Control.Margin%2A>-Eigenschaft für ein Steuerelement.

![Ränder und Abstände bei Windows Forms-Steuerelementen](./media/vs-winformpadmargin.gif)

Die- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft weist ein Steuerelement an, sich automatisch an seinen Inhalt zu anpassen. Die Größe wird nicht so geändert, dass Sie kleiner als der Wert der ursprünglichen <xref:System.Windows.Forms.Control.Size%2A> Eigenschaft ist, und der Wert der zugehörigen-Eigenschaft wird berücksichtigt <xref:System.Windows.Forms.Control.Padding%2A> .

## <a name="prerequisites"></a>Voraussetzungen

Sie benötigen Visual Studio, um diese exemplarische Vorgehensweise abzuschließen.

## <a name="create-the-project"></a>Erstellen des Projekts

1. Erstellen Sie in Visual Studio ein **Windows-Anwendungs** Projekt mit dem Namen `LayoutExample` .

2. Wählen Sie in der **Windows Forms-Designer** das Formular aus.

## <a name="set-margins-for-controls"></a>Ränder für Steuerelemente festlegen

Sie können den Standardabstand zwischen den Steuerelementen mithilfe der- <xref:System.Windows.Forms.Control.Margin%2A> Eigenschaft festlegen. Wenn Sie ein Steuerelement nahe genug auf ein anderes Steuerelement verschieben, wird eine Ausrichtungslinie angezeigt, in der die Ränder für die beiden Steuerelemente angezeigt werden. Das Steuerelement, das Sie verschieben, wird auch an den durch die Ränder definierten Abstand ausgerichtet.

### <a name="arrange-controls-on-your-form-using-the-margin-property"></a>Anordnen von Steuerelementen auf dem Formular mithilfe der Margin-Eigenschaft

1. Ziehen Sie zwei-Steuer <xref:System.Windows.Forms.Button> Elemente aus der **Toolbox** auf das Formular.

2. Wählen Sie eines der Steuer <xref:System.Windows.Forms.Button> Elemente aus, und verschieben Sie es in die Nähe der anderen, bis Sie fast berührt werden.

   Sehen Sie sich die angezeigte schräschlange an. Diese Distanz ist die Summe der Werte der beiden Steuerelemente <xref:System.Windows.Forms.Control.Margin%2A> . Das Steuerelement, das Sie in diese Entfernung verschieben. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Anordnen von Steuerelementen auf Windows Forms mithilfe](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)von Richtungslinien.

3. Ändern Sie die- <xref:System.Windows.Forms.Control.Margin%2A> Eigenschaft eines der Steuerelemente, indem <xref:System.Windows.Forms.Control.Margin%2A> Sie den Eintrag im **Eigenschaften** Fenster erweitern und die- <xref:System.Windows.Forms.Padding.All%2A> Eigenschaft auf **20** festlegen.

4. Wählen Sie eines der Steuer <xref:System.Windows.Forms.Button> Elemente aus, und verschieben Sie es in die Nähe des anderen.

   Die Richtungslinie, die die Summe der Randwerte definiert, ist länger, und das Steuerelement geht in einen größeren Abstand vom anderen Steuerelement.

5. Ändern Sie die- <xref:System.Windows.Forms.Control.Margin%2A> Eigenschaft des ausgewählten Steuer Elements <xref:System.Windows.Forms.Control.Margin%2A> , indem Sie im **Eigenschaften** Fenster den Eintrag erweitern und die- <xref:System.Windows.Forms.Padding.Top%2A> Eigenschaft auf **5** festlegen.

6. Verschieben Sie das ausgewählte Steuerelement unterhalb des anderen Steuer Elements, und beobachten Sie, dass die Ausrichtungslinie kürzer ist. Verschieben Sie das ausgewählte Steuerelement auf die linke Seite des anderen Steuer Elements, und beobachten Sie, dass die Ausrichtungslinie den in Schritt 4 beobachteten Wert beibehält.

7. Sie können jeden der Aspekte der- <xref:System.Windows.Forms.Control.Margin%2A> Eigenschaft,,, <xref:System.Windows.Forms.Padding.Left%2A> , <xref:System.Windows.Forms.Padding.Top%2A> <xref:System.Windows.Forms.Padding.Right%2A> <xref:System.Windows.Forms.Padding.Bottom%2A> auf unterschiedliche Werte festlegen, oder Sie können alle mit der-Eigenschaft auf denselben Wert festlegen <xref:System.Windows.Forms.Padding.All%2A> .

## <a name="set-padding-for-controls"></a>Auffüllen für Steuerelemente festlegen

Um das genaue Layout zu erzielen, das für Ihre Anwendung erforderlich ist, enthalten die Steuerelemente häufig untergeordnete Steuerelemente. Verwenden Sie die-Eigenschaft des übergeordneten Steuer Elements <xref:System.Windows.Forms.Control.Padding%2A> in Verbindung mit der-Eigenschaft des untergeordneten Steuer Elements, wenn Sie die Nähe des Rahmens des untergeordneten Steuer Elements zum Rahmen des übergeordneten Steuer Elements angeben möchten <xref:System.Windows.Forms.Control.Margin%2A> . Die <xref:System.Windows.Forms.Control.Padding%2A> -Eigenschaft wird auch zum Steuern der Nähe des Inhalts eines Steuer Elements (z. b. <xref:System.Windows.Forms.Button> die-Eigenschaft eines Steuer Elements <xref:System.Windows.Forms.Control.Text%2A> ) zu seinen Rahmen verwendet.

### <a name="arrange-controls-on-your-form-using-padding"></a>Anordnen von Steuerelementen auf dem Formular mithilfe von Auffüllung

1. Ziehen Sie ein <xref:System.Windows.Forms.Button> -Steuerelement aus der **Toolbox** auf das Formular.

2. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.AutoSize%2A> in **true**.

3. Ändern <xref:System.Windows.Forms.Control.Padding%2A> <xref:System.Windows.Forms.Control.Padding%2A> Sie die-Eigenschaft, indem Sie im **Eigenschaften** Fenster den Eintrag erweitern und die- <xref:System.Windows.Forms.Padding.All%2A> Eigenschaft auf **5** festlegen.

   Das-Steuerelement wird erweitert, um Platz für den neuen Leerraum bereitzustellen.

4. Ziehen Sie ein <xref:System.Windows.Forms.GroupBox> -Steuerelement aus der **Toolbox** auf das Formular. Ziehen Sie ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** in das- <xref:System.Windows.Forms.GroupBox> Steuerelement. Positionieren <xref:System.Windows.Forms.Button> Sie das Steuerelement so, dass es mit der unteren rechten Ecke des Steuer Elements geleert wird <xref:System.Windows.Forms.GroupBox> .

   Beachten Sie die Richtungslinien, die angezeigt werden, wenn das <xref:System.Windows.Forms.Button> -Steuerelement den unteren und rechten Rand des Steuer Elements nähert <xref:System.Windows.Forms.GroupBox> . Diese Richtungslinien entsprechen der- <xref:System.Windows.Forms.Control.Margin%2A> Eigenschaft von <xref:System.Windows.Forms.Button> .

5. Ändern <xref:System.Windows.Forms.GroupBox> Sie die-Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Padding%2A> <xref:System.Windows.Forms.Control.Padding%2A> , indem Sie den Eintrag im **Eigenschaften** Fenster erweitern und die- <xref:System.Windows.Forms.Padding.All%2A> Eigenschaft auf **20** festlegen.

6. Wählen Sie das <xref:System.Windows.Forms.Button> Steuerelement im <xref:System.Windows.Forms.GroupBox> -Steuerelement aus, und verschieben Sie es in die Mitte des <xref:System.Windows.Forms.GroupBox> .

   Die Richtungslinien werden in einer größeren Entfernung von den Rahmen des Steuer Elements angezeigt <xref:System.Windows.Forms.GroupBox> . Diese Distanz ist die Summe aus der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Margin%2A> und der <xref:System.Windows.Forms.GroupBox> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Padding%2A> .

## <a name="size-controls-automatically"></a>Größe von Steuerelementen automatisch

Bei manchen Anwendungen ist die Größe eines-Steuer Elements zur Laufzeit nicht identisch wie zur Entwurfszeit. Der Text eines <xref:System.Windows.Forms.Button> Steuer Elements kann z. b. aus einer Datenbank entnommen werden, und seine Länge ist im Voraus nicht bekannt.

Wenn die- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft auf festgelegt ist `true` , wird die Größe des Steuer Elements auf seinen Inhalt festgelegt. Weitere Informationen finden Sie unter [Übersicht über die AutoSize-Eigenschaft](autosize-property-overview.md).

### <a name="arrange-controls-on-your-form-using-the-autosize-property"></a>Anordnen von Steuerelementen auf dem Formular mithilfe der AutoSize-Eigenschaft

1. Ziehen Sie ein <xref:System.Windows.Forms.Button> -Steuerelement aus der **Toolbox** auf das Formular.

2. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.AutoSize%2A> in **true**.

3. Ändern <xref:System.Windows.Forms.Button> Sie die-Eigenschaft des Steuer Elements <xref:System.Windows.Forms.Control.Text%2A> in **diese Schaltfläche hat eine lange Zeichenfolge für die Text-Eigenschaft**.

   Wenn Sie die Änderung übertragen, <xref:System.Windows.Forms.Button> ändert sich das Steuerelement selbst an den neuen Text.

4. Ziehen Sie ein anderes <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** auf das Formular.

5. Ändern <xref:System.Windows.Forms.Button> Sie die-Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Text%2A> in "**diese Schaltfläche weist eine lange Zeichenfolge für die Text-Eigenschaft auf.**"

   Wenn Sie die Änderung übertragen, <xref:System.Windows.Forms.Button> ändert sich das Steuerelement nicht selbst, und der Text wird durch den rechten Rand des Steuer Elements abgeschnitten.

6. Ändern <xref:System.Windows.Forms.Control.Padding%2A> <xref:System.Windows.Forms.Control.Padding%2A> Sie die-Eigenschaft, indem Sie im **Eigenschaften** Fenster den Eintrag erweitern und die- <xref:System.Windows.Forms.Padding.All%2A> Eigenschaft auf **5** festlegen.

   Der Text im Inneren des Steuer Elements wird auf allen vier Seiten abgeschnitten.

7. Ändern <xref:System.Windows.Forms.Button> Sie die-Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.AutoSize%2A> in **true**.

   Die <xref:System.Windows.Forms.Button> Größe des Steuer Elements ändert sich in die gesamte Zeichenfolge. Außerdem wurde der Text Auffüllung um den Text erweitert, wodurch das <xref:System.Windows.Forms.Button> Steuerelement in alle vier Richtungen erweitert wird.

8. Ziehen Sie ein <xref:System.Windows.Forms.Button> -Steuerelement aus der **Toolbox** auf das Formular. Positionieren Sie es in der Nähe der unteren rechten Ecke des Formulars.

9. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.AutoSize%2A> in **true**.

10. Legen <xref:System.Windows.Forms.Button> Sie die-Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Anchor%2A> auf fest <xref:System.Windows.Forms.AnchorStyles.Right> <xref:System.Windows.Forms.AnchorStyles.Bottom> .

11. Ändern <xref:System.Windows.Forms.Button> Sie die-Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Text%2A> in "**diese Schaltfläche weist eine lange Zeichenfolge für die Text-Eigenschaft auf.**"

   Wenn Sie einen Commit für die Änderung durchsetzen, ändert <xref:System.Windows.Forms.Button> sich das Steuerelement in sich nach links. Im allgemeinen erhöht die automatische Größenanpassung die Größe eines Steuer Elements in der Richtung, die der <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschafts Einstellung entgegensteht.

## <a name="autosize-and-autosizemode-properties"></a>AutoSize-Eigenschaft und AutoSizeMode-Eigenschaft

 Einige Steuerelemente unterstützen die- `AutoSizeMode` Eigenschaft, die eine präzisere Steuerung des automatischen Größen Anpassungs Verhaltens eines Steuer Elements ermöglicht.

### <a name="use-the-autosizemode-property"></a>Verwenden der AutoSizeMode-Eigenschaft

1. Ziehen Sie ein <xref:System.Windows.Forms.Panel> -Steuerelement aus der **Toolbox** auf das Formular.

2. Legen Sie den Wert der <xref:System.Windows.Forms.Panel> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.AutoSize%2A> auf **true** fest.

3. Ziehen Sie ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** in das- <xref:System.Windows.Forms.Panel> Steuerelement.

4. Platzieren Sie das <xref:System.Windows.Forms.Button> Steuerelement in der Nähe der unteren rechten Ecke des- <xref:System.Windows.Forms.Panel> Steuer Elements.

5. Wählen Sie das Steuerelement aus, und ziehen Sie <xref:System.Windows.Forms.Panel> den unteren rechten Ziehpunkt. Ändern Sie die Größe des Steuer Elements, sodass es <xref:System.Windows.Forms.Panel> größer und kleiner ist.

   > [!NOTE]
   > Sie können die Größe des Steuer Elements frei ändern <xref:System.Windows.Forms.Panel> , aber Sie können es nicht kleiner als die Position der <xref:System.Windows.Forms.Button> unteren rechten Ecke des Steuer Elements anpassen. Dieses Verhalten wird durch den Standardwert der- `AutoSizeMode` Eigenschaft angegeben, d. h <xref:System.Windows.Forms.AutoSizeMode.GrowOnly> ..

6. Legen Sie den Wert der <xref:System.Windows.Forms.Panel> -Eigenschaft des-Steuer Elements `AutoSizeMode` auf fest <xref:System.Windows.Forms.AutoSizeMode.GrowAndShrink> .

   Die <xref:System.Windows.Forms.Panel> Größe des Steuer Elements, um das Steuerelement zu umschließen <xref:System.Windows.Forms.Button> . Die Größe des Steuer Elements kann nicht geändert werden <xref:System.Windows.Forms.Panel> .

7. Ziehen Sie das- <xref:System.Windows.Forms.Button> Steuerelement in die obere linke Ecke des- <xref:System.Windows.Forms.Panel> Steuer Elements.

   Das <xref:System.Windows.Forms.Panel> -Steuerelement wird an die <xref:System.Windows.Forms.Button> neue Position des-Steuer Elements angepasst.

## <a name="next-steps"></a>Nächste Schritte

Es gibt noch viele weitere Layoutfeatures zum Anordnen von Steuerelementen in Ihren Windows Forms Anwendungen. Hier sind einige Kombinationen, die Sie möglicherweise ausprobieren:

- Erstellen Sie ein Formular mithilfe eines- <xref:System.Windows.Forms.TableLayoutPanel> Steuer Elements. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Anordnen von Steuerelementen auf Windows Forms mithilfe von TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md). Versuchen Sie, die Werte der <xref:System.Windows.Forms.TableLayoutPanel> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Padding%2A> sowie die- <xref:System.Windows.Forms.Control.Margin%2A> Eigenschaft für die untergeordneten Steuerelemente zu ändern.

- Verwenden Sie das gleiche Experiment mit einem- <xref:System.Windows.Forms.FlowLayoutPanel> Steuerelement. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Anordnen von Steuerelementen auf Windows Forms mithilfe von FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md).

- Experimentieren Sie mit dem Andocken von untergeordneten Steuerelementen in einem <xref:System.Windows.Forms.Panel> Die <xref:System.Windows.Forms.Control.Padding%2A> -Eigenschaft ist eine allgemeinere Umsetzung der <xref:System.Windows.Forms.ScrollableControl.DockPadding%2A> -Eigenschaft, und Sie können sich selbst dafür sorgen, dass dies der Fall ist, indem Sie ein untergeordnetes Steuerelement in ein <xref:System.Windows.Forms.Panel> -Steuerelement einfügen und die-Eigenschaft des untergeordneten Steuer Elements <xref:System.Windows.Forms.Control.Dock%2A> auf festlegen <xref:System.Windows.Forms.DockStyle.Fill> Legen <xref:System.Windows.Forms.Panel> Sie die-Eigenschaft des Steuer Elements <xref:System.Windows.Forms.Control.Padding%2A> auf verschiedene Werte fest, und notieren Sie den Effekt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Control.AutoSize%2A>
- <xref:System.Windows.Forms.ScrollableControl.DockPadding%2A>
- <xref:System.Windows.Forms.Control.Margin%2A>
- <xref:System.Windows.Forms.Control.Padding%2A>
- [Übersicht über die AutoSize-Eigenschaft](autosize-property-overview.md)
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von Ausrichtungslinien](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
