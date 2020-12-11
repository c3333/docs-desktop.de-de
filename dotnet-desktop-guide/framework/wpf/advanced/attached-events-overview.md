---
title: Übersicht über angefügte Ereignisse
ms.date: 03/30/2017
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- handling attached events [WPF]
- defining attached events as routed events [WPF]
- attached events [WPF], scenarios for
- attached events vs. routed events [WPF]
- backing attached events with routed events [WPF]
- attached events [WPF], definition
ms.assetid: 2c40eae3-80e4-4a45-ae09-df6c9ab4d91e
ms.openlocfilehash: bcd9f0d3feac9cd5df475268edb4001e2c99f87a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976441"
---
# <a name="attached-events-overview"></a>Übersicht über angefügte Ereignisse

Extensible Application Markup Language (XAML) definiert eine Sprachkomponente und einen Ereignistyp, der als *angefügtes Ereignis* bezeichnet wird. Mit dem Konzept eines angefügten Ereignisses können Sie einen Handler für ein bestimmtes Ereignis zu einem beliebigen Element und nicht zu einem Element, das tatsächlich das Ereignis definiert oder erbt, hinzufügen. In diesem Fall definiert oder „besitzt“ weder das Objekt, das potenziell das Ereignis auslöst, noch die Instanz der Richtungsbehandlung das Ereignis.  

<a name="prerequisites"></a>
## <a name="prerequisites"></a>Voraussetzungen  
 In diesem Thema wird davon ausgegangen, dass Sie die Artikel [Übersicht über Routingereignisse](routed-events-overview.md) und [Übersicht über XAML (WPF)](/dotnet/desktop-wpf/fundamentals/xaml) gelesen haben.  
  
<a name="Syntax"></a>
## <a name="attached-event-syntax"></a>Syntax der angefügten Ereignisse  
 Angefügte Ereignisse verfügen über eine XAML-Syntax und ein Codierungs Muster, das vom Unterstützungs Code verwendet werden muss, um die angefügte Ereignis Verwendung zu unterstützen.  
  
 In der XAML-Syntax wird das angefügte-Ereignis nicht nur anhand seines Ereignis namens angegeben, sondern durch seinen besitzenden Typ plus dem Ereignis Namen, getrennt durch einen Punkt (.). Da der Name des Ereignisses mit dem Namen des besitzenden Typs qualifiziert wird, ermöglicht es die Syntax der angefügten Ereignisse jedem angefügten Ereignis an jedes Element angefügt zu werden, die instanziiert werden können.  
  
 Im folgenden finden Sie beispielsweise die XAML-Syntax zum Anfügen eines Handlers für ein benutzerdefiniertes `NeedsCleaning` angefügtes Ereignis:  
  
 [!code-xaml[WPFAquariumSln#AE](~/samples/snippets/csharp/VS_Snippets_Wpf/WPFAquariumSln/CSharp/WPFAquarium/Window1.xaml#ae)]  
  
 Beachten Sie das `aqua:`-Präfix. Das Präfix ist in diesem Fall erforderlich, da das angefügte Ereignis ein benutzerdefiniertes Ereignis ist, das aus einer benutzerdefinierten zugeordneten xmlns stammt.  
  
<a name="WPFImplements"></a>
## <a name="how-wpf-implements-attached-events"></a>So implementiert WPF angefügte Ereignisse

In WPF werden angefügte Ereignisse von einem <xref:System.Windows.RoutedEvent> Feld gestützt und durch die Struktur weitergeleitet, nachdem Sie ausgelöst wurden. In der Regel ist die Quelle des angefügten Ereignisses (das Objekt, welches das Ereignis auslöst) eine System- oder Dienstquelle, und das Objekt, das den Ereignis auslösenden Code ausführt, ist daher nicht direkter Teil der Elementstruktur.  
  
<a name="Scenarios"></a>
## <a name="scenarios-for-attached-events"></a>Szenarios für angefügte Ereignisse  
 In WPF sind angefügte Ereignisse in bestimmten Funktionsbereichen vorhanden, in denen eine Abstraktion auf Dienst Ebene vorhanden ist, z. b. für die Ereignisse, die von der statischen- <xref:System.Windows.Input.Mouse> Klasse oder der-Klasse aktiviert werden <xref:System.Windows.Controls.Validation> . Klassen, die mit dem Dienst interagieren oder ihn verwenden, können entweder das Ereignis in der Syntax für angefügte Ereignisse verwenden, oder sie können das angefügte Ereignis als Routingereignis darstellen, das Teil davon ist, wie die Klasse die Funktionen des Diensts integriert.  
  
 Obwohl WPF eine Reihe angefügter Ereignisse definiert, sind die Szenarien, in denen Sie das angefügte Ereignis entweder direkt verwenden oder verarbeiten, sehr eingeschränkt. Im Allgemeinen dient das angefügte-Ereignis einem Architektur Zweck, wird aber dann an ein nicht angefügtes (mit einem CLR-Ereignis "Wrapper") geroutetes Ereignis weitergeleitet.  
  
 Beispielsweise kann das zugrunde liegende angefügte Ereignis leichter für <xref:System.Windows.Input.Mouse.MouseDown?displayProperty=nameWithType> jede angegebene behandelt werden <xref:System.Windows.UIElement> , indem <xref:System.Windows.UIElement.MouseDown> auf diese verwendet wird, <xref:System.Windows.UIElement> anstatt mit der angefügten Ereignis Syntax in XAML oder Code umzugehen. Das angefügte Ereignis dient einem Zweck in der Architektur, da es die zukünftige Erweiterung der Eingabegeräte ermöglicht. Das hypothetische Gerät müsste nur eine Erhöhung <xref:System.Windows.Input.Mouse.MouseDown?displayProperty=nameWithType> bewirken, um Maus Eingaben zu simulieren, und es muss nicht von abgeleitet werden <xref:System.Windows.Input.Mouse> . Dieses Szenario beinhaltet jedoch die Code Behandlung der Ereignisse, und die XAML-Behandlung des angefügten Ereignisses ist für dieses Szenario nicht relevant.  
  
<a name="Handling"></a>
## <a name="handling-an-attached-event-in-wpf"></a>Behandeln eines angefügten Ereignisses in WPF  
 Der Prozess für die Behandlung eines angefügten Ereignisses und den von Ihnen geschriebenen Handlercode ist im Grunde derselbe wie für ein Routingereignis.  
  
 Im Allgemeinen unterscheidet sich ein angefügtes WPF-Ereignis nicht stark von einem WPF-Routing Ereignis. Die Unterschiede sind die Art und Weise, wie das Ereignis generiert wird und wie es von einer Klasse als Member verfügbar gemacht wird (was sich auch auf die XAML-HandlerSyntax auswirkt).  
  
 Wie bereits erwähnt, sind die vorhandenen WPF-angefügten Ereignisse jedoch nicht besonders für die Handhabung in WPF vorgesehen. Der Zweck des Ereignisses ist häufiger das Aktivieren eines zusammengesetzten Elements, um den Status an ein übergeordnetes Element in Zusammensetzung zu melden. In diesem Fall wird das Ereignis in der Regel im Code ausgelöst und beruht auf Klassenbehandlung in der entsprechenden übergeordneten Klasse. Beispielsweise wird erwartet, dass Elemente innerhalb eines <xref:System.Windows.Controls.Primitives.Selector> das angefügte- <xref:System.Windows.Controls.Primitives.Selector.Selected> Ereignis, d. h. eine von der-Klasse behandelte Klasse <xref:System.Windows.Controls.Primitives.Selector> und dann potenziell von der- <xref:System.Windows.Controls.Primitives.Selector> Klasse in ein anderes Routing Ereignis konvertieren <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> . Weitere Informationen über Routingereignisse und Klassenbehandlung finden Sie unter [Markieren von Routingereignissen als behandelt und Klassenbehandlung](marking-routed-events-as-handled-and-class-handling.md).  
  
<a name="Custom"></a>
## <a name="defining-your-own-attached-events-as-routed-events"></a>Definieren Ihres eigenen angefügten Ereignisses als Routingereignisse  
 Wenn Sie von allgemeinen WPF-Basisklassen ableiten, können Sie Ihre eigenen angefügten Ereignisse implementieren, indem Sie bestimmte Muster Methoden in die Klasse einschließen und Hilfsmethoden verwenden, die bereits in den Basisklassen vorhanden sind.  
  
 Das Muster ist wie folgt:  
  
- Eine Methode, die einen __*EventName*-Handler__ mit zwei Parametern hinzufügt. Der erste Parameter ist die-Instanz, der der Ereignishandler hinzugefügt wird. Der zweite Parameter ist der hinzu zufügende Ereignishandler. Die Methode muss `public` und sein und darf `static` keinen Rückgabewert aufweisen.  
  
- Eine Methode zum __Entfernen des *EventName*-Handlers__ mit zwei Parametern. Der erste Parameter ist die Instanz, aus der der Ereignishandler entfernt wird. Der zweite Parameter ist der Ereignishandler, der entfernt werden soll. Die Methode muss `public` und sein und darf `static` keinen Rückgabewert aufweisen.  
  
 Mit der Add-Accessor-Methode zum __Hinzufügen von Ereignis *Namen*__ wird die XAML-Verarbeitung vereinfacht, wenn Attribute angefügter Ereignishandler für ein Element Die Handler zum __Hinzufügen eines *EventName*-Handlers__ und zum __Entfernen von *EventName*-Handlern__ aktivieren auch den Code Zugriff auf den Ereignishandlerspeicher für das  
  
 Dieses allgemeine Muster ist für die praktische Implementierung in einem Framework noch nicht exakt genug, da jede gegebene XAML-Readerimplementierung unterschiedliche Schemas zum Identifizieren von zugrunde liegenden Ereignissen in der unterstützenden Sprache und Architektur aufweisen kann. Dies ist einer der Gründe, warum WPF angefügte Ereignisse als geroutete Ereignisse implementiert. der Bezeichner, der für ein Ereignis () verwendet werden soll, <xref:System.Windows.RoutedEvent> wird bereits vom WPF-Ereignis System definiert. Außerdem ist das Routing eines Ereignisses eine natürliche Implementierungs Erweiterung auf dem XAML-sprach Ebenenkonzept eines angefügten Ereignisses.  
  
 Die __Add *EventName* Handler__ -Implementierung für ein angefügtes WPF-Ereignis besteht aus dem Aufruf von <xref:System.Windows.UIElement.AddHandler%2A> mit dem Routing Ereignis und dem Handler als Argumente.  
  
 Diese Implementierungsstrategie und das Routing Ereignis System in der Regel schränken die Verarbeitung angefügter Ereignisse auf <xref:System.Windows.UIElement> abgeleitete Klassen oder <xref:System.Windows.ContentElement> abgeleitete Klassen ein, da nur diese Klassen über <xref:System.Windows.UIElement.AddHandler%2A> Implementierungen verfügen.  
  
 Der folgende Code definiert z. b `NeedsCleaning` . das angefügte-Ereignis für die Owner-Klasse `Aquarium` und verwendet dabei die von WPF angefügte Ereignis Strategie, um das angefügte-Ereignis als Routing Ereignis zu deklarieren.  
  
 [!code-csharp[WPFAquariumSln#AECode](~/samples/snippets/csharp/VS_Snippets_Wpf/WPFAquariumSln/CSharp/WPFAquariumObjects/Class1.cs#aecode)]
 [!code-vb[WPFAquariumSln#AECode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WPFAquariumSln/visualbasic/wpfaquariumobjects/class1.vb#aecode)]  
  
 Beachten Sie, dass es sich bei der Methode, die zum Einrichten des Bezeichners für angefügte Ereignis Bezeichner verwendet wird, um <xref:System.Windows.EventManager.RegisterRoutedEvent%2A> dieselbe Methode handelt, mit der ein nicht angefügtes Routing Ereignis registriert wird Angefügte Ereignisse und Routingereignisse werden alle in einem zentralisierten internen Speicher registriert. Diese Implementierung des Ereignisspeichers ermöglicht die konzeptionelle Besonderheit „Ereignisse als Schnittstelle“, die im Artikel [Übersicht über Routingereignisse](routed-events-overview.md) diskutiert wird.  
  
<a name="Raising"></a>
## <a name="raising-a-wpf-attached-event"></a>Auslösen eines angefügten Ereignisses von WPF  
 Es ist in der Regel nicht erforderlich, vorhandene WPF-definierte angefügte Ereignisse aus Ihrem Code zu übernehmen. Diese Ereignisse folgen dem allgemeinen "Service"-Konzeptmodell, und Dienst Klassen wie <xref:System.Windows.Input.InputManager> sind dafür verantwortlich, die Ereignisse zu erhöhen.  
  
 Wenn Sie jedoch ein benutzerdefiniertes angefügtes Ereignis basierend auf dem WPF-Modell mit der Grundlage von angehängten Ereignissen definieren <xref:System.Windows.RoutedEvent> , können Sie verwenden, <xref:System.Windows.UIElement.RaiseEvent%2A> um ein angefügtes-Ereignis aus beliebigen oder zu erhöhen <xref:System.Windows.UIElement> <xref:System.Windows.ContentElement> . Um ein Routing Ereignis (angefügt oder nicht) zu erhöhen, müssen Sie ein bestimmtes Element in der Elementstruktur als Ereignis Quelle deklarieren. Diese Quelle wird als Aufrufer gemeldet <xref:System.Windows.UIElement.RaiseEvent%2A> . Das Element zu bestimmen, welches als die Quelle in der Struktur gemeldet ist, unterliegt Ihrer Verantwortung des Dienstes.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Routingereignisse](routed-events-overview.md)
- [Ausführliche Erläuterung der XAML-Syntax](xaml-syntax-in-detail.md)
- [XAML- und benutzerdefinierte Klassen für WPF](xaml-and-custom-classes-for-wpf.md)
