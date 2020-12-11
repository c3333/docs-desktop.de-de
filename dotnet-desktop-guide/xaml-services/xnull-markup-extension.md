---
title: x:Null-Markuperweiterung
ms.date: 03/30/2017
f1_keywords:
- NullExtension
- x:NullExtension
- x:Null
- "Null"
- xNull
helpviewer_keywords:
- Null markup extension in XAML [XAML Services]
- x:Null markup extension [XAML Services]
- XAML [XAML Services], x:Null markup extension
ms.assetid: 2e3ccc21-4996-481d-91b5-3910d8b3bfa3
ms.openlocfilehash: 7f7c4cd44448b6e4e8b8934a63b56b910ce0428a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975376"
---
# <a name="xnull-markup-extension"></a>x:Null-Markuperweiterung

Gibt `null` als Wert für ein XAML-Element an.

## <a name="xaml-attribute-usage"></a>Verwendung von XAML-Attributen

```xaml
<object property="{x:Null}" .../>
```

## <a name="remarks"></a>Bemerkungen

Das Schlüsselwort für einen NULL-Verweis in c# und C++ ist NULL. Das Microsoft Visual Basic-Schlüsselwort für einen NULL-Verweis ist `Nothing` , Sie verwenden jedoch immer `{x:Null}` als XAML-Verwendung, unabhängig davon, welche Code Behind-Sprache Sie der XAML zuordnen.

Die `x:Null` Markup Erweiterung hat keine festleg baren Eigenschaften.

Eine null-Verwendung ist häufig dem XAML-Element zugeordnet, das einen CLR-Wert verfügbar macht <xref:System.Nullable%601> .

Die `x:Null` Markup Erweiterung verwendet, wie alle XAML-Markup Erweiterungen, die geschweiften Klammern (), um `{,}` die Behandlung von Attributwerten als Literale oder ereignishandlerverweise zu vermeiden. Die Attribut Syntax ist die Syntax, die in dieser Markup Erweiterung am häufigsten verwendet wird. Eine Objekt Element Syntax `<x:Null />` ist technisch möglich, wird jedoch nur selten verwendet, da die `x:Null` Markup Erweiterung keine Positions Parameter oder Konstruktions Argumente aufweist.

Weitere Informationen zu Markup Erweiterungen finden Sie unter [Markup Erweiterungen und WPF-XAML](../framework/wpf/advanced/markup-extensions-and-wpf-xaml.md).

In .net XAML-Diensten wird die Behandlung dieser Markup Erweiterung durch die- <xref:System.Windows.Markup.NullExtension> Klasse definiert.

## <a name="wpf-usage-notes"></a>Hinweise zur WPF-Verwendung

Beachten Sie, dass `null` nicht notwendigerweise der anfängliche nicht festgelegte Wert für eine Verweistyp-Abhängigkeits Eigenschaft ist. Der anfängliche Standardwert kann für jede Abhängigkeits Eigenschaft variieren und kann auf Eigenschafts spezifischen Metadaten basieren. Viele Abhängigkeits Eigenschaften akzeptieren `null` aufgrund ihrer Validierungs Rückruf Implementierungen nicht als Wert, entweder durch Markup oder Code. Weitere Informationen zu Abhängigkeitseigenschaften finden Sie unter [Übersicht über Abhängigkeitseigenschaften](../framework/wpf/advanced/dependency-properties-overview.md).

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.DependencyProperty.UnsetValue>
- [Übersicht über XAML (WPF)](../net/wpf/fundamentals/xaml.md)
- [Markuperweiterungen und WPF-XAML](../framework/wpf/advanced/markup-extensions-and-wpf-xaml.md)
