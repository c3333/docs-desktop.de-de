---
title: XamlName-Grammatik
ms.date: 03/30/2017
helpviewer_keywords:
- DottedXamlName grammar [XAML Services]
- grammar [XAML Services], DottedXamlName
- grammar [XAML Services], XamlName
- names in XAML [XAML Services]
- XamlName grammar [XAML Services]
ms.assetid: 11e4cada-41d2-494d-9531-0d3df4dfcbe3
ms.openlocfilehash: 484406ff23c60389d71a638cd516c74d8d7edbe5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977950"
---
# <a name="xamlname-grammar"></a>XamlName-Grammatik

Die XamlName-Grammatik ist eine bestimmte Grammatik, die in der XAML-Sprachspezifikation [MS-XAML] definiert ist, die zur einfacheren Wiedergabe hier reproduziert wird.

## <a name="from-the-xaml-specification"></a>Aus der XAML-Spezifikation

Die [MS-XAML]-Spezifikation definiert den Grammatik-XamlName, um den Satz von juristischen symbolischen bezeichmern zu identifizieren, die für Typen und Eigenschaften verwendet werden.

Zeichen folgen Werte vom Typ XamlName müssen der folgenden Grammatik entsprechen:

```xaml
XamlName ::= NameStartChar ( NameChar )*
NameStartChar ::= LetterCharacter | '_'
NameChar ::= NameStartChar | DecimalDigit | CombiningCharacter
LetterCharacter ::= UnicodeLu | UnicodeLl | UnicodeLo | UnicodeLt | UnicodeNl
DecimalDigit ::= UnicodeNd
CombiningCharacter ::= UnicodeMn | UnicodeMc
```

Dabei werden die folgenden allgemeinen Kategoriewerte angenommen, wie in der Unicode-Zeichen Datenbank definiert.

| Unicode-Kategorie   | BESCHREIBUNG                   |
|--------------------|-------------------------------|
| Lu                 | Letter, Uppercase (Buchstabe, Großschreibung)             |
| Ll                 | Letter, Lowercase (Buchstabe, Kleinschreibung)             |
| Lt                 | Letter, Titlecase (Buchstabe, großer Anfangsbuchstabe)             |
| Lm                 | Letter, Modifier (Buchstabe, Modifizierer)              |
| Lo                 | Letter, Other (Buchstabe, andere)                 |
| Mn                 | Markierung, nicht Abstand             |
| Mc                 | Mark, Spacing Combining (Satzzeichen, Kombinationszeichen mit Vorschub)       |
| Nd                 | Zahl, Decimal               |
| Nl                 | Number, Letter (Zahl, Buchstabe)                |

XAML definiert eine zweite Grammatik (DottedXamlName), die für Eigenschafts-und Ereignis qualifizierte Verweise und auch für angefügte Member verwendet wird. Weitere Informationen finden Sie unter <xref:System.Windows.DependencyProperty> und [Übersicht über XAML (WPF)](../net/wpf/fundamentals/xaml.md).

Zeichen folgen Werte vom Typ "DottedXamlName" müssen der folgenden Grammatik entsprechen:

```xaml
DottedXamlName ::= XamlName '.' XamlName
```

## <a name="remarks"></a>Bemerkungen

Die vollständige Spezifikation finden Sie unter [ \[ MS-XAML \] ](/previous-versions/msp-n-p/ff650760(v=pandp.10)).
