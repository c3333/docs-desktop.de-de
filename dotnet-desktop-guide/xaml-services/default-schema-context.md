---
title: Standard-XAML-Schemakontext und WPF-XAML-Schemakontext
ms.date: 03/30/2017
ms.assetid: 04e06a15-09b3-4210-9bdf-9a64c2eccb83
ms.openlocfilehash: 2e92372de61230a98a02282cc28fc3f479cd94eb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978119"
---
# <a name="default-xaml-schema-context-and-wpf-xaml-schema-context"></a>Standard-XAML-Schemakontext und WPF-XAML-Schemakontext
Ein XAML-Schema Kontext ist eine konzeptionelle Entität, die qualifiziert, wie eine XAML-Produktion mit einem bestimmten XAML-Vokabular mit dem Schreibverhalten des Objekts interagiert, einschließlich der Auflösung der Typzuordnung, der Art und Weise, wie Assemblys geladen werden, wie bestimmte Reader-und Writer-Einstellungen interpretiert werden In diesem Thema werden die Funktionen von .net XAML-Diensten und der zugeordnete XAML-Standardschema Kontext beschrieben, der auf dem CLR-Typsystem basiert. In diesem Thema wird auch der XAML-Schema Kontext beschrieben, der für WPF verwendet wird.

## <a name="default-xaml-schema-context"></a>XAML-Standard Schema Kontext

.Net XAML-Dienste implementieren und verwenden einen standardmäßigen XAML-Schema Kontext. Das standardmäßige XAML-Schema Kontext Verhalten ist in der-API der-Klasse nicht immer vollständig sichtbar <xref:System.Xaml.XamlSchemaContext> . In vielen Fällen ist das Verhalten, das der XAML-Standardschema Kontext beeinflusst, durch die gemeinsame API des XAML-Typsystems (z. b. Member von <xref:System.Xaml.XamlMember> oder) <xref:System.Xaml.XamlType> oder durch APIs, die für XAML-Reader und XAML-Writer verfügbar gemacht werden, die den XAML-Standardschema Kontext verwenden, zu beobachten.

Sie können einen erstellen <xref:System.Xaml.XamlSchemaContext> , der das Standardverhalten kapselt, indem Sie den- <xref:System.Xaml.XamlSchemaContext> Konstruktor aufrufen. Dadurch wird explizit der XAML-Standardschema Kontext erstellt. Derselbe XAML-Standardschema Kontext wird implizit erstellt, wenn Sie einen XAML-Reader oder einen XAML-Writer mithilfe von APIs initialisieren, die nicht explizit einen <xref:System.Xaml.XamlSchemaContext> Eingabeparameter akzeptieren.

Der XAML-Standardschema Kontext basiert auf der CLR-Reflektion für das Typmapping-Verhalten. Dies umfasst die Untersuchung der definierenden CLR <xref:System.Type> und der zugehörigen <xref:System.Reflection.PropertyInfo> oder <xref:System.Reflection.MethodInfo> . Außerdem wird die CLR-Zuordnung für Typen oder Member verwendet, um die Besonderheiten für XAML-Typ-oder XAML-Element Informationen einzugeben, die den CLR-Unterstützungstyp verwenden. Der standardmäßige XAML-Schema Kontext erfordert keine Typsystem-Erweiterungs Techniken wie z. b. das- `Invoker` Muster, da die erforderlichen Informationen über das CLR-Typsystem verfügbar sind.

Beim Laden von Assemblys basiert der standardmäßige XAML-Schema Kontext hauptsächlich auf assemblywerten, die in XAML-Namespace Zuordnungen bereitgestellt werden. Außerdem <xref:System.Xaml.XamlReaderSettings.LocalAssembly%2A> kann eine Assembly für Szenarien wie das Laden interner Typen in eine Assembly laden.

## <a name="wpf-xaml-schema-context"></a>WPF-XAML-Schema Kontext

Der WPF-XAML-Schema Kontext wird in diesem Thema beschrieben, da die WPF-Implementierung eine interessante Abbildung der Features bietet, die durch Implementieren eines nicht standardmäßigen XAML-Schema Kontexts eingeführt werden können. Außerdem wird das XAML-Schema Kontext Konzept in der WPF-Dokumentation, die WPF-XAML adressiert, nicht sehr ausführlich erläutert. das Verhalten, das der XAML-Schema Kontext ermöglicht, ist möglicherweise nur vollständig verständlich, wenn er in eine Erläuterung der Funktionsweise des XAML-Standardschema Kontexts integriert ist. Der WPF-XAML-Schema Kontext implementiert das folgende Verhalten.

**Such Überschreibungen:** WPF verfügt über einige Inhalts Modelle für XAML, in denen XAML-Inhalts Eigenschaften vorhanden sind, die ohne attributiert funktionieren <xref:System.Windows.Markup.ContentPropertyAttribute> . <xref:System.Xaml.XamlType.LookupContentProperty%2A> über Schreibungen für WPF implementieren dieses Verhalten.

**Verzögerung für WPF-Ausdrücke:** WPF verfügt über mehrere Ausdrucks Klassen, die einen Wert verzögern, bis ein Lauf Zeit Kontext verfügbar ist. Außerdem handelt es sich bei der Vorlagen Erweiterung um ein Laufzeitverhalten, das auf verzögerungstechniken basiert.

**System Such Optimierungen eingeben:** WPF verfügt über ein umfangreiches XAML-Vokabular und-Objektmodell, einschließlich Basisklassenmember-Definitionen, die auf buchstäblich hunderte von WPF-definierten Klassen erben. Außerdem ist WPF selbst auf mehrere Assemblys verteilt. WPF optimiert die Typsuche mithilfe von Nachschlage Tabellen und anderen Techniken. Dies bietet Leistungsverbesserungen im Vergleich zum standardmäßigen XAML-Schema Kontext und seiner CLR-basierten Typsuche. In Fällen, in denen Typen in einer Nachschlage Tabelle nicht vorhanden sind, verwendet das Verhalten XAML-Schema Kontext Techniken, die dem standardmäßigen XAML-Schema Kontext ähneln.

**XamlType-und XamlMember-Erweiterung:** WPF erweitert Eigenschafts Konzepte mit Abhängigkeits Eigenschaften und Ereignis Konzepten mit Routing Ereignissen. Um diesen Konzepten einen besseren Einblick in XAML-Verarbeitungsvorgänge zu verleihen, erweitert WPF <xref:System.Xaml.XamlType> und und <xref:System.Xaml.XamlMember> fügt interne Eigenschaften hinzu, die Eigenschaften von Abhängigkeits Eigenschaften und Routing Ereignissen melden.

### <a name="accessing-the-wpf-xaml-schema-context"></a>Zugreifen auf den WPF-XAML-Schema Kontext

Wenn Sie XAML-Techniken verwenden, die auf WPF oder basieren <xref:System.Windows.Markup.XamlReader?displayProperty=nameWithType> <xref:System.Windows.Markup.XamlWriter?displayProperty=nameWithType> , wird der WPF-XAML-Schema Kontext bereits für diese XAML-Reader-und XAML-Writer-Implementierungen verwendet.

Wenn Sie andere XAML-Reader-oder XAML-Writer-Implementierungen verwenden, die nicht mit dem WPF-XAML-Schema Kontext initialisiert werden, können Sie möglicherweise einen funktionierenden WPF-XAML-Schema Kontext von erhalten <xref:System.Windows.Markup.XamlReader.GetWpfSchemaContext%2A?displayProperty=nameWithType> . Sie können diesen Wert dann als Initialisierung für eine andere API verwenden, die einen verwendet <xref:System.Xaml.XamlSchemaContext> . Beispielsweise können Sie <xref:System.Xaml.XamlXmlReader.%23ctor%2A> für die Initialisierung aufzurufen und den WPF-XAML-Schema Kontext übergeben. Oder Sie können den WPF-XAML-Schema Kontext für XAML-typsystemvorgänge verwenden. Dies kann die Konstruktions Initialisierung eines- <xref:System.Xaml.XamlType> oder- <xref:System.Xaml.XamlMember> oder-Aufrufs einschließen <xref:System.Xaml.XamlSchemaContext.GetXamlType%2A?displayProperty=nameWithType> .

Beachten Sie Folgendes: Wenn Sie auf bestimmte Aspekte von WPF-XAML aus einer reinen XAML-knotenstreamperspektive zugreifen, haben einige der Funktionen des WPF-Frameworks möglicherweise noch nicht reagiert. Beispielsweise werden WPF-Vorlagen für Steuerelemente noch nicht angewendet. Wenn Sie auf eine Eigenschaft zugreifen, die zur Laufzeit möglicherweise mit einer vollständigen visuellen Struktur aufgefüllt ist, wird Ihnen möglicherweise nur ein Eigenschafts Wert angezeigt, der auf eine Vorlage verweist. Der Dienst Kontext, der für WPF-Markup Erweiterungen bereitgestellt wird, ist möglicherweise auch nicht genau, wenn er aus einer anderen Situation als Laufzeitumgebung bereitgestellt wird, und kann beim Schreiben eines Objekt Diagramms zu Ausnahmen führen

## <a name="xaml-and-assembly-loading"></a>XAML und Laden von Assemblys

Das Laden von Assemblys für XAML-und .net XAML-Dienste ist in das CLR-definierte Konzept von integriert <xref:System.AppDomain> . Ein XAML-Schema Kontext interpretiert das Laden von Assemblys oder das Suchen von Typen zur Laufzeit oder Entwurfszeit basierend auf der Verwendung von <xref:System.AppDomain> und anderen Faktoren. Die Logik unterscheidet sich geringfügig abhängig davon, ob der XAML-Code für einen XAML-Reader lose XAML ist, ob XAML von in eine DLL kompiliert wird `XamlBuildTask` oder ob die von WPF generierte BAML ist `PresentationBuildTask` .

Der XAML-Schema Kontext für WPF ist in das WPF-Anwendungsmodell integriert, das wiederum sowie andere Faktoren verwendet, bei denen <xref:System.AppDomain> es sich um WPF-Implementierungsdetails handelt.

#### <a name="xaml-reader-input-loose-xaml"></a>Eingabe von XAML-Reader (lose XAML)

01. Der XAML-Schema Kontext durchläuft die <xref:System.AppDomain> der Anwendung und sucht nach einer bereits geladenen Assembly, die mit allen Aspekten des Namens übereinstimmt, beginnend mit der zuletzt geladenen Assembly. Wenn eine Entsprechung gefunden wird, wird diese Assembly zur Auflösung verwendet.

02. Andernfalls wird eine der folgenden auf der CLR-API basierenden Verfahren <xref:System.Reflection.Assembly> verwendet, um eine Assembly zu laden:

    - Wenn der Name in der Zuordnung qualifiziert ist, wenden Sie <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> auf den qualifizierten Namen an.

    - Wenn der vorherige Schritt fehlschlägt, verwenden Sie den Kurznamen (und das öffentliche Schlüssel Token, falls vorhanden), um aufzurufen <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> .

    - Wenn der Name in der Zuordnung nicht qualifiziert ist, wird aufgerufen <xref:System.Reflection.Assembly.LoadWithPartialName%2A?displayProperty=nameWithType> .

#### <a name="xamlbuildtask"></a>XamlBuildTask

`XamlBuildTask` wird für Windows Communication Foundation (WCF) und Windows Workflow Foundation verwendet.

Beachten Sie, dass Assemblyverweise über `XamlBuildTask` immer voll qualifiziert sind.

1. Ruft <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> den qualifizierten Namen auf.

2. Wenn der vorherige Schritt fehlschlägt, verwenden Sie den Kurznamen (und das öffentliche Schlüssel Token, falls vorhanden), um aufzurufen <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> .

#### <a name="baml-presentationbuildtask"></a>BAML (presentationbuildtask)

Es gibt zwei Aspekte beim Laden von Assemblys für BAML: das Laden der anfänglichen Assembly, die die BAML als Komponente enthält, und das Laden der typunterstützungs-Assemblys für alle Typen, auf die von der BAML-Produktion verwiesen wird.

##### <a name="assembly-load-for-initial-markup"></a>Assemblyauslastung für erstes Markup:

Der Verweis auf die Assembly, aus der das Markup geladen werden soll, ist immer nicht qualifiziert.

1. Der WPF-XAML-Schema Kontext durchläuft die <xref:System.AppDomain> der WPF-Anwendung und sucht nach einer bereits geladenen Assembly, die mit allen Aspekten des Namens übereinstimmt, beginnend mit der zuletzt geladenen Assembly. Wenn eine Entsprechung gefunden wird, wird diese Assembly zur Auflösung verwendet.

2. Wenn der vorherige Schritt fehlschlägt, verwenden Sie den Kurznamen (und das öffentliche Schlüssel Token, falls vorhanden), um aufzurufen <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> .

##### <a name="assembly-references-by-baml-types"></a>Assemblyverweise von BAML-Typen:

Assemblyverweise für Typen, die in der BAML-Produktion verwendet werden, sind immer voll qualifiziert, als Ausgabe der Buildaufgabe.

01. Der WPF-XAML-Schema Kontext durchläuft die <xref:System.AppDomain> der WPF-Anwendung und sucht nach einer bereits geladenen Assembly, die mit allen Aspekten des Namens übereinstimmt, beginnend mit der zuletzt geladenen Assembly. Wenn eine Entsprechung gefunden wird, wird diese Assembly zur Auflösung verwendet.

02. Andernfalls wird eine der folgenden Techniken verwendet, um eine Assembly zu laden:

    - Ruft <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> den qualifizierten Namen auf.
  
    - Wenn eine Kombination aus Kurzname und öffentliches Schlüssel Token der Assembly entspricht, aus der die BAML geladen wurde, verwenden Sie diese Assembly.

    - Verwenden Sie den Kurznamen und das öffentliche Schlüssel Token, um aufzurufen <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> .

## <a name="see-also"></a>Siehe auch

- [Grundlagen zu XAML-Knotenstreamstrukturen und -konzepten](understanding-xaml-node-stream-structures-and-concepts.md)
