---
title: 'Gewusst wie: Datenbindung an ein InkCanvas-Steuerelement'
ms.date: 03/30/2017
helpviewer_keywords:
- InkCanvas [WPF], binding data to
- binding data [WPF], to InkCanvas
ms.assetid: 8d6b4d9e-ea7f-4412-ba83-3feccec5a515
ms.openlocfilehash: 5d3fc0ed7b6176d7bc68bf20af42c311b5563908
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977588"
---
# <a name="how-to-data-bind-to-an-inkcanvas"></a><span data-ttu-id="d3859-102">Gewusst wie: Datenbindung an ein InkCanvas-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d3859-102">How to: Data Bind to an InkCanvas</span></span>
## <a name="example"></a><span data-ttu-id="d3859-103">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3859-103">Example</span></span>  
 <span data-ttu-id="d3859-104">Im folgenden Beispiel wird veranschaulicht, wie die- <xref:System.Windows.Controls.InkCanvas.Strokes%2A> Eigenschaft einer <xref:System.Windows.Controls.InkCanvas> an eine andere gebunden wird <xref:System.Windows.Controls.InkCanvas> .</span><span class="sxs-lookup"><span data-stu-id="d3859-104">The following example demonstrates how to bind the <xref:System.Windows.Controls.InkCanvas.Strokes%2A> property of an <xref:System.Windows.Controls.InkCanvas> to another <xref:System.Windows.Controls.InkCanvas>.</span></span>  
  
 [!code-xaml[InkCanvasBindingSnippet#2](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window2.xaml#2)]  
  
 <span data-ttu-id="d3859-105">Im folgenden Beispiel wird veranschaulicht, wie die- <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> Eigenschaft an eine Datenquelle gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="d3859-105">The following example demonstrates how to bind the <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> property to a data source.</span></span>  
  
 [!code-xaml[InkCanvasBindingSnippet#3](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window2.xaml#3)]  
[!code-xaml[InkCanvasBindingSnippet#4](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window2.xaml#4)]  
  
 <span data-ttu-id="d3859-106">Im folgenden Beispiel werden zwei- <xref:System.Windows.Controls.InkCanvas> Objekte in XAML deklariert und eine Datenbindung zwischen Ihnen und anderen Datenquellen hergestellt.</span><span class="sxs-lookup"><span data-stu-id="d3859-106">The following example declares two <xref:System.Windows.Controls.InkCanvas> objects in XAML and establishes data binding between them and other data sources.</span></span>  <span data-ttu-id="d3859-107">Der erste <xref:System.Windows.Controls.InkCanvas> , so genannte `ic` , wird an zwei Datenquellen gebunden.</span><span class="sxs-lookup"><span data-stu-id="d3859-107">The first <xref:System.Windows.Controls.InkCanvas>, called `ic`, is bound to two data sources.</span></span>  <span data-ttu-id="d3859-108">Die <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> für `ic` sind an- <xref:System.Windows.Controls.ListBox> Objekte gebunden, die wiederum an Arrays gebunden sind, die im XAML-Code definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d3859-108">The <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> and <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> properties on `ic` are bound to <xref:System.Windows.Controls.ListBox> objects, which are in turn bound to arrays defined in the XAML.</span></span>  <span data-ttu-id="d3859-109">Die <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> Eigenschaften, und <xref:System.Windows.Controls.InkCanvas.Strokes%2A> des zweiten <xref:System.Windows.Controls.InkCanvas> sind an die erste <xref:System.Windows.Controls.InkCanvas> , `ic` .</span><span class="sxs-lookup"><span data-stu-id="d3859-109">The <xref:System.Windows.Controls.InkCanvas.EditingMode%2A>, <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A>, and <xref:System.Windows.Controls.InkCanvas.Strokes%2A> properties of the second <xref:System.Windows.Controls.InkCanvas> are bound to the first <xref:System.Windows.Controls.InkCanvas>, `ic`.</span></span>  
  
 [!code-xaml[InkCanvasBindingSnippet#1](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window1.xaml#1)]
