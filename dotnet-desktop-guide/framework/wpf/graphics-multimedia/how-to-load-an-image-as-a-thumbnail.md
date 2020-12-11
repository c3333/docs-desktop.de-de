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
# <a name="how-to-load-an-image-as-a-thumbnail"></a>Gewusst wie: Laden eines Bilds als Miniaturansicht
In den folgenden Beispielen wird gezeigt, wie ein <xref:System.Windows.Controls.Image> als Miniaturansicht geladen wird, um den Anwendungs Speicher zu sparen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> Eigenschaft eines <xref:System.Windows.Media.Imaging.BitmapImage> in festgelegt [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] , um den zum Laden des Bilds erforderlichen Speicherplatz zu reduzieren.  
  
 [!code-xaml[ImageElementExample_snip#ImageSimpleExampleInlineMarkup](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml#imagesimpleexampleinlinemarkup)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> Eigenschaft eines-Objekts <xref:System.Windows.Media.Imaging.BitmapImage> im Code festgelegt, um den zum Laden des Bilds erforderlichen Speicherplatz zu reduzieren.  
  
 [!code-csharp[ImageElementExample_snip#ImageSimpleExampleInlineCode1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml.cs#imagesimpleexampleinlinecode1)]
 [!code-vb[ImageElementExample_snip#ImageSimpleExampleInlineCode1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample_snip/VB/ImageSimpleExample.xaml.vb#imagesimpleexampleinlinecode1)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Bildverarbeitung](imaging-overview.md)
