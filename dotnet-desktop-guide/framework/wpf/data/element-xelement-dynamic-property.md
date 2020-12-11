---
title: Element (dynamische XElement-Eigenschaft)
ms.date: 10/22/2019
ms.topic: reference
apiname:
- XElement.Element
apitype: Assembly
ms.openlocfilehash: fc0277d0dc38574696f01e6915e5382744345771
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974640"
---
# <a name="element-xelement-dynamic-property"></a><span data-ttu-id="11461-102">Element (dynamische XElement-Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="11461-102">Element (XElement dynamic property)</span></span>

<span data-ttu-id="11461-103">Ermittelt einen Indexer, der zum Abrufen der Instanz des untergeordneten Elements verwendet wird, die dem angegebenen erweiterten Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="11461-103">Gets an indexer used to retrieve the child element instance that corresponds to the specified expanded name.</span></span>

## <a name="syntax"></a><span data-ttu-id="11461-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11461-104">Syntax</span></span>

```xaml
elem.Element[{namespaceName}localName]
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="11461-105">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11461-105">Property value/return value</span></span>

<span data-ttu-id="11461-106">Indexer des Typs `XElement Item(String expandedName)`.</span><span class="sxs-lookup"><span data-stu-id="11461-106">An indexer of the type `XElement Item(String expandedName)`.</span></span> <span data-ttu-id="11461-107">Dieser Indexer nimmt einen erweiterten Namensparameter und gibt das zugehörige <xref:System.Xml.Linq.XElement> oder, wenn kein Element mit dem angegebenen Namen existiert, `null` zurück.</span><span class="sxs-lookup"><span data-stu-id="11461-107">This indexer takes an expanded name parameter and returns the corresponding <xref:System.Xml.Linq.XElement>, or `null` if there is no element with the specified name.</span></span>

## <a name="remarks"></a><span data-ttu-id="11461-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11461-108">Remarks</span></span>

<span data-ttu-id="11461-109">Diese Eigenschaft entspricht der <xref:System.Xml.Linq.XContainer.Element%2A>-Methode der <xref:System.Xml.Linq.XContainer?displayProperty=fullName>-Klasse.</span><span class="sxs-lookup"><span data-stu-id="11461-109">This property is equivalent to <xref:System.Xml.Linq.XContainer.Element%2A> method of the <xref:System.Xml.Linq.XContainer?displayProperty=fullName> class.</span></span>

## <a name="see-also"></a><span data-ttu-id="11461-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11461-110">See also</span></span>

- <xref:System.Xml.Linq.XContainer.Element%2A?displayProperty=fullName>
- [<span data-ttu-id="11461-111">Dynamische Eigenschaften der XElement-Klasse</span><span class="sxs-lookup"><span data-stu-id="11461-111">XElement class dynamic properties</span></span>](attribute-xelement-dynamic-property.md)
- [<span data-ttu-id="11461-112">Elemente</span><span class="sxs-lookup"><span data-stu-id="11461-112">Elements</span></span>](elements-xelement-dynamic-property.md)
