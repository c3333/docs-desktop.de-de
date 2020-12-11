---
title: 'Gewusst wie: Ermitteln, ob ein Druckauftrag zu dieser Tageszeit gedruckt werden kann'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- print queues [WPF], timing
- printers [WPF], availability
- print jobs [WPF], timing
ms.assetid: 7e9c8ec1-abf6-4b3d-b1c6-33b35d3c4063
ms.openlocfilehash: 859dc75169e443d07361951692a428507886fa2e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977587"
---
# <a name="how-to-discover-whether-a-print-job-can-be-printed-at-this-time-of-day"></a>Gewusst wie: Ermitteln, ob ein Druckauftrag zu dieser Tageszeit gedruckt werden kann
Druck Warteschlangen sind nicht immer für 24 Stunden pro Tag verfügbar. Sie verfügen über Start-und Endzeit Eigenschaften, die festgelegt werden können, um Sie zu bestimmten Tageszeiten nicht verfügbar zu machen. Diese Funktion kann z. b. verwendet werden, um einen Drucker für die ausschließliche Verwendung einer bestimmten Abteilung nach 5 Uhr zu reservieren. Diese Abteilung hätte eine andere Warteschlange als die von anderen Abteilungen verwendete Warteschlange. Die Warteschlange für die anderen Abteilungen ist so eingestellt, dass Sie nach 5 Uhr nicht verfügbar ist, während die Warteschlange für die bevorzugte Abteilung jederzeit als verfügbar festgelegt werden kann.  
  
 Darüber hinaus können Druckaufträge selbst so festgelegt werden, dass Sie nur innerhalb eines angegebenen Zeitraums gedruckt werden können.  
  
 Die <xref:System.Printing.PrintQueue> Klassen und, die <xref:System.Printing.PrintSystemJobInfo> in den APIs von Microsoft .NET Framework verfügbar gemacht werden, bieten eine Möglichkeit zur Remote Überprüfung, ob ein angegebener Druckauftrag zum aktuellen Zeitpunkt für eine bestimmte Warteschlange gedruckt werden kann.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt ein Beispiel, mit dem Probleme mit einem Druckauftrag diagnostiziert werden können.  
  
 Für diese Art von Funktion gibt es die folgenden zwei Hauptschritte:  
  
1. Lesen Sie die <xref:System.Printing.PrintQueue.StartTimeOfDay%2A> -Eigenschaft und die-Eigenschaft <xref:System.Printing.PrintQueue.UntilTimeOfDay%2A> des <xref:System.Printing.PrintQueue> , um zu bestimmen, ob die aktuelle Zeit zwischen Ihnen liegt.  
  
2. Lesen Sie die <xref:System.Printing.PrintSystemJobInfo.StartTimeOfDay%2A> -Eigenschaft und die-Eigenschaft <xref:System.Printing.PrintSystemJobInfo.UntilTimeOfDay%2A> des <xref:System.Printing.PrintSystemJobInfo> , um zu bestimmen, ob die aktuelle Zeit zwischen Ihnen liegt.  
  
 Allerdings entstehen Komplikationen aufgrund der Tatsache, dass es sich bei diesen Eigenschaften nicht um <xref:System.DateTime> Objekte handelt. Stattdessen handelt es sich um <xref:System.Int32> Objekte, die die Tageszeit als Anzahl von Minuten seit Mitternacht Ausdrücken. Außerdem ist dies nicht Mitternacht in der aktuellen Zeitzone, sondern Mitternacht UTC (koordinierte Weltzeit).  
  
 Im ersten Codebeispiel wird die statische Methode **ReportQueueAndJobAvailability** dargestellt, der ein weitergegeben wird, <xref:System.Printing.PrintSystemJobInfo> und Hilfsmethoden werden aufgerufen, um zu bestimmen, ob der Auftrag zum aktuellen Zeitpunkt gedruckt werden kann, und andernfalls, wenn er nicht gedruckt werden kann. Beachten Sie, dass ein <xref:System.Printing.PrintQueue> nicht an die-Methode übermittelt wird. Dies liegt daran, dass der <xref:System.Printing.PrintSystemJobInfo> einen Verweis auf die Warteschlange in der- <xref:System.Printing.PrintSystemJobInfo.HostingPrintQueue%2A> Eigenschaft enthält.  
  
 Die untergeordneten Methoden enthalten die überladene **ReportAvailabilityAtThisTime** -Methode, die entweder einen <xref:System.Printing.PrintQueue> oder einen <xref:System.Printing.PrintSystemJobInfo> als Parameter annehmen kann. Es ist auch ein **TimeConverter. converttolocalhumanread abletime**-Wert vorhanden. Alle diese Methoden werden im folgenden erläutert.  
  
 Die Methode **ReportQueueAndJobAvailability** prüft zunächst, ob die Warteschlange oder der Druckauftrag zu diesem Zeitpunkt nicht verfügbar ist. Wenn eine der beiden Optionen nicht verfügbar ist, wird überprüft, ob die Warteschlange nicht verfügbar ist. Wenn Sie nicht verfügbar ist, meldet die Methode diesen Fakt und die Uhrzeit, zu der die Warteschlange wieder verfügbar wird. Anschließend wird der Auftrag überprüft, und wenn er nicht verfügbar ist, meldet er die nächste Zeitspanne, zu der er gedruckt werden kann. Schließlich meldet die-Methode die früheste Uhrzeit, zu der der Auftrag drucken kann. Dies ist das spätere zwei fache.  
  
- Der Zeitpunkt, zu dem die Druck Warteschlange als nächstes verfügbar ist.  
  
- Der Zeitpunkt, zu dem der Druckauftrag als nächstes verfügbar ist.  
  
 Beim Melden der Tageszeiten <xref:System.DateTime.ToShortTimeString%2A> wird auch die-Methode aufgerufen, da diese Methode die Jahre, Monate und Tage der Ausgabe unterdrückt. Die Verfügbarkeit einer Druck Warteschlange oder eines Druckauftrags kann nicht auf bestimmte Jahre, Monate oder Tage beschränkt werden.  
  
 [!code-cpp[DiagnoseProblematicPrintJob#ReportQueueAndJobAvailability](~/samples/snippets/cpp/VS_Snippets_Wpf/DiagnoseProblematicPrintJob/CPP/Program.cpp#reportqueueandjobavailability)]
 [!code-csharp[DiagnoseProblematicPrintJob#ReportQueueAndJobAvailability](~/samples/snippets/csharp/VS_Snippets_Wpf/DiagnoseProblematicPrintJob/CSharp/Program.cs#reportqueueandjobavailability)]
 [!code-vb[DiagnoseProblematicPrintJob#ReportQueueAndJobAvailability](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DiagnoseProblematicPrintJob/visualbasic/program.vb#reportqueueandjobavailability)]  
  
 Die zwei über Ladungen der **ReportAvailabilityAtThisTime** -Methode sind mit Ausnahme des an Sie übergebenen Typs identisch, sodass nur die- <xref:System.Printing.PrintQueue> Version unten dargestellt wird.  
  
> [!NOTE]
> Die Tatsache, dass die Methoden mit Ausnahme des Typs identisch sind, wirft die Frage, warum das Beispiel keine generische Methode " **ReportAvailabilityAtThisTime \<T>**" erstellt. Der Grund hierfür ist, dass eine solche Methode auf eine Klasse beschränkt werden muss, die die Eigenschaften **StartTimeOfDay** und **UntilTimeOfDay** hat, die von der-Methode aufgerufen werden, aber eine generische Methode kann nur auf eine einzelne Klasse eingeschränkt werden, und die einzige Klasse, die sowohl für <xref:System.Printing.PrintQueue> als auch <xref:System.Printing.PrintSystemJobInfo> in der Vererbungs Struktur gilt, <xref:System.Printing.PrintSystemObject> verfügt über keine derartigen Eigenschaften.  
  
 Die **ReportAvailabilityAtThisTime** -Methode (im folgenden Codebeispiel dargestellt) beginnt mit dem Initialisieren einer <xref:System.Boolean> Sentinel-Variablen in `true` . Sie wird auf zurückgesetzt `false` , wenn die Warteschlange nicht verfügbar ist.  
  
 Als nächstes überprüft die Methode, ob die Start-und "Until"-Zeiten identisch sind. Wenn dies der Fall ist, ist die Warteschlange immer verfügbar, sodass die Methode zurückgibt `true` .  
  
 Wenn die Warteschlange nicht ständig verfügbar ist, verwendet die-Methode die statische- <xref:System.DateTime.UtcNow%2A> Eigenschaft, um die aktuelle Zeit als-Objekt zu erhalten <xref:System.DateTime> . (Lokale Zeit ist nicht erforderlich, da die <xref:System.Printing.PrintQueue.StartTimeOfDay%2A> -Eigenschaft und die-Eigenschaft <xref:System.Printing.PrintQueue.UntilTimeOfDay%2A> selbst in UTC-Zeit sind.)  
  
 Diese beiden Eigenschaften sind jedoch keine- <xref:System.DateTime> Objekte. Sie <xref:System.Int32> Ausdrücken die Zeit als Anzahl von Minuten nach-UTC-Mitternacht. Wir müssen also unser <xref:System.DateTime> Objekt in Minuten nach Mitternacht konvertieren. Wenn dies der Fall ist, prüft die Methode einfach, ob "Now" zwischen den Start-und "Until"-Zeiten der Warteschlange liegt, und legt den Sentinel auf "false" fest, wenn "Now" nicht zwischen den beiden Vorkommen liegt, und gibt den Sentinel zurück.  
  
 [!code-cpp[DiagnoseProblematicPrintJob#PrintQueueStartUntil](~/samples/snippets/cpp/VS_Snippets_Wpf/DiagnoseProblematicPrintJob/CPP/Program.cpp#printqueuestartuntil)]
 [!code-csharp[DiagnoseProblematicPrintJob#PrintQueueStartUntil](~/samples/snippets/csharp/VS_Snippets_Wpf/DiagnoseProblematicPrintJob/CSharp/Program.cs#printqueuestartuntil)]
 [!code-vb[DiagnoseProblematicPrintJob#PrintQueueStartUntil](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DiagnoseProblematicPrintJob/visualbasic/program.vb#printqueuestartuntil)]  
  
 Die **TimeConverter. converttolocalhumanleabletime** -Methode (im folgenden Codebeispiel dargestellt) verwendet keine Methoden, die mit Microsoft .NET Framework eingeführt wurden, sodass die Diskussion kurz ist. Die Methode verfügt über einen Double-Konvertierungs Task: Sie muss eine ganze Zahl sein, die Minuten nach Mitternacht ausdrückt, und Sie muss in eine lesbare Zeit konvertiert werden, und Sie muss in die Ortszeit konvertiert werden. Dies wird erreicht, indem zuerst ein <xref:System.DateTime> -Objekt erstellt wird, das auf Mitternacht UTC festgelegt ist. Anschließend wird die- <xref:System.DateTime.AddMinutes%2A> Methode verwendet, um die Minuten hinzuzufügen, die an die-Methode weitergegeben wurden. Dadurch wird <xref:System.DateTime> die ursprüngliche Zeit zurückgegeben, die an die-Methode übermittelt wurde. Die <xref:System.DateTime.ToLocalTime%2A> Methode konvertiert diese dann in die lokale Zeit.  
  
 [!code-cpp[DiagnoseProblematicPrintJob#TimeConverter](~/samples/snippets/cpp/VS_Snippets_Wpf/DiagnoseProblematicPrintJob/CPP/Program.cpp#timeconverter)]
 [!code-csharp[DiagnoseProblematicPrintJob#TimeConverter](~/samples/snippets/csharp/VS_Snippets_Wpf/DiagnoseProblematicPrintJob/CSharp/Program.cs#timeconverter)]
 [!code-vb[DiagnoseProblematicPrintJob#TimeConverter](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DiagnoseProblematicPrintJob/visualbasic/program.vb#timeconverter)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.DateTime>
- <xref:System.Printing.PrintSystemJobInfo>
- <xref:System.Printing.PrintQueue>
- [Dokumente in WPF](documents-in-wpf.md)
- [Übersicht über das Drucken](printing-overview.md)
