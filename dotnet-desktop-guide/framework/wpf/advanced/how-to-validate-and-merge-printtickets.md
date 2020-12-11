---
title: 'Gewusst wie: Überprüfen und Zusammenführen von PrintTickets'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- merging PrintTickets [WPF]
- PrintTicket [WPF], merging
- validation of PrintTickets [WPF]
- PrintTicket [WPF], validation
ms.assetid: 4fe2d501-d0b0-4fef-86af-6ffe6c162532
ms.openlocfilehash: bd7f399555b343a52ec6f36aa3b8c706747d8b06
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977836"
---
# <a name="how-to-validate-and-merge-printtickets"></a>Gewusst wie: Überprüfen und Zusammenführen von PrintTickets
Das Microsoft Windows- [Druck Schema](/windows/win32/printdocs/printschema) enthält die flexiblen und erweiterbaren <xref:System.Printing.PrintCapabilities> -und- <xref:System.Printing.PrintTicket> Elemente. Die frühere Funktion stellt die Funktionen eines Druck Geräts dar, und letztere gibt an, wie das Gerät diese Funktionen in Bezug auf eine bestimmte Sequenz von Dokumenten, ein einzelnes Dokument oder eine einzelne Seite verwenden soll.  
  
 Eine typische Abfolge von Aufgaben für eine Anwendung, die das Drucken unterstützt, sieht wie folgt aus.  
  
1. Bestimmen Sie die Fähigkeiten eines Druckers.  
  
2. Konfigurieren <xref:System.Printing.PrintTicket> Sie, um diese Funktionen zu verwenden.  
  
3. Überprüfen Sie die <xref:System.Printing.PrintTicket> .  
  
 Dieser Artikel zeigt, wie Sie dies tun.  
  
## <a name="example"></a>Beispiel  
 Im folgenden einfachen Beispiel sind wir nur daran interessiert, ob ein Drucker Duplexing unterstützen kann – zweiseitiges Drucken. Die wichtigsten Schritte sind wie folgt.  
  
1. Ein- <xref:System.Printing.PrintCapabilities> Objekt mit der-Methode zu erhalten <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A> .  
  
2. Testen Sie, ob die gewünschte Funktion vorhanden ist. Im folgenden Beispiel wird die- <xref:System.Printing.PrintCapabilities.DuplexingCapability%2A> Eigenschaft des- <xref:System.Printing.PrintCapabilities> Objekts für das vorhanden sein der Druckfunktion auf beiden Seiten eines Papier Blatts getestet, wobei die "Seiten Drehung" entlang der langen Seite des Blatts angezeigt wird. Da <xref:System.Printing.PrintCapabilities.DuplexingCapability%2A> eine Auflistung ist, verwenden wir die- `Contains` Methode von <xref:System.Collections.ObjectModel.ReadOnlyCollection%601> .  
  
    > [!NOTE]
    > Dieser Schritt ist nicht unbedingt erforderlich. Die <xref:System.Printing.PrintQueue.MergeAndValidatePrintTicket%2A> unten verwendete Methode überprüft jede Anforderung in der auf <xref:System.Printing.PrintTicket> die Funktionen des Druckers. Wenn die angeforderte Funktion nicht vom Drucker unterstützt wird, ersetzt der Druckertreiber eine alternative Anforderung in der, die <xref:System.Printing.PrintTicket> von der-Methode zurückgegeben wird.  
  
3. Wenn der Drucker Duplexing unterstützt, erstellt der Beispielcode einen, der das <xref:System.Printing.PrintTicket> Duplexing anfordert. Die Anwendung gibt jedoch nicht alle möglichen Druckereinstellungen an, die im-Element verfügbar sind <xref:System.Printing.PrintTicket> . Der Programmierer und die Programmzeit würden verschwendet werden. Stattdessen legt der Code nur die Duplexing-Anforderung fest und führt diese dann <xref:System.Printing.PrintTicket> mit einem vorhandenen, vollständig konfigurierten und validierten, <xref:System.Printing.PrintTicket> , in diesem Fall, dem Standard des Benutzers zusammen <xref:System.Printing.PrintTicket> .  
  
4. Entsprechend Ruft das Beispiel die <xref:System.Printing.PrintQueue.MergeAndValidatePrintTicket%2A> -Methode auf, um den neuen Minimalwert <xref:System.Printing.PrintTicket> mit dem Standard des Benutzers zusammenzuführen <xref:System.Printing.PrintTicket> . Dadurch wird eine zurückgegeben <xref:System.Printing.ValidationResult> , die die neue <xref:System.Printing.PrintTicket> als eine ihrer Eigenschaften enthält.  
  
5. Im Beispiel wird dann getestet, ob die neuen <xref:System.Printing.PrintTicket> Anforderungen Duplexing werden. Wenn dies der Fall ist, wird das Beispiel zum neuen Standarddruck Ticket für den Benutzer. Wenn Schritt 2 oben ausgelassen wurde und der Drucker die Duplexing-Komponente nicht auf der langen Seite unterstützte, hätte der Test dazu geführt `false` . (Siehe den obigen Hinweis.)  
  
6. Der letzte bedeutende Schritt besteht darin, die Änderung mit der-Methode an die- <xref:System.Printing.PrintQueue.UserPrintTicket%2A> Eigenschaft des zu übergeben <xref:System.Printing.PrintQueue> <xref:System.Printing.PrintQueue.Commit%2A> .  
  
 [!code-csharp[PrintTicketManagment#UsingMergeAndValidate](~/samples/snippets/csharp/VS_Snippets_Wpf/PrintTicketManagment/CSharp/printticket.cs#usingmergeandvalidate)]
 [!code-vb[PrintTicketManagment#UsingMergeAndValidate](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PrintTicketManagment/visualbasic/printticket.vb#usingmergeandvalidate)]  
  
 Um dieses Beispiel schnell testen zu können, wird der restliche Rest der Abbildung unten dargestellt. Erstellen Sie ein Projekt und einen Namespace, und fügen Sie die Code Ausschnitte in diesem Artikel in den Namespace-Block ein.  
  
 [!code-csharp[PrintTicketManagment#UIForMergeAndValidatePTUtility](~/samples/snippets/csharp/VS_Snippets_Wpf/PrintTicketManagment/CSharp/printticket.cs#uiformergeandvalidateptutility)]
 [!code-vb[PrintTicketManagment#UIForMergeAndValidatePTUtility](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PrintTicketManagment/visualbasic/printticket.vb#uiformergeandvalidateptutility)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Printing.PrintCapabilities>
- <xref:System.Printing.PrintTicket>
- <xref:System.Printing.PrintServer.GetPrintQueues%2A>
- <xref:System.Printing.PrintServer>
- <xref:System.Printing.EnumeratedPrintQueueTypes>
- <xref:System.Printing.PrintQueue>
- <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A>
- [Dokumente in WPF](documents-in-wpf.md)
- [Übersicht über das Drucken](printing-overview.md)
- [Druck Schema](/windows/win32/printdocs/printschema)
