---
title: Erstellen eines komplexen Rasters
description: Ein Beispiel für die Verwendung eines Raster Steuer Elements zum Erstellen eines Layouts, das wie ein monatlicher Kalender aussieht.
ms.date: 03/30/2017
helpviewer_keywords:
- calendar [WPF], creating
- monthly calendar [WPF], creating
- Grid control [WPF], creating [WPF], complex grid
ms.assetid: 4ce3040a-a156-4364-9596-98ca1eca5550
ms.openlocfilehash: ab5490d608b21fe8b29a078dc1f0147f038c27a3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978075"
---
# <a name="how-to-create-a-complex-grid"></a>Erstellen eines komplexen Rasters

Dieses Beispiel zeigt, wie ein-Steuerelement verwendet wird, <xref:System.Windows.Controls.Grid> um ein Layout zu erstellen, das wie ein monatlicher Kalender aussieht.

## <a name="example"></a>Beispiel

Im folgenden Beispiel werden acht Zeilen und acht Spalten mithilfe der <xref:System.Windows.Controls.RowDefinition> -Klasse und der- <xref:System.Windows.Controls.ColumnDefinition> Klasse definiert. Dabei werden die <xref:System.Windows.Controls.Grid.ColumnSpan%2A?displayProperty=nameWithType> <xref:System.Windows.Controls.Grid.RowSpan%2A?displayProperty=nameWithType> angefügten Eigenschaften und sowie-Elemente verwendet, die <xref:System.Windows.Shapes.Rectangle> die Hintergründe verschiedener Spalten und Zeilen ausfüllen. Dieser Entwurf ist möglich, da mehr als ein Element in jeder Zelle in einer vorhanden sein kann <xref:System.Windows.Controls.Grid> , ein Grund Unterschied zwischen <xref:System.Windows.Controls.Grid> und <xref:System.Windows.Documents.Table> .

Im Beispiel werden vertikale Farbverläufe für <xref:System.Windows.Shapes.Shape.Fill%2A> die Spalten und Zeilen verwendet, um die visuelle Darstellung und die Lesbarkeit des Kalenders zu verbessern. Formatierte <xref:System.Windows.Controls.TextBlock> Elemente stellen die Datumsangaben und Wochentage dar. <xref:System.Windows.Controls.TextBlock> Elemente werden mithilfe der <xref:System.Windows.FrameworkElement.Margin%2A> Eigenschaften-und Ausrichtungs Eigenschaften, die im Stil für die Anwendung definiert sind, in ihren Zellen vollkommen positioniert.

[!code-xaml[GridComplex#1](~/samples/snippets/csharp/VS_Snippets_Wpf/GridComplex/CS/default.xaml#1)]

Die folgende Abbildung zeigt das resultierende Steuerelement, ein anpassbarer Kalender:

![Screenshot des resultierenden Steuer Elements](././media/how-to-create-a-complex-grid/wpf-manual-calendar.png)

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Grid?displayProperty=nameWithType>
- <xref:System.Windows.Documents.TableCell?displayProperty=nameWithType>
- [Übersicht über das Zeichnen mit Volltonfarben und Farbverläufen](../graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md)
- [Übersicht über Panel-Elemente](panels-overview.md)
- [Tabellen Übersicht](../advanced/table-overview.md)
