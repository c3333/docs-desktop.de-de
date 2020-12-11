---
title: 'Gewusst wie: Auflisten des Zeichnungsinhalts eines visuellen Objekts'
ms.date: 03/30/2017
helpviewer_keywords:
- retrieving the DrawingGroup value of a Visual [WPF]
- enumerating the contents of a Visual [WPF]
ms.assetid: 2974ddb3-2997-4713-8fd2-e93d549c58a8
ms.openlocfilehash: 25aa0c3706005c1e16cedd7e06914db764545ebb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977854"
---
# <a name="how-to-enumerate-drawing-content-of-a-visual"></a>Gewusst wie: Auflisten des Zeichnungsinhalts eines visuellen Objekts
Das- <xref:System.Windows.Media.Drawing> Objekt stellt ein Objektmodell für das Auflisten des Inhalts eines bereit <xref:System.Windows.Media.Visual> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> -Methode verwendet, um den <xref:System.Windows.Media.DrawingGroup> Wert eines abzurufen <xref:System.Windows.Media.Visual> und ihn aufzulisten.  
  
> [!NOTE]
> Wenn Sie den Inhalt der Visualisierung auflisten, rufen Sie <xref:System.Windows.Media.Drawing> Objekte ab, und nicht die zugrunde liegende Darstellung der Renderingdaten als Liste von Vektorgrafik Anweisungs Listen. Weitere Informationen finden Sie unter [Übersicht über das WPF-Grafikenrendering](wpf-graphics-rendering-overview.md).  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMRetrieveDrawings](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/EnumerateDrawingsExample.xaml.cs#graphicsmmretrievedrawings)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.Drawing>
- <xref:System.Windows.Media.DrawingGroup>
- <xref:System.Windows.Media.VisualTreeHelper>
- [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md)
- [Übersicht über das WPF-Grafikrendering](wpf-graphics-rendering-overview.md)
