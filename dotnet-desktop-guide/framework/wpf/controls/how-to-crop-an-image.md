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
# <a name="how-to-crop-an-image"></a>Gewusst wie: Zuschneiden eines Bilds

Dieses Beispiel zeigt, wie Sie ein Bild mithilfe von Zuschneiden <xref:System.Windows.Media.Imaging.CroppedBitmap> .  
  
 <xref:System.Windows.Media.Imaging.CroppedBitmap> wird hauptsächlich verwendet, wenn Sie eine abgeschnittene Version eines Bilds codieren, um Sie in eine Datei zu speichern. Informationen zum Zuschneiden eines Bilds zu Anzeige Zwecken finden Sie im Thema Gewusst [wie: Erstellen eines Clip-Bereichs](/previous-versions/dotnet/netframework-3.5/ms746710(v=vs.90)) .  
  
## <a name="example"></a>Beispiel  

 Im folgenden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] werden die in den Beispielen unten verwendeten Ressourcen definiert.  
  
 [!code-xaml[imageelementexample#CroppedXAML1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml1)]  
  
 Im folgenden Beispiel wird ein Bild mithilfe von <xref:System.Windows.Media.Imaging.CroppedBitmap> als Quelle erstellt.  
  
 [!code-xaml[imageelementexample#CroppedXAML2](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml2)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp1)]
 [!code-vb[imageelementexample#CroppedCSharp1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp1)]  
  
 <xref:System.Windows.Media.Imaging.CroppedBitmap>Kann auch als Quelle eines anderen verwendet werden, wobei <xref:System.Windows.Media.Imaging.CroppedBitmap> das Zuschneiden Verkettung wird. Beachten Sie, dass die <xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A> Werte verwendet, die relativ zur zugeschnittenen Quell Bitmap und nicht zum Anfangs Bild sind.  
  
 [!code-xaml[imageelementexample#CroppedXAML3](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml3)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp2](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp2)]
 [!code-vb[imageelementexample#CroppedCSharp2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp2)]  
  
## <a name="see-also"></a>Siehe auch

- [Gewusst wie: Erstellen eines Clip-Bereichs](/previous-versions/dotnet/netframework-3.5/ms746710(v=vs.90))
