---
title: 'Gewusst wie: Klonen eines Druckers'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- print queues [WPF]
- cloning printers [WPF]
- printers [WPF], cloning
- print queues [WPF], cloning
- cloning print queues [WPF]
ms.assetid: dd6997c9-fe04-40f8-88a6-92e3ac0889eb
ms.openlocfilehash: e6af8d6410c4e383990bdaa27f97cc698be71719
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976934"
---
# <a name="how-to-clone-a-printer"></a>Gewusst wie: Klonen eines Druckers
Die meisten Unternehmen werden zu einem bestimmten Zeitpunkt mehrere Drucker desselben Modells erwerben. Diese werden in der Regel mit praktisch identischen Konfigurationseinstellungen installiert. Die Installation der einzelnen Drucker kann zeitaufwändig und fehleranfällig sein. Der <xref:System.Printing.IndexedProperties?displayProperty=nameWithType> -Namespace und die- <xref:System.Printing.PrintServer.InstallPrintQueue%2A> Klasse, die mit Microsoft .NET Framework verfügbar gemacht werden, ermöglichen es, eine beliebige Anzahl zusätzlicher Druck Warteschlangen, die von einer vorhandenen Druck Warteschlange geklont werden, sofort zu installieren  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine zweite Druck Warteschlange aus einer vorhandenen Druck Warteschlange geklont. Die zweite unterscheidet sich von der ersten nur unter dem Namen, dem Speicherort, dem Port und dem Freigabe Status. Dies sind die folgenden Hauptschritte:  
  
1. Erstellen Sie ein- <xref:System.Printing.PrintQueue> Objekt für den vorhandenen Drucker, der geklont werden soll.  
  
2. Erstellen Sie einen <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> aus der <xref:System.Printing.PrintSystemObject.PropertiesCollection%2A> von <xref:System.Printing.PrintQueue> . Die- <xref:System.Collections.DictionaryEntry.Value%2A> Eigenschaft jedes Eintrags in diesem Wörterbuch ist ein Objekt von einem der Typen, die von abgeleitet werden <xref:System.Printing.IndexedProperties.PrintProperty> . Es gibt zwei Möglichkeiten, den Wert eines Eintrags in diesem Wörterbuch festzulegen.  
  
    - Verwenden Sie die **Remove** -Methode und die-Methode des Wörterbuchs <xref:System.Printing.IndexedProperties.PrintPropertyDictionary.Add%2A> , um den Eintrag zu entfernen, und fügen Sie ihn dann erneut mit dem gewünschten Wert  
  
    - Verwenden Sie die-Methode des-Wörterbuchs <xref:System.Printing.IndexedProperties.PrintPropertyDictionary.SetProperty%2A> .  
  
     Im folgenden Beispiel werden beide Methoden veranschaulicht.  
  
3. Erstellen <xref:System.Printing.IndexedProperties.PrintBooleanProperty> Sie ein-Objekt, und legen <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> Sie es auf "IsShared" und dessen auf fest <xref:System.Printing.IndexedProperties.PrintBooleanProperty.Value%2A> `true` .  
  
4. Verwenden <xref:System.Printing.IndexedProperties.PrintBooleanProperty> Sie das-Objekt, um den Wert des <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> "IsShared"-Eintrags zu verwenden.  
  
5. Erstellen Sie ein <xref:System.Printing.IndexedProperties.PrintStringProperty> -Objekt, und legen <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> Sie dessen auf "ShareName" und dessen <xref:System.Printing.IndexedProperties.PrintStringProperty.Value%2A> auf einen entsprechenden fest <xref:System.String> .  
  
6. Verwenden <xref:System.Printing.IndexedProperties.PrintStringProperty> Sie das-Objekt, um den Wert des <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> "ShareName"-Eintrags zu verwenden.  
  
7. Erstellen Sie ein weiteres <xref:System.Printing.IndexedProperties.PrintStringProperty> -Objekt, und legen <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> Sie dessen auf "Location" und dessen auf <xref:System.Printing.IndexedProperties.PrintStringProperty.Value%2A> einen entsprechenden fest <xref:System.String> .  
  
8. Verwenden Sie das zweite <xref:System.Printing.IndexedProperties.PrintStringProperty> -Objekt, um den Wert des <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> "Location"-Eintrags zu verwenden.  
  
9. Erstellen Sie ein Array von <xref:System.String> s. Jedes Element ist der Name eines Ports auf dem Server.  
  
10. Verwenden <xref:System.Printing.PrintServer.InstallPrintQueue%2A> Sie, um den neuen Drucker mit den neuen Werten zu installieren.  
  
 Unten ist ein Beispiel angegeben.  
  
 [!code-csharp[ClonePrinter#ClonePrinter](~/samples/snippets/csharp/VS_Snippets_Wpf/ClonePrinter/CSharp/Program.cs#cloneprinter)]
 [!code-vb[ClonePrinter#ClonePrinter](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ClonePrinter/visualbasic/program.vb#cloneprinter)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Printing.IndexedProperties>
- <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>
- <xref:System.Printing.LocalPrintServer>
- <xref:System.Printing.PrintQueue>
- <xref:System.Collections.DictionaryEntry>
- [Dokumente in WPF](documents-in-wpf.md)
- [Übersicht über das Drucken](printing-overview.md)
