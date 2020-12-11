---
title: x:Reference-Markuperweiterung
ms.date: 03/30/2017
helpviewer_keywords:
- x:Reference markup extension [XAML Services]
- XAML [XAML Services], x:Reference Markup Extension
- Reference markup extension [XAML Services]
ms.assetid: 2982e68b-d26b-4aa3-826a-34c57a9c5199
ms.openlocfilehash: f06e259893111a436e5afe2df754c3edee326d54
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975374"
---
# <a name="xreference-markup-extension"></a><span data-ttu-id="1084c-102">x:Reference-Markuperweiterung</span><span class="sxs-lookup"><span data-stu-id="1084c-102">x:Reference Markup Extension</span></span>

<span data-ttu-id="1084c-103">Verweist auf eine-Instanz, die an anderer Stelle in XAML-Markup deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="1084c-103">References an instance that is declared elsewhere in XAML markup.</span></span> <span data-ttu-id="1084c-104">Der Verweis bezieht sich auf die eines Elements `x:Name` .</span><span class="sxs-lookup"><span data-stu-id="1084c-104">The reference refers to an element's `x:Name`.</span></span>

## <a name="xaml-attribute-usage"></a><span data-ttu-id="1084c-105">Verwendung von XAML-Attributen</span><span class="sxs-lookup"><span data-stu-id="1084c-105">XAML Attribute Usage</span></span>

```xaml
<object property="{x:Reference instancexName}" .../>
```

## <a name="xaml-object-element-usage"></a><span data-ttu-id="1084c-106">Verwendung von XAML-Objektelementen</span><span class="sxs-lookup"><span data-stu-id="1084c-106">XAML Object Element Usage</span></span>

```xaml
<object>
  <object.property>
    <x:Reference Name="instancexName"/>
  </object.property>
</object>
```

## <a name="xaml-values"></a><span data-ttu-id="1084c-107">XAML-Werte</span><span class="sxs-lookup"><span data-stu-id="1084c-107">XAML Values</span></span>

|||
|-|-|
|`instancexName`|<span data-ttu-id="1084c-108">Der `x:Name` Wert (oder Wert der <xref:System.Windows.Markup.RuntimeNamePropertyAttribute> identifizierten Eigenschaft) der Instanz, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1084c-108">The `x:Name` value (or value of the <xref:System.Windows.Markup.RuntimeNamePropertyAttribute>-identified property) of the referenced instance.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1084c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1084c-109">Remarks</span></span>

<span data-ttu-id="1084c-110">`x:Reference` bietet Unterstützung auf XAML-Sprachebene für ein Element Verweis Konzept, das anderweitig in bestimmten Frameworks wie WPF implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1084c-110">`x:Reference` provides XAML language-level support for an element reference concept that was otherwise implemented in specific frameworks such as WPF.</span></span>

## <a name="xreference-and-wpf"></a><span data-ttu-id="1084c-111">x:Reference und WPF</span><span class="sxs-lookup"><span data-stu-id="1084c-111">x:Reference and WPF</span></span>

<span data-ttu-id="1084c-112">In WPF und XAML 2006 werden Element Verweise durch die Funktion der Bindung auf Frameworkebene adressiert <xref:System.Windows.Data.Binding.ElementName%2A> .</span><span class="sxs-lookup"><span data-stu-id="1084c-112">In WPF and XAML 2006, element references are addressed by the framework-level feature of <xref:System.Windows.Data.Binding.ElementName%2A> binding.</span></span> <span data-ttu-id="1084c-113">Für die meisten WPF-Anwendungen und-Szenarien <xref:System.Windows.Data.Binding.ElementName%2A> sollte die Bindung weiterhin verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1084c-113">For most WPF applications and scenarios, <xref:System.Windows.Data.Binding.ElementName%2A> binding should still be used.</span></span> <span data-ttu-id="1084c-114">Ausnahmen zu dieser allgemeinen Anleitung können Fälle enthalten, in denen Datenkontext oder andere Bereichs Überlegungen vorhanden sind, die die Datenbindung nicht praktikabel machen und bei denen die Markup Kompilierung nicht beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="1084c-114">Exceptions to this general guidance might include cases where there are data context or other scoping considerations that make data binding impractical and where markup compilation is not involved.</span></span>

<span data-ttu-id="1084c-115">`x:Reference` ist ein Konstrukt, das in XAML 2009 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1084c-115">`x:Reference` is a construct defined in XAML 2009.</span></span> <span data-ttu-id="1084c-116">In WPF können Sie XAML 2009-Funktionen verwenden, jedoch nur für XAML, das nicht WPF-markupkompiliert ist.</span><span class="sxs-lookup"><span data-stu-id="1084c-116">In WPF, you can use XAML 2009 features, but only for XAML that is not WPF markup-compiled.</span></span> <span data-ttu-id="1084c-117">Markupkompilierte XAML und die BAML-Form von XAML unterstützen die XAML 2009-Schlüsselwörter und -Funktionen derzeit nicht.</span><span class="sxs-lookup"><span data-stu-id="1084c-117">Markup-compiled XAML and the BAML form of XAML do not currently support the XAML 2009 language keywords and features.</span></span>
