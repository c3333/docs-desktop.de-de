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
# <a name="how-to-use-a-resourcedictionary-to-manage-localizable-string-resources"></a>Gewusst wie: Verwalten lokalisierbarer Zeichenfolgenressourcen mit einem ResourceDictionary
Dieses Beispiel zeigt, wie Sie mit einem <xref:System.Windows.ResourceDictionary> lokalisierbare Zeichen folgen Ressourcen für Windows Presentation Foundation (WPF)-Anwendungen verpacken.  
  
### <a name="to-use-a-resourcedictionary-to-manage-localizable-string-resources"></a>So verwenden Sie ResourceDictionary zum Verwalten lokalisierbarer Zeichenfolgenressourcen  
  
1. Erstellen Sie eine, die die Zeichen folgen <xref:System.Windows.ResourceDictionary> enthält, die Sie lokalisieren möchten. Der folgende Code enthält hierzu ein Beispiel.  
  
     [!code-xaml[StringLocalizationSample#StringResourceDictionary](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/StringResources.xaml#stringresourcedictionary)]  
  
     Dieser Code definiert eine Zeichen folgen Ressource vom `localizedMessage` Typ <xref:System.String> aus dem <xref:System> Namespace in mscorlib.dll.  
  
2. Fügen Sie der <xref:System.Windows.ResourceDictionary> Anwendung mit dem folgenden Code hinzu.  
  
     [!code-xaml[StringLocalizationSample#ReferencingStringResourceDictionary](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/App.xaml#referencingstringresourcedictionary)]  
  
3. Verwenden Sie die Zeichen folgen Ressource aus Markup, indem Sie [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] wie im folgenden Beispiel verwenden.  
  
     [!code-xaml[StringLocalizationSample#GetLocalizedResourceFromMarkup](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/MainWindow.xaml#getlocalizedresourcefrommarkup)]  
  
4. Verwenden Sie die Zeichenfolge von CodeBehind mithilfe von Code so wie folgt.  
  
     [!code-csharp[StringLocalizationSample#GetLocalizedResourceFromCode](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/MainWindow.xaml.cs#getlocalizedresourcefromcode)]
     [!code-vb[StringLocalizationSample#GetLocalizedResourceFromCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/StringLocalizationSample/VisualBasic/MainWindow.xaml.vb#getlocalizedresourcefromcode)]  
  
5. Lokalisieren Sie die Anwendung. Weitere Informationen finden Sie unter [Lokalisieren einer Anwendung](how-to-localize-an-application.md).
