---
title: 'Gewusst wie: Laden eines Bilds als Miniaturansicht'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- loading images as thumbnails [WPF]
- images [WPF], loading as thumbnails
- thumbnails [WPF], loading images as
ms.assetid: 02e055a0-54df-499a-b8b6-ab6ff7535cff
ms.openlocfilehash: a5b2f4b7de52203ded711e9e829886a5c25c6067
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976775"
---
# <a name="how-to-load-an-image-as-a-thumbnail"></a><span data-ttu-id="ab31d-102">Gewusst wie: Laden eines Bilds als Miniaturansicht</span><span class="sxs-lookup"><span data-stu-id="ab31d-102">How to: Load an Image as a Thumbnail</span></span>
<span data-ttu-id="ab31d-103">In den folgenden Beispielen wird gezeigt, wie ein <xref:System.Windows.Controls.Image> als Miniaturansicht geladen wird, um den Anwendungs Speicher zu sparen.</span><span class="sxs-lookup"><span data-stu-id="ab31d-103">The following examples show how to load an <xref:System.Windows.Controls.Image> as a thumbnail to conserve application memory.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ab31d-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ab31d-104">Example</span></span>  
 <span data-ttu-id="ab31d-105">Im folgenden Beispiel wird die- <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> Eigenschaft eines <xref:System.Windows.Media.Imaging.BitmapImage> in festgelegt [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] , um den zum Laden des Bilds erforderlichen Speicherplatz zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="ab31d-105">The following example sets the <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> property of a <xref:System.Windows.Media.Imaging.BitmapImage> in [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] to reduce the memory required to load the image.</span></span>  
  
 [!code-xaml[ImageElementExample_snip#ImageSimpleExampleInlineMarkup](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml#imagesimpleexampleinlinemarkup)]  
  
## <a name="example"></a><span data-ttu-id="ab31d-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ab31d-106">Example</span></span>  
 <span data-ttu-id="ab31d-107">Im folgenden Beispiel wird die- <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> Eigenschaft eines-Objekts <xref:System.Windows.Media.Imaging.BitmapImage> im Code festgelegt, um den zum Laden des Bilds erforderlichen Speicherplatz zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="ab31d-107">The following example sets the <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> property of a <xref:System.Windows.Media.Imaging.BitmapImage> in code to reduce the memory required to load the image.</span></span>  
  
 [!code-csharp[ImageElementExample_snip#ImageSimpleExampleInlineCode1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml.cs#imagesimpleexampleinlinecode1)]
 [!code-vb[ImageElementExample_snip#ImageSimpleExampleInlineCode1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample_snip/VB/ImageSimpleExample.xaml.vb#imagesimpleexampleinlinecode1)]  
  
## <a name="see-also"></a><span data-ttu-id="ab31d-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab31d-108">See also</span></span>

- [<span data-ttu-id="ab31d-109">Übersicht über die Bildverarbeitung</span><span class="sxs-lookup"><span data-stu-id="ab31d-109">Imaging Overview</span></span>](imaging-overview.md)
