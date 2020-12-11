---
title: Erstellen eines Rahmens um ein Steuerelement mithilfe von Padding
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- margins
- controls [Windows Forms], Margin property
- padding [Windows Forms], Windows Forms
- controls [Windows Forms], Padding property
- controls [Windows Forms], outlining
- Padding property [Windows Forms]
- margins [Windows Forms], Windows Forms
- Margin property [Windows Forms]
ms.assetid: bac7ed4d-a163-4259-98bd-155a36345890
ms.openlocfilehash: 114186ab5784cf892cb01e9fe2648ce22cecc4b7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976340"
---
# <a name="how-to-create-a-border-around-a-windows-forms-control-using-padding"></a><span data-ttu-id="8fa93-102">Vorgehensweise: Erstellen eines Rahmens um ein Windows Forms-Steuerelement mithilfe von Abständen</span><span class="sxs-lookup"><span data-stu-id="8fa93-102">How to: Create a Border Around a Windows Forms Control Using Padding</span></span>
<span data-ttu-id="8fa93-103">Im folgenden Codebeispiel wird veranschaulicht, wie Sie einen Rahmen oder eine Gliederung um ein-Steuerelement erstellen <xref:System.Windows.Forms.RichTextBox> .</span><span class="sxs-lookup"><span data-stu-id="8fa93-103">The following code example demonstrates how to create a border or outline around a <xref:System.Windows.Forms.RichTextBox> control.</span></span> <span data-ttu-id="8fa93-104">Im Beispiel wird der Wert der <xref:System.Windows.Forms.Panel> -Eigenschaft eines Steuer Elements <xref:System.Windows.Forms.Padding> auf 5 festgelegt, und die-Eigenschaft eines untergeordneten Steuer Elements wird auf festgelegt <xref:System.Windows.Forms.Control.Dock%2A> <xref:System.Windows.Forms.RichTextBox> <xref:System.Windows.Forms.DockStyle.Fill> .</span><span class="sxs-lookup"><span data-stu-id="8fa93-104">The example sets the value of a <xref:System.Windows.Forms.Panel> control’s <xref:System.Windows.Forms.Padding> property to 5 and sets the <xref:System.Windows.Forms.Control.Dock%2A> property of a child <xref:System.Windows.Forms.RichTextBox> control to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span> <span data-ttu-id="8fa93-105">Der <xref:System.Windows.Forms.Control.BackColor%2A> des <xref:System.Windows.Forms.Panel> Steuer Elements ist auf festgelegt <xref:System.Drawing.Color.Blue%2A> , wodurch ein blauer Rahmen um das Steuerelement erstellt wird <xref:System.Windows.Forms.RichTextBox> .</span><span class="sxs-lookup"><span data-stu-id="8fa93-105">The <xref:System.Windows.Forms.Control.BackColor%2A> of the <xref:System.Windows.Forms.Panel> control is set to <xref:System.Drawing.Color.Blue%2A>, which creates a blue border around the <xref:System.Windows.Forms.RichTextBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8fa93-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8fa93-106">Example</span></span>  
 [!code-csharp[System.Windows.Forms.Padding#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Padding/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.Padding#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Padding/VB/Form1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="8fa93-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fa93-107">See also</span></span>

- <xref:System.Windows.Forms.Padding>
- [<span data-ttu-id="8fa93-108">Rand und Abstand in Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="8fa93-108">Margin and Padding in Windows Forms Controls</span></span>](margin-and-padding-in-windows-forms-controls.md)
