---
title: Behandeln von Benutzereingabe Ereignissen in Steuerelementen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms controls, user input
- user input [Windows Forms], Windows Forms controls
ms.assetid: 3de74dcf-fae3-42d0-92b5-bc04a61a6888
ms.openlocfilehash: 19adeb6c803c76cba4139841f58087487d523a50
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976936"
---
# <a name="how-to-handle-user-input-events-in-windows-forms-controls"></a>Vorgehensweise: Behandeln von Benutzereingabeereignissen in Windows Forms-Steuerelementen
In diesem Beispiel wird veranschaulicht, wie die meisten Tastatur-, Maus-, Fokus- und Validierungsereignisse behandelt werden, die in einem Windows Forms-Steuerelement auftreten können. Das Textfeld `TextBoxInput` empfängt die Ereignisse, wenn es den Fokus besitzt; Informationen zu den einzelnen Ereignissen werden in der Reihenfolge, in der die Ereignisse ausgelöst werden, in das Textfeld `TextBoxOutput` geschrieben. Die Anwendung verfügt zudem über eine Reihe von Kontrollkästchen, mit denen gefiltert werden kann, welche Ereignisse gemeldet werden.  
  
## <a name="example"></a>Beispiel  
 [!code-cpp[System.Windows.Forms.UserInputWalkthrough#0](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/cpp/form1.cpp#0)]
 [!code-csharp[System.Windows.Forms.UserInputWalkthrough#0](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/CS/form1.cs#0)]
 [!code-vb[System.Windows.Forms.UserInputWalkthrough#0](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.UserInputWalkthrough/VB/form1.vb#0)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".  
  
## <a name="see-also"></a>Siehe auch

- [Benutzereingabe in Windows Forms](user-input-in-windows-forms.md)
