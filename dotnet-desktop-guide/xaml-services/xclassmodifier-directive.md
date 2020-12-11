---
title: x:ClassModifier-Anweisung
ms.date: 03/30/2017
f1_keywords:
- xClassModifier
- x:ClassModifier
- ClassModifier
helpviewer_keywords:
- XAML [XAML Services], x:ClassModifier attribute
- x:ClassModifier attribute [XAML Services]
- ClassModifier attribute in XAML [XAML Services]
ms.assetid: ef30ab78-d334-4668-917d-c9f66c3b6aea
ms.openlocfilehash: 2d795ad1caa766d21ea98e5a97c98304067cbef1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975405"
---
# <a name="xclassmodifier-directive"></a><span data-ttu-id="612e2-102">x:ClassModifier-Anweisung</span><span class="sxs-lookup"><span data-stu-id="612e2-102">x:ClassModifier Directive</span></span>

<span data-ttu-id="612e2-103">Ändert das XAML-Kompilierungs Verhalten, wenn `x:Class` ebenfalls bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="612e2-103">Modifies XAML compilation behavior when `x:Class` is also provided.</span></span> <span data-ttu-id="612e2-104">Anstatt eine partielle zu erstellen, die `class` über eine `Public` Zugriffsebene (Standardeinstellung) verfügt, wird der bereitgestellte `x:Class` mit einer `NotPublic` Zugriffsebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="612e2-104">Specifically, instead of creating a partial `class` that has a `Public` access level (the default), the provided `x:Class` is created with a `NotPublic` access level.</span></span> <span data-ttu-id="612e2-105">Dieses Verhalten wirkt sich auf die Zugriffsebene für die-Klasse in den generierten Assemblys aus.</span><span class="sxs-lookup"><span data-stu-id="612e2-105">This behavior affects the access level for the class in the generated assemblies.</span></span>

## <a name="xaml-attribute-usage"></a><span data-ttu-id="612e2-106">Verwendung von XAML-Attributen</span><span class="sxs-lookup"><span data-stu-id="612e2-106">XAML Attribute Usage</span></span>

```xaml
<object x:Class="namespace.classname" x:ClassModifier="NotPublic">
   ...
</object>
```

## <a name="xaml-values"></a><span data-ttu-id="612e2-107">XAML-Werte</span><span class="sxs-lookup"><span data-stu-id="612e2-107">XAML Values</span></span>

|||
|-|-|
|<span data-ttu-id="612e2-108">*NotPublic*</span><span class="sxs-lookup"><span data-stu-id="612e2-108">*NotPublic*</span></span>|<span data-ttu-id="612e2-109">Die genaue Zeichenfolge, die an <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> übergeben <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> werden soll, und variiert abhängig von der verwendeten Programmiersprache Code-Behind.</span><span class="sxs-lookup"><span data-stu-id="612e2-109">The exact string to pass to specify <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> versus <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> varies, depending on the code-behind programming language that you use.</span></span> <span data-ttu-id="612e2-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="612e2-110">See Remarks.</span></span>|

## <a name="dependencies"></a><span data-ttu-id="612e2-111">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="612e2-111">Dependencies</span></span>

<span data-ttu-id="612e2-112">[x:Class](xclass-directive.md) muss auch für dasselbe Element bereitgestellt werden, und dieses Element muss das Stamm Element in einer Seite sein.</span><span class="sxs-lookup"><span data-stu-id="612e2-112">[x:Class](xclass-directive.md) must also be provided on the same element, and that element must be the root element in a page.</span></span> <span data-ttu-id="612e2-113">Weitere Informationen finden Sie im [ \[ Abschnitt zu MS-XAML \] 4.3.1.8](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="612e2-113">For more information, see [\[MS-XAML\] Section 4.3.1.8](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

## <a name="remarks"></a><span data-ttu-id="612e2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="612e2-114">Remarks</span></span>

<span data-ttu-id="612e2-115">Der Wert von `x:ClassModifier` in der .net XAML-Dienste-Verwendung variiert je nach Programmiersprache.</span><span class="sxs-lookup"><span data-stu-id="612e2-115">The value of `x:ClassModifier` in .NET XAML Services usage varies by programming language.</span></span> <span data-ttu-id="612e2-116">Die zu verwendende Zeichenfolge hängt davon ab, wie die jeweilige Sprache implementiert <xref:System.CodeDom.Compiler.CodeDomProvider> , und die Typkonverter, die zurückgegeben werden, um die Bedeutung für und zu definieren <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="612e2-116">The string to use depends on how each language implements its <xref:System.CodeDom.Compiler.CodeDomProvider> and the type converters it returns to define the meanings for <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> and <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType>, and whether that language is case sensitive.</span></span>

- <span data-ttu-id="612e2-117">Für c# ist die Zeichenfolge, die an übergeben werden soll, <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> `internal` .</span><span class="sxs-lookup"><span data-stu-id="612e2-117">For C#, the string to pass to designate <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> is `internal`.</span></span>

- <span data-ttu-id="612e2-118">Bei Microsoft Visual Basic .net ist die Zeichenfolge, die an übergeben werden soll, <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> `Friend` .</span><span class="sxs-lookup"><span data-stu-id="612e2-118">For Microsoft Visual Basic .NET, the string to pass to designate <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> is `Friend`.</span></span>

- <span data-ttu-id="612e2-119">Für C++/CLI sind keine Ziele vorhanden, die das Kompilieren von XAML unterstützen. Daher ist der zu Übergabe Wert nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="612e2-119">For C++/CLI, no targets exist that support compiling XAML; therefore, the value to pass is unspecified.</span></span>

<span data-ttu-id="612e2-120">Sie können auch <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> ( `public` in c# `Public` in Visual Basic) angeben. die Angabe von <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> ist jedoch nur selten durchgeführt, da <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> bereits das Standardverhalten ist.</span><span class="sxs-lookup"><span data-stu-id="612e2-120">You can also specify <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> (`public` in C#, `Public` in Visual Basic); however, specifying <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> is infrequently done because <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> is already the default behavior.</span></span>

<span data-ttu-id="612e2-121">Andere Werte mit äquivalenten Zugriffs ebeneneinschränkungen für Benutzercode, wie z. b. `private` in c#, sind für nicht relevant, `x:ClassModifier` da in XAML keine Klassen Verweise unterstützt werden und der- <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> Modifizierer daher dieselbe Auswirkung hat.</span><span class="sxs-lookup"><span data-stu-id="612e2-121">Other values with equivalent user code access-level restrictions, such as `private` in C#, are not relevant for `x:ClassModifier` because nested class references are not supported in XAML, and therefore, the <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> modifier has the same effect.</span></span>

## <a name="security-notes"></a><span data-ttu-id="612e2-122">Sicherheitshinweise</span><span class="sxs-lookup"><span data-stu-id="612e2-122">Security Notes</span></span>

<span data-ttu-id="612e2-123">Die Zugriffsebene, wie Sie in deklariert `x:ClassModifier` wird, unterliegt weiterhin der Interpretation durch bestimmte Frameworks und deren Funktionen.</span><span class="sxs-lookup"><span data-stu-id="612e2-123">The access level as declared in `x:ClassModifier` is still subject to interpretation by particular frameworks and their capabilities.</span></span> <span data-ttu-id="612e2-124">WPF enthält Funktionen zum Laden und Instanziieren von Typen `x:ClassModifier` , bei denen ist `internal` , wenn auf diese Klasse von einer WPF-Ressource über einen Paket-URI-Verweis verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="612e2-124">WPF includes capabilities to load and instantiate types where `x:ClassModifier` is `internal`, if that class is referenced from a WPF resource through a pack URI reference.</span></span> <span data-ttu-id="612e2-125">In diesem Fall und möglicherweise andere, wie Sie von anderen Frameworks implementiert werden, verlassen sich nicht ausschließlich darauf, dass `x:ClassModifier` alle möglichen instanziierungsversuche blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="612e2-125">As a consequence of this case and potentially others like it implemented by other frameworks, do not rely exclusively on `x:ClassModifier` to block all possible instantiation attempts.</span></span>

## <a name="see-also"></a><span data-ttu-id="612e2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="612e2-126">See also</span></span>

- [<span data-ttu-id="612e2-127">x:Class-Direktive</span><span class="sxs-lookup"><span data-stu-id="612e2-127">x:Class Directive</span></span>](xclass-directive.md)
- [<span data-ttu-id="612e2-128">Code-Behind und XAML in WPF</span><span class="sxs-lookup"><span data-stu-id="612e2-128">Code-Behind and XAML in WPF</span></span>](../framework/wpf/advanced/code-behind-and-xaml-in-wpf.md)
- [<span data-ttu-id="612e2-129">x:FieldModifier-Anweisung</span><span class="sxs-lookup"><span data-stu-id="612e2-129">x:FieldModifier Directive</span></span>](xfieldmodifier-directive.md)
- [<span data-ttu-id="612e2-130">Sicherheit (WPF)</span><span class="sxs-lookup"><span data-stu-id="612e2-130">Security (WPF)</span></span>](../framework/wpf/security-wpf.md)
- [<span data-ttu-id="612e2-131">Aus WPF zu System.Xaml migrierte Typen</span><span class="sxs-lookup"><span data-stu-id="612e2-131">Types Migrated from WPF to System.Xaml</span></span>](../framework/wpf/advanced/types-migrated-from-wpf-to-system.md)
