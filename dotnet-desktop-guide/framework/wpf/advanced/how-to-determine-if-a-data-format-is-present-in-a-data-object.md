---
title: 'Gewusst wie: Feststellen, ob ein Datenformat in einem Datenobjekt vorhanden ist'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataFormats class [WPF]
- drag-and-drop [WPF], data formats present
- data formats [WPF], determining if present
ms.assetid: e487a454-c9fc-4e53-aeaa-c458d059ad4c
ms.openlocfilehash: 4cec733490e2a9dc5d54b3b253ac38a5090ac885
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976880"
---
# <a name="how-to-determine-if-a-data-format-is-present-in-a-data-object"></a><span data-ttu-id="ec96c-102">Gewusst wie: Feststellen, ob ein Datenformat in einem Datenobjekt vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="ec96c-102">How to: Determine if a Data Format is Present in a Data Object</span></span>
<span data-ttu-id="ec96c-103">In den folgenden Beispielen wird gezeigt, wie die verschiedenen <xref:System.Windows.DataObject.GetDataPresent%2A> Methoden Überladungen verwendet werden, um abzufragen, ob ein bestimmtes Datenformat in einem Datenobjekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ec96c-103">The following examples show how to use the various <xref:System.Windows.DataObject.GetDataPresent%2A> method overloads to query whether a particular data format is present in a data object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec96c-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ec96c-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="ec96c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec96c-105">Description</span></span>  
 <span data-ttu-id="ec96c-106">Der folgende Beispielcode verwendet die- <xref:System.Windows.DataObject.GetDataPresent%28System.String%29> Überladung, um das vorhanden sein eines bestimmten Datenformats anhand der Deskriptorzeichenfolge abzufragen.</span><span class="sxs-lookup"><span data-stu-id="ec96c-106">The following example code uses the <xref:System.Windows.DataObject.GetDataPresent%28System.String%29> overload to query for the presence of a particular data format by descriptor string.</span></span>  
  
### <a name="code"></a><span data-ttu-id="ec96c-107">Code</span><span class="sxs-lookup"><span data-stu-id="ec96c-107">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_String](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_querydataformats_string)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_String](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_querydataformats_string)]  
  
## <a name="example"></a><span data-ttu-id="ec96c-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ec96c-108">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="ec96c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec96c-109">Description</span></span>  
 <span data-ttu-id="ec96c-110">Der folgende Beispielcode verwendet die- <xref:System.Windows.DataObject.GetDataPresent%28System.Type%29> Überladung, um das vorhanden sein eines bestimmten Datenformats nach Typ abzufragen.</span><span class="sxs-lookup"><span data-stu-id="ec96c-110">The following example code uses the <xref:System.Windows.DataObject.GetDataPresent%28System.Type%29> overload to query for the presence of a particular data format by type.</span></span>  
  
### <a name="code"></a><span data-ttu-id="ec96c-111">Code</span><span class="sxs-lookup"><span data-stu-id="ec96c-111">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_Type](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_querydataformats_type)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_Type](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_querydataformats_type)]  
  
## <a name="example"></a><span data-ttu-id="ec96c-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ec96c-112">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="ec96c-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec96c-113">Description</span></span>  
 <span data-ttu-id="ec96c-114">Der folgende Beispielcode verwendet die <xref:System.Windows.DataObject.GetDataPresent%28System.String%2CSystem.Boolean%29> -Überladung, um Daten anhand der Deskriptorzeichenfolge abzufragen und anzugeben, wie Auto konvertierbare Datenformate behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ec96c-114">The following example code uses the <xref:System.Windows.DataObject.GetDataPresent%28System.String%2CSystem.Boolean%29> overload to query for data by descriptor string, and specifying how to treat auto-convertible data formats.</span></span>  
  
### <a name="code"></a><span data-ttu-id="ec96c-115">Code</span><span class="sxs-lookup"><span data-stu-id="ec96c-115">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_Autoconvert](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_querydataformats_autoconvert)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_QueryDataFormats_Autoconvert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_querydataformats_autoconvert)]  
  
## <a name="see-also"></a><span data-ttu-id="ec96c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec96c-116">See also</span></span>

- <xref:System.Windows.IDataObject>
