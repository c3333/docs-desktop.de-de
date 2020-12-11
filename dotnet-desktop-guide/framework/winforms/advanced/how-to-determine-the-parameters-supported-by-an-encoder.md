---
title: 'Vorgehensweise: Ermitteln der von einem Encoder unterstützten Parameter'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- encoder parameters [Windows Forms], determining supported
ms.assetid: f47ae459-e3ce-4d41-a140-2f6c6aea3f44
ms.openlocfilehash: 3e5345180e0ff3321b9ef0b885b836d3e9456f28
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972359"
---
# <a name="how-to-determine-the-parameters-supported-by-an-encoder"></a><span data-ttu-id="2263b-102">Vorgehensweise: Ermitteln der von einem Encoder unterstützten Parameter</span><span class="sxs-lookup"><span data-stu-id="2263b-102">How to: Determine the Parameters Supported by an Encoder</span></span>
<span data-ttu-id="2263b-103">Sie können Bildparameter anpassen, z. b. Qualität und Komprimierungs Ebene, aber Sie müssen wissen, welche Parameter von einem bestimmten Bild Encoder unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2263b-103">You can adjust image parameters, such as quality and compression level, but you must know which parameters are supported by a given image encoder.</span></span> <span data-ttu-id="2263b-104">Die- <xref:System.Drawing.Image> Klasse stellt die- <xref:System.Drawing.Image.GetEncoderParameterList%2A> Methode bereit, sodass Sie bestimmen können, welche Bildparameter für einen bestimmten Encoder unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2263b-104">The <xref:System.Drawing.Image> class provides the <xref:System.Drawing.Image.GetEncoderParameterList%2A> method so that you can determine which image parameters are supported for a particular encoder.</span></span> <span data-ttu-id="2263b-105">Sie geben den Encoder mit einer GUID an.</span><span class="sxs-lookup"><span data-stu-id="2263b-105">You specify the encoder with a GUID.</span></span> <span data-ttu-id="2263b-106">Die- <xref:System.Drawing.Image.GetEncoderParameterList%2A> Methode gibt ein Array von- <xref:System.Drawing.Imaging.EncoderParameter> Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="2263b-106">The <xref:System.Drawing.Image.GetEncoderParameterList%2A> method returns an array of <xref:System.Drawing.Imaging.EncoderParameter> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2263b-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2263b-107">Example</span></span>  
 <span data-ttu-id="2263b-108">Im folgenden Beispielcode werden die unterstützten Parameter für den JPEG-Encoder ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="2263b-108">The following example code outputs the supported parameters for the JPEG encoder.</span></span> <span data-ttu-id="2263b-109">Verwenden Sie die Liste der Parameter Kategorien und zugeordneten GUIDs in der <xref:System.Drawing.Imaging.Encoder> Klassen Übersicht, um die Kategorie für jeden Parameter zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2263b-109">Use the list of parameter categories and associated GUIDs in the <xref:System.Drawing.Imaging.Encoder> class overview to determine the category for each parameter.</span></span>  
  
 [!code-csharp[UsingImageEncodersDecoders#3](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#3)]
 [!code-vb[UsingImageEncodersDecoders#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#3)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="2263b-110">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="2263b-110">Compiling the Code</span></span>  
 <span data-ttu-id="2263b-111">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2263b-111">This example requires:</span></span>  
  
- <span data-ttu-id="2263b-112">Eine Windows Forms-Anwendung</span><span class="sxs-lookup"><span data-stu-id="2263b-112">A Windows Forms application.</span></span>  
  
- <span data-ttu-id="2263b-113">Ein <xref:System.Windows.Forms.PaintEventArgs> , bei dem es sich um einen Parameter von handelt <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="2263b-113">A <xref:System.Windows.Forms.PaintEventArgs>, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2263b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2263b-114">See also</span></span>

- [<span data-ttu-id="2263b-115">Vorgehensweise: Auflisten installierter Encoder</span><span class="sxs-lookup"><span data-stu-id="2263b-115">How to: List Installed Encoders</span></span>](how-to-list-installed-encoders.md)
- [<span data-ttu-id="2263b-116">Bitmaptypen</span><span class="sxs-lookup"><span data-stu-id="2263b-116">Types of Bitmaps</span></span>](types-of-bitmaps.md)
- [<span data-ttu-id="2263b-117">Verwenden von Bildencodern und -decodern in Managed GDI+</span><span class="sxs-lookup"><span data-stu-id="2263b-117">Using Image Encoders and Decoders in Managed GDI+</span></span>](using-image-encoders-and-decoders-in-managed-gdi.md)
