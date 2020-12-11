---
title: Erstellen einer Vorlage in WPF
description: Erfahren Sie, wie Sie in Windows Presentation Foundation und .NET Framework eine Steuerelement Vorlage erstellen und darauf verweisen.
author: adegeo
ms.author: adegeo
ms.date: 12/03/2020
no-loc:
- <Window>
- <ControlTemplate>
- <Ellipse>
- <ContentPresenter>
- <Trigger>
- <Setter>
- <PropertyTrigger>
- <Grid>
- <VisualStateManager.VisualStateGroups>
- <VisualStateGroup>
- <VisualState>
- <Storyboard>
- SizeToContent
- MinWidth
- TargetType
- Title
ms.topic: how-to
helpviewer_keywords:
- control contract [WPF]
- controls [WPF], visual structure changes
- ControlTemplate [WPF], customizing for existing controls
- skinning controls [WPF]
- controls [WPF], appearance specified by state
- templates [WPF], custom for existing controls
ms.openlocfilehash: 0402ffbc1d6663efea4dae72878681ecfb0311d9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977823"
---
# <a name="create-a-template-for-a-control"></a>Erstellen einer Vorlage für ein Steuerelement

Mit Windows Presentation Foundation (WPF) können Sie die visuelle Struktur und das Verhalten eines vorhandenen Steuerelements mit Ihrer eigenen wiederverwendbaren Vorlage anpassen. Vorlagen können global auf Anwendungen, Fenster und Seiten oder direkt auf Steuerelemente angewendet werden. Die meisten Szenarien, in denen Sie ein neues Steuerelement erstellen müssen, können stattdessen durch Erstellen einer neuen Vorlage für ein vorhandenes Steuerelement abgedeckt werden.

In diesem Artikel erfahren Sie, wie Sie eine neue <xref:System.Windows.Controls.ControlTemplate> für das <xref:System.Windows.Controls.Button>-Steuerelement erstellen.

## <a name="when-to-create-a-controltemplate"></a>Wann sollte eine ControlTemplate erstellt werden?

Steuerelemente verfügen über viele Eigenschaften, etwa über <xref:System.Windows.Controls.Border.Background%2A>, <xref:System.Windows.Controls.Control.Foreground%2A> und <xref:System.Windows.Controls.Control.FontFamily%2A>. Diese Eigenschaften steuern verschiedene Aspekte der Darstellung des Steuerelements, aber die Änderungen, die Sie vornehmen können, indem Sie diese Eigenschaften festlegen, sind eingeschränkt. Beispielsweise können Sie die <xref:System.Windows.Controls.Control.Foreground%2A>-Eigenschaft auf „Blue“ festlegen und <xref:System.Windows.Controls.Control.FontStyle%2A> für ein <xref:System.Windows.Controls.CheckBox>-Element auf kursiv. Sie erstellen eine <xref:System.Windows.Controls.ControlTemplate>, wenn Sie die Darstellung des Steuerelements über das hinaus ändern möchten, was durch das Festlegen anderer Steuerelementeigenschaften möglich ist.

In den meisten Benutzeroberflächen weis eine Schaltfläche dieselbe allgemeine Darstellung auf: ein Rechteck mit Text. Wenn Sie eine abgerundete Schaltfläche erstellen möchten, können Sie ein neues Steuerelement erstellen, das von der Schaltfläche erbt oder die Funktionalität der Schaltfläche neu erstellt. Außerdem würde das neue Benutzersteuerelement das abgerundete visuelle Element bereitstellen.

Sie können vermeiden, neue Steuerelemente zu erstellen, indem Sie das visuelle Layout eines vorhandenen Steuerelements anpassen. Mit einer abgerundeten Schaltfläche erstellen Sie eine <xref:System.Windows.Controls.ControlTemplate> mit dem gewünschten visuellen Layout.

Wenn Sie jedoch ein Steuerelement mit neuen Funktionen, anderen Eigenschaften und neuen Einstellungen benötigen, erstellen Sie ein neues <xref:System.Windows.Controls.UserControl>-Element.

## <a name="prerequisites"></a>Voraussetzungen

Erstellen Sie eine neue WPF-Anwendung, und legen Sie in " *MainWindow. XAML* " (oder einem anderen Fenster Ihrer Wahl) die folgenden Eigenschaften für das **\: :: NO-LOC ( <Window> ):::** Element fest:

|     |     |
| --- | --- |
| **Title**         | `Template Intro Sample` |
| **SizeToContent** | `WidthAndHeight` |
| **MinWidth**      | `250` |

Legen Sie den Inhalt des **\: :: NO-LOC ( <Window> ):::-** Elements auf den folgenden XAML-Code fest:

[!code-xaml[Initial](./snippets/how-to-create-apply-template/csharp/Window1.xaml#Initial)]

Schließlich sollte die Datei *MainWindow.xaml* ähnlich wie im Folgenden aussehen:

[!code-xaml[InitialWhole](./snippets/how-to-create-apply-template/csharp/Window1.xaml#InitialWhole)]

Wenn Sie die Anwendung ausführen, sieht dies wie folgt aus:

![WPF-Fenster mit zwei Schaltflächen ohne Stilangabe](media/how-to-create-apply-template/unstyled-button.png)

## <a name="create-a-controltemplate"></a>Erstellen einer ControlTemplate

Eine <xref:System.Windows.Controls.ControlTemplate> wird üblicherweise deklariert, indem sie im Abschnitt `Resources` einer XAML-Datei als Ressource deklariert wird. Da es sich bei Vorlagen um Ressourcen handelt, unterliegen sie denselben Gültigkeitsbereichsregeln, die für alle Ressourcen gelten. Einfach ausgedrückt: Wo Sie eine Vorlage deklarieren, wirkt sich darauf aus, wo die Vorlage angewendet werden kann. Wenn Sie die Vorlage beispielsweise im Stammelement der XAML-Anwendungsdefinitionsdatei deklarieren, kann die Vorlage überall in Ihrer Anwendung verwendet werden. Wenn Sie die Vorlage in einem Fenster definieren, können nur die Steuerelemente in diesem Fenster die Vorlage verwenden.

Fügen Sie zunächst der Datei *MainWindow.xaml* ein `Window.Resources`-Element hinzu:

[!code-xaml[WindowResStart](./snippets/how-to-create-apply-template/csharp/Window2.xaml#WindowResStart)]

Erstellen Sie ein neues **\: :: NO-LOC ( <ControlTemplate> ):::** mit den folgenden Eigenschaften festgelegt:

|     |     |
| --- | --- |
| **x:Key**         | `roundbutton` |
| **TargetType**    | `Button` |

Diese Steuerelementvorlage ist einfach:

- ein Stammelement für das-Steuerelement, ein <xref:System.Windows.Controls.Grid>
- ein <xref:System.Windows.Shapes.Ellipse>-Element, um das abgerundete Aussehen der Schaltfläche zu zeichnen
- ein <xref:System.Windows.Controls.ContentPresenter>-Element, um den benutzerdefinierten Schaltflächeninhalt anzuzeigen

[!code-xaml[ControlTemplate](./snippets/how-to-create-apply-template/csharp/Window3.xaml#ControlTemplate)]

### <a name="templatebinding"></a>TemplateBinding

Beim Erstellen einer neuen <xref:System.Windows.Controls.ControlTemplate> können Sie weiterhin die öffentlichen Eigenschaften verwenden, um die Darstellung der Steuerelemente anzupassen. Die [TemplateBinding](../advanced/templatebinding-markup-extension.md)-Markuperweiterung bindet eine Eigenschaft eines in der <xref:System.Windows.Controls.ControlTemplate> enthaltenen Elements an eine vom Steuerelement definierte öffentliche Eigenschaft. Bei Verwendung einer [TemplateBinding](../advanced/templatebinding-markup-extension.md) können Steuerelementeigenschaften als Parameter der Vorlage fungieren. D.h., beim Festlegen einer Steuerelementeigenschaft wird dieser Wert an das Element mit [TemplateBinding](../advanced/templatebinding-markup-extension.md) übergeben.

### <a name="ellipse"></a>Ellipse

Beachten Sie, dass die-Eigenschaft **:::no-loc text="Fill":::** und die-Eigenschaft **:::no-loc text="Stroke":::** des **\: :: NO-LOC ( <Ellipse> ):::** -Elements an die-und-Eigenschaften des Steuer Elements gebunden sind <xref:System.Windows.Controls.Control.Foreground> <xref:System.Windows.Controls.Control.Background> .

### <a name="contentpresenter"></a>ContentPresenter

Ein [ \: :: NO-LOC ( <ContentPresenter> ):::-](xref:System.Windows.Controls.ContentPresenter) Element wird auch der Vorlage hinzugefügt. Da diese Vorlage für eine Schaltfläche konzipiert ist, müssen Sie berücksichtigen, dass die Schaltfläche von <xref:System.Windows.Controls.ContentControl> erbt. Die Schaltfläche stellt den Inhalt des Elements dar. Sie können beliebige Elemente innerhalb der Schaltfläche festlegen, z. B. Nur-Text oder sogar ein anderes Steuerelement. Beide folgenden Schaltflächen sind gültig:

```xaml
<Button>My Text</Button>

<!-- and -->

<Button>
    <CheckBox>Checkbox in a button</CheckBox>
</Button>
```

In den beiden vorherigen Beispielen werden der Text und das Kontrollkästchen als [Button.Content](xref:System.Windows.Controls.ContentControl.Content)-Eigenschaft festgelegt. Alles, was festgelegt wird, wenn der Inhalt über " **\: :: NO-LOC ( <ContentPresenter> ):::**" angezeigt werden kann, was die Vorlage bewirkt.

Wenn die <xref:System.Windows.Controls.ControlTemplate> auf einen <xref:System.Windows.Controls.ContentControl>-Typ angewendet wird, z. B. auf ein `Button`-Element, wird nach einem <xref:System.Windows.Controls.ContentPresenter>-Element in der-Elementstruktur gesucht. Wenn der `ContentPresenter` gefunden wird, bindet die Vorlage automatisch die <xref:System.Windows.Controls.ContentControl.Content>-Eigenschaft des Steuerelements an den `ContentPresenter`.

## <a name="use-the-template"></a>Verwenden der Vorlage

Suchen Sie die Schaltflächen, die zu Beginn dieses Artikels deklariert wurden.

[!code-xaml[Initial](./snippets/how-to-create-apply-template/csharp/Window1.xaml#Initial)]

Legen Sie die <xref:System.Windows.Controls.Control.Template>-Eigenschaft der zweiten Schaltfläche auf die `roundbutton`-Ressource fest:

[!code-xaml[StyledButton](./snippets/how-to-create-apply-template/csharp/Window3.xaml#StyledButton)]

Wenn Sie das Projekt ausführen und das Ergebnis untersuchen, sehen Sie, dass die Schaltfläche einen abgerundeten Hintergrund aufweist.

![WPF-Fenster mit einer ovalen Vorlagenschaltfläche](media/how-to-create-apply-template/styled-button.png)

Vielleicht haben Sie bemerkt, dass die Schaltfläche kein Kreis ist, sondern verzerrt ist. Aufgrund der Art und Weise, wie das **\: :: NO-LOC ( <Ellipse> ):::** Element funktioniert, wird es immer erweitert, um den verfügbaren Platz auszufüllen. Vereinheitlichen Sie den Kreis, indem Sie die Eigenschaften der Schaltfläche **:::no-loc text="width":::** und **:::no-loc text="height":::** in den gleichen Wert ändern:

[!code-xaml[StyledButtonSize](./snippets/how-to-create-apply-template/csharp/Window3.xaml#StyledButtonSize)]

![WPF-Fenster mit einer runden Vorlagenschaltfläche](media/how-to-create-apply-template/styled-uniform-button.png)

## <a name="add-a-trigger"></a>Hinzufügen eines Triggers

Obwohl eine Schaltfläche mit einer angewendeten Vorlage anders aussieht, verhält sie sich wie jede andere Schaltfläche. Wenn Sie auf die Schaltfläche klicken, wird das <xref:System.Windows.Controls.Primitives.ButtonBase.Click>-Ereignis ausgelöst. Möglicherweise haben Sie jedoch bemerkt, dass die visuellen Elemente der Schaltfläche nicht geändert werden, wenn Sie den Mauszeiger über die Schaltfläche bewegen. Diese visuellen Interaktionen werden alle durch die Vorlage definiert.

Durch die dynamischen Ereignis- und Eigenschaftensysteme, die von WPF bereitgestellt werden, können Sie eine bestimmte Eigenschaft für einen Wert beobachten und die Vorlage ggf. neu formatieren. In diesem Beispiel beobachten Sie die <xref:System.Windows.UIElement.IsMouseOver>-Eigenschaft der Schaltfläche. Wenn sich der Mauszeiger über dem Steuerelement befindet, formatieren Sie " **\: :: NO-LOC ( <Ellipse> ):::** " mit einer neuen Farbe. Dieser Triggertyp wird als *PropertyTrigger* bezeichnet.

Damit dies funktioniert, müssen Sie einen Namen zu " **\: :: NO-LOC ( <Ellipse> ):::** " hinzufügen, auf den Sie verweisen können. Vergeben Sie den Namen **backgroundElement**.

[!code-xaml[EllipseName](./snippets/how-to-create-apply-template/csharp/Window4.xaml#EllipseName)]

Fügen Sie als nun der [ControlTemplate.Triggers](xref:System.Windows.Controls.ControlTemplate.Triggers)-Sammlung einen neuen <xref:System.Windows.Trigger> hinzu. Der Trigger überwacht das `IsMouseOver`-Ereignis für den Wert `true`.

[!code-xaml[ControlTemplate](./snippets/how-to-create-apply-template/csharp/Window4.xaml?name=ControlTemplate&highlight=6-10)]

Fügen Sie als nächstes " **\: :: NO-LOC ( <Setter> ):::** " zu " **\: :: NO-LOC ( <Trigger> ):::** " hinzu, um die **Fill** -Eigenschaft von " **\: :: NO-LOC ( <Ellipse> )::** :" in eine neue Farbe zu ändern.

[!code-xaml[MouseOver](./snippets/how-to-create-apply-template/csharp/Window5.xaml#MouseOver)]

Führen Sie das Projekt aus. Beachten Sie, dass beim Bewegen der Maus über die Schaltfläche die Farbe von **\: :: NO-LOC ( <Ellipse> ):::** Changes geändert wird.

![Mausbewegung über die WPF-Schaltfläche, um die Füllfarbe zu ändern](media/how-to-create-apply-template/mouse-move-over-button.gif)

## <a name="use-a-visualstate"></a>Verwenden eines VisualState

Visuelle Zustände werden von einem-Steuerelement definiert und ausgelöst. Wenn die Maus z. B. über das Steuerelement bewegt wird, wird der `CommonStates.MouseOver`-Zustand ausgelöst. Sie können Eigenschaftsänderungen auf der Grundlage des aktuellen Zustands des Steuerelements animieren. Im vorherigen Abschnitt wurde ein **\: :: NO-LOC ( <PropertyTrigger> ):::** verwendet, um den Vordergrund der Schaltfläche in zu ändern, `AliceBlue` als die- `IsMouseOver` Eigenschaft war `true` . Erstellen Sie stattdessen einen visuellen Zustand, der die Änderung dieser Farbe animiert und für einen fließenden Übergang sorgt. Weitere Informationen zu *VisualStates* finden Sie unter [Stile und Vorlagen in WPF](styles-templates-overview.md#visual-states).

Um das **\: :: NO-LOC ( <PropertyTrigger> ):::** in einen animierten visuellen Zustand zu konvertieren, entfernen Sie zuerst das- **\<ControlTemplate.Triggers>** Element aus der Vorlage.

[!code-xaml[CleanTemplate](./snippets/how-to-create-apply-template/csharp/Window5.xaml#CleanTemplate)]

Fügen Sie anschließend im Verzeichnis **\: :: NO-LOC ( <Grid> ):::** root der Steuerelement Vorlage das **\: :: NO-LOC (<VisualStateManager. VisualStateGroups>)::** : Element mit a **\: :: NO-LOC ( <VisualStateGroup> )::** : for hinzu `CommonStates` . Definieren Sie zwei Zustände, `Normal` und `MouseOver`.

[!code-xaml[VisualState](./snippets/how-to-create-apply-template/csharp/Window6.xaml#VisualState)]

Alle in " **\: :: NO-LOC ( <VisualState> ):::** " definierten Animationen werden angewendet, wenn dieser Zustand ausgelöst wird. Erstellen Sie Animationen für jeden Zustand. Animationen werden in ein:: **\: No-Loc ( <Storyboard> ):::-** Element eingefügt. Weitere Informationen zu Storyboards finden Sie unter [Übersicht über Storyboards](../graphics-multimedia/storyboards-overview.md).

- Normal

  Dieser Zustand animiert die Ellipsenfüllung und stellt sie in der Farbe `Background` des Steuerelements wieder her.

  [!code-xaml[NormalState](./snippets/how-to-create-apply-template/csharp/Window6.xaml#NormalState)]

- MouseOver

  Dieser Zustand animiert die Farbe `Background` der Ellipse in eine neue Farbe: `Yellow`.

  [!code-xaml[MouseOverState](./snippets/how-to-create-apply-template/csharp/Window6.xaml#MouseOverState)]

Das **\: :: NO-LOC ( <ControlTemplate> ):::** sollte nun wie folgt aussehen.

[!code-xaml[FinalTemplate](./snippets/how-to-create-apply-template/csharp/Window7.xaml#FinalTemplate)]

Führen Sie das Projekt aus. Beachten Sie, dass beim Bewegen der Maus über die Schaltfläche die Farbe des **\: :: NO-LOC ( <Ellipse> ):::** animates ist.

![Bewegen der Maus über die WPF-Schaltfläche zum Ändern des visuellen Zustands](media/how-to-create-apply-template/mouse-move-over-button-visualstate.gif)

## <a name="next-steps"></a>Nächste Schritte

- [Stile und Vorlagen in WPF](styles-templates-overview.md)
- [Überblick über XAML-Ressourcen](../advanced/xaml-resources-define.md)
