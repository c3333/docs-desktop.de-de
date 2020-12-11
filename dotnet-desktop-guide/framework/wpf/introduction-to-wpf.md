---
title: Einführung in WPF
titleSuffix: ''
description: Sorgen Sie für eine visuell beeindruckende Benutzererfahrung in Windows. Entdecken Sie die wichtigsten Funktionen und Konzepte von Windows Presentation Foundation (WPF).
ms.date: 11/04/2016
ms.topic: overview
ms.assetid: b8d7cf43-d1f2-4f3d-adb0-4f3a6428edc0
dev_langs:
- csharp
- vb
ms.openlocfilehash: 9eb2ca898413a07c58ac868900a278e02fd1f587
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978184"
---
# <a name="wpf-overview"></a>WPF-Übersicht

Mit Windows Presentation Foundation (WPF) können Sie Desktop-Clientanwendungen für Windows erstellen, die visuell herausragende Benutzeroberflächen haben.

![Contoso Healthcare-Beispiel](media/introduction-to-wpf/wpfintrofigure24.png)

Der Kern von WPF ist eine auflösungsunabhängige und vektorbasierte Rendering-Engine, die die Leistungsfähigkeit moderner Grafikhardware nutzt. Dieser Kern wird durch WPF um mehrere Anwendungsentwicklungsfeatures erweitert, wozu Extensible Application Markup Language (XAML), Steuerelemente, Datenbindung, Layout, 2D- und 3D-Grafik, Animationen, Stile, Vorlagen, Dokumente, Medien, Text und Typographie zählen. WPF ist Teil von .NET. Sie können also Anwendungen erstellen, die andere Elemente der .NET-API beinhalten.

Diese Übersicht ist für Einsteiger gedacht und beschreibt die wichtigsten Funktionen und Konzepte von WPF.

## <a name="program-with-wpf"></a>Programmieren mit WPF

WPF ist eine Teilmenge von .NET-Typen, die sich (zum größten Teil) im <xref:System.Windows>-Namespace befinden. Wenn Sie bereits Anwendungen mit .NET und verwalteten Technologien wie ASP.NET und Windows Forms erstellt haben, sind Sie mit den Grundlagen der WPF-Programmierung vertraut. Sie instanziieren Klassen, legen Eigenschaften fest, rufen Methoden auf und behandeln Ereignisse und verwenden dafür Ihre bevorzugte .NET Framework-Programmiersprache, etwa C# oder Visual Basic.

WPF umfasst zusätzliche Programmierkonstrukte, mit denen Eigenschaften und Ereignisse erweitert werden: [Abhängigkeitseigenschaften](advanced/dependency-properties-overview.md) und [Routingereignisse](advanced/routed-events-overview.md).

## <a name="markup-and-code-behind"></a>Markup und CodeBehind

WPF ermöglicht es Ihnen, eine Anwendung sowohl mit *Markup* als auch mit *CodeBehind* zu entwickeln, eine Vorgehensweise, mit der ASP.NET-Entwickler vertraut sein sollten. Im Grundsatz verwenden Sie XAML-Markup, um die Darstellung einer Anwendung zu implementieren, und verwaltete Programmiersprachen (CodeBehind), um das Verhalten der Anwendung zu implementieren. Diese Trennung von Darstellung und Verhalten bietet folgende Vorteile:

- Entwicklungs- und Wartungskosten werden verringert, weil darstellungsspezifisches Markup nicht unmittelbar mit verhaltensspezifischem Code gekoppelt ist.

- Die Entwicklung ist effizienter, da Designer die Darstellung einer Anwendung implementieren können, während Entwickler gleichzeitig das Verhalten der Anwendung implementieren.

- Die[Globalisierung und Lokalisierung](advanced/wpf-globalization-and-localization-overview.md) für WPF-Anwendungen wird stark vereinfacht.

### <a name="markup"></a>Markup

XAML ist eine auf XML basierende Markupsprache, mit der die Darstellung einer Anwendung deklarativ implementiert werden kann. Sie wird üblicherweise dazu verwendet, Fenster, Dialogfelder, Seiten und Benutzersteuerelemente zu erstellen und diese mit Steuerelementen, Formen und Grafiken zu füllen.

Im folgenden Beispiel wird XAML verwendet, um die Darstellung eines Fensters zu implementieren, das eine einzelne Schaltfläche enthält:

```xaml
<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    Title="Window with Button"
    Width="250" Height="100">

  <!-- Add button to window -->
  <Button Name="button">Click Me!</Button>

</Window>
```

In diesem XAML-Code werden ein Fenster und eine Schaltfläche definiert, indem das `Window` - und das `Button` -Element verwendet werden. Jedes Element wird mit Attributen konfiguriert. Hier wird beispielsweise das `Window` -Attribut des `Title` -Elements verwendet, um den Text für die Titelleiste des Fensters festzulegen. Zur Laufzeit werden die im Markup definierten Elemente und Attribute von WPF in Instanzen von WPF-Klassen konvertiert. Beispielsweise wird das `Window` -Element in eine Instanz der <xref:System.Windows.Window> -Klasse konvertiert, deren <xref:System.Windows.Window.Title%2A> -Eigenschaft dem Wert des `Title` -Attributs entspricht.

Die folgende Abbildung zeigt die Benutzeroberfläche (UI), die vom XAML-Code im vorherigen Beispiel definiert wurde:

![Ein Fenster, das eine Schaltfläche enthält](media/introduction-to-wpf/wpfintrofigure10.png)

Da XAML auf XML basiert, wird die damit erstellte Benutzeroberfläche in einer Hierarchie geschachtelter Elemente zusammengestellt, die als [Elementstruktur](advanced/trees-in-wpf.md)bezeichnet wird. Die Elementstruktur stellt eine logische und intuitive Art und Weise zum Erstellen und Verwalten von Benutzeroberflächen bereit.

### <a name="code-behind"></a>CodeBehind

Der Hauptzweck einer Anwendung besteht darin, die Funktionalität zu implementieren, mit der auf Benutzeraktionen reagiert wird, wozu auch das Behandeln von Ereignissen (z. B. Klicken auf Menüs, Symbolleisten oder Schaltflächen) sowie das Aufrufen von Geschäftslogik und als Reaktion darauf von Datenzugriffslogik zählen. In WPF wird dieses Verhalten in Code implementiert, der mit Markup verknüpft ist. Diese Art von Code wird als CodeBehind bezeichnet. Das folgende Beispiel zeigt das aktualisierte Markup aus dem vorherigen Beispiel und den Code-Behind:

```xaml
<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    x:Class="SDKSample.AWindow"
    Title="Window with Button"
    Width="250" Height="100">

  <!-- Add button to window -->
  <Button Name="button" Click="button_Click">Click Me!</Button>

</Window>
```

```csharp
using System.Windows; // Window, RoutedEventArgs, MessageBox

namespace SDKSample
{
    public partial class AWindow : Window
    {
        public AWindow()
        {
            // InitializeComponent call is required to merge the UI
            // that is defined in markup with this class, including  
            // setting properties and registering event handlers
            InitializeComponent();
        }

        void button_Click(object sender, RoutedEventArgs e)
        {
            // Show message box when button is clicked.
            MessageBox.Show("Hello, Windows Presentation Foundation!");
        }
    }
}
```

```vb
Namespace SDKSample

    Partial Public Class AWindow
        Inherits System.Windows.Window

        Public Sub New()

            ' InitializeComponent call is required to merge the UI
            ' that is defined in markup with this class, including  
            ' setting properties and registering event handlers
            InitializeComponent()

        End Sub

        Private Sub button_Click(ByVal sender As Object, ByVal e As RoutedEventArgs)

            ' Show message box when button is clicked.
            MessageBox.Show("Hello, Windows Presentation Foundation!")

        End Sub

    End Class

End Namespace
```

In diesem Beispiel wird im CodeBehind eine Klasse implementiert, die aus der <xref:System.Windows.Window> -Klasse abgeleitet wird. Das `x:Class` -Attribut wird verwendet, um den Markupcode mit der CodeBehind-Klasse zu verknüpfen. `InitializeComponent` wird vom Konstruktor der CodeBehind-Klasse aufgerufen, um die im Markup definierte Benutzeroberfläche mit der CodeBehind-Klasse zusammenzuführen. ( `InitializeComponent` wird für Sie generiert, wenn Ihre Anwendung erstellt wird. aus diesem Grund müssen Sie Sie nicht manuell implementieren.) Durch die Kombination von `x:Class` und `InitializeComponent` wird sichergestellt, dass die Implementierung bei jeder Erstellung ordnungsgemäß initialisiert wird. In der CodeBehind-Klasse wird außerdem ein Ereignishandler für das <xref:System.Windows.Controls.Primitives.ButtonBase.Click>-Ereignis der Schaltfläche implementiert. Wird auf die Schaltfläche geklickt, zeigt der Ereignishandler ein Meldungsfeld an, indem er die <xref:System.Windows.MessageBox.Show%2A?displayProperty=fullName> -Methode aufruft.

In der folgenden Abbildung wird das Ergebnis angezeigt, wenn auf die Schaltfläche geklickt wird:

![Eine MessageBox](media/introduction-to-wpf/wpfintrofigure25.png)

## <a name="controls"></a>Steuerelemente

Die Elemente einer Benutzeroberfläche, die mit dem Anwendungsmodell bereitgestellt werden, sind konstruierte Steuerelemente. In WPF ist *Steuerelement* ein Sammelbegriff, der sich auf eine Kategorie von WPF-Klassen bezieht, die entweder in einem Fenster oder auf einer Seite gehostet werden, eine Benutzeroberfläche haben und ein bestimmtes Verhalten implementieren.

Weitere Informationen finden Sie unter Steuer [Elemente](controls/index.md).

### <a name="wpf-controls-by-function"></a>WPF-Steuerelemente nach Funktion

Die integrierten WPF-Steuerelemente sind hier aufgeführt:

- **Schalt** Flächen: <xref:System.Windows.Controls.Button> und <xref:System.Windows.Controls.Primitives.RepeatButton> .

- **Datenanzeige**: <xref:System.Windows.Controls.DataGrid> , <xref:System.Windows.Controls.ListView> und <xref:System.Windows.Controls.TreeView> .

- **Datumsanzeige und-Auswahl**: <xref:System.Windows.Controls.Calendar> und <xref:System.Windows.Controls.DatePicker> .

- **Dialog Felder**: <xref:Microsoft.Win32.OpenFileDialog> , <xref:System.Windows.Controls.PrintDialog> und <xref:Microsoft.Win32.SaveFileDialog> .

- **Digitales** frei Hand Eingaben: <xref:System.Windows.Controls.InkCanvas> und <xref:System.Windows.Controls.InkPresenter> .

- **Dokumente**: <xref:System.Windows.Controls.DocumentViewer> , <xref:System.Windows.Controls.FlowDocumentPageViewer> , <xref:System.Windows.Controls.FlowDocumentReader> , <xref:System.Windows.Controls.FlowDocumentScrollViewer> und <xref:System.Windows.Controls.StickyNoteControl> .

- **Eingabe**: <xref:System.Windows.Controls.TextBox> , <xref:System.Windows.Controls.RichTextBox> und <xref:System.Windows.Controls.PasswordBox> .

- **Layout**: <xref:System.Windows.Controls.Border> , <xref:System.Windows.Controls.Primitives.BulletDecorator> , <xref:System.Windows.Controls.Canvas> , <xref:System.Windows.Controls.DockPanel> , <xref:System.Windows.Controls.Expander> , <xref:System.Windows.Controls.Grid> , <xref:System.Windows.Controls.GridView> , <xref:System.Windows.Controls.GridSplitter> , <xref:System.Windows.Controls.GroupBox> , <xref:System.Windows.Controls.Panel> , <xref:System.Windows.Controls.Primitives.ResizeGrip> , <xref:System.Windows.Controls.Separator> , <xref:System.Windows.Controls.Primitives.ScrollBar> , <xref:System.Windows.Controls.ScrollViewer> , <xref:System.Windows.Controls.StackPanel> , <xref:System.Windows.Controls.Primitives.Thumb> , <xref:System.Windows.Controls.Viewbox> , <xref:System.Windows.Controls.VirtualizingStackPanel> , <xref:System.Windows.Window> und <xref:System.Windows.Controls.WrapPanel> .

- **Medien**: <xref:System.Windows.Controls.Image> , <xref:System.Windows.Controls.MediaElement> und <xref:System.Windows.Controls.SoundPlayerAction> .

- **Menüs**: <xref:System.Windows.Controls.ContextMenu> , <xref:System.Windows.Controls.Menu> und <xref:System.Windows.Controls.ToolBar> .

- **Navigation**: <xref:System.Windows.Controls.Frame> , <xref:System.Windows.Documents.Hyperlink> , <xref:System.Windows.Controls.Page> , <xref:System.Windows.Navigation.NavigationWindow> und <xref:System.Windows.Controls.TabControl> .

- **Auswahl**: <xref:System.Windows.Controls.CheckBox> , <xref:System.Windows.Controls.ComboBox> , <xref:System.Windows.Controls.ListBox> , <xref:System.Windows.Controls.RadioButton> und <xref:System.Windows.Controls.Slider> .

- **Benutzerinformationen**: <xref:System.Windows.Controls.AccessText> , <xref:System.Windows.Controls.Label> , <xref:System.Windows.Controls.Primitives.Popup> , <xref:System.Windows.Controls.ProgressBar> , <xref:System.Windows.Controls.Primitives.StatusBar> , <xref:System.Windows.Controls.TextBlock> und <xref:System.Windows.Controls.ToolTip> .

## <a name="input-and-commands"></a>Eingabe und Befehle

Steuerelemente sind üblicherweise dafür vorgesehen, Benutzereingaben zu erkennen und darauf zu reagieren. Im [WPF-Eingabesystem](advanced/input-overview.md) werden sowohl direkte Ereignisse als auch Routingereignisse verwendet, um Texteingaben, Fokusverwaltung und Mauspositionierung zu unterstützen.

Anwendungen haben häufig komplexe Eingabeanforderungen. WPF stellt ein [Befehlssystem](advanced/commanding-overview.md) bereit, über das Eingabeaktionen eines Benutzers von dem Code getrennt sind, mit dem auf diese Aktionen reagiert wird.

## <a name="layout"></a>Layout

Wenn Sie eine Benutzeroberfläche erstellen, ordnen Sie die Steuerelemente nach Position und Größe an, um ein Layout zu formen. Eine Hauptanforderung für jedes Layout besteht darin, sich an Änderungen der Fenstergröße und Anzeigeeinstellungen anpassen zu können. WPF bietet ein erstklassiges erweiterbares Layoutsystem, sodass Sie keinen zusätzlichen Code schreiben müssen, um ein Layout in diesen Fällen anzupassen.

Die Basis des Layoutsystems ist relative Positionierung, wodurch die Fähigkeit zur Anpassung an geänderte Fenster- und Anzeigebedingungen verbessert wird. Das Layoutsystem verwaltet außerdem die Aushandlung zwischen Steuerelementen, um das Layout zu bestimmen. Die Aushandlung ist ein zweistufiger Vorgang: Zuerst teilt ein Steuerelement seinem übergeordneten Element mit, welche Position und Größe es benötigt, und anschließend teilt das übergeordnete Element dem Steuerelement mit, welcher Raum ihm zur Verfügung steht.

Das Layoutsystem wird untergeordneten Steuerelementen über WPF-Basisklassen verfügbar gemacht. Für allgemeine Layouts wie Raster, Stapeln und Andocken enthält WPF mehrere Layoutsteuerelemente:

- <xref:System.Windows.Controls.Canvas>: Untergeordnete Steuerelemente stellen ihr eigenes Layout bereit.

- <xref:System.Windows.Controls.DockPanel>: Untergeordnete Steuerelemente werden an den Rändern des Bereichs ausgerichtet.

- <xref:System.Windows.Controls.Grid>: Untergeordnete Steuerelemente werden anhand von Zeilen und Spalten positioniert.

- <xref:System.Windows.Controls.StackPanel>: Untergeordnete Steuerelemente werden entweder vertikal oder horizontal gestapelt.

- <xref:System.Windows.Controls.VirtualizingStackPanel>: Untergeordnete Steuerelemente werden virtualisiert und auf einer einzelnen Linie angeordnet, die horizontal oder vertikal verläuft.

- <xref:System.Windows.Controls.WrapPanel>: Untergeordnete Steuerelemente werden der Reihe nach von links nach rechts angeordnet und, wenn sich in der jeweiligen Zeile mehr Steuerelemente befinden, als der Platz zulässt, ggf. auf die nächste Zeile umbrochen.

Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Controls.DockPanel> , um mehrere Steuerelemente zu bilden <xref:System.Windows.Controls.TextBox> :

[!code-xaml[IntroToWPFSnippets#LayoutMARKUP](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_1.xaml)]

Das <xref:System.Windows.Controls.DockPanel>-Objekt ermöglicht es den untergeordneten <xref:System.Windows.Controls.TextBox>-Steuerelementen, ihm Informationen über ihre Anordnung bereitzustellen. Dazu wird von der <xref:System.Windows.Controls.DockPanel>-Klasse die angehängte `Dock`-Eigenschaft implementiert, die für die untergeordneten Steuerelemente verfügbar gemacht wird, damit jedes von ihnen eine Andockart festlegen kann.

> [!NOTE]
> Eine Eigenschaft, die von einem übergeordneten Steuerelement zur Verwendung durch untergeordnete Steuerelemente implementiert wird, ist ein WPF-Konstrukt, das als [angefügte Eigenschaft](advanced/attached-properties-overview.md) bezeichnet wird.

In der folgenden Abbildung wird das Ergebnis des XAML-Markups im vorherigen Beispiel gezeigt:

![DockPanel-Seite](media/introduction-to-wpf/wpfintrofigure11.png)

## <a name="data-binding"></a>Datenbindung

Die meisten Anwendungen werden erstellt, um Benutzern die Möglichkeit zum Anzeigen und Bearbeiten von Daten bereitzustellen. Bei WPF-Anwendungen wird die Arbeit zum Speichern und Zugreifen auf Daten von Technologien wie Microsoft SQL Server und ADO.NET übernommen. Nachdem auf die Daten zugegriffen wurde und diese in die verwalteten Objekte einer Anwendung geladen wurden, beginnt die harte Arbeit für WPF-Anwendungen. Dies umfasst im Wesentlichen zwei Dinge:

1. Kopieren der Daten aus den verwalteten Objekten in Steuerelemente, wo die Daten angezeigt und bearbeitet werden können.

2. Sicherstellen, dass Änderungen, die über Steuerelemente an den Daten vorgenommen wurden, in die verwalteten Objekte kopiert werden.

Um die Entwicklung von Anwendungen zu vereinfachen, stellt WPF eine Datenbindungs-Engine bereit, mit dem diese Schritte automatisch ausgeführt werden können. Das Kernelement der Datenbindungs-Engine ist die <xref:System.Windows.Data.Binding> , deren Aufgabe es ist, ein Steuerelement (das Bindungsziel) an ein Datenobjekt (die Bindungsquelle) zu binden. Diese Beziehung wird in der folgenden Abbildung veranschaulicht:

![Grundlegendes Datenbindungsdiagramm](media/introduction-to-wpf/databindingmostbasic.png)

Im nächsten Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.TextBox>-Objekt an eine Instanz eines benutzerdefinierten `Person`-Objekts gebunden wird. Die `Person`-Implementierung wird im folgenden Beispielcode dargestellt:

[!code-vb[SimpleDataBindingSnippets#PersonClassCODE](~/samples/snippets/visualbasic/wpf/introduction-to-wpf/introduction-to-wpf_2.vb)]
[!code-csharp[SimpleDataBindingSnippets#PersonClassCODE](~/samples/snippets/csharp/wpf/introduction-to-wpf/introduction-to-wpf_2.cs)]

Das folgende Markup bindet das <xref:System.Windows.Controls.TextBox> an eine Instanz eines benutzerdefinierten- `Person` Objekts:

```xaml
 <Window
     xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
     xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
     x:Class="SDKSample.DataBindingWindow">

   <!-- Bind the TextBox to the data source (TextBox.Text to Person.Name) -->
   <TextBox Name="personNameTextBox" Text="{Binding Path=Name}" />

 </Window>
```

[!code-vb[SimpleDataBindingSnippets#DataBindingCODEBEHIND](~/samples/snippets/visualbasic/wpf/introduction-to-wpf/introduction-to-wpf_6.vb)]
[!code-csharp[SimpleDataBindingSnippets#DataBindingCODEBEHIND](~/samples/snippets/csharp/wpf/introduction-to-wpf/introduction-to-wpf_6.cs)]

In diesem Beispiel wird die `Person` -Klasse in CodeBehind instanziiert und als Datenkontext für die `DataBindingWindow`-Klasse festgelegt. Im Markupcode wird die <xref:System.Windows.Controls.TextBox.Text%2A> -Eigenschaft des <xref:System.Windows.Controls.TextBox> -Steuerelements an die `Person.Name` -Eigenschaft gebunden (über die XAML-Syntax`{Binding ... }`). Dieser XAML-Code weist WPF an, das <xref:System.Windows.Controls.TextBox> -Steuerelement an das `Person` -Objekt zu binden, das in der <xref:System.Windows.FrameworkElement.DataContext%2A> -Eigenschaft des Fensters gespeichert ist.

Die Datenbindungs-Engine von WPF bietet zusätzliche Unterstützung, wozu Validierung, Sortierung, Filterung und Gruppierung gehören. Darüber hinaus wird für Datenbindung die Verwendung von Datenvorlagen unterstützt, um eine benutzerdefinierte Benutzeroberfläche für gebundene Daten zu erstellen, wenn die Benutzeroberfläche nicht geeignet ist, die von den WPF-Standardsteuerelementen angezeigt wird.

Weitere Informationen finden Sie unter [Übersicht über Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview).

## <a name="graphics"></a>Grafiken

Mit WPF wird ein umfangreicher, skalierbarer und flexibler Satz von Grafikfeatures eingeführt, die die folgenden Vorteile bieten:

- **Auflösungsunabhängige und geräteunabhängige Grafik**. Die grundlegende Maßeinheit im WPF-Grafiksystem ist das geräteunabhängige Pixel, das, unabhängig von der jeweiligen Bildschirmauflösung, immer 1/96 Zoll entspricht. Diese Maßeinheit bildet die Grundlage für auflösungs- und geräteunabhängiges Rendering. Jedes geräteunabhängige Pixel wird automatisch skaliert, um mit der DPI-Einstellung (Dots Per Inch) des Systems übereinzustimmen, auf dem das Pixel gerendert wird.

- **Höhere Genauigkeit**. Das WPF-Koordinatensystem wird mit Gleitkommazahlen mit doppelter Genauigkeit gemessen. Transformationen und Durchlässigkeitswerte werden ebenfalls mit doppelter Genauigkeit ausgedrückt. WPF unterstützt auch eine breite Farbskala (scRGB) und unterstützt das Verwalten von Eingaben aus unterschiedlichen Farbräumen.

- **Erweiterte Unterstützung für Grafiken und Animationen**. WPF vereinfacht die Grafikprogrammierung, indem es Animationsszenen für Sie verwaltet. Sie müssen sich keine Gedanken über Szenenverarbeitung, Renderingschleifen und bilineare Interpolation machen. Darüber bietet WPF Treffertest-Unterstützung und vollständige Alpha-Compositing-Unterstützung.

- **Hardware Beschleunigung**. Das WPF-Grafiksystem nutzt die Vorteile der Grafikhardware, um die CPU-Auslastung zu verringern.

### <a name="2d-shapes"></a>2D-Formen

Zu WPF gehört eine Bibliothek häufig verwendeter vektorbasierter 2D-Formen, etwa Rechtecke und Ellipsen, die in der folgenden Abbildung dargestellt sind:

![Ellipsen und Rechtecke](media/introduction-to-wpf/wpfintrofigure4.PNG)

Eine interessante Fähigkeit von Formen ist, dass sie nicht nur zur Anzeige vorhanden sind, sondern für sie auch viele der Features implementiert sind, die Sie von Steuerelementen erwarten, einschließlich Tastatur- und Mauseingaben. Das folgende Beispiel zeigt das- <xref:System.Windows.UIElement.MouseUp> Ereignis einer <xref:System.Windows.Shapes.Ellipse> , die behandelt wird:

[!code-xaml[IntroToWPFSnippets#HandleEllipseMouseUpEventMARKUP](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_7.xaml)]

[!code-vb[IntroToWPFSnippets#HandleEllipseMouseUpEventCODEBEHIND](~/samples/snippets/visualbasic/wpf/introduction-to-wpf/introduction-to-wpf_8.vb)]
[!code-csharp[IntroToWPFSnippets#HandleEllipseMouseUpEventCODEBEHIND](~/samples/snippets/csharp/wpf/introduction-to-wpf/introduction-to-wpf_8.cs)]

In der folgenden Abbildung wird gezeigt, was durch den vorangehenden Code erzeugt wird:

![Ein Fenster mit dem Text "you clicked the ellipse&#33;" (Sie haben auf das Auslassungszeichen geklickt).](media/introduction-to-wpf/wpfintrofigure12.png)

Weitere Informationen finden Sie unter [Übersicht über Formen und grundlegende Zeichnungen in WPF](/dotnet/desktop-wpf/data/data-binding-overview).

### <a name="2d-geometries"></a>2D-Geometrien

Die von WPF bereitgestellten 2D-Formen decken die grundlegenden Standardformen ab. Möglicherweise müssen Sie jedoch benutzerdefinierte Formen erstellen, um den Entwurf einer angepassten Benutzeroberfläche zu ermöglichen. Zu diesem Zweck stellt WPF Geometrien bereit. In der folgenden Abbildung wird veranschaulicht, wie Geometrien verwendet werden können, um eine benutzerdefinierte Form zu erstellen, die direkt gezeichnet, als Pinsel verwendet oder dazu verwendet werden kann, andere Formen und Steuerelemente auszuschneiden.

Mit<xref:System.Windows.Shapes.Path> -Objekten können geschlossene oder offene Formen, Mehrfachformen und sogar gekrümmte Formen gezeichnet werden.

<xref:System.Windows.Media.Geometry>-Objekte können zum Ausschneiden, zum Ausführen von Treffertests und zum Rendern von 2D-Grafikdaten verwendet werden.

![Verschiedene Einsatzbereiche eines Pfades](media/introduction-to-wpf/wpfintrofigure5.png)

Weitere Informationen finden Sie unter [Übersicht über die Geometrie](graphics-multimedia/geometry-overview.md).

### <a name="2d-effects"></a>2D-Effekte

Eine Teilmenge der 2D-Funktionen von WPF umfasst visuelle Effekte wie Farbverläufe, Bitmaps, Zeichnungen, Zeichnen mit Videos, Drehung, Skalierung und Neigung. Diese werden alle mit Pinsel erreicht. in der folgenden Abbildung werden einige Beispiele gezeigt:

![Darstellung unterschiedlicher Pinsel](media/introduction-to-wpf/wpfintrofigure6.png)

Weitere Informationen finden Sie unter [Übersicht über WPF-Pinsel](graphics-multimedia/wpf-brushes-overview.md).

### <a name="3d-rendering"></a>3D-Rendering

WPF beinhaltet auch 3D-Renderingfunktionen, die mit 2D-Grafiken integriert werden können, um die Erstellung ansprechendere und interessanter Benutzeroberflächen zu ermöglichen. Beispielsweise zeigt die folgende Abbildung 2D-Bilder, die auf 3D-Formen gerendert werden:

![Bildschirmabbildung für Visual3D-Beispiel](media/introduction-to-wpf/wpfintrofigure13.png)

Weitere Informationen finden Sie unter [Übersicht über 3D-Grafiken](graphics-multimedia/3-d-graphics-overview.md).

## <a name="animation"></a>Animation

Die WPF-Animationsunterstützung ermöglicht es Ihnen, Steuerelemente wachsen, bewegen, schütteln sowie ein- und ausblenden zu lassen, um interessante Seitenübergänge zu erstellen, und vieles mehr. Die meisten WPF-Klassen, selbst benutzerdefinierte Klassen, können animiert werden. In der folgenden Abbildung wird eine einfache Animation in Aktion gezeigt:

![Bilder eines animierten Cubes](media/introduction-to-wpf/wpfintrofigure7.png)

Weitere Informationen finden Sie unter [Übersicht über Animationen](graphics-multimedia/animation-overview.md).

## <a name="media"></a>Medien

Eine Möglichkeit, Inhalte interessant zu vermitteln, ist die Verwendung audiovisueller Medien. WPF bietet spezielle Unterstützung für Bilder, Video und Audio.

### <a name="images"></a>Bilder

In den meisten Anwendungen werden Bilder verwendet, und WPF bietet mehrere Möglichkeiten, Bilder zu verwenden. Die folgende Abbildung zeigt eine Benutzeroberfläche mit einem Listenfeld, das Miniaturbilder enthält. Wird eine Miniaturansicht ausgewählt, wird das Bild in voller Größe angezeigt.

![Miniaturbilder und ein Bild in voller Größe](media/introduction-to-wpf/wpfintrofigure8.png)

Weitere Informationen finden Sie unter [Übersicht über die Bildverarbeitung](graphics-multimedia/imaging-overview.md).

### <a name="video-and-audio"></a>Video und Audio

Mit dem <xref:System.Windows.Controls.MediaElement> -Steuerelement kann sowohl Video als auch Audio wiedergegeben werden, und es ist flexibel genug, um als Grundlage für einen benutzerdefinierten Media Player verwendet zu werden. Mit dem folgenden XAML-Markup wird ein Media Player implementiert:

[!code-xaml[IntroToWPFSnippets#MediaElementMARKUP](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_9.xaml)]

Das-Fenster in der folgenden Abbildung zeigt das- <xref:System.Windows.Controls.MediaElement> Steuerelement in Aktion an:

![Ein MediaElement-Steuerelement mit Audio und Video](media/introduction-to-wpf/wpfintrofigure1.png)

Weitere Informationen finden Sie unter [Grafiken und Multimedia](graphics-multimedia/index.md).

## <a name="text-and-typography"></a>Text und Typografie

Um ein qualitativ hochwertiges Textrendering zu ermöglichen, bietet WPF die folgenden Features:

- Unterstützung für OpenType-Schriftarten

- ClearType-Optimierungen

- Hohe Leistung durch Nutzung von Hardwarebeschleunigung

- Einbinden von Text in Medien, Grafiken und Animationen

- Unterstützung internationaler Schriftarten und Fallbackmechanismen

Die folgende Abbildung zeigt die Anwendung von Text Dekorationen, um die Text Integration mit Grafiken zu demonstrieren:

![Text mit verschiedenen Textergänzungen](media/introduction-to-wpf/wpfintrofigure23.png)

Weitere Informationen finden Sie unter [Typografie in WPF](advanced/typography-in-wpf.md).

## <a name="customize-wpf-apps"></a>Anpassen von WPF-Apps

Bis zu dieser Stelle haben die WPF-Kernbausteine zur Entwicklung von Anwendungen kennen gelernt. Sie verwenden das Anwendungsmodell, um Anwendungsinhalte, die hauptsächlich aus Steuerelementen bestehen, zu hosten und bereitzustellen. Das WPF-Layoutsystem verwenden Sie, um die Anordnung von Steuerelementen in einer Benutzeroberfläche zu vereinfachen und sicherzustellen, dass die Anordnung bei Änderungen von Fenstergröße und Anzeigeeinstellungen erhalten bleibt. Da die meisten Anwendungen Benutzern ein Bearbeiten von Daten ermöglichen, verwenden Sie Datenbindung, um den Arbeitsaufwand für das Einbinden der Daten in die jeweilige Benutzeroberfläche zu reduzieren. Um die visuelle Darstellung Ihrer Anwendung zu verbessern, verwenden Sie die umfangreiche Grafik-, Animations- und Medienunterstützung, die von WPF bereitgestellt wird.

Häufig reichen die Grundelemente jedoch nicht aus, um eine wirklich herausragende und visuell eindrucksvolle Benutzeroberfläche zu erstellen und zu verwalten. Die Standardsteuerelemente von WPF passen möglicherweise nicht zum gewünschten Erscheinungsbild Ihrer Anwendung. Daten können vielleicht nicht auf die bestmögliche Art angezeigt werden. Der Gesamteindruck Ihrer Anwendung ist eventuell nicht für das standarmäßige Aussehen und Verhalten der Windows-Designs geeignet. In vielerlei Hinsicht erfordert eine Präsentationstechnologie visuelle Erweiterbarkeit ebenso wie jede andere Art von Erweiterbarkeit.

Aus diesem Grund bietet die WPF eine Vielzahl von Mechanismen zum Erzeugen einzigartiger Benutzeroberflächen, wie z. B. ein umfangreiches Inhaltsmodell für Steuerelemente, Trigger, Steuerelement- und Datenvorlagen, Stile, Ressourcen für Benutzeroberflächen, Designs und Skins.

### <a name="content-model"></a>Inhaltsmodell

Die meisten WPF-Steuerelemente haben hauptsächlich die Aufgabe, Inhalte anzuzeigen. In WPF werden der Typ und die Anzahl von Elementen, die den Inhalt eines Steuerelements bilden können, als *Inhaltsmodell* des Steuerelements bezeichnet. Einige Steuerelemente können ein einzelnes Element und einen einzelnen Inhaltstyp enthalten. Beispielsweise ist der Inhalt eines <xref:System.Windows.Controls.TextBox> -Steuerelements ein Zeichenfolgenwert, der der <xref:System.Windows.Controls.TextBox.Text%2A> -Eigenschaft zugewiesen ist. Im folgenden Beispiel wird der Inhalt einer festgelegt <xref:System.Windows.Controls.TextBox> :

```xaml
<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    x:Class="SDKSample.TextBoxContentWindow"
    Title="TextBox Content">

    <TextBox Text="This is the content of a TextBox." />
</Window>
```

Die folgende Abbildung zeigt das Ergebnis:

![Ein TextBox-Steuerelement, das Text enthält](media/introduction-to-wpf/wpfintrofigure21.png)

Andere Steuerelemente können dagegen mehrere Elemente verschiedener Inhaltstypen enthalten. Der Inhalt eines <xref:System.Windows.Controls.Button>-Steuerelements, der durch die <xref:System.Windows.Controls.ContentControl.Content%2A>-Eigenschaft angegeben ist, kann eine Vielzahl von Elementen enthalten, etwa Layoutsteuerelemente, Text, Bildern und Formen. Das folgende Beispiel zeigt eine <xref:System.Windows.Controls.Button> mit Inhalt, der,,, <xref:System.Windows.Controls.DockPanel> und enthält <xref:System.Windows.Controls.Label> <xref:System.Windows.Controls.Border> <xref:System.Windows.Controls.MediaElement> :

```xaml
<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    x:Class="SDKSample.ButtonContentWindow"
    Title="Button Content">

  <Button Margin="20">
    <!-- Button Content -->
    <DockPanel Width="200" Height="180">
      <Label DockPanel.Dock="Top" HorizontalAlignment="Center">Click Me!</Label>
      <Border Background="Black" BorderBrush="Yellow" BorderThickness="2"
        CornerRadius="2" Margin="5">
        <MediaElement Source="media/wpf.wmv" Stretch="Fill" />
      </Border>
    </DockPanel>
  </Button>
</Window>
```

Die folgende Abbildung zeigt den Inhalt dieser Schaltfläche:

![Eine Schaltfläche, die mehrere Inhaltstypen enthält](media/introduction-to-wpf/wpfintrofigure22.png)

Weitere Informationen zu den Arten von Inhalten, die von verschiedenen Steuerelementen unterstützt werden, finden Sie unter [WPF-Inhalts Modell](controls/wpf-content-model.md).

### <a name="triggers"></a>Auslöser

Obwohl der Hauptzweck von XAML-Markup in der Implementierung der Darstellung einer Anwendung besteht, lassen sich mit XAML auch einige Aspekte des Verhaltens einer Anwendung implementieren. Ein Beispiel ist die Verwendung von Triggern, um die Darstellung einer Anwendung anhand von Benutzeraktionen zu ändern. Weitere Informationen finden Sie unter [Stile und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview).

### <a name="control-templates"></a>Steuerelementvorlagen

Die standardmäßigen Benutzeroberflächen für WPF-Steuerelemente werden üblicherweise aus anderen Steuerelementen und Formen erstellt. Beispielsweise besteht ein <xref:System.Windows.Controls.Button> -Steuerelement aus einem <xref:Microsoft.Windows.Themes.ButtonChrome> - und einem <xref:System.Windows.Controls.ContentPresenter> -Steuerelement. Das <xref:Microsoft.Windows.Themes.ButtonChrome> -Steuerelement stellt die Standarddarstellung der Schaltfläche bereit, während das <xref:System.Windows.Controls.ContentPresenter> -Steuerelement den Inhalt der Schaltfläche anzeigt, der in der <xref:System.Windows.Controls.ContentControl.Content%2A> -Eigenschaft angegeben ist.

Manchmal passt die Standarddarstellung eines Steuerelements nicht zum Gesamterscheinungsbild einer Anwendung. In diesem Fall können Sie ein <xref:System.Windows.Controls.ControlTemplate> -Objekt verwenden, um die Darstellung der Benutzeroberfläche des Steuerelements anzupassen, ohne dessen Inhalt und Verhalten zu ändern.

Im folgenden Beispiel wird gezeigt, wie die Darstellung eines mit <xref:System.Windows.Controls.Button> einem geändert wird <xref:System.Windows.Controls.ControlTemplate> :

[!code-xaml[IntroToWPFSnippets#ButtonControlTemplateWindowMARKUP](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_16.xaml)]

[!code-csharp[IntroToWPFSnippets#ButtonControlTemplateWindowCODEBEHIND](~/samples/snippets/csharp/wpf/introduction-to-wpf/introduction-to-wpf_17.cs)]
[!code-vb[IntroToWPFSnippets#ButtonControlTemplateWindowCODEBEHIND](~/samples/snippets/visualbasic/wpf/introduction-to-wpf/introduction-to-wpf_17.vb)]

In diesem Beispiel wurde die Standardbenutzeroberfläche der Schaltfläche durch ein <xref:System.Windows.Shapes.Ellipse>-Steuerelement ersetzt, das einen dunkelblauem Rand hat und über ein <xref:System.Windows.Media.RadialGradientBrush>-Steuerelement gefüllt wird. Das <xref:System.Windows.Controls.ContentPresenter> -Steuerelement zeigt den Inhalt des <xref:System.Windows.Controls.Button>-Steuerelements an („Click Me!“). Wenn auf das <xref:System.Windows.Controls.Button> -Steuerelement geklickt wird, wird das <xref:System.Windows.Controls.Primitives.ButtonBase.Click> -Ereignis weiterhin als Teil des Standardverhaltens des <xref:System.Windows.Controls.Button> n-Steuerelements ausgelöst. Das Ergebnis ist in der folgenden Abbildung dargestellt:

![Eine elliptische Schaltfläche und ein zweites Fenster](media/introduction-to-wpf/wpfintrofigure2.png)

### <a name="data-templates"></a>Datenvorlagen

Während Sie mit einer Steuerelementvorlage die Darstellung eines Steuerelements angeben können, können Sie mit einer Datenvorlage die Darstellung des Inhalts eines Steuerelements angeben. Datenvorlagen werden häufig dazu verwendet, die Anzeige gebundener Daten zu verbessern. Die folgende Abbildung zeigt die Standarddarstellung für ein- <xref:System.Windows.Controls.ListBox> Objekt, das an eine Auflistung von-Objekten gebunden ist `Task` , wobei jede Aufgabe einen Namen, eine Beschreibung und eine Priorität hat:

![Ein Listenfeld mit der Standarddarstellung](media/introduction-to-wpf/wpfintrofigure18.png)

Die Standarddarstellung entspricht dem, was Sie von einem <xref:System.Windows.Controls.ListBox>-Steuerelement erwarten. Allerdings enthält die Standarddarstellung jeder Aufgabe nur den Aufgabennamen. Um den Aufgabennamen, die Beschreibung und die Priorität anzuzeigen, muss die Standarddarstellung der gebundenen Listenelemente des <xref:System.Windows.Controls.ListBox> -Steuerelements über ein <xref:System.Windows.DataTemplate>-Objekt geändert werden. Der folgende XAML-Code definiert eine solche <xref:System.Windows.DataTemplate> , die auf jede Aufgabe angewendet wird, indem das-Attribut verwendet wird <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A> :

```xaml
<Window
  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
  x:Class="SDKSample.DataTemplateWindow"
  Title="With a Data Template">
  <Window.Resources>
    <!-- Data Template (applied to each bound task item in the task collection) -->
    <DataTemplate x:Key="myTaskTemplate">
      <Border Name="border" BorderBrush="DarkSlateBlue" BorderThickness="2"
        CornerRadius="2" Padding="5" Margin="5">
        <Grid>
          <Grid.RowDefinitions>
            <RowDefinition/>
            <RowDefinition/>
            <RowDefinition/>
          </Grid.RowDefinitions>
          <Grid.ColumnDefinitions>
            <ColumnDefinition Width="Auto" />
            <ColumnDefinition />
          </Grid.ColumnDefinitions>
          <TextBlock Grid.Row="0" Grid.Column="0" Padding="0,0,5,0" Text="Task Name:"/>
          <TextBlock Grid.Row="0" Grid.Column="1" Text="{Binding Path=TaskName}"/>
          <TextBlock Grid.Row="1" Grid.Column="0" Padding="0,0,5,0" Text="Description:"/>
          <TextBlock Grid.Row="1" Grid.Column="1" Text="{Binding Path=Description}"/>
          <TextBlock Grid.Row="2" Grid.Column="0" Padding="0,0,5,0" Text="Priority:"/>
          <TextBlock Grid.Row="2" Grid.Column="1" Text="{Binding Path=Priority}"/>
        </Grid>
      </Border>
    </DataTemplate>
  </Window.Resources>

  <!-- UI -->
  <DockPanel>
    <!-- Title -->
    <Label DockPanel.Dock="Top" FontSize="18" Margin="5" Content="My Task List:"/>

    <!-- Data template is specified by the ItemTemplate attribute -->
    <ListBox
      ItemsSource="{Binding}"
      ItemTemplate="{StaticResource myTaskTemplate}"
      HorizontalContentAlignment="Stretch"
      IsSynchronizedWithCurrentItem="True"
      Margin="5,0,5,5" />

 </DockPanel>
</Window>
```

Die folgende Abbildung zeigt die Auswirkung dieses Codes:

![Listenfeld, das eine Datenvorlage verwendet](media/introduction-to-wpf/wpfintrofigure19.png)

Beachten Sie, dass das Verhalten und die Gesamtdarstellung des <xref:System.Windows.Controls.ListBox>-Steuerelements beibehalten wurden. Lediglich die Darstellung der vom Listenfeld angezeigten Inhalte wurde geändert.

Weitere Informationen finden Sie unter [Übersicht über Daten](data/data-templating-overview.md)Vorlagen.

### <a name="styles"></a>Stile

Stile ermöglichen Entwicklern und Designern die Standardisierung auf ein bestimmtes Erscheinungsbild ihres Produkts. WPF stellt ein solides Formatmodell bereit, dessen Grundlage das <xref:System.Windows.Style> -Element bildet. Im folgenden Beispiel wird ein Stil erstellt, mit dem die Hintergrundfarbe für jedes <xref:System.Windows.Controls.Button> in einem Fenster auf festgelegt wird `Orange` :

```xaml
<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    x:Class="SDKSample.StyleWindow"
    Title="Styles">
  <!-- Style that will be applied to all buttons -->
  <Style TargetType="{x:Type Button}">
    <Setter Property="Background" Value="Orange" />
    <Setter Property="BorderBrush" Value="Crimson" />
    <Setter Property="FontSize" Value="20" />
    <Setter Property="FontWeight" Value="Bold" />
    <Setter Property="Margin" Value="5" />
  </Style>
  <!-- This button will have the style applied to it -->
  <Button>Click Me!</Button>

  <!-- This label will not have the style applied to it -->
  <Label>Don't Click Me!</Label>

  <!-- This button will have the style applied to it -->
  <Button>Click Me!</Button>
</Window>
```

Da sich dieser Stil auf alle <xref:System.Windows.Controls.Button>-Steuerelemente bezieht, wird er automatisch auf alle Schaltflächen im Fenster angewendet. Dies ist in der folgenden Abbildung zu sehen:

![Zwei orangefarbene Schaltflächen](media/introduction-to-wpf/wpfintrofigure20.png)

Weitere Informationen finden Sie unter [Stile und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview).

### <a name="resources"></a>Ressourcen

Die Steuerelemente in einer Anwendung sollten die gleiche Darstellung haben, wozu alles von Schriftarten und Hintergrundfarben bis zu Steuerelementvorlagen, Datenvorlagen und Stilen gehören kann. Über die WPF-Unterstützung für Benutzeroberflächenressourcen können diese Ressourcen in einem einzigen Speicherort kapseln, um sie wiederzuverwenden.

Im folgenden Beispiel wird eine gemeinsame Hintergrundfarbe definiert, die von einem und einem gemeinsam verwendet wird <xref:System.Windows.Controls.Button> <xref:System.Windows.Controls.Label> :

```xaml
<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    x:Class="SDKSample.ResourcesWindow"
    Title="Resources Window">

  <!-- Define window-scoped background color resource -->
  <Window.Resources>
    <SolidColorBrush x:Key="defaultBackground" Color="Red" />
  </Window.Resources>

  <!-- Button background is defined by window-scoped resource -->
  <Button Background="{StaticResource defaultBackground}">One Button</Button>

  <!-- Label background is defined by window-scoped resource -->
  <Label Background="{StaticResource defaultBackground}">One Label</Label>
</Window>
```

In diesem Beispiel wird mit dem `Window.Resources` -Eigenschaftenelements eine Ressource für die Hintergrundfarbe implementiert. Diese Ressource ist für alle untergeordneten Elemente des <xref:System.Windows.Window>-Elements verfügbar. Es gibt eine Vielzahl von Ressourcenbereichen, von denen einige nachfolgend in der Reihenfolge aufgeführt sind, in der sie aufgelöst werden:

1. Ein einzelnes Steuerelement (über die geerbte <xref:System.Windows.FrameworkElement.Resources%2A?displayProperty=fullName> -Eigenschaft)

2. Ein <xref:System.Windows.Window> - oder <xref:System.Windows.Controls.Page> -Element (ebenfalls über die geerbte <xref:System.Windows.FrameworkElement.Resources%2A?displayProperty=fullName> -Eigenschaft)

3. Ein <xref:System.Windows.Application> -Element (über die <xref:System.Windows.Application.Resources%2A?displayProperty=fullName> -Eigenschaft)

Durch die Vielzahl von Bereichen erhalten Sie Flexibilität in Bezug auf die Art, mit der Sie Ihre Ressourcen definieren und freigeben.

Anstatt Ihre Ressourcen direkt mit einem bestimmten Bereich zu verknüpfen, können Sie eine oder mehrere Ressourcen über ein separates <xref:System.Windows.ResourceDictionary> -Element verpacken, auf das in anderen Teilen einer Anwendung verwiesen werden kann. Im folgenden Beispiel wird z. b. eine Standard Hintergrundfarbe in einem Ressourcen Wörterbuch definiert:

```xaml
<ResourceDictionary
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">

  <!-- Define background color resource -->
  <SolidColorBrush x:Key="defaultBackground" Color="Red" />

  <!-- Define other resources -->
</ResourceDictionary>
```

Im folgenden Beispiel wird auf das Ressourcen Wörterbuch verwiesen, das im vorherigen Beispiel definiert wurde, sodass es in einer Anwendung freigegeben ist:

```xaml
<Application
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    x:Class="SDKSample.App">

  <Application.Resources>
    <ResourceDictionary>
      <ResourceDictionary.MergedDictionaries>
        <ResourceDictionary Source="BackgroundColorResources.xaml"/>
      </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
  </Application.Resources>
</Application>
```

Ressourcen und Ressourcenwörterbücher bilden die Grundlage der WPF-Unterstützung für Designs und Skins.

Weitere Informationen finden Sie unter [Ressourcen](/dotnet/desktop-wpf/fundamentals/xaml-resources-define).

### <a name="custom-controls"></a>Benutzerdefinierte Steuerelemente

Obwohl WPF umfangreiche Unterstützung für Anpassungen bietet, kann es Fälle geben, in denen die vorhandenen WPF-Steuerelemente den Anforderungen Ihrer Anwendung oder denen der Benutzer nicht genügen. Dies kann auftreten, wenn Folgendes zutrifft:

- Die von Ihnen gewünschte Benutzeroberfläche kann nicht erstellt werden, indem das Aussehen und Verhalten vorhandener WPF-Implementierungen angepasst wird.

- Das von Ihnen gewünschte Verhalten wird von vorhandenen WPF-Implementierungen nicht (oder nicht einfach) unterstützt.

An diesem Punkt können Sie jedoch eines der drei WPF-Modelle nutzen, um ein neues Steuerelement zu erstellen. Jedes Modell ist für ein bestimmtes Szenario vorgesehen und erfordert, dass Ihr benutzerdefiniertes Steuerelement aus einer bestimmten WPF-Basisklasse abgeleitet wird. Die drei Modelle sind hier aufgeführt:

- **Benutzersteuerelementmodell** Ein benutzerdefiniertes Steuerelement wird aus <xref:System.Windows.Controls.UserControl> abgeleitet und besteht aus mindestens einem anderen Steuerelement.

- **Steuerelementmodell** Ein benutzerdefiniertes Steuerelement wird aus <xref:System.Windows.Controls.Control> abgeleitet und dazu verwendet, eine Implementierung zu erstellen, deren Verhalten mithilfe von Vorlagen von ihrer Darstellung getrennt wird, so wie beim Großteil der WPF-Steuerelemente. Durch Ableiten aus <xref:System.Windows.Controls.Control> erhalten Sie für ein Erstellen einer benutzerdefinierten Benutzeroberfläche mehr Freiheit als mit Benutzersteuerelementen, dies kann jedoch höheren Aufwand erfordern.

- **Frameworkelementmodell**. Ein benutzerdefiniertes Steuerelement wird aus <xref:System.Windows.FrameworkElement> abgeleitet, wenn seine Darstellung durch benutzerdefinierte Renderinglogik (nicht durch Vorlagen) definiert ist.

Das folgende Beispiel zeigt ein benutzerdefiniertes numerisches auf-/ab-Steuerelement, <xref:System.Windows.Controls.UserControl> das von abgeleitet wird

[!code-xaml[IntroToWPFSnippets#UserControlMARKUP](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_33.xaml)]

[!code-csharp[IntroToWPFSnippets#UserControlCODEBEHIND1](~/samples/snippets/csharp/wpf/introduction-to-wpf/introduction-to-wpf_34.cs)]
[!code-vb[IntroToWPFSnippets#UserControlCODEBEHIND1](~/samples/snippets/visualbasic/wpf/introduction-to-wpf/introduction-to-wpf_34.vb)]

Im folgenden Beispiel wird der XAML-Code veranschaulicht, der erforderlich ist, um das Benutzer Steuerelement in einen zu integrieren <xref:System.Windows.Window> :

[!code-xaml[IntroToWPFSnippets#UserControlWindowMARKUP1](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_37.xaml)]

Die folgende Abbildung zeigt das-Steuerelement, das `NumericUpDown` in einem gehostet wird <xref:System.Windows.Window> :

![Ein benutzerdefiniertes UserControl](media/introduction-to-wpf/wpfintrofigure3.png)

Weitere Informationen zu benutzerdefinierten Steuerelementen finden Sie unter [Übersicht über das Erstellen von Steuer](controls/control-authoring-overview.md)Elementen.

## <a name="wpf-best-practices"></a>Bewährte Methoden für WPF

Wie bei jeder Entwicklungsplattform kann das gewünschte Ergebnis mit WPF auf verschiedene Arten erreicht werden. Um sichergehen zu können, dass Ihre WPF-Anwendungen die geforderte Benutzerfreundlichkeit bereitstellen und grundsätzlich den Ansprüche der Zielgruppe entsprechen, gibt es empfohlene bewährte Methoden in Bezug auf Barrierefreiheit, Globalisierung, Lokalisierung und Leistung. Weitere Informationen finden Sie unter

- [Bedienungshilfen](/dotnet/framework/ui-automation/accessibility-best-practices)
- [Übersicht über WPF-Globalisierung und -Lokalisierung](advanced/wpf-globalization-and-localization-overview.md)
- [Optimieren der WPF-Anwendungsleistung](advanced/optimizing-wpf-application-performance.md)
- [WPF-Sicherheit](security-wpf.md)

## <a name="next-steps"></a>Nächste Schritte

In diesem Artikel wurden die Schlüsselfeatures von WPF erläutert. Jetzt können Sie Ihre erste WPF-App erstellen.

> [!div class="nextstepaction"]
> [Exemplarische Vorgehensweise: Meine erste WPF-Desktopanwendung](getting-started/walkthrough-my-first-wpf-desktop-application.md)

## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit WPF](getting-started/index.md)
- [Windows Presentation Foundation](index.md)
- [Ressourcen für die WPF-Community](getting-started/community-feedback.md)
