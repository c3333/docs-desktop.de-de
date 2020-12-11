---
title: 'Vorgehensweise: Definieren des Verhaltens bei Größen- und Positionsänderungen in einem geteilten Fenster'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- split windows [Windows Forms], resizing
- splitter windows [Windows Forms], resizing
- SplitContainer control [Windows Forms], resizing
ms.assetid: 9bf73f36-ed2d-4a02-b15a-0770eff4fdfa
ms.openlocfilehash: 8cdcfdfaa135a92ed6a6e96d4a72de2c97f2493d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975678"
---
# <a name="how-to-define-resize-and-positioning-behavior-in-a-split-window"></a><span data-ttu-id="e2d5a-102">Vorgehensweise: Definieren des Verhaltens bei Größen- und Positionsänderungen in einem geteilten Fenster</span><span class="sxs-lookup"><span data-stu-id="e2d5a-102">How to: Define Resize and Positioning Behavior in a Split Window</span></span>
<span data-ttu-id="e2d5a-103">Die Bereiche des <xref:System.Windows.Forms.SplitContainer> Steuer Elements eignen sich gut für die Größenänderung und Bearbeitung durch Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-103">The panels of the <xref:System.Windows.Forms.SplitContainer> control lend themselves well to being resized and manipulated by users.</span></span> <span data-ttu-id="e2d5a-104">Es gibt jedoch Zeiten, in denen Sie den Splitter Programm gesteuert steuern möchten – wo er positioniert ist und zu welchem Grad er verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-104">However, there will be times when you will want to programmatically control the splitter—where it is positioned and to what degree it can be moved.</span></span>  
  
 <span data-ttu-id="e2d5a-105">Mit der <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> -Eigenschaft und den anderen Eigenschaften des- <xref:System.Windows.Forms.SplitContainer> Steuer Elements können Sie das Verhalten ihrer Benutzeroberfläche genau an Ihre Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-105">The <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> property and the other properties on the <xref:System.Windows.Forms.SplitContainer> control give you precise control over the behavior of your user interface to suit your needs.</span></span> <span data-ttu-id="e2d5a-106">Diese Eigenschaften sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-106">These properties are listed in the following table.</span></span>  
  
|<span data-ttu-id="e2d5a-107">Name</span><span class="sxs-lookup"><span data-stu-id="e2d5a-107">Name</span></span>|<span data-ttu-id="e2d5a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2d5a-108">Description</span></span>|  
|----------|-----------------|  
|<span data-ttu-id="e2d5a-109"><xref:System.Windows.Forms.SplitContainer.IsSplitterFixed%2A> -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e2d5a-109"><xref:System.Windows.Forms.SplitContainer.IsSplitterFixed%2A> property</span></span>|<span data-ttu-id="e2d5a-110">Bestimmt, ob der Splitter mithilfe der Tastatur oder der Maus verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-110">Determines if the splitter is movable by means of the keyboard or mouse.</span></span>|  
|<span data-ttu-id="e2d5a-111"><xref:System.Windows.Forms.SplitContainer.SplitterDistance%2A> -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e2d5a-111"><xref:System.Windows.Forms.SplitContainer.SplitterDistance%2A> property</span></span>|<span data-ttu-id="e2d5a-112">Bestimmt den Abstand vom linken oder oberen Rand bis zur verschiebbaren Splitter Leiste in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-112">Determines the distance in pixels from the left or upper edge to the movable splitter bar.</span></span>|  
|<span data-ttu-id="e2d5a-113"><xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e2d5a-113"><xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> property</span></span>|<span data-ttu-id="e2d5a-114">Bestimmt den minimalen Abstand in Pixel, dass der Splitter vom Benutzer verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-114">Determines the minimum distance, in pixels, that the splitter can be moved by the user.</span></span>|  
  
 <span data-ttu-id="e2d5a-115">Im folgenden Beispiel wird die-Eigenschaft dahingehend geändert, dass <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> ein "Ausrichten von Trenn-Splitter"-Effekt erstellt wird. wenn der Benutzer den Splitter zieht, wird er in Einheiten von 10 Pixeln anstatt in der Standardeinstellung 1 erhöht.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-115">The example below modifies the <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> property to create a "snapping splitter" effect; when the user drags the splitter, it increments in units of 10 pixels rather than the default 1.</span></span>  
  
### <a name="to-define-splitcontainer-resize-behavior"></a><span data-ttu-id="e2d5a-116">So definieren Sie das Verhalten der SplitContainer-Größenänderung</span><span class="sxs-lookup"><span data-stu-id="e2d5a-116">To define SplitContainer resize behavior</span></span>  
  
1. <span data-ttu-id="e2d5a-117">Legen Sie die-Eigenschaft in einer-Prozedur <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> auf die gewünschte Größe fest, damit das "ausrichten"-Verhalten des Splitters erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-117">In a procedure, set the <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> property to the desired size, so that the 'snapping' behavior of the splitter is achieved.</span></span>  
  
     <span data-ttu-id="e2d5a-118">Im folgenden Codebeispiel wird im-Ereignis des Formulars der <xref:System.Windows.Forms.Form.Load> Splitter im-Steuerelement so festgelegt, dass beim Ziehen <xref:System.Windows.Forms.SplitContainer> 10 Pixel gesprungen werden.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-118">In the following code example, within the form's <xref:System.Windows.Forms.Form.Load> event, the splitter within the <xref:System.Windows.Forms.SplitContainer> control is set to jump 10 pixels when dragged.</span></span>  
  
    ```vb  
    Private Sub Form1_Load(ByVal sender As System.Object, _  
        ByVal e As System.EventArgs) Handles MyBase.Load  
        Dim splitSnapper as new SplitContainer()  
        splitSnapper.SplitterIncrement = 10  
        splitSnapper.Dock = DockStyle.Fill  
        splitSnapper.Parent = me  
    End Sub  
    ```  
  
    ```csharp  
    private void Form1_Load(System.Object sender, System.EventArgs e)  
    {  
        SplitContainer splitSnapper = new SplitContainer();  
        splitSnapper.SplitterIncrement = 10;  
        splitSnapper.Dock = DockStyle.Fill;  
        splitSnapper.Parent = this;  
    }  
    ```  
  
     <span data-ttu-id="e2d5a-119">(Visual c#) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-119">(Visual C#) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.Load += new System.EventHandler(this.Form1_Load);  
    ```  
  
     <span data-ttu-id="e2d5a-120">Das Verschieben des Splitters leicht nach links oder rechts hat keine erkennbaren Auswirkungen. Wenn der Mauszeiger jedoch 10 Pixel in beide Richtungen wechselt, wird der Splitter an der neuen Position ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="e2d5a-120">Moving the splitter slightly to the left or right will have no discernible effect; however, when the mouse pointer goes 10 pixels in either direction, the splitter will snap to the new position.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2d5a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2d5a-121">See also</span></span>

- <xref:System.Windows.Forms.SplitContainer>
- <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A>
