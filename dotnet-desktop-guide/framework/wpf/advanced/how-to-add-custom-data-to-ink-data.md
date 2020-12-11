---
title: 'Gewusst wie: Hinzufügen von benutzerdefinierten Daten zu Freihanddaten'
ms.date: 03/30/2017
helpviewer_keywords:
- ink data [WPF], adding custom data
- InkCanvas [WPF], displaying
ms.assetid: f02aac6f-3436-4f7c-b6ea-0452cba5332c
ms.openlocfilehash: 7c59a205df5358daec101339cc6a308c8e38a9d6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976568"
---
# <a name="how-to-add-custom-data-to-ink-data"></a><span data-ttu-id="ec1f1-102">Gewusst wie: Hinzufügen von benutzerdefinierten Daten zu Freihanddaten</span><span class="sxs-lookup"><span data-stu-id="ec1f1-102">How to: Add Custom Data to Ink Data</span></span>
<span data-ttu-id="ec1f1-103">Sie können frei Hand Eingaben benutzerdefinierte Daten hinzufügen, die gespeichert werden, wenn die frei Hand Eingabe als frei Hand Format (Ink serialisiert Format) gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="ec1f1-103">You can add custom data to ink that will be saved when the ink is saved as ink serialized format (ISF).</span></span>  <span data-ttu-id="ec1f1-104">Sie können die benutzerdefinierten Daten in <xref:System.Windows.Ink.DrawingAttributes> , oder speichern <xref:System.Windows.Ink.StrokeCollection> <xref:System.Windows.Ink.Stroke> .</span><span class="sxs-lookup"><span data-stu-id="ec1f1-104">You can save the custom data to the <xref:System.Windows.Ink.DrawingAttributes>, the <xref:System.Windows.Ink.StrokeCollection>, or the <xref:System.Windows.Ink.Stroke>.</span></span>  <span data-ttu-id="ec1f1-105">Wenn Sie benutzerdefinierte Daten in drei Objekten speichern können, können Sie entscheiden, ob die Daten am besten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ec1f1-105">Being able to save custom data on three objects gives you the ability to decide the best place to save the data.</span></span>  <span data-ttu-id="ec1f1-106">Alle drei Klassen verwenden ähnliche Methoden zum Speichern und Zugreifen auf benutzerdefinierte Daten.</span><span class="sxs-lookup"><span data-stu-id="ec1f1-106">All three classes use similar methods to store and access custom data.</span></span>  
  
 <span data-ttu-id="ec1f1-107">Nur die folgenden Typen können als benutzerdefinierte Daten gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="ec1f1-107">Only the following types can be saved as custom data:</span></span>  
  
- <xref:System.Boolean>  
  
- <span data-ttu-id="ec1f1-108"><xref:System.Boolean>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-108"><xref:System.Boolean>[]</span></span>  
  
- <xref:System.Byte>  
  
- <span data-ttu-id="ec1f1-109"><xref:System.Byte>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-109"><xref:System.Byte>[]</span></span>  
  
- <xref:System.Char>  
  
- <span data-ttu-id="ec1f1-110"><xref:System.Char>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-110"><xref:System.Char>[]</span></span>  
  
- <xref:System.DateTime>  
  
- <span data-ttu-id="ec1f1-111"><xref:System.DateTime>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-111"><xref:System.DateTime>[]</span></span>  
  
- <xref:System.Decimal>  
  
- <span data-ttu-id="ec1f1-112"><xref:System.Decimal>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-112"><xref:System.Decimal>[]</span></span>  
  
- <xref:System.Double>  
  
- <span data-ttu-id="ec1f1-113"><xref:System.Double>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-113"><xref:System.Double>[]</span></span>  
  
- <xref:System.Int16>  
  
- <span data-ttu-id="ec1f1-114"><xref:System.Int16>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-114"><xref:System.Int16>[]</span></span>  
  
- <xref:System.Int32>  
  
- <span data-ttu-id="ec1f1-115"><xref:System.Int32>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-115"><xref:System.Int32>[]</span></span>  
  
- <xref:System.Int64>  
  
- <span data-ttu-id="ec1f1-116"><xref:System.Int64>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-116"><xref:System.Int64>[]</span></span>  
  
- <xref:System.Single>  
  
- <span data-ttu-id="ec1f1-117"><xref:System.Single>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-117"><xref:System.Single>[]</span></span>  
  
- <xref:System.String>  
  
- <xref:System.UInt16>  
  
- <span data-ttu-id="ec1f1-118"><xref:System.UInt16>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-118"><xref:System.UInt16>[]</span></span>  
  
- <xref:System.UInt32>  
  
- <span data-ttu-id="ec1f1-119"><xref:System.UInt32>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-119"><xref:System.UInt32>[]</span></span>  
  
- <xref:System.UInt64>  
  
- <span data-ttu-id="ec1f1-120"><xref:System.UInt64>[]</span><span class="sxs-lookup"><span data-stu-id="ec1f1-120"><xref:System.UInt64>[]</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec1f1-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ec1f1-121">Example</span></span>  
 <span data-ttu-id="ec1f1-122">Im folgenden Beispiel wird veranschaulicht, wie benutzerdefinierte Daten aus einem hinzugefügt und abgerufen werden <xref:System.Windows.Ink.StrokeCollection> .</span><span class="sxs-lookup"><span data-stu-id="ec1f1-122">The following example demonstrates how to add and retrieve custom data from a <xref:System.Windows.Ink.StrokeCollection>.</span></span>  
  
 [!code-csharp[HowToAddCustomDataToInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAddCustomDataToInk/CSharp/Window1.xaml.cs#1)]  
  
 <span data-ttu-id="ec1f1-123">Im folgenden Beispiel wird eine Anwendung erstellt, die eine <xref:System.Windows.Controls.InkCanvas> und zwei Schaltflächen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="ec1f1-123">The following example creates an application that displays an <xref:System.Windows.Controls.InkCanvas> and two buttons.</span></span>  <span data-ttu-id="ec1f1-124">Mit der Schaltfläche `switchAuthor` können zwei Stifte von zwei verschiedenen Autoren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec1f1-124">The button, `switchAuthor`, enables two pens to be used by two different authors.</span></span>  <span data-ttu-id="ec1f1-125">Die Schaltfläche `changePenColors` ändert die Farbe jedes Strichs in der <xref:System.Windows.Controls.InkCanvas> entsprechend dem Autor.</span><span class="sxs-lookup"><span data-stu-id="ec1f1-125">The button `changePenColors` changes the color of each stroke on the <xref:System.Windows.Controls.InkCanvas> according to the author.</span></span>  <span data-ttu-id="ec1f1-126">Die Anwendung definiert zwei <xref:System.Windows.Ink.DrawingAttributes> -Objekte und fügt jeder eine benutzerdefinierte Eigenschaft hinzu, die angibt, welcher Autor die gezeichnet hat <xref:System.Windows.Ink.Stroke> .</span><span class="sxs-lookup"><span data-stu-id="ec1f1-126">The application defines two <xref:System.Windows.Ink.DrawingAttributes> objects and adds a custom property to each one that indicates which author drew the <xref:System.Windows.Ink.Stroke>.</span></span>  <span data-ttu-id="ec1f1-127">Wenn der Benutzer `changePenColors` auf klickt, ändert die Anwendung die Darstellung des Strichs entsprechend dem Wert der benutzerdefinierten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ec1f1-127">When the user clicks `changePenColors`, the application changes the appearance of the stroke according to the value of the custom property.</span></span>  
  
 [!code-xaml[HowToAddCustomDataToInk#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAddCustomDataToInk/CSharp/Window1.xaml#2)]  
  
 [!code-csharp[HowToAddCustomDataToInk#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAddCustomDataToInk/CSharp/Window1.xaml.cs#3)]
