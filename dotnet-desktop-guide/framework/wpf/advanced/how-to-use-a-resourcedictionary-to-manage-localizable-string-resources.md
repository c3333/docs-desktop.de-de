---
title: 'Gewusst wie: Verwalten lokalisierbarer Zeichenfolgenressourcen mit einem ResourceDictionary'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- resources [WPF], packaging string resources
- packaging string resources [WPF]
- ResourceDictionary [WPF]
- localization [WPF], packaging string resources
ms.assetid: 19e7d9a5-20df-4ad3-b157-fe6515902e5e
ms.openlocfilehash: 3e7a6813497a6a4a7251b49382ed32e4a7b521da
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976275"
---
# <a name="how-to-use-a-resourcedictionary-to-manage-localizable-string-resources"></a><span data-ttu-id="3b48d-102">Gewusst wie: Verwalten lokalisierbarer Zeichenfolgenressourcen mit einem ResourceDictionary</span><span class="sxs-lookup"><span data-stu-id="3b48d-102">How to: Use a ResourceDictionary to Manage Localizable String Resources</span></span>
<span data-ttu-id="3b48d-103">Dieses Beispiel zeigt, wie Sie mit einem <xref:System.Windows.ResourceDictionary> lokalisierbare Zeichen folgen Ressourcen für Windows Presentation Foundation (WPF)-Anwendungen verpacken.</span><span class="sxs-lookup"><span data-stu-id="3b48d-103">This example shows how to use a <xref:System.Windows.ResourceDictionary> to package localizable string resources for Windows Presentation Foundation (WPF) applications.</span></span>  
  
### <a name="to-use-a-resourcedictionary-to-manage-localizable-string-resources"></a><span data-ttu-id="3b48d-104">So verwenden Sie ResourceDictionary zum Verwalten lokalisierbarer Zeichenfolgenressourcen</span><span class="sxs-lookup"><span data-stu-id="3b48d-104">To use a ResourceDictionary to manage localizable string resources</span></span>  
  
1. <span data-ttu-id="3b48d-105">Erstellen Sie eine, die die Zeichen folgen <xref:System.Windows.ResourceDictionary> enthält, die Sie lokalisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3b48d-105">Create a <xref:System.Windows.ResourceDictionary> that contains the strings you would like to localize.</span></span> <span data-ttu-id="3b48d-106">Der folgende Code enthält hierzu ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="3b48d-106">The following code shows an example.</span></span>  
  
     [!code-xaml[StringLocalizationSample#StringResourceDictionary](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/StringResources.xaml#stringresourcedictionary)]  
  
     <span data-ttu-id="3b48d-107">Dieser Code definiert eine Zeichen folgen Ressource vom `localizedMessage` Typ <xref:System.String> aus dem <xref:System> Namespace in mscorlib.dll.</span><span class="sxs-lookup"><span data-stu-id="3b48d-107">This code defines a string resource, `localizedMessage`, of type <xref:System.String>, from the <xref:System> namespace in mscorlib.dll.</span></span>  
  
2. <span data-ttu-id="3b48d-108">Fügen Sie der <xref:System.Windows.ResourceDictionary> Anwendung mit dem folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="3b48d-108">Add the <xref:System.Windows.ResourceDictionary> to your application, using the following code.</span></span>  
  
     [!code-xaml[StringLocalizationSample#ReferencingStringResourceDictionary](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/App.xaml#referencingstringresourcedictionary)]  
  
3. <span data-ttu-id="3b48d-109">Verwenden Sie die Zeichen folgen Ressource aus Markup, indem Sie [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] wie im folgenden Beispiel verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b48d-109">Use the string resource from markup, using [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] like the following.</span></span>  
  
     [!code-xaml[StringLocalizationSample#GetLocalizedResourceFromMarkup](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/MainWindow.xaml#getlocalizedresourcefrommarkup)]  
  
4. <span data-ttu-id="3b48d-110">Verwenden Sie die Zeichenfolge von CodeBehind mithilfe von Code so wie folgt.</span><span class="sxs-lookup"><span data-stu-id="3b48d-110">Use the string resource from code-behind, using code like the following.</span></span>  
  
     [!code-csharp[StringLocalizationSample#GetLocalizedResourceFromCode](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/MainWindow.xaml.cs#getlocalizedresourcefromcode)]
     [!code-vb[StringLocalizationSample#GetLocalizedResourceFromCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/StringLocalizationSample/VisualBasic/MainWindow.xaml.vb#getlocalizedresourcefromcode)]  
  
5. <span data-ttu-id="3b48d-111">Lokalisieren Sie die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3b48d-111">Localize the application.</span></span> <span data-ttu-id="3b48d-112">Weitere Informationen finden Sie unter [Lokalisieren einer Anwendung](how-to-localize-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="3b48d-112">For more information, see [Localize an Application](how-to-localize-an-application.md).</span></span>
