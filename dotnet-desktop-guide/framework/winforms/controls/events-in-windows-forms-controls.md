---
title: Ereignisse in Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- events [Windows Forms], custom controls (using code)
- custom controls [Windows Forms], events overview (using code)
ms.assetid: 7e3d1379-87aa-437c-afce-c99454eff30e
ms.openlocfilehash: 27edaf2d895453d64d35ba6eff724df583a9b7dd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975771"
---
# <a name="events-in-windows-forms-controls"></a>Ereignisse in Windows Forms-Steuerelementen

Ein Windows Forms-Steuerelement erbt mehr als 60 Ereignisse von <xref:System.Windows.Forms.Control?displayProperty=nameWithType> . Dazu gehört das <xref:System.Windows.Forms.Control.Paint> -Ereignis, das bewirkt, dass ein Steuerelement gezeichnet wird, Ereignisse im Zusammenhang mit dem Anzeigen eines Fensters, z <xref:System.Windows.Forms.Control.Resize> <xref:System.Windows.Forms.Control.Layout> . b. die Ereignisse und Einige Ereignisse auf niedriger Ebene werden <xref:System.Windows.Forms.Control> in Semantik Ereignisse wie und synthetisiert <xref:System.Windows.Forms.Control.Click> <xref:System.Windows.Forms.Control.DoubleClick> . Ausführliche Informationen zu geerbten Ereignissen finden Sie unter <xref:System.Windows.Forms.Control> .  
  
 Wenn das benutzerdefinierte Steuerelement geerbte Ereignisfunktionen überschreiben muss, hängen Sie keinen Delegaten an, sondern überschreiben Sie die geerbte Methode `On`*EventName*. Wenn Sie mit dem Ereignismodell in .NET Framework nicht vertraut sind, finden Sie unter [Auslösen von Ereignissen aus einer Komponente](/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)) weitere Informationen.  
  
## <a name="see-also"></a>Siehe auch

- [Überschreiben der OnPaint-Methode](overriding-the-onpaint-method.md)
- [Behandeln von Benutzereingaben](handling-user-input.md)
- [Definieren eines Ereignisses](defining-an-event-in-windows-forms-controls.md)
- [Ereignisse](/dotnet/standard/events/index)
