---
title: 'Gewusst wie: Erstellen eines Add-Ins, das eine Benutzeroberfläche ist'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- creating an add-in that is a UI [WPF]
- add-ins [WPF], UI
- creating UI add-ins [WPF]
- UI add-ins [WPF], creating
- implementing UI add-ins [WPF]
- pipeline segments [WPF], creating add-ins
ms.assetid: 86375525-282b-4039-8352-8680051a10ea
ms.openlocfilehash: fd37e651dc94485becf972533bc095f9ad253335
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977125"
---
# <a name="how-to-create-an-add-in-that-is-a-ui"></a>Gewusst wie: Erstellen eines Add-Ins, das eine Benutzeroberfläche ist

Dieses Beispiel zeigt, wie ein Add-in erstellt wird, das ein Windows Presentation Foundation (WPF) ist, das von einer eigenständigen WPF-Anwendung gehostet wird.  
  
 Das-Add-in ist eine Benutzeroberfläche, die ein WPF-Benutzer Steuerelement ist. Der Inhalt des Benutzersteuerelements ist eine einzelne Schaltfläche, bei der ein Meldungsfeld angezeigt wird, wenn Benutzer darauf klicken. Die eigenständige WPF-Anwendung hostet die Add-in-Benutzeroberfläche als Inhalt des Haupt Anwendungsfensters.  
  
 **Voraussetzungen**  
  
 In diesem Beispiel werden die WPF-Erweiterungen für das .NET Framework Add-in-Modell hervorgehoben, das dieses Szenario ermöglicht, und es wird Folgendes vorausgesetzt:  
  
- Kenntnisse des .NET Framework Add-in-Modells, einschließlich Pipeline, Add-in und Host Entwicklung. Wenn Sie mit diesen Konzepten nicht vertraut sind, finden Sie weitere Informationen unter [Add-Ins und Erweiterbarkeit](/previous-versions/dotnet/netframework-4.0/bb384200(v%3dvs.100)). Ein Tutorial, in dem die Implementierung einer Pipeline, ein Add-in und eine Host Anwendung veranschaulicht wird, finden Sie unter Exemplarische Vorgehensweise [: Erstellen einer erweiterbaren Anwendung](/previous-versions/dotnet/netframework-4.0/bb788290(v%3dvs.100)).  
  
- Kenntnisse der WPF-Erweiterungen für das .NET Framework Add-in-Modell. Informationen finden Sie unter [Übersicht über WPF Add-Ins](wpf-add-ins-overview.md).  
  
## <a name="example"></a>Beispiel  

 Zum Erstellen eines Add-Ins, bei dem es sich um eine WPF-Benutzeroberfläche handelt, ist für jedes Pipeline Segment, das Add-in und die Host Anwendung spezifischer Code erforderlich.  

<a name="Contract"></a>

## <a name="implementing-the-contract-pipeline-segment"></a>Implementieren des Vertragspipelinesegments

Wenn ein Add-in eine Benutzeroberfläche ist, muss der Vertrag für das Add-in implementieren <xref:System.AddIn.Contract.INativeHandleContract> . Im Beispiel implementiert, `IWPFAddInContract` <xref:System.AddIn.Contract.INativeHandleContract> wie im folgenden Code gezeigt.  
  
[!code-csharp[SimpleAddInIsAUISample#ContractCode](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInIsAUISample/CSharp/Contracts/IWPFAddInContract.cs#contractcode)]
[!code-vb[SimpleAddInIsAUISample#ContractCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInIsAUISample/VisualBasic/Contracts/IWPFAddInContract.vb#contractcode)]

<a name="AddInViewPipeline"></a>

## <a name="implementing-the-add-in-view-pipeline-segment"></a>Implementieren des Add-In-Ansichtspipelinesegments

Da das Add-in als Unterklasse des Typs implementiert ist <xref:System.Windows.FrameworkElement> , muss die Add-in-Ansicht auch Unterklasse sein <xref:System.Windows.FrameworkElement> . Der folgende Code zeigt die Add-in-Ansicht des Vertrags, der als- `WPFAddInView` Klasse implementiert ist.  
  
[!code-csharp[SimpleAddInIsAUISample#AddInViewCode](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInIsAUISample/CSharp/AddInViews/WPFAddInView.cs#addinviewcode)]  
[!code-vb[SimpleAddInIsAUISample#AddInViewCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInIsAUISample/VisualBasic/AddInViews/WPFAddInView.vb#AddInViewCode)]  
  
Hier wird die Add-in-Ansicht von abgeleitet <xref:System.Windows.Controls.UserControl> . Folglich sollte die Add-in-Benutzeroberfläche auch von abgeleitet werden <xref:System.Windows.Controls.UserControl> .  
  
<a name="AddInSideAdapter"></a>

## <a name="implementing-the-add-in-side-adapter-pipeline-segment"></a>Implementieren des Add-In-seitigen Adapterpipelinesegments

Während der Vertrag ein ist <xref:System.AddIn.Contract.INativeHandleContract> , ist das Add-in ein <xref:System.Windows.FrameworkElement> (wie durch das Add-in-Ansichts Pipeline Segment angegeben). Daher <xref:System.Windows.FrameworkElement> muss <xref:System.AddIn.Contract.INativeHandleContract> vor dem Überschreiten der Isolations Grenze in eine konvertiert werden. Diese Arbeit wird vom Add-in-seitigen Adapter durch Aufrufen von ausgeführt <xref:System.AddIn.Pipeline.FrameworkElementAdapters.ViewToContractAdapter%2A> , wie im folgenden Code gezeigt.  
  
[!code-csharp[SimpleAddInIsAUISample#AddInSideAdapterCode](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInIsAUISample/CSharp/AddInSideAdapters/WPFAddIn_ViewToContractAddInSideAdapter.cs#addinsideadaptercode)]  
[!code-vb[SimpleAddInIsAUISample#AddInSideAdapterCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInIsAUISample/VisualBasic/AddInSideAdapters/WPFAddIn_ViewToContractAddInSideAdapter.vb#addinsideadaptercode)]

Im Add-in-Modell, in dem ein Add-in eine Benutzeroberfläche zurückgibt (siehe [Erstellen eines Add-In, das eine Benutzeroberfläche zurückgibt](how-to-create-an-add-in-that-returns-a-ui.md)), konvertiert der Add-in-Adapter den <xref:System.Windows.FrameworkElement> in einen, <xref:System.AddIn.Contract.INativeHandleContract> indem er aufgerufen hat <xref:System.AddIn.Pipeline.FrameworkElementAdapters.ViewToContractAdapter%2A> . <xref:System.AddIn.Pipeline.FrameworkElementAdapters.ViewToContractAdapter%2A> muss in diesem Modell auch aufgerufen werden, obwohl Sie eine Methode implementieren müssen, von der der Code zum Aufrufen geschrieben werden muss. Dazu überschreiben <xref:System.AddIn.Pipeline.ContractBase.QueryContract%2A> und implementieren Sie den Code, der aufruft, <xref:System.AddIn.Pipeline.FrameworkElementAdapters.ViewToContractAdapter%2A> Wenn der Code, der aufruft, <xref:System.AddIn.Pipeline.ContractBase.QueryContract%2A> einen erwartet <xref:System.AddIn.Contract.INativeHandleContract> . In diesem Fall ist der Aufrufer der hostseitige Adapter, der in einem nachfolgenden Unterabschnitt behandelt wird.  
  
> [!NOTE]
> Außerdem müssen Sie <xref:System.AddIn.Pipeline.ContractBase.QueryContract%2A> in diesem Modell überschreiben, um die Tabstopps zwischen der Benutzeroberfläche der Host Anwendung und der Add-in-Benutzeroberfläche zu ermöglichen Weitere Informationen finden Sie unter "WPF-Add-In Einschränkungen" in [WPF Add-Ins Übersicht](wpf-add-ins-overview.md).  
  
Da der Add-in-seitige Adapter eine Schnittstelle implementiert, die von abgeleitet ist <xref:System.AddIn.Contract.INativeHandleContract> , müssen Sie auch implementieren <xref:System.AddIn.Contract.INativeHandleContract.GetHandle%2A> , obwohl dies ignoriert wird, wenn <xref:System.AddIn.Pipeline.ContractBase.QueryContract%2A> überschrieben wird.  
  
<a name="HostViewPipeline"></a>

## <a name="implementing-the-host-view-pipeline-segment"></a>Implementieren des Host-Ansichtspipelinesegments

In diesem Modell erwartet die Host Anwendung in der Regel, dass die Host Ansicht eine <xref:System.Windows.FrameworkElement> Unterklasse ist. Der Host seitige Adapter muss den <xref:System.AddIn.Contract.INativeHandleContract> in einen konvertieren, <xref:System.Windows.FrameworkElement> nachdem der <xref:System.AddIn.Contract.INativeHandleContract> die Isolations Grenze überschreitet. Da eine Methode nicht von der Host Anwendung aufgerufen wird, um das zu erhalten <xref:System.Windows.FrameworkElement> , muss die Host Ansicht den "Return" zurückgeben, <xref:System.Windows.FrameworkElement> indem Sie Sie enthält. Folglich muss die Host Ansicht von einer Unterklasse von abgeleitet <xref:System.Windows.FrameworkElement> werden, die andere Benutzeroberflächen enthalten kann, z <xref:System.Windows.Controls.UserControl> . b.. Der folgende Code zeigt die Host Ansicht des Vertrags, der als-Klasse implementiert ist `WPFAddInHostView` .  

[!code-csharp[WPFAddInHostView class](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInIsAUISample/CSharp/HostViews/WPFAddInHostView.cs#HostViewCode)]
[!code-vb[WPFAddInHostView class](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInIsAUISample/VisualBasic/HostViews/WPFAddInHostView.vb#HostViewCode)]

<a name="HostSideAdapter"></a>

## <a name="implementing-the-host-side-adapter-pipeline-segment"></a>Implementieren des hostseitigen Adapterpipelinesegments

Während der Vertrag ein ist <xref:System.AddIn.Contract.INativeHandleContract> , erwartet die Host Anwendung eine <xref:System.Windows.Controls.UserControl> (wie in der Host Ansicht angegeben). Folglich <xref:System.AddIn.Contract.INativeHandleContract> muss nach dem über <xref:System.Windows.FrameworkElement> schreiten der Isolations Grenze in eine konvertiert werden, bevor als Inhalt der Host Ansicht (die von abgeleitet wird) festgelegt wird <xref:System.Windows.Controls.UserControl> .  
  
Dieser Vorgang wird vom hostseitigen Adapter ausgeführt, wie im folgenden Code gezeigt.  

[!code-csharp[Host-side adapter](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInIsAUISample/CSharp/HostSideAdapters/WPFAddIn_ContractToViewHostSideAdapter.cs#HostSideAdapterCode)]
[!code-vb[Host-side adapter](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInIsAUISample/VisualBasic/HostSideAdapters/WPFAddIn_ContractToViewHostSideAdapter.vb#HostSideAdapterCode)]

Wie Sie sehen, ruft der Host seitige Adapter den ab, <xref:System.AddIn.Contract.INativeHandleContract> indem er die-Methode des Add-in-seitigen Adapters aufruft <xref:System.AddIn.Pipeline.ContractBase.QueryContract%2A> (Dies ist der Punkt, an dem der die <xref:System.AddIn.Contract.INativeHandleContract> Isolations Grenze überschreitet).  
  
Der Host seitige Adapter konvertiert dann den <xref:System.AddIn.Contract.INativeHandleContract> in einen, <xref:System.Windows.FrameworkElement> indem er aufgerufen wird <xref:System.AddIn.Pipeline.FrameworkElementAdapters.ContractToViewAdapter%2A> . Schließlich wird der <xref:System.Windows.FrameworkElement> als Inhalt der Host Ansicht festgelegt.  
  
<a name="AddIn"></a>

## <a name="implementing-the-add-in"></a>Implementieren des Add-Ins

Sind der Add-In-seitige Adapter und die Add-In-Ansicht eingerichtet, kann das Add-In durch Ableiten von der Add-In-Ansicht implementiert werden, wie in folgendem Code gezeigt.  

[!code-csharp[Add-in implementation](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInIsAUISample/CSharp/WPFAddIn1/AddInUI.xaml.cs#AddInCodeBehind)]
[!code-vb[Add-in implementation](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInIsAUISample/VisualBasic/WPFAddIn1/AddInUI.xaml.vb#AddInCodeBehind)]

In diesem Beispiel können Sie einen interessanten Vorteil dieses Modells sehen: Add-in-Entwickler müssen nur das Add-in implementieren (da es sich auch um die Benutzeroberfläche handelt), anstatt sowohl eine Add-in-Klasse als auch eine Add-in-Benutzeroberfläche zu implementieren.  
  
<a name="HostApp"></a>

## <a name="implementing-the-host-application"></a>Implementieren der Hostanwendung

Wenn der Host seitige Adapter und die Host Ansicht erstellt wurden, kann die Host Anwendung das .NET Framework Add-in-Modell verwenden, um die Pipeline zu öffnen und eine Host Ansicht des Add-Ins abzurufen. Diese Schritte werden im folgenden Code gezeigt.  

[!code-csharp[Acquiring a host view of the add-in](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInIsAUISample/CSharp/Host/MainWindow.xaml.cs#GetUICode)]
[!code-vb[Acquiring a host view of the add-in](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInIsAUISample/VisualBasic/Host/MainWindow.xaml.vb#GetUICode)]

Die Host Anwendung verwendet typische .NET Framework Add-in-Modellcode, um das Add-in zu aktivieren, das implizit die Host Ansicht an die Host Anwendung zurückgibt. Die Host Anwendung zeigt anschließend die Host Ansicht (ist <xref:System.Windows.Controls.UserControl> ) aus einer an <xref:System.Windows.Controls.Grid> .  
  
 Der Code für die Verarbeitung von Interaktionen mit der Add-in-Benutzeroberfläche wird in der Anwendungsdomäne des Add-Ins ausgeführt. Diese Interaktionen umfassen Folgendes:  
  
- Behandeln des <xref:System.Windows.Controls.Button> <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignisses.  
  
- Die wird angezeigt <xref:System.Windows.MessageBox> .  
  
 Diese Aktivität ist von der Hostanwendung vollständig isoliert.  
  
## <a name="see-also"></a>Siehe auch

- [Add-Ins und Erweiterbarkeit](/previous-versions/dotnet/netframework-4.0/bb384200(v%3dvs.100))
- [Übersicht über WPF-Add-Ins](wpf-add-ins-overview.md)
