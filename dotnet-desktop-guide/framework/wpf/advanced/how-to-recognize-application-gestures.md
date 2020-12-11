---
title: 'Gewusst wie: Erkennen von Bewegungen in Anwendungen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- application gestures [WPF], recognizing
- gestures [WPF], recognizing
ms.assetid: d58b740f-5192-4a3e-af59-7aa162e6ca15
ms.openlocfilehash: 647e7c9c1d785cebfdc362dc48511d865f3945dc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977741"
---
# <a name="how-to-recognize-application-gestures"></a>Gewusst wie: Erkennen von Bewegungen in Anwendungen
Im folgenden Beispiel wird veranschaulicht, wie frei Hand Eingaben gelöscht werden, wenn ein Benutzer eine <xref:System.Windows.Ink.ApplicationGesture.ScratchOut> Geste für eine vornimmt <xref:System.Windows.Controls.InkCanvas> . In diesem Beispiel wird davon ausgegangen <xref:System.Windows.Controls.InkCanvas> , dass `inkCanvas1` in der XAML-Datei deklariert ist.  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[HowToRecognizeGestures#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToRecognizeGestures/CSharp/Window1.xaml.cs#1)]
 [!code-vb[HowToRecognizeGestures#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToRecognizeGestures/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Ink.ApplicationGesture>
- <xref:System.Windows.Controls.InkCanvas>
- <xref:System.Windows.Controls.InkCanvas.Gesture>
