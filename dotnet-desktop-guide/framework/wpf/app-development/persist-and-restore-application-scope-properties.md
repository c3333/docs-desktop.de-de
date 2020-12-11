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
# <a name="how-to-persist-and-restore-application-scope-properties-across-application-sessions"></a><span data-ttu-id="941a6-102">Gewusst wie: Beibehalten und Wiederherstellen von Eigenschaften für den Anwendungsbereich über mehrere Anwendungssitzungen</span><span class="sxs-lookup"><span data-stu-id="941a6-102">How to: Persist and Restore Application-Scope Properties Across Application Sessions</span></span>
<span data-ttu-id="941a6-103">Dieses Beispiel zeigt, wie Sie die Eigenschaften des Anwendungsbereichs beibehalten, wenn eine Anwendung heruntergefahren wird, und wie Sie die Eigenschaften des Anwendungsbereichs beim nächsten Start einer Anwendung wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="941a6-103">This example shows how to persist application-scope properties when an application shuts down, and how to restore application-scope properties when an application is next launch.</span></span>  
  
## <a name="example"></a><span data-ttu-id="941a6-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="941a6-104">Example</span></span>  
 <span data-ttu-id="941a6-105">Die Anwendung speichert die Eigenschaften des Anwendungsbereichs auf und stellt Sie aus dem isolierten Speicher wieder her.</span><span class="sxs-lookup"><span data-stu-id="941a6-105">The application persists application-scope properties to, and restores them from, isolated storage.</span></span> <span data-ttu-id="941a6-106">Isolierter Speicher ist ein geschützter Speicherbereich, der von Anwendungen ohne Datei Zugriffsberechtigung sicher verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="941a6-106">Isolated storage is a protected storage area that can safely be used by applications without file access permission.</span></span>  <span data-ttu-id="941a6-107">Die Datei *app. XAML* definiert die `App_Startup` -Methode als Handler für das <xref:System.Windows.Application.Startup?displayProperty=nameWithType> -Ereignis und die- `App_Exit` Methode als Handler für das-  <xref:System.Windows.Application.Exit?displayProperty=nameWithType> Ereignis, wie in den hervorgehobenen Zeilen des ersten Beispiels gezeigt.</span><span class="sxs-lookup"><span data-stu-id="941a6-107">The *App.xaml* file defines the `App_Startup` method as the handler for the <xref:System.Windows.Application.Startup?displayProperty=nameWithType> event, and the `App_Exit` method as the handler for the  <xref:System.Windows.Application.Exit?displayProperty=nameWithType> event, as shown in the highlighted lines of the first example.</span></span> <span data-ttu-id="941a6-108">Das zweite Beispiel zeigt einen Teil der *app.XAML.cs* -und *app. XAML. vb* -Dateien, die den Code für die `App_Startup` -Methode hervorheben, die Eigenschaften für den Anwendungsbereich wiederherstellt, und die `App_Exit` -Methode, die Anwendungsbereichs Eigenschaften speichert.</span><span class="sxs-lookup"><span data-stu-id="941a6-108">The second example shows a portion of the *App.xaml.cs* and *App.xaml.vb* files that highlights the code for the `App_Startup` method, which restores application-scope properties, and the `App_Exit` method, which saves application-scope properties.</span></span>

 [!code-xaml[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesXAML1](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml?highlight=1-7)]
  
 [!code-csharp[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND1](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml.cs?highlight=17-55)]
 [!code-vb[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/visualbasic/application.xaml.vb?highlight=14-45)]
