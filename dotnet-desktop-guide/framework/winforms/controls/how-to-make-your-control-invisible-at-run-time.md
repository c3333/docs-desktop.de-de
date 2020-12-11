---
title: 'Vorgehensweise: Ausblenden des Steuerelements zur Laufzeit'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], making invisible at run time
- invisible controls
- user controls [Windows Forms], invisible
- custom controls [Windows Forms], invisible
- run time [Windows Forms], making controls invisible
ms.assetid: 69eb2e72-32f5-4f79-a157-c2c5f60c1628
ms.openlocfilehash: e9af529541a40a951d6defea180dbbef04c8f3be
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974808"
---
# <a name="how-to-make-your-control-invisible-at-run-time"></a><span data-ttu-id="7bb87-102">Vorgehensweise: Ausblenden des Steuerelements zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="7bb87-102">How to: Make Your Control Invisible at Run Time</span></span>
<span data-ttu-id="7bb87-103">Es kann vorkommen, dass Sie ein Benutzer Steuerelement erstellen möchten, das zur Laufzeit unsichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="7bb87-103">There are times when you might want to create a user control that is invisible at run time.</span></span> <span data-ttu-id="7bb87-104">Beispielsweise ist ein Steuerelement, das eine Wecker-Uhr ist, möglicherweise unsichtbar, außer wenn der Alarm ertönt.</span><span class="sxs-lookup"><span data-stu-id="7bb87-104">For example, a control that is an alarm clock might be invisible except when the alarm was sounding.</span></span> <span data-ttu-id="7bb87-105">Dies lässt sich problemlos erreichen, indem die-Eigenschaft festgelegt wird <xref:System.Windows.Forms.Control.Visible%2A> .</span><span class="sxs-lookup"><span data-stu-id="7bb87-105">This is easily accomplished by setting the <xref:System.Windows.Forms.Control.Visible%2A> property.</span></span> <span data-ttu-id="7bb87-106">Wenn die- <xref:System.Windows.Forms.Control.Visible%2A> Eigenschaft ist `true` , wird das Steuerelement normal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7bb87-106">If the <xref:System.Windows.Forms.Control.Visible%2A> property is `true`, your control will appear as normal.</span></span> <span data-ttu-id="7bb87-107">Wenn `false` , wird das Steuerelement ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="7bb87-107">If `false`, your control will be hidden.</span></span> <span data-ttu-id="7bb87-108">Obwohl Code in Ihrem Steuerelement möglicherweise weiterhin ausgeführt wird und unsichtbar ist, können Sie nicht über die Benutzeroberfläche mit dem Steuerelement interagieren.</span><span class="sxs-lookup"><span data-stu-id="7bb87-108">Although code in your control may still run while invisible, you will not be able to interact with the control through the user interface.</span></span> <span data-ttu-id="7bb87-109">Wenn Sie ein unsichtbares Steuerelement erstellen möchten, das weiterhin auf Benutzereingaben antwortet (z. b. Mausklicks), sollten Sie ein transparentes Steuerelement erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bb87-109">If you want to create an invisible control that still responds to user input (for example, mouse clicks), you should create a transparent control.</span></span> <span data-ttu-id="7bb87-110">Weitere Informationen finden Sie unter [Erteilen eines transparenten Hintergrunds für ein Steuer](how-to-give-your-control-a-transparent-background.md)Element.</span><span class="sxs-lookup"><span data-stu-id="7bb87-110">For more information, see [Giving Your Control a Transparent Background](how-to-give-your-control-a-transparent-background.md).</span></span>  
  
### <a name="to-make-your-control-invisible-at-run-time"></a><span data-ttu-id="7bb87-111">So machen Sie das Steuerelement zur Laufzeit unsichtbar</span><span class="sxs-lookup"><span data-stu-id="7bb87-111">To make your control invisible at run time</span></span>  
  
1. <span data-ttu-id="7bb87-112">Legen Sie die <xref:System.Windows.Forms.Control.Visible%2A> -Eigenschaft auf `false`fest.</span><span class="sxs-lookup"><span data-stu-id="7bb87-112">Set the <xref:System.Windows.Forms.Control.Visible%2A> property to `false`.</span></span>  
  
    ```vb  
    ' To set the Visible property from within your object's own code.  
    Me.Visible = False  
    ' To set the Visible property from another object.  
    myControl1.Visible = False  
    ```  
  
    ```csharp  
    // To set the Visible property from within your object's own code.  
    this.Visible = false;  
    // To set the Visible property from another object.  
    myControl1.Visible = false;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="7bb87-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bb87-113">See also</span></span>

- <xref:System.Windows.Forms.Control.Visible%2A>
- [<span data-ttu-id="7bb87-114">Entwickeln benutzerdefinierter Windows Forms-Steuerelemente mit .NET Framework</span><span class="sxs-lookup"><span data-stu-id="7bb87-114">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="7bb87-115">Vorgehensweise: Verwenden eines transparenten Hintergrunds für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7bb87-115">How to: Give Your Control a Transparent Background</span></span>](how-to-give-your-control-a-transparent-background.md)
