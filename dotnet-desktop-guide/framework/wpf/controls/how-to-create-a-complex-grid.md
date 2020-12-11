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
# <a name="how-to-create-a-complex-grid"></a><span data-ttu-id="01cca-103">Erstellen eines komplexen Rasters</span><span class="sxs-lookup"><span data-stu-id="01cca-103">How to create a complex Grid</span></span>

<span data-ttu-id="01cca-104">Dieses Beispiel zeigt, wie ein-Steuerelement verwendet wird, <xref:System.Windows.Controls.Grid> um ein Layout zu erstellen, das wie ein monatlicher Kalender aussieht.</span><span class="sxs-lookup"><span data-stu-id="01cca-104">This example shows how to use a <xref:System.Windows.Controls.Grid> control to create a layout that looks like a monthly calendar.</span></span>

## <a name="example"></a><span data-ttu-id="01cca-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="01cca-105">Example</span></span>

<span data-ttu-id="01cca-106">Im folgenden Beispiel werden acht Zeilen und acht Spalten mithilfe der <xref:System.Windows.Controls.RowDefinition> -Klasse und der- <xref:System.Windows.Controls.ColumnDefinition> Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="01cca-106">The following example defines eight rows and eight columns by using the <xref:System.Windows.Controls.RowDefinition> and <xref:System.Windows.Controls.ColumnDefinition> classes.</span></span> <span data-ttu-id="01cca-107">Dabei werden die <xref:System.Windows.Controls.Grid.ColumnSpan%2A?displayProperty=nameWithType> <xref:System.Windows.Controls.Grid.RowSpan%2A?displayProperty=nameWithType> angefügten Eigenschaften und sowie-Elemente verwendet, die <xref:System.Windows.Shapes.Rectangle> die Hintergründe verschiedener Spalten und Zeilen ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="01cca-107">It uses the <xref:System.Windows.Controls.Grid.ColumnSpan%2A?displayProperty=nameWithType> and <xref:System.Windows.Controls.Grid.RowSpan%2A?displayProperty=nameWithType> attached properties, together with <xref:System.Windows.Shapes.Rectangle> elements, which fill the backgrounds of various columns and rows.</span></span> <span data-ttu-id="01cca-108">Dieser Entwurf ist möglich, da mehr als ein Element in jeder Zelle in einer vorhanden sein kann <xref:System.Windows.Controls.Grid> , ein Grund Unterschied zwischen <xref:System.Windows.Controls.Grid> und <xref:System.Windows.Documents.Table> .</span><span class="sxs-lookup"><span data-stu-id="01cca-108">This design is possible because more than one element can exist in each cell in a <xref:System.Windows.Controls.Grid>, a principle difference between <xref:System.Windows.Controls.Grid> and <xref:System.Windows.Documents.Table>.</span></span>

<span data-ttu-id="01cca-109">Im Beispiel werden vertikale Farbverläufe für <xref:System.Windows.Shapes.Shape.Fill%2A> die Spalten und Zeilen verwendet, um die visuelle Darstellung und die Lesbarkeit des Kalenders zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="01cca-109">The example uses vertical gradients to <xref:System.Windows.Shapes.Shape.Fill%2A> the columns and rows to improve the visual presentation and readability of the calendar.</span></span> <span data-ttu-id="01cca-110">Formatierte <xref:System.Windows.Controls.TextBlock> Elemente stellen die Datumsangaben und Wochentage dar.</span><span class="sxs-lookup"><span data-stu-id="01cca-110">Styled <xref:System.Windows.Controls.TextBlock> elements represent the dates and days of the week.</span></span> <span data-ttu-id="01cca-111"><xref:System.Windows.Controls.TextBlock> Elemente werden mithilfe der <xref:System.Windows.FrameworkElement.Margin%2A> Eigenschaften-und Ausrichtungs Eigenschaften, die im Stil für die Anwendung definiert sind, in ihren Zellen vollkommen positioniert.</span><span class="sxs-lookup"><span data-stu-id="01cca-111"><xref:System.Windows.Controls.TextBlock> elements are absolutely positioned within their cells by using the <xref:System.Windows.FrameworkElement.Margin%2A> property and alignment properties that are defined within the style for the application.</span></span>

[!code-xaml[GridComplex#1](~/samples/snippets/csharp/VS_Snippets_Wpf/GridComplex/CS/default.xaml#1)]

<span data-ttu-id="01cca-112">Die folgende Abbildung zeigt das resultierende Steuerelement, ein anpassbarer Kalender:</span><span class="sxs-lookup"><span data-stu-id="01cca-112">The following image shows the resulting control, a customizable calendar:</span></span>

![Screenshot des resultierenden Steuer Elements](././media/how-to-create-a-complex-grid/wpf-manual-calendar.png)

## <a name="see-also"></a><span data-ttu-id="01cca-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01cca-114">See also</span></span>

- <xref:System.Windows.Controls.Grid?displayProperty=nameWithType>
- <xref:System.Windows.Documents.TableCell?displayProperty=nameWithType>
- [<span data-ttu-id="01cca-115">Übersicht über das Zeichnen mit Volltonfarben und Farbverläufen</span><span class="sxs-lookup"><span data-stu-id="01cca-115">Painting with Solid Colors and Gradients Overview</span></span>](../graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md)
- [<span data-ttu-id="01cca-116">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="01cca-116">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="01cca-117">Tabellen Übersicht</span><span class="sxs-lookup"><span data-stu-id="01cca-117">Table Overview</span></span>](../advanced/table-overview.md)
