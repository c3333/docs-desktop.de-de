---
title: Benutzeroberflächen Automatisierung eines benutzerdefinierten Steuer Elements
ms.date: 03/30/2017
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [WPF], applying UI automation
- accessibility [WPF], applying to custom controls
- custom controls [WPF], improving accessibility
- UI Automation [WPF], using with custom controls
ms.assetid: 47b310fc-fbd5-4ce2-a606-22d04c6d4911
ms.openlocfilehash: 684f08a2a56c2095163c3deeed0223dabad2cea7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977699"
---
# <a name="ui-automation-of-a-wpf-custom-control"></a>Benutzeroberflächenautomatisierung eines benutzerdefinierten WPF-Steuerelements
[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] stellt eine einzelne allgemeine Schnittstelle bereit, die Automatisierungsclients zum Untersuchen oder Ausführen der Benutzerschnittstellen in unterschiedlichen Plattformen und Frameworks verwenden können. [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] ermöglicht es jeweils Qualitätssicherungcode (Testcode) und Barrierefreiheitsanwendungen, z.B. die Sprachausgabe, Benutzerschnittstellenelemente zu untersuchen und Benutzerzugriff mit ihnen aus anderem Code zu simulieren. Informationen zu [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] für alle Plattformen finden Sie unter „Barrierefreiheit“.  
  
 In diesem Thema wird beschrieben, wie ein serverseitiger Benutzeroberflächenautomatisierungs-Anbieter, der in einer WPF-Anwendung ausgeführt wird, für ein benutzerdefiniertes Steuerelement implementiert wird. WPF unterstützt [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] über eine Struktur von Peer-Automatisierungsobjekten, die zur Struktur der Elemente der Benutzeroberfläche parallel ist. Testcode und -anwendungen, die Barrierefreiheitsfunktionen bereitstellen, können Automatisierungspeerobjekte direkt (für Code, der gerade ausgeführt wird) oder über eine allgemeine Schnittstelle verwenden, die von [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] bereitgestellt wird.  

<a name="AutomationPeerClasses"></a>
## <a name="automation-peer-classes"></a>Automatisierungspeerklassen  
 WPF-Steuerelemente unterstützen [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] über eine Struktur von Peer Klassen, die von abgeleitet werden <xref:System.Windows.Automation.Peers.AutomationPeer> . Gemäß der Konvention beginnen Namen von Peerklassen mit dem Klassennamen des Steuerelements und enden mit „AutomationPeer“. Beispielsweise <xref:System.Windows.Automation.Peers.ButtonAutomationPeer> ist die Peer Klasse für die <xref:System.Windows.Controls.Button> Steuerelement Klasse. Die Peer Klassen entsprechen ungefähr den [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] Steuerelement Typen, sind jedoch für WPF-Elemente spezifisch. Automatisierungscode der auf WPF-Anwendungen über die [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]-Schnittstelle zugreift, verwendet keine Automatisierungspeers direkt, jedoch kann der Automatisierungscode im selben Prozessbereich Automatisierungspeers direkt verwenden.  
  
<a name="BuiltInAutomationPeerClasses"></a>
## <a name="built-in-automation-peer-classes"></a>Integrierte Automatisierungspeerklassen  
 Elemente implementieren eine Automatisierungspeerklasse, wenn sie Schnittstellenaktivität vom Benutzer akzeptieren oder Informationen enthalten, die von Benutzern von Anwendungen der Sprachausgabe benötigt werden. Nicht alle visuellen WPF-Elemente verfügen über Automatisierungspeers. Beispiele für Klassen, die Automatisierungs Peers implementieren <xref:System.Windows.Controls.Button> , sind, <xref:System.Windows.Controls.TextBox> und <xref:System.Windows.Controls.Label> . Beispiele für Klassen, die keine Automatisierungspeers implementieren, sind Klassen, die von abgeleitet werden, z. b. <xref:System.Windows.Controls.Decorator> <xref:System.Windows.Controls.Border> und Klassen, die auf basieren <xref:System.Windows.Controls.Panel> , z <xref:System.Windows.Controls.Grid> . b <xref:System.Windows.Controls.Canvas> .  
  
 Die Basis <xref:System.Windows.Controls.Control> Klasse verfügt nicht über eine entsprechende Peer Klasse. Wenn Sie eine Peer Klasse benötigen, die einem benutzerdefinierten Steuerelement entspricht, das von abgeleitet <xref:System.Windows.Controls.Control> wird, sollten Sie die benutzerdefinierte Peer Klasse von ableiten <xref:System.Windows.Automation.Peers.FrameworkElementAutomationPeer> .  
  
<a name="SecurityConsiderations"></a>
## <a name="security-considerations-for-derived-peers"></a>Sicherheitsüberlegungen zu abgeleiteten Peers  
 Automatisierungspeers müssen in einer Teilausführungsumgebung ausgeführt werden. Code in der UIAutomationClient-Assembly ist nicht konfiguriert, in einer teilweise vertrauenswürdigen Umgebung ausgeführt zu werden, und Automatisierungspeercode sollte nicht auf diese Assembly verweisen. Stattdessen sollten Sie diese Klassen in der UIAutomationTypes-Assembly verwenden. Sie sollten z. b. die- <xref:System.Windows.Automation.AutomationElementIdentifiers> Klasse aus der UIAutomationTypes-Assembly verwenden, die der- <xref:System.Windows.Automation.AutomationElement> Klasse in der UIAutomationClient-Assembly entspricht. Es ist sicher, auf die UIAutomationTypes-Assembly in Automatisierungspeercode zu verweisen.  
  
<a name="PeerNavigation"></a>
## <a name="peer-navigation"></a>Peernavigation  
 Nach dem Auffinden eines Automatisierungspeer kann in-Process-Code durch Aufrufen der-Methode und der-Methode des-Objekts durch Aufrufen der- <xref:System.Windows.Automation.Peers.AutomationPeer.GetChildren%2A> <xref:System.Windows.Automation.Peers.AutomationPeer.GetParent%2A> Methode Die Navigation zwischen WPF-Elementen in einem-Steuerelement wird von der-Implementierung der-Methode des Peers unterstützt <xref:System.Windows.Automation.Peers.AutomationPeer.GetChildrenCore%2A> . Das Benutzeroberflächenautomatisierungssystem ruft diese Methode auf, um eine Struktur von Unterelementen zu erstellen, die in einem Steuerelement vorhanden sind, z.B. Listenelemente in einem Listenfeld. Die Standard <xref:System.Windows.Automation.Peers.UIElementAutomationPeer.GetChildrenCore%2A?displayProperty=nameWithType> Methode durchläuft die visuelle Struktur der Elemente, um die Struktur von Automatisierungspeers zu erstellen. Benutzerdefinierte Steuerelemente überschreiben diese Methode, um untergeordnete Elemente für Automatisierungsclients verfügbar zu machen, dabei werden die Automatisierungspeers von Elementen zurückgegeben, die Informationen ausdrücken oder Benutzerinteraktion erlauben.  
  
<a name="Customizations"></a>
## <a name="customizations-in-a-derived-peer"></a>Anpassungen in einem abgeleiteten Peer  
 Alle Klassen, die von abgeleitet werden <xref:System.Windows.UIElement> und <xref:System.Windows.ContentElement> die geschützte virtuelle Methode enthalten <xref:System.Windows.UIElement.OnCreateAutomationPeer%2A> . WPF-Aufrufe <xref:System.Windows.UIElement.OnCreateAutomationPeer%2A> , um das Automatisierungs Peer Objekt für jedes Steuerelement zu erhalten. Automatisierungscode kann Peers zum Abrufen von Informationen über Merkmale und Funktionen des Steuerelements verwenden und um interaktive Verwendung zu simulieren. Ein benutzerdefiniertes Steuerelement, das Automation unterstützt, muss <xref:System.Windows.UIElement.OnCreateAutomationPeer%2A> eine Instanz einer von abgeleiteten Klasse überschreiben und zurückgeben <xref:System.Windows.Automation.Peers.AutomationPeer> . Wenn ein benutzerdefiniertes Steuerelement beispielsweise von der- <xref:System.Windows.Controls.Primitives.ButtonBase> Klasse abgeleitet ist, sollte das von zurückgegebene-Objekt <xref:System.Windows.UIElement.OnCreateAutomationPeer%2A> von abgeleitet werden <xref:System.Windows.Automation.Peers.ButtonBaseAutomationPeer> .  
  
 Wenn Sie ein benutzerdefiniertes Steuerelement implementieren, müssen Sie die „Kernmethoden“ der grundlegenden Automatisierungspeerklasse außer Kraft setzen, die das Verhalten eindeutig beschreiben und für Ihr benutzerdefiniertes Steuerelement spezifisch sind.  
  
### <a name="override-oncreateautomationpeer"></a>OnCreateAutomationPeer außer Kraft setzen  
 Überschreiben <xref:System.Windows.UIElement.OnCreateAutomationPeer%2A> Sie die-Methode für das benutzerdefinierte Steuerelement, sodass es das Anbieter Objekt zurückgibt, das direkt oder indirekt von abgeleitet werden muss <xref:System.Windows.Automation.Peers.AutomationPeer> .  
  
### <a name="override-getpattern"></a>GetPattern außer Kraft setzen  
 Automatisierungspeers vereinfachen zwar manche technischen Aspekte der Implementierung von serverseitigen [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]-Anbietern, aber Automatisierungspeers von benutzerdefinierten Steuerelementen müssen dennoch Musterschnittstellen behandeln. Wie nicht-WPF-Anbieter unterstützen Peers Steuerelement Muster, indem Sie Implementierungen von Schnittstellen im- <xref:System.Windows.Automation.Provider?displayProperty=nameWithType> Namespace bereitstellen, z <xref:System.Windows.Automation.Provider.IInvokeProvider> . b.. Die Schnittstellen der Steuerelementmuster können entweder vom Peer selbst, oder von einem anderen Objekt implementiert werden. Die Peer-Implementierung von <xref:System.Windows.Automation.Peers.AutomationPeer.GetPattern%2A> gibt das Objekt zurück, das das angegebene Muster unterstützt. [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] der Code Ruft die <xref:System.Windows.Automation.Peers.UIElementAutomationPeer.GetPattern%2A> Methode auf und gibt einen- <xref:System.Windows.Automation.Peers.PatternInterface> Enumerationswert an. Die außer Kraft Setzung von <xref:System.Windows.Automation.Peers.UIElementAutomationPeer.GetPattern%2A> sollte das Objekt zurückgeben, das das angegebene Muster implementiert. Wenn das Steuerelement keine benutzerdefinierte Implementierung eines Musters hat, können Sie die-Implementierung des Basistyps aufrufen <xref:System.Windows.Automation.Peers.AutomationPeer.GetPattern%2A> , um entweder seine-Implementierung abzurufen, oder NULL, wenn das Muster für diesen Steuerelement Typen nicht unterstützt wird. Beispielsweise kann ein benutzerdefiniertes NumericUpDown-Steuerelement auf einen Wert innerhalb eines Bereichs festgelegt werden, sodass [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] der Peer die- <xref:System.Windows.Automation.Provider.IRangeValueProvider> Schnittstelle implementieren würde. Im folgenden Beispiel wird gezeigt, wie die-Methode des Peers <xref:System.Windows.Automation.Peers.UIElementAutomationPeer.GetPattern%2A> überschrieben wird, um auf einen-Wert zu reagieren <xref:System.Windows.Automation.Peers.PatternInterface.RangeValue?displayProperty=nameWithType> .  
  
 [!code-csharp[CustomControlNumericUpDown#GetPattern](~/samples/snippets/csharp/VS_Snippets_Wpf/CustomControlNumericUpDown/CSharp/CustomControlLibrary/NumericUpDown.cs#getpattern)]
 [!code-vb[CustomControlNumericUpDown#GetPattern](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CustomControlNumericUpDown/visualbasic/customcontrollibrary/numericupdown.vb#getpattern)]  
  
 Eine <xref:System.Windows.Automation.Peers.UIElementAutomationPeer.GetPattern%2A> Methode kann auch ein Unterelement als Muster Anbieter angeben. Der folgende Code zeigt, wie die <xref:System.Windows.Controls.ItemsControl> Verarbeitung von scrollmustern an den Peer des internen Steuer Elements überträgt <xref:System.Windows.Controls.ScrollViewer> .  
  
```csharp  
public override object GetPattern(PatternInterface patternInterface)  
{  
    if (patternInterface == PatternInterface.Scroll)  
    {  
        ItemsControl owner = (ItemsControl) base.Owner;  
  
        // ScrollHost is internal to the ItemsControl class  
        if (owner.ScrollHost != null)  
        {  
            AutomationPeer peer = UIElementAutomationPeer.CreatePeerForElement(owner.ScrollHost);  
            if ((peer != null) && (peer is IScrollProvider))  
            {  
                peer.EventsSource = this;  
                return (IScrollProvider) peer;  
            }  
        }  
    }  
    return base.GetPattern(patternInterface);  
}  
```  
  
```vb  
Public Class Class1  
    Public Overrides Function GetPattern(ByVal patternInterface__1 As PatternInterface) As Object  
        If patternInterface1 = PatternInterface.Scroll Then  
            Dim owner As ItemsControl = DirectCast(MyBase.Owner, ItemsControl)  
  
            ' ScrollHost is internal to the ItemsControl class  
            If owner.ScrollHost IsNot Nothing Then  
                Dim peer As AutomationPeer = UIElementAutomationPeer.CreatePeerForElement(owner.ScrollHost)  
                If (peer IsNot Nothing) AndAlso (TypeOf peer Is IScrollProvider) Then  
                    peer.EventsSource = Me  
                    Return DirectCast(peer, IScrollProvider)  
                End If  
            End If  
        End If  
        Return MyBase.GetPattern(patternInterface1)  
    End Function  
End Class  
```  
  
 Um ein Unterelement für die Muster Behandlung anzugeben, ruft dieser Code das untergeordnete Objekt ab, erstellt mithilfe der-Methode einen Peer, <xref:System.Windows.Automation.Peers.UIElementAutomationPeer.CreatePeerForElement%2A> legt die <xref:System.Windows.Automation.Peers.AutomationPeer.EventsSource%2A> -Eigenschaft des neuen Peers auf den aktuellen Peer fest und gibt den neuen Peer zurück. Durch Festlegen von <xref:System.Windows.Automation.Peers.AutomationPeer.EventsSource%2A> für ein Unterelement wird verhindert, dass das Unterelement in der Automatisierungs Peer Struktur angezeigt wird, und es werden alle Ereignisse, die vom Unterelement ausgelöst werden, als Ausgangswert aus dem in angegebenen Steuerelement festgelegt <xref:System.Windows.Automation.Peers.AutomationPeer.EventsSource%2A> . Das <xref:System.Windows.Controls.ScrollViewer> -Steuerelement wird nicht in der Automatisierungs Struktur angezeigt, und die von ihm generierten scrollereignisse scheinen aus dem-Objekt zu stammen <xref:System.Windows.Controls.ItemsControl> .  
  
### <a name="override-core-methods"></a>„Kern“-Methode außer Kraft setzen  
 Der Automatisierungscode ruft Informationen über Ihr Steuerelement ab, indem er die öffentlichen Methoden der Peer-Klasse aufruft. Um Informationen über Ihr Steuerelement bereitzustellen, setzen Sie jede Methode außer Kraft, deren Name mit „Core“ endet, falls die Implementierung Ihrer Steuerelemente sich von der Implementierung unterscheidet, die von der Basis-Automatisierungspeerklasse bereitgestellt wird. Das-Steuerelement muss mindestens die <xref:System.Windows.Automation.Peers.AutomationPeer.GetClassNameCore%2A> -Methode und die- <xref:System.Windows.Automation.Peers.AutomationPeer.GetAutomationControlTypeCore%2A> Methode implementieren, wie im folgenden Beispiel gezeigt.  
  
 [!code-csharp[CustomControlNumericUpDown#CoreOverrides](~/samples/snippets/csharp/VS_Snippets_Wpf/CustomControlNumericUpDown/CSharp/CustomControlLibrary/NumericUpDown.cs#coreoverrides)]
 [!code-vb[CustomControlNumericUpDown#CoreOverrides](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CustomControlNumericUpDown/visualbasic/customcontrollibrary/numericupdown.vb#coreoverrides)]  
  
 Ihre Implementierung von <xref:System.Windows.Automation.Peers.AutomationPeer.GetAutomationControlTypeCore%2A> beschreibt das Steuerelement, indem ein-Wert zurückgegeben wird <xref:System.Windows.Automation.ControlType> . Obwohl Sie zurückgeben können <xref:System.Windows.Automation.ControlType.Custom?displayProperty=nameWithType> , sollten Sie einen der spezifischeren Steuerelement Typen zurückgeben, wenn er das Steuerelement genau beschreibt. Der Rückgabewert <xref:System.Windows.Automation.ControlType.Custom?displayProperty=nameWithType> erfordert zusätzliche Arbeit, damit der Anbieter implementiert [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] , und [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] Client Produkte können die Steuerelement Struktur, die Tastatur Interaktion und mögliche Steuerelement Muster nicht vorhersehen.  
  
 Implementieren Sie die <xref:System.Windows.Automation.Peers.AutomationPeer.IsContentElementCore%2A> -Methode und die- <xref:System.Windows.Automation.Peers.AutomationPeer.IsControlElementCore%2A> Methode, um anzugeben, ob das Steuerelement Dateninhalte enthält oder eine interaktive Rolle in der Benutzeroberfläche erfüllt (oder beides). Standardmäßig geben die beiden Methoden `true` zurück. Diese Einstellungen verbessern die Nutzbarkeit der Automatisierungstools, wie z.B. Sprachausgabe-Tools, die mit diesen Methoden die Automatisierungsstruktur filtern. Wenn die <xref:System.Windows.Automation.Peers.AutomationPeer.GetPattern%2A> Methode die Muster Verarbeitung an einen untergeordneten Peer überträgt, kann die-Methode des Subelements-Peers <xref:System.Windows.Automation.Peers.AutomationPeer.IsControlElementCore%2A> false zurückgeben, um den subelarpeer aus der Automatisierungs Struktur auszublenden. Beispielsweise wird der Bildlauf in einem <xref:System.Windows.Controls.ListBox> von einer verarbeitet <xref:System.Windows.Controls.ScrollViewer> , und der <xref:System.Windows.Automation.Peers.PatternInterface.Scroll?displayProperty=nameWithType> Automatisierungspeer für wird von der-Methode der-Instanz zurückgegeben, die <xref:System.Windows.Automation.Peers.AutomationPeer.GetPattern%2A> <xref:System.Windows.Automation.Peers.ScrollViewerAutomationPeer> dem zugeordnet ist <xref:System.Windows.Automation.Peers.ListBoxAutomationPeer> . Daher gibt die- <xref:System.Windows.Automation.Peers.AutomationPeer.IsControlElementCore%2A> Methode von <xref:System.Windows.Automation.Peers.ScrollViewerAutomationPeer> zurück `false` , sodass der <xref:System.Windows.Automation.Peers.ScrollViewerAutomationPeer> nicht in der Automatisierungs Struktur angezeigt wird.  
  
 Ihr Automatisierungspeer sollte dem Steuerelement entsprechende Standardwerte bereitstellen. Beachten Sie, dass XAML, das auf das Steuerelement verweist, ihre Peer Implementierungen von Kern Methoden durch Einschließen von Attributen überschreiben kann <xref:System.Windows.Automation.AutomationProperties> . Der folgende XAML-Code erstellt z.B.. eine Schaltfläche mit zwei benutzerdefinierten [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]-Eigenschaften.  
  
```xaml  
<Button AutomationProperties.Name="Special"
    AutomationProperties.HelpText="This is a special button."/>  
```  
  
### <a name="implement-pattern-providers"></a>Implementieren von Musteranbietern  
 Die von einem benutzerdefinierten Anbieter implementierten Schnittstellen werden explizit deklariert, wenn das besitzende Element direkt von abgeleitet wird <xref:System.Windows.Controls.Control> . Der folgende Code deklariert z. b. einen Peer für einen <xref:System.Windows.Controls.Control> , der einen Bereichs Wert implementiert.  
  
```csharp  
public class RangePeer1 : FrameworkElementAutomationPeer, IRangeValueProvider { }  
```  
  
```vb  
Public Class RangePeer1  
    Inherits FrameworkElementAutomationPeer  
    Implements IRangeValueProvider  
End Class  
```  
  
 Wenn das besitzende Steuerelement von einem bestimmten Steuerelement, z <xref:System.Windows.Controls.Primitives.RangeBase> . b., abgeleitet ist, kann der Peer von einer entsprechenden abgeleiteten Peer Klasse abgeleitet werden. In diesem Fall wird der Peer von abgeleitet <xref:System.Windows.Automation.Peers.RangeBaseAutomationPeer> , der eine Basis Implementierung von bereitstellt <xref:System.Windows.Automation.Provider.IRangeValueProvider> . Der folgende Code veranschaulicht die Deklaration eines solchen Peers.  
  
```csharp  
public class RangePeer2 : RangeBaseAutomationPeer { }  
```  
  
```vb  
Public Class RangePeer2  
    Inherits RangeBaseAutomationPeer  
End Class  
```  
  
Eine Beispiel Implementierung finden Sie im [c#](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/CustomControlNumericUpDown/CSharp) -oder [Visual Basic](https://github.com/dotnet/docs/tree/master/samples/snippets/visualbasic/VS_Snippets_Wpf/CustomControlNumericUpDown/visualbasic) Quellcode, der implementiert und ein benutzerdefiniertes NumericUpDown-Steuerelement verwendet.  
  
### <a name="raise-events"></a>Auslösen von Ereignissen  
 Automatisierungsclients können Automatisierungsereignisse abonnieren. Benutzerdefinierte Steuerelemente müssen Änderungen zum Steuern des Zustands melden, indem Sie die- <xref:System.Windows.Automation.Peers.AutomationPeer.RaiseAutomationEvent%2A> Methode aufrufen. Wenn sich ein Eigenschafts Wert ändert, wird auch die- <xref:System.Windows.Automation.Peers.AutomationPeer.RaisePropertyChangedEvent%2A> Methode aufgerufen. Der folgende Code zeigt, wie Sie das Peerobjekt aus dem Steuerelementcode abrufen und eine Methode zum Auslösen eines Ereignisses aufrufen. Als Optimierung überprüft der Code, ob Listener für diesen Ereignistyp vorhanden sind. Ereignisse werden nur dann ausgelöst, wenn Listener vorhanden sind, sodass unnötiger Aufwand vermieden wird und das Steuerelement reaktionsfähig bleibt.  
  
 [!code-csharp[CustomControlNumericUpDown#RaiseEventFromControl](~/samples/snippets/csharp/VS_Snippets_Wpf/CustomControlNumericUpDown/CSharp/CustomControlLibrary/NumericUpDown.cs#raiseeventfromcontrol)]
 [!code-vb[CustomControlNumericUpDown#RaiseEventFromControl](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CustomControlNumericUpDown/visualbasic/customcontrollibrary/numericupdown.vb#raiseeventfromcontrol)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Benutzeroberflächenautomatisierung](/dotnet/framework/ui-automation/ui-automation-overview)
- [Implementierung eines serverseitigen Benutzeroberflächenautomatisierungs-Anbieters](/dotnet/framework/ui-automation/server-side-ui-automation-provider-implementation)
- [Benutzerdefiniertes NumericUpDown-Steuerelement (c#) auf GitHub](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/CustomControlNumericUpDown/CSharp)  
- [Benutzerdefiniertes NumericUpDown-Steuerelement (Visual Basic) auf GitHub](https://github.com/dotnet/docs/tree/master/samples/snippets/visualbasic/VS_Snippets_Wpf/CustomControlNumericUpDown/visualbasic)
