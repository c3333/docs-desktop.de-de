---
title: Elements (dynamische XElement-Eigenschaft)
ms.date: 10/22/2019
ms.topic: reference
apiname:
- XElement.Elements
apitype: Assembly
ms.openlocfilehash: 812adabd3bfb01fd9313ce3f35e6cb0a5e23344e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972450"
---
# <a name="elements-xelement-dynamic-property"></a>Elements (dynamische XElement-Eigenschaft)

Sucht nach einem Indexer, der zum Abrufen der untergeordneten Elemente des aktuellen Elements verwendet wird, die dem angegebenen erweiterten Namen entsprechen.

## <a name="syntax"></a>Syntax

```xaml
elem.Elements[{namespaceName}localName]
```

## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Indexer des Typs `IEnumerable<XElement> Item(String expandedName)`. Dieser Indexer nimmt den erweiterten Namen des gewünschten untergeordneten Elements und gibt die passenden untergeordneten Elemente in einer <xref:System.Collections.IEnumerable>`<`<xref:System.Xml.Linq.XElement>`>`-Auflistung zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist identisch mit der <xref:System.Xml.Linq.XContainer.Elements(System.Xml.Linq.XName)?displayProperty=fullName>-Methode der <xref:System.Xml.Linq.XContainer>-Klasse.

Die Elemente in der zurückgegebenen Auflistung sind in derselben Reihenfolge aufgeführt wie im XML-Quelldokument.

Diese Eigenschaft verwendet die verzögerte Ausführung.

## <a name="see-also"></a>Siehe auch

- [Dynamische Eigenschaften der XElement-Klasse](attribute-xelement-dynamic-property.md)
- [Element](element-xelement-dynamic-property.md)
- [Nachfolgerelemente](descendants-xelement-dynamic-property.md)
