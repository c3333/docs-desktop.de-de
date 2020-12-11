---
title: 'Vorgehensweise: Überspannen von Zeilen und Spalten in einem TableLayoutPanel-Steuerelement'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.SpanRowsColumns
helpviewer_keywords:
- columns [Windows Forms], spanning
- merging cells
- TableLayoutPanel control [Windows Forms], spanning rows and columns
- rows [Windows Forms], spanning
- cells [Windows Forms], merging
ms.assetid: a8a2fdd3-a848-48b0-a4cd-4e85ebded87e
ms.openlocfilehash: a215b2b4e05bab5c81d2779d4b67d5b9d57b6ba5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976745"
---
# <a name="how-to-span-rows-and-columns-in-a-tablelayoutpanel-control"></a><span data-ttu-id="c2e74-102">Vorgehensweise: Überspannen von Zeilen und Spalten in einem TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c2e74-102">How to: Span Rows and Columns in a TableLayoutPanel Control</span></span>
<span data-ttu-id="c2e74-103">Steuerelemente in einem <xref:System.Windows.Forms.TableLayoutPanel> -Steuerelement können angrenzende Zeilen und Spalten umfassen.</span><span class="sxs-lookup"><span data-stu-id="c2e74-103">Controls in a <xref:System.Windows.Forms.TableLayoutPanel> control can span adjacent rows and columns.</span></span>

## <a name="to-span-columns-and-rows"></a><span data-ttu-id="c2e74-104">Zum Spannen von Spalten und Zeilen</span><span class="sxs-lookup"><span data-stu-id="c2e74-104">To span columns and rows</span></span>

1. <span data-ttu-id="c2e74-105">Ziehen Sie ein <xref:System.Windows.Forms.TableLayoutPanel> -Steuerelement aus der **Toolbox** auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="c2e74-105">Drag a <xref:System.Windows.Forms.TableLayoutPanel> control from the **Toolbox** onto your form.</span></span>

2. <span data-ttu-id="c2e74-106">Ziehen Sie ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** in die linke obere Zelle des- <xref:System.Windows.Forms.TableLayoutPanel> Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c2e74-106">Drag a <xref:System.Windows.Forms.Button> control from the **Toolbox** into the upper-left cell of the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

3. <span data-ttu-id="c2e74-107">Legen <xref:System.Windows.Forms.Button> Sie die **ColumnSpan** -Eigenschaft des Steuer Elements auf **2** fest.</span><span class="sxs-lookup"><span data-stu-id="c2e74-107">Set the <xref:System.Windows.Forms.Button> control's **ColumnSpan** property to **2**.</span></span> <span data-ttu-id="c2e74-108">Beachten Sie, dass das <xref:System.Windows.Forms.Button> -Steuerelement die erste und die zweite Spalte umfasst.</span><span class="sxs-lookup"><span data-stu-id="c2e74-108">Note that the <xref:System.Windows.Forms.Button> control spans the first and second columns.</span></span>

4. <span data-ttu-id="c2e74-109">Legen <xref:System.Windows.Forms.Button> Sie die **RowSpan** -Eigenschaft des Steuer Elements auf **2** fest.</span><span class="sxs-lookup"><span data-stu-id="c2e74-109">Set the <xref:System.Windows.Forms.Button> control's **RowSpan** property to **2**.</span></span> <span data-ttu-id="c2e74-110">Beachten Sie, dass das <xref:System.Windows.Forms.Button> -Steuerelement die erste und die zweite Zeile umfasst.</span><span class="sxs-lookup"><span data-stu-id="c2e74-110">Note that the <xref:System.Windows.Forms.Button> control spans the first and second rows.</span></span>

5. <span data-ttu-id="c2e74-111">Legen <xref:System.Windows.Forms.Button> Sie die **ColumnSpan** -Eigenschaft des Steuer Elements auf **1** fest.</span><span class="sxs-lookup"><span data-stu-id="c2e74-111">Set the <xref:System.Windows.Forms.Button> control's **ColumnSpan** property to **1**.</span></span> <span data-ttu-id="c2e74-112">Beachten Sie, dass das <xref:System.Windows.Forms.Button> -Steuerelement in die erste Spalte wechselt und die erste und zweite Zeile umfasst.</span><span class="sxs-lookup"><span data-stu-id="c2e74-112">Note that the <xref:System.Windows.Forms.Button> control moves into the first column and spans the first and second rows.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2e74-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2e74-113">See also</span></span>

- [<span data-ttu-id="c2e74-114">TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c2e74-114">TableLayoutPanel Control</span></span>](tablelayoutpanel-control-windows-forms.md)
