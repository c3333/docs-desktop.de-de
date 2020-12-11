---
title: 'Vorgehensweise: Auflisten installierter Encoder'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image codecs [Windows Forms], listing
- image encoders [Windows Forms], listing
ms.assetid: 49e8e4e9-7a67-42d9-86bf-08821cdc282e
ms.openlocfilehash: 2634dd96b3aa5edcecde092919eb328b7f3dadc3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976155"
---
# <a name="how-to-list-installed-encoders"></a><span data-ttu-id="c9109-102">Vorgehensweise: Auflisten installierter Encoder</span><span class="sxs-lookup"><span data-stu-id="c9109-102">How to: List Installed Encoders</span></span>
<span data-ttu-id="c9109-103">Möglicherweise möchten Sie die auf einem Computer verfügbaren Bild Encoder auflisten, um zu bestimmen, ob Ihre Anwendung in einem bestimmten Bild Dateiformat gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c9109-103">You may want to list the image encoders available on a computer, to determine whether your application can save to a particular image file format.</span></span> <span data-ttu-id="c9109-104">Die- <xref:System.Drawing.Imaging.ImageCodecInfo> Klasse stellt die <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> statischen-Methoden bereit, damit Sie bestimmen können, welche Bild Encoder verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c9109-104">The <xref:System.Drawing.Imaging.ImageCodecInfo> class provides the <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> static methods so that you can determine which image encoders are available.</span></span> <span data-ttu-id="c9109-105"><xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> Gibt ein Array von- <xref:System.Drawing.Imaging.ImageCodecInfo> Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="c9109-105"><xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> returns an array of <xref:System.Drawing.Imaging.ImageCodecInfo> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c9109-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c9109-106">Example</span></span>  
 <span data-ttu-id="c9109-107">Im folgenden Codebeispiel wird die Liste der installierten Encoder und deren Eigenschaftswerte ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="c9109-107">The following code example outputs the list of installed encoders and their property values.</span></span>  
  
 [!code-csharp[UsingImageEncodersDecoders#1](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#1)]
 [!code-vb[UsingImageEncodersDecoders#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c9109-108">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="c9109-108">Compiling the Code</span></span>  
 <span data-ttu-id="c9109-109">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c9109-109">This example requires:</span></span>  
  
- <span data-ttu-id="c9109-110">Eine Windows Forms-Anwendung</span><span class="sxs-lookup"><span data-stu-id="c9109-110">A Windows Forms application.</span></span>  
  
- <span data-ttu-id="c9109-111">Ein <xref:System.Windows.Forms.PaintEventArgs> , bei dem es sich um einen Parameter von handelt <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="c9109-111">A <xref:System.Windows.Forms.PaintEventArgs>, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9109-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9109-112">See also</span></span>

- [<span data-ttu-id="c9109-113">Vorgehensweise: Auflisten installierter Decoder</span><span class="sxs-lookup"><span data-stu-id="c9109-113">How to: List Installed Decoders</span></span>](how-to-list-installed-decoders.md)
- [<span data-ttu-id="c9109-114">Verwenden von Bildencodern und -decodern in Managed GDI+</span><span class="sxs-lookup"><span data-stu-id="c9109-114">Using Image Encoders and Decoders in Managed GDI+</span></span>](using-image-encoders-and-decoders-in-managed-gdi.md)
