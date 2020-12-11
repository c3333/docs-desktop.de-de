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
# <a name="how-to-get-print-system-object-properties-without-reflection"></a>Gewusst wie: Abrufen von Drucksystemobjekt-Eigenschaften ohne Reflektion
Die Verwendung von Reflektion zum itemisieren der Eigenschaften (und der Typen dieser Eigenschaften) für ein Objekt kann die Anwendungsleistung beeinträchtigen. Der- <xref:System.Printing.IndexedProperties> Namespace bietet eine Möglichkeit, diese Informationen mithilfe von Reflektion zu erhalten.  
  
## <a name="example"></a>Beispiel  
 Hierfür sind die folgenden Schritte erforderlich.  
  
1. Erstellen Sie eine Instanz des Typs. Im folgenden Beispiel ist der Typ der Typ, der im Lieferumfang <xref:System.Printing.PrintQueue> Microsoft .NET Frameworks enthalten ist, aber fast identischer Code sollte für Typen verwendet werden, von denen Sie abgeleitet sind <xref:System.Printing.PrintSystemObject> .  
  
2. Erstellen Sie einen <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> aus dem des Typs <xref:System.Printing.PrintSystemObject.PropertiesCollection%2A> . Die- <xref:System.Collections.DictionaryEntry.Value%2A> Eigenschaft jedes Eintrags in diesem Wörterbuch ist ein Objekt von einem der Typen, die von abgeleitet werden <xref:System.Printing.IndexedProperties.PrintProperty> .  
  
3. Listet die Elemente des Wörterbuchs auf. Führen Sie für jeden der folgenden Schritte aus:  
  
4. Wandeln Sie den Wert jedes Eintrags in um, <xref:System.Printing.IndexedProperties.PrintProperty> und verwenden Sie ihn, um ein-Objekt zu erstellen <xref:System.Printing.IndexedProperties.PrintProperty> .  
  
5. Gibt den Typ des <xref:System.Printing.IndexedProperties.PrintProperty.Value%2A> der einzelnen-Objekte an <xref:System.Printing.IndexedProperties.PrintProperty> .  
  
 [!code-csharp[GetPrintObjectPropertyTypesWithoutReflection#ShowPropertyTypesWithoutReflection](~/samples/snippets/csharp/VS_Snippets_Wpf/GetPrintObjectPropertyTypesWithoutReflection/CSharp/Program.cs#showpropertytypeswithoutreflection)]
 [!code-vb[GetPrintObjectPropertyTypesWithoutReflection#ShowPropertyTypesWithoutReflection](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GetPrintObjectPropertyTypesWithoutReflection/visualbasic/program.vb#showpropertytypeswithoutreflection)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Printing.IndexedProperties.PrintProperty>
- <xref:System.Printing.PrintSystemObject>
- <xref:System.Printing.IndexedProperties>
- <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>
- <xref:System.Printing.LocalPrintServer>
- <xref:System.Printing.PrintQueue>
- <xref:System.Collections.DictionaryEntry>
- [Dokumente in WPF](documents-in-wpf.md)
- [Übersicht über das Drucken](printing-overview.md)
