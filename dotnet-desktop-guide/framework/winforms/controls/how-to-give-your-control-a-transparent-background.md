---
title: 'Vorgehensweise: Verwenden eines transparenten Hintergrunds für ein Steuerelement'
ms.date: 03/30/2017
helpviewer_keywords:
- transparent backgrounds [Windows Forms], custom controls
- custom controls [Windows Forms], transparent background
- transparency [Windows Forms], Windows Forms custom controls
ms.assetid: 32433e63-f4e9-4305-9857-6de3edeb944a
ms.openlocfilehash: a82807ea3873b2217d1f05f6c720c599ea79abdd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976495"
---
# <a name="how-to-give-your-control-a-transparent-background"></a><span data-ttu-id="cac2c-102">Vorgehensweise: Verwenden eines transparenten Hintergrunds für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="cac2c-102">How to: Give Your Control a Transparent Background</span></span>
<span data-ttu-id="cac2c-103">In früheren Versionen von .NET Framework wird für Steuerelemente ein Festlegen auf transparente Hintergrundfarben nur dann unterstützt, wenn zunächst die <xref:System.Windows.Forms.Control.SetStyle%2A> -Methode im Konstruktor der Formulare festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="cac2c-103">In earlier versions of the .NET Framework, controls didn't support setting transparent backcolors without first setting the <xref:System.Windows.Forms.Control.SetStyle%2A> method in the forms's constructor.</span></span> <span data-ttu-id="cac2c-104">In der aktuellen Framework-Version kann die Hintergrundfarbe für die meisten Steuerelemente zur Entwurfszeit im Fenster <xref:System.Drawing.Color.Transparent%2A> Eigenschaften **oder in Code im Konstruktor des Formulars auf** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cac2c-104">In the current framework version, the backcolor for most controls can be set to <xref:System.Drawing.Color.Transparent%2A> in the **Properties** window at design time, or in code in the form's constructor.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="cac2c-105">Windows Forms-Steuerelemente unterstützen keine echte Transparenz.</span><span class="sxs-lookup"><span data-stu-id="cac2c-105">Windows Forms controls do not support true transparency.</span></span> <span data-ttu-id="cac2c-106">Der Hintergrund eines transparenten Windows Forms-Steuerelements wird von seinem übergeordneten Element gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cac2c-106">The background of a transparent Windows Forms control is painted by its parent.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="cac2c-107">Das <xref:System.Windows.Controls.Button> -Steuerelement unterstützt keine transparente Hintergrundfarbe, selbst wenn die <xref:System.Windows.Forms.ButtonBase.BackColor%2A> -Eigenschaft auf <xref:System.Drawing.Color.Transparent%2A>festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cac2c-107">The <xref:System.Windows.Controls.Button> control doesn't support a transparent backcolor even when the <xref:System.Windows.Forms.ButtonBase.BackColor%2A> property is set to <xref:System.Drawing.Color.Transparent%2A>.</span></span>  
  
### <a name="to-give-your-control-a-transparent-backcolor"></a><span data-ttu-id="cac2c-108">So weisen Sie dem Steuerelement eine transparente Hintergrundfarbe zu</span><span class="sxs-lookup"><span data-stu-id="cac2c-108">To give your control a transparent backcolor</span></span>  
  
- <span data-ttu-id="cac2c-109">Wählen Sie im Eigenschaftenfenster die <xref:System.Windows.Forms.ButtonBase.BackColor%2A> -Eigenschaft aus, und legen Sie diese auf <xref:System.Drawing.Color.Transparent%2A>fest.</span><span class="sxs-lookup"><span data-stu-id="cac2c-109">In the Properties window, choose the <xref:System.Windows.Forms.ButtonBase.BackColor%2A> property and set it to <xref:System.Drawing.Color.Transparent%2A></span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cac2c-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cac2c-110">See also</span></span>

- <xref:System.Drawing.Color.FromArgb%2A>
- [<span data-ttu-id="cac2c-111">Entwickeln benutzerdefinierter Windows Forms-Steuerelemente mit .NET Framework</span><span class="sxs-lookup"><span data-stu-id="cac2c-111">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="cac2c-112">Verwenden von verwalteten Grafikklassen</span><span class="sxs-lookup"><span data-stu-id="cac2c-112">Using Managed Graphics Classes</span></span>](../advanced/using-managed-graphics-classes.md)
- [<span data-ttu-id="cac2c-113">Vorgehensweise: Zeichnen deckender und halbtransparenter Linien</span><span class="sxs-lookup"><span data-stu-id="cac2c-113">How to: Draw Opaque and Semitransparent Lines</span></span>](../advanced/how-to-draw-opaque-and-semitransparent-lines.md)
