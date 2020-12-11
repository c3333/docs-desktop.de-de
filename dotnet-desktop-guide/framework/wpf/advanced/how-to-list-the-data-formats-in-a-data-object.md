---
title: 'Gewusst wie: Auflisten der Datenformate in einem Datenobjekt'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag-and-drop [WPF], listing data formats
- DataFormats class [WPF]
- data formats [WPF], listing
ms.assetid: 18e7ba4b-ccef-4815-ae2d-3a32891010c0
ms.openlocfilehash: f8230eac33a18a0d99cc757d54c2b901c1afe977
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977687"
---
# <a name="how-to-list-the-data-formats-in-a-data-object"></a><span data-ttu-id="9a78c-102">Gewusst wie: Auflisten der Datenformate in einem Datenobjekt</span><span class="sxs-lookup"><span data-stu-id="9a78c-102">How to: List the Data Formats in a Data Object</span></span>
<span data-ttu-id="9a78c-103">In den folgenden Beispielen wird gezeigt, wie <xref:System.Windows.DataObject.GetFormats%2A> Sie die-Methoden Überladungen verwenden, um ein Array von Zeichen folgen zu erhalten, das die einzelnen in einem Datenobjekt verfügbaren Datenformate bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9a78c-103">The following examples show how to use the <xref:System.Windows.DataObject.GetFormats%2A> method overloads get an array of strings denoting each data format that is available in a data object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9a78c-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9a78c-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="9a78c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a78c-105">Description</span></span>  
 <span data-ttu-id="9a78c-106">Der folgende Beispielcode verwendet die- <xref:System.Windows.DataObject.GetFormats%2A> Überladung, um ein Array von Zeichen folgen zu erhalten, das alle in einem Datenobjekt verfügbaren Datenformate (sowohl System eigen als auch automatisch konvertierbar) anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9a78c-106">The following example code uses the <xref:System.Windows.DataObject.GetFormats%2A> overload to get an array of strings denoting all data formats available in a data object (both native and auto-convertible).</span></span>  
  
### <a name="code"></a><span data-ttu-id="9a78c-107">Code</span><span class="sxs-lookup"><span data-stu-id="9a78c-107">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getalldataformats)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getalldataformats)]  
  
## <a name="example"></a><span data-ttu-id="9a78c-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9a78c-108">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="9a78c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a78c-109">Description</span></span>  
 <span data-ttu-id="9a78c-110">Der folgende Beispielcode verwendet die- <xref:System.Windows.DataObject.GetFormats%2A> Überladung, um ein Array von Zeichen folgen zu erhalten, das nur in einem Datenobjekt verfügbare Datenformate bezeichnet (automatisch konvertierbare Datenformate werden gefiltert).</span><span class="sxs-lookup"><span data-stu-id="9a78c-110">The following example code uses the <xref:System.Windows.DataObject.GetFormats%2A> overload to get an array of strings denoting only data formats available in a data object (auto-convertible data formats are filtered).</span></span>  
  
### <a name="code"></a><span data-ttu-id="9a78c-111">Code</span><span class="sxs-lookup"><span data-stu-id="9a78c-111">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats_NativeOnly](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getalldataformats_nativeonly)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats_NativeOnly](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getalldataformats_nativeonly)]  
  
## <a name="see-also"></a><span data-ttu-id="9a78c-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a78c-112">See also</span></span>

- <xref:System.Windows.IDataObject>
- [<span data-ttu-id="9a78c-113">Übersicht über Drag &amp; Drop</span><span class="sxs-lookup"><span data-stu-id="9a78c-113">Drag and Drop Overview</span></span>](drag-and-drop-overview.md)
