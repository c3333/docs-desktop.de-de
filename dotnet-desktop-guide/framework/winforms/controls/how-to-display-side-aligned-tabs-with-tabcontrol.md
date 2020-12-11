---
title: 'Vorgehensweise: Anzeigen von seitlich ausgerichteten Registerkarten mit TabControl'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tab pages [Windows Forms], displaying side-aligned tabs
- tabs [Windows Forms], displaying side-aligned tabs
- TabControl control [Windows Forms], displaying side-aligned tabs
ms.assetid: 110d5abd-3ae3-4ded-95bf-778aaac798a0
ms.openlocfilehash: d98c5906d99dff9371f8290e7dbc9c9011cd0c29
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975653"
---
# <a name="how-to-display-side-aligned-tabs-with-tabcontrol"></a><span data-ttu-id="e6d85-102">Vorgehensweise: Anzeigen von seitlich ausgerichteten Registerkarten mit TabControl</span><span class="sxs-lookup"><span data-stu-id="e6d85-102">How to: Display Side-Aligned Tabs with TabControl</span></span>
<span data-ttu-id="e6d85-103">Die <xref:System.Windows.Forms.TabControl.Alignment%2A>-Eigenschaft des <xref:System.Windows.Forms.TabControl> unterstützt das vertikale Anzeigen von Registerkarten (entlang des linken oder rechten Rands des Steuerelements), im Gegensatz zu horizontal (am oberen oder unteren Rand des Steuerelements).</span><span class="sxs-lookup"><span data-stu-id="e6d85-103">The <xref:System.Windows.Forms.TabControl.Alignment%2A> property of <xref:System.Windows.Forms.TabControl> supports displaying tabs vertically (along the left or right edge of the control), as opposed to horizontally (across the top or bottom of the control).</span></span> <span data-ttu-id="e6d85-104">Standardmäßig führt diese vertikale Anzeige zu einer wenig benutzerfreundlichen Oberfläche, weil die <xref:System.Windows.Forms.TabPage.Text%2A>-Eigenschaft des <xref:System.Windows.Forms.TabPage>-Objekts nicht auf der Registerkarte angezeigt wird, wenn visuelle Stile aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="e6d85-104">By default, this vertical display results in a poor user experience, because the <xref:System.Windows.Forms.TabPage.Text%2A> property of the <xref:System.Windows.Forms.TabPage> object does not display in the tab when visual styles are enabled.</span></span> <span data-ttu-id="e6d85-105">Es gibt auch keine direkte Möglichkeit, die Textrichtung auf der Registerkarte zu steuern. Mithilfe von "Besitzer zeichnen" können Sie <xref:System.Windows.Forms.TabControl> dieses Verhalten verbessern.</span><span class="sxs-lookup"><span data-stu-id="e6d85-105">There is also no direct way to control the direction of the text within the tab. You can use owner draw on <xref:System.Windows.Forms.TabControl> to improve this experience.</span></span>  
  
 <span data-ttu-id="e6d85-106">Das folgende Verfahren zeigt, wie rechtsbündig ausgerichtete Registerkarten gerendert werden, wobei der Registerkartentext von links nach rechts verläuft, indem Sie die Funktion „Ownerdrawn“ verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6d85-106">The following procedure shows how to render right-aligned tabs, with the tab text running from left to right, by using the "owner draw" feature.</span></span>  
  
### <a name="to-display-right-aligned-tabs"></a><span data-ttu-id="e6d85-107">So zeigen Sie rechtsbündig ausgerichtete Registerkarten an</span><span class="sxs-lookup"><span data-stu-id="e6d85-107">To display right-aligned tabs</span></span>  
  
1. <span data-ttu-id="e6d85-108">Fügen Sie Ihrem Formular einen <xref:System.Windows.Forms.TabControl> hinzu.</span><span class="sxs-lookup"><span data-stu-id="e6d85-108">Add a <xref:System.Windows.Forms.TabControl> to your form.</span></span>  
  
2. <span data-ttu-id="e6d85-109">Legen Sie die <xref:System.Windows.Forms.TabControl.Alignment%2A> -Eigenschaft auf <xref:System.Windows.Forms.TabAlignment.Right>fest.</span><span class="sxs-lookup"><span data-stu-id="e6d85-109">Set the <xref:System.Windows.Forms.TabControl.Alignment%2A> property to <xref:System.Windows.Forms.TabAlignment.Right>.</span></span>  
  
3. <span data-ttu-id="e6d85-110">Legen Sie die <xref:System.Windows.Forms.TabControl.SizeMode%2A>-Eigenschaft auf <xref:System.Windows.Forms.TabSizeMode.Fixed> fest, damit alle Registerkarten gleich breit sind.</span><span class="sxs-lookup"><span data-stu-id="e6d85-110">Set the <xref:System.Windows.Forms.TabControl.SizeMode%2A> property to <xref:System.Windows.Forms.TabSizeMode.Fixed>, so that all tabs are the same width.</span></span>  
  
4. <span data-ttu-id="e6d85-111">Legen Sie die <xref:System.Windows.Forms.TabControl.ItemSize%2A>-Eigenschaft auf die gewünschte feste Größe für die Registerkarten fest.</span><span class="sxs-lookup"><span data-stu-id="e6d85-111">Set the <xref:System.Windows.Forms.TabControl.ItemSize%2A> property to the preferred fixed size for the tabs.</span></span> <span data-ttu-id="e6d85-112">Denken Sie daran, dass sich die <xref:System.Windows.Forms.TabControl.ItemSize%2A>-Eigenschaft verhält, als seien die Registerkarten am oberen Rand, obwohl sie rechtsbündig ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="e6d85-112">Keep in mind that the <xref:System.Windows.Forms.TabControl.ItemSize%2A> property behaves as though the tabs were on top, although they are right-aligned.</span></span> <span data-ttu-id="e6d85-113">Demzufolge müssen Sie, um die Registerkarten zu verbreitern, die <xref:System.Drawing.Size.Height%2A>-Eigenschaft ändern, und um sie höher zu machen, müssen Sie die <xref:System.Drawing.Size.Width%2A>-Eigenschaft ändern.</span><span class="sxs-lookup"><span data-stu-id="e6d85-113">As a result, in order to make the tabs wider, you must change the <xref:System.Drawing.Size.Height%2A> property, and in order to make them taller, you must change the <xref:System.Drawing.Size.Width%2A> property.</span></span>  
  
     <span data-ttu-id="e6d85-114">Für ein optimales Ergebnis mit dem folgenden Codebeispiel legen Sie die <xref:System.Drawing.Size.Width%2A> der Registerkarten auf 25 und die <xref:System.Drawing.Size.Height%2A> auf 100 fest.</span><span class="sxs-lookup"><span data-stu-id="e6d85-114">For best result with the code example below, set the <xref:System.Drawing.Size.Width%2A> of the tabs to 25 and the <xref:System.Drawing.Size.Height%2A> to 100.</span></span>  
  
5. <span data-ttu-id="e6d85-115">Legen Sie die <xref:System.Windows.Forms.TabControl.DrawMode%2A> -Eigenschaft auf <xref:System.Windows.Forms.TabDrawMode.OwnerDrawFixed>fest.</span><span class="sxs-lookup"><span data-stu-id="e6d85-115">Set the <xref:System.Windows.Forms.TabControl.DrawMode%2A> property to <xref:System.Windows.Forms.TabDrawMode.OwnerDrawFixed>.</span></span>  
  
6. <span data-ttu-id="e6d85-116">Definieren Sie einen Ereignishandler für das <xref:System.Windows.Forms.TabControl.DrawItem>-Ereignis des <xref:System.Windows.Forms.TabControl>, das den Text von links nach rechts rendert.</span><span class="sxs-lookup"><span data-stu-id="e6d85-116">Define a handler for the <xref:System.Windows.Forms.TabControl.DrawItem> event of <xref:System.Windows.Forms.TabControl> that renders the text from left to right.</span></span>  
  
     [!code-csharp[TabControl.RightAlignedTabs#1](~/samples/snippets/csharp/VS_Snippets_Winforms/TabControl.RightAlignedTabs/CS/Form1.cs#1)]
     [!code-vb[TabControl.RightAlignedTabs#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/TabControl.RightAlignedTabs/VB/Form1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="e6d85-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6d85-117">See also</span></span>

- [<span data-ttu-id="e6d85-118">TabControl-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e6d85-118">TabControl Control</span></span>](tabcontrol-control-windows-forms.md)
