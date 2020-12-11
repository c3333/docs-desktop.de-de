---
title: 'Gewusst wie: Speichern von mehreren Datenformaten in einem Datenobjekt'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataObject class [WPF], storing multiple formats
- DataFormats class [WPF], storing multiple formats
- drag-and-drop [WPF], storing multiple formats
ms.assetid: 941ace29-29c4-4c26-b75b-ea7d06aa0d69
ms.openlocfilehash: 3f8e7233e1d28fec1f7dac114b04287aa3aff49f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974872"
---
# <a name="how-to-store-multiple-data-formats-in-a-data-object"></a><span data-ttu-id="bdfc8-102">Gewusst wie: Speichern von mehreren Datenformaten in einem Datenobjekt</span><span class="sxs-lookup"><span data-stu-id="bdfc8-102">How to: Store Multiple Data Formats in a Data Object</span></span>
<span data-ttu-id="bdfc8-103">Im folgenden Beispiel wird gezeigt, wie die- <xref:System.Windows.DataObject.SetData%28System.String%2CSystem.Object%29> Methode zum Hinzufügen von Daten zu einem Datenobjekt in mehreren Formaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-103">The following example shows how to use the <xref:System.Windows.DataObject.SetData%28System.String%2CSystem.Object%29> method to add data to a data object in multiple formats.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bdfc8-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bdfc8-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="bdfc8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdfc8-105">Description</span></span>  
  
### <a name="code"></a><span data-ttu-id="bdfc8-106">Code</span><span class="sxs-lookup"><span data-stu-id="bdfc8-106">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_StoreMultipleFormats](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_storemultipleformats)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_StoreMultipleFormats](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_storemultipleformats)]  
  
## <a name="see-also"></a><span data-ttu-id="bdfc8-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdfc8-107">See also</span></span>

- <xref:System.Windows.IDataObject>
- [<span data-ttu-id="bdfc8-108">Übersicht über Drag &amp; Drop</span><span class="sxs-lookup"><span data-stu-id="bdfc8-108">Drag and Drop Overview</span></span>](drag-and-drop-overview.md)
