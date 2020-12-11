---
title: Koordinaten
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms coordinates
- screen coordinates
- client coordinates
- coordinates [Windows Forms], Windows Forms
ms.assetid: cc06e61f-43b6-4408-a676-2542dcfcd96e
ms.openlocfilehash: c95888f31bfc867e9c028d53072ab3d710256708
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974708"
---
# <a name="windows-forms-coordinates"></a>Windows Forms-Koordinaten
Das Koordinatensystem für ein Windows Form basiert auf Geräte Koordinaten, und die grundlegende Maßeinheit beim Zeichnen in Windows Forms ist die Geräteeinheit (in der Regel das Pixel). Die Punkte auf dem Bildschirm werden durch x-und y-Koordinatenpaare beschrieben, wobei die x-Koordinaten nach rechts und die y-Koordinaten von oben nach unten vergrößert werden. Die Position des Ursprungs (relativ zum Bildschirm) variiert abhängig davon, ob Sie Bildschirm-oder Client Koordinaten angeben.  
  
## <a name="screen-coordinates"></a>Bildschirm Koordinaten  
 Eine Windows Forms Anwendung gibt die Position eines Fensters auf dem Bildschirm in Bildschirm Koordinaten an. Bei Bildschirm Koordinaten wird der Ursprung in der oberen linken Ecke des Bildschirms angezeigt. Die vollständige Position eines Fensters wird häufig durch eine <xref:System.Drawing.Rectangle> Struktur beschrieben, die die Bildschirm Koordinaten zweier Punkte enthält, die die oberen linken und unteren rechten Ecke des Fensters definieren.  
  
## <a name="client-coordinates"></a>Client Koordinaten  
 Eine Windows Forms Anwendung gibt die Position von Punkten in einem Formular oder Steuerelement mithilfe von Client Koordinaten an. Der Ursprung für Client Koordinaten ist die linke obere Ecke des Client Bereichs des Steuer Elements oder Formulars. Mithilfe von Client Koordinaten wird sichergestellt, dass eine Anwendung beim Zeichnen in einem Formular oder Steuerelement konsistente Koordinaten Werte verwenden kann, unabhängig von der Position des Formulars oder Steuer Elements auf dem Bildschirm.  
  
 Die Abmessungen des Client Bereichs werden auch durch eine Struktur beschrieben <xref:System.Drawing.Rectangle> , die Client Koordinaten für den Bereich enthält. In allen Fällen ist die obere linke Koordinate des Rechtecks im Client Bereich enthalten, während die Koordinate der unteren rechten Seite ausgeschlossen wird. Grafik Vorgänge enthalten nicht den rechten und unteren Rand eines Client Bereichs. Die- <xref:System.Drawing.Graphics.FillRectangle%2A> Methode wird z. b. am rechten und unteren Rand des angegebenen Rechtecks aufgefüllt, enthält diese Ränder jedoch nicht.  
  
## <a name="mapping-from-one-type-of-coordinate-to-another"></a>Zuordnung von einem Koordinatentyp zu einem anderen  
 Gelegentlich müssen Sie möglicherweise von Bildschirm Koordinaten zu Client Koordinaten zuordnen. Dies können Sie problemlos erreichen, indem Sie die Methoden und verwenden, die <xref:System.Windows.Forms.Control.PointToClient%2A> <xref:System.Windows.Forms.Control.PointToScreen%2A> in der-Klasse verfügbar sind <xref:System.Windows.Forms.Control> . Beispielsweise wird die- <xref:System.Windows.Forms.Control.MousePosition%2A> Eigenschaft von <xref:System.Windows.Forms.Control> in Bildschirm Koordinaten gemeldet, Sie möchten Sie jedoch möglicherweise in Client Koordinaten konvertieren.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Control.PointToClient%2A>
- <xref:System.Windows.Forms.Control.PointToScreen%2A>
