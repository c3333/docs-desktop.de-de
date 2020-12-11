---
title: 'Vorgehensweise: Anwenden einer Zeichnung auf ein 3D-Modell'
ms.date: 03/30/2017
helpviewer_keywords:
- drawings [WPF], applying to 3D models
- 3D models [WPF], applying drawings to
ms.assetid: 68357577-b7fc-446e-8be9-a8cc7df3a350
ms.openlocfilehash: 794ca9a48bcec42c3eee4d8da143f3ae9d27fcf2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977272"
---
# <a name="how-to-apply-a-drawing-to-a-3d-model"></a>Vorgehensweise: Anwenden einer Zeichnung auf ein 3D-Modell

In diesem Beispiel wird gezeigt, wie Sie <xref:System.Windows.Media.DrawingBrush> als <xref:System.Windows.Media.Media3D.Material> auf ein 3D-Modell angewendetes verwenden können.

Im folgenden Code wird ein <xref:System.Windows.Media.DrawingGroup> als Inhalt eines definiert <xref:System.Windows.Media.DrawingBrush> .  Der <xref:System.Windows.Media.DrawingBrush> wird als <xref:System.Windows.Media.Media3D.DiffuseMaterial.Brush%2A> -Eigenschaft des festgelegt <xref:System.Windows.Media.Media3D.DiffuseMaterial> , der auf eine 3D-Ebene angewendet wird.

> [!NOTE]
> Es ist häufig wünschenswert, komplexe Objekte und Werte wie die nachfolgende Zeichnung als Ressourcen zu definieren, die wieder verwendet werden können, und den Code zu vereinfachen. Weitere Informationen finden Sie unter [XAML-Ressourcen](/dotnet/desktop-wpf/fundamentals/xaml-resources-define) .

[!code-xaml[3DGallery_snip#ApplyDrawingToMaterialInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ApplyDrawingToMaterialExample.xaml#applydrawingtomaterialinline1)]

## <a name="example"></a>Beispiel

Der folgende Code zeigt das gesamte Beispiel.

[!code-xaml[3DGallery_snip#ApplyDrawingToMaterialExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ApplyDrawingToMaterialExample.xaml#applydrawingtomaterialexamplewholepage)]

## <a name="see-also"></a>Siehe auch

- [XAML-Ressourcen](/dotnet/desktop-wpf/fundamentals/xaml-resources-define)
- [Erstellen einer 3D-Szene](how-to-create-a-3-d-scene.md)
- [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md)
- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
