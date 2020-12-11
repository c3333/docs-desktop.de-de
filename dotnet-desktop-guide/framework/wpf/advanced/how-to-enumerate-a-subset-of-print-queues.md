---
title: 'Gewusst wie: Auflisten einer Teilmenge von Druckwarteschlangen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- enumerating [WPF], subset of print queues
- print queues [WPF], enumerating subset of
ms.assetid: cc4a1b5b-d46f-4c5e-bc26-22c226e4bee0
ms.openlocfilehash: aae41931f012f6d34fc057fdd6ee9fc9baab6e7b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977543"
---
# <a name="how-to-enumerate-a-subset-of-print-queues"></a><span data-ttu-id="3dd4d-102">Gewusst wie: Auflisten einer Teilmenge von Druckwarteschlangen</span><span class="sxs-lookup"><span data-stu-id="3dd4d-102">How to: Enumerate a Subset of Print Queues</span></span>
<span data-ttu-id="3dd4d-103">Eine häufige Situation von IT-Spezialisten, die eine unternehmensweite Gruppe von Druckern verwalten, besteht darin, eine Liste von Druckern zu generieren, die bestimmte Merkmale aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-103">A common situation faced by information technology (IT) professionals managing a company-wide set of printers is to generate a list of printers having certain characteristics.</span></span> <span data-ttu-id="3dd4d-104">Diese Funktionalität wird von der <xref:System.Printing.PrintServer.GetPrintQueues%2A> -Methode eines <xref:System.Printing.PrintServer> -Objekts und der- <xref:System.Printing.EnumeratedPrintQueueTypes> Enumeration bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-104">This functionality is provided by the <xref:System.Printing.PrintServer.GetPrintQueues%2A> method of a <xref:System.Printing.PrintServer> object and the <xref:System.Printing.EnumeratedPrintQueueTypes> enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3dd4d-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3dd4d-105">Example</span></span>  
 <span data-ttu-id="3dd4d-106">Im folgenden Beispiel beginnt der Code mit dem Erstellen eines Arrays von Flags, die die Merkmale der Druck Warteschlangen angeben, die aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-106">In the example below, the code begins by creating an array of flags that specify the characteristics of the print queues we want to list.</span></span> <span data-ttu-id="3dd4d-107">In diesem Beispiel suchen wir nach Druck Warteschlangen, die lokal auf dem Druckserver installiert sind und freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-107">In this example, we are looking for print queues that are installed locally on the print server and are shared.</span></span> <span data-ttu-id="3dd4d-108">Die- <xref:System.Printing.EnumeratedPrintQueueTypes> Enumeration bietet viele weitere Möglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-108">The <xref:System.Printing.EnumeratedPrintQueueTypes> enumeration provides many other possibilities.</span></span>  
  
 <span data-ttu-id="3dd4d-109">Der Code erstellt dann ein- <xref:System.Printing.LocalPrintServer> Objekt, eine von abgeleitete Klasse <xref:System.Printing.PrintServer> .</span><span class="sxs-lookup"><span data-stu-id="3dd4d-109">The code then creates a <xref:System.Printing.LocalPrintServer> object, a class derived from <xref:System.Printing.PrintServer>.</span></span> <span data-ttu-id="3dd4d-110">Der lokale Druckserver ist der Computer, auf dem die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-110">The local print server is the computer on which the application is running.</span></span>  
  
 <span data-ttu-id="3dd4d-111">Der letzte bedeutende Schritt besteht darin, das Array an die-Methode zu übergeben <xref:System.Printing.PrintServer.GetPrintQueues%2A> .</span><span class="sxs-lookup"><span data-stu-id="3dd4d-111">The last significant step is to pass the array to the <xref:System.Printing.PrintServer.GetPrintQueues%2A> method.</span></span>  
  
 <span data-ttu-id="3dd4d-112">Abschließend werden dem Benutzer die Ergebnisse präsentiert.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-112">Finally, the results are presented to the user.</span></span>  
  
 [!code-cpp[EnumerateSubsetOfPrintQueues#ListSubsetOfPrintQueues](~/samples/snippets/cpp/VS_Snippets_Wpf/EnumerateSubsetOfPrintQueues/CPP/Program.cpp#listsubsetofprintqueues)]
 [!code-csharp[EnumerateSubsetOfPrintQueues#ListSubsetOfPrintQueues](~/samples/snippets/csharp/VS_Snippets_Wpf/EnumerateSubsetOfPrintQueues/CSharp/Program.cs#listsubsetofprintqueues)]
 [!code-vb[EnumerateSubsetOfPrintQueues#ListSubsetOfPrintQueues](~/samples/snippets/visualbasic/VS_Snippets_Wpf/EnumerateSubsetOfPrintQueues/visualbasic/program.vb#listsubsetofprintqueues)]  
  
 <span data-ttu-id="3dd4d-113">Sie können dieses Beispiel erweitern, indem Sie die `foreach` Schleife ausführen, durch die die einzelnen Druck Warteschlangen durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-113">You could extend this example by having the `foreach` loop that steps through each print queue do further screening.</span></span> <span data-ttu-id="3dd4d-114">Beispielsweise können Sie Drucker herausfiltern, die das zweiseitige Drucken nicht unterstützen, indem Sie die-Schleife jeder Druck Warteschlange aufrufen <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A> und den zurückgegebenen Wert für das vorhanden sein von Duplexing testen.</span><span class="sxs-lookup"><span data-stu-id="3dd4d-114">For example, you could screen out printers that do not support two-sided printing by having the loop call each print queue's <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A> method and test the returned value for the presence of duplexing.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3dd4d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dd4d-115">See also</span></span>

- <xref:System.Printing.PrintServer.GetPrintQueues%2A>
- <xref:System.Printing.PrintServer>
- <xref:System.Printing.LocalPrintServer>
- <xref:System.Printing.EnumeratedPrintQueueTypes>
- <xref:System.Printing.PrintQueue>
- <xref:System.Printing.PrintQueue.GetPrintCapabilities%2A>
- [<span data-ttu-id="3dd4d-116">Dokumente in WPF</span><span class="sxs-lookup"><span data-stu-id="3dd4d-116">Documents in WPF</span></span>](documents-in-wpf.md)
- [<span data-ttu-id="3dd4d-117">Übersicht über das Drucken</span><span class="sxs-lookup"><span data-stu-id="3dd4d-117">Printing Overview</span></span>](printing-overview.md)
- [<span data-ttu-id="3dd4d-118">Microsoft XPS-Dokument-Generator</span><span class="sxs-lookup"><span data-stu-id="3dd4d-118">Microsoft XPS Document Writer</span></span>](/windows/win32/printdocs/microsoft-xps-document-writer)
