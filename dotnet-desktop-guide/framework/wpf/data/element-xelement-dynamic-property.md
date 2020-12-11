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
# <a name="element-xelement-dynamic-property"></a>Element (dynamische XElement-Eigenschaft)

Ermittelt einen Indexer, der zum Abrufen der Instanz des untergeordneten Elements verwendet wird, die dem angegebenen erweiterten Namen entspricht.

## <a name="syntax"></a>Syntax

```xaml
elem.Element[{namespaceName}localName]
```

## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Indexer des Typs `XElement Item(String expandedName)`. Dieser Indexer nimmt einen erweiterten Namensparameter und gibt das zugehörige <xref:System.Xml.Linq.XElement> oder, wenn kein Element mit dem angegebenen Namen existiert, `null` zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft entspricht der <xref:System.Xml.Linq.XContainer.Element%2A>-Methode der <xref:System.Xml.Linq.XContainer?displayProperty=fullName>-Klasse.

## <a name="see-also"></a>Siehe auch

- <xref:System.Xml.Linq.XContainer.Element%2A?displayProperty=fullName>
- [Dynamische Eigenschaften der XElement-Klasse](attribute-xelement-dynamic-property.md)
- [Elemente](elements-xelement-dynamic-property.md)
