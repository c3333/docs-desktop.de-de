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
# <a name="how-to-validate-and-merge-printtickets"></a><span data-ttu-id="5e091-102">Gewusst wie: Überprüfen und Zusammenführen von PrintTickets</span><span class="sxs-lookup"><span data-stu-id="5e091-102">How to: Validate and Merge PrintTickets</span></span>
<span data-ttu-id="5e091-103">Das Microsoft Windows- [Druck Schema](/windows/win32/printdocs/printschema) enthält die flexiblen und erweiterbaren <xref:System.Printing.PrintCapabilities> -und- <xref:System.Printing.PrintTicket> Elemente.</span><span class="sxs-lookup"><span data-stu-id="5e091-103">The Microsoft Windows [Print Schema](/windows/win32/printdocs/printschema) includes the flexible and extensible <xref:System.Printing.PrintCapabilities> and <xref:System.Printing.PrintTicket> elements.</span></span> <span data-ttu-id="5e091-104">Die frühere Funktion stellt die Funktionen eines Druck Geräts dar, und letztere gibt an, wie das Gerät diese Funktionen in Bezug auf eine bestimmte Sequenz von Dokumenten, ein einzelnes Dokument oder eine einzelne Seite verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="5e091-104">The former itemizes the capabilities of a print device and the latter specifies how the device should use those capabilities with respect to a particular sequence of documents, individual document, or individual page.</span></span>  
  
 <span data-ttu-id="5e091-105">Eine typische Abfolge von Aufgaben für eine Anwendung, die das Drucken unterstützt, sieht wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="5e091-105">A typical sequence of tasks for an application that supports printing would be as follows.</span></span>  
  
1. <span data-ttu-id="5e091-106">Bestimmen Sie die Fähigkeiten eines Druckers.</span><span class="sxs-lookup"><span data-stu-id="5e091-106">Determine a printer's capabilities.</span></span>  
  
2. <span data-ttu-id="5e091-107">Konfigurieren <xref:System.Printing.PrintTicket> Sie, um diese Funktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e091-107">Configure a <xref:System.Printing.PrintTicket> to use those capabilities.</span></span>  
  
3. <span data-ttu-id="5e091-108">Überprüfen Sie die <xref:System.Printing.PrintTicket> .</span><span class="sxs-lookup"><span data-stu-id="5e091-108">Validate the <xref:System.Printing.PrintTicket>.</span></span>  
  
 <span data-ttu-id="5e091-109">Dieser Artikel zeigt, wie Sie dies tun.</span><span class="sxs-lookup"><span data-stu-id="5e091-109">This article shows how to do this.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5e091-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5e091-110">Example</span></span>  
 <span data-ttu-id="5e091-111">Im folgenden einfachen Beispiel sind wir nur daran interessiert, ob ein Drucker Duplexing unterstützen kann – zweiseitiges Drucken.</span><span class="sxs-lookup"><span data-stu-id="5e091-111">In the simple example below, we are interested only in whether a printer can support duplexing — two-sided printing.</span></span> <span data-ttu-id="5e091-112">Die wichtigsten Schritte sind wie folgt.</span><span class="sxs-lookup"><span data-stu-id="5e091-112">The major steps are as follows.</span></span>  
  
1. <span data-ttu-id="5e091-113">Ein- <xref:System.Printing.PrintCapabilities> Objekt mit der-Methode zu erhalten <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A> .</span><span class="sxs-lookup"><span data-stu-id="5e091-113">Get a <xref:System.Printing.PrintCapabilities> object with the <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A> method.</span></span>  
  
2. <span data-ttu-id="5e091-114">Testen Sie, ob die gewünschte Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5e091-114">Test for the presence of the capability you want.</span></span> <span data-ttu-id="5e091-115">Im folgenden Beispiel wird die- <xref:System.Printing.PrintCapabilities.DuplexingCapability%2A> Eigenschaft des- <xref:System.Printing.PrintCapabilities> Objekts für das vorhanden sein der Druckfunktion auf beiden Seiten eines Papier Blatts getestet, wobei die "Seiten Drehung" entlang der langen Seite des Blatts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5e091-115">In the example below, we test the <xref:System.Printing.PrintCapabilities.DuplexingCapability%2A> property of the <xref:System.Printing.PrintCapabilities> object for the presence of the capability of printing on both sides of a sheet of paper with the "page turning" along the long side of the sheet.</span></span> <span data-ttu-id="5e091-116">Da <xref:System.Printing.PrintCapabilities.DuplexingCapability%2A> eine Auflistung ist, verwenden wir die- `Contains` Methode von <xref:System.Collections.ObjectModel.ReadOnlyCollection%601> .</span><span class="sxs-lookup"><span data-stu-id="5e091-116">Since <xref:System.Printing.PrintCapabilities.DuplexingCapability%2A> is a collection, we use the `Contains` method of <xref:System.Collections.ObjectModel.ReadOnlyCollection%601>.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="5e091-117">Dieser Schritt ist nicht unbedingt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5e091-117">This step is not strictly necessary.</span></span> <span data-ttu-id="5e091-118">Die <xref:System.Printing.PrintQueue.MergeAndValidatePrintTicket%2A> unten verwendete Methode überprüft jede Anforderung in der auf <xref:System.Printing.PrintTicket> die Funktionen des Druckers.</span><span class="sxs-lookup"><span data-stu-id="5e091-118">The <xref:System.Printing.PrintQueue.MergeAndValidatePrintTicket%2A> method used below will check each request in the <xref:System.Printing.PrintTicket> against the capabilities of the printer.</span></span> <span data-ttu-id="5e091-119">Wenn die angeforderte Funktion nicht vom Drucker unterstützt wird, ersetzt der Druckertreiber eine alternative Anforderung in der, die <xref:System.Printing.PrintTicket> von der-Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5e091-119">If the requested capability is not supported by printer, the printer driver will substitute an alternative request in the <xref:System.Printing.PrintTicket> returned by the method.</span></span>  
  
3. <span data-ttu-id="5e091-120">Wenn der Drucker Duplexing unterstützt, erstellt der Beispielcode einen, der das <xref:System.Printing.PrintTicket> Duplexing anfordert.</span><span class="sxs-lookup"><span data-stu-id="5e091-120">If the printer supports duplexing, the sample code creates a <xref:System.Printing.PrintTicket> that asks for duplexing.</span></span> <span data-ttu-id="5e091-121">Die Anwendung gibt jedoch nicht alle möglichen Druckereinstellungen an, die im-Element verfügbar sind <xref:System.Printing.PrintTicket> .</span><span class="sxs-lookup"><span data-stu-id="5e091-121">But the application does not specify every possible printer setting available in the <xref:System.Printing.PrintTicket> element.</span></span> <span data-ttu-id="5e091-122">Der Programmierer und die Programmzeit würden verschwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e091-122">That would be wasteful of both programmer and program time.</span></span> <span data-ttu-id="5e091-123">Stattdessen legt der Code nur die Duplexing-Anforderung fest und führt diese dann <xref:System.Printing.PrintTicket> mit einem vorhandenen, vollständig konfigurierten und validierten, <xref:System.Printing.PrintTicket> , in diesem Fall, dem Standard des Benutzers zusammen <xref:System.Printing.PrintTicket> .</span><span class="sxs-lookup"><span data-stu-id="5e091-123">Instead, the code sets only the duplexing request and then merges this <xref:System.Printing.PrintTicket> with an existing, fully configured and validated, <xref:System.Printing.PrintTicket>, in this case, the user's default <xref:System.Printing.PrintTicket>.</span></span>  
  
4. <span data-ttu-id="5e091-124">Entsprechend Ruft das Beispiel die <xref:System.Printing.PrintQueue.MergeAndValidatePrintTicket%2A> -Methode auf, um den neuen Minimalwert <xref:System.Printing.PrintTicket> mit dem Standard des Benutzers zusammenzuführen <xref:System.Printing.PrintTicket> .</span><span class="sxs-lookup"><span data-stu-id="5e091-124">Accordingly, the sample calls the <xref:System.Printing.PrintQueue.MergeAndValidatePrintTicket%2A> method to merge the new, minimal, <xref:System.Printing.PrintTicket> with the user's default <xref:System.Printing.PrintTicket>.</span></span> <span data-ttu-id="5e091-125">Dadurch wird eine zurückgegeben <xref:System.Printing.ValidationResult> , die die neue <xref:System.Printing.PrintTicket> als eine ihrer Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="5e091-125">This returns a <xref:System.Printing.ValidationResult> that includes the new <xref:System.Printing.PrintTicket> as one of its properties.</span></span>  
  
5. <span data-ttu-id="5e091-126">Im Beispiel wird dann getestet, ob die neuen <xref:System.Printing.PrintTicket> Anforderungen Duplexing werden.</span><span class="sxs-lookup"><span data-stu-id="5e091-126">The sample then tests that the new <xref:System.Printing.PrintTicket> requests duplexing.</span></span> <span data-ttu-id="5e091-127">Wenn dies der Fall ist, wird das Beispiel zum neuen Standarddruck Ticket für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5e091-127">If it does, then the sample makes it the new default print ticket for the user.</span></span> <span data-ttu-id="5e091-128">Wenn Schritt 2 oben ausgelassen wurde und der Drucker die Duplexing-Komponente nicht auf der langen Seite unterstützte, hätte der Test dazu geführt `false` .</span><span class="sxs-lookup"><span data-stu-id="5e091-128">If step 2 above had been left out and the printer did not support duplexing along the long side, then the test would have resulted in `false`.</span></span> <span data-ttu-id="5e091-129">(Siehe den obigen Hinweis.)</span><span class="sxs-lookup"><span data-stu-id="5e091-129">(See the note above.)</span></span>  
  
6. <span data-ttu-id="5e091-130">Der letzte bedeutende Schritt besteht darin, die Änderung mit der-Methode an die- <xref:System.Printing.PrintQueue.UserPrintTicket%2A> Eigenschaft des zu übergeben <xref:System.Printing.PrintQueue> <xref:System.Printing.PrintQueue.Commit%2A> .</span><span class="sxs-lookup"><span data-stu-id="5e091-130">The last significant step is to commit the change to the <xref:System.Printing.PrintQueue.UserPrintTicket%2A> property of the <xref:System.Printing.PrintQueue> with the <xref:System.Printing.PrintQueue.Commit%2A> method.</span></span>  
  
 [!code-csharp[PrintTicketManagment#UsingMergeAndValidate](~/samples/snippets/csharp/VS_Snippets_Wpf/PrintTicketManagment/CSharp/printticket.cs#usingmergeandvalidate)]
 [!code-vb[PrintTicketManagment#UsingMergeAndValidate](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PrintTicketManagment/visualbasic/printticket.vb#usingmergeandvalidate)]  
  
 <span data-ttu-id="5e091-131">Um dieses Beispiel schnell testen zu können, wird der restliche Rest der Abbildung unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5e091-131">So that you can quickly test this example, the remainder of it is presented below.</span></span> <span data-ttu-id="5e091-132">Erstellen Sie ein Projekt und einen Namespace, und fügen Sie die Code Ausschnitte in diesem Artikel in den Namespace-Block ein.</span><span class="sxs-lookup"><span data-stu-id="5e091-132">Create a project and a namespace and then paste both the code snippets in this article into the namespace block.</span></span>  
  
 [!code-csharp[PrintTicketManagment#UIForMergeAndValidatePTUtility](~/samples/snippets/csharp/VS_Snippets_Wpf/PrintTicketManagment/CSharp/printticket.cs#uiformergeandvalidateptutility)]
 [!code-vb[PrintTicketManagment#UIForMergeAndValidatePTUtility](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PrintTicketManagment/visualbasic/printticket.vb#uiformergeandvalidateptutility)]  
  
## <a name="see-also"></a><span data-ttu-id="5e091-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e091-133">See also</span></span>

- <xref:System.Printing.PrintCapabilities>
- <xref:System.Printing.PrintTicket>
- <xref:System.Printing.PrintServer.GetPrintQueues%2A>
- <xref:System.Printing.PrintServer>
- <xref:System.Printing.EnumeratedPrintQueueTypes>
- <xref:System.Printing.PrintQueue>
- <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A>
- [<span data-ttu-id="5e091-134">Dokumente in WPF</span><span class="sxs-lookup"><span data-stu-id="5e091-134">Documents in WPF</span></span>](documents-in-wpf.md)
- [<span data-ttu-id="5e091-135">Übersicht über das Drucken</span><span class="sxs-lookup"><span data-stu-id="5e091-135">Printing Overview</span></span>](printing-overview.md)
- [<span data-ttu-id="5e091-136">Druck Schema</span><span class="sxs-lookup"><span data-stu-id="5e091-136">Print Schema</span></span>](/windows/win32/printdocs/printschema)
