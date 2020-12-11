---
title: 'Gewusst wie: Extrahieren eines mit einer Datei verknüpften Symbols'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- displaying a file name and its file type icon in a ListView control [Windows Forms]
- file name extension icons [Windows Forms], displaying in a ListView
- extracting icons associated with a file type [Windows Forms]
ms.assetid: 88e2ad8b-c34f-415a-84f2-dad756b5c928
ms.openlocfilehash: 28769144b0e1c631a31c3c541747a6215f861d0e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975912"
---
# <a name="how-to-extract-the-icon-associated-with-a-file-in-windows-forms"></a><span data-ttu-id="81d98-102">Vorgehensweise: Extrahieren eines mit einer Datei verknüpften Symbols in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="81d98-102">How to: Extract the Icon Associated with a File in Windows Forms</span></span>
<span data-ttu-id="81d98-103">Viele Dateien verfügen über eingebettete Symbole, die eine visuelle Darstellung des zugeordneten Dateityps bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="81d98-103">Many files have embedded icons that provide a visual representation of the associated file type.</span></span> <span data-ttu-id="81d98-104">Beispielsweise enthalten Microsoft Word-Dokumente ein Symbol, mit dem Sie als Word-Dokumente identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="81d98-104">For example, Microsoft Word documents contain an icon that identifies them as Word documents.</span></span> <span data-ttu-id="81d98-105">Wenn Sie Dateien in einem Listen Steuerelement oder Tabellen Steuerelement anzeigen, möchten Sie möglicherweise das Symbol anzeigen, das den Dateityp neben den einzelnen Dateinamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="81d98-105">When displaying files in a list control or table control, you may want to display the icon representing the file type next to each file name.</span></span> <span data-ttu-id="81d98-106">Dies kann problemlos mithilfe der-Methode durchzuführen sein <xref:System.Drawing.Icon.ExtractAssociatedIcon%2A> .</span><span class="sxs-lookup"><span data-stu-id="81d98-106">You can do this easily by using the <xref:System.Drawing.Icon.ExtractAssociatedIcon%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="81d98-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="81d98-107">Example</span></span>  
 <span data-ttu-id="81d98-108">Im folgenden Codebeispiel wird veranschaulicht, wie das Symbol, das einer Datei zugeordnet ist, extrahiert und der Dateiname und das zugehörige Symbol in einem-Steuerelement angezeigt werden <xref:System.Windows.Forms.ListView> .</span><span class="sxs-lookup"><span data-stu-id="81d98-108">The following code example demonstrates how to extract the icon associated with a file and display the file name and its associated icon in a <xref:System.Windows.Forms.ListView> control.</span></span>  
  
 [!code-csharp[System.Drawing.Icon.ExtractAssociatedIconEx#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Icon.ExtractAssociatedIconEx/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.Icon.ExtractAssociatedIconEx#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Icon.ExtractAssociatedIconEx/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="81d98-109">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="81d98-109">Compiling the Code</span></span>  
 <span data-ttu-id="81d98-110">So kompilieren Sie das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="81d98-110">To compile the example:</span></span>  
  
- <span data-ttu-id="81d98-111">Fügen Sie den vorangehenden Code in ein Windows Form ein, und nennen Sie die `ExtractAssociatedIconExample` -Methode aus dem Konstruktor des Formulars oder der <xref:System.Windows.Forms.Form.Load> Ereignis Behandlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="81d98-111">Paste the preceding code into a Windows Form, and call the `ExtractAssociatedIconExample` method from the form's constructor or <xref:System.Windows.Forms.Form.Load> event-handling method.</span></span>  
  
     <span data-ttu-id="81d98-112">Sie müssen sicherstellen, dass das Formular den <xref:System.IO> Namespace importiert.</span><span class="sxs-lookup"><span data-stu-id="81d98-112">You will need to make sure that your form imports the <xref:System.IO> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81d98-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81d98-113">See also</span></span>

- [<span data-ttu-id="81d98-114">Bilder, Bitmaps und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="81d98-114">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="81d98-115">ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="81d98-115">ListView Control</span></span>](../controls/listview-control-windows-forms.md)
