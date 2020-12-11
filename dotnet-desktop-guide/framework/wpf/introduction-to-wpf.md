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
# <a name="wpf-overview"></a><span data-ttu-id="3cfb7-104">WPF-Übersicht</span><span class="sxs-lookup"><span data-stu-id="3cfb7-104">WPF overview</span></span>

<span data-ttu-id="3cfb7-105">Mit Windows Presentation Foundation (WPF) können Sie Desktop-Clientanwendungen für Windows erstellen, die visuell herausragende Benutzeroberflächen haben.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-105">Windows Presentation Foundation (WPF) lets you create desktop client applications for Windows with visually stunning user experiences.</span></span>

![Contoso Healthcare-Beispiel](media/introduction-to-wpf/wpfintrofigure24.png)

<span data-ttu-id="3cfb7-107">Der Kern von WPF ist eine auflösungsunabhängige und vektorbasierte Rendering-Engine, die die Leistungsfähigkeit moderner Grafikhardware nutzt.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-107">The core of WPF is a resolution-independent and vector-based rendering engine that is built to take advantage of modern graphics hardware.</span></span> <span data-ttu-id="3cfb7-108">Dieser Kern wird durch WPF um mehrere Anwendungsentwicklungsfeatures erweitert, wozu Extensible Application Markup Language (XAML), Steuerelemente, Datenbindung, Layout, 2D- und 3D-Grafik, Animationen, Stile, Vorlagen, Dokumente, Medien, Text und Typographie zählen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-108">WPF extends the core with a comprehensive set of application-development features that include Extensible Application Markup Language (XAML), controls, data binding, layout, 2D and 3D graphics, animation, styles, templates, documents, media, text, and typography.</span></span> <span data-ttu-id="3cfb7-109">WPF ist Teil von .NET. Sie können also Anwendungen erstellen, die andere Elemente der .NET-API beinhalten.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-109">WPF is part of .NET, so you can build applications that incorporate other elements of the .NET API.</span></span>

<span data-ttu-id="3cfb7-110">Diese Übersicht ist für Einsteiger gedacht und beschreibt die wichtigsten Funktionen und Konzepte von WPF.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-110">This overview is intended for newcomers and covers the key capabilities and concepts of WPF.</span></span>

## <a name="program-with-wpf"></a><span data-ttu-id="3cfb7-111">Programmieren mit WPF</span><span class="sxs-lookup"><span data-stu-id="3cfb7-111">Program with WPF</span></span>

<span data-ttu-id="3cfb7-112">WPF ist eine Teilmenge von .NET-Typen, die sich (zum größten Teil) im <xref:System.Windows>-Namespace befinden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-112">WPF exists as a subset of .NET types that are (for the most part) located in the <xref:System.Windows> namespace.</span></span> <span data-ttu-id="3cfb7-113">Wenn Sie bereits Anwendungen mit .NET und verwalteten Technologien wie ASP.NET und Windows Forms erstellt haben, sind Sie mit den Grundlagen der WPF-Programmierung vertraut. Sie instanziieren Klassen, legen Eigenschaften fest, rufen Methoden auf und behandeln Ereignisse und verwenden dafür Ihre bevorzugte .NET Framework-Programmiersprache, etwa C# oder Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-113">If you have previously built applications with .NET using managed technologies like ASP.NET and Windows Forms, the fundamental WPF programming experience should be familiar; you instantiate classes, set properties, call methods, and handle events, using your favorite .NET programming language, such as C# or Visual Basic.</span></span>

<span data-ttu-id="3cfb7-114">WPF umfasst zusätzliche Programmierkonstrukte, mit denen Eigenschaften und Ereignisse erweitert werden: [Abhängigkeitseigenschaften](advanced/dependency-properties-overview.md) und [Routingereignisse](advanced/routed-events-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-114">WPF includes additional programming constructs that enhance properties and events: [dependency properties](advanced/dependency-properties-overview.md) and [routed events](advanced/routed-events-overview.md).</span></span>

## <a name="markup-and-code-behind"></a><span data-ttu-id="3cfb7-115">Markup und CodeBehind</span><span class="sxs-lookup"><span data-stu-id="3cfb7-115">Markup and code-behind</span></span>

<span data-ttu-id="3cfb7-116">WPF ermöglicht es Ihnen, eine Anwendung sowohl mit *Markup* als auch mit *CodeBehind* zu entwickeln, eine Vorgehensweise, mit der ASP.NET-Entwickler vertraut sein sollten.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-116">WPF lets you develop an application using both *markup* and *code-behind*, an experience with which ASP.NET developers should be familiar.</span></span> <span data-ttu-id="3cfb7-117">Im Grundsatz verwenden Sie XAML-Markup, um die Darstellung einer Anwendung zu implementieren, und verwaltete Programmiersprachen (CodeBehind), um das Verhalten der Anwendung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-117">You generally use XAML markup to implement the appearance of an application while using managed programming languages (code-behind) to implement its behavior.</span></span> <span data-ttu-id="3cfb7-118">Diese Trennung von Darstellung und Verhalten bietet folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-118">This separation of appearance and behavior has the following benefits:</span></span>

- <span data-ttu-id="3cfb7-119">Entwicklungs- und Wartungskosten werden verringert, weil darstellungsspezifisches Markup nicht unmittelbar mit verhaltensspezifischem Code gekoppelt ist.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-119">Development and maintenance costs are reduced because appearance-specific markup is not tightly coupled with behavior-specific code.</span></span>

- <span data-ttu-id="3cfb7-120">Die Entwicklung ist effizienter, da Designer die Darstellung einer Anwendung implementieren können, während Entwickler gleichzeitig das Verhalten der Anwendung implementieren.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-120">Development is more efficient because designers can implement an application's appearance simultaneously with developers who are implementing the application's behavior.</span></span>

- <span data-ttu-id="3cfb7-121">Die[Globalisierung und Lokalisierung](advanced/wpf-globalization-and-localization-overview.md) für WPF-Anwendungen wird stark vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-121">[Globalization and localization](advanced/wpf-globalization-and-localization-overview.md) for WPF applications is simplified.</span></span>

### <a name="markup"></a><span data-ttu-id="3cfb7-122">Markup</span><span class="sxs-lookup"><span data-stu-id="3cfb7-122">Markup</span></span>

<span data-ttu-id="3cfb7-123">XAML ist eine auf XML basierende Markupsprache, mit der die Darstellung einer Anwendung deklarativ implementiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-123">XAML is an XML-based markup language that implements an application's appearance declaratively.</span></span> <span data-ttu-id="3cfb7-124">Sie wird üblicherweise dazu verwendet, Fenster, Dialogfelder, Seiten und Benutzersteuerelemente zu erstellen und diese mit Steuerelementen, Formen und Grafiken zu füllen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-124">You typically use it to create windows, dialog boxes, pages, and user controls, and to fill them with controls, shapes, and graphics.</span></span>

<span data-ttu-id="3cfb7-125">Im folgenden Beispiel wird XAML verwendet, um die Darstellung eines Fensters zu implementieren, das eine einzelne Schaltfläche enthält:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-125">The following example uses XAML to implement the appearance of a window that contains a single button:</span></span>

```xaml
<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    Title="Window with Button"
    Width="250" Height="100">

  <!-- Add button to window -->
  <Button Name="button">Click Me!</Button>

</Window>
```

<span data-ttu-id="3cfb7-126">In diesem XAML-Code werden ein Fenster und eine Schaltfläche definiert, indem das `Window` - und das `Button` -Element verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-126">Specifically, this XAML defines a window and a button by using the `Window` and `Button` elements, respectively.</span></span> <span data-ttu-id="3cfb7-127">Jedes Element wird mit Attributen konfiguriert. Hier wird beispielsweise das `Window` -Attribut des `Title` -Elements verwendet, um den Text für die Titelleiste des Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-127">Each element is configured with attributes, such as the `Window` element's `Title` attribute to specify the window's title-bar text.</span></span> <span data-ttu-id="3cfb7-128">Zur Laufzeit werden die im Markup definierten Elemente und Attribute von WPF in Instanzen von WPF-Klassen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-128">At run time, WPF converts the elements and attributes that are defined in markup to instances of WPF classes.</span></span> <span data-ttu-id="3cfb7-129">Beispielsweise wird das `Window` -Element in eine Instanz der <xref:System.Windows.Window> -Klasse konvertiert, deren <xref:System.Windows.Window.Title%2A> -Eigenschaft dem Wert des `Title` -Attributs entspricht.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-129">For example, the `Window` element is converted to an instance of the <xref:System.Windows.Window> class whose <xref:System.Windows.Window.Title%2A> property is the value of the `Title` attribute.</span></span>

<span data-ttu-id="3cfb7-130">Die folgende Abbildung zeigt die Benutzeroberfläche (UI), die vom XAML-Code im vorherigen Beispiel definiert wurde:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-130">The following figure shows the user interface (UI) that is defined by the XAML in the previous example:</span></span>

![Ein Fenster, das eine Schaltfläche enthält](media/introduction-to-wpf/wpfintrofigure10.png)

<span data-ttu-id="3cfb7-132">Da XAML auf XML basiert, wird die damit erstellte Benutzeroberfläche in einer Hierarchie geschachtelter Elemente zusammengestellt, die als [Elementstruktur](advanced/trees-in-wpf.md)bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-132">Since XAML is XML-based, the UI that you compose with it is assembled in a hierarchy of nested elements known as an [element tree](advanced/trees-in-wpf.md).</span></span> <span data-ttu-id="3cfb7-133">Die Elementstruktur stellt eine logische und intuitive Art und Weise zum Erstellen und Verwalten von Benutzeroberflächen bereit.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-133">The element tree provides a logical and intuitive way to create and manage UIs.</span></span>

### <a name="code-behind"></a><span data-ttu-id="3cfb7-134">CodeBehind</span><span class="sxs-lookup"><span data-stu-id="3cfb7-134">Code-behind</span></span>

<span data-ttu-id="3cfb7-135">Der Hauptzweck einer Anwendung besteht darin, die Funktionalität zu implementieren, mit der auf Benutzeraktionen reagiert wird, wozu auch das Behandeln von Ereignissen (z. B. Klicken auf Menüs, Symbolleisten oder Schaltflächen) sowie das Aufrufen von Geschäftslogik und als Reaktion darauf von Datenzugriffslogik zählen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-135">The main behavior of an application is to implement the functionality that responds to user interactions, including handling events (for example, clicking a menu, tool bar, or button) and calling business logic and data access logic in response.</span></span> <span data-ttu-id="3cfb7-136">In WPF wird dieses Verhalten in Code implementiert, der mit Markup verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-136">In WPF, this behavior is implemented in code that is associated with markup.</span></span> <span data-ttu-id="3cfb7-137">Diese Art von Code wird als CodeBehind bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-137">This type of code is known as code-behind.</span></span> <span data-ttu-id="3cfb7-138">Das folgende Beispiel zeigt das aktualisierte Markup aus dem vorherigen Beispiel und den Code-Behind:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-138">The following example shows the updated markup from the previous example and the code-behind:</span></span>

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

<span data-ttu-id="3cfb7-139">In diesem Beispiel wird im CodeBehind eine Klasse implementiert, die aus der <xref:System.Windows.Window> -Klasse abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-139">In this example, the code-behind implements a class that derives from the <xref:System.Windows.Window> class.</span></span> <span data-ttu-id="3cfb7-140">Das `x:Class` -Attribut wird verwendet, um den Markupcode mit der CodeBehind-Klasse zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-140">The `x:Class` attribute is used to associate the markup with the code-behind class.</span></span> <span data-ttu-id="3cfb7-141">`InitializeComponent` wird vom Konstruktor der CodeBehind-Klasse aufgerufen, um die im Markup definierte Benutzeroberfläche mit der CodeBehind-Klasse zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-141">`InitializeComponent` is called from the code-behind class's constructor to merge the UI that is defined in markup with the code-behind class.</span></span> <span data-ttu-id="3cfb7-142">( `InitializeComponent` wird für Sie generiert, wenn Ihre Anwendung erstellt wird. aus diesem Grund müssen Sie Sie nicht manuell implementieren.) Durch die Kombination von `x:Class` und `InitializeComponent` wird sichergestellt, dass die Implementierung bei jeder Erstellung ordnungsgemäß initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-142">(`InitializeComponent` is generated for you when your application is built, which is why you don't need to implement it manually.) The combination of `x:Class` and `InitializeComponent` ensure that your implementation is correctly initialized whenever it is created.</span></span> <span data-ttu-id="3cfb7-143">In der CodeBehind-Klasse wird außerdem ein Ereignishandler für das <xref:System.Windows.Controls.Primitives.ButtonBase.Click>-Ereignis der Schaltfläche implementiert.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-143">The code-behind class also implements an event handler for the button's <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event.</span></span> <span data-ttu-id="3cfb7-144">Wird auf die Schaltfläche geklickt, zeigt der Ereignishandler ein Meldungsfeld an, indem er die <xref:System.Windows.MessageBox.Show%2A?displayProperty=fullName> -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-144">When the button is clicked, the event handler shows a message box by calling the <xref:System.Windows.MessageBox.Show%2A?displayProperty=fullName> method.</span></span>

<span data-ttu-id="3cfb7-145">In der folgenden Abbildung wird das Ergebnis angezeigt, wenn auf die Schaltfläche geklickt wird:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-145">The following figure shows the result when the button is clicked:</span></span>

![Eine MessageBox](media/introduction-to-wpf/wpfintrofigure25.png)

## <a name="controls"></a><span data-ttu-id="3cfb7-147">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3cfb7-147">Controls</span></span>

<span data-ttu-id="3cfb7-148">Die Elemente einer Benutzeroberfläche, die mit dem Anwendungsmodell bereitgestellt werden, sind konstruierte Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-148">The user experiences that are delivered by the application model are constructed controls.</span></span> <span data-ttu-id="3cfb7-149">In WPF ist *Steuerelement* ein Sammelbegriff, der sich auf eine Kategorie von WPF-Klassen bezieht, die entweder in einem Fenster oder auf einer Seite gehostet werden, eine Benutzeroberfläche haben und ein bestimmtes Verhalten implementieren.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-149">In WPF, *control* is an umbrella term that applies to a category of WPF classes that are hosted in either a window or a page, have a user interface, and implement some behavior.</span></span>

<span data-ttu-id="3cfb7-150">Weitere Informationen finden Sie unter Steuer [Elemente](controls/index.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-150">For more information, see [Controls](controls/index.md).</span></span>

### <a name="wpf-controls-by-function"></a><span data-ttu-id="3cfb7-151">WPF-Steuerelemente nach Funktion</span><span class="sxs-lookup"><span data-stu-id="3cfb7-151">WPF controls by function</span></span>

<span data-ttu-id="3cfb7-152">Die integrierten WPF-Steuerelemente sind hier aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-152">The built-in WPF controls are listed here:</span></span>

- <span data-ttu-id="3cfb7-153">**Schalt** Flächen: <xref:System.Windows.Controls.Button> und <xref:System.Windows.Controls.Primitives.RepeatButton> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-153">**Buttons**: <xref:System.Windows.Controls.Button> and <xref:System.Windows.Controls.Primitives.RepeatButton>.</span></span>

- <span data-ttu-id="3cfb7-154">**Datenanzeige**: <xref:System.Windows.Controls.DataGrid> , <xref:System.Windows.Controls.ListView> und <xref:System.Windows.Controls.TreeView> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-154">**Data Display**: <xref:System.Windows.Controls.DataGrid>, <xref:System.Windows.Controls.ListView>, and <xref:System.Windows.Controls.TreeView>.</span></span>

- <span data-ttu-id="3cfb7-155">**Datumsanzeige und-Auswahl**: <xref:System.Windows.Controls.Calendar> und <xref:System.Windows.Controls.DatePicker> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-155">**Date Display and Selection**: <xref:System.Windows.Controls.Calendar> and <xref:System.Windows.Controls.DatePicker>.</span></span>

- <span data-ttu-id="3cfb7-156">**Dialog Felder**: <xref:Microsoft.Win32.OpenFileDialog> , <xref:System.Windows.Controls.PrintDialog> und <xref:Microsoft.Win32.SaveFileDialog> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-156">**Dialog Boxes**: <xref:Microsoft.Win32.OpenFileDialog>, <xref:System.Windows.Controls.PrintDialog>, and <xref:Microsoft.Win32.SaveFileDialog>.</span></span>

- <span data-ttu-id="3cfb7-157">**Digitales** frei Hand Eingaben: <xref:System.Windows.Controls.InkCanvas> und <xref:System.Windows.Controls.InkPresenter> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-157">**Digital Ink**: <xref:System.Windows.Controls.InkCanvas> and <xref:System.Windows.Controls.InkPresenter>.</span></span>

- <span data-ttu-id="3cfb7-158">**Dokumente**: <xref:System.Windows.Controls.DocumentViewer> , <xref:System.Windows.Controls.FlowDocumentPageViewer> , <xref:System.Windows.Controls.FlowDocumentReader> , <xref:System.Windows.Controls.FlowDocumentScrollViewer> und <xref:System.Windows.Controls.StickyNoteControl> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-158">**Documents**: <xref:System.Windows.Controls.DocumentViewer>, <xref:System.Windows.Controls.FlowDocumentPageViewer>, <xref:System.Windows.Controls.FlowDocumentReader>, <xref:System.Windows.Controls.FlowDocumentScrollViewer>, and <xref:System.Windows.Controls.StickyNoteControl>.</span></span>

- <span data-ttu-id="3cfb7-159">**Eingabe**: <xref:System.Windows.Controls.TextBox> , <xref:System.Windows.Controls.RichTextBox> und <xref:System.Windows.Controls.PasswordBox> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-159">**Input**: <xref:System.Windows.Controls.TextBox>, <xref:System.Windows.Controls.RichTextBox>, and <xref:System.Windows.Controls.PasswordBox>.</span></span>

- <span data-ttu-id="3cfb7-160">**Layout**: <xref:System.Windows.Controls.Border> , <xref:System.Windows.Controls.Primitives.BulletDecorator> , <xref:System.Windows.Controls.Canvas> , <xref:System.Windows.Controls.DockPanel> , <xref:System.Windows.Controls.Expander> , <xref:System.Windows.Controls.Grid> , <xref:System.Windows.Controls.GridView> , <xref:System.Windows.Controls.GridSplitter> , <xref:System.Windows.Controls.GroupBox> , <xref:System.Windows.Controls.Panel> , <xref:System.Windows.Controls.Primitives.ResizeGrip> , <xref:System.Windows.Controls.Separator> , <xref:System.Windows.Controls.Primitives.ScrollBar> , <xref:System.Windows.Controls.ScrollViewer> , <xref:System.Windows.Controls.StackPanel> , <xref:System.Windows.Controls.Primitives.Thumb> , <xref:System.Windows.Controls.Viewbox> , <xref:System.Windows.Controls.VirtualizingStackPanel> , <xref:System.Windows.Window> und <xref:System.Windows.Controls.WrapPanel> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-160">**Layout**: <xref:System.Windows.Controls.Border>, <xref:System.Windows.Controls.Primitives.BulletDecorator>, <xref:System.Windows.Controls.Canvas>, <xref:System.Windows.Controls.DockPanel>, <xref:System.Windows.Controls.Expander>, <xref:System.Windows.Controls.Grid>, <xref:System.Windows.Controls.GridView>, <xref:System.Windows.Controls.GridSplitter>, <xref:System.Windows.Controls.GroupBox>, <xref:System.Windows.Controls.Panel>, <xref:System.Windows.Controls.Primitives.ResizeGrip>, <xref:System.Windows.Controls.Separator>, <xref:System.Windows.Controls.Primitives.ScrollBar>, <xref:System.Windows.Controls.ScrollViewer>, <xref:System.Windows.Controls.StackPanel>, <xref:System.Windows.Controls.Primitives.Thumb>, <xref:System.Windows.Controls.Viewbox>, <xref:System.Windows.Controls.VirtualizingStackPanel>, <xref:System.Windows.Window>, and <xref:System.Windows.Controls.WrapPanel>.</span></span>

- <span data-ttu-id="3cfb7-161">**Medien**: <xref:System.Windows.Controls.Image> , <xref:System.Windows.Controls.MediaElement> und <xref:System.Windows.Controls.SoundPlayerAction> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-161">**Media**: <xref:System.Windows.Controls.Image>, <xref:System.Windows.Controls.MediaElement>, and <xref:System.Windows.Controls.SoundPlayerAction>.</span></span>

- <span data-ttu-id="3cfb7-162">**Menüs**: <xref:System.Windows.Controls.ContextMenu> , <xref:System.Windows.Controls.Menu> und <xref:System.Windows.Controls.ToolBar> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-162">**Menus**: <xref:System.Windows.Controls.ContextMenu>, <xref:System.Windows.Controls.Menu>, and <xref:System.Windows.Controls.ToolBar>.</span></span>

- <span data-ttu-id="3cfb7-163">**Navigation**: <xref:System.Windows.Controls.Frame> , <xref:System.Windows.Documents.Hyperlink> , <xref:System.Windows.Controls.Page> , <xref:System.Windows.Navigation.NavigationWindow> und <xref:System.Windows.Controls.TabControl> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-163">**Navigation**: <xref:System.Windows.Controls.Frame>, <xref:System.Windows.Documents.Hyperlink>, <xref:System.Windows.Controls.Page>, <xref:System.Windows.Navigation.NavigationWindow>, and <xref:System.Windows.Controls.TabControl>.</span></span>

- <span data-ttu-id="3cfb7-164">**Auswahl**: <xref:System.Windows.Controls.CheckBox> , <xref:System.Windows.Controls.ComboBox> , <xref:System.Windows.Controls.ListBox> , <xref:System.Windows.Controls.RadioButton> und <xref:System.Windows.Controls.Slider> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-164">**Selection**: <xref:System.Windows.Controls.CheckBox>, <xref:System.Windows.Controls.ComboBox>, <xref:System.Windows.Controls.ListBox>, <xref:System.Windows.Controls.RadioButton>, and <xref:System.Windows.Controls.Slider>.</span></span>

- <span data-ttu-id="3cfb7-165">**Benutzerinformationen**: <xref:System.Windows.Controls.AccessText> , <xref:System.Windows.Controls.Label> , <xref:System.Windows.Controls.Primitives.Popup> , <xref:System.Windows.Controls.ProgressBar> , <xref:System.Windows.Controls.Primitives.StatusBar> , <xref:System.Windows.Controls.TextBlock> und <xref:System.Windows.Controls.ToolTip> .</span><span class="sxs-lookup"><span data-stu-id="3cfb7-165">**User Information**: <xref:System.Windows.Controls.AccessText>, <xref:System.Windows.Controls.Label>, <xref:System.Windows.Controls.Primitives.Popup>, <xref:System.Windows.Controls.ProgressBar>, <xref:System.Windows.Controls.Primitives.StatusBar>, <xref:System.Windows.Controls.TextBlock>, and <xref:System.Windows.Controls.ToolTip>.</span></span>

## <a name="input-and-commands"></a><span data-ttu-id="3cfb7-166">Eingabe und Befehle</span><span class="sxs-lookup"><span data-stu-id="3cfb7-166">Input and commands</span></span>

<span data-ttu-id="3cfb7-167">Steuerelemente sind üblicherweise dafür vorgesehen, Benutzereingaben zu erkennen und darauf zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-167">Controls most often detect and respond to user input.</span></span> <span data-ttu-id="3cfb7-168">Im [WPF-Eingabesystem](advanced/input-overview.md) werden sowohl direkte Ereignisse als auch Routingereignisse verwendet, um Texteingaben, Fokusverwaltung und Mauspositionierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-168">The [WPF input system](advanced/input-overview.md) uses both direct and routed events to support text input, focus management, and mouse positioning.</span></span>

<span data-ttu-id="3cfb7-169">Anwendungen haben häufig komplexe Eingabeanforderungen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-169">Applications often have complex input requirements.</span></span> <span data-ttu-id="3cfb7-170">WPF stellt ein [Befehlssystem](advanced/commanding-overview.md) bereit, über das Eingabeaktionen eines Benutzers von dem Code getrennt sind, mit dem auf diese Aktionen reagiert wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-170">WPF provides a [command system](advanced/commanding-overview.md) that separates user-input actions from the code that responds to those actions.</span></span>

## <a name="layout"></a><span data-ttu-id="3cfb7-171">Layout</span><span class="sxs-lookup"><span data-stu-id="3cfb7-171">Layout</span></span>

<span data-ttu-id="3cfb7-172">Wenn Sie eine Benutzeroberfläche erstellen, ordnen Sie die Steuerelemente nach Position und Größe an, um ein Layout zu formen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-172">When you create a user interface, you arrange your controls by location and size to form a layout.</span></span> <span data-ttu-id="3cfb7-173">Eine Hauptanforderung für jedes Layout besteht darin, sich an Änderungen der Fenstergröße und Anzeigeeinstellungen anpassen zu können.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-173">A key requirement of any layout is to adapt to changes in window size and display settings.</span></span> <span data-ttu-id="3cfb7-174">WPF bietet ein erstklassiges erweiterbares Layoutsystem, sodass Sie keinen zusätzlichen Code schreiben müssen, um ein Layout in diesen Fällen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-174">Rather than forcing you to write the code to adapt a layout in these circumstances, WPF provides a first-class, extensible layout system for you.</span></span>

<span data-ttu-id="3cfb7-175">Die Basis des Layoutsystems ist relative Positionierung, wodurch die Fähigkeit zur Anpassung an geänderte Fenster- und Anzeigebedingungen verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-175">The cornerstone of the layout system is relative positioning, which increases the ability to adapt to changing window and display conditions.</span></span> <span data-ttu-id="3cfb7-176">Das Layoutsystem verwaltet außerdem die Aushandlung zwischen Steuerelementen, um das Layout zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-176">In addition, the layout system manages the negotiation between controls to determine the layout.</span></span> <span data-ttu-id="3cfb7-177">Die Aushandlung ist ein zweistufiger Vorgang: Zuerst teilt ein Steuerelement seinem übergeordneten Element mit, welche Position und Größe es benötigt, und anschließend teilt das übergeordnete Element dem Steuerelement mit, welcher Raum ihm zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-177">The negotiation is a two-step process: first, a control tells its parent what location and size it requires; second, the parent tells the control what space it can have.</span></span>

<span data-ttu-id="3cfb7-178">Das Layoutsystem wird untergeordneten Steuerelementen über WPF-Basisklassen verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-178">The layout system is exposed to child controls through base WPF classes.</span></span> <span data-ttu-id="3cfb7-179">Für allgemeine Layouts wie Raster, Stapeln und Andocken enthält WPF mehrere Layoutsteuerelemente:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-179">For common layouts such as grids, stacking, and docking, WPF includes several layout controls:</span></span>

- <span data-ttu-id="3cfb7-180"><xref:System.Windows.Controls.Canvas>: Untergeordnete Steuerelemente stellen ihr eigenes Layout bereit.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-180"><xref:System.Windows.Controls.Canvas>: Child controls provide their own layout.</span></span>

- <span data-ttu-id="3cfb7-181"><xref:System.Windows.Controls.DockPanel>: Untergeordnete Steuerelemente werden an den Rändern des Bereichs ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-181"><xref:System.Windows.Controls.DockPanel>: Child controls are aligned to the edges of the panel.</span></span>

- <span data-ttu-id="3cfb7-182"><xref:System.Windows.Controls.Grid>: Untergeordnete Steuerelemente werden anhand von Zeilen und Spalten positioniert.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-182"><xref:System.Windows.Controls.Grid>: Child controls are positioned by rows and columns.</span></span>

- <span data-ttu-id="3cfb7-183"><xref:System.Windows.Controls.StackPanel>: Untergeordnete Steuerelemente werden entweder vertikal oder horizontal gestapelt.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-183"><xref:System.Windows.Controls.StackPanel>: Child controls are stacked either vertically or horizontally.</span></span>

- <span data-ttu-id="3cfb7-184"><xref:System.Windows.Controls.VirtualizingStackPanel>: Untergeordnete Steuerelemente werden virtualisiert und auf einer einzelnen Linie angeordnet, die horizontal oder vertikal verläuft.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-184"><xref:System.Windows.Controls.VirtualizingStackPanel>: Child controls are virtualized and arranged on a single line that is either horizontally or vertically oriented.</span></span>

- <span data-ttu-id="3cfb7-185"><xref:System.Windows.Controls.WrapPanel>: Untergeordnete Steuerelemente werden der Reihe nach von links nach rechts angeordnet und, wenn sich in der jeweiligen Zeile mehr Steuerelemente befinden, als der Platz zulässt, ggf. auf die nächste Zeile umbrochen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-185"><xref:System.Windows.Controls.WrapPanel>: Child controls are positioned in left-to-right order and wrapped to the next line when there are more controls on the current line than space allows.</span></span>

<span data-ttu-id="3cfb7-186">Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Controls.DockPanel> , um mehrere Steuerelemente zu bilden <xref:System.Windows.Controls.TextBox> :</span><span class="sxs-lookup"><span data-stu-id="3cfb7-186">The following example uses a <xref:System.Windows.Controls.DockPanel> to lay out several <xref:System.Windows.Controls.TextBox> controls:</span></span>

[!code-xaml[IntroToWPFSnippets#LayoutMARKUP](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_1.xaml)]

<span data-ttu-id="3cfb7-187">Das <xref:System.Windows.Controls.DockPanel>-Objekt ermöglicht es den untergeordneten <xref:System.Windows.Controls.TextBox>-Steuerelementen, ihm Informationen über ihre Anordnung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-187">The <xref:System.Windows.Controls.DockPanel> allows the child <xref:System.Windows.Controls.TextBox> controls to tell it how to arrange them.</span></span> <span data-ttu-id="3cfb7-188">Dazu wird von der <xref:System.Windows.Controls.DockPanel>-Klasse die angehängte `Dock`-Eigenschaft implementiert, die für die untergeordneten Steuerelemente verfügbar gemacht wird, damit jedes von ihnen eine Andockart festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-188">To do this, the <xref:System.Windows.Controls.DockPanel> implements a `Dock` attached property that is exposed to the child controls to allow each of them to specify a dock style.</span></span>

> [!NOTE]
> <span data-ttu-id="3cfb7-189">Eine Eigenschaft, die von einem übergeordneten Steuerelement zur Verwendung durch untergeordnete Steuerelemente implementiert wird, ist ein WPF-Konstrukt, das als [angefügte Eigenschaft](advanced/attached-properties-overview.md) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-189">A property that's implemented by a parent control for use by child controls is a WPF construct called an [attached property](advanced/attached-properties-overview.md).</span></span>

<span data-ttu-id="3cfb7-190">In der folgenden Abbildung wird das Ergebnis des XAML-Markups im vorherigen Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-190">The following figure shows the result of the XAML markup in the preceding example:</span></span>

![DockPanel-Seite](media/introduction-to-wpf/wpfintrofigure11.png)

## <a name="data-binding"></a><span data-ttu-id="3cfb7-192">Datenbindung</span><span class="sxs-lookup"><span data-stu-id="3cfb7-192">Data binding</span></span>

<span data-ttu-id="3cfb7-193">Die meisten Anwendungen werden erstellt, um Benutzern die Möglichkeit zum Anzeigen und Bearbeiten von Daten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-193">Most applications are created to provide users with the means to view and edit data.</span></span> <span data-ttu-id="3cfb7-194">Bei WPF-Anwendungen wird die Arbeit zum Speichern und Zugreifen auf Daten von Technologien wie Microsoft SQL Server und ADO.NET übernommen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-194">For WPF applications, the work of storing and accessing data is already provided for by technologies such as SQL Server and ADO .NET.</span></span> <span data-ttu-id="3cfb7-195">Nachdem auf die Daten zugegriffen wurde und diese in die verwalteten Objekte einer Anwendung geladen wurden, beginnt die harte Arbeit für WPF-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-195">After the data is accessed and loaded into an application's managed objects, the hard work for WPF applications begins.</span></span> <span data-ttu-id="3cfb7-196">Dies umfasst im Wesentlichen zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-196">Essentially, this involves two things:</span></span>

1. <span data-ttu-id="3cfb7-197">Kopieren der Daten aus den verwalteten Objekten in Steuerelemente, wo die Daten angezeigt und bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-197">Copying the data from the managed objects into controls, where the data can be displayed and edited.</span></span>

2. <span data-ttu-id="3cfb7-198">Sicherstellen, dass Änderungen, die über Steuerelemente an den Daten vorgenommen wurden, in die verwalteten Objekte kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-198">Ensuring that changes made to data by using controls are copied back to the managed objects.</span></span>

<span data-ttu-id="3cfb7-199">Um die Entwicklung von Anwendungen zu vereinfachen, stellt WPF eine Datenbindungs-Engine bereit, mit dem diese Schritte automatisch ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-199">To simplify application development, WPF provides a data binding engine to automatically perform these steps.</span></span> <span data-ttu-id="3cfb7-200">Das Kernelement der Datenbindungs-Engine ist die <xref:System.Windows.Data.Binding> , deren Aufgabe es ist, ein Steuerelement (das Bindungsziel) an ein Datenobjekt (die Bindungsquelle) zu binden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-200">The core unit of the data binding engine is the <xref:System.Windows.Data.Binding> class, whose job is to bind a control (the binding target) to a data object (the binding source).</span></span> <span data-ttu-id="3cfb7-201">Diese Beziehung wird in der folgenden Abbildung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-201">This relationship is illustrated by the following figure:</span></span>

![Grundlegendes Datenbindungsdiagramm](media/introduction-to-wpf/databindingmostbasic.png)

<span data-ttu-id="3cfb7-203">Im nächsten Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.TextBox>-Objekt an eine Instanz eines benutzerdefinierten `Person`-Objekts gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-203">The next example demonstrates how to bind a <xref:System.Windows.Controls.TextBox> to an instance of a custom `Person` object.</span></span> <span data-ttu-id="3cfb7-204">Die `Person`-Implementierung wird im folgenden Beispielcode dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-204">The `Person` implementation is shown in the following code:</span></span>

[!code-vb[SimpleDataBindingSnippets#PersonClassCODE](~/samples/snippets/visualbasic/wpf/introduction-to-wpf/introduction-to-wpf_2.vb)]
[!code-csharp[SimpleDataBindingSnippets#PersonClassCODE](~/samples/snippets/csharp/wpf/introduction-to-wpf/introduction-to-wpf_2.cs)]

<span data-ttu-id="3cfb7-205">Das folgende Markup bindet das <xref:System.Windows.Controls.TextBox> an eine Instanz eines benutzerdefinierten- `Person` Objekts:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-205">The following markup binds the <xref:System.Windows.Controls.TextBox> to an instance of a custom `Person` object:</span></span>

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

<span data-ttu-id="3cfb7-206">In diesem Beispiel wird die `Person` -Klasse in CodeBehind instanziiert und als Datenkontext für die `DataBindingWindow`-Klasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-206">In this example, the `Person` class is instantiated in code-behind and is set as the data context for the `DataBindingWindow`.</span></span> <span data-ttu-id="3cfb7-207">Im Markupcode wird die <xref:System.Windows.Controls.TextBox.Text%2A> -Eigenschaft des <xref:System.Windows.Controls.TextBox> -Steuerelements an die `Person.Name` -Eigenschaft gebunden (über die XAML-Syntax`{Binding ... }`).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-207">In markup, the <xref:System.Windows.Controls.TextBox.Text%2A> property of the <xref:System.Windows.Controls.TextBox> is bound to the `Person.Name` property (using the "`{Binding ... }`" XAML syntax).</span></span> <span data-ttu-id="3cfb7-208">Dieser XAML-Code weist WPF an, das <xref:System.Windows.Controls.TextBox> -Steuerelement an das `Person` -Objekt zu binden, das in der <xref:System.Windows.FrameworkElement.DataContext%2A> -Eigenschaft des Fensters gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-208">This XAML tells WPF to bind the <xref:System.Windows.Controls.TextBox> control to the `Person` object that is stored in the <xref:System.Windows.FrameworkElement.DataContext%2A> property of the window.</span></span>

<span data-ttu-id="3cfb7-209">Die Datenbindungs-Engine von WPF bietet zusätzliche Unterstützung, wozu Validierung, Sortierung, Filterung und Gruppierung gehören.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-209">The WPF data binding engine provides additional support that includes validation, sorting, filtering, and grouping.</span></span> <span data-ttu-id="3cfb7-210">Darüber hinaus wird für Datenbindung die Verwendung von Datenvorlagen unterstützt, um eine benutzerdefinierte Benutzeroberfläche für gebundene Daten zu erstellen, wenn die Benutzeroberfläche nicht geeignet ist, die von den WPF-Standardsteuerelementen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-210">Furthermore, data binding supports the use of data templates to create custom user interface for bound data when the user interface displayed by the standard WPF controls is not appropriate.</span></span>

<span data-ttu-id="3cfb7-211">Weitere Informationen finden Sie unter [Übersicht über Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-211">For more information, see [Data binding overview](/dotnet/desktop-wpf/data/data-binding-overview).</span></span>

## <a name="graphics"></a><span data-ttu-id="3cfb7-212">Grafiken</span><span class="sxs-lookup"><span data-stu-id="3cfb7-212">Graphics</span></span>

<span data-ttu-id="3cfb7-213">Mit WPF wird ein umfangreicher, skalierbarer und flexibler Satz von Grafikfeatures eingeführt, die die folgenden Vorteile bieten:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-213">WPF introduces an extensive, scalable, and flexible set of graphics features that have the following benefits:</span></span>

- <span data-ttu-id="3cfb7-214">**Auflösungsunabhängige und geräteunabhängige Grafik**.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-214">**Resolution-independent and device-independent graphics**.</span></span> <span data-ttu-id="3cfb7-215">Die grundlegende Maßeinheit im WPF-Grafiksystem ist das geräteunabhängige Pixel, das, unabhängig von der jeweiligen Bildschirmauflösung, immer 1/96 Zoll entspricht. Diese Maßeinheit bildet die Grundlage für auflösungs- und geräteunabhängiges Rendering.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-215">The basic unit of measurement in the WPF graphics system is the device-independent pixel, which is 1/96th of an inch, regardless of actual screen resolution, and provides the foundation for resolution-independent and device-independent rendering.</span></span> <span data-ttu-id="3cfb7-216">Jedes geräteunabhängige Pixel wird automatisch skaliert, um mit der DPI-Einstellung (Dots Per Inch) des Systems übereinzustimmen, auf dem das Pixel gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-216">Each device-independent pixel automatically scales to match the dots-per-inch (dpi) setting of the system it renders on.</span></span>

- <span data-ttu-id="3cfb7-217">**Höhere Genauigkeit**.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-217">**Improved precision**.</span></span> <span data-ttu-id="3cfb7-218">Das WPF-Koordinatensystem wird mit Gleitkommazahlen mit doppelter Genauigkeit gemessen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-218">The WPF coordinate system is measured with double-precision floating-point numbers rather than single-precision.</span></span> <span data-ttu-id="3cfb7-219">Transformationen und Durchlässigkeitswerte werden ebenfalls mit doppelter Genauigkeit ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-219">Transformations and opacity values are also expressed as double-precision.</span></span> <span data-ttu-id="3cfb7-220">WPF unterstützt auch eine breite Farbskala (scRGB) und unterstützt das Verwalten von Eingaben aus unterschiedlichen Farbräumen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-220">WPF also supports a wide color gamut (scRGB) and provides integrated support for managing inputs from different color spaces.</span></span>

- <span data-ttu-id="3cfb7-221">**Erweiterte Unterstützung für Grafiken und Animationen**.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-221">**Advanced graphics and animation support**.</span></span> <span data-ttu-id="3cfb7-222">WPF vereinfacht die Grafikprogrammierung, indem es Animationsszenen für Sie verwaltet. Sie müssen sich keine Gedanken über Szenenverarbeitung, Renderingschleifen und bilineare Interpolation machen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-222">WPF simplifies graphics programming by managing animation scenes for you; there is no need to worry about scene processing, rendering loops, and bilinear interpolation.</span></span> <span data-ttu-id="3cfb7-223">Darüber bietet WPF Treffertest-Unterstützung und vollständige Alpha-Compositing-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-223">Additionally, WPF provides hit-testing support and full alpha-compositing support.</span></span>

- <span data-ttu-id="3cfb7-224">**Hardware Beschleunigung**.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-224">**Hardware acceleration**.</span></span> <span data-ttu-id="3cfb7-225">Das WPF-Grafiksystem nutzt die Vorteile der Grafikhardware, um die CPU-Auslastung zu verringern.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-225">The WPF graphics system takes advantage of graphics hardware to minimize CPU usage.</span></span>

### <a name="2d-shapes"></a><span data-ttu-id="3cfb7-226">2D-Formen</span><span class="sxs-lookup"><span data-stu-id="3cfb7-226">2D shapes</span></span>

<span data-ttu-id="3cfb7-227">Zu WPF gehört eine Bibliothek häufig verwendeter vektorbasierter 2D-Formen, etwa Rechtecke und Ellipsen, die in der folgenden Abbildung dargestellt sind:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-227">WPF provides a library of common vector-drawn 2D shapes, such as the rectangles and ellipses that are shown in the following illustration:</span></span>

![Ellipsen und Rechtecke](media/introduction-to-wpf/wpfintrofigure4.PNG)

<span data-ttu-id="3cfb7-229">Eine interessante Fähigkeit von Formen ist, dass sie nicht nur zur Anzeige vorhanden sind, sondern für sie auch viele der Features implementiert sind, die Sie von Steuerelementen erwarten, einschließlich Tastatur- und Mauseingaben.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-229">An interesting capability of shapes is that they are not just for display; shapes implement many of the features that you expect from controls, including keyboard and mouse input.</span></span> <span data-ttu-id="3cfb7-230">Das folgende Beispiel zeigt das- <xref:System.Windows.UIElement.MouseUp> Ereignis einer <xref:System.Windows.Shapes.Ellipse> , die behandelt wird:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-230">The following example shows the <xref:System.Windows.UIElement.MouseUp> event of an <xref:System.Windows.Shapes.Ellipse> being handled:</span></span>

[!code-xaml[IntroToWPFSnippets#HandleEllipseMouseUpEventMARKUP](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_7.xaml)]

[!code-vb[IntroToWPFSnippets#HandleEllipseMouseUpEventCODEBEHIND](~/samples/snippets/visualbasic/wpf/introduction-to-wpf/introduction-to-wpf_8.vb)]
[!code-csharp[IntroToWPFSnippets#HandleEllipseMouseUpEventCODEBEHIND](~/samples/snippets/csharp/wpf/introduction-to-wpf/introduction-to-wpf_8.cs)]

<span data-ttu-id="3cfb7-231">In der folgenden Abbildung wird gezeigt, was durch den vorangehenden Code erzeugt wird:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-231">The following figure shows what is produced by the preceding code:</span></span>

![Ein Fenster mit dem Text "you clicked the ellipse&#33;" (Sie haben auf das Auslassungszeichen geklickt).](media/introduction-to-wpf/wpfintrofigure12.png)

<span data-ttu-id="3cfb7-233">Weitere Informationen finden Sie unter [Übersicht über Formen und grundlegende Zeichnungen in WPF](/dotnet/desktop-wpf/data/data-binding-overview).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-233">For more information, see [Shapes and basic drawing in WPF overview](/dotnet/desktop-wpf/data/data-binding-overview).</span></span>

### <a name="2d-geometries"></a><span data-ttu-id="3cfb7-234">2D-Geometrien</span><span class="sxs-lookup"><span data-stu-id="3cfb7-234">2D geometries</span></span>

<span data-ttu-id="3cfb7-235">Die von WPF bereitgestellten 2D-Formen decken die grundlegenden Standardformen ab.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-235">The 2D shapes provided by WPF cover the standard set of basic shapes.</span></span> <span data-ttu-id="3cfb7-236">Möglicherweise müssen Sie jedoch benutzerdefinierte Formen erstellen, um den Entwurf einer angepassten Benutzeroberfläche zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-236">However, you may need to create custom shapes to facilitate the design of a customized user interface.</span></span> <span data-ttu-id="3cfb7-237">Zu diesem Zweck stellt WPF Geometrien bereit.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-237">For this purpose, WPF provides geometries.</span></span> <span data-ttu-id="3cfb7-238">In der folgenden Abbildung wird veranschaulicht, wie Geometrien verwendet werden können, um eine benutzerdefinierte Form zu erstellen, die direkt gezeichnet, als Pinsel verwendet oder dazu verwendet werden kann, andere Formen und Steuerelemente auszuschneiden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-238">The following figure demonstrates the use of geometries to create a custom shape that can be drawn directly, used as a brush, or used to clip other shapes and controls.</span></span>

<span data-ttu-id="3cfb7-239">Mit<xref:System.Windows.Shapes.Path> -Objekten können geschlossene oder offene Formen, Mehrfachformen und sogar gekrümmte Formen gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-239"><xref:System.Windows.Shapes.Path> objects can be used to draw closed or open shapes, multiple shapes, and even curved shapes.</span></span>

<span data-ttu-id="3cfb7-240"><xref:System.Windows.Media.Geometry>-Objekte können zum Ausschneiden, zum Ausführen von Treffertests und zum Rendern von 2D-Grafikdaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-240"><xref:System.Windows.Media.Geometry> objects can be used for clipping, hit-testing, and rendering 2D graphic data.</span></span>

![Verschiedene Einsatzbereiche eines Pfades](media/introduction-to-wpf/wpfintrofigure5.png)

<span data-ttu-id="3cfb7-242">Weitere Informationen finden Sie unter [Übersicht über die Geometrie](graphics-multimedia/geometry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-242">For more information, see [Geometry overview](graphics-multimedia/geometry-overview.md).</span></span>

### <a name="2d-effects"></a><span data-ttu-id="3cfb7-243">2D-Effekte</span><span class="sxs-lookup"><span data-stu-id="3cfb7-243">2D effects</span></span>

<span data-ttu-id="3cfb7-244">Eine Teilmenge der 2D-Funktionen von WPF umfasst visuelle Effekte wie Farbverläufe, Bitmaps, Zeichnungen, Zeichnen mit Videos, Drehung, Skalierung und Neigung.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-244">A subset of WPF 2D capabilities includes visual effects, such as gradients, bitmaps, drawings, painting with videos, rotation, scaling, and skewing.</span></span> <span data-ttu-id="3cfb7-245">Diese werden alle mit Pinsel erreicht. in der folgenden Abbildung werden einige Beispiele gezeigt:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-245">These are all achieved with brushes; the following figure shows some examples:</span></span>

![Darstellung unterschiedlicher Pinsel](media/introduction-to-wpf/wpfintrofigure6.png)

<span data-ttu-id="3cfb7-247">Weitere Informationen finden Sie unter [Übersicht über WPF-Pinsel](graphics-multimedia/wpf-brushes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-247">For more information, see [WPF brushes overview](graphics-multimedia/wpf-brushes-overview.md).</span></span>

### <a name="3d-rendering"></a><span data-ttu-id="3cfb7-248">3D-Rendering</span><span class="sxs-lookup"><span data-stu-id="3cfb7-248">3D rendering</span></span>

<span data-ttu-id="3cfb7-249">WPF beinhaltet auch 3D-Renderingfunktionen, die mit 2D-Grafiken integriert werden können, um die Erstellung ansprechendere und interessanter Benutzeroberflächen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-249">WPF also includes 3D rendering capabilities that integrate with 2D graphics to allow the creation of more exciting and interesting user interfaces.</span></span> <span data-ttu-id="3cfb7-250">Beispielsweise zeigt die folgende Abbildung 2D-Bilder, die auf 3D-Formen gerendert werden:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-250">For example, the following figure shows 2D images rendered onto 3D shapes:</span></span>

![Bildschirmabbildung für Visual3D-Beispiel](media/introduction-to-wpf/wpfintrofigure13.png)

<span data-ttu-id="3cfb7-252">Weitere Informationen finden Sie unter [Übersicht über 3D-Grafiken](graphics-multimedia/3-d-graphics-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-252">For more information, see [3D graphics overview](graphics-multimedia/3-d-graphics-overview.md).</span></span>

## <a name="animation"></a><span data-ttu-id="3cfb7-253">Animation</span><span class="sxs-lookup"><span data-stu-id="3cfb7-253">Animation</span></span>

<span data-ttu-id="3cfb7-254">Die WPF-Animationsunterstützung ermöglicht es Ihnen, Steuerelemente wachsen, bewegen, schütteln sowie ein- und ausblenden zu lassen, um interessante Seitenübergänge zu erstellen, und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-254">WPF animation support lets you make controls grow, shake, spin, and fade, to create interesting page transitions, and more.</span></span> <span data-ttu-id="3cfb7-255">Die meisten WPF-Klassen, selbst benutzerdefinierte Klassen, können animiert werden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-255">You can animate most WPF classes, even custom classes.</span></span> <span data-ttu-id="3cfb7-256">In der folgenden Abbildung wird eine einfache Animation in Aktion gezeigt:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-256">The following figure shows a simple animation in action:</span></span>

![Bilder eines animierten Cubes](media/introduction-to-wpf/wpfintrofigure7.png)

<span data-ttu-id="3cfb7-258">Weitere Informationen finden Sie unter [Übersicht über Animationen](graphics-multimedia/animation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-258">For more information, see [Animation overview](graphics-multimedia/animation-overview.md).</span></span>

## <a name="media"></a><span data-ttu-id="3cfb7-259">Medien</span><span class="sxs-lookup"><span data-stu-id="3cfb7-259">Media</span></span>

<span data-ttu-id="3cfb7-260">Eine Möglichkeit, Inhalte interessant zu vermitteln, ist die Verwendung audiovisueller Medien.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-260">One way to convey rich content is through the use of audiovisual media.</span></span> <span data-ttu-id="3cfb7-261">WPF bietet spezielle Unterstützung für Bilder, Video und Audio.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-261">WPF provides special support for images, video, and audio.</span></span>

### <a name="images"></a><span data-ttu-id="3cfb7-262">Bilder</span><span class="sxs-lookup"><span data-stu-id="3cfb7-262">Images</span></span>

<span data-ttu-id="3cfb7-263">In den meisten Anwendungen werden Bilder verwendet, und WPF bietet mehrere Möglichkeiten, Bilder zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-263">Images are common to most applications, and WPF provides several ways to use them.</span></span> <span data-ttu-id="3cfb7-264">Die folgende Abbildung zeigt eine Benutzeroberfläche mit einem Listenfeld, das Miniaturbilder enthält.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-264">The following figure shows a user interface with a list box that contains thumbnail images.</span></span> <span data-ttu-id="3cfb7-265">Wird eine Miniaturansicht ausgewählt, wird das Bild in voller Größe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-265">When a thumbnail is selected, the image is shown full-size.</span></span>

![Miniaturbilder und ein Bild in voller Größe](media/introduction-to-wpf/wpfintrofigure8.png)

<span data-ttu-id="3cfb7-267">Weitere Informationen finden Sie unter [Übersicht über die Bildverarbeitung](graphics-multimedia/imaging-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-267">For more information, see [Imaging overview](graphics-multimedia/imaging-overview.md).</span></span>

### <a name="video-and-audio"></a><span data-ttu-id="3cfb7-268">Video und Audio</span><span class="sxs-lookup"><span data-stu-id="3cfb7-268">Video and audio</span></span>

<span data-ttu-id="3cfb7-269">Mit dem <xref:System.Windows.Controls.MediaElement> -Steuerelement kann sowohl Video als auch Audio wiedergegeben werden, und es ist flexibel genug, um als Grundlage für einen benutzerdefinierten Media Player verwendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-269">The <xref:System.Windows.Controls.MediaElement> control is capable of playing both video and audio, and it is flexible enough to be the basis for a custom media player.</span></span> <span data-ttu-id="3cfb7-270">Mit dem folgenden XAML-Markup wird ein Media Player implementiert:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-270">The following XAML markup implements a media player:</span></span>

[!code-xaml[IntroToWPFSnippets#MediaElementMARKUP](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_9.xaml)]

<span data-ttu-id="3cfb7-271">Das-Fenster in der folgenden Abbildung zeigt das- <xref:System.Windows.Controls.MediaElement> Steuerelement in Aktion an:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-271">The window in the following figure shows the <xref:System.Windows.Controls.MediaElement> control in action:</span></span>

![Ein MediaElement-Steuerelement mit Audio und Video](media/introduction-to-wpf/wpfintrofigure1.png)

<span data-ttu-id="3cfb7-273">Weitere Informationen finden Sie unter [Grafiken und Multimedia](graphics-multimedia/index.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-273">For more information, see [Graphics and multimedia](graphics-multimedia/index.md).</span></span>

## <a name="text-and-typography"></a><span data-ttu-id="3cfb7-274">Text und Typografie</span><span class="sxs-lookup"><span data-stu-id="3cfb7-274">Text and typography</span></span>

<span data-ttu-id="3cfb7-275">Um ein qualitativ hochwertiges Textrendering zu ermöglichen, bietet WPF die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-275">To facilitate high-quality text rendering, WPF offers the following features:</span></span>

- <span data-ttu-id="3cfb7-276">Unterstützung für OpenType-Schriftarten</span><span class="sxs-lookup"><span data-stu-id="3cfb7-276">OpenType font support.</span></span>

- <span data-ttu-id="3cfb7-277">ClearType-Optimierungen</span><span class="sxs-lookup"><span data-stu-id="3cfb7-277">ClearType enhancements.</span></span>

- <span data-ttu-id="3cfb7-278">Hohe Leistung durch Nutzung von Hardwarebeschleunigung</span><span class="sxs-lookup"><span data-stu-id="3cfb7-278">High performance that takes advantage of hardware acceleration.</span></span>

- <span data-ttu-id="3cfb7-279">Einbinden von Text in Medien, Grafiken und Animationen</span><span class="sxs-lookup"><span data-stu-id="3cfb7-279">Integration of text with media, graphics, and animation.</span></span>

- <span data-ttu-id="3cfb7-280">Unterstützung internationaler Schriftarten und Fallbackmechanismen</span><span class="sxs-lookup"><span data-stu-id="3cfb7-280">International font support and fallback mechanisms.</span></span>

<span data-ttu-id="3cfb7-281">Die folgende Abbildung zeigt die Anwendung von Text Dekorationen, um die Text Integration mit Grafiken zu demonstrieren:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-281">As a demonstration of text integration with graphics, the following figure shows the application of text decorations:</span></span>

![Text mit verschiedenen Textergänzungen](media/introduction-to-wpf/wpfintrofigure23.png)

<span data-ttu-id="3cfb7-283">Weitere Informationen finden Sie unter [Typografie in WPF](advanced/typography-in-wpf.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-283">For more information, see [Typography in Windows Presentation Foundation](advanced/typography-in-wpf.md).</span></span>

## <a name="customize-wpf-apps"></a><span data-ttu-id="3cfb7-284">Anpassen von WPF-Apps</span><span class="sxs-lookup"><span data-stu-id="3cfb7-284">Customize WPF apps</span></span>

<span data-ttu-id="3cfb7-285">Bis zu dieser Stelle haben die WPF-Kernbausteine zur Entwicklung von Anwendungen kennen gelernt.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-285">Up to this point, you've seen the core WPF building blocks for developing applications.</span></span> <span data-ttu-id="3cfb7-286">Sie verwenden das Anwendungsmodell, um Anwendungsinhalte, die hauptsächlich aus Steuerelementen bestehen, zu hosten und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-286">You use the application model to host and deliver application content, which consists mainly of controls.</span></span> <span data-ttu-id="3cfb7-287">Das WPF-Layoutsystem verwenden Sie, um die Anordnung von Steuerelementen in einer Benutzeroberfläche zu vereinfachen und sicherzustellen, dass die Anordnung bei Änderungen von Fenstergröße und Anzeigeeinstellungen erhalten bleibt.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-287">To simplify the arrangement of controls in a user interface, and to ensure the arrangement is maintained in the face of changes to window size and display settings, you use the WPF layout system.</span></span> <span data-ttu-id="3cfb7-288">Da die meisten Anwendungen Benutzern ein Bearbeiten von Daten ermöglichen, verwenden Sie Datenbindung, um den Arbeitsaufwand für das Einbinden der Daten in die jeweilige Benutzeroberfläche zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-288">Because most applications let users interact with data, you use data binding to reduce the work of integrating your user interface with data.</span></span> <span data-ttu-id="3cfb7-289">Um die visuelle Darstellung Ihrer Anwendung zu verbessern, verwenden Sie die umfangreiche Grafik-, Animations- und Medienunterstützung, die von WPF bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-289">To enhance the visual appearance of your application, you use the comprehensive range of graphics, animation, and media support provided by WPF.</span></span>

<span data-ttu-id="3cfb7-290">Häufig reichen die Grundelemente jedoch nicht aus, um eine wirklich herausragende und visuell eindrucksvolle Benutzeroberfläche zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-290">Often, though, the basics are not enough for creating and managing a truly distinct and visually stunning user experience.</span></span> <span data-ttu-id="3cfb7-291">Die Standardsteuerelemente von WPF passen möglicherweise nicht zum gewünschten Erscheinungsbild Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-291">The standard WPF controls might not integrate with the desired appearance of your application.</span></span> <span data-ttu-id="3cfb7-292">Daten können vielleicht nicht auf die bestmögliche Art angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-292">Data might not be displayed in the most effective way.</span></span> <span data-ttu-id="3cfb7-293">Der Gesamteindruck Ihrer Anwendung ist eventuell nicht für das standarmäßige Aussehen und Verhalten der Windows-Designs geeignet.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-293">Your application's overall user experience may not be suited to the default look and feel of Windows themes.</span></span> <span data-ttu-id="3cfb7-294">In vielerlei Hinsicht erfordert eine Präsentationstechnologie visuelle Erweiterbarkeit ebenso wie jede andere Art von Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-294">In many ways, a presentation technology needs visual extensibility as much as any other type of extensibility.</span></span>

<span data-ttu-id="3cfb7-295">Aus diesem Grund bietet die WPF eine Vielzahl von Mechanismen zum Erzeugen einzigartiger Benutzeroberflächen, wie z. B. ein umfangreiches Inhaltsmodell für Steuerelemente, Trigger, Steuerelement- und Datenvorlagen, Stile, Ressourcen für Benutzeroberflächen, Designs und Skins.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-295">For this reason, WPF provides a variety of mechanisms for creating unique user experiences, including a rich content model for controls, triggers, control and data templates, styles, user interface resources, and themes and skins.</span></span>

### <a name="content-model"></a><span data-ttu-id="3cfb7-296">Inhaltsmodell</span><span class="sxs-lookup"><span data-stu-id="3cfb7-296">Content model</span></span>

<span data-ttu-id="3cfb7-297">Die meisten WPF-Steuerelemente haben hauptsächlich die Aufgabe, Inhalte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-297">The main purpose of a majority of the WPF controls is to display content.</span></span> <span data-ttu-id="3cfb7-298">In WPF werden der Typ und die Anzahl von Elementen, die den Inhalt eines Steuerelements bilden können, als *Inhaltsmodell* des Steuerelements bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-298">In WPF, the type and number of items that can constitute the content of a control is referred to as the control's *content model*.</span></span> <span data-ttu-id="3cfb7-299">Einige Steuerelemente können ein einzelnes Element und einen einzelnen Inhaltstyp enthalten. Beispielsweise ist der Inhalt eines <xref:System.Windows.Controls.TextBox> -Steuerelements ein Zeichenfolgenwert, der der <xref:System.Windows.Controls.TextBox.Text%2A> -Eigenschaft zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-299">Some controls can contain a single item and type of content; for example, the content of a <xref:System.Windows.Controls.TextBox> is a string value that is assigned to the <xref:System.Windows.Controls.TextBox.Text%2A> property.</span></span> <span data-ttu-id="3cfb7-300">Im folgenden Beispiel wird der Inhalt einer festgelegt <xref:System.Windows.Controls.TextBox> :</span><span class="sxs-lookup"><span data-stu-id="3cfb7-300">The following example sets the content of a <xref:System.Windows.Controls.TextBox>:</span></span>

```xaml
<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    x:Class="SDKSample.TextBoxContentWindow"
    Title="TextBox Content">

    <TextBox Text="This is the content of a TextBox." />
</Window>
```

<span data-ttu-id="3cfb7-301">Die folgende Abbildung zeigt das Ergebnis:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-301">The following figure shows the result:</span></span>

![Ein TextBox-Steuerelement, das Text enthält](media/introduction-to-wpf/wpfintrofigure21.png)

<span data-ttu-id="3cfb7-303">Andere Steuerelemente können dagegen mehrere Elemente verschiedener Inhaltstypen enthalten. Der Inhalt eines <xref:System.Windows.Controls.Button>-Steuerelements, der durch die <xref:System.Windows.Controls.ContentControl.Content%2A>-Eigenschaft angegeben ist, kann eine Vielzahl von Elementen enthalten, etwa Layoutsteuerelemente, Text, Bildern und Formen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-303">Other controls, however, can contain multiple items of different types of content; the content of a <xref:System.Windows.Controls.Button>, specified by the <xref:System.Windows.Controls.ContentControl.Content%2A> property, can contain a variety of items including layout controls, text, images, and shapes.</span></span> <span data-ttu-id="3cfb7-304">Das folgende Beispiel zeigt eine <xref:System.Windows.Controls.Button> mit Inhalt, der,,, <xref:System.Windows.Controls.DockPanel> und enthält <xref:System.Windows.Controls.Label> <xref:System.Windows.Controls.Border> <xref:System.Windows.Controls.MediaElement> :</span><span class="sxs-lookup"><span data-stu-id="3cfb7-304">The following example shows a <xref:System.Windows.Controls.Button> with content that includes a <xref:System.Windows.Controls.DockPanel>, a <xref:System.Windows.Controls.Label>, a <xref:System.Windows.Controls.Border>, and a <xref:System.Windows.Controls.MediaElement>:</span></span>

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

<span data-ttu-id="3cfb7-305">Die folgende Abbildung zeigt den Inhalt dieser Schaltfläche:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-305">The following figure shows the content of this button:</span></span>

![Eine Schaltfläche, die mehrere Inhaltstypen enthält](media/introduction-to-wpf/wpfintrofigure22.png)

<span data-ttu-id="3cfb7-307">Weitere Informationen zu den Arten von Inhalten, die von verschiedenen Steuerelementen unterstützt werden, finden Sie unter [WPF-Inhalts Modell](controls/wpf-content-model.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-307">For more information on the kinds of content that is supported by various controls, see [WPF content model](controls/wpf-content-model.md).</span></span>

### <a name="triggers"></a><span data-ttu-id="3cfb7-308">Auslöser</span><span class="sxs-lookup"><span data-stu-id="3cfb7-308">Triggers</span></span>

<span data-ttu-id="3cfb7-309">Obwohl der Hauptzweck von XAML-Markup in der Implementierung der Darstellung einer Anwendung besteht, lassen sich mit XAML auch einige Aspekte des Verhaltens einer Anwendung implementieren.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-309">Although the main purpose of XAML markup is to implement an application's appearance, you can also use XAML to implement some aspects of an application's behavior.</span></span> <span data-ttu-id="3cfb7-310">Ein Beispiel ist die Verwendung von Triggern, um die Darstellung einer Anwendung anhand von Benutzeraktionen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-310">One example is the use of triggers to change an application's appearance based on user interactions.</span></span> <span data-ttu-id="3cfb7-311">Weitere Informationen finden Sie unter [Stile und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-311">For more information, see [Styles and templates](/dotnet/desktop-wpf/fundamentals/styles-templates-overview).</span></span>

### <a name="control-templates"></a><span data-ttu-id="3cfb7-312">Steuerelementvorlagen</span><span class="sxs-lookup"><span data-stu-id="3cfb7-312">Control templates</span></span>

<span data-ttu-id="3cfb7-313">Die standardmäßigen Benutzeroberflächen für WPF-Steuerelemente werden üblicherweise aus anderen Steuerelementen und Formen erstellt.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-313">The default user interfaces for WPF controls are typically constructed from other controls and shapes.</span></span> <span data-ttu-id="3cfb7-314">Beispielsweise besteht ein <xref:System.Windows.Controls.Button> -Steuerelement aus einem <xref:Microsoft.Windows.Themes.ButtonChrome> - und einem <xref:System.Windows.Controls.ContentPresenter> -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-314">For example, a <xref:System.Windows.Controls.Button> is composed of both <xref:Microsoft.Windows.Themes.ButtonChrome> and <xref:System.Windows.Controls.ContentPresenter> controls.</span></span> <span data-ttu-id="3cfb7-315">Das <xref:Microsoft.Windows.Themes.ButtonChrome> -Steuerelement stellt die Standarddarstellung der Schaltfläche bereit, während das <xref:System.Windows.Controls.ContentPresenter> -Steuerelement den Inhalt der Schaltfläche anzeigt, der in der <xref:System.Windows.Controls.ContentControl.Content%2A> -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-315">The <xref:Microsoft.Windows.Themes.ButtonChrome> provides the standard button appearance, while the <xref:System.Windows.Controls.ContentPresenter> displays the button's content, as specified by the <xref:System.Windows.Controls.ContentControl.Content%2A> property.</span></span>

<span data-ttu-id="3cfb7-316">Manchmal passt die Standarddarstellung eines Steuerelements nicht zum Gesamterscheinungsbild einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-316">Sometimes the default appearance of a control may be incongruent with the overall appearance of an application.</span></span> <span data-ttu-id="3cfb7-317">In diesem Fall können Sie ein <xref:System.Windows.Controls.ControlTemplate> -Objekt verwenden, um die Darstellung der Benutzeroberfläche des Steuerelements anzupassen, ohne dessen Inhalt und Verhalten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-317">In this case, you can use a <xref:System.Windows.Controls.ControlTemplate> to change the appearance of the control's user interface without changing its content and behavior.</span></span>

<span data-ttu-id="3cfb7-318">Im folgenden Beispiel wird gezeigt, wie die Darstellung eines mit <xref:System.Windows.Controls.Button> einem geändert wird <xref:System.Windows.Controls.ControlTemplate> :</span><span class="sxs-lookup"><span data-stu-id="3cfb7-318">The following example shows how to change the appearance of a <xref:System.Windows.Controls.Button> by using a <xref:System.Windows.Controls.ControlTemplate>:</span></span>

[!code-xaml[IntroToWPFSnippets#ButtonControlTemplateWindowMARKUP](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_16.xaml)]

[!code-csharp[IntroToWPFSnippets#ButtonControlTemplateWindowCODEBEHIND](~/samples/snippets/csharp/wpf/introduction-to-wpf/introduction-to-wpf_17.cs)]
[!code-vb[IntroToWPFSnippets#ButtonControlTemplateWindowCODEBEHIND](~/samples/snippets/visualbasic/wpf/introduction-to-wpf/introduction-to-wpf_17.vb)]

<span data-ttu-id="3cfb7-319">In diesem Beispiel wurde die Standardbenutzeroberfläche der Schaltfläche durch ein <xref:System.Windows.Shapes.Ellipse>-Steuerelement ersetzt, das einen dunkelblauem Rand hat und über ein <xref:System.Windows.Media.RadialGradientBrush>-Steuerelement gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-319">In this example, the default button user interface has been replaced with an <xref:System.Windows.Shapes.Ellipse> that has a dark blue border and is filled using a <xref:System.Windows.Media.RadialGradientBrush>.</span></span> <span data-ttu-id="3cfb7-320">Das <xref:System.Windows.Controls.ContentPresenter> -Steuerelement zeigt den Inhalt des <xref:System.Windows.Controls.Button>-Steuerelements an („Click Me!“).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-320">The <xref:System.Windows.Controls.ContentPresenter> control displays the content of the <xref:System.Windows.Controls.Button>, "Click Me!"</span></span> <span data-ttu-id="3cfb7-321">Wenn auf das <xref:System.Windows.Controls.Button> -Steuerelement geklickt wird, wird das <xref:System.Windows.Controls.Primitives.ButtonBase.Click> -Ereignis weiterhin als Teil des Standardverhaltens des <xref:System.Windows.Controls.Button> n-Steuerelements ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-321">When the <xref:System.Windows.Controls.Button> is clicked, the <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event is still raised as part of the <xref:System.Windows.Controls.Button> control's default behavior.</span></span> <span data-ttu-id="3cfb7-322">Das Ergebnis ist in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-322">The result is shown in the following figure:</span></span>

![Eine elliptische Schaltfläche und ein zweites Fenster](media/introduction-to-wpf/wpfintrofigure2.png)

### <a name="data-templates"></a><span data-ttu-id="3cfb7-324">Datenvorlagen</span><span class="sxs-lookup"><span data-stu-id="3cfb7-324">Data templates</span></span>

<span data-ttu-id="3cfb7-325">Während Sie mit einer Steuerelementvorlage die Darstellung eines Steuerelements angeben können, können Sie mit einer Datenvorlage die Darstellung des Inhalts eines Steuerelements angeben.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-325">Whereas a control template lets you specify the appearance of a control, a data template lets you specify the appearance of a control's content.</span></span> <span data-ttu-id="3cfb7-326">Datenvorlagen werden häufig dazu verwendet, die Anzeige gebundener Daten zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-326">Data templates are frequently used to enhance how bound data is displayed.</span></span> <span data-ttu-id="3cfb7-327">Die folgende Abbildung zeigt die Standarddarstellung für ein- <xref:System.Windows.Controls.ListBox> Objekt, das an eine Auflistung von-Objekten gebunden ist `Task` , wobei jede Aufgabe einen Namen, eine Beschreibung und eine Priorität hat:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-327">The following figure shows the default appearance for a <xref:System.Windows.Controls.ListBox> that is bound to a collection of `Task` objects, where each task has a name, description, and priority:</span></span>

![Ein Listenfeld mit der Standarddarstellung](media/introduction-to-wpf/wpfintrofigure18.png)

<span data-ttu-id="3cfb7-329">Die Standarddarstellung entspricht dem, was Sie von einem <xref:System.Windows.Controls.ListBox>-Steuerelement erwarten.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-329">The default appearance is what you would expect from a <xref:System.Windows.Controls.ListBox>.</span></span> <span data-ttu-id="3cfb7-330">Allerdings enthält die Standarddarstellung jeder Aufgabe nur den Aufgabennamen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-330">However, the default appearance of each task contains only the task name.</span></span> <span data-ttu-id="3cfb7-331">Um den Aufgabennamen, die Beschreibung und die Priorität anzuzeigen, muss die Standarddarstellung der gebundenen Listenelemente des <xref:System.Windows.Controls.ListBox> -Steuerelements über ein <xref:System.Windows.DataTemplate>-Objekt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-331">To show the task name, description, and priority, the default appearance of the <xref:System.Windows.Controls.ListBox> control's bound list items must be changed by using a <xref:System.Windows.DataTemplate>.</span></span> <span data-ttu-id="3cfb7-332">Der folgende XAML-Code definiert eine solche <xref:System.Windows.DataTemplate> , die auf jede Aufgabe angewendet wird, indem das-Attribut verwendet wird <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A> :</span><span class="sxs-lookup"><span data-stu-id="3cfb7-332">The following XAML defines such a <xref:System.Windows.DataTemplate>, which is applied to each task by using the <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A> attribute:</span></span>

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

<span data-ttu-id="3cfb7-333">Die folgende Abbildung zeigt die Auswirkung dieses Codes:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-333">The following figure shows the effect of this code:</span></span>

![Listenfeld, das eine Datenvorlage verwendet](media/introduction-to-wpf/wpfintrofigure19.png)

<span data-ttu-id="3cfb7-335">Beachten Sie, dass das Verhalten und die Gesamtdarstellung des <xref:System.Windows.Controls.ListBox>-Steuerelements beibehalten wurden. Lediglich die Darstellung der vom Listenfeld angezeigten Inhalte wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-335">Note that the <xref:System.Windows.Controls.ListBox> has retained its behavior and overall appearance; only the appearance of the content being displayed by the list box has changed.</span></span>

<span data-ttu-id="3cfb7-336">Weitere Informationen finden Sie unter [Übersicht über Daten](data/data-templating-overview.md)Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-336">For more information, see [Data templating overview](data/data-templating-overview.md).</span></span>

### <a name="styles"></a><span data-ttu-id="3cfb7-337">Stile</span><span class="sxs-lookup"><span data-stu-id="3cfb7-337">Styles</span></span>

<span data-ttu-id="3cfb7-338">Stile ermöglichen Entwicklern und Designern die Standardisierung auf ein bestimmtes Erscheinungsbild ihres Produkts.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-338">Styles enable developers and designers to standardize on a particular appearance for their product.</span></span> <span data-ttu-id="3cfb7-339">WPF stellt ein solides Formatmodell bereit, dessen Grundlage das <xref:System.Windows.Style> -Element bildet.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-339">WPF provides a strong style model, the foundation of which is the <xref:System.Windows.Style> element.</span></span> <span data-ttu-id="3cfb7-340">Im folgenden Beispiel wird ein Stil erstellt, mit dem die Hintergrundfarbe für jedes <xref:System.Windows.Controls.Button> in einem Fenster auf festgelegt wird `Orange` :</span><span class="sxs-lookup"><span data-stu-id="3cfb7-340">The following example creates a style that sets the background color for every <xref:System.Windows.Controls.Button> on a window to `Orange`:</span></span>

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

<span data-ttu-id="3cfb7-341">Da sich dieser Stil auf alle <xref:System.Windows.Controls.Button>-Steuerelemente bezieht, wird er automatisch auf alle Schaltflächen im Fenster angewendet. Dies ist in der folgenden Abbildung zu sehen:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-341">Because this style targets all <xref:System.Windows.Controls.Button> controls, the style is automatically applied to all the buttons in the window, as shown in the following figure:</span></span>

![Zwei orangefarbene Schaltflächen](media/introduction-to-wpf/wpfintrofigure20.png)

<span data-ttu-id="3cfb7-343">Weitere Informationen finden Sie unter [Stile und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-343">For more information, see [Styles and templates](/dotnet/desktop-wpf/fundamentals/styles-templates-overview).</span></span>

### <a name="resources"></a><span data-ttu-id="3cfb7-344">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3cfb7-344">Resources</span></span>

<span data-ttu-id="3cfb7-345">Die Steuerelemente in einer Anwendung sollten die gleiche Darstellung haben, wozu alles von Schriftarten und Hintergrundfarben bis zu Steuerelementvorlagen, Datenvorlagen und Stilen gehören kann.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-345">Controls in an application should share the same appearance, which can include anything from fonts and background colors to control templates, data templates, and styles.</span></span> <span data-ttu-id="3cfb7-346">Über die WPF-Unterstützung für Benutzeroberflächenressourcen können diese Ressourcen in einem einzigen Speicherort kapseln, um sie wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-346">You can use WPF's support for user interface resources to encapsulate these resources in a single location for reuse.</span></span>

<span data-ttu-id="3cfb7-347">Im folgenden Beispiel wird eine gemeinsame Hintergrundfarbe definiert, die von einem und einem gemeinsam verwendet wird <xref:System.Windows.Controls.Button> <xref:System.Windows.Controls.Label> :</span><span class="sxs-lookup"><span data-stu-id="3cfb7-347">The following example defines a common background color that is shared by a <xref:System.Windows.Controls.Button> and a <xref:System.Windows.Controls.Label>:</span></span>

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

<span data-ttu-id="3cfb7-348">In diesem Beispiel wird mit dem `Window.Resources` -Eigenschaftenelements eine Ressource für die Hintergrundfarbe implementiert.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-348">This example implements a background color resource by using the `Window.Resources` property element.</span></span> <span data-ttu-id="3cfb7-349">Diese Ressource ist für alle untergeordneten Elemente des <xref:System.Windows.Window>-Elements verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-349">This resource is available to all children of the <xref:System.Windows.Window>.</span></span> <span data-ttu-id="3cfb7-350">Es gibt eine Vielzahl von Ressourcenbereichen, von denen einige nachfolgend in der Reihenfolge aufgeführt sind, in der sie aufgelöst werden:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-350">There are a variety of resource scopes, including the following, listed in the order in which they are resolved:</span></span>

1. <span data-ttu-id="3cfb7-351">Ein einzelnes Steuerelement (über die geerbte <xref:System.Windows.FrameworkElement.Resources%2A?displayProperty=fullName> -Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3cfb7-351">An individual control (using the inherited <xref:System.Windows.FrameworkElement.Resources%2A?displayProperty=fullName> property).</span></span>

2. <span data-ttu-id="3cfb7-352">Ein <xref:System.Windows.Window> - oder <xref:System.Windows.Controls.Page> -Element (ebenfalls über die geerbte <xref:System.Windows.FrameworkElement.Resources%2A?displayProperty=fullName> -Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3cfb7-352">A <xref:System.Windows.Window> or a <xref:System.Windows.Controls.Page> (also using the inherited <xref:System.Windows.FrameworkElement.Resources%2A?displayProperty=fullName> property).</span></span>

3. <span data-ttu-id="3cfb7-353">Ein <xref:System.Windows.Application> -Element (über die <xref:System.Windows.Application.Resources%2A?displayProperty=fullName> -Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3cfb7-353">An <xref:System.Windows.Application> (using the <xref:System.Windows.Application.Resources%2A?displayProperty=fullName> property).</span></span>

<span data-ttu-id="3cfb7-354">Durch die Vielzahl von Bereichen erhalten Sie Flexibilität in Bezug auf die Art, mit der Sie Ihre Ressourcen definieren und freigeben.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-354">The variety of scopes gives you flexibility with respect to the way in which you define and share your resources.</span></span>

<span data-ttu-id="3cfb7-355">Anstatt Ihre Ressourcen direkt mit einem bestimmten Bereich zu verknüpfen, können Sie eine oder mehrere Ressourcen über ein separates <xref:System.Windows.ResourceDictionary> -Element verpacken, auf das in anderen Teilen einer Anwendung verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-355">As an alternative to directly associating your resources with a particular scope, you can package one or more resources by using a separate <xref:System.Windows.ResourceDictionary> that can be referenced in other parts of an application.</span></span> <span data-ttu-id="3cfb7-356">Im folgenden Beispiel wird z. b. eine Standard Hintergrundfarbe in einem Ressourcen Wörterbuch definiert:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-356">For example, the following example defines a default background color in a resource dictionary:</span></span>

```xaml
<ResourceDictionary
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">

  <!-- Define background color resource -->
  <SolidColorBrush x:Key="defaultBackground" Color="Red" />

  <!-- Define other resources -->
</ResourceDictionary>
```

<span data-ttu-id="3cfb7-357">Im folgenden Beispiel wird auf das Ressourcen Wörterbuch verwiesen, das im vorherigen Beispiel definiert wurde, sodass es in einer Anwendung freigegeben ist:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-357">The following example references the resource dictionary defined in the previous example so that it is shared across an application:</span></span>

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

<span data-ttu-id="3cfb7-358">Ressourcen und Ressourcenwörterbücher bilden die Grundlage der WPF-Unterstützung für Designs und Skins.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-358">Resources and resource dictionaries are the foundation of WPF support for themes and skins.</span></span>

<span data-ttu-id="3cfb7-359">Weitere Informationen finden Sie unter [Ressourcen](/dotnet/desktop-wpf/fundamentals/xaml-resources-define).</span><span class="sxs-lookup"><span data-stu-id="3cfb7-359">For more information, see [Resources](/dotnet/desktop-wpf/fundamentals/xaml-resources-define).</span></span>

### <a name="custom-controls"></a><span data-ttu-id="3cfb7-360">Benutzerdefinierte Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3cfb7-360">Custom controls</span></span>

<span data-ttu-id="3cfb7-361">Obwohl WPF umfangreiche Unterstützung für Anpassungen bietet, kann es Fälle geben, in denen die vorhandenen WPF-Steuerelemente den Anforderungen Ihrer Anwendung oder denen der Benutzer nicht genügen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-361">Although WPF provides a host of customization support, you may encounter situations where existing WPF controls do not meet the needs of either your application or its users.</span></span> <span data-ttu-id="3cfb7-362">Dies kann auftreten, wenn Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-362">This can occur when:</span></span>

- <span data-ttu-id="3cfb7-363">Die von Ihnen gewünschte Benutzeroberfläche kann nicht erstellt werden, indem das Aussehen und Verhalten vorhandener WPF-Implementierungen angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-363">The user interface that you require cannot be created by customizing the look and feel of existing WPF implementations.</span></span>

- <span data-ttu-id="3cfb7-364">Das von Ihnen gewünschte Verhalten wird von vorhandenen WPF-Implementierungen nicht (oder nicht einfach) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-364">The behavior that you require is not supported (or not easily supported) by existing WPF implementations.</span></span>

<span data-ttu-id="3cfb7-365">An diesem Punkt können Sie jedoch eines der drei WPF-Modelle nutzen, um ein neues Steuerelement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-365">At this point, however, you can take advantage of one of three WPF models to create a new control.</span></span> <span data-ttu-id="3cfb7-366">Jedes Modell ist für ein bestimmtes Szenario vorgesehen und erfordert, dass Ihr benutzerdefiniertes Steuerelement aus einer bestimmten WPF-Basisklasse abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-366">Each model targets a specific scenario and requires your custom control to derive from a particular WPF base class.</span></span> <span data-ttu-id="3cfb7-367">Die drei Modelle sind hier aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="3cfb7-367">The three models are listed here:</span></span>

- <span data-ttu-id="3cfb7-368">**Benutzersteuerelementmodell**</span><span class="sxs-lookup"><span data-stu-id="3cfb7-368">**User Control Model**.</span></span> <span data-ttu-id="3cfb7-369">Ein benutzerdefiniertes Steuerelement wird aus <xref:System.Windows.Controls.UserControl> abgeleitet und besteht aus mindestens einem anderen Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-369">A custom control derives from <xref:System.Windows.Controls.UserControl> and is composed of one or more other controls.</span></span>

- <span data-ttu-id="3cfb7-370">**Steuerelementmodell**</span><span class="sxs-lookup"><span data-stu-id="3cfb7-370">**Control Model**.</span></span> <span data-ttu-id="3cfb7-371">Ein benutzerdefiniertes Steuerelement wird aus <xref:System.Windows.Controls.Control> abgeleitet und dazu verwendet, eine Implementierung zu erstellen, deren Verhalten mithilfe von Vorlagen von ihrer Darstellung getrennt wird, so wie beim Großteil der WPF-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-371">A custom control derives from <xref:System.Windows.Controls.Control> and is used to build implementations that separate their behavior from their appearance using templates, much like the majority of WPF controls.</span></span> <span data-ttu-id="3cfb7-372">Durch Ableiten aus <xref:System.Windows.Controls.Control> erhalten Sie für ein Erstellen einer benutzerdefinierten Benutzeroberfläche mehr Freiheit als mit Benutzersteuerelementen, dies kann jedoch höheren Aufwand erfordern.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-372">Deriving from <xref:System.Windows.Controls.Control> allows you more freedom for creating a custom user interface than user controls, but it may require more effort.</span></span>

- <span data-ttu-id="3cfb7-373">**Frameworkelementmodell**.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-373">**Framework Element Model**.</span></span> <span data-ttu-id="3cfb7-374">Ein benutzerdefiniertes Steuerelement wird aus <xref:System.Windows.FrameworkElement> abgeleitet, wenn seine Darstellung durch benutzerdefinierte Renderinglogik (nicht durch Vorlagen) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-374">A custom control derives from <xref:System.Windows.FrameworkElement> when its appearance is defined by custom rendering logic (not templates).</span></span>

<span data-ttu-id="3cfb7-375">Das folgende Beispiel zeigt ein benutzerdefiniertes numerisches auf-/ab-Steuerelement, <xref:System.Windows.Controls.UserControl> das von abgeleitet wird</span><span class="sxs-lookup"><span data-stu-id="3cfb7-375">The following example shows a custom numeric up/down control that derives from <xref:System.Windows.Controls.UserControl>:</span></span>

[!code-xaml[IntroToWPFSnippets#UserControlMARKUP](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_33.xaml)]

[!code-csharp[IntroToWPFSnippets#UserControlCODEBEHIND1](~/samples/snippets/csharp/wpf/introduction-to-wpf/introduction-to-wpf_34.cs)]
[!code-vb[IntroToWPFSnippets#UserControlCODEBEHIND1](~/samples/snippets/visualbasic/wpf/introduction-to-wpf/introduction-to-wpf_34.vb)]

<span data-ttu-id="3cfb7-376">Im folgenden Beispiel wird der XAML-Code veranschaulicht, der erforderlich ist, um das Benutzer Steuerelement in einen zu integrieren <xref:System.Windows.Window> :</span><span class="sxs-lookup"><span data-stu-id="3cfb7-376">The following example illustrates the XAML that is required to incorporate the user control into a <xref:System.Windows.Window>:</span></span>

[!code-xaml[IntroToWPFSnippets#UserControlWindowMARKUP1](~/samples/snippets/xaml/wpf/introduction-to-wpf/introduction-to-wpf_37.xaml)]

<span data-ttu-id="3cfb7-377">Die folgende Abbildung zeigt das-Steuerelement, das `NumericUpDown` in einem gehostet wird <xref:System.Windows.Window> :</span><span class="sxs-lookup"><span data-stu-id="3cfb7-377">The following figure shows the `NumericUpDown` control hosted in a <xref:System.Windows.Window>:</span></span>

![Ein benutzerdefiniertes UserControl](media/introduction-to-wpf/wpfintrofigure3.png)

<span data-ttu-id="3cfb7-379">Weitere Informationen zu benutzerdefinierten Steuerelementen finden Sie unter [Übersicht über das Erstellen von Steuer](controls/control-authoring-overview.md)Elementen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-379">For more information on custom controls, see [Control authoring overview](controls/control-authoring-overview.md).</span></span>

## <a name="wpf-best-practices"></a><span data-ttu-id="3cfb7-380">Bewährte Methoden für WPF</span><span class="sxs-lookup"><span data-stu-id="3cfb7-380">WPF best practices</span></span>

<span data-ttu-id="3cfb7-381">Wie bei jeder Entwicklungsplattform kann das gewünschte Ergebnis mit WPF auf verschiedene Arten erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-381">As with any development platform, WPF can be used in a variety of ways to achieve the desired result.</span></span> <span data-ttu-id="3cfb7-382">Um sichergehen zu können, dass Ihre WPF-Anwendungen die geforderte Benutzerfreundlichkeit bereitstellen und grundsätzlich den Ansprüche der Zielgruppe entsprechen, gibt es empfohlene bewährte Methoden in Bezug auf Barrierefreiheit, Globalisierung, Lokalisierung und Leistung.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-382">As a way of ensuring that your WPF applications provide the required user experience and meet the demands of the audience in general, there are recommended best practices for accessibility, globalization and localization, and performance.</span></span> <span data-ttu-id="3cfb7-383">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="3cfb7-383">For more information, see:</span></span>

- [<span data-ttu-id="3cfb7-384">Bedienungshilfen</span><span class="sxs-lookup"><span data-stu-id="3cfb7-384">Accessibility</span></span>](/dotnet/framework/ui-automation/accessibility-best-practices)
- [<span data-ttu-id="3cfb7-385">Übersicht über WPF-Globalisierung und -Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="3cfb7-385">WPF globalization and localization</span></span>](advanced/wpf-globalization-and-localization-overview.md)
- [<span data-ttu-id="3cfb7-386">Optimieren der WPF-Anwendungsleistung</span><span class="sxs-lookup"><span data-stu-id="3cfb7-386">WPF app performance</span></span>](advanced/optimizing-wpf-application-performance.md)
- [<span data-ttu-id="3cfb7-387">WPF-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="3cfb7-387">WPF security</span></span>](security-wpf.md)

## <a name="next-steps"></a><span data-ttu-id="3cfb7-388">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="3cfb7-388">Next steps</span></span>

<span data-ttu-id="3cfb7-389">In diesem Artikel wurden die Schlüsselfeatures von WPF erläutert.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-389">We've looked at the key features of WPF.</span></span> <span data-ttu-id="3cfb7-390">Jetzt können Sie Ihre erste WPF-App erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cfb7-390">Now it's time to build your first WPF app.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="3cfb7-391">Exemplarische Vorgehensweise: Meine erste WPF-Desktopanwendung</span><span class="sxs-lookup"><span data-stu-id="3cfb7-391">Walkthrough: My first WPF desktop app</span></span>](getting-started/walkthrough-my-first-wpf-desktop-application.md)

## <a name="see-also"></a><span data-ttu-id="3cfb7-392">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cfb7-392">See also</span></span>

- [<span data-ttu-id="3cfb7-393">Erste Schritte mit WPF</span><span class="sxs-lookup"><span data-stu-id="3cfb7-393">Get started with WPF</span></span>](getting-started/index.md)
- [<span data-ttu-id="3cfb7-394">Windows Presentation Foundation</span><span class="sxs-lookup"><span data-stu-id="3cfb7-394">Windows Presentation Foundation</span></span>](index.md)
- [<span data-ttu-id="3cfb7-395">Ressourcen für die WPF-Community</span><span class="sxs-lookup"><span data-stu-id="3cfb7-395">WPF community resources</span></span>](getting-started/community-feedback.md)
