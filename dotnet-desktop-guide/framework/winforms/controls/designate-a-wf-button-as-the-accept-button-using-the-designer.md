---
title: Festlegen einer Schaltfläche als "annehmen"-Schaltfläche mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- buttons [Windows Forms], default on Windows Forms
- Accept button on Windows Forms
- Button control [Windows Forms], designating as default
- Windows Forms controls, default button on form
ms.assetid: a1da0590-755f-49f2-aca7-609fac6351bf
ms.openlocfilehash: 27a5de51f8c5b2c84cc205e09ac1a2179c315752
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972138"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-accept-button-using-the-designer"></a><span data-ttu-id="e7d11-102">Vorgehensweise: Definieren einer Windows Forms-Schaltfläche als „Annehmen“-Schaltfläche mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="e7d11-102">How to: Designate a Windows Forms Button as the Accept Button Using the Designer</span></span>
<span data-ttu-id="e7d11-103">In jedem Windows-Formular können Sie ein Steuerelement als <xref:System.Windows.Forms.Button> Accept-Schaltfläche festlegen, das auch als Standard Schaltfläche bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="e7d11-103">On any Windows Form, you can designate a <xref:System.Windows.Forms.Button> control to be the accept button, also known as the default button.</span></span> <span data-ttu-id="e7d11-104">Wenn der Benutzer die EINGABETASTE drückt, wird die Standard Schaltfläche unabhängig davon, welches andere Steuerelement im Formular den Fokus besitzt, angeklickt.</span><span class="sxs-lookup"><span data-stu-id="e7d11-104">Whenever the user presses the ENTER key, the default button is clicked regardless of which other control on the form has the focus.</span></span> <span data-ttu-id="e7d11-105">Dies gilt auch, wenn das Steuerelement mit dem Fokus eine andere Schaltfläche ist – in diesem Fall wird auf die Schaltfläche mit dem Fokus geklickt – oder ein mehrzeilige Textfeld oder ein benutzerdefiniertes Steuerelement, das die EINGABETASTE fängt.</span><span class="sxs-lookup"><span data-stu-id="e7d11-105">The exceptions to this are when the control with focus is another button — in that case, the button with the focus will be clicked — or a multiline text box, or a custom control that traps the ENTER key.</span></span>

## <a name="to-designate-the-accept-button"></a><span data-ttu-id="e7d11-106">So bestimmen Sie die Accept-Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="e7d11-106">To designate the accept button</span></span>

1. <span data-ttu-id="e7d11-107">Wählen Sie das Formular aus, in dem sich die Schaltfläche befindet.</span><span class="sxs-lookup"><span data-stu-id="e7d11-107">Select the form on which the button resides.</span></span>

2. <span data-ttu-id="e7d11-108">Legen Sie im Fenster **Eigenschaften** die-Eigenschaft des Formulars <xref:System.Windows.Forms.Form.AcceptButton%2A> auf den <xref:System.Windows.Forms.Button> Namen des-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="e7d11-108">In the **Properties** window, set the form's <xref:System.Windows.Forms.Form.AcceptButton%2A> property to the <xref:System.Windows.Forms.Button> control's name.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7d11-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7d11-109">See also</span></span>

- <xref:System.Windows.Forms.Form.AcceptButton%2A>
- [<span data-ttu-id="e7d11-110">Übersicht über das Button-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e7d11-110">Button Control Overview</span></span>](button-control-overview-windows-forms.md)
- [<span data-ttu-id="e7d11-111">Methoden zur Auswahl eines Button-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e7d11-111">Ways to Select a Windows Forms Button Control</span></span>](ways-to-select-a-windows-forms-button-control.md)
- [<span data-ttu-id="e7d11-112">Gewusst wie: Reagieren auf das Anklicken von Schaltflächen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e7d11-112">How to: Respond to Windows Forms Button Clicks</span></span>](how-to-respond-to-windows-forms-button-clicks.md)
- [<span data-ttu-id="e7d11-113">Vorgehensweise: Definieren einer Windows Forms-Schaltfläche als „Abbrechen“-Schaltfläche mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="e7d11-113">How to: Designate a Windows Forms Button as the Cancel Button Using the Designer</span></span>](designate-a-wf-button-as-the-cancel-button-using-the-designer.md)
- [<span data-ttu-id="e7d11-114">Button-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e7d11-114">Button Control</span></span>](button-control-windows-forms.md)
