---
title: 'Gewusst wie: Erstellen eines Add-Ins, das eine Benutzeroberfläche zurückgibt'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- creating an add-in that returns a UI [WPF]
- implementing add-in pipeline segments [WPF]
- add-in [WPF], returns a UI
ms.assetid: 57f274b7-4c66-4b72-92eb-81939a393776
ms.openlocfilehash: 8e26a77fcf0d265444316ee374d835791a10749e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977991"
---
# <a name="how-to-create-an-add-in-that-returns-a-ui"></a>Gewusst wie: Erstellen eines Add-Ins, das eine Benutzeroberfläche zurückgibt

Dieses Beispiel zeigt, wie Sie ein Add-in erstellen, das eine Windows Presentation Foundation (WPF) an eine eigenständige WPF-Host Anwendung zurückgibt.  
  
 Das Add-in gibt eine Benutzeroberfläche zurück, die ein WPF-Benutzer Steuerelement ist. Der Inhalt des Benutzersteuerelements ist eine einzelne Schaltfläche, bei der ein Meldungsfeld angezeigt wird, wenn Benutzer darauf klicken. Die eigenständige WPF-Anwendung hostet das Add-in und zeigt das Benutzer Steuerelement (das vom Add-in zurückgegeben wird) als Inhalt des Hauptfensters der Anwendung an.  
  
 **Voraussetzungen**  
  
 In diesem Beispiel werden die WPF-Erweiterungen für das .NET Framework Add-in-Modell hervorgehoben, das dieses Szenario ermöglicht, und es wird Folgendes vorausgesetzt:  
  
- Kenntnisse des .NET Framework Add-in-Modells, einschließlich Pipeline, Add-in und Host Entwicklung. Wenn Sie mit diesen Konzepten nicht vertraut sind, finden Sie weitere Informationen unter [Add-Ins und Erweiterbarkeit](/previous-versions/dotnet/netframework-4.0/bb384200(v%3dvs.100)). Ein Tutorial, in dem die Implementierung einer Pipeline, ein Add-in und eine Host Anwendung veranschaulicht wird, finden Sie unter Exemplarische Vorgehensweise [: Erstellen einer erweiterbaren Anwendung](/previous-versions/dotnet/netframework-4.0/bb788290(v%3dvs.100)).  
  
- Informationen zu den WPF-Erweiterungen für das .NET Framework Add-in-Modell finden Sie hier: [Übersicht über WPF-Add-Ins](wpf-add-ins-overview.md).  
  
## <a name="example"></a>Beispiel  

 Zum Erstellen eines Add-Ins, das eine WPF-Benutzeroberfläche zurückgibt, ist bestimmter Code für jedes Pipeline Segment, das Add-in und die Host Anwendung erforderlich.  

<a name="Contract"></a>

## <a name="implementing-the-contract-pipeline-segment"></a>Implementieren des Vertragspipelinesegments  

 Eine Methode muss vom Vertrag zum Zurückgeben einer Benutzeroberfläche definiert werden, und der Rückgabewert muss vom Typ sein <xref:System.AddIn.Contract.INativeHandleContract> . Dies wird durch die- `GetAddInUI` Methode des- `IWPFAddInContract` Vertrags im folgenden Code veranschaulicht.  
  
 [!code-csharp[SimpleAddInReturnsAUISample#ContractCode](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/CSharp/Contracts/IWPFAddInContract.cs#contractcode)]
 [!code-vb[SimpleAddInReturnsAUISample#ContractCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/VisualBasic/Contracts/IWPFAddInContract.vb#contractcode)]  
  
<a name="AddInView"></a>

## <a name="implementing-the-add-in-view-pipeline-segment"></a>Implementieren des Add-In-Ansichtspipelinesegments  

 Da das Add-in die UIs implementiert, die es als Unterklassen von bereitstellt <xref:System.Windows.FrameworkElement> , muss die-Methode in der Add-in-Ansicht, die mit korreliert, `IWPFAddInView.GetAddInUI` einen Wert vom Typ zurückgeben <xref:System.Windows.FrameworkElement> . Im folgenden Code wird die als Schnittstelle implementierte Add-In-Ansicht des Vertrags gezeigt.  
  
 [!code-csharp[SimpleAddInReturnsAUISample#AddInViewCode](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/CSharp/AddInViews/IWPFAddInView.cs#addinviewcode)]
 [!code-vb[SimpleAddInReturnsAUISample#AddInViewCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/VisualBasic/AddInViews/IWPFAddInView.vb#addinviewcode)]  
  
<a name="AddInSideAdapter"></a>

## <a name="implementing-the-add-in-side-adapter-pipeline-segment"></a>Implementieren des Add-In-seitigen Adapterpipelinesegments  

 Die Contract-Methode gibt einen zurück <xref:System.AddIn.Contract.INativeHandleContract> , aber das Add-in gibt eine zurück <xref:System.Windows.FrameworkElement> (wie von der Add-in-Ansicht angegeben). Folglich <xref:System.Windows.FrameworkElement> muss <xref:System.AddIn.Contract.INativeHandleContract> vor dem Überschreiten der Isolations Grenze in eine konvertiert werden. Diese Arbeit wird vom Add-in-seitigen Adapter durch Aufrufen von ausgeführt <xref:System.AddIn.Pipeline.FrameworkElementAdapters.ViewToContractAdapter%2A> , wie im folgenden Code gezeigt.  
  
 [!code-csharp[SimpleAddInReturnsAUISample#AddInSideAdapterCode](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/CSharp/AddInSideAdapters/WPFAddIn_ViewToContractAddInSideAdapter.cs#addinsideadaptercode)]
 [!code-vb[SimpleAddInReturnsAUISample#AddInSideAdapterCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/VisualBasic/AddInSideAdapters/WPFAddIn_ViewToContractAddInSideAdapter.vb#addinsideadaptercode)]  
  
<a name="HostView"></a>

## <a name="implementing-the-host-view-pipeline-segment"></a>Implementieren des Host-Ansichtspipelinesegments  

 Da die Host Anwendung eine anzeigt <xref:System.Windows.FrameworkElement> , muss die Methode in der Host Ansicht, die mit korreliert, `IWPFAddInHostView.GetAddInUI` einen Wert vom Typ zurückgeben <xref:System.Windows.FrameworkElement> . Im folgenden Code wird die als Schnittstelle implementierte Hostansicht des Vertrags gezeigt.  
  
 [!code-csharp[SimpleAddInReturnsAUISample#HostViewCode](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/CSharp/HostViews/IWPFAddInHostView.cs#hostviewcode)]
 [!code-vb[SimpleAddInReturnsAUISample#HostViewCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/VisualBasic/HostViews/IWPFAddInHostView.vb#hostviewcode)]  
  
<a name="HostSideAdapter"></a>

## <a name="implementing-the-host-side-adapter-pipeline-segment"></a>Implementieren des hostseitigen Adapterpipelinesegments  

 Die Contract-Methode gibt einen zurück <xref:System.AddIn.Contract.INativeHandleContract> , aber die Host Anwendung erwartet einen <xref:System.Windows.FrameworkElement> (wie in der Host Ansicht angegeben). Folglich <xref:System.AddIn.Contract.INativeHandleContract> muss nach dem über <xref:System.Windows.FrameworkElement> schreiten der Isolations Grenze in eine konvertiert werden. Diese Arbeit wird vom Host seitigen Adapter durch Aufrufen von ausgeführt <xref:System.AddIn.Pipeline.FrameworkElementAdapters.ContractToViewAdapter%2A> , wie im folgenden Code gezeigt.  
  
 [!code-csharp[SimpleAddInReturnsAUISample#HostSideAdapterCode](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/CSharp/HostSideAdapters/WPFAddIn_ContractToViewHostSideAdapter.cs#hostsideadaptercode)]
 [!code-vb[SimpleAddInReturnsAUISample#HostSideAdapterCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/VisualBasic/HostSideAdapters/WPFAddIn_ContractToViewHostSideAdapter.vb#hostsideadaptercode)]  
  
<a name="AddIn"></a>

## <a name="implementing-the-add-in"></a>Implementieren des Add-Ins  

 Wenn der Add-in-seitige Adapter und die Add-in-Ansicht erstellt wurden, muss das Add-in ( `WPFAddIn1.AddIn` ) die- `IWPFAddInView.GetAddInUI` Methode implementieren, um ein-Objekt zurückzugeben <xref:System.Windows.FrameworkElement> ( <xref:System.Windows.Controls.UserControl> in diesem Beispiel). Die Implementierung des <xref:System.Windows.Controls.UserControl> , `AddInUI` , wird durch den folgenden Code dargestellt.  
  
 [!code-xaml[SimpleAddInReturnsAUISample#AddInUIMarkup](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/CSharp/WPFAddIn1/AddInUI.xaml#addinuimarkup)]  
  
 [!code-csharp[SimpleAddInReturnsAUISample#AddInUICodeBehind](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/CSharp/WPFAddIn1/AddInUI.xaml.cs#addinuicodebehind)]
 [!code-vb[SimpleAddInReturnsAUISample#AddInUICodeBehind](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/VisualBasic/WPFAddIn1/AddInUI.xaml.vb#addinuicodebehind)]  
  
 Die Implementierung von `IWPFAddInView.GetAddInUI` durch das Add-in muss einfach eine neue Instanz von zurückgeben `AddInUI` , wie im folgenden Code gezeigt.  
  
 [!code-csharp[SimpleAddInReturnsAUISample#AddInCode](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/CSharp/WPFAddIn1/AddIn.cs#addincode)]
 [!code-vb[SimpleAddInReturnsAUISample#AddInCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/VisualBasic/WPFAddIn1/AddIn.vb#addincode)]  
  
<a name="App"></a>

## <a name="implementing-the-host-application"></a>Implementieren der Hostanwendung  

 Wenn der Host seitige Adapter und die Host Ansicht erstellt wurden, kann die Host Anwendung das .NET Framework Add-in-Modell verwenden, um die Pipeline zu öffnen, eine Host Ansicht des Add-Ins abzurufen und die Methode aufzurufen `IWPFAddInHostView.GetAddInUI` . Diese Schritte werden im folgenden Code gezeigt.  
  
 [!code-csharp[SimpleAddInReturnsAUISample#GetUICode](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/CSharp/Host/MainWindow.xaml.cs#getuicode)]
 [!code-vb[SimpleAddInReturnsAUISample#GetUICode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleAddInReturnsAUISample/VisualBasic/Host/MainWindow.xaml.vb#getuicode)]  
  
## <a name="see-also"></a>Siehe auch

- [Add-Ins und Erweiterbarkeit](/previous-versions/dotnet/netframework-4.0/bb384200(v%3dvs.100))
- [Übersicht über WPF-Add-Ins](wpf-add-ins-overview.md)
