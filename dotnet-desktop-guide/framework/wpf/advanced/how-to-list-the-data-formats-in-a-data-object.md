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
# <a name="how-to-list-the-data-formats-in-a-data-object"></a>Gewusst wie: Auflisten der Datenformate in einem Datenobjekt
In den folgenden Beispielen wird gezeigt, wie <xref:System.Windows.DataObject.GetFormats%2A> Sie die-Methoden Überladungen verwenden, um ein Array von Zeichen folgen zu erhalten, das die einzelnen in einem Datenobjekt verfügbaren Datenformate bezeichnet.  
  
## <a name="example"></a>Beispiel  
  
### <a name="description"></a>BESCHREIBUNG  
 Der folgende Beispielcode verwendet die- <xref:System.Windows.DataObject.GetFormats%2A> Überladung, um ein Array von Zeichen folgen zu erhalten, das alle in einem Datenobjekt verfügbaren Datenformate (sowohl System eigen als auch automatisch konvertierbar) anzeigt.  
  
### <a name="code"></a>Code  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getalldataformats)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getalldataformats)]  
  
## <a name="example"></a>Beispiel  
  
### <a name="description"></a>BESCHREIBUNG  
 Der folgende Beispielcode verwendet die- <xref:System.Windows.DataObject.GetFormats%2A> Überladung, um ein Array von Zeichen folgen zu erhalten, das nur in einem Datenobjekt verfügbare Datenformate bezeichnet (automatisch konvertierbare Datenformate werden gefiltert).  
  
### <a name="code"></a>Code  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats_NativeOnly](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getalldataformats_nativeonly)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetAllDataFormats_NativeOnly](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getalldataformats_nativeonly)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.IDataObject>
- [Übersicht über Drag &amp; Drop](drag-and-drop-overview.md)
