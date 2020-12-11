---
title: 'Gewusst wie: Verwenden von MatrixTransform zum Erstellen benutzerdefinierter Transformationen'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], custom Transforms
ms.assetid: 919381ca-989f-47cf-86b4-1094060236e4
ms.openlocfilehash: 1971d5fe9422c5138f140517e6fd4c9f9b2cf48b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977513"
---
# <a name="how-to-use-a-matrixtransform-to-create-custom-transforms"></a>Gewusst wie: Verwenden von MatrixTransform zum Erstellen benutzerdefinierter Transformationen
Dieses Beispiel zeigt, wie Sie mit einem <xref:System.Windows.Media.MatrixTransform> die Position, die Streckung und die Schiefe eines übersetzen (verschieben) <xref:System.Windows.Controls.Button> .  
  
> [!NOTE]
> Verwenden Sie die- <xref:System.Windows.Media.MatrixTransform> Klasse, um benutzerdefinierte Transformationen zu erstellen, die nicht von den <xref:System.Windows.Media.RotateTransform> <xref:System.Windows.Media.SkewTransform> Klassen,, oder bereitgestellt werden <xref:System.Windows.Media.ScaleTransform> <xref:System.Windows.Media.TranslateTransform> .  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[Transforms_snip#MatrixTransform](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MatrixTransformExample.xaml#matrixtransform)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.MatrixTransform>
- <xref:System.Windows.Media.Transform>
- [Übersicht über Transformationen](transforms-overview.md)
- [Artikel zu Vorgehensweisen](transformations-how-to-topics.md)
- [Übersicht über Formen und die grundlegenden Funktionen zum Zeichnen in WPF](shapes-and-basic-drawing-in-wpf-overview.md)
