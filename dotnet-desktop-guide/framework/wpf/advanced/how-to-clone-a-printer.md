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
# <a name="how-to-clone-a-printer"></a><span data-ttu-id="399dc-102">Gewusst wie: Klonen eines Druckers</span><span class="sxs-lookup"><span data-stu-id="399dc-102">How to: Clone a Printer</span></span>
<span data-ttu-id="399dc-103">Die meisten Unternehmen werden zu einem bestimmten Zeitpunkt mehrere Drucker desselben Modells erwerben.</span><span class="sxs-lookup"><span data-stu-id="399dc-103">Most businesses will, at some point, buy multiple printers of the same model.</span></span> <span data-ttu-id="399dc-104">Diese werden in der Regel mit praktisch identischen Konfigurationseinstellungen installiert.</span><span class="sxs-lookup"><span data-stu-id="399dc-104">Typically, these are all installed with virtually identical configuration settings.</span></span> <span data-ttu-id="399dc-105">Die Installation der einzelnen Drucker kann zeitaufwändig und fehleranfällig sein.</span><span class="sxs-lookup"><span data-stu-id="399dc-105">Installing each printer can be time-consuming and error prone.</span></span> <span data-ttu-id="399dc-106">Der <xref:System.Printing.IndexedProperties?displayProperty=nameWithType> -Namespace und die- <xref:System.Printing.PrintServer.InstallPrintQueue%2A> Klasse, die mit Microsoft .NET Framework verfügbar gemacht werden, ermöglichen es, eine beliebige Anzahl zusätzlicher Druck Warteschlangen, die von einer vorhandenen Druck Warteschlange geklont werden, sofort zu installieren</span><span class="sxs-lookup"><span data-stu-id="399dc-106">The <xref:System.Printing.IndexedProperties?displayProperty=nameWithType> namespace and the <xref:System.Printing.PrintServer.InstallPrintQueue%2A> class that are exposed with Microsoft .NET Framework makes it possible to instantly install any number of additional print queues that are cloned from an existing print queue.</span></span>  
  
## <a name="example"></a><span data-ttu-id="399dc-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="399dc-107">Example</span></span>  
 <span data-ttu-id="399dc-108">Im folgenden Beispiel wird eine zweite Druck Warteschlange aus einer vorhandenen Druck Warteschlange geklont.</span><span class="sxs-lookup"><span data-stu-id="399dc-108">In the example below, a second print queue is cloned from an existing print queue.</span></span> <span data-ttu-id="399dc-109">Die zweite unterscheidet sich von der ersten nur unter dem Namen, dem Speicherort, dem Port und dem Freigabe Status.</span><span class="sxs-lookup"><span data-stu-id="399dc-109">The second differs from the first only in its name, location, port, and shared status.</span></span> <span data-ttu-id="399dc-110">Dies sind die folgenden Hauptschritte:</span><span class="sxs-lookup"><span data-stu-id="399dc-110">The major steps for doing this are as follows.</span></span>  
  
1. <span data-ttu-id="399dc-111">Erstellen Sie ein- <xref:System.Printing.PrintQueue> Objekt für den vorhandenen Drucker, der geklont werden soll.</span><span class="sxs-lookup"><span data-stu-id="399dc-111">Create a <xref:System.Printing.PrintQueue> object for the existing printer that is going to be cloned.</span></span>  
  
2. <span data-ttu-id="399dc-112">Erstellen Sie einen <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> aus der <xref:System.Printing.PrintSystemObject.PropertiesCollection%2A> von <xref:System.Printing.PrintQueue> .</span><span class="sxs-lookup"><span data-stu-id="399dc-112">Create a <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> from the <xref:System.Printing.PrintSystemObject.PropertiesCollection%2A> of the <xref:System.Printing.PrintQueue>.</span></span> <span data-ttu-id="399dc-113">Die- <xref:System.Collections.DictionaryEntry.Value%2A> Eigenschaft jedes Eintrags in diesem Wörterbuch ist ein Objekt von einem der Typen, die von abgeleitet werden <xref:System.Printing.IndexedProperties.PrintProperty> .</span><span class="sxs-lookup"><span data-stu-id="399dc-113">The <xref:System.Collections.DictionaryEntry.Value%2A> property of each entry in this dictionary is an object of one of the types derived from <xref:System.Printing.IndexedProperties.PrintProperty>.</span></span> <span data-ttu-id="399dc-114">Es gibt zwei Möglichkeiten, den Wert eines Eintrags in diesem Wörterbuch festzulegen.</span><span class="sxs-lookup"><span data-stu-id="399dc-114">There are two ways to set the value of an entry in this dictionary.</span></span>  
  
    - <span data-ttu-id="399dc-115">Verwenden Sie die **Remove** -Methode und die-Methode des Wörterbuchs <xref:System.Printing.IndexedProperties.PrintPropertyDictionary.Add%2A> , um den Eintrag zu entfernen, und fügen Sie ihn dann erneut mit dem gewünschten Wert</span><span class="sxs-lookup"><span data-stu-id="399dc-115">Use the dictionary's **Remove** and <xref:System.Printing.IndexedProperties.PrintPropertyDictionary.Add%2A> methods to remove the entry and then re-add it with the desired value.</span></span>  
  
    - <span data-ttu-id="399dc-116">Verwenden Sie die-Methode des-Wörterbuchs <xref:System.Printing.IndexedProperties.PrintPropertyDictionary.SetProperty%2A> .</span><span class="sxs-lookup"><span data-stu-id="399dc-116">Use the dictionary's <xref:System.Printing.IndexedProperties.PrintPropertyDictionary.SetProperty%2A> method.</span></span>  
  
     <span data-ttu-id="399dc-117">Im folgenden Beispiel werden beide Methoden veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="399dc-117">The example below illustrates both ways.</span></span>  
  
3. <span data-ttu-id="399dc-118">Erstellen <xref:System.Printing.IndexedProperties.PrintBooleanProperty> Sie ein-Objekt, und legen <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> Sie es auf "IsShared" und dessen auf fest <xref:System.Printing.IndexedProperties.PrintBooleanProperty.Value%2A> `true` .</span><span class="sxs-lookup"><span data-stu-id="399dc-118">Create a <xref:System.Printing.IndexedProperties.PrintBooleanProperty> object and set its <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> to "IsShared" and its <xref:System.Printing.IndexedProperties.PrintBooleanProperty.Value%2A> to `true`.</span></span>  
  
4. <span data-ttu-id="399dc-119">Verwenden <xref:System.Printing.IndexedProperties.PrintBooleanProperty> Sie das-Objekt, um den Wert des <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> "IsShared"-Eintrags zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="399dc-119">Use the <xref:System.Printing.IndexedProperties.PrintBooleanProperty> object to be the value of the <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>'s "IsShared" entry.</span></span>  
  
5. <span data-ttu-id="399dc-120">Erstellen Sie ein <xref:System.Printing.IndexedProperties.PrintStringProperty> -Objekt, und legen <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> Sie dessen auf "ShareName" und dessen <xref:System.Printing.IndexedProperties.PrintStringProperty.Value%2A> auf einen entsprechenden fest <xref:System.String> .</span><span class="sxs-lookup"><span data-stu-id="399dc-120">Create a <xref:System.Printing.IndexedProperties.PrintStringProperty> object and set its <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> to "ShareName" and its <xref:System.Printing.IndexedProperties.PrintStringProperty.Value%2A> to an appropriate <xref:System.String>.</span></span>  
  
6. <span data-ttu-id="399dc-121">Verwenden <xref:System.Printing.IndexedProperties.PrintStringProperty> Sie das-Objekt, um den Wert des <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> "ShareName"-Eintrags zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="399dc-121">Use the <xref:System.Printing.IndexedProperties.PrintStringProperty> object to be the value of the <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>'s "ShareName" entry.</span></span>  
  
7. <span data-ttu-id="399dc-122">Erstellen Sie ein weiteres <xref:System.Printing.IndexedProperties.PrintStringProperty> -Objekt, und legen <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> Sie dessen auf "Location" und dessen auf <xref:System.Printing.IndexedProperties.PrintStringProperty.Value%2A> einen entsprechenden fest <xref:System.String> .</span><span class="sxs-lookup"><span data-stu-id="399dc-122">Create another <xref:System.Printing.IndexedProperties.PrintStringProperty> object and set its <xref:System.Printing.IndexedProperties.PrintProperty.Name%2A> to "Location" and its <xref:System.Printing.IndexedProperties.PrintStringProperty.Value%2A> to an appropriate <xref:System.String>.</span></span>  
  
8. <span data-ttu-id="399dc-123">Verwenden Sie das zweite <xref:System.Printing.IndexedProperties.PrintStringProperty> -Objekt, um den Wert des <xref:System.Printing.IndexedProperties.PrintPropertyDictionary> "Location"-Eintrags zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="399dc-123">Use the second <xref:System.Printing.IndexedProperties.PrintStringProperty> object to be the value of the <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>'s "Location" entry.</span></span>  
  
9. <span data-ttu-id="399dc-124">Erstellen Sie ein Array von <xref:System.String> s.</span><span class="sxs-lookup"><span data-stu-id="399dc-124">Create an array of <xref:System.String>s.</span></span> <span data-ttu-id="399dc-125">Jedes Element ist der Name eines Ports auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="399dc-125">Each item is the name of a port on the server.</span></span>  
  
10. <span data-ttu-id="399dc-126">Verwenden <xref:System.Printing.PrintServer.InstallPrintQueue%2A> Sie, um den neuen Drucker mit den neuen Werten zu installieren.</span><span class="sxs-lookup"><span data-stu-id="399dc-126">Use <xref:System.Printing.PrintServer.InstallPrintQueue%2A> to install the new printer with the new values.</span></span>  
  
 <span data-ttu-id="399dc-127">Unten ist ein Beispiel angegeben.</span><span class="sxs-lookup"><span data-stu-id="399dc-127">An example is below.</span></span>  
  
 [!code-csharp[ClonePrinter#ClonePrinter](~/samples/snippets/csharp/VS_Snippets_Wpf/ClonePrinter/CSharp/Program.cs#cloneprinter)]
 [!code-vb[ClonePrinter#ClonePrinter](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ClonePrinter/visualbasic/program.vb#cloneprinter)]  
  
## <a name="see-also"></a><span data-ttu-id="399dc-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="399dc-128">See also</span></span>

- <xref:System.Printing.IndexedProperties>
- <xref:System.Printing.IndexedProperties.PrintPropertyDictionary>
- <xref:System.Printing.LocalPrintServer>
- <xref:System.Printing.PrintQueue>
- <xref:System.Collections.DictionaryEntry>
- [<span data-ttu-id="399dc-129">Dokumente in WPF</span><span class="sxs-lookup"><span data-stu-id="399dc-129">Documents in WPF</span></span>](documents-in-wpf.md)
- [<span data-ttu-id="399dc-130">Übersicht über das Drucken</span><span class="sxs-lookup"><span data-stu-id="399dc-130">Printing Overview</span></span>](printing-overview.md)
