---
title: 'Gewusst wie: Verwenden des automatischen Layouts zum Erstellen einer Schaltfläche'
ms.date: 03/30/2017
helpviewer_keywords:
- Button controls [WPF], creating with automatic layout
- automatic layout [WPF], creating buttons
ms.assetid: 96c206d0-9e77-4784-9d2d-5045aed2021c
ms.openlocfilehash: 05b874f9894841d3c318ee131d15165111fd596a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976271"
---
# <a name="how-to-use-automatic-layout-to-create-a-button"></a><span data-ttu-id="1da36-102">Gewusst wie: Verwenden des automatischen Layouts zum Erstellen einer Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="1da36-102">How to: Use Automatic Layout to Create a Button</span></span>
<span data-ttu-id="1da36-103">Dieses Beispiel beschreibt, wie der automatische Layoutansatz zum Erstellen einer Schaltfläche in einer lokalisierbaren Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1da36-103">This example describes how to use the automatic layout approach to create a button in a localizable application.</span></span>  
  
 <span data-ttu-id="1da36-104">Die Lokalisierung eines [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] kann ein zeitaufwändiger Prozess sein.</span><span class="sxs-lookup"><span data-stu-id="1da36-104">Localization of a [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] can be a time consuming process.</span></span> <span data-ttu-id="1da36-105">Oft müssen Lokalisierungsexperten die Größe von Elementen ändern und sie neu positionieren, um Text zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="1da36-105">Often localizers need to resize and reposition elements in addition to translating text.</span></span> <span data-ttu-id="1da36-106">In der letzten Sprache, in der eine [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] für die erforderliche Anpassung angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="1da36-106">In the past each language that a [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] was adapted for required adjustment.</span></span> <span data-ttu-id="1da36-107">Nun können Sie mit den Funktionen von [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Elemente entwerfen, die die Notwendigkeit einer Anpassung verringern.</span><span class="sxs-lookup"><span data-stu-id="1da36-107">Now with the capabilities of [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] you can design elements that reduce the need for adjustment.</span></span> <span data-ttu-id="1da36-108">Der Ansatz zum Schreiben von Anwendungen, die einfacher geändert und neu positioniert werden können, wird als bezeichnet `automatic layout` .</span><span class="sxs-lookup"><span data-stu-id="1da36-108">The approach to writing applications that can be more easily resized and repositioned is called `automatic layout`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1da36-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1da36-109">Example</span></span>  

<span data-ttu-id="1da36-110">In den folgenden beiden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispielen werden Anwendungen erstellt, die eine Schaltfläche instanziieren, eine mit englischem Text und eine mit spanischem Text.</span><span class="sxs-lookup"><span data-stu-id="1da36-110">The following two [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] examples create applications that instantiate a button; one with English text and one with Spanish text.</span></span> <span data-ttu-id="1da36-111">Beachten Sie, dass der Code mit Ausnahme des Texts der gleiche ist; die Schaltfläche wird an den Text angepasst.</span><span class="sxs-lookup"><span data-stu-id="1da36-111">Notice that the code is the same except for the text; the button adjusts to fit the text.</span></span>

[!code-xaml[LocalizationBtn_snip#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn_snip/CS/Pane1.xaml#1)]  
  
[!code-xaml[LocalizationBtn#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn/CS/Pane1.xaml#1)]  
  
 <span data-ttu-id="1da36-112">Die folgende Grafik zeigt die Ausgabe der Codebeispiele mit Schaltflächen, die automatisch geändert werden könnten:</span><span class="sxs-lookup"><span data-stu-id="1da36-112">The following graphic shows the output of the code samples with auto-resizable buttons:</span></span>
  
 ![Die gleiche Schaltfläche mit Text in unterschiedlichen Sprachen](./media/use-automatic-layout-overview/auto-resizable-button.png)  
  
## <a name="see-also"></a><span data-ttu-id="1da36-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1da36-114">See also</span></span>

- [<span data-ttu-id="1da36-115">Übersicht über die Verwendung eines automatischen Layouts</span><span class="sxs-lookup"><span data-stu-id="1da36-115">Use Automatic Layout Overview</span></span>](use-automatic-layout-overview.md)
- [<span data-ttu-id="1da36-116">Verwenden eines Rasters für automatisches Layout</span><span class="sxs-lookup"><span data-stu-id="1da36-116">Use a Grid for Automatic Layout</span></span>](how-to-use-a-grid-for-automatic-layout.md)
