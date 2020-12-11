---
title: 'Gewusst wie: Verwenden eines Ressourcenwörterbuchs für den Anwendungsbereich'
description: Erfahren Sie, wie Sie ein benutzerdefiniertes Ressourcen Wörterbuch im Anwendungsbereich in Windows Presentation Foundation (WPF) definieren und verwenden.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- dictionaries [WPF], resource
- resource dictionaries [WPF], application-scope
- application-scope resource dictionaries
ms.assetid: 53857682-bd2c-4f2c-8f25-1307d0b451a2
ms.openlocfilehash: 7423cf03e5ebb94eb9ad5f3a0ee0bd5e524cccba
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975080"
---
# <a name="how-to-use-an-application-scope-resource-dictionary"></a><span data-ttu-id="a66ab-103">Gewusst wie: Verwenden eines Ressourcenwörterbuchs für den Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="a66ab-103">How to: Use an Application-Scope Resource Dictionary</span></span>

<span data-ttu-id="a66ab-104">In diesem Beispiel wird gezeigt, wie ein benutzerdefiniertes Ressourcenverzeichnis für den Anwendungsbereich definiert und verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a66ab-104">This example shows how to define and use an application-scope custom resource dictionary.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a66ab-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a66ab-105">Example</span></span>  

 <span data-ttu-id="a66ab-106"><xref:System.Windows.Application> macht einen Anwendungsbereichs Speicher für freigegebene Ressourcen verfügbar: <xref:System.Windows.Application.Resources%2A> .</span><span class="sxs-lookup"><span data-stu-id="a66ab-106"><xref:System.Windows.Application> exposes an application-scope store for shared resources: <xref:System.Windows.Application.Resources%2A>.</span></span> <span data-ttu-id="a66ab-107">Standardmäßig wird die- <xref:System.Windows.Application.Resources%2A> Eigenschaft mit einer Instanz des-Typs initialisiert <xref:System.Windows.ResourceDictionary> .</span><span class="sxs-lookup"><span data-stu-id="a66ab-107">By default, the <xref:System.Windows.Application.Resources%2A> property is initialized with an instance of the <xref:System.Windows.ResourceDictionary> type.</span></span> <span data-ttu-id="a66ab-108">Diese Instanz wird verwendet, wenn Sie mithilfe von Eigenschaften für den Anwendungsbereich erhalten und festlegen <xref:System.Windows.Application.Resources%2A> .</span><span class="sxs-lookup"><span data-stu-id="a66ab-108">You use this instance when you get and set application-scope properties using <xref:System.Windows.Application.Resources%2A>.</span></span> <span data-ttu-id="a66ab-109">Weitere Informationen finden Sie unter Gewusst [wie: Einrichten und Festlegen einer Application-Scope Ressource](/previous-versions/dotnet/netframework-4.0/aa348547(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="a66ab-109">For more information, see [How to: Get and Set an Application-Scope Resource](/previous-versions/dotnet/netframework-4.0/aa348547(v=vs.100)).</span></span>
  
 <span data-ttu-id="a66ab-110">Wenn Sie über mehrere Ressourcen verfügen, die Sie mithilfe von festgelegt haben <xref:System.Windows.Application.Resources%2A> , können Sie stattdessen ein benutzerdefiniertes Ressourcen Wörterbuch verwenden, um diese Ressourcen zu speichern und stattdessen festzulegen <xref:System.Windows.Application.Resources%2A> .</span><span class="sxs-lookup"><span data-stu-id="a66ab-110">If you have multiple resources that you set using <xref:System.Windows.Application.Resources%2A>, you can instead use a custom resource dictionary to store those resources and set <xref:System.Windows.Application.Resources%2A> with it instead.</span></span> <span data-ttu-id="a66ab-111">Das folgende Beispiel zeigt, wie Sie mit XAML ein benutzerdefiniertes Ressourcen Wörterbuch deklarieren.</span><span class="sxs-lookup"><span data-stu-id="a66ab-111">The following shows how you declare a custom resource dictionary using XAML.</span></span>
  
 [!code-xaml[HOWTOResourceDictionaries#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MyResourceDictionary.xaml#1)]  
  
 <span data-ttu-id="a66ab-112">Durch das austauschen ganzer Ressourcen Wörterbücher mithilfe <xref:System.Windows.Application.Resources%2A> von können Sie Anwendungsbereichs Designs unterstützen, wobei jedes Design von einem einzigen Ressourcen Wörterbuch gekapselt wird.</span><span class="sxs-lookup"><span data-stu-id="a66ab-112">Swapping entire resource dictionaries using <xref:System.Windows.Application.Resources%2A> allows you to support application-scope themes, where each theme is encapsulated by a single resource dictionary.</span></span> <span data-ttu-id="a66ab-113">Im folgenden Beispiel wird das Festlegen der <xref:System.Windows.ResourceDictionary> veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a66ab-113">The following example shows how to set the <xref:System.Windows.ResourceDictionary>.</span></span>  
  
 [!code-xaml[HOWTOResourceDictionaries#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/App.xaml#2)]  
  
 <span data-ttu-id="a66ab-114">Im folgenden wird gezeigt, wie Sie Ressourcen im Anwendungsbereich aus dem Ressourcen Wörterbuch, das von verfügbar gemacht wird, <xref:System.Windows.Application.Resources%2A> in XAML erhalten.</span><span class="sxs-lookup"><span data-stu-id="a66ab-114">The following shows how you can get application-scope resources from the resource dictionary exposed by <xref:System.Windows.Application.Resources%2A> in XAML.</span></span>  
  
 [!code-xaml[HOWTOResourceDictionaries#4](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MainWindow.xaml#4)]  
  
 <span data-ttu-id="a66ab-115">Im Folgenden wird gezeigt, wie Sie die Ressourcen auch in Code abrufen können.</span><span class="sxs-lookup"><span data-stu-id="a66ab-115">The following shows how you can also get the resources in code.</span></span>  
  
 [!code-csharp[HOWTOResourceDictionaries#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MainWindow.xaml.cs#3)]
 [!code-vb[HOWTOResourceDictionaries#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToResourceDictionaries/VB/MainWindow.xaml.vb#3)]  
  
 <span data-ttu-id="a66ab-116">Bei der Verwendung von müssen zwei Aspekte berücksichtigt werden <xref:System.Windows.Application.Resources%2A> .</span><span class="sxs-lookup"><span data-stu-id="a66ab-116">There are two considerations to make when using <xref:System.Windows.Application.Resources%2A>.</span></span> <span data-ttu-id="a66ab-117">Zuerst ist der Wörterbuch *Schlüssel* ein Objekt, sodass Sie genau dieselbe Objektinstanz verwenden müssen, wenn Sie einen Eigenschafts Wert festlegen und erhalten.</span><span class="sxs-lookup"><span data-stu-id="a66ab-117">First, the dictionary *key* is an object, so you must use exactly the same object instance when both setting and getting a property value.</span></span> <span data-ttu-id="a66ab-118">(Beachten Sie, dass bei Verwendung einer Zeichenfolge beim Schlüssel die Groß-/Kleinschreibung beachtet wird.) Zweitens ist der Wörterbuch *Wert* ein Objekt, sodass Sie den Wert in den gewünschten Typ konvertieren müssen, wenn Sie einen Eigenschafts Wert erhalten.</span><span class="sxs-lookup"><span data-stu-id="a66ab-118">(Note that the key is case-sensitive when using a string.) Second, the dictionary *value* is an object, so you will have to convert the value to the desired type when getting a property value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a66ab-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a66ab-119">See also</span></span>

- <xref:System.Windows.ResourceDictionary>
- <xref:System.Windows.Application.Resources%2A>
- [<span data-ttu-id="a66ab-120">XAML-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a66ab-120">XAML Resources</span></span>](/dotnet/desktop-wpf/fundamentals/xaml-resources-define)
- [<span data-ttu-id="a66ab-121">Zusammengeführte Ressourcenwörterbücher</span><span class="sxs-lookup"><span data-stu-id="a66ab-121">Merged Resource Dictionaries</span></span>](../advanced/merged-resource-dictionaries.md)
