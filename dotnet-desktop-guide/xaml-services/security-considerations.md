---
title: XAML-Sicherheitsüberlegungen
ms.date: 03/30/2017
helpviewer_keywords:
- security [XAML Services], .NET XAML services
- XAML security [XAML Services]
ms.assetid: 544296d4-f38e-4498-af49-c9f4dad28964
ms.openlocfilehash: 1864910b339c74e3033fb4d6d8baebffada1a4f8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978172"
---
# <a name="xaml-security-considerations"></a>Überlegungen zur XAML-Sicherheit

In diesem Artikel werden bewährte Methoden für die Sicherheit in Anwendungen beschrieben, wenn Sie die XAML-und .net XAML-Dienste-API verwenden.

## <a name="untrusted-xaml-in-applications"></a>Nicht vertrauenswürdige XAML in Anwendungen

Im Allgemeinen ist nicht vertrauenswürdiger XAML-Code eine beliebige XAML-Quelle, die von der Anwendung nicht speziell eingeschlossen oder ausgegeben wurde.

XAML, das in `resx` einer vertrauenswürdigen und signierten Assembly in eine Ressource vom Typ kompiliert oder als Ressource gespeichert wird, ist nicht grundsätzlich nicht vertrauenswürdig. Sie können XAML als vertrauenswürdig einstufen, wenn Sie die Assembly als Ganzes vertrauenswürdig einstufen. In den meisten Fällen betreffen Sie nur die Vertrauens Aspekte von Loose XAML, bei dem es sich um eine XAML-Quelle handelt, die Sie aus einem Stream oder anderen e/a-Vorgängen laden. Der Lose XAML-Code ist keine bestimmte Komponente oder Funktion eines Anwendungs Modells mit einer Bereitstellungs-und Paket Erstellungs Infrastruktur. Eine Assembly kann jedoch ein Verhalten implementieren, das das Laden von Loose XAML einschließt.

Bei nicht vertrauenswürdigem XAML sollten Sie es im allgemeinen genauso behandeln wie bei nicht vertrauenswürdigem Code. Verwenden Sie Sandkasten oder andere Metaphern, um zu verhindern, dass möglicherweise nicht vertrauenswürdiger XAML auf ihren vertrauenswürdigen Code zugreift

Die Art von XAML-Funktionen bietet dem XAML das Recht, Objekte zu erstellen und ihre Eigenschaften festzulegen. Diese Funktionen umfassen auch den Zugriff auf Typkonverter, das Mapping und den Zugriff auf Assemblys in der Anwendungsdomäne, die Verwendung von Markup Erweiterungen, `x:Code` Blöcken usw.

Zusätzlich zu den Funktionen auf Sprachebene wird XAML für die Benutzeroberflächen Definition in vielen Technologien verwendet. Das Laden von nicht vertrauenswürdigem XAML kann das Laden einer bösartigen Spoofing-Benutzeroberfläche bedeuten.

## <a name="sharing-context-between-readers-and-writers"></a>Gemeinsame Nutzung von Kontext zwischen Lesern und Writern

Die Architektur der .net XAML-Dienste für XAML-Reader und XAML-Writer erfordert häufig die Freigabe eines XAML-Readers für einen XAML-Writer oder einen freigegebenen XAML-Schema Kontext. Die Freigabe von Objekten oder Kontexten ist möglicherweise erforderlich, wenn Sie XAML-Knoten Schleifen Logik schreiben oder einen benutzerdefinierten Speicherpfad bereitstellen. Geben Sie keine XAML-Reader-Instanzen, keinen standardmäßigen XAML-Schema Kontext oder Einstellungen für XAML-Reader/Writer-Klassen zwischen vertrauenswürdigem und nicht vertrauenswürdigem Code frei.

Die meisten Szenarien und Vorgänge, die das Schreiben von XAML-Objekten für eine CLR-basierte Typunterstützung betreffen, können nur XAML-Standardschema Kontext verwenden. Der standardmäßige XAML-Schema Kontext umfasst nicht explizit Einstellungen, die eine vollständige Vertrauenswürdigkeit gefährden könnten. Es ist daher sicher, den Kontext zwischen vertrauenswürdigen und nicht vertrauenswürdigen XAML-Reader-/schreibkomponenten gemeinsam zu nutzen. Wenn Sie dies jedoch tun, ist es immer noch eine bewährte Vorgehensweise, solche Reader und Writer in separaten Bereichen zu belassen <xref:System.AppDomain> , wobei eine davon speziell für teilweise Vertrauenswürdigkeit gedacht/Sandkasten ist.

## <a name="xaml-namespaces-and-assembly-trust"></a>XAML-Namespaces und assemblyvertrauensstellung

Die grundlegende nicht qualifizierte Syntax und Definition, wie XAML eine benutzerdefinierte XAML-Namespace Zuordnung zu einer Assembly interpretiert, unterscheidet nicht zwischen einer vertrauenswürdigen und nicht vertrauenswürdigen Assembly, die in die Anwendungsdomäne geladen wurde. Daher ist es für eine nicht vertrauenswürdige Assembly technisch möglich, eine beabsichtigte XAML-Namespace Zuordnung einer vertrauenswürdigen Assembly zu spolieren und das deklarierte Objekt und die Eigenschafts Informationen einer XAML-Quelle zu erfassen. Wenn Sie über Sicherheitsanforderungen verfügen, um diese Situation zu vermeiden, sollte die gewünschte XAML-Namespace Zuordnung mithilfe einer der folgenden Verfahren erfolgen:

- Verwenden Sie einen voll qualifizierten Assemblynamen mit starkem Namen in jeder XAML-Namespace Zuordnung, die vom XAML-Code der Anwendung erstellt wurde.

- Beschränken Sie die assemblyzuordnung auf einen festgelegten Satz von Verweisassemblys, indem Sie eine bestimmte <xref:System.Xaml.XamlSchemaContext> für XAML-Reader und XAML-objektwriter erstellen Siehe <xref:System.Xaml.XamlSchemaContext.%23ctor%28System.Collections.Generic.IEnumerable%7BSystem.Reflection.Assembly%7D%29>.

## <a name="xaml-type-mapping-and-type-system-access"></a>XAML-Typzuordnung und typsystemzugriff

XAML unterstützt ein eigenes Typsystem, das in vielerlei Hinsicht ein Peer ist, wie CLR das grundlegende CLR-Typsystem implementiert. Für bestimmte Aspekte des typbewusstseins, bei denen Sie basierend auf den Typinformationen Vertrauens Entscheidungen über einen Typ treffen, sollten Sie jedoch die Typinformationen in den CLR-Unterstützungs Typen zurückstellen. Dies liegt daran, dass einige der spezifischen Berichterstattungs Funktionen des XAML-Typsystems als virtuelle Methoden offen bleiben und daher nicht vollständig unter der Steuerung der ursprünglichen .net XAML-Dienst Implementierungen liegen. Diese Erweiterbarkeits Punkte liegen vor, weil das XAML-Typsystem erweiterbar ist, um der Erweiterbarkeit von XAML selbst und den möglichen Alternativen Typmapping-Strategien gegenüber der standardmäßigen CLR-gestützten Implementierung und dem standardmäßigen XAML-Schema Kontext zu entsprechen. Weitere Informationen finden Sie in den spezifischen Hinweisen zu einigen Eigenschaften von <xref:System.Xaml.XamlType> und <xref:System.Xaml.XamlMember> .

## <a name="see-also"></a>Siehe auch

- <xref:System.Xaml.Permissions.XamlAccessLevel>
