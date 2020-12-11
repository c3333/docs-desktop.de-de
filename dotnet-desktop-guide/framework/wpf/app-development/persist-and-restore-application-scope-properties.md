---
title: 'Gewusst wie: Beibehalten und Wiederherstellen von Eigenschaften für den Anwendungsbereich über mehrere Anwendungssitzungen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- application-scope properties [WPF], persisting
- persisting application-scope properties [WPF]
- properties [WPF], persisting
- restoring application-scope properties [WPF]
- properties [WPF], restoring
- application-scope properties [WPF], restoring
ms.assetid: 55d5904a-f444-4eb5-abd3-6bc74dd14226
ms.openlocfilehash: d9c2dda2745e7528902b6b1c4f46d17264d1a8d8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977386"
---
# <a name="how-to-persist-and-restore-application-scope-properties-across-application-sessions"></a>Gewusst wie: Beibehalten und Wiederherstellen von Eigenschaften für den Anwendungsbereich über mehrere Anwendungssitzungen
Dieses Beispiel zeigt, wie Sie die Eigenschaften des Anwendungsbereichs beibehalten, wenn eine Anwendung heruntergefahren wird, und wie Sie die Eigenschaften des Anwendungsbereichs beim nächsten Start einer Anwendung wiederherstellen.  
  
## <a name="example"></a>Beispiel  
 Die Anwendung speichert die Eigenschaften des Anwendungsbereichs auf und stellt Sie aus dem isolierten Speicher wieder her. Isolierter Speicher ist ein geschützter Speicherbereich, der von Anwendungen ohne Datei Zugriffsberechtigung sicher verwendet werden kann.  Die Datei *app. XAML* definiert die `App_Startup` -Methode als Handler für das <xref:System.Windows.Application.Startup?displayProperty=nameWithType> -Ereignis und die- `App_Exit` Methode als Handler für das-  <xref:System.Windows.Application.Exit?displayProperty=nameWithType> Ereignis, wie in den hervorgehobenen Zeilen des ersten Beispiels gezeigt. Das zweite Beispiel zeigt einen Teil der *app.XAML.cs* -und *app. XAML. vb* -Dateien, die den Code für die `App_Startup` -Methode hervorheben, die Eigenschaften für den Anwendungsbereich wiederherstellt, und die `App_Exit` -Methode, die Anwendungsbereichs Eigenschaften speichert.

 [!code-xaml[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesXAML1](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml?highlight=1-7)]
  
 [!code-csharp[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND1](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml.cs?highlight=17-55)]
 [!code-vb[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/visualbasic/application.xaml.vb?highlight=14-45)]
