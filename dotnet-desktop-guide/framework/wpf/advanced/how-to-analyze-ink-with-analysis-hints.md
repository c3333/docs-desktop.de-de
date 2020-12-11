---
title: 'Gewusst wie: Analysieren von Freihandeingaben mit Analysehinweisen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ink [WPF], analyzing
- analyzing ink [WPF]
- ink [WPF], AnalysisHintNode objects [WPF]
- AnalysisHintNode objects [WPF]
ms.assetid: d4421ed4-77f5-4640-829e-9f1de50b2ff2
ms.openlocfilehash: 5e94628d357a2ca75ad1b6fb7e464a3355f1fd5f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976392"
---
# <a name="how-to-analyze-ink-with-analysis-hints"></a><span data-ttu-id="f224b-102">Gewusst wie: Analysieren von Freihandeingaben mit Analysehinweisen</span><span class="sxs-lookup"><span data-stu-id="f224b-102">How to: Analyze Ink with Analysis Hints</span></span>

<span data-ttu-id="f224b-103">Ein [System. Windows. Ink. AnalysisHintNode](/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) stellt einen Hinweis für den [System. Windows. Ink. InkAnalyzer](/previous-versions/dotnet/netframework-3.5/ms616754(v=vs.90)) bereit, an den er angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f224b-103">An [System.Windows.Ink.AnalysisHintNode](/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) provides a hint for the [System.Windows.Ink.InkAnalyzer](/previous-versions/dotnet/netframework-3.5/ms616754(v=vs.90)) to which it is attached.</span></span>  <span data-ttu-id="f224b-104">Der Hinweis gilt für den von der [System. Windows. Ink. ContextNode. Location% 2a](/previous-versions/dotnet/netframework-3.5/ms594508(v=vs.90)) -Eigenschaft des [System. Windows. Ink. AnalysisHintNode](/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) angegebenen Bereich und stellt zusätzlichen Kontext für den Ink-Analyzer bereit, um die Erkennungsgenauigkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="f224b-104">The hint applies to the area specified by the [System.Windows.Ink.ContextNode.Location%2A](/previous-versions/dotnet/netframework-3.5/ms594508(v=vs.90)) property of the [System.Windows.Ink.AnalysisHintNode](/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) and provides extra context to the ink analyzer to improve recognition accuracy.</span></span> <span data-ttu-id="f224b-105">Der [System. Windows. Ink. InkAnalyzer](/previous-versions/dotnet/netframework-3.5/ms616754(v=vs.90)) wendet diese Kontextinformationen an, wenn frei Hand Eingaben aus dem Bereich des Hinweises analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="f224b-105">The [System.Windows.Ink.InkAnalyzer](/previous-versions/dotnet/netframework-3.5/ms616754(v=vs.90)) applies this context information when analyzing ink obtained from within the hint's area.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f224b-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f224b-106">Example</span></span>  

 <span data-ttu-id="f224b-107">Das folgende Beispiel ist eine Anwendung, die mehrere [System. Windows. Ink. AnalysisHintNode](/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) -Objekte in einem Formular verwendet, das frei Hand Eingaben akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="f224b-107">The following example is an application that uses multiple [System.Windows.Ink.AnalysisHintNode](/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) objects on a form that accepts ink input.</span></span> <span data-ttu-id="f224b-108">Die Anwendung verwendet die [System. Windows. Ink. AnalysisHintNode. Faktoid% 2a](/previous-versions/dotnet/netframework-3.5/ms594341(v=vs.90)) -Eigenschaft, um Kontextinformationen für jeden Eintrag im Formular bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f224b-108">The application uses the [System.Windows.Ink.AnalysisHintNode.Factoid%2A](/previous-versions/dotnet/netframework-3.5/ms594341(v=vs.90)) property to provide context information for each entry on the form.</span></span>  <span data-ttu-id="f224b-109">Die Anwendung verwendet die Hintergrundanalyse, um die frei Hand Eingaben zu analysieren, und löscht die Form aller frei Hand Eingaben fünf Sekunden, nachdem der Benutzer das Hinzufügen von frei</span><span class="sxs-lookup"><span data-stu-id="f224b-109">The application uses background analysis to analyze the ink and clears the form of all ink five seconds after the user stops adding ink.</span></span>  
  
 [!code-xaml[HowToAnalyzeInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAnalyzeInk/CSharp/FormAnalyzer.xaml#1)]  
  
 [!code-csharp[HowToAnalyzeInk#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAnalyzeInk/CSharp/FormAnalyzer.xaml.cs#2)]
 [!code-vb[HowToAnalyzeInk#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToAnalyzeInk/VisualBasic/FormAnalyzer.xaml.vb#2)]
