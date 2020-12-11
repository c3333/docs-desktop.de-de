---
title: 'Vorgehensweise: Ausrichten und Strecken eines Steuerelements in einem TableLayoutPanel-Steuerelement'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.AlignStretchCtrl
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms], stretching controls
- controls [Windows Forms], stretching
- controls [Windows Forms], aligning
ms.assetid: 7dc1a157-6fee-4995-8ebc-b65bdc0909a8
ms.openlocfilehash: fd32593bcad9e3f3ef93edee8aa2659d423f9feb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976367"
---
# <a name="how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control"></a><span data-ttu-id="a802d-102">Vorgehensweise: Ausrichten und Strecken eines Steuerelements in einem TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="a802d-102">How to: Align and Stretch a Control in a TableLayoutPanel Control</span></span>

<span data-ttu-id="a802d-103">Sie können Steuerelemente in einem <xref:System.Windows.Forms.TableLayoutPanel> mit der-Eigenschaft und der-Eigenschaft ausrichten und erweitern <xref:System.Windows.Forms.Control.Anchor%2A> <xref:System.Windows.Forms.Control.Dock%2A> .</span><span class="sxs-lookup"><span data-stu-id="a802d-103">You can align and stretch controls in a <xref:System.Windows.Forms.TableLayoutPanel> with the <xref:System.Windows.Forms.Control.Anchor%2A> and <xref:System.Windows.Forms.Control.Dock%2A> properties.</span></span>

## <a name="align-and-stretch-a-control"></a><span data-ttu-id="a802d-104">Ausrichten und Strecken eines Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="a802d-104">Align and stretch a control</span></span>

1. <span data-ttu-id="a802d-105">Ziehen Sie in Visual Studio ein- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement aus der **Toolbox** auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="a802d-105">In Visual Studio, drag a <xref:System.Windows.Forms.TableLayoutPanel> control from the **Toolbox** onto your form.</span></span>

2. <span data-ttu-id="a802d-106">Ziehen Sie ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** in die linke obere Zelle des- <xref:System.Windows.Forms.TableLayoutPanel> Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="a802d-106">Drag a <xref:System.Windows.Forms.Button> control from the **Toolbox** into the upper-left cell of the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span> <span data-ttu-id="a802d-107">Das- <xref:System.Windows.Forms.Button> Steuerelement wird in der Zelle zentriert.</span><span class="sxs-lookup"><span data-stu-id="a802d-107">The <xref:System.Windows.Forms.Button> control is centered in the cell.</span></span>

3. <span data-ttu-id="a802d-108">Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Anchor%2A> auf fest `Left,Right` .</span><span class="sxs-lookup"><span data-stu-id="a802d-108">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Anchor%2A> property to `Left,Right`.</span></span> <span data-ttu-id="a802d-109">Das Steuerelement wird so <xref:System.Windows.Forms.Button> gestreckt, dass es der Breite der Zelle entspricht.</span><span class="sxs-lookup"><span data-stu-id="a802d-109">The <xref:System.Windows.Forms.Button> control stretches to match the width of the cell.</span></span>

4. <span data-ttu-id="a802d-110">Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Anchor%2A> auf fest `Top,Bottom` .</span><span class="sxs-lookup"><span data-stu-id="a802d-110">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Anchor%2A> property to `Top,Bottom`.</span></span> <span data-ttu-id="a802d-111">Das-Steuerelement wird so <xref:System.Windows.Forms.Button> gestreckt, dass es der Höhe der Zelle entspricht.</span><span class="sxs-lookup"><span data-stu-id="a802d-111">The <xref:System.Windows.Forms.Button> control stretches to match the height of the cell.</span></span>

5. <span data-ttu-id="a802d-112">Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Dock%2A> auf fest <xref:System.Windows.Forms.DockStyle.Fill> .</span><span class="sxs-lookup"><span data-stu-id="a802d-112">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span> <span data-ttu-id="a802d-113">Das-Steuerelement wird <xref:System.Windows.Forms.Button> erweitert, um die Zelle auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="a802d-113">The <xref:System.Windows.Forms.Button> control expands to fill the cell.</span></span>

6. <span data-ttu-id="a802d-114">Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Dock%2A> auf fest <xref:System.Windows.Forms.DockStyle.None> .</span><span class="sxs-lookup"><span data-stu-id="a802d-114">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.None>.</span></span> <span data-ttu-id="a802d-115">Das <xref:System.Windows.Forms.Button> Steuerelement wird auf seine ursprüngliche Größe zurückgesetzt und wechselt zur linken oberen Ecke der Zelle.</span><span class="sxs-lookup"><span data-stu-id="a802d-115">The <xref:System.Windows.Forms.Button> control returns to its original size and moves to the upper-left corner of the cell.</span></span> <span data-ttu-id="a802d-116">Der **Windows Forms-Designer** hat die- <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaft auf festgelegt `Top, Left` .</span><span class="sxs-lookup"><span data-stu-id="a802d-116">The **Windows Forms Designer** has set the <xref:System.Windows.Forms.Control.Anchor%2A> property to `Top, Left`.</span></span>

7. <span data-ttu-id="a802d-117">Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Anchor%2A> auf fest `Bottom,Right` .</span><span class="sxs-lookup"><span data-stu-id="a802d-117">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Anchor%2A> property to `Bottom,Right`.</span></span> <span data-ttu-id="a802d-118">Das- <xref:System.Windows.Forms.Button> Steuerelement wechselt zur unteren rechten Ecke der Zelle.</span><span class="sxs-lookup"><span data-stu-id="a802d-118">The <xref:System.Windows.Forms.Button> control moves to the lower-right corner of the cell.</span></span>

8. <span data-ttu-id="a802d-119">Legen Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Anchor%2A> auf fest <xref:System.Windows.Forms.AnchorStyles.None> .</span><span class="sxs-lookup"><span data-stu-id="a802d-119">Set the value of the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Anchor%2A> property to <xref:System.Windows.Forms.AnchorStyles.None>.</span></span> <span data-ttu-id="a802d-120">Das- <xref:System.Windows.Forms.Button> Steuerelement wechselt in den Mittelpunkt der Zelle.</span><span class="sxs-lookup"><span data-stu-id="a802d-120">The <xref:System.Windows.Forms.Button> control moves to the center of the cell.</span></span>

## <a name="see-also"></a><span data-ttu-id="a802d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a802d-121">See also</span></span>

- [<span data-ttu-id="a802d-122">TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="a802d-122">TableLayoutPanel Control</span></span>](tablelayoutpanel-control-windows-forms.md)
