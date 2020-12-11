---
title: xml:space-Behandlung in XAML
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [XAML Services], xml:space attribute
- XAML [XAML Services], white-space processing
- xml:space attribute [XAML Services]
- white-space processing [XAML Services]
ms.assetid: 5e1814f0-5b30-43d5-8c88-dede335a89d7
ms.openlocfilehash: b05fb396850316c76721c72276ebb97f7e805ed3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975386"
---
# <a name="xmlspace-handling-in-xaml"></a>xml:space-Behandlung in XAML

Das `xml:space` -Attribut ist ein XML-definiertes Attribut, das das signifikante Verhalten der Leerraum Verarbeitung in einem Object-Element deklariert. Dieses Verhalten ist relevant für den gesamten Inhalt (inneren Text), der in dem Element enthalten `xml:space` ist, in dem deklariert ist, und auch für untergeordnete Elemente.

## <a name="xaml-attribute-usage"></a>Verwendung von XAML-Attributen

```xaml
<object xml:space="preserve" />
```

 \- oder -

```xaml
<object xml:space="default" />
```

## <a name="remarks"></a>Bemerkungen

Die Definition für das- `xml:space` Attribut in XAML, einschließlich der beiden möglichen Werte, wird von abgeleitet, `xml:space` wie von den W3C-Spezifikationen für XML als "spezielles Attribut" definiert.

Der Standardwert des `xml:space` Attributs ist der Literalwert `"default"` . Für den-Wert `"default"` oder, wenn `xml:space` überhaupt nicht angegeben wird, ist das Verhalten der signifikanten leer Raum Verarbeitung die Standardbehandlung, wie im Thema [Leerraum Verarbeitung in XAML](white-space-processing.md)definiert.

Um Leerraum in Objekt Element Inhalt beizubehalten, geben Sie `xml:space="preserve"` für dieses Objekt Element an.

Bei den meisten Interpretationen `xml:space` werden die Attribut Effekte und der Wert des Attributs auf untergeordnete Elemente beschränkt.

Eine vollständige Erläuterung der Leerraum Verarbeitung in XAML finden Sie unter [Leerraum Verarbeitung in XAML](white-space-processing.md).

## <a name="see-also"></a>Siehe auch

- [Leerstellenverarbeitung in XAML](white-space-processing.md)
- [Übersicht über XAML (WPF)](../net/wpf/fundamentals/xaml.md)
