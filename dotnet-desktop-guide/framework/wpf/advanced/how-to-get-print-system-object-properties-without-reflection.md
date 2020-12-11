---
title: 'Gewusst wie: Abrufen von Drucksystemobjekt-Eigenschaften ohne Reflektion'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- PrintSystemObject [WPF], getting properties
ms.assetid: 43560f28-183d-41c1-b9d1-de7c2552273e
ms.openlocfilehash: bb906dafd98e75708764b5f0f009900719f6a475
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976288"
---
# <a name="how-to-get-print-system-object-properties-without-reflection"></a><span data-ttu-id="02614-102">Gewusst wie: Abrufen von Drucksystemobjekt-Eigenschaften ohne Reflektion</span><span class="sxs-lookup"><span data-stu-id="02614-102">How to: Get Print System Object Properties Without Reflection</span></span>
<span data-ttu-id="02614-103">Die Verwendung von Reflektion zum itemisieren der Eigenschaften (und der Typen dieser Eigenschaften) für ein Objekt kann die Anwendungsleistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="02614-103">Using reflection to itemize the properties (and the types of those properties) on an object can slow application performance.</span></span> <span data-ttu-id="02614-104">Der- <xref:System.Printing.IndexedProperties> Namespace bietet eine Möglichkeit, diese Informationen mithilfe von Reflektion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="02614-104">The <xref:System.Printing.IndexedProperties> namespace provides a means to getting this information with using reflection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="02614-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="02614-105">Example</span></span>  
 <span data-ttu-id="02614-106">Hierfür sind die folgenden Schritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="02614-106">The steps for doing this are as follows.</span></span>  
  
1. <span data-ttu-id="02614-107">Erstellen Sie eine Instanz des Typs.</span><span class="sxs-lookup"><span data-stu-id="02614-107">Create an instance of the type.</span></span> <span data-ttu-id="02614-108">Im folgenden Beispiel ist der Typ der Typ, der im Lieferumfang <xref:System.Printing.PrintQueue> Microsoft .NET Frameworks enthalten ist, aber fast identischer Code sollte für Typen verwendet werden, von denen Sie abgeleitet sind <xref:System.Printing.PrintSystemObject> .</span><span class="sxs-lookup"><span data-stu-id="02614-108">In the example below, the type is the <xref:System.Printing.PrintQueue> type that ships with Microsoft .NET Framework, but nearly identical code should work for types that you derive from <xref:System.Printing.PrintSystemObject>.</span></span>  
  
2. <span data-ttu-id="02614-109">Erstellen Sie einen <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> aus dem des Typs <xref:System.Printing.PrintSystemObject.PropertiesCollection%2A> .</span><span class="sxs-lookup"><span data-stu-id="02614-109">Create a <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> from the type's <xref:System.Printing.PrintSystemObject.PropertiesCollection%2A>.</span></span> <span data-ttu-id="02614-110">Die- <xref:System.Collections.DictionaryEntry.Value%2A> Eigenschaft jedes Eintrags in diesem Wörterbuch ist ein Objekt von einem der Typen, die von abgeleitet werden <xref:System.Printing.IndexedProperties.PrintProperty> .</span><span class="sxs-lookup"><span data-stu-id="02614-110">The <xref:System.Collections.DictionaryEntry.Value%2A> property of each entry in this dictionary is an object of one of the types derived from <xref:System.Printing.IndexedProperties.PrintProperty>.</span></span>  
  
3. <span data-ttu-id="02614-111">Listet die Elemente des Wörterbuchs auf.</span><span class="sxs-lookup"><span data-stu-id="02614-111">Enumerate the members of the dictionary.</span></span> <span data-ttu-id="02614-112">Führen Sie für jeden der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="02614-112">For each of them, do the following.</span></span>  
  
4. <span data-ttu-id="02614-113">Wandeln Sie den Wert jedes Eintrags in um, <xref:System.Printing.IndexedProperties.PrintProperty> und verwenden Sie ihn, um ein-Objekt zu erstellen <xref:System.Printing.IndexedProperties.PrintProperty> .</span><span class="sxs-lookup"><span data-stu-id="02614-113">Up-cast the value of each entry to <xref:System.Printing.IndexedProperties.PrintProperty> and use it to create a <xref:System.Printing.IndexedProperties.PrintProperty> object.</span></span>  
  
5. <span data-ttu-id="02614-114">Gibt den Typ des <xref:System.Printing.IndexedProperties.PrintProperty.Value%2A> der einzelnen-Objekte an <xref:System.Printing.IndexedProperties.PrintProperty> .</span><span class="sxs-lookup"><span data-stu-id="02614-114">Get the type of the <xref:System.Printing.IndexedProperties.PrintProperty.Value%2A> of each of the <xref:System.Printing.IndexedProperties.PrintProperty> object.</span></span>  
  
 [!code-csharp[GetPrintObjectPropertyTypesWithoutReflection#ShowPropertyTypesWithoutReflection](~/samples/snippets/csharp/VS_Snippets_Wpf/GetPrintObjectPropertyTypesWithoutReflection/CSharp/Program.cs#showpropertytypeswithoutreflection)]
 [!code-vb[GetPrintObjectPropertyTypesWithoutReflection#ShowPropertyTypesWithoutReflection](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GetPrintObjectPropertyTypesWithoutReflection/visualbasic/program.vb#showpropertytypeswithoutreflection)]  
  
## <a name="see-also"></a><span data-ttu-id="02614-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02614-115">See also</span></span>

- <xref:System.Printing.IndexedProperties.PrintProperty>
- <xref:System.Printing.PrintSystemObject>
- <xref:System.Printing.IndexedProperties>
- <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>
- <xref:System.Printing.LocalPrintServer>
- <xref:System.Printing.PrintQueue>
- <xref:System.Collections.DictionaryEntry>
- [<span data-ttu-id="02614-116">Dokumente in WPF</span><span class="sxs-lookup"><span data-stu-id="02614-116">Documents in WPF</span></span>](documents-in-wpf.md)
- [<span data-ttu-id="02614-117">Übersicht über das Drucken</span><span class="sxs-lookup"><span data-stu-id="02614-117">Printing Overview</span></span>](printing-overview.md)
