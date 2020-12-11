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
# <a name="how-to-analyze-ink-with-analysis-hints"></a>Gewusst wie: Analysieren von Freihandeingaben mit Analysehinweisen

Ein [System. Windows. Ink. AnalysisHintNode](/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) stellt einen Hinweis für den [System. Windows. Ink. InkAnalyzer](/previous-versions/dotnet/netframework-3.5/ms616754(v=vs.90)) bereit, an den er angefügt wird.  Der Hinweis gilt für den von der [System. Windows. Ink. ContextNode. Location% 2a](/previous-versions/dotnet/netframework-3.5/ms594508(v=vs.90)) -Eigenschaft des [System. Windows. Ink. AnalysisHintNode](/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) angegebenen Bereich und stellt zusätzlichen Kontext für den Ink-Analyzer bereit, um die Erkennungsgenauigkeit zu verbessern. Der [System. Windows. Ink. InkAnalyzer](/previous-versions/dotnet/netframework-3.5/ms616754(v=vs.90)) wendet diese Kontextinformationen an, wenn frei Hand Eingaben aus dem Bereich des Hinweises analysiert werden.  
  
## <a name="example"></a>Beispiel  

 Das folgende Beispiel ist eine Anwendung, die mehrere [System. Windows. Ink. AnalysisHintNode](/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) -Objekte in einem Formular verwendet, das frei Hand Eingaben akzeptiert. Die Anwendung verwendet die [System. Windows. Ink. AnalysisHintNode. Faktoid% 2a](/previous-versions/dotnet/netframework-3.5/ms594341(v=vs.90)) -Eigenschaft, um Kontextinformationen für jeden Eintrag im Formular bereitzustellen.  Die Anwendung verwendet die Hintergrundanalyse, um die frei Hand Eingaben zu analysieren, und löscht die Form aller frei Hand Eingaben fünf Sekunden, nachdem der Benutzer das Hinzufügen von frei  
  
 [!code-xaml[HowToAnalyzeInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAnalyzeInk/CSharp/FormAnalyzer.xaml#1)]  
  
 [!code-csharp[HowToAnalyzeInk#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAnalyzeInk/CSharp/FormAnalyzer.xaml.cs#2)]
 [!code-vb[HowToAnalyzeInk#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToAnalyzeInk/VisualBasic/FormAnalyzer.xaml.vb#2)]
