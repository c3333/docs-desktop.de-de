---
title: 'Gewusst wie: Löschen von Freihandeingaben auf einem benutzerdefinierten Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [WPF], erasing ink on
- ink [WPF], erasing on custom control
ms.assetid: d88c50f9-b4d8-4962-a28b-67d6a15a5fe0
ms.openlocfilehash: 60e2af64cb0c5b313f4f1201cab70da6a88f61e7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977576"
---
# <a name="how-to-erase-ink-on-a-custom-control"></a><span data-ttu-id="74e24-102">Gewusst wie: Löschen von Freihandeingaben auf einem benutzerdefinierten Steuerelement</span><span class="sxs-lookup"><span data-stu-id="74e24-102">How to: Erase Ink on a Custom Control</span></span>
<span data-ttu-id="74e24-103"><xref:System.Windows.Ink.IncrementalStrokeHitTester>Bestimmt, ob der aktuell gezeichnete Strich einen anderen Strich schneidet.</span><span class="sxs-lookup"><span data-stu-id="74e24-103">The <xref:System.Windows.Ink.IncrementalStrokeHitTester> determines whether the currently drawn stroke intersects another stroke.</span></span>  <span data-ttu-id="74e24-104">Dies ist nützlich, um ein Steuerelement zu erstellen, mit dem ein Benutzer Teile eines Strichs löschen kann. Dies ist die Art und Weise, in der ein Benutzer auf einem <xref:System.Windows.Controls.InkCanvas> <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> festgelegt ist <xref:System.Windows.Controls.InkCanvasEditingMode.EraseByPoint></span><span class="sxs-lookup"><span data-stu-id="74e24-104">This is useful for creating a control that enables a user to erase parts of a stroke, the way a user can on an <xref:System.Windows.Controls.InkCanvas> when the <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> is set to <xref:System.Windows.Controls.InkCanvasEditingMode.EraseByPoint>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="74e24-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="74e24-105">Example</span></span>  
 <span data-ttu-id="74e24-106">Im folgenden Beispiel wird ein benutzerdefiniertes Steuerelement erstellt, das es dem Benutzer ermöglicht, Teile von Strichen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="74e24-106">The following example creates a custom control that enables the user to erase parts of strokes.</span></span>  <span data-ttu-id="74e24-107">Dieses Beispiel erstellt ein Steuerelement, das frei Hand Eingaben enthält, wenn es initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="74e24-107">This example creates a control that contains ink when it is initialized.</span></span>  <span data-ttu-id="74e24-108">Informationen zum Erstellen eines Steuer Elements, das frei Hand Eingaben sammelt, finden Sie unter [Creating an Ink Input Control](creating-an-ink-input-control.md).</span><span class="sxs-lookup"><span data-stu-id="74e24-108">To create a control that collects ink, see [Creating an Ink Input Control](creating-an-ink-input-control.md).</span></span>  
  
 [!code-csharp[HowToEraseInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToEraseInk/CSharp/InkEraser.cs#1)]
 [!code-vb[HowToEraseInk#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToEraseInk/VisualBasic/InkEraser.vb#1)]
