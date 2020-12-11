---
title: Integrierte Typen für häufige XAML-Sprachprimitive
ms.date: 03/30/2017
helpviewer_keywords:
- XAML language primitives [XAML Services]
- XAML [XAML Services], built-in types
- x:String [XAML Services]
- x:TimeSpan [XAML Services]
- x:Byte [XAML Services]
- x:Double [XAML Services]
- XAML [XAML Services], types
- x:Uri [XAML Services]
- XAML built-in types [XAML Services]
- x:Int64 [XAML Services]
- x:Single [XAML Services]
- x:Int32 [XAML Services]
ms.assetid: 11de2f08-5b95-4989-b5ec-5178eb968184
ms.openlocfilehash: ec0e2a29a191d5057ce66a5f3272d00e92b01bd7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977670"
---
# <a name="built-in-types-for-common-xaml-language-primitives"></a><span data-ttu-id="10d3e-102">Integrierte Typen für häufige XAML-sprach primitive</span><span class="sxs-lookup"><span data-stu-id="10d3e-102">Built-in types for common XAML language primitives</span></span>

<span data-ttu-id="10d3e-103">In XAML 2009 wird die Unterstützung auf XAML-Sprachebene für mehrere Datentypen eingeführt, bei denen es sich um häufig verwendete Primitiven in der Common Language Runtime (CLR) und anderen Programmiersprachen handelt.</span><span class="sxs-lookup"><span data-stu-id="10d3e-103">XAML 2009 introduces XAML language-level support for several data types that are frequently used primitives in the common language runtime (CLR) and in other programming languages.</span></span> <span data-ttu-id="10d3e-104">In XAML 2009 wurde Unterstützung für die folgenden Primitiven hinzugefügt: `x:Object`, `x:Boolean`, `x:Char`, `x:String`, `x:Decimal`, `x:Single`, `x:Double`, `x:Int16`, `x:Int32`, `x:Int64`, `x:TimeSpan`, `x:Uri`, `x:Byte`und `x:Array`</span><span class="sxs-lookup"><span data-stu-id="10d3e-104">XAML 2009 adds support for these primitives: `x:Object`, `x:Boolean`, `x:Char`, `x:String`, `x:Decimal`, `x:Single`, `x:Double`, `x:Int16`, `x:Int32`, `x:Int64`, `x:TimeSpan`, `x:Uri`, `x:Byte`, and `x:Array`</span></span>

## <a name="previous-techniques-for-language-primitives-in-xaml-markup"></a><span data-ttu-id="10d3e-105">Vorherige Techniken für Sprachprimitive in XAML-Markup</span><span class="sxs-lookup"><span data-stu-id="10d3e-105">Previous Techniques for Language Primitives in XAML Markup</span></span>

 <span data-ttu-id="10d3e-106">In XAML für frühere WPF-Versionen konnten Sie durch die Zuordnung der Assembly und des Namespace, die eine CLR-Primitivendefinitionsklasse für .NET Framework enthielten, auf die CLR-Sprachprimitiven verweisen.</span><span class="sxs-lookup"><span data-stu-id="10d3e-106">In XAML for previous WPF versions, you could reference the CLR language primitives by mapping the assembly and namespace that contained a CLR primitive definition class for the .NET Framework.</span></span> <span data-ttu-id="10d3e-107">Die meisten dieser Primitive befinden sich in der mscorlib-Assembly und im <xref:System> -Namespace.</span><span class="sxs-lookup"><span data-stu-id="10d3e-107">Most of these are in the mscorlib assembly and <xref:System> namespace.</span></span> <span data-ttu-id="10d3e-108">Um beispielsweise <xref:System.Int32>zu verwenden, konnten Sie die folgende Zuordnung deklarieren (anschließend folgt eine Beispielverwendung):</span><span class="sxs-lookup"><span data-stu-id="10d3e-108">For example, to use <xref:System.Int32>, you could declare the following mapping (with an example usage shown thereafter):</span></span>

```xaml
<Application xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
xmlns:sys="clr-namespace:System;assembly=mscorlib">
  <Application.Resources>
    <sys:Int32 x:Key="intMeaning">42</sys:Int32>
  </Application.Resources>
</Application>
```

## <a name="xaml-2009-language-primitives"></a><span data-ttu-id="10d3e-109">XAML 2009-Sprachprimitive</span><span class="sxs-lookup"><span data-stu-id="10d3e-109">XAML 2009 Language Primitives</span></span>

<span data-ttu-id="10d3e-110">Gemäß der Konvention werden die Sprachprimitiven für XAML und alle anderen XAML-Sprachelemente mit dem `x:` -Präfix angezeigt.</span><span class="sxs-lookup"><span data-stu-id="10d3e-110">By convention, the language primitives for XAML and all other XAML language elements are shown, including the `x:` prefix.</span></span> <span data-ttu-id="10d3e-111">So werden XAML-Sprachelemente in der Regel in realem Markup verwendet.</span><span class="sxs-lookup"><span data-stu-id="10d3e-111">This is how XAML language elements are typically used in real-world markup.</span></span> <span data-ttu-id="10d3e-112">Diese Konvention gilt in der Begriffsdokumentation für XAML in WPF und auch in der XAML-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="10d3e-112">This convention is followed in the conceptual documentation for XAML in WPF and also in the XAML specification.</span></span>

### <a name="xobject"></a><span data-ttu-id="10d3e-113">x:Object</span><span class="sxs-lookup"><span data-stu-id="10d3e-113">x:Object</span></span>

<span data-ttu-id="10d3e-114">Für CLR-Unterstützung entspricht die `x:Object` -Primitive <xref:System.Object>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-114">For CLR backing, the `x:Object` primitive corresponds to <xref:System.Object>.</span></span>

<span data-ttu-id="10d3e-115">Dieser Primitive wird in der Regel nicht in Anwendungsmarkup verwendet, könnte aber für einige Szenarios nützlich sein, wie z. B. die Überprüfung der Zuweisungsfähigkeit in einem XAML-Typsystem.</span><span class="sxs-lookup"><span data-stu-id="10d3e-115">This primitive is not typically used in application markup, but might be useful for some scenarios such as checking assignability in a XAML type system.</span></span>

### <a name="xboolean"></a><span data-ttu-id="10d3e-116">x:Boolean</span><span class="sxs-lookup"><span data-stu-id="10d3e-116">x:Boolean</span></span>

<span data-ttu-id="10d3e-117">Für CLR-Unterstützung entspricht die `x:Boolean` -Primitive <xref:System.Boolean>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-117">For CLR backing, the `x:Boolean` primitive corresponds to <xref:System.Boolean>.</span></span>

<span data-ttu-id="10d3e-118">Wenn XAML Werte für `x:Boolean` analysiert, wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="10d3e-118">XAML parses values for `x:Boolean` as case insensitive.</span></span> <span data-ttu-id="10d3e-119">Beachten Sie, dass `x:Bool` keine akzeptierte Alternative ist.</span><span class="sxs-lookup"><span data-stu-id="10d3e-119">Note that `x:Bool` is not an accepted alternative.</span></span> <span data-ttu-id="10d3e-120">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.17 und 5.4.11](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-120">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.17 and 5.4.11](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xchar"></a><span data-ttu-id="10d3e-121">x:Char</span><span class="sxs-lookup"><span data-stu-id="10d3e-121">x:Char</span></span>

<span data-ttu-id="10d3e-122">Für CLR-Unterstützung entspricht die `x:Char` -Primitive <xref:System.Char>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-122">For CLR backing, the `x:Char` primitive corresponds to <xref:System.Char>.</span></span>

<span data-ttu-id="10d3e-123">Zeichenfolgen- und Zeichentypen verfügen über Interaktion mit der Gesamtcodierung der Datei auf XML-Ebene.</span><span class="sxs-lookup"><span data-stu-id="10d3e-123">String and char types have interaction with the overall encoding of the file at the XML level.</span></span> <span data-ttu-id="10d3e-124">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.7 und 5.4.1](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-124">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.7 and 5.4.1](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xstring"></a><span data-ttu-id="10d3e-125">x:String</span><span class="sxs-lookup"><span data-stu-id="10d3e-125">x:String</span></span>

<span data-ttu-id="10d3e-126">Für CLR-Unterstützung entspricht die `x:String` -Primitive <xref:System.String>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-126">For CLR backing, the `x:String` primitive corresponds to <xref:System.String>.</span></span>

<span data-ttu-id="10d3e-127">Zeichenfolgen- und Zeichentypen verfügen über Interaktion mit der Gesamtcodierung der Datei auf XML-Ebene.</span><span class="sxs-lookup"><span data-stu-id="10d3e-127">String and char types have interaction with the overall encoding of the file at the XML level.</span></span> <span data-ttu-id="10d3e-128">Die Definition der XAML-Sprachspezifikation finden Sie in den [ \[ Abschnitten zu MS-XAML \] 5.2.6](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-128">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.6](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xdecimal"></a><span data-ttu-id="10d3e-129">x:Decimal</span><span class="sxs-lookup"><span data-stu-id="10d3e-129">x:Decimal</span></span>

<span data-ttu-id="10d3e-130">Für CLR-Unterstützung entspricht die `x:Decimal` -Primitive <xref:System.Decimal>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-130">For CLR backing, the `x:Decimal` primitive corresponds to <xref:System.Decimal>.</span></span>

<span data-ttu-id="10d3e-131">Die XAML-Verarbeitung erfolgt grundsätzlich unter der `en-US` Kultur.</span><span class="sxs-lookup"><span data-stu-id="10d3e-131">XAML parsing is inherently done under `en-US` culture.</span></span> <span data-ttu-id="10d3e-132">Gemäß der `en-US` -Kultur ist das richtige Trennzeichen für die Bestandteile einer Dezimalzahl immer ein Punkt (`.`), und zwar unabhängig von Kultureinstellungen der Entwicklungsumgebung oder dem tatsächlichen Clientziel, in das die XAML zur Laufzeit geladen wird.</span><span class="sxs-lookup"><span data-stu-id="10d3e-132">Under `en-US` culture, the correct separator for the components of a decimal is always a period (`.`) regardless of culture settings of the development environment, or of the eventual client target where the XAML is loaded at run time.</span></span>

<span data-ttu-id="10d3e-133">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.14 und 5.4.8](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-133">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.14 and 5.4.8](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xsingle"></a><span data-ttu-id="10d3e-134">x:Single</span><span class="sxs-lookup"><span data-stu-id="10d3e-134">x:Single</span></span>

<span data-ttu-id="10d3e-135">Für CLR-Unterstützung entspricht die `x:Single` -Primitive <xref:System.Single>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-135">For CLR backing, the `x:Single` primitive corresponds to <xref:System.Single>.</span></span>

<span data-ttu-id="10d3e-136">Zusätzlich zu den numerischen Werten ermöglicht die Textsyntax für `x:Single` auch die `Infinity`-, `-Infinity`- und `NaN`-Token.</span><span class="sxs-lookup"><span data-stu-id="10d3e-136">In addition to the numeric values, text syntax for `x:Single` also permits the tokens `Infinity`, `-Infinity`, and `NaN`.</span></span> <span data-ttu-id="10d3e-137">Bei diesen Token wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="10d3e-137">These tokens are treated as case sensitive.</span></span>

<span data-ttu-id="10d3e-138">`x:Single` kann Werte in wissenschaftlicher Schreibweise unterstützen, wenn das erste Zeichen in der Textsyntax `e` oder `E`ist.</span><span class="sxs-lookup"><span data-stu-id="10d3e-138">`x:Single` can support values in scientific notation form, if the first character in text syntax is `e` or `E`.</span></span>

<span data-ttu-id="10d3e-139">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.8 und 5.4.2](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-139">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.8 and 5.4.2](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xdouble"></a><span data-ttu-id="10d3e-140">x:Double</span><span class="sxs-lookup"><span data-stu-id="10d3e-140">x:Double</span></span>

<span data-ttu-id="10d3e-141">Für CLR-Unterstützung entspricht die `x:Double` -Primitive <xref:System.Double>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-141">For CLR backing, the `x:Double` primitive corresponds to <xref:System.Double>.</span></span>

<span data-ttu-id="10d3e-142">Zusätzlich zu den numerischen Werten ermöglicht die Textsyntax für `x:Double` auch die `Infinity`-, `-Infinity`- und `NaN`-Token.</span><span class="sxs-lookup"><span data-stu-id="10d3e-142">In addition to the numeric values, text syntax for `x:Double` permits the tokens `Infinity`, `-Infinity`, and `NaN`.</span></span> <span data-ttu-id="10d3e-143">Bei diesen Token wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="10d3e-143">These tokens are treated as case sensitive.</span></span>

<span data-ttu-id="10d3e-144">`x:Double` kann Werte in wissenschaftlicher Schreibweise unterstützen.</span><span class="sxs-lookup"><span data-stu-id="10d3e-144">`x:Double` can support values in scientific notation form.</span></span> <span data-ttu-id="10d3e-145">Verwenden Sie das Zeichen `e` oder `E` , um den Exponententeil einzuführen.</span><span class="sxs-lookup"><span data-stu-id="10d3e-145">Use the character `e` or `E` to introduce the exponent portion.</span></span>

<span data-ttu-id="10d3e-146">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.9 und 5.4.3](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-146">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.9 and 5.4.3](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xint16"></a><span data-ttu-id="10d3e-147">x:Int16</span><span class="sxs-lookup"><span data-stu-id="10d3e-147">x:Int16</span></span>

<span data-ttu-id="10d3e-148">Für CLR-Unterstützung entspricht die `x:Int16` -Primitive <xref:System.Int16> , und `x:Int16` wird als signiert behandelt.</span><span class="sxs-lookup"><span data-stu-id="10d3e-148">For CLR backing, the `x:Int16` primitive corresponds to <xref:System.Int16> and `x:Int16` is treated as signed.</span></span> <span data-ttu-id="10d3e-149">In XAML wird das Nichtvorhandensein eines Pluszeichens (`+`) in der Textsyntax als positiv signierter Wert impliziert.</span><span class="sxs-lookup"><span data-stu-id="10d3e-149">In XAML, the absence of a plus (`+`) sign in text syntax is implied as a positive signed value.</span></span>

<span data-ttu-id="10d3e-150">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.11 und 5.4.5](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-150">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.11 and 5.4.5](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xint32"></a><span data-ttu-id="10d3e-151">x:Int32</span><span class="sxs-lookup"><span data-stu-id="10d3e-151">x:Int32</span></span>

<span data-ttu-id="10d3e-152">Für CLR-Unterstützung entspricht die `x:Int32` -Primitive <xref:System.Int32>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-152">For CLR backing, the `x:Int32` primitive corresponds to <xref:System.Int32>.</span></span> <span data-ttu-id="10d3e-153">`x:Int32` wird als signiert behandelt.</span><span class="sxs-lookup"><span data-stu-id="10d3e-153">`x:Int32` is treated as signed.</span></span> <span data-ttu-id="10d3e-154">In XAML wird das Nichtvorhandensein eines Pluszeichens (`+`) in der Textsyntax als positiv signierter Wert impliziert.</span><span class="sxs-lookup"><span data-stu-id="10d3e-154">In XAML, the absence of a plus (`+`) sign in text syntax is implied as a positive signed value.</span></span>

<span data-ttu-id="10d3e-155">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.12 und 5.4.6](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-155">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.12 and 5.4.6](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xint64"></a><span data-ttu-id="10d3e-156">x:Int64</span><span class="sxs-lookup"><span data-stu-id="10d3e-156">x:Int64</span></span>

<span data-ttu-id="10d3e-157">Für CLR-Unterstützung entspricht die `x:Int64` -Primitive <xref:System.Int64>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-157">For CLR backing, the `x:Int64` primitive corresponds to <xref:System.Int64>.</span></span> <span data-ttu-id="10d3e-158">`x:Int64` wird als signiert behandelt.</span><span class="sxs-lookup"><span data-stu-id="10d3e-158">`x:Int64` is treated as signed.</span></span> <span data-ttu-id="10d3e-159">In XAML wird das Nichtvorhandensein eines Pluszeichens (`+`) in der Textsyntax als positiv signierter Wert impliziert.</span><span class="sxs-lookup"><span data-stu-id="10d3e-159">In XAML, the absence of a plus (`+`) sign in text syntax is implied as a positive signed value.</span></span>

<span data-ttu-id="10d3e-160">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.13 und 5.4.7](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-160">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.13 and 5.4.7](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xtimespan"></a><span data-ttu-id="10d3e-161">x:TimeSpan</span><span class="sxs-lookup"><span data-stu-id="10d3e-161">x:TimeSpan</span></span>

<span data-ttu-id="10d3e-162">Für CLR-Unterstützung entspricht die `x:TimeSpan` -Primitive <xref:System.TimeSpan>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-162">For CLR backing, the `x:TimeSpan` primitive corresponds to <xref:System.TimeSpan>.</span></span>

<span data-ttu-id="10d3e-163">Die XAML-Verarbeitung für das Zeit Datumsformat erfolgt grundsätzlich unter der `en-US` Kultur.</span><span class="sxs-lookup"><span data-stu-id="10d3e-163">XAML parsing for time-date format is inherently done under `en-US` culture.</span></span>

<span data-ttu-id="10d3e-164">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.16 und 5.4.10](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-164">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.16 and 5.4.10](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xuri"></a><span data-ttu-id="10d3e-165">x:Uri</span><span class="sxs-lookup"><span data-stu-id="10d3e-165">x:Uri</span></span>

<span data-ttu-id="10d3e-166">Für CLR-Unterstützung entspricht die `x:Uri` -Primitive <xref:System.Uri>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-166">For CLR backing, the `x:Uri` primitive corresponds to <xref:System.Uri>.</span></span>

<span data-ttu-id="10d3e-167">Die Überprüfung auf Protokolle ist nicht Bestandteil der XAML-Definition für `x:Uri`.</span><span class="sxs-lookup"><span data-stu-id="10d3e-167">Checking for protocols is not part of the XAML definition for `x:Uri`.</span></span>

<span data-ttu-id="10d3e-168">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.15 und 5.4.9](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-168">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.15 and 5.4.9](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xbyte"></a><span data-ttu-id="10d3e-169">x:Byte</span><span class="sxs-lookup"><span data-stu-id="10d3e-169">x:Byte</span></span>

<span data-ttu-id="10d3e-170">Für CLR-Unterstützung entspricht die `x:Byte` -Primitive <xref:System.Byte>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-170">For CLR backing, the `x:Byte` primitive corresponds to <xref:System.Byte>.</span></span> <span data-ttu-id="10d3e-171">Eine <xref:System.Byte>  /  `x:Byte` wird als nicht signiert behandelt.</span><span class="sxs-lookup"><span data-stu-id="10d3e-171">A <xref:System.Byte> / `x:Byte` is treated as unsigned.</span></span>

<span data-ttu-id="10d3e-172">Die Definition der XAML-Sprachspezifikation finden Sie unter [ \[ MS-XAML \] -Abschnitte 5.2.10 und 5.4.4](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-172">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.10 and 5.4.4](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

### <a name="xarray"></a><span data-ttu-id="10d3e-173">x:Array</span><span class="sxs-lookup"><span data-stu-id="10d3e-173">x:Array</span></span>

<span data-ttu-id="10d3e-174">Für CLR-Unterstützung entspricht die `x:Array` -Primitive <xref:System.Array>.</span><span class="sxs-lookup"><span data-stu-id="10d3e-174">For CLR backing, the `x:Array` primitive corresponds to <xref:System.Array>.</span></span>

<span data-ttu-id="10d3e-175">In XAML 2006 können Sie ein Array mit einer Markuperweiterungssyntax definieren. Die XAML 2009-Syntax ist dagegen eine sprachdefinierte Primitive, die keinen Zugriff auf eine Markuperweiterung erfordert.</span><span class="sxs-lookup"><span data-stu-id="10d3e-175">You can define an array in XAML 2006  by using a markup extension syntax; however, the XAML 2009 syntax is a language-defined primitive that does not require accessing a markup extension.</span></span> <span data-ttu-id="10d3e-176">Weitere Informationen zur Unterstützung von XAML 2006 finden Sie unter [x:Array Markup Extension](xarray-markup-extension.md).</span><span class="sxs-lookup"><span data-stu-id="10d3e-176">For more information about XAML 2006 support, see [x:Array Markup Extension](xarray-markup-extension.md).</span></span>

<span data-ttu-id="10d3e-177">Die Definition der XAML-Sprachspezifikation finden Sie in den [ \[ Abschnitten zu MS-XAML \] 5.2.18](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span><span class="sxs-lookup"><span data-stu-id="10d3e-177">For the XAML language specification definition, see [\[MS-XAML\] Sections 5.2.18](/previous-versions/msp-n-p/ff650760(v=pandp.10)).</span></span>

## <a name="wpf-support"></a><span data-ttu-id="10d3e-178">WPF-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="10d3e-178">WPF Support</span></span>

<span data-ttu-id="10d3e-179">In WPF können Sie XAML 2009-Funktionen verwenden, jedoch nur für XAML, das nicht markupkompiliert ist.</span><span class="sxs-lookup"><span data-stu-id="10d3e-179">In WPF, you can use XAML 2009 features but only for XAML that is not markup-compiled.</span></span> <span data-ttu-id="10d3e-180">Markupkompilierte XAML für WPF und die BAML-Form von XAML unterstützen die XAML 2009-Schlüsselwörter und -Funktionen derzeit nicht.</span><span class="sxs-lookup"><span data-stu-id="10d3e-180">Markup-compiled XAML for WPF and the BAML form of XAML do not currently support the XAML 2009 keywords and features.</span></span>

<span data-ttu-id="10d3e-181">Ein Szenario, in dem XAML 2009-Funktionen mit WPF verwendet werden können, liegt vor, wenn Sie Loose XAML erstellen und dieses XAML dann mit <xref:System.Windows.Markup.XamlReader.Load%2A?displayProperty=nameWithType>in eine WPF-Laufzeit und ein Objektdiagramm laden.</span><span class="sxs-lookup"><span data-stu-id="10d3e-181">A scenario where you can use XAML 2009 features together with WPF is if you author loose XAML and you then load that XAML into a WPF runtime and object graph with <xref:System.Windows.Markup.XamlReader.Load%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="10d3e-182">Der WPF- <xref:System.Windows.Markup.XamlReader?displayProperty=nameWithType> und sein <xref:System.Windows.Markup.XamlReader.Load%2A> können XAML 2009-Sprachschlüsselwörter und -Funktionen in eine gültige Objektdiagrammdarstellung verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="10d3e-182">The WPF <xref:System.Windows.Markup.XamlReader?displayProperty=nameWithType> and its <xref:System.Windows.Markup.XamlReader.Load%2A> can process XAML 2009 language keywords and features into a valid object graph representation.</span></span>
