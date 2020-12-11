---
title: Festlegen einer Schaltfläche als "Abbrechen"-Schaltfläche mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- buttons [Windows Forms], cancel buttons
- Button control [Windows Forms], designating as cancel button
ms.assetid: 30e77d9c-d565-4ab5-a84a-62c043af8822
ms.openlocfilehash: 95d1139b6e339055f944ad0b0967a6d91283d49e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972135"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-cancel-button-using-the-designer"></a><span data-ttu-id="980b6-102">Vorgehensweise: Definieren einer Windows Forms-Schaltfläche als „Abbrechen“-Schaltfläche mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="980b6-102">How to: Designate a Windows Forms Button as the Cancel Button Using the Designer</span></span>
<span data-ttu-id="980b6-103">In jedem Windows Form können Sie ein Steuerelement als <xref:System.Windows.Forms.Button> Schaltfläche "Abbrechen" festlegen.</span><span class="sxs-lookup"><span data-stu-id="980b6-103">On any Windows Form, you can designate a <xref:System.Windows.Forms.Button> control to be the cancel button.</span></span> <span data-ttu-id="980b6-104">Wenn der Benutzer die ESC-Taste drückt, wird auf eine Schaltfläche Abbrechen geklickt, unabhängig davon, welches andere Steuerelement im Formular den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="980b6-104">A cancel button is clicked whenever the user presses the ESC key, regardless of which other control on the form has the focus.</span></span> <span data-ttu-id="980b6-105">Eine solche Schaltfläche wird in der Regel so programmiert, dass der Benutzer schnell einen Vorgang beenden kann, ohne dass eine Aktion ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="980b6-105">Such a button is usually programmed to enable the user to quickly exit an operation without committing to any action.</span></span>

## <a name="to-designate-the-cancel-button"></a><span data-ttu-id="980b6-106">So bestimmen Sie die Schaltfläche Abbrechen</span><span class="sxs-lookup"><span data-stu-id="980b6-106">To designate the cancel button</span></span>

1. <span data-ttu-id="980b6-107">Wählen Sie das Formular aus, in dem sich die Schaltfläche befindet.</span><span class="sxs-lookup"><span data-stu-id="980b6-107">Select the form on which the button resides.</span></span>

2. <span data-ttu-id="980b6-108">Legen Sie im Fenster **Eigenschaften** die-Eigenschaft des Formulars <xref:System.Windows.Forms.Form.CancelButton%2A> auf den <xref:System.Windows.Forms.Button> Namen des-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="980b6-108">In the **Properties** window, set the form's <xref:System.Windows.Forms.Form.CancelButton%2A> property to the <xref:System.Windows.Forms.Button> control's name.</span></span>

## <a name="see-also"></a><span data-ttu-id="980b6-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="980b6-109">See also</span></span>

- <xref:System.Windows.Forms.Form.CancelButton%2A>
- [<span data-ttu-id="980b6-110">Übersicht über das Button-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="980b6-110">Button Control Overview</span></span>](button-control-overview-windows-forms.md)
- [<span data-ttu-id="980b6-111">Methoden zur Auswahl eines Button-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="980b6-111">Ways to Select a Windows Forms Button Control</span></span>](ways-to-select-a-windows-forms-button-control.md)
- [<span data-ttu-id="980b6-112">Gewusst wie: Reagieren auf das Anklicken von Schaltflächen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="980b6-112">How to: Respond to Windows Forms Button Clicks</span></span>](how-to-respond-to-windows-forms-button-clicks.md)
- [<span data-ttu-id="980b6-113">Vorgehensweise: Definieren einer Windows Forms-Schaltfläche als „Annehmen“-Schaltfläche mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="980b6-113">How to: Designate a Windows Forms Button as the Accept Button Using the Designer</span></span>](designate-a-wf-button-as-the-accept-button-using-the-designer.md)
- [<span data-ttu-id="980b6-114">Button-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="980b6-114">Button Control</span></span>](button-control-windows-forms.md)
