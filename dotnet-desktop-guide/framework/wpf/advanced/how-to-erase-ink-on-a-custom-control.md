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
# <a name="how-to-erase-ink-on-a-custom-control"></a>Gewusst wie: Löschen von Freihandeingaben auf einem benutzerdefinierten Steuerelement
<xref:System.Windows.Ink.IncrementalStrokeHitTester>Bestimmt, ob der aktuell gezeichnete Strich einen anderen Strich schneidet.  Dies ist nützlich, um ein Steuerelement zu erstellen, mit dem ein Benutzer Teile eines Strichs löschen kann. Dies ist die Art und Weise, in der ein Benutzer auf einem <xref:System.Windows.Controls.InkCanvas> <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> festgelegt ist <xref:System.Windows.Controls.InkCanvasEditingMode.EraseByPoint>  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein benutzerdefiniertes Steuerelement erstellt, das es dem Benutzer ermöglicht, Teile von Strichen zu löschen.  Dieses Beispiel erstellt ein Steuerelement, das frei Hand Eingaben enthält, wenn es initialisiert wird.  Informationen zum Erstellen eines Steuer Elements, das frei Hand Eingaben sammelt, finden Sie unter [Creating an Ink Input Control](creating-an-ink-input-control.md).  
  
 [!code-csharp[HowToEraseInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToEraseInk/CSharp/InkEraser.cs#1)]
 [!code-vb[HowToEraseInk#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToEraseInk/VisualBasic/InkEraser.vb#1)]
