---
title: Generics in XAML
ms.date: 03/30/2017
helpviewer_keywords:
- generics [XAML Services]
ms.assetid: 835bfed7-585c-4216-ae67-b674edab8b92
ms.openlocfilehash: 9354f74b978652c36df28a91a6b9db5cfff4bb1e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978114"
---
# <a name="generics-in-xaml"></a>Generics in XAML

.Net XAML-Dienste, die in implementiert sind, <xref:System.Xaml?displayProperty=fullName> unterstützen die Verwendung generischer CLR-Typen. Diese Unterstützung umfasst das Angeben der Einschränkungen von Generika als Typargument und das Erzwingen der Einschränkung durch Aufrufen der entsprechenden `Add` Methode für generische Sammlungs Fälle. In diesem Thema werden Aspekte der Verwendung von und verweisen auf generische Typen in XAML beschrieben.

## <a name="xtypearguments"></a>x:TypeArguments

`x:TypeArguments` ist eine Direktive, die von der XAML-Sprache definiert wird. Wenn Sie als Member eines XAML-Typs verwendet wird, der von einem generischen Typ unterstützt wird, `x:TypeArguments` übergibt einschränkende Typargumente des generischen Typs an den Unterstützungs Konstruktor. Eine Referenz Syntax, die sich auf die .net XAML-Dienste bezieht `x:TypeArguments` , einschließlich Syntax Beispielen, finden Sie unter [x:TypeArguments-Direktive](xtypearguments-directive.md).

Da `x:TypeArguments` eine Zeichenfolge und die Typkonverterunterstützung verwendet, wird Sie in der Regel in der XAML-Verwendung als Attribut deklariert.

Im XAML-knotenstream können die von deklarierten Informationen `x:TypeArguments` aus <xref:System.Xaml.XamlType.TypeArguments%2A?displayProperty=nameWithType> an einer `StartObject` Position im knotenstream abgerufen werden. Der Rückgabewert von <xref:System.Xaml.XamlType.TypeArguments%2A?displayProperty=nameWithType> ist eine Liste von <xref:System.Xaml.XamlType> Werten. Die Bestimmung, ob ein XAML-Typ einen generischen Typ darstellt, kann durch Aufrufen von vorgenommen werden <xref:System.Xaml.XamlType.IsGeneric%2A?displayProperty=nameWithType> .

## <a name="rules-and-syntax-conventions-for-generics-in-xaml"></a>Regeln und Syntax Konventionen für Generika in XAML

In XAML muss ein generischer Typ immer als eingeschränkter generischer Typ dargestellt werden. Im XAML-Typsystem oder in einem XAML-knotenstream ist ein nicht eingeschränkter generischer Typ niemals vorhanden und kann nicht in XAML-Markup dargestellt werden. In der XAML-Attribut Syntax kann auf eine generische verwiesen werden, wenn es sich um eine geschachtelte Typeinschränkung eines generischen handelt, auf das von verwiesen wird `x:TypeArguments` , oder für Fälle, in denen `x:Type` einen CLR-Typverweis für einen generischen Typ bereitstellt. Verweisende Generika werden durch die-Klasse unterstützt, die <xref:System.Xaml.Schema.XamlTypeTypeConverter> von .net XAML-Diensten definiert wird.

Das von aktivierte XAML-Attribut Syntax Formular <xref:System.Xaml.Schema.XamlTypeTypeConverter> ändert die typische MSIL/CLR-Syntax Konvention, die spitzen Klammern für Typen und Einschränkungen von Generika verwendet und stattdessen die Klammern für den Einschränkungs Container ersetzt. Ein Beispiel finden Sie unter [x:TypeArguments-Direktive](xtypearguments-directive.md).

## <a name="generics-and-xaml-2009-features"></a>Generika-und XAML 2009-Features

Wenn Sie XAML 2009 anstelle der Zuordnung der CLR-Basis Typen zum Abrufen von XAML-Typen für allgemeine sprach primitive verwenden, können Sie [XAML 2009-](types-for-primitives.md) Typen als Informationselemente in verwenden `x:TypeArguments` . Sie könnten z. b. Folgendes deklarieren (Präfix Zuordnungen werden nicht angezeigt, aber ist der XAML- `x` sprach-XAML-Namespace für XAML 2009):

```xaml
<my:BusinessObject x:TypeArguments="x:String,x:Int32"/>
```

## <a name="generics-support-in-wpf"></a>Generika Unterstützung in WPF

Bei der Verwendung von XAML 2006 muss [x:Class](xclass-directive.md) auch für das gleiche Element wie angegeben werden, `x:TypeArguments` und dieses Element muss das Stamm Element in einem XAML-Dokument sein. Das root-Element muss einem generischen Typ mit mindestens einem Typargument zugeordnet werden. z. B. <xref:System.Windows.Navigation.PageFunction%601>.

Mögliche Problem Umgehungen zur Unterstützung generischer Verwendungen sind das Definieren einer benutzerdefinierten Markup Erweiterung, die generische Typen zurückgeben kann, oder das Bereitstellen einer Wrapping Klassendefinition, die von einem generischen Typ abgeleitet ist, aber die generische Einschränkung in der eigenen Klassendefinition vereinfacht.

In WPF können Sie XAML 2009-Funktionen zusammen mit verwenden `x:TypeArguments` , jedoch nur für Loose XAML (XAML, das nicht Markup kompiliert ist). Markupkompilierte XAML für WPF und die BAML-Form von XAML unterstützen die XAML 2009-Schlüsselwörter und -Funktionen derzeit nicht.

Benutzerdefinierte Workflows in Windows Workflow Foundation für .NET Framework 3,5 unterstützen keine generische XAML-Verwendung.

## <a name="see-also"></a>Siehe auch

- [x:TypeArguments-Anweisung](xtypearguments-directive.md)
- [x:Class-Direktive](xclass-directive.md)
- [Integrierte Typen für häufige XAML-Sprachprimitive](types-for-primitives.md)
