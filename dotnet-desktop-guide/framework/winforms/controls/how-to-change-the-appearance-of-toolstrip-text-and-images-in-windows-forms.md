---
title: 'Gewusst wie: Ändern der Darstellung von ToolStrip-Text und-Bildern'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], appearance
- toolbars [Windows Forms], images
- examples [Windows Forms], toolbars
- toolbars [Windows Forms], appearance
- ToolStrip control [Windows Forms], images
- ToolStrip control [Windows Forms], text
- toolbars [Windows Forms], text
ms.assetid: d62dc9d1-2edd-4dfa-aed7-1335d6e13d86
ms.openlocfilehash: 7816e138e44554683c201895ece1f886ace8bfa6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976524"
---
# <a name="how-to-change-the-appearance-of-toolstrip-text-and-images-in-windows-forms"></a><span data-ttu-id="b31d1-102">Vorgehensweise: Ändern der Darstellung von ToolStrip-Text und -Bildern in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b31d1-102">How to: Change the Appearance of ToolStrip Text and Images in Windows Forms</span></span>
<span data-ttu-id="b31d1-103">Sie können steuern, ob Text und Bilder auf einem angezeigt werden <xref:System.Windows.Forms.ToolStripItem> und wie Sie relativ zueinander und in ausgerichtet werden <xref:System.Windows.Forms.ToolStrip> .</span><span class="sxs-lookup"><span data-stu-id="b31d1-103">You can control whether text and images are displayed on a <xref:System.Windows.Forms.ToolStripItem> and how they are aligned relative to each other and the <xref:System.Windows.Forms.ToolStrip>.</span></span>  
  
### <a name="to-define-what-is-displayed-on-a-toolstripitem"></a><span data-ttu-id="b31d1-104">So definieren Sie, was auf einem ToolStripItem angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="b31d1-104">To define what is displayed on a ToolStripItem</span></span>  
  
- <span data-ttu-id="b31d1-105">Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.DisplayStyle%2A> Eigenschaft auf den gewünschten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="b31d1-105">Set the <xref:System.Windows.Forms.ToolStripItem.DisplayStyle%2A> property to the desired value.</span></span> <span data-ttu-id="b31d1-106">Die Möglichkeiten sind `Image` , `ImageAndText` , `None` und `Text` .</span><span class="sxs-lookup"><span data-stu-id="b31d1-106">The possibilities are `Image`, `ImageAndText`, `None`, and `Text`.</span></span> <span data-ttu-id="b31d1-107">Der Standardwert ist `ImageAndText`.</span><span class="sxs-lookup"><span data-stu-id="b31d1-107">The default is `ImageAndText`.</span></span>  
  
    ```vb  
    ToolStripButton2.DisplayStyle = _  
        System.Windows.Forms.ToolStripItemDisplayStyle.Image  
    ```  
  
    ```csharp  
    toolStripButton2.DisplayStyle = System.Windows.Forms.ToolStripItemDisplayStyle.Image;  
    ```  
  
### <a name="to-align-text-on-a-toolstripitem"></a><span data-ttu-id="b31d1-108">So richten Sie Text auf einem Tool Strip Item aus</span><span class="sxs-lookup"><span data-stu-id="b31d1-108">To align text on a ToolStripItem</span></span>  
  
- <span data-ttu-id="b31d1-109">Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.TextAlign%2A> Eigenschaft auf den gewünschten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="b31d1-109">Set the <xref:System.Windows.Forms.ToolStripItem.TextAlign%2A> property to the desired value.</span></span> <span data-ttu-id="b31d1-110">Die Möglichkeiten sind eine beliebige Kombination aus Top, Middle und Bottom mit Links, zentriert und rechts.</span><span class="sxs-lookup"><span data-stu-id="b31d1-110">The possibilities are any combination of top, middle, and bottom with left, center, and right.</span></span> <span data-ttu-id="b31d1-111">Der Standardwert ist `MiddleCenter`.</span><span class="sxs-lookup"><span data-stu-id="b31d1-111">The default is `MiddleCenter`.</span></span>  
  
    ```vb  
    ToolStripSplitButton1.TextAlign = _  
        System.Drawing.ContentAlignment.MiddleRight  
    ```  
  
    ```csharp  
    toolStripSplitButton1.TextAlign = System.Drawing.ContentAlignment.MiddleRight;  
    ```  
  
### <a name="to-align-an-image-on-a-toolstripitem"></a><span data-ttu-id="b31d1-112">So richten Sie ein Bild auf einem ToolStripItem-Element aus</span><span class="sxs-lookup"><span data-stu-id="b31d1-112">To align an image on a ToolStripItem</span></span>  
  
- <span data-ttu-id="b31d1-113">Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.ImageAlign%2A> Eigenschaft auf den gewünschten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="b31d1-113">Set the <xref:System.Windows.Forms.ToolStripItem.ImageAlign%2A> property to the desired value.</span></span> <span data-ttu-id="b31d1-114">Die Möglichkeiten sind eine beliebige Kombination aus Top, Middle und Bottom mit Links, zentriert und rechts.</span><span class="sxs-lookup"><span data-stu-id="b31d1-114">The possibilities are any combination of top, middle, and bottom with left, center, and right.</span></span> <span data-ttu-id="b31d1-115">Der Standardwert ist `MiddleLeft`.</span><span class="sxs-lookup"><span data-stu-id="b31d1-115">The default is `MiddleLeft`.</span></span>  
  
    ```vb  
    ToolStripSplitButton1.ImageAlign = _  
        System.Drawing.ContentAlignment.MiddleRight  
    ```  
  
    ```csharp  
    toolStripSplitButton1.ImageAlign = System.Drawing.ContentAlignment.MiddleRight;  
    ```  
  
### <a name="to-define-how-toolstripitem-text-and-images-are-displayed-relative-to-each-other"></a><span data-ttu-id="b31d1-116">So definieren Sie, wie Text und Bilder von ToolStripItem zueinander zueinander angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="b31d1-116">To define how ToolStripItem text and images are displayed relative to each other</span></span>  
  
- <span data-ttu-id="b31d1-117">Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.TextImageRelation%2A> Eigenschaft auf den gewünschten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="b31d1-117">Set the <xref:System.Windows.Forms.ToolStripItem.TextImageRelation%2A> property to the desired value.</span></span> <span data-ttu-id="b31d1-118">Mögliche Werte sind `ImageAboveText`, `ImageBeforeText`, `Overlay`, `TextAboveImage` und `TextBeforeImage`.</span><span class="sxs-lookup"><span data-stu-id="b31d1-118">The possibilities are `ImageAboveText`, `ImageBeforeText`, `Overlay`, `TextAboveImage`, and `TextBeforeImage`.</span></span> <span data-ttu-id="b31d1-119">Der Standardwert ist `ImageBeforeText`.</span><span class="sxs-lookup"><span data-stu-id="b31d1-119">The default is `ImageBeforeText`.</span></span>  
  
    ```vb  
    ToolStripButton1.TextImageRelation = _  
        System.Windows.Forms.TextImageRelation.ImageAboveText  
    ```  
  
    ```csharp  
    toolStripButton1.TextImageRelation = System.Windows.Forms.TextImageRelation.ImageAboveText;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="b31d1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b31d1-120">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- [<span data-ttu-id="b31d1-121">Übersicht über das ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b31d1-121">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
- [<span data-ttu-id="b31d1-122">Architektur des ToolStrip-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="b31d1-122">ToolStrip Control Architecture</span></span>](toolstrip-control-architecture.md)
- [<span data-ttu-id="b31d1-123">Zusammenfassung der ToolStrip-Technologie</span><span class="sxs-lookup"><span data-stu-id="b31d1-123">ToolStrip Technology Summary</span></span>](toolstrip-technology-summary.md)
