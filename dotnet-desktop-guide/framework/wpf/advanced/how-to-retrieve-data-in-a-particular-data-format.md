---
title: 'Gewusst wie: Abrufen von Daten in einem bestimmten Datenformat'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag-and-drop [WPF], retrieving data
- DataFormats class [WPF], retrieving data
- DataObject class [WPF], retrieving data
ms.assetid: a625acf3-1144-44cd-add7-456aefc3859f
ms.openlocfilehash: b3ec1b8fa873fd449956912e9e77e98b0362cb0e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975964"
---
# <a name="how-to-retrieve-data-in-a-particular-data-format"></a>Gewusst wie: Abrufen von Daten in einem bestimmten Datenformat
In den folgenden Beispielen wird gezeigt, wie Daten aus einem Datenobjekt in einem angegebenen Format abgerufen werden.  
  
## <a name="example"></a>Beispiel  
  
### <a name="description"></a>BESCHREIBUNG  
 Der folgende Beispielcode verwendet die-Überladung <xref:System.Windows.DataObject.GetDataPresent%28System.String%29> , um zunächst zu überprüfen, ob ein angegebenes Datenformat verfügbar ist (nativ oder durch automatische Konvertierung). wenn das angegebene Format verfügbar ist, ruft das Beispiel die Daten mithilfe der- <xref:System.Windows.DataObject.GetData%28System.String%29> Methode ab.  
  
### <a name="code"></a>Code  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getspecificdataformat)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getspecificdataformat)]  
  
## <a name="example"></a>Beispiel  
  
### <a name="description"></a>BESCHREIBUNG  
 Der folgende Beispielcode verwendet die-Überladung <xref:System.Windows.DataObject.GetDataPresent%28System.String%2CSystem.Boolean%29> , um zunächst zu überprüfen, ob ein angegebenes Datenformat System intern verfügbar ist (automatisch konvertierbare Datenformate werden gefiltert). wenn das angegebene Format verfügbar ist, ruft das Beispiel die Daten mithilfe der- <xref:System.Windows.DataObject.GetData%28System.String%29> Methode ab.  
  
### <a name="code"></a>Code  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat_Native](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getspecificdataformat_native)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat_Native](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getspecificdataformat_native)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.IDataObject>
- [Übersicht über Drag &amp; Drop](drag-and-drop-overview.md)
