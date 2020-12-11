---
title: 'Gewusst wie: Erstellen eines Datenobjekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataObject class [WPF], creating
- data objects [WPF], creating
- drag-and-drop [WPF], creating data objects
ms.assetid: 022fa142-717d-4fea-a53c-3b52e9d91aff
ms.openlocfilehash: deae8751518d9322e8d924a1b1fcbc20e25b35ed
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977595"
---
# <a name="how-to-create-a-data-object"></a><span data-ttu-id="53e34-102">Gewusst wie: Erstellen eines Datenobjekts</span><span class="sxs-lookup"><span data-stu-id="53e34-102">How to: Create a Data Object</span></span>
<span data-ttu-id="53e34-103">Die folgenden Beispiele zeigen verschiedene Möglichkeiten zum Erstellen eines Datenobjekts mithilfe der von der-Klasse bereitgestellten Konstruktoren <xref:System.Windows.DataObject> .</span><span class="sxs-lookup"><span data-stu-id="53e34-103">The following examples show various ways to create a data object using the constructors provided by the <xref:System.Windows.DataObject> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="53e34-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="53e34-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="53e34-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53e34-105">Description</span></span>  
 <span data-ttu-id="53e34-106">Der folgende Beispielcode erstellt ein neues Datenobjekt und verwendet einen der überladenen Konstruktoren ( <xref:System.Windows.DataObject.%23ctor%28System.Object%29> ), um das Datenobjekt mit einer Zeichenfolge zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="53e34-106">The following example code creates a new data object and uses one of the overloaded constructors (<xref:System.Windows.DataObject.%23ctor%28System.Object%29>) to initialize the data object with a string.</span></span>  <span data-ttu-id="53e34-107">In diesem Fall wird ein entsprechendes Datenformat automatisch gemäß dem Typ der gespeicherten Daten bestimmt, und die automatische Typumwandlung der gespeicherten Daten ist standardmäßig zulässig.</span><span class="sxs-lookup"><span data-stu-id="53e34-107">In this case, an appropriate data format is determined automatically according to the stored data's type, and auto-converting of the stored data is allowed by default.</span></span>  
  
### <a name="code"></a><span data-ttu-id="53e34-108">Code</span><span class="sxs-lookup"><span data-stu-id="53e34-108">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Simple](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_simple)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Simple](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_simple)]  
  
### <a name="description"></a><span data-ttu-id="53e34-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53e34-109">Description</span></span>  
 <span data-ttu-id="53e34-110">Der folgende Beispielcode ist eine komprimierte Version des oben gezeigten Codes.</span><span class="sxs-lookup"><span data-stu-id="53e34-110">The following example code is a condensed version of the code shown above.</span></span>  
  
### <a name="code"></a><span data-ttu-id="53e34-111">Code</span><span class="sxs-lookup"><span data-stu-id="53e34-111">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Simple_Condensed](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_simple_condensed)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Simple_Condensed](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_simple_condensed)]  
  
## <a name="example"></a><span data-ttu-id="53e34-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="53e34-112">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="53e34-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53e34-113">Description</span></span>  
 <span data-ttu-id="53e34-114">Der folgende Beispielcode erstellt ein neues Datenobjekt und verwendet einen der überladenen Konstruktoren ( <xref:System.Windows.DataObject.%23ctor%28System.String%2CSystem.Object%29> ), um das Datenobjekt mit einer Zeichenfolge und einem angegebenen Datenformat zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="53e34-114">The following example code creates a new data object and uses one of the overloaded constructors (<xref:System.Windows.DataObject.%23ctor%28System.String%2CSystem.Object%29>) to initialize the data object with a string and a specified data format.</span></span>  <span data-ttu-id="53e34-115">In diesem Fall wird das Datenformat durch eine Zeichenfolge angegeben; die- <xref:System.Windows.DataFormats> Klasse stellt einen Satz vordefinierter typzeichenfolgen bereit.</span><span class="sxs-lookup"><span data-stu-id="53e34-115">In this case the data format is specified by a string; the <xref:System.Windows.DataFormats> class provides a set of pre-defined type strings.</span></span> <span data-ttu-id="53e34-116">Die automatische Typumwandlung der gespeicherten Daten ist standardmäßig zulässig.</span><span class="sxs-lookup"><span data-stu-id="53e34-116">Auto-converting of the stored data is allowed by default.</span></span>  
  
### <a name="code"></a><span data-ttu-id="53e34-117">Code</span><span class="sxs-lookup"><span data-stu-id="53e34-117">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_TypeString](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_typestring)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_TypeString](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_typestring)]  
  
### <a name="description"></a><span data-ttu-id="53e34-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53e34-118">Description</span></span>  
 <span data-ttu-id="53e34-119">Der folgende Beispielcode ist eine komprimierte Version des oben gezeigten Codes.</span><span class="sxs-lookup"><span data-stu-id="53e34-119">The following example code is a condensed version of the code shown above.</span></span>  
  
### <a name="code"></a><span data-ttu-id="53e34-120">Code</span><span class="sxs-lookup"><span data-stu-id="53e34-120">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_TypeString_Condensed](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_typestring_condensed)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_TypeString_Condensed](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_typestring_condensed)]  
  
## <a name="example"></a><span data-ttu-id="53e34-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="53e34-121">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="53e34-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53e34-122">Description</span></span>  
 <span data-ttu-id="53e34-123">Der folgende Beispielcode erstellt ein neues Datenobjekt und verwendet einen der überladenen Konstruktoren ( <xref:System.Windows.DataObject.%23ctor%2A> ), um das Datenobjekt mit einer Zeichenfolge und einem angegebenen Datenformat zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="53e34-123">The following example code creates a new data object and uses one of the overloaded constructors (<xref:System.Windows.DataObject.%23ctor%2A>) to initialize the data object with a string and a specified data format.</span></span>  <span data-ttu-id="53e34-124">In diesem Fall wird das Datenformat durch einen <xref:System.Type> Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="53e34-124">In this case the data format is specified by a <xref:System.Type> parameter.</span></span>  <span data-ttu-id="53e34-125">Die automatische Typumwandlung der gespeicherten Daten ist standardmäßig zulässig.</span><span class="sxs-lookup"><span data-stu-id="53e34-125">Auto-converting of the stored data is allowed by default.</span></span>  
  
### <a name="code"></a><span data-ttu-id="53e34-126">Code</span><span class="sxs-lookup"><span data-stu-id="53e34-126">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Type](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_type)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Type](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_type)]  
  
### <a name="description"></a><span data-ttu-id="53e34-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53e34-127">Description</span></span>  
 <span data-ttu-id="53e34-128">Der folgende Beispielcode ist eine komprimierte Version des oben gezeigten Codes.</span><span class="sxs-lookup"><span data-stu-id="53e34-128">The following example code is a condensed version of the code shown above.</span></span>  
  
### <a name="code"></a><span data-ttu-id="53e34-129">Code</span><span class="sxs-lookup"><span data-stu-id="53e34-129">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Type_Condensed](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_type_condensed)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Type_Condensed](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_type_condensed)]  
  
## <a name="example"></a><span data-ttu-id="53e34-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="53e34-130">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="53e34-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53e34-131">Description</span></span>  
 <span data-ttu-id="53e34-132">Der folgende Beispielcode erstellt ein neues Datenobjekt und verwendet einen der überladenen Konstruktoren ( <xref:System.Windows.DataObject.%23ctor%28System.String%2CSystem.Object%2CSystem.Boolean%29> ), um das Datenobjekt mit einer Zeichenfolge und einem angegebenen Datenformat zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="53e34-132">The following example code creates a new data object and uses one of the overloaded constructors (<xref:System.Windows.DataObject.%23ctor%28System.String%2CSystem.Object%2CSystem.Boolean%29>) to initialize the data object with a string and a specified data format.</span></span>  <span data-ttu-id="53e34-133">In diesem Fall wird das Datenformat durch eine Zeichenfolge angegeben; die- <xref:System.Windows.DataFormats> Klasse stellt einen Satz vordefinierter typzeichenfolgen bereit.</span><span class="sxs-lookup"><span data-stu-id="53e34-133">In this case the data format is specified by a string; the <xref:System.Windows.DataFormats> class provides a set of pre-defined type strings.</span></span> <span data-ttu-id="53e34-134">Diese bestimmte Konstruktorüberladung ermöglicht dem Aufrufer, anzugeben, ob die automatische Konvertierungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="53e34-134">This particular constructor overload enables the caller to specify whether auto-converting is allowed.</span></span>  
  
### <a name="code"></a><span data-ttu-id="53e34-135">Code</span><span class="sxs-lookup"><span data-stu-id="53e34-135">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_AutoConvert](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_autoconvert)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_AutoConvert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_autoconvert)]  
  
### <a name="description"></a><span data-ttu-id="53e34-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53e34-136">Description</span></span>  
 <span data-ttu-id="53e34-137">Der folgende Beispielcode ist eine komprimierte Version des oben gezeigten Codes.</span><span class="sxs-lookup"><span data-stu-id="53e34-137">The following example code is a condensed version of the code shown above.</span></span>  
  
### <a name="code"></a><span data-ttu-id="53e34-138">Code</span><span class="sxs-lookup"><span data-stu-id="53e34-138">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_AutoConvert_Condensed](~/samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_autoconvert_condensed)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_AutoConvert_Condensed](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_autoconvert_condensed)]  
  
## <a name="see-also"></a><span data-ttu-id="53e34-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53e34-139">See also</span></span>

- <xref:System.Windows.IDataObject>
