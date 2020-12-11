---
title: 'Gewusst wie: Verwenden eines Rasters für automatisches Layout'
ms.date: 03/30/2017
helpviewer_keywords:
- grids [WPF], automatic layout
- automatic layout [WPF], grid use
ms.assetid: ab9de407-e0c1-4047-bdf0-24951bf73879
ms.openlocfilehash: 5389d8d6130367d36a5c81b3bdc316c989474ce2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976278"
---
# <a name="how-to-use-a-grid-for-automatic-layout"></a><span data-ttu-id="cfea5-102">Gewusst wie: Verwenden eines Rasters für automatisches Layout</span><span class="sxs-lookup"><span data-stu-id="cfea5-102">How to: Use a Grid for Automatic Layout</span></span>
<span data-ttu-id="cfea5-103">Dieses Beispiel beschreibt, wie ein Raster im automatischen Layoutansatz zum Erstellen einer lokalisierbaren Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfea5-103">This example describes how to use a grid in the automatic layout approach to creating a localizable application.</span></span>  
  
 <span data-ttu-id="cfea5-104">Die Lokalisierung eines [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] kann ein zeitaufwändiger Prozess sein.</span><span class="sxs-lookup"><span data-stu-id="cfea5-104">Localization of a [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] can be a time consuming process.</span></span> <span data-ttu-id="cfea5-105">Oft müssen Lokalisierungsexperten die Größe von Elementen ändern und sie neu positionieren, um Text zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="cfea5-105">Often localizers need to re-size and reposition elements in addition to translating text.</span></span> <span data-ttu-id="cfea5-106">In der letzten Sprache, in der eine [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] für die erforderliche Anpassung angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="cfea5-106">In the past each language that a [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] was adapted for required adjustment.</span></span> <span data-ttu-id="cfea5-107">Nun können Sie mit den Funktionen von [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Elemente entwerfen, die die Notwendigkeit einer Anpassung verringern.</span><span class="sxs-lookup"><span data-stu-id="cfea5-107">Now with the capabilities of [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] you can design elements that reduce the need for adjustment.</span></span> <span data-ttu-id="cfea5-108">Der Ansatz zum Schreiben von Anwendungen, die leichter neu skaliert und neu positioniert werden können, heißt `auto layout` .</span><span class="sxs-lookup"><span data-stu-id="cfea5-108">The approach to writing applications that can be more easily re-sized and repositioned is called `auto layout`.</span></span>  
  
 <span data-ttu-id="cfea5-109">Das folgende [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispiel veranschaulicht die Verwendung eines Rasters, um einige Schaltflächen und Text zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="cfea5-109">The following [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] example demonstrates using a grid to position some buttons and text.</span></span> <span data-ttu-id="cfea5-110">Beachten Sie, dass die Höhe und Breite der Zellen auf festgelegt ist. aus diesem `Auto` Grund wird die Zelle, die die Schaltfläche mit einem Bild enthält, an das Bild angepasst.</span><span class="sxs-lookup"><span data-stu-id="cfea5-110">Notice that the height and width of the cells are set to `Auto`; therefore the cell that contains the button with an image adjusts to fit the image.</span></span> <span data-ttu-id="cfea5-111">Da das <xref:System.Windows.Controls.Grid> Element an seinen Inhalt angepasst werden kann, kann es nützlich sein, wenn das automatische Layoutverfahren zum Entwerfen von Anwendungen eingesetzt wird, die lokalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="cfea5-111">Because the <xref:System.Windows.Controls.Grid> element can adjust to its content it can be useful when taking the automatic layout approach to designing applications that can be localized.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cfea5-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cfea5-112">Example</span></span>  
 <span data-ttu-id="cfea5-113">Das folgende Beispiel veranschaulicht die Verwendung von eines Rasters.</span><span class="sxs-lookup"><span data-stu-id="cfea5-113">The following example shows how to use a grid.</span></span>  
  
 [!code-xaml[LocalizationGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LocalizationGrid/CS/Pane1.xaml#1)]  
  
 <span data-ttu-id="cfea5-114">Die folgende Grafik zeigt die Ausgabe des Codebeispiels.</span><span class="sxs-lookup"><span data-stu-id="cfea5-114">The following graphic shows the output of the code sample.</span></span>  
  
 <span data-ttu-id="cfea5-115">![Rasterbeispiel](./media/glob-grid.png "glob_grid")</span><span class="sxs-lookup"><span data-stu-id="cfea5-115">![Grid example](./media/glob-grid.png "glob_grid")</span></span>  
<span data-ttu-id="cfea5-116">Raster</span><span class="sxs-lookup"><span data-stu-id="cfea5-116">Grid</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cfea5-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfea5-117">See also</span></span>

- [<span data-ttu-id="cfea5-118">Übersicht über die Verwendung eines automatischen Layouts</span><span class="sxs-lookup"><span data-stu-id="cfea5-118">Use Automatic Layout Overview</span></span>](use-automatic-layout-overview.md)
- [<span data-ttu-id="cfea5-119">Verwenden des automatischen Layouts zum Erstellen einer Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="cfea5-119">Use Automatic Layout to Create a Button</span></span>](how-to-use-automatic-layout-to-create-a-button.md)
