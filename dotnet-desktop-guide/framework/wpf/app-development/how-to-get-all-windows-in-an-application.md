---
title: 'Gewusst wie: alle Fenster in einer Anwendung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- window objects [WPF], getting
ms.assetid: f120f06e-993b-4a97-9657-af0d1986981f
ms.openlocfilehash: 34316f0c6f81b960a8e00131a30b9a237b9ca938
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977961"
---
# <a name="how-to-get-all-windows-in-an-application"></a><span data-ttu-id="f474f-102">Gewusst wie: alle Fenster in einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="f474f-102">How to: Get all Windows in an Application</span></span>
<span data-ttu-id="f474f-103">Dieses Beispiel zeigt, wie Sie alle <xref:System.Windows.Window> Objekte in einer Anwendung erhalten.</span><span class="sxs-lookup"><span data-stu-id="f474f-103">This example shows how to get all <xref:System.Windows.Window> objects in an application.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f474f-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f474f-104">Example</span></span>  
 <span data-ttu-id="f474f-105">Jedes instanziierte <xref:System.Windows.Window> Objekt, ob sichtbar oder nicht, wird automatisch einer Auflistung von Fenster verweisen hinzugefügt, die von verwaltet <xref:System.Windows.Application> werden und von verfügbar gemacht werden <xref:System.Windows.Application.Windows%2A> .</span><span class="sxs-lookup"><span data-stu-id="f474f-105">Every instantiated <xref:System.Windows.Window> object, whether visible or not, is automatically added to a collection of window references that is managed by <xref:System.Windows.Application>, and exposed from <xref:System.Windows.Application.Windows%2A>.</span></span>  
  
 <span data-ttu-id="f474f-106"><xref:System.Windows.Application.Windows%2A>Mithilfe des folgenden Codes können Sie alle instanziierten Fenster aufzählen:</span><span class="sxs-lookup"><span data-stu-id="f474f-106">You can enumerate <xref:System.Windows.Application.Windows%2A> to get all instantiated windows using the following code:</span></span>  
  
 [!code-csharp[HOWTOWindowManagementSnippets#GetAllWindows](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/CustomWindow.xaml.cs#getallwindows)]
 [!code-vb[HOWTOWindowManagementSnippets#GetAllWindows](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/customwindow.xaml.vb#getallwindows)]
