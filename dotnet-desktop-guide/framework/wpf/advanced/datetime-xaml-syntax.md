---
title: DateTime-XAML-Syntax
ms.date: 03/30/2017
helpviewer_keywords:
- DateTime XAML syntax [WPF], strings for
- DateTime XAML syntax [WPF], where used
- short date format [WPF], DateTime
- DateTime XAML syntax [WPF]
- DateTime XAML text [WPF]
- DateTime XAML syntax [WPF], format strings for
ms.assetid: 5901710a-609b-40c8-9d65-f0016cd9090b
ms.openlocfilehash: dc7291f09c44f8a0b616bf38c1c90eb92ec906e6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976408"
---
# <a name="datetime-xaml-syntax"></a>DateTime-XAML-Syntax
Einige Steuerelemente, z <xref:System.Windows.Controls.Calendar> . b. und <xref:System.Windows.Controls.DatePicker> , verfügen über Eigenschaften, die den- <xref:System.DateTime> Typ verwenden. Auch wenn Sie in der Regel ein Anfangsdatum oder eine Uhrzeit für diese Steuerelemente im CodeBehind zur Laufzeit angeben, können Sie ein Anfangsdatum oder eine Uhrzeit in XAML angeben. Der WPF-XAML-Parser behandelt die Analyse von <xref:System.DateTime> Werten mithilfe einer integrierten XAML-Text Syntax. In diesem Thema werden die Besonderheiten der <xref:System.DateTime> XAML-Text Syntax beschrieben.  

<a name="where_datetime_xaml_syntax_is_used"></a>
## <a name="when-to-use-datetime-xaml-syntax"></a>Verwenden von DateTime-XAML-Syntax  
 Das Festlegen von Datumsangaben in XAML ist nicht immer erforderlich und möglicherweise auch nicht erwünscht. Beispielsweise können Sie die-Eigenschaft verwenden, <xref:System.DateTime.Now%2A?displayProperty=nameWithType> um ein Datum zur Laufzeit zu initialisieren, oder Sie können alle Datums Anpassungen für einen Kalender im Code-Behind basierend auf Benutzereingaben durchführen. Es gibt jedoch Szenarios, in denen Sie möglicherweise Datumsangaben in einem <xref:System.Windows.Controls.Calendar> und <xref:System.Windows.Controls.DatePicker> in einer Steuerelement Vorlage hart codieren möchten. Die <xref:System.DateTime> XAML-Syntax muss für diese Szenarien verwendet werden.  
  
### <a name="datetime-xaml-syntax-is-a-native-behavior"></a>DateTime-XAML-Syntax als natives Verhalten  
 <xref:System.DateTime> ist eine Klasse, die in den Basisklassen Bibliotheken der CLR definiert ist. Da sich die Basisklassen Bibliotheken auf den Rest der CLR beziehen, ist es nicht möglich, <xref:System.ComponentModel.TypeConverterAttribute> auf die Klasse anzuwenden und einen Typkonverter zu verwenden, um Zeichen folgen aus XAML zu verarbeiten und Sie <xref:System.DateTime> in das Laufzeitobjekt Modell zu konvertieren. Es gibt keine `DateTimeConverter`-Klasse, die das Konvertierungsverhalten ermöglicht. Das in diesem Thema beschriebene Konvertierungsverhalten ist vielmehr ein natives Verhalten im WPF-XAML-Parser.  
  
<a name="format_strings_for_datetime_xaml_syntax"></a>
## <a name="format-strings-for-datetime-xaml-syntax"></a>Formatzeichenfolgen für DateTime-XAML-Syntax  
 Sie können das Format eines <xref:System.DateTime> mit einer Format Zeichenfolge angeben. Formatzeichenfolgen formalisieren die Textsyntax, die zum Erstellen eines Werts verwendet werden kann. <xref:System.DateTime> Werte für die vorhandenen WPF-Steuerelemente verwenden im Allgemeinen nur die Datums Komponenten von <xref:System.DateTime> und nicht die Zeit Komponenten.  
  
 Wenn <xref:System.DateTime> Sie in XAML angeben, können Sie eine beliebige Format Zeichenfolge verwenden.  
  
 Sie können auch Formate und Formatzeichenfolgen verwenden, die in diesem Thema nicht speziell beschrieben werden. Technisch gesehen verwendet der XAML-Code für einen beliebigen Wert, der <xref:System.DateTime> vom WPF-XAML-Parser analysiert und dann analysiert wird, einen internen-Befehl <xref:System.DateTime.Parse%2A?displayProperty=nameWithType> , daher können Sie jede von akzeptierte Zeichenfolge <xref:System.DateTime.Parse%2A?displayProperty=nameWithType> für Ihre XAML-Eingabe verwenden. Weitere Informationen finden Sie unter <xref:System.DateTime.Parse%2A?displayProperty=nameWithType>.  
  
> [!IMPORTANT]
> Die DateTime-XAML-Syntax verwendet immer `en-us` als für die System <xref:System.Globalization.CultureInfo> eigene Konvertierung. Dies wird nicht durch <xref:System.Windows.FrameworkElement.Language%2A> den Wert oder `xml:lang` Wert in der XAML beeinflusst, da die Typkonvertierung auf Attribut Ebene ohne diesen Kontext erfolgt. Versuchen Sie nicht, die hier angezeigten Formatzeichenfolgen aufgrund von kulturellen Abweichungen, wie z. B. der Reihenfolge von Tag und Monat, zu interpolieren. Die hier angezeigten Formatzeichenfolgen sind die genauen Formatzeichenfolgen für die Analyse von XAML unabhängig von anderen Kultureinstellungen.  
  
 In den folgenden Abschnitten werden einige der allgemeinen-Format Zeichenfolgen beschrieben <xref:System.DateTime> .  
  
### <a name="short-date-pattern-d"></a>Kurzes Datumsmuster („d“)  
 Das folgende Beispiel zeigt das kurze Datumsformat für ein <xref:System.DateTime> in XAML:  
  
 `M/d/YYYY`  
  
 Dies ist die einfachste Möglichkeit, alle erforderlichen Informationen für eine typische Verwendung durch WPF-Steuerelemente anzugeben. Eine Beeinflussung durch versehentliche Zeitzonenverschiebungen gegenüber einer Zeitkomponente ist nicht vorhanden. Daher wird dieses Format anderen Formaten vorgezogen.  
  
 Um z.B. das Datum vom 1. Juni 2010 anzugeben, verwenden Sie die folgende Zeichenfolge:  
  
 `3/1/2010`  
  
 Weitere Informationen finden Sie unter <xref:System.Globalization.DateTimeFormatInfo.ShortDatePattern%2A?displayProperty=nameWithType>.  
  
### <a name="sortable-datetime-pattern-s"></a>Sortierbares DateTime-Muster („s“)  
 Der folgende Code zeigt das sortierbare <xref:System.DateTime> Muster in XAML:  
  
 `yyyy'-'MM'-'dd'T'HH':'mm':'ss`  
  
 Um z.B. das Datum vom 1. Juni 2010 anzugeben, verwenden Sie die folgende Zeichenfolge (alle Zeitkomponenten werden mit 0 eingegeben):  
  
 `2010-06-01T000:00:00`  
  
### <a name="rfc1123-pattern-r"></a>RFC1123-Muster („r“)  
 Das RFC1123-Muster ist hilfreich, da es sich um eine Zeichenfolgeneingabe aus anderen Datumsgeneratoren handeln könnte, die aus kulturinvarianten Gründen auch das RFC1123-Muster verwenden. Der folgende Code zeigt das RFC1123- <xref:System.DateTime> Muster in XAML:  
  
 `ddd, dd MMM yyyy HH':'mm':'ss 'UTC'`  
  
 Um z.B. das Datum vom 1. Juni 2010 anzugeben, verwenden Sie die folgende Zeichenfolge (alle Zeitkomponenten werden mit 0 eingegeben):  
  
 `Mon, 01 Jun 2010 00:00:00 UTC`  
  
### <a name="other-formats-and-patterns"></a>Andere Formate und Muster  
 Wie bereits erwähnt, <xref:System.DateTime> kann ein in XAML als eine beliebige Zeichenfolge angegeben werden, die als Eingabe für zulässig ist <xref:System.DateTime.Parse%2A?displayProperty=nameWithType> . Dies schließt andere formalisierte Formate (z. b <xref:System.Globalization.DateTimeFormatInfo.UniversalSortableDateTimePattern%2A> .) und Formate ein, die nicht als bestimmtes Formular formalisiert werden <xref:System.Globalization.DateTimeFormatInfo> . Beispielsweise ist das Formular `YYYY/mm/dd` als Eingabe für zulässig <xref:System.DateTime.Parse%2A?displayProperty=nameWithType> . In diesem Thema werden nicht alle Formate beschrieben, die funktionieren, sondern das kurze Datumsmuster als Standardverfahren empfohlen werden.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über XAML (WPF)](/dotnet/desktop-wpf/fundamentals/xaml)
