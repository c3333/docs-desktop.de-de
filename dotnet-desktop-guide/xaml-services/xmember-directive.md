---
title: x:Member-Direktive
ms.date: 03/30/2017
ms.assetid: 4d8394ef-644c-4331-b6c5-be855d392980
ms.openlocfilehash: dc3779f05515af744db5a9c47cd56ebf1f56967a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975390"
---
# <a name="xmember-directive"></a><span data-ttu-id="e4bbb-102">x:Member-Direktive</span><span class="sxs-lookup"><span data-stu-id="e4bbb-102">x:Member Directive</span></span>

<span data-ttu-id="e4bbb-103">Deklariert einen XAML-Member im Markup.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-103">Declares a XAML member in markup.</span></span>

## <a name="xaml-object-element-usage"></a><span data-ttu-id="e4bbb-104">Verwendung von XAML-Objektelementen</span><span class="sxs-lookup"><span data-stu-id="e4bbb-104">XAML Object Element Usage</span></span>

```xaml
<object x:Class="className">
  <x:Members>
    <x:Member Name="propertyName"/>
    additionalMembers
  </x:Members>
</object>
```

## <a name="xaml-values"></a><span data-ttu-id="e4bbb-105">XAML-Werte</span><span class="sxs-lookup"><span data-stu-id="e4bbb-105">XAML Values</span></span>

|||
|-|-|
|`className`|<span data-ttu-id="e4bbb-106">Der Name der Sicherungsklasse oder partiellen Klasse für die XAML-Produktion.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-106">Name of the backing class or partial class for the XAML production.</span></span>|
|`memberName`|<span data-ttu-id="e4bbb-107">Der Membername der Eigenschaft, die definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-107">Member name of the property being defined.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e4bbb-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4bbb-108">Remarks</span></span>

<span data-ttu-id="e4bbb-109">In der .net XAML-Dienst Implementierung.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-109">In .NET XAML Services implementation, .</span></span> <span data-ttu-id="e4bbb-110">hat `x:Member` keine direkte Typunterstützung, wird jedoch durch die <xref:System.Windows.Markup.MemberDefinition>-Klasse unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-110">`x:Member` does not have a direct type backing, but is supported by the <xref:System.Windows.Markup.MemberDefinition> class.</span></span> <span data-ttu-id="e4bbb-111">In einem XAML-Knotenstream wird ein `x:Member`-Element als ein Member namens `Member` aus dem XAML-Namespace der XAML-Sprache dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-111">In a XAML node stream, an `x:Member` element is represented as a member named `Member`, from the XAML language XAML namespace.</span></span> <span data-ttu-id="e4bbb-112">Der Member `Member` enthält Attribute gemäß Deklaration durch Markup.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-112">The member `Member` holds attributes as declared by markup.</span></span>

<span data-ttu-id="e4bbb-113">Die Bedeutung von `Name` und `Type` wird nicht auf der Ebene der .net XAML-Dienste zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-113">The meaning of `Name` and `Type` are not assigned at .NET XAML Services level.</span></span> <span data-ttu-id="e4bbb-114">Sie sind im ursprünglichen XAML-Knotenstream als Zeichenfolgenwerte gespeichert, um später gemäß den Regeln interpretiert zu werden, die möglicherweise von bestimmten Frameworks erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-114">They are stored in the initial XAML node stream as string values, to be interpreted later under the rules that might be imposed by specific frameworks.</span></span> <span data-ttu-id="e4bbb-115">Die Bedeutung kann, je nach Implementierung, an der Bedeutung eines XAML-Namens oder eines XAML-Typs ausgerichtet werden oder kann nur in einem Unterstützungstypsystem gültig sein.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-115">The meaning might align to a XAML name and XAML type meaning, or might only be valid in a backing type system, depending on the implementation.</span></span>

<span data-ttu-id="e4bbb-116">Damit eine praktische Verwendung von `x:Members` als Mittel zum Angeben von Memberdefinitionen in Markup unterstützt wird, müssen die Member einer Klasse zugeordnet sein, die geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-116">To support a practical usage of `x:Members` as a means to specify member definitions in markup, the members must be associated with a class that can be modified.</span></span> <span data-ttu-id="e4bbb-117">Das beabsichtigte Modell besteht darin, dass `x:Members` als ein Member eines Typs vorhanden ist, der eine `x:Class` angibt.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-117">The intended model is that `x:Members` exists as a member of a type that specifies an `x:Class`.</span></span> <span data-ttu-id="e4bbb-118">Der Mechanismus zum Zuordnen von Typen und Membern oder zum Erstellen dynamischer Element Definitionen wird jedoch auf der Ebene der .net XAML-Dienste nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-118">However, the mechanism for associating types and members or for producing dynamic member definitions is not supported at .NET XAML Services level.</span></span> <span data-ttu-id="e4bbb-119">Dies wird von einzelnen Frameworks übernommen, die Anwendungsmodelle haben, die Memberdefinitionen von XAML unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-119">This is left to individual frameworks that have application models that support member definitions from XAML.</span></span> <span data-ttu-id="e4bbb-120">In der Regel sind, damit dieses Feature unterstützt wird, MSBUILD-Buildvorgänge erforderlich, die XAML als Markup kompilieren und es als CodeBehind integrieren oder reine Von-XAML-Assemblys generieren.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-120">Typically, MSBUILD build actions that markup-compile the XAML and either integrate it with code-behind or produce pure from-XAML assemblies are needed to support that feature.</span></span>

## <a name="xproperty-for-windows-workflow-foundation"></a><span data-ttu-id="e4bbb-121">x:Property für Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="e4bbb-121">x:Property for Windows Workflow Foundation</span></span>

<span data-ttu-id="e4bbb-122">Für Windows Workflow Foundation definiert `x:Property` die Member einer benutzerdefinierten Aktivität, die vollständig in XAML erstellt ist, oder XAML-definierte dynamische Member für einen Aktivitäts-Designer mit CodeBehind.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-122">For Windows Workflow Foundation, `x:Property` defines the members of a custom activity composed entirely in XAML, or XAML –defined dynamic members for an activity designer with code-behind.</span></span> <span data-ttu-id="e4bbb-123">`x:Class` muss auch für das Stammelement der XAML-Produktion angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-123">`x:Class` must also be specified on the root element of the XAML production.</span></span> <span data-ttu-id="e4bbb-124">Dies ist keine Voraussetzung für die .net XAML-Dienst Ebene, sondern wird eine Anforderung, wenn die XAML-Produktion von den MSBuild-Buildaktionen geladen wird, die benutzerdefinierte Aktivitäten unterstützen, und Windows Workflow Foundation XAML im Allgemeinen.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-124">This is not a requirement at .NET XAML Services level, but becomes a requirement when the XAML production is loaded by the MSBUILD build actions that support custom activities and Windows Workflow Foundation XAML in general.</span></span> <span data-ttu-id="e4bbb-125">Windows Workflow Foundation verwendet nicht den reinen XAML-Typnamen als beabsichtigten Wert für das `x:Property` `Type` Attribut, sondern verwendet stattdessen eine Konvention, die hier nicht dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-125">Windows Workflow Foundation does not use the pure XAML type name as its intended value for the `x:Property` `Type` attribute, and instead uses a convention that is not documented here.</span></span> <span data-ttu-id="e4bbb-126">Weitere Informationen finden Sie unter [DynamicActivity-Erstellung](/previous-versions/dotnet/netframework-4.0/dd807392(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="e4bbb-126">For more information, see [DynamicActivity Creation](/previous-versions/dotnet/netframework-4.0/dd807392(v=vs.100)).</span></span>
