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
# <a name="-escape-sequence--markup-extension"></a><span data-ttu-id="8059c-102">{} Escapesequenz/Markup Erweiterung</span><span class="sxs-lookup"><span data-stu-id="8059c-102">{} Escape sequence / markup extension</span></span>

<span data-ttu-id="8059c-103">Stellt die XAML-Escapesequenz für Attributwerte bereit.</span><span class="sxs-lookup"><span data-stu-id="8059c-103">Provides the XAML escape sequence for attribute values.</span></span> <span data-ttu-id="8059c-104">Die Escapesequenz ermöglicht, dass die nachfolgenden Werte im Attribut als Literale interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="8059c-104">The escape sequence allows the subsequent values in the attribute to be interpreted as a literal.</span></span>

## <a name="xaml-attribute-usage"></a><span data-ttu-id="8059c-105">Verwendung von XAML-Attributen</span><span class="sxs-lookup"><span data-stu-id="8059c-105">XAML Attribute Usage</span></span>

```xaml
<object property="{} literalValue" .../>
```

## <a name="xaml-property-element-usage"></a><span data-ttu-id="8059c-106">Verwendung von XAML-Eigenschaftenelementen</span><span class="sxs-lookup"><span data-stu-id="8059c-106">XAML Property Element Usage</span></span>

```xaml
<object>
  <object.property>
    {} literalValue
  </object.property>
</object>
```

## <a name="xaml-values"></a><span data-ttu-id="8059c-107">XAML-Werte</span><span class="sxs-lookup"><span data-stu-id="8059c-107">XAML Values</span></span>

|||
|-|-|
|<span data-ttu-id="8059c-108">*LiteralValue*</span><span class="sxs-lookup"><span data-stu-id="8059c-108">*literalValue*</span></span>|<span data-ttu-id="8059c-109">Die Literale Zeichenfolge, die der Escapesequenz folgt.</span><span class="sxs-lookup"><span data-stu-id="8059c-109">The literal string that follows the escape sequence.</span></span> <span data-ttu-id="8059c-110">In der Regel enthält diese Zeichenfolge eine öffnende oder schließende geschweifter Klammer ({oder}).</span><span class="sxs-lookup"><span data-stu-id="8059c-110">Typically this string contains an open or close brace ({ or }).</span></span>|

## <a name="remarks"></a><span data-ttu-id="8059c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8059c-111">Remarks</span></span>

<span data-ttu-id="8059c-112">Die Escapesequenz ( {} ) wird verwendet, damit eine öffnende geschweifter Klammer ({) als Literalzeichen in XAML verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8059c-112">The escape sequence ({}) is used so that an open brace ({) can be used as a literal character in XAML.</span></span>

<span data-ttu-id="8059c-113">XAML-Reader verwenden normalerweise die öffnende geschweifte Klammer ({), um den Einstiegspunkt einer Markup Erweiterung anzugeben. Allerdings wird zuerst das nächste Zeichen überprüft, um zu bestimmen, ob es sich um eine schließende geschweifte Klammer (}) handelt.</span><span class="sxs-lookup"><span data-stu-id="8059c-113">XAML readers typically use the open brace ({) to denote the entry point of a markup extension; however, they first check the next character to determine whether it is a closing brace (}).</span></span> <span data-ttu-id="8059c-114">Nur wenn die beiden geschweiften Klammern ( {} ) nebeneinander liegen, gelten Sie als Escapesequenz.</span><span class="sxs-lookup"><span data-stu-id="8059c-114">Only when the two braces ({}) are adjacent, are they considered an escape sequence.</span></span>

<span data-ttu-id="8059c-115">Wenn die Escapesequenz gefunden wird, sollte der XAML-Reader den Rest der Zeichenfolge als Zeichenfolge verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8059c-115">If the escape sequence is encountered, the XAML reader should process the remainder of the string as a string.</span></span> <span data-ttu-id="8059c-116">Wenn jedoch die Escapesequenz auf einen Member angewendet wird, der über einen Typkonverter verfügt, kann die Zeichenfolge die Typkonvertierung durchlaufen, wenn Sie von einem XAML-Writer interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="8059c-116">However, if the escape sequence is applied to a member that has a type converter, the string might undergo type conversion when it is interpreted by a XAML writer.</span></span>

<span data-ttu-id="8059c-117">Die Escapesequenz ist keine Markup Erweiterung und wird nicht durch eine-Klasse unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8059c-117">The escape sequence is not a markup extension and is not backed by a class.</span></span> <span data-ttu-id="8059c-118">Dabei handelt es sich jedoch um eine Konvention, die XAML-Reader (einschließlich benutzerdefinierter XAML-Reader) berücksichtigen sollten.</span><span class="sxs-lookup"><span data-stu-id="8059c-118">However, it is a convention that XAML readers (including custom XAML readers) should respect.</span></span>

<span data-ttu-id="8059c-119">Ein Anführungszeichen (") kann auf diese Weise nicht als Escapesequenz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8059c-119">A quotation mark (") cannot be used as an escape sequence in this manner.</span></span> <span data-ttu-id="8059c-120">Wenn Sie ein Anführungszeichen als Eigenschafts Wert für eine nicht Inhalts Eigenschaft festlegen müssen, verwenden Sie die Eigenschafts Element Syntax, und platzieren Sie das Anführungszeichen als Zeichenfolge innerhalb des Property-Elements, oder verwenden Sie eine XML-Zeichen Entität.</span><span class="sxs-lookup"><span data-stu-id="8059c-120">If you need to set a quotation mark as a property value for a noncontent property, use property element syntax and place the quotation mark as a string inside the property element, or use an XML character entity.</span></span> <span data-ttu-id="8059c-121">Bei einer Inhalts Eigenschaft kann es sich bei dem Anführungszeichen um den gesamten Inhalt handeln.</span><span class="sxs-lookup"><span data-stu-id="8059c-121">For a content property, the quotation mark can be the entire content.</span></span>

<span data-ttu-id="8059c-122">Die Escapesequenz ( {} ) ist häufig erforderlich, wenn ein XML-Typ angegeben wird, der einen Namespace Qualifizierer an einer Position enthalten muss, an der eine XAML-Markup Erweiterung angezeigt werden kann</span><span class="sxs-lookup"><span data-stu-id="8059c-122">The escape sequence ({}) is frequently required when specifying an XML type that must include a namespace qualifier in a location where a XAML markup extension might appear.</span></span> <span data-ttu-id="8059c-123">Dieser Speicherort enthält den Anfang eines XAML-Attribut Werts und in einer Markup Erweiterung direkt nach einem Gleichheitszeichen (=).</span><span class="sxs-lookup"><span data-stu-id="8059c-123">This location includes the start of a XAML attribute value, and in a markup extension immediately after an equal sign (=).</span></span> <span data-ttu-id="8059c-124">Das folgende Beispiel zeigt Escapesequenzen für einen XML-Namespace, der am Anfang eines XAML-Attribut Werts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8059c-124">The following example shows escape sequences for an XML namespace that appears at the start of a XAML attribute value.</span></span>

[!code-xaml[XLINQExample#StackPanelResources](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml#stackpanelresources)]

## <a name="see-also"></a><span data-ttu-id="8059c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8059c-125">See also</span></span>

- [<span data-ttu-id="8059c-126">Typkonverter und Markuperweiterungen für XAML</span><span class="sxs-lookup"><span data-stu-id="8059c-126">Type Converters and Markup Extensions for XAML</span></span>](type-converters-and-markup-extensions.md)
- [<span data-ttu-id="8059c-127">XML-Zeichenentitäten und XAML</span><span class="sxs-lookup"><span data-stu-id="8059c-127">XML Character Entities and XAML</span></span>](xml-character-entities.md)
