---
title: x:FactoryMethod-Anweisung
ms.date: 03/30/2017
helpviewer_keywords:
- XAML. x:FactoryMethod directive [XAML Services]
- FactoryMethod directive in XAML [XAML Services]
- x:FactoryMethod directive [XAML Services]
ms.assetid: 829bcbdf-5318-4afb-9a03-c310e0d2f23d
ms.openlocfilehash: 5e864b6f5d664b079036a5d915e2f6f81b83639f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975393"
---
# <a name="xfactorymethod-directive"></a><span data-ttu-id="75839-102">x:FactoryMethod-Anweisung</span><span class="sxs-lookup"><span data-stu-id="75839-102">x:FactoryMethod Directive</span></span>
<span data-ttu-id="75839-103">Gibt eine andere Methode als einen Konstruktor an, der von einem XAML-Prozessor zum Initialisieren eines Objekts nach der Auflösung des Unterstützungs Typs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="75839-103">Specifies a method other than a constructor that a XAML processor should use to initialize an object after resolving its backing type.</span></span>  
  
## <a name="xaml-attribute-usage-no-xarguments"></a><span data-ttu-id="75839-104">Verwendung von XAML-Attributen, keine x:Arguments</span><span class="sxs-lookup"><span data-stu-id="75839-104">XAML Attribute Usage, no x:Arguments</span></span>  
  
```xaml  
<object x:FactoryMethod="methodname"...>  
  ...  
</object>  
```  
  
## <a name="xaml-attribute-usage-xarguments-as-elements"></a><span data-ttu-id="75839-105">Verwendung von XAML-Attributen, x:Arguments als Element (e)</span><span class="sxs-lookup"><span data-stu-id="75839-105">XAML Attribute Usage, x:Arguments as Element(s)</span></span>  
  
```xaml  
<object x:FactoryMethod="methodname"...>  
  <x:Arguments>  
    oneOrMoreObjectElements  
  </x:Arguments>  
</object>  
```  
  
## <a name="xaml-values"></a><span data-ttu-id="75839-106">XAML-Werte</span><span class="sxs-lookup"><span data-stu-id="75839-106">XAML Values</span></span>  
  
|||  
|-|-|  
|`methodname`|<span data-ttu-id="75839-107">Der Name der Zeichen folgen Methode einer Methode, die XAML-Prozessoren aufruft, um die Instanz zu initialisieren, die als angegeben wird `object` .</span><span class="sxs-lookup"><span data-stu-id="75839-107">The string method name of a method that XAML processors call to initialize the instance specified as `object`.</span></span> <span data-ttu-id="75839-108">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="75839-108">See Remarks.</span></span>|  
|`oneOrMoreObjectElements`|<span data-ttu-id="75839-109">Ein oder mehrere Objekt Elemente für-Objekte, die factorymethodenparameter angeben.</span><span class="sxs-lookup"><span data-stu-id="75839-109">One or more object elements for objects that specify factory method parameters.</span></span> <span data-ttu-id="75839-110">Die Reihenfolge ist wichtig. Sie gibt die Reihenfolge an, in der Argumente an die Factorymethode geleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75839-110">Order is significant; it signifies the order in which arguments should be passed to the factory method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="75839-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75839-111">Remarks</span></span>  
 <span data-ttu-id="75839-112">Wenn `methodname` eine Instanzmethode ist, kann Sie nicht qualifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="75839-112">If `methodname` is an instance method, it cannot be qualified.</span></span>  
  
 <span data-ttu-id="75839-113">Statische Methoden als Factorymethoden werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75839-113">Static methods as factory methods are supported.</span></span> <span data-ttu-id="75839-114">Wenn `methodname` eine statische Methode ist, `methodname` wird als Kombination bereitgestellt `typeName.methodName` , wobei `typeName` die Klasse benennt, die die statische Factorymethode definiert.</span><span class="sxs-lookup"><span data-stu-id="75839-114">If `methodname` is a static method, `methodname` is provided as a `typeName.methodName` combination, where `typeName` names the class that defines the static factory method.</span></span> <span data-ttu-id="75839-115">`typeName` kann als Präfix qualifiziert werden, wenn auf einen Typ in einem zugeordneten xmlns verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="75839-115">`typeName` can be prefix-qualified if referring to a type in a mapped xmlns.</span></span> <span data-ttu-id="75839-116">`typeName` kann ein anderer Typ sein als `typeof(object)` .</span><span class="sxs-lookup"><span data-stu-id="75839-116">`typeName` can be a different type than `typeof(object)`.</span></span>  
  
 <span data-ttu-id="75839-117">Die Factorymethode muss eine deklarierte öffentliche Methode des Typs sein, der das relevante Objekt Element unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75839-117">The factory method must be a declared public method of the type that backs the relevant object element.</span></span>  
  
 <span data-ttu-id="75839-118">Die Factorymethode muss eine Instanz zurückgeben, die dem relevanten Objekt zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="75839-118">The factory method must return an instance that is assignable to the relevant object.</span></span> <span data-ttu-id="75839-119">Factorymethoden sollten niemals NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="75839-119">Factory methods should never return null.</span></span>  
  
 <span data-ttu-id="75839-120">`x:Arguments` arbeitet mit einem Prinzip der besten Entsprechung für Signaturen von Factorymethoden.</span><span class="sxs-lookup"><span data-stu-id="75839-120">`x:Arguments` operates on a principle of best match for signatures of factory methods.</span></span> <span data-ttu-id="75839-121">Bei der Übereinstimmung wird die Parameter Anzahl zuerst ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="75839-121">Matching evaluates the parameter count first.</span></span> <span data-ttu-id="75839-122">Wenn mehr als eine mögliche Entsprechung für eine Parameter Anzahl vorhanden ist, wird der Parametertyp ausgewertet und die beste Entsprechung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="75839-122">If there is more than one possible match for a parameter count, parameter type is then evaluated and best match is determined.</span></span> <span data-ttu-id="75839-123">Wenn nach dieser Evaluierungsphase immer noch Mehrdeutigkeit vorliegt, ist das XAML-Prozessor Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="75839-123">If there is still ambiguity after this phase of evaluation, XAML processor behavior is undefined.</span></span>  
  
 <span data-ttu-id="75839-124">Die `x:FactoryMethod` Element Verwendung ist im typischen Sinn nicht die Verwendung von Eigenschafts Elementen, da das direktivenmarkup nicht auf den Typ des enthaltenden Objekt Elements verweist.</span><span class="sxs-lookup"><span data-stu-id="75839-124">The `x:FactoryMethod` element usage is not property element usage in the typical sense, because the directive markup does not reference the containing object element's type.</span></span> <span data-ttu-id="75839-125">Es wird erwartet, dass die Element Verwendung weniger häufig ist als die Attribut Verwendung.</span><span class="sxs-lookup"><span data-stu-id="75839-125">It is expected that element usage is less common than attribute usage.</span></span> <span data-ttu-id="75839-126">`x:Arguments` (entweder Attribut-oder Element Verwendung) kann zusammen mit `x:FactoryMethod` der Verwendung von Elementen verwendet werden, dies wird jedoch nicht speziell in den Verwendungs Abschnitten veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="75839-126">`x:Arguments` (either attribute or element usage) can be used along with `x:FactoryMethod` element usage, but this is not specifically shown in the Usage sections.</span></span>  
  
 <span data-ttu-id="75839-127">`x:FactoryMethod` Da ein Element vor allen anderen Eigenschaften Elementen stehen muss, muss vor allen Elementen `x:Arguments` stehen, die ebenfalls als-Elemente bereitgestellt werden, und vor jedem Text-/InnerText-/Initialisierungstext stehen muss.</span><span class="sxs-lookup"><span data-stu-id="75839-127">`x:FactoryMethod` as an element must precede any other property elements, must precede any `x:Arguments` also provided as elements, and must precede any content/inner text/initialization text.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75839-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75839-128">See also</span></span>

- [<span data-ttu-id="75839-129">x:Arguments-Anweisung</span><span class="sxs-lookup"><span data-stu-id="75839-129">x:Arguments Directive</span></span>](xarguments-directive.md)
