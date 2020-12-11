---
title: 'Gewusst wie: Zuschneiden eines Bilds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [WPF], cropping
- cropping images [WPF]
ms.assetid: c6bba109-c6e7-4cf8-bfe6-9cf8d01bb4fc
ms.openlocfilehash: 09a8dd01dec8bf93be627520b1c4700263427411
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977817"
---
# <a name="how-to-crop-an-image"></a><span data-ttu-id="249b4-102">Gewusst wie: Zuschneiden eines Bilds</span><span class="sxs-lookup"><span data-stu-id="249b4-102">How to: Crop an Image</span></span>

<span data-ttu-id="249b4-103">Dieses Beispiel zeigt, wie Sie ein Bild mithilfe von Zuschneiden <xref:System.Windows.Media.Imaging.CroppedBitmap> .</span><span class="sxs-lookup"><span data-stu-id="249b4-103">This example shows how to crop an image using <xref:System.Windows.Media.Imaging.CroppedBitmap>.</span></span>  
  
 <span data-ttu-id="249b4-104"><xref:System.Windows.Media.Imaging.CroppedBitmap> wird hauptsächlich verwendet, wenn Sie eine abgeschnittene Version eines Bilds codieren, um Sie in eine Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="249b4-104"><xref:System.Windows.Media.Imaging.CroppedBitmap> is primarily used when encoding a cropped version of an image to save out to a file.</span></span> <span data-ttu-id="249b4-105">Informationen zum Zuschneiden eines Bilds zu Anzeige Zwecken finden Sie im Thema Gewusst [wie: Erstellen eines Clip-Bereichs](/previous-versions/dotnet/netframework-3.5/ms746710(v=vs.90)) .</span><span class="sxs-lookup"><span data-stu-id="249b4-105">To crop an image for display purposes see the [How to: Create a Clip Region](/previous-versions/dotnet/netframework-3.5/ms746710(v=vs.90)) topic.</span></span>  
  
## <a name="example"></a><span data-ttu-id="249b4-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="249b4-106">Example</span></span>  

 <span data-ttu-id="249b4-107">Im folgenden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] werden die in den Beispielen unten verwendeten Ressourcen definiert.</span><span class="sxs-lookup"><span data-stu-id="249b4-107">The following [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] defines resources used within the samples below.</span></span>  
  
 [!code-xaml[imageelementexample#CroppedXAML1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml1)]  
  
 <span data-ttu-id="249b4-108">Im folgenden Beispiel wird ein Bild mithilfe von <xref:System.Windows.Media.Imaging.CroppedBitmap> als Quelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="249b4-108">The following example creates an image using a <xref:System.Windows.Media.Imaging.CroppedBitmap> as its source.</span></span>  
  
 [!code-xaml[imageelementexample#CroppedXAML2](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml2)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp1)]
 [!code-vb[imageelementexample#CroppedCSharp1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp1)]  
  
 <span data-ttu-id="249b4-109"><xref:System.Windows.Media.Imaging.CroppedBitmap>Kann auch als Quelle eines anderen verwendet werden, wobei <xref:System.Windows.Media.Imaging.CroppedBitmap> das Zuschneiden Verkettung wird.</span><span class="sxs-lookup"><span data-stu-id="249b4-109">The <xref:System.Windows.Media.Imaging.CroppedBitmap> can also be used as the source of another <xref:System.Windows.Media.Imaging.CroppedBitmap>, chaining the cropping.</span></span> <span data-ttu-id="249b4-110">Beachten Sie, dass die <xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A> Werte verwendet, die relativ zur zugeschnittenen Quell Bitmap und nicht zum Anfangs Bild sind.</span><span class="sxs-lookup"><span data-stu-id="249b4-110">Note that the <xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A> uses values that are relative to the source cropped bitmap and not the initial image.</span></span>  
  
 [!code-xaml[imageelementexample#CroppedXAML3](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml3)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp2](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp2)]
 [!code-vb[imageelementexample#CroppedCSharp2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp2)]  
  
## <a name="see-also"></a><span data-ttu-id="249b4-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="249b4-111">See also</span></span>

- <span data-ttu-id="249b4-112">[Gewusst wie: Erstellen eines Clip-Bereichs](/previous-versions/dotnet/netframework-3.5/ms746710(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="249b4-112">[How to: Create a Clip Region](/previous-versions/dotnet/netframework-3.5/ms746710(v=vs.90))</span></span>
