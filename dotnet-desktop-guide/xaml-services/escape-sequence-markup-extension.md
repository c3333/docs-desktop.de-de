---
title: '{} Escapesequenz: Markup Erweiterung'
ms.date: 03/30/2017
f1_keywords:
- '{}'
helpviewer_keywords:
- XAML [XAML Services], quotation mark (")
- '{} escape sequence [XAML Services]'
- XAML [XAML Services], {} escape sequence
- XAML [XAML Services], escape sequence
- quotation mark (") [XAML Services]
- escape sequence [XAML Services]
ms.assetid: 3ce3e2ad-a868-43f9-9c98-b29561cb146e
ms.openlocfilehash: f84243994557d76fa52d72b060a1ba35460e98b0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978117"
---
# <a name="-escape-sequence--markup-extension"></a>{} Escapesequenz/Markup Erweiterung

Stellt die XAML-Escapesequenz für Attributwerte bereit. Die Escapesequenz ermöglicht, dass die nachfolgenden Werte im Attribut als Literale interpretiert werden.

## <a name="xaml-attribute-usage"></a>Verwendung von XAML-Attributen

```xaml
<object property="{} literalValue" .../>
```

## <a name="xaml-property-element-usage"></a>Verwendung von XAML-Eigenschaftenelementen

```xaml
<object>
  <object.property>
    {} literalValue
  </object.property>
</object>
```

## <a name="xaml-values"></a>XAML-Werte

|||
|-|-|
|*LiteralValue*|Die Literale Zeichenfolge, die der Escapesequenz folgt. In der Regel enthält diese Zeichenfolge eine öffnende oder schließende geschweifter Klammer ({oder}).|

## <a name="remarks"></a>Bemerkungen

Die Escapesequenz ( {} ) wird verwendet, damit eine öffnende geschweifter Klammer ({) als Literalzeichen in XAML verwendet werden kann.

XAML-Reader verwenden normalerweise die öffnende geschweifte Klammer ({), um den Einstiegspunkt einer Markup Erweiterung anzugeben. Allerdings wird zuerst das nächste Zeichen überprüft, um zu bestimmen, ob es sich um eine schließende geschweifte Klammer (}) handelt. Nur wenn die beiden geschweiften Klammern ( {} ) nebeneinander liegen, gelten Sie als Escapesequenz.

Wenn die Escapesequenz gefunden wird, sollte der XAML-Reader den Rest der Zeichenfolge als Zeichenfolge verarbeiten. Wenn jedoch die Escapesequenz auf einen Member angewendet wird, der über einen Typkonverter verfügt, kann die Zeichenfolge die Typkonvertierung durchlaufen, wenn Sie von einem XAML-Writer interpretiert wird.

Die Escapesequenz ist keine Markup Erweiterung und wird nicht durch eine-Klasse unterstützt. Dabei handelt es sich jedoch um eine Konvention, die XAML-Reader (einschließlich benutzerdefinierter XAML-Reader) berücksichtigen sollten.

Ein Anführungszeichen (") kann auf diese Weise nicht als Escapesequenz verwendet werden. Wenn Sie ein Anführungszeichen als Eigenschafts Wert für eine nicht Inhalts Eigenschaft festlegen müssen, verwenden Sie die Eigenschafts Element Syntax, und platzieren Sie das Anführungszeichen als Zeichenfolge innerhalb des Property-Elements, oder verwenden Sie eine XML-Zeichen Entität. Bei einer Inhalts Eigenschaft kann es sich bei dem Anführungszeichen um den gesamten Inhalt handeln.

Die Escapesequenz ( {} ) ist häufig erforderlich, wenn ein XML-Typ angegeben wird, der einen Namespace Qualifizierer an einer Position enthalten muss, an der eine XAML-Markup Erweiterung angezeigt werden kann Dieser Speicherort enthält den Anfang eines XAML-Attribut Werts und in einer Markup Erweiterung direkt nach einem Gleichheitszeichen (=). Das folgende Beispiel zeigt Escapesequenzen für einen XML-Namespace, der am Anfang eines XAML-Attribut Werts angezeigt wird.

[!code-xaml[XLINQExample#StackPanelResources](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml#stackpanelresources)]

## <a name="see-also"></a>Siehe auch

- [Typkonverter und Markuperweiterungen für XAML](type-converters-and-markup-extensions.md)
- [XML-Zeichenentitäten und XAML](xml-character-entities.md)
