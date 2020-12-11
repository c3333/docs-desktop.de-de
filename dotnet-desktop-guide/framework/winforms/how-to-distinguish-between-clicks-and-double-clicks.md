---
title: 'Vorgehensweise: Unterscheiden zwischen Klicks und Doppelklicks'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- mouse [Windows Forms], click
- mouse [Windows Forms], double-click
- mouse clicks [Windows Forms], single versus double
ms.assetid: d836ac8c-85bc-4f3a-a761-8aee03dc682c
ms.openlocfilehash: cff6c283651b5994e869756524a3ee83ecdcfda9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972295"
---
# <a name="how-to-distinguish-between-clicks-and-double-clicks"></a>Vorgehensweise: Unterscheiden zwischen Klicks und Doppelklicks
Normalerweise wird mit einem einzigen *Klick* eine Benutzerschnittstellenaktion initiiert, und mit einem *Doppelklick* wird die Aktion erweitert. So wird mit einem einzigen Klick ein Element markiert, und mit einem Doppelklick wird das ausgewählte Element bearbeitet. Allerdings lassen sich die Windows Forms-Klickereignisse nicht so einfach an ein Szenario anpassen, in dem ein Klick und ein Doppelklick inkompatible Aktionen ausführen, da eine Aktion, die mit dem <xref:System.Windows.Forms.Control.Click>- oder <xref:System.Windows.Forms.Control.MouseClick>-Ereignis verknüpft ist, ausgeführt wird, bevor die mit dem <xref:System.Windows.Forms.Control.DoubleClick>- oder <xref:System.Windows.Forms.Control.MouseDoubleClick>-Ereignis verknüpfte Aktion ausgeführt wird. In diesem Thema werden zwei Lösungen für dieses Problem erörtert. Eine Lösung besteht darin, das Doppelklickereignis zu behandeln und ein Rollback der Aktionen in der Behandlung des Klickereignisses zu initiieren. In selten Fällen müssen Sie ggf. das Klick- und Doppelklickverhalten simulieren, indem Sie das <xref:System.Windows.Forms.Control.MouseDown>-Ereignis behandeln und dabei die Eigenschaften <xref:System.Windows.Forms.SystemInformation.DoubleClickTime%2A> und <xref:System.Windows.Forms.SystemInformation.DoubleClickSize%2A> der <xref:System.Windows.Forms.SystemInformation>-Klasse verwenden. Sie messen die Zeit zwischen den Klicks, und wenn ein zweiter Klick erfolgt, bevor der Wert von <xref:System.Windows.Forms.SystemInformation.DoubleClickTime%2A> erreicht wurde und der Klick innerhalb des von <xref:System.Windows.Forms.SystemInformation.DoubleClickSize%2A> definierten Rechtecks erfolgt ist, führen Sie die Doppelklickaktion aus, andernfalls führen Sie die Klickaktion aus.  
  
### <a name="to-roll-back-a-click-action"></a>So führen Sie ein Rollback einer Klickaktion durch  
  
- Vergewissern Sie sich, dass das Steuerelement, mit dem Sie arbeiten, über das standardmäßig Doppelklickverhalten verfügt. Andernfalls aktivieren Sie das Steuerelement mit der <xref:System.Windows.Forms.Control.SetStyle%2A>-Methode. Behandeln Sie das Doppelklickereignis, und führen Sie ein Rollback der Klickaktion und der Doppelklickaktion durch. Im folgenden Codebeispiel wird gezeigt, wie eine benutzerdefinierte Schaltfläche mit aktiviertem Doppelklick erstellt und wie ein Rollback der Klickaktion im Behandlungscode des Doppelklickereignisses initiiert wird.  
  
     [!code-csharp[System.Windows.Forms.ButtonDoubleClick#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ButtonDoubleClick/CS/Form1.cs#1)]
     [!code-vb[System.Windows.Forms.ButtonDoubleClick#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ButtonDoubleClick/VB/Form1.vb#1)]  
  
### <a name="to-distinguish-between-clicks-in-the-mousedown-event"></a>So unterscheiden Sie zwischen Klicks im MouseDown-Ereignis  
  
- Behandeln Sie das <xref:System.Windows.Forms.Control.MouseDown>-Ereignis, und ermitteln Sie die Position und die Zeitspanne zwischen Klicks mit den geeigneten <xref:System.Windows.Forms.SystemInformation>-Eigenschaften und einer <xref:System.Windows.Forms.Timer>-Komponente. Machen Sie die geeignete Aktion davon abhängig, ob ein Klick oder ein Doppelklick stattfindet. Das folgende Codebeispiel veranschaulicht, wie Sie dabei vorgehen.  
  
     [!code-cpp[System.Windows.Forms.SingleVersusDoubleClick#0](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.SingleVersusDoubleClick/cpp/form1.cpp#0)]
     [!code-csharp[System.Windows.Forms.SingleVersusDoubleClick#0](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.SingleVersusDoubleClick/CS/form1.cs#0)]
     [!code-vb[System.Windows.Forms.SingleVersusDoubleClick#0](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.SingleVersusDoubleClick/VB/form1.vb#0)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Voraussetzungen für diese Beispiele sind:  
  
- Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".  
  
## <a name="see-also"></a>Siehe auch

- [Mauseingabe in einer Windows Forms-Anwendung](mouse-input-in-a-windows-forms-application.md)
