---
title: Descendants (dynamische XElement-Eigenschaft)
ms.date: 10/22/2019
ms.topic: reference
ms.openlocfilehash: 8d14b0a94d1a2028a56f649a574f157264ba50fa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972451"
---
# <a name="descendants-xelement-dynamic-property"></a><span data-ttu-id="338b8-102">Descendants (dynamische XElement-Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="338b8-102">Descendants (XElement dynamic property)</span></span>

<span data-ttu-id="338b8-103">Sucht nach einem Indexer, der zum Abrufen aller Nachfolgerelemente des aktuellen Elements verwendet wird, die dem angegebenen erweiterten Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="338b8-103">Gets an indexer used to retrieve all the descendant elements of the current element that match the specified expanded name.</span></span>

## <a name="syntax"></a><span data-ttu-id="338b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="338b8-104">Syntax</span></span>

```xaml
elem.Descendants[{namespaceName}localName]
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="338b8-105">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="338b8-105">Property value/return value</span></span>

<span data-ttu-id="338b8-106">Indexer des Typs `IEnumerable<XElement> Item(String expandedName)`.</span><span class="sxs-lookup"><span data-stu-id="338b8-106">An indexer of the type `IEnumerable<XElement> Item(String expandedName)`.</span></span> <span data-ttu-id="338b8-107">Dieser Indexer nimmt den erweiterten Namen der angegebenen Nachfolgerelemente und gibt die passenden untergeordneten Elemente in einer <xref:System.Collections.IEnumerable>`<`<xref:System.Xml.Linq.XElement>`>`-Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="338b8-107">This indexer takes the expanded name of the specified descendant elements and returns the matching child elements in an <xref:System.Collections.IEnumerable>`<`<xref:System.Xml.Linq.XElement>`>` collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="338b8-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="338b8-108">Remarks</span></span>

<span data-ttu-id="338b8-109">Diese Eigenschaft ist identisch mit der <xref:System.Xml.Linq.XContainer.Descendants(System.Xml.Linq.XName)?displayProperty=fullName>-Methode der <xref:System.Xml.Linq.XContainer>-Klasse.</span><span class="sxs-lookup"><span data-stu-id="338b8-109">This property is equivalent to the <xref:System.Xml.Linq.XContainer.Descendants(System.Xml.Linq.XName)?displayProperty=fullName> method of the <xref:System.Xml.Linq.XContainer> class.</span></span>

<span data-ttu-id="338b8-110">Die Elemente in der zurückgegebenen Auflistung sind in derselben Reihenfolge aufgeführt wie im XML-Quelldokument.</span><span class="sxs-lookup"><span data-stu-id="338b8-110">The elements in the returned collection are in XML source document order.</span></span>

<span data-ttu-id="338b8-111">Diese Eigenschaft verwendet die verzögerte Ausführung.</span><span class="sxs-lookup"><span data-stu-id="338b8-111">This property uses deferred execution.</span></span>

## <a name="see-also"></a><span data-ttu-id="338b8-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="338b8-112">See also</span></span>

- [<span data-ttu-id="338b8-113">Dynamische Eigenschaften der XElement-Klasse</span><span class="sxs-lookup"><span data-stu-id="338b8-113">XElement class dynamic properties</span></span>](attribute-xelement-dynamic-property.md)
- [<span data-ttu-id="338b8-114">Elemente</span><span class="sxs-lookup"><span data-stu-id="338b8-114">Elements</span></span>](elements-xelement-dynamic-property.md)
