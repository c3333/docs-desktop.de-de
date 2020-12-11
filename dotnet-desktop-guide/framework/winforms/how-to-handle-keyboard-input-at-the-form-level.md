---
title: 'Vorgehensweise: Behandeln von Tastatureingaben auf Formularebene'
description: Erfahren Sie, wie Tastatureingaben für Ihre Windows Forms auf Formular Ebene behandelt werden, bevor Nachrichten ein Steuerelement erreichen.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- keyboard input [Windows Forms], at form level
- Windows Forms, handling keyboard input
- keyboards [Windows Forms], form-level input
ms.assetid: d7f8b390-dc91-42d2-ae0f-2ffa388127ad
ms.openlocfilehash: 6f0695b6f665a613e0e4e001a4f9bbfc09dd45ed
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976289"
---
# <a name="how-to-handle-keyboard-input-at-the-form-level"></a><span data-ttu-id="9e77a-103">Vorgehensweise: Behandeln von Tastatureingaben auf Formularebene</span><span class="sxs-lookup"><span data-stu-id="9e77a-103">How to: Handle Keyboard Input at the Form Level</span></span>
<span data-ttu-id="9e77a-104">Windows Forms bieten die Möglichkeit, Tastatureingaben auf Formularebene zu behandeln, bevor die Eingaben an ein Steuerelement weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9e77a-104">Windows Forms provides the ability to handle keyboard messages at the form level, before the messages reach a control.</span></span> <span data-ttu-id="9e77a-105">In diesem Thema wird gezeigt, wie Sie diese Aufgabe ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e77a-105">This topic shows how to accomplish this task.</span></span>  
  
### <a name="to-handle-a-keyboard-message-at-the-form-level"></a><span data-ttu-id="9e77a-106">So behandeln Sie eine Tastatureingabe auf Formularebene</span><span class="sxs-lookup"><span data-stu-id="9e77a-106">To handle a keyboard message at the form level</span></span>  
  
- <span data-ttu-id="9e77a-107">Behandeln Sie das Ereignis <xref:System.Windows.Forms.Control.KeyPress> oder <xref:System.Windows.Forms.Control.KeyDown> im Startformular, und legen Sie die <xref:System.Windows.Forms.Form.KeyPreview%2A>-Eigenschaft des Formulars auf `true` fest, damit Tastatureingaben vom Formular empfangen werden, bevor sie an irgendeines der Steuerelemente auf dem Formular weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9e77a-107">Handle the <xref:System.Windows.Forms.Control.KeyPress> or <xref:System.Windows.Forms.Control.KeyDown> event of the startup form, and set the <xref:System.Windows.Forms.Form.KeyPreview%2A> property of the form to `true` so that keyboard messages are received by the form before they reach any controls on the form.</span></span> <span data-ttu-id="9e77a-108">Im folgenden Codebeispiel wird das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis behandelt, indem alle Zahlentasten erkannt und "1", "4" und "7" verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9e77a-108">The following code example handles the <xref:System.Windows.Forms.Control.KeyPress> event by detecting all of the number keys and consuming '1', '4', and '7'.</span></span>  
  
     [!code-cpp[System.Windows.Forms.KeyboardInputForm#10](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInputForm/cpp/form1.cpp#10)]
     [!code-csharp[System.Windows.Forms.KeyboardInputForm#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInputForm/CS/form1.cs#10)]
     [!code-vb[System.Windows.Forms.KeyboardInputForm#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInputForm/VB/form1.vb#10)]  
  
## <a name="example"></a><span data-ttu-id="9e77a-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e77a-109">Example</span></span>  
 <span data-ttu-id="9e77a-110">Das folgende Codebeispiel ist die vollständige Anwendung für das vorstehende Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="9e77a-110">The following code example is the entire application for the above example.</span></span> <span data-ttu-id="9e77a-111">Die Anwendung enthält ein <xref:System.Windows.Forms.TextBox> sowie mehrere andere Steuerelemente, die es Ihnen ermöglichen, den Fokus aus dem <xref:System.Windows.Forms.TextBox> zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="9e77a-111">The application includes a <xref:System.Windows.Forms.TextBox> along with several other controls that allow you to move focus from the <xref:System.Windows.Forms.TextBox>.</span></span> <span data-ttu-id="9e77a-112">Das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis der Haupt-<xref:System.Windows.Forms.Form> verarbeitet "1", "4" und "7", und das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis des <xref:System.Windows.Forms.TextBox> verarbeitet "2", "5" und "8", während die restlichen Tasten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9e77a-112">The <xref:System.Windows.Forms.Control.KeyPress> event of the main <xref:System.Windows.Forms.Form> consumes '1', '4', and '7', and the <xref:System.Windows.Forms.Control.KeyPress> event of the <xref:System.Windows.Forms.TextBox> consumes '2', '5', and '8' while displaying the remaining keys.</span></span> <span data-ttu-id="9e77a-113">Vergleichen Sie die Ausgabe von <xref:System.Windows.Forms.MessageBox>, wenn Sie eine Zahlentaste drücken, während das <xref:System.Windows.Forms.TextBox> den Fokus besitzt, mit der Ausgabe von <xref:System.Windows.Forms.MessageBox>, wenn sie eine Zahlentaste drücken, während eines der andere Steuerelemente den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="9e77a-113">Compare the <xref:System.Windows.Forms.MessageBox> output when you press a number key while the <xref:System.Windows.Forms.TextBox> has focus with the <xref:System.Windows.Forms.MessageBox> output when you press a number key while focus is on one of the other controls.</span></span>  
  
 [!code-cpp[System.Windows.Forms.KeyBoardInputForm#0](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInputForm/cpp/form1.cpp#0)]
 [!code-csharp[System.Windows.Forms.KeyBoardInputForm#0](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInputForm/CS/form1.cs#0)]
 [!code-vb[System.Windows.Forms.KeyBoardInputForm#0](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyboardInputForm/VB/form1.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9e77a-114">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="9e77a-114">Compiling the Code</span></span>  
 <span data-ttu-id="9e77a-115">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9e77a-115">This example requires:</span></span>  
  
- <span data-ttu-id="9e77a-116">Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="9e77a-116">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9e77a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e77a-117">See also</span></span>

- [<span data-ttu-id="9e77a-118">Tastatureingaben in einer Windows Forms-Anwendung</span><span class="sxs-lookup"><span data-stu-id="9e77a-118">Keyboard Input in a Windows Forms Application</span></span>](keyboard-input-in-a-windows-forms-application.md)
