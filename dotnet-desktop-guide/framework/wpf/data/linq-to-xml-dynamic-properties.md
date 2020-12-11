---
title: Dynamische Eigenschaften LINQ to XML Referenz
ms.date: 10/22/2019
ms.topic: reference
ms.openlocfilehash: ca3684716f9b562d0e6a006c26730a1d1a28f8b1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975960"
---
# <a name="linq-to-xml-dynamic-properties"></a><span data-ttu-id="cfa23-102">Dynamische Eigenschaften in LINQ to XML</span><span class="sxs-lookup"><span data-stu-id="cfa23-102">LINQ to XML dynamic properties</span></span>

<span data-ttu-id="cfa23-103">Dieser Abschnitt enthält Referenzinformationen zu den dynamischen Eigenschaften in LINQ to XML.</span><span class="sxs-lookup"><span data-stu-id="cfa23-103">This section provides reference information about the dynamic properties in LINQ to XML.</span></span> <span data-ttu-id="cfa23-104">Diese Eigenschaften werden von den Klassen <xref:System.Xml.Linq.XAttribute> und <xref:System.Xml.Linq.XElement>im <xref:System.Xml.Linq>-Namespace verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="cfa23-104">Specifically, these properties are exposed by the <xref:System.Xml.Linq.XAttribute> and <xref:System.Xml.Linq.XElement> classes, which are in the <xref:System.Xml.Linq> namespace.</span></span>

<span data-ttu-id="cfa23-105">Wie im Artikel [Übersicht über die WPF-Datenbindung mit LINQ to XML](wpf-data-binding-with-linq-to-xml-overview.md) erläutert, gibt es für jede dynamische Eigenschaft in derselben Klasse eine entsprechende öffentliche Standardeigenschaft oder -methode.</span><span class="sxs-lookup"><span data-stu-id="cfa23-105">As explained in the topic [Overview of WPF data binding with LINQ to XML](wpf-data-binding-with-linq-to-xml-overview.md), each of the dynamic properties is equivalent to a standard public property or method in the same class.</span></span> <span data-ttu-id="cfa23-106">Diese Standardmember können für die Mehrzahl der Fälle eingesetzt werden. Die dynamischen Eigenschaften werden speziell für LINQ to XML-Datenbindungsszenarios bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cfa23-106">These standard members should be used for most purposes; dynamic properties are provided specifically for LINQ to XML data binding scenarios.</span></span> <span data-ttu-id="cfa23-107">Weitere Informationen zu den Standardmembern dieser Klassen finden Sie in den Referenzthemen zu den Klassen <xref:System.Xml.Linq.XAttribute> und <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="cfa23-107">For more information about the standard members of these classes, see the <xref:System.Xml.Linq.XAttribute> and <xref:System.Xml.Linq.XElement> reference topics.</span></span>

<span data-ttu-id="cfa23-108">Die dynamischen Eigenschaften in diesem Abschnitt lassen sich hinsichtlich ihrer aufgelösten Werte in zwei Kategorien einteilen:</span><span class="sxs-lookup"><span data-stu-id="cfa23-108">With respect to their resolved values, the dynamic properties in this section fall into two categories:</span></span>

- <span data-ttu-id="cfa23-109">einfache dynamische Eigenschaften, wie die `Value`-Eigenschaften in den Klassen <xref:System.Xml.Linq.XAttribute> und <xref:System.Xml.Linq.XElement>, die einen einzelnen Wert ergeben</span><span class="sxs-lookup"><span data-stu-id="cfa23-109">Simple ones, such as the `Value` properties in the <xref:System.Xml.Linq.XAttribute> and <xref:System.Xml.Linq.XElement> classes, that resolve to a single value.</span></span>

- <span data-ttu-id="cfa23-110">Indizierte Werte, wie die Eigenschaften [Elements](elements-xelement-dynamic-property.md) und [Descendants](descendants-xelement-dynamic-property.md) der <xref:System.Xml.Linq.XElement>-Klasse, die einen Indexertyp ergeben.</span><span class="sxs-lookup"><span data-stu-id="cfa23-110">Indexed values, such as the [Elements](elements-xelement-dynamic-property.md) and [Descendants](descendants-xelement-dynamic-property.md) properties of <xref:System.Xml.Linq.XElement>, that resolve into an indexer type.</span></span> <span data-ttu-id="cfa23-111">Damit der Indexertyp den gewünschten Wert bzw. die gewünschte Auflistung ergibt, muss ihm ein erweiterter Namensparameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="cfa23-111">For indexer types to be resolved to the desired value or collection, an expanded name parameter must be passed to them.</span></span>

<span data-ttu-id="cfa23-112">Alle dynamischen Eigenschaften, die einen indizierten Wert des Typs <xref:System.Collections.Generic.IEnumerable%601> zurückgeben, arbeiten mit verzögerter Ausführung.</span><span class="sxs-lookup"><span data-stu-id="cfa23-112">All the dynamic properties that return an indexed value of type <xref:System.Collections.Generic.IEnumerable%601> use deferred execution.</span></span> <span data-ttu-id="cfa23-113">Weitere Informationen zur verzögerten Ausführung finden Sie unter [Einführung in LINQ-Abfragen (C#)](/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries).</span><span class="sxs-lookup"><span data-stu-id="cfa23-113">For more information about deferred execution, see [Introduction to LINQ queries (C#)](/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries).</span></span>

## <a name="reference"></a><span data-ttu-id="cfa23-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="cfa23-114">Reference</span></span>

- <xref:System.Xml.Linq>
- <xref:System.Xml.Linq.XElement?displayProperty=fullName>
- <xref:System.Xml.Linq.XAttribute?displayProperty=fullName>

## <a name="see-also"></a><span data-ttu-id="cfa23-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfa23-115">See also</span></span>

- [<span data-ttu-id="cfa23-116">WPF-Datenbindung mit LINQ to XML</span><span class="sxs-lookup"><span data-stu-id="cfa23-116">WPF data binding with LINQ to XML</span></span>](wpf-data-binding-with-linq-to-xml-overview.md)
- [<span data-ttu-id="cfa23-117">Übersicht über WPF-Datenbindung mit LINQ to XML</span><span class="sxs-lookup"><span data-stu-id="cfa23-117">WPF data binding with LINQ to XML overview</span></span>](wpf-data-binding-with-linq-to-xml-overview.md)
- [<span data-ttu-id="cfa23-118">Einführung in LINQ-Abfragen (c#)</span><span class="sxs-lookup"><span data-stu-id="cfa23-118">Introduction to LINQ queries (C#)</span></span>](/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries)
