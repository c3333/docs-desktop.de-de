---
title: Label-Steuerelement
description: Hier erfahren Sie mehr über das Label-Steuerelement in Windows Forms für .NET. Bezeichnungen werden verwendet, um visuelle Elemente für den Benutzer zu identifizieren.
ms.date: 10/26/2020
ms.topic: overview
f1_keywords:
- Label
helpviewer_keywords:
- images [Windows Forms], displaying in labels
- labels
- Label control [Windows Forms], about Label control
ms.openlocfilehash: 6f669b7aef1182c35e125ff8dd3ca5ccb299b898
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942085"
---
# <a name="label-control-overview-windows-forms-net"></a><span data-ttu-id="13a2e-104">Übersicht über das Label-Steuerelement (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="13a2e-104">Label control overview (Windows Forms .NET)</span></span>

<span data-ttu-id="13a2e-105"><xref:System.Windows.Forms.Label>-Steuerelemente in Windows Forms werden verwendet, um Text anzuzeigen, der vom Benutzer nicht bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="13a2e-105">Windows Forms <xref:System.Windows.Forms.Label> controls are used to display text that cannot be edited by the user.</span></span> <span data-ttu-id="13a2e-106">Sie werden zum Identifizieren von Objekten in einem Formular und zum Bereitstellen einer Beschreibung verwendet, was ein bestimmtes Steuerelement darstellt oder macht.</span><span class="sxs-lookup"><span data-stu-id="13a2e-106">They're used to identify objects on a form and to provide a description of what a certain control represents or does.</span></span> <span data-ttu-id="13a2e-107">Beispielsweise können Sie Bezeichnungen verwenden, um unter anderem Textfeldern, Listenfeldern und Kombinationsfeldern beschreibende Beschriftungstexte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="13a2e-107">For example, you can use labels to add descriptive captions to text boxes, list boxes, combo boxes, and so on.</span></span> <span data-ttu-id="13a2e-108">Sie können auch Code schreiben, mit dem der Text geändert wird, der von einer Bezeichnung als Reaktion auf Ereignisse zur Laufzeit angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="13a2e-108">You can also write code that changes the text displayed by a label in response to events at run time.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="working-with-the-label-control"></a><span data-ttu-id="13a2e-109">Arbeiten mit dem Label-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="13a2e-109">Working with the Label Control</span></span>  

<span data-ttu-id="13a2e-110">Da das <xref:System.Windows.Forms.Label>-Steuerelement keinen Fokus erhalten kann, kann es zum Erstellen von Tastenkombinationen für andere Steuerelemente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13a2e-110">Because the <xref:System.Windows.Forms.Label> control can't receive focus, it can be used to create access keys for other controls.</span></span> <span data-ttu-id="13a2e-111">Mithilfe einer Tastenkombination kann ein Benutzer das nächste Steuerelement in der Aktivierreihenfolge fokussieren, indem er die <kbd>ALT-TASTE</kbd> mit der ausgewählten Tastenkombination drückt.</span><span class="sxs-lookup"><span data-stu-id="13a2e-111">An access key allows a user to focus the next control in tab order by pressing the <kbd>Alt</kbd> key with the chosen access key.</span></span> <span data-ttu-id="13a2e-112">Weitere Informationen finden Sie unter [Verwenden einer Bezeichnung zum Fokussieren eines Steuerelements](how-to-create-access-keys.md#use-a-label-to-focus-a-control).</span><span class="sxs-lookup"><span data-stu-id="13a2e-112">For more information, see [Use a label to focus a control](how-to-create-access-keys.md#use-a-label-to-focus-a-control).</span></span>
  
<span data-ttu-id="13a2e-113">Der in der Bezeichnung angezeigte Beschriftungstext ist in der <xref:System.Windows.Forms.Label.Text%2A>-Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="13a2e-113">The caption displayed in the label is contained in the <xref:System.Windows.Forms.Label.Text%2A> property.</span></span> <span data-ttu-id="13a2e-114">Mit der <xref:System.Windows.Forms.Label.TextAlign%2A>-Eigenschaft können Sie die Ausrichtung des Texts innerhalb der Bezeichnung festlegen.</span><span class="sxs-lookup"><span data-stu-id="13a2e-114">The <xref:System.Windows.Forms.Label.TextAlign%2A> property allows you to set the alignment of the text within the label.</span></span> <span data-ttu-id="13a2e-115">Weitere Informationen finden Sie unter [Vorgehensweise: Festlegen des durch ein Windows Forms-Steuerelement angezeigten Texts](how-to-set-the-display-text.md).</span><span class="sxs-lookup"><span data-stu-id="13a2e-115">For more information, see [How to: Set the Text Displayed by a Windows Forms Control](how-to-set-the-display-text.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="13a2e-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13a2e-116">See also</span></span>

- [<span data-ttu-id="13a2e-117">Verwenden einer Bezeichnung zum Fokussieren eines Steuerelements (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="13a2e-117">Use a label to focus a control (Windows Forms .NET)</span></span>](how-to-create-access-keys.md#use-a-label-to-focus-a-control)
- [<span data-ttu-id="13a2e-118">Vorgehensweise: Festlegen des durch ein Steuerelement angezeigten Texts (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="13a2e-118">How to: Set the text displayed by a control (Windows Forms .NET)</span></span>](how-to-set-the-display-text.md)
- <xref:System.Windows.Forms.ContainerControl.AutoScaleMode%2A>
- <xref:System.Windows.Forms.Control.Scale%2A>
- <xref:System.Windows.Forms.ContainerControl.PerformAutoScale%2A>
- <xref:System.Windows.Forms.ContainerControl.AutoScaleDimensions%2A>
