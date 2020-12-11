---
title: XAML-Namespaces für .net XAML-Dienste
ms.date: 03/30/2017
ms.assetid: e4f15f13-c420-4c1e-aeab-9b6f50212047
ms.openlocfilehash: 2ae57d08fade85c59fea2a54b653a2f775b57415
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976967"
---
# <a name="xaml-namespaces-for-net-xaml-services"></a>XAML-Namespaces für .net XAML-Dienste
Ein XAML-Namespace ist ein Konzept, das die Definition eines XML-Namespace erweitert. Ähnlich wie bei einem XML-Namespace können Sie einen XAML-Namespace mit einem- `xmlns` Attribut im Markup definieren. XAML-Namespaces werden auch im XAML-knotenstream und anderen XAML-Dienste-APIs dargestellt. In diesem Thema wird das XAML-Namespace Konzept definiert, und es wird beschrieben, wie XAML-Namespaces definiert und von XAML-Schema Kontexten und anderen Aspekten von .net XAML-Diensten verwendet werden können.  
  
## <a name="xml-namespace-and-xaml-namespace"></a>XML-Namespace und XAML-Namespace  
 Ein XAML-Namespace ist ein spezieller XML-Namespace, ebenso wie XAML eine spezielle Form von XML ist und das einfache XML-Formular für das Markup verwendet. In Markup deklarieren Sie einen XAML-Namespace und seine Zuordnung über ein Attribut, das `xmlns` auf ein Element angewendet wird. Die- `xmlns` Deklaration kann an demselben Element vorgenommen werden, in dem der XAML-Namespace deklariert ist. Eine XAML-Namespace Deklaration, die an einem Element vorgenommen wird, ist für dieses Element, alle Attribute dieses Elements und alle untergeordneten Elemente dieses Elements gültig. Attribute können einen XAML-Namespace verwenden, der nicht mit dem Element identisch ist, das das Attribut enthält, solange der Attribut Name selbst auf das Präfix als Teil seines Attribut namens im Markup verweist.  
  
 Der Unterschied zwischen einem XAML-Namespace und einem XML-Namespace besteht darin, dass ein XML-Namespace verwendet werden kann, um auf ein Schema zu verweisen oder einfach Entitäten zu unterscheiden. Bei XAML müssen die Typen und Member, die in XAML verwendet werden, letztendlich in Unterstützungs Typen aufgelöst werden, und die XML-Schema Konzepte gelten nicht für diese Funktion. Der XAML-Namespace enthält Informationen, die der XAML-Schema Kontext haben muss, um diese Typzuordnung auszuführen.  
  
## <a name="xaml-namespace-components"></a>XAML-Namespace Komponenten  
 Die XAML-Namespace Definition verfügt über zwei Komponenten: ein Präfix und einen Bezeichner. Jede dieser Komponenten ist vorhanden, wenn ein XAML-Namespace im Markup deklariert wird oder im XAML-Typsystem definiert ist.  
  
 Das Präfix kann eine beliebige Zeichenfolge sein, die [in der Spezifikation "W3C-Namespaces in XML 1,0](https://www.w3.org/TR/REC-xml-names/)" zulässig ist. Gemäß der Konvention sind die Präfixe in der Regel kurze Zeichen folgen, da das Präfix mehrmals in einer typischen Markup Datei wiederholt wird. Bestimmte XAML-Namespaces, die für die Verwendung in mehreren XAML-Implementierungen vorgesehen sind, verwenden bestimmte konventionelle Präfixe. Beispielsweise wird der XAML-Namespace der XAML-Sprache in der Regel mit dem-Präfix zugeordnet `x` . Sie können einen XAML-Standard Namespace definieren, in dem das Präfix nicht in der Definition angegeben ist, aber als leere Zeichenfolge dargestellt wird, wenn Sie definiert oder abgefragt wird by.net XAML Services-API. In der Regel wird der standardmäßige XAML-Namespace absichtlich gewählt, um eine maximierte Menge an Präfix-Markup-Markup durch eine XAML-implementierende Technologie und deren Szenarien und vokabarys zu fördern.  
  
 Der Bezeichner kann eine beliebige Zeichenfolge sein, die [in der Spezifikation der W3C-Namespaces in XML 1,0](https://www.w3.org/TR/REC-xml-names/)zulässig ist. Gemäß der Konvention werden Bezeichner für XML-Namespaces oder XAML-Namespaces häufig in der URI-Form angegeben, in der Regel als ein Protokoll qualifizierter absoluter URI. Häufig werden Versionsinformationen, die ein bestimmtes XAML-Vokabular definieren, als Teil der Pfad Zeichenfolge impliziert. XAML-Namespaces fügen über die XML-URI-Konvention hinaus eine zusätzliche bezeichnerkonvention hinzu. Bei XAML-Namespaces kommuniziert der Bezeichner mit Informationen, die von einem XAML-Schema Kontext benötigt werden, um die Typen aufzulösen, die als Elemente unter diesem XAML-Namespace angegeben werden, oder um Attribute zu Membern aufzulösen.  
  
 Um Informationen an einen XAML-Schema Kontext zu übermitteln, kann der Bezeichner für einen XAML-Namespace weiterhin in der URI-Form vorliegen. In diesem Fall wird der URI jedoch auch als passender Bezeichner in einer bestimmten Assembly oder Liste von Assemblys deklariert. Dies erfolgt in Assemblys durch Zuweisen der Assembly mit <xref:System.Windows.Markup.XmlnsDefinitionAttribute> . Diese Methode, mit der der XAML-Namespace identifiziert und ein CLR-basiertes Typauflösungs Verhalten in der attributierten Assembly unterstützt wird, wird vom standardmäßigen XAML-Schema Kontext in .net XAML-Diensten unterstützt. Im Allgemeinen kann diese Konvention in Fällen verwendet werden, in denen der XAML-Schema Kontext die CLR enthält oder auf dem standardmäßigen XAML-Schema Kontext basiert, der zum Lesen von CLR-Attributen aus CLR-Assemblys erforderlich ist.  
  
 XAML-Namespaces können auch durch eine Konvention identifiziert werden, die einen CLR-Namespace und eine typdefinierende Assembly kommuniziert. Diese Konvention wird in Fällen verwendet, in denen keine <xref:System.Windows.Markup.XmlnsDefinitionAttribute> Zuordnung in den Assemblys vorhanden ist, die Typen enthalten. Diese Konvention ist potenziell komplexer als die URI-Konvention und bietet auch das Potenzial für Mehrdeutigkeit und Duplizierung, da es mehrere Möglichkeiten gibt, auf eine Assembly zu verweisen.  
  
 Die grundlegendste Form eines Bezeichners, der den CLR-Namespace und die assemblykonvention verwendet, lautet wie folgt:  
  
 `clr-namespace:clrnsName; assembly=assemblyShortName`
  
 `clr-namespace:` und `; assembly=` sind literalkomponenten der-Syntax.  
  
 *clrnsname* ist der Zeichen folgen Name, der einen CLR-Namespace identifiziert. Dieser Zeichen folgen Name enthält alle internen Punktzeichen (.), die Hinweise zum CLR-Namespace und seine Beziehung zu anderen CLR-Namespaces bereitstellen.
  
 *AssemblyShortName* ist der Zeichen folgen Name einer Assembly, die Typen definiert, die in XAML nützlich sind. Es wird erwartet, dass die Typen, auf die über den deklarierten XAML-Namespace zugegriffen werden soll, von der Assembly definiert und innerhalb des CLR-Namespace deklariert werden, der von *clrnsname* angegeben wird. Dieser Zeichen folgen Name ähnelt in der Regel den Informationen, die von gemeldet werden <xref:System.Reflection.AssemblyName.Name%2A?displayProperty=nameWithType> .  
  
 Eine vollständigere Definition des CLR-Namespace und der assemblykonvention lautet wie folgt:  
  
 `clr-namespace:clrnsName; assembly=assemblyName`
  
 *AssemblyName* stellt eine beliebige Zeichenfolge dar, die als Eingabe zulässig ist <xref:System.Reflection.Assembly.Load%28System.String%29?displayProperty=nameWithType> . Diese Zeichenfolge kann Kultur, öffentliche Schlüssel oder Versionsinformationen enthalten (Definitionen dieser Konzepte werden im Referenz Thema für definiert <xref:System.Reflection.Assembly> ). COFF-Format und-Beweis (wie von anderen über Ladungen von verwendet <xref:System.Reflection.Assembly.Load%2A> ) sind für das Laden von XAML-Assemblys nicht relevant. alle ladeinformationen müssen als Zeichenfolge dargestellt werden.  
  
 Das Angeben eines öffentlichen Schlüssels für die Assembly ist ein nützliches Verfahren für die XAML-Sicherheit oder das Entfernen möglicher Mehrdeutigkeiten, die vorhanden sein können, wenn Assemblys mit einfachem Namen geladen oder bereits in einem Cache oder einer Anwendungsdomäne vorhanden sind. Weitere Informationen finden Sie unter [XAML-Sicherheitsüberlegungen](security-considerations.md).  
  
## <a name="xaml-namespace-declarations-in-the-xaml-services-api"></a>XAML-Namespace Deklarationen in der XAML-Dienste-API  
 In der XAML-Dienste-API wird eine XAML-Namespace Deklaration durch ein- <xref:System.Xaml.NamespaceDeclaration> Objekt dargestellt. Wenn Sie einen XAML-Namespace im Code deklarieren, nennen Sie den- <xref:System.Xaml.NamespaceDeclaration.%23ctor%28System.String%2CSystem.String%29> Konstruktor. Der `ns` -Parameter und der- `prefix` Parameter werden als Zeichen folgen angegeben. die Eingabe, die für diese Parameter bereitgestellt wird, entspricht der Definition des XAML-Namespace Bezeichners und des XAML-Namespace Präfixes, wie zuvor in diesem Thema beschrieben.  
  
 Wenn Sie XAML-Namespace Informationen als Teil eines XAML-knotenstreams oder eines anderen Zugriffs auf das XAML-Typsystem untersuchen, <xref:System.Xaml.NamespaceDeclaration.Namespace%2A?displayProperty=nameWithType> meldet den XAML-Namespace Bezeichner und <xref:System.Xaml.NamespaceDeclaration.Prefix%2A?displayProperty=nameWithType> meldet das XAML-Namespace Präfix.  
  
 In einem XAML-knotenstream können die XAML-Namespace Informationen als XAML-Knoten angezeigt werden, der der Entität vorangestellt ist, auf die Sie angewendet wird. Dies schließt Fälle ein, bei denen die XAML-Namespace Informationen dem `StartObject` des XAML-Stamm Elements vorausgeht. Weitere Informationen finden Sie unter [Understanding XAML Node Stream Structures and Concepts](understanding-xaml-node-stream-structures-and-concepts.md).  
  
 In vielen Szenarien, in denen die .net XAML Services-API verwendet wird, wird erwartet, dass mindestens eine XAML-Namespace Deklaration vorhanden ist, und die Deklaration muss Informationen enthalten, die von einem XAML-Schema Kontext benötigt werden. Die XAML-Namespaces müssen entweder Assemblys angeben, die geladen werden sollen, oder unterstützen, bestimmte Typen in Namespaces und Assemblys aufzulösen, die bereits vom XAML-Schema Kontext geladen oder bekannt sind.  
  
 Um einen XAML-knotenstream zu generieren, müssen XAML-Typinformationen über den XAML-Schema Kontext verfügbar sein. Die XAML-Typinformationen können nicht bestimmt werden, ohne zuerst den relevanten XAML-Namespace für jeden zu erstellenden Knoten zu ermitteln. An diesem Punkt werden noch keine Instanzen von Typen erstellt, aber der XAML-Schema Kontext muss möglicherweise Informationen aus der definierenden Assembly und dem Sicherungstyp suchen. Um z. b. das Markup zu verarbeiten `<Party><PartyFavor/></Party>` , muss der XAML-Schema Kontext in der Lage sein, den Namen und den Typ von zu bestimmen `ContentProperty` `Party` , und muss daher auch die XAML-Namespace Informationen für `Party` und kennen `PartyFavor` . Im Fall des standardmäßigen XAML-Schema Kontexts meldet die statische Reflektion einen Großteil der XAML-typsysteminformationen, die erforderlich sind, um XAML-Typknoten im knotenstream zu generieren.  
  
 Zum Generieren eines Objekt Diagramms aus einem XAML-knotenstream müssen XAML-Namespace Deklarationen für jedes im ursprünglichen Markup verwendete XAML-Präfix vorhanden sein und im XAML-knotenstream aufgezeichnet werden. An diesem Punkt werden Instanzen erstellt, und es tritt ein echtes typzuordnungsverhalten auf.  
  
 Wenn Sie XAML-Namespace Informationen vorab auffüllen müssen, können Sie in Fällen, in denen der XAML-Namespace, den der XAML-Schema Kontext verwenden soll, nicht im Markup definiert werden. eine Methode, die Sie verwenden können, ist das Deklarieren von XML-Namespace Deklarationen im <xref:System.Xml.XmlParserContext> für eine <xref:System.Xml.XmlReader> . Verwenden Sie diese dann <xref:System.Xml.XmlReader> als Eingabe für einen XAML-Reader-Konstruktor oder <xref:System.Xaml.XamlServices.Load%28System.Xml.XmlReader%29?displayProperty=nameWithType> .  
  
 Zwei weitere APIs, die für die XAML-Namespace Behandlung in .net XAML-Diensten relevant sind, sind die Attribute <xref:System.Windows.Markup.XmlnsDefinitionAttribute> und <xref:System.Windows.Markup.XmlnsPrefixAttribute> . Diese Attribute gelten für Assemblys. <xref:System.Windows.Markup.XmlnsDefinitionAttribute> wird von einem XAML-Schema Kontext verwendet, um eine XAML-Namespace Deklaration zu interpretieren, die einen URI enthält. <xref:System.Windows.Markup.XmlnsPrefixAttribute> wird von Tools verwendet, die XAML ausgeben, sodass ein bestimmter XAML-Namespace mit einem vorhersagbaren Präfix serialisiert werden kann. Weitere Informationen finden Sie unter [XAML-bezogene CLR-Attribute für benutzerdefinierte Typen und Bibliotheken](clr-attributes-with-custom-types-and-libraries.md).  
  
## <a name="see-also"></a>Siehe auch

- [Grundlagen zu XAML-Knotenstreamstrukturen und -konzepten](understanding-xaml-node-stream-structures-and-concepts.md)
