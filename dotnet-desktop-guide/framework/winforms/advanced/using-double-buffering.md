---
title: Verwenden der doppelten Pufferung
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], double buffering
- double buffering
- flicker [Windows Forms], reducing in Windows Forms
- buffering [Windows Forms], double buffering
ms.assetid: dc484e33-7101-4e4b-ada5-d3c96155fbcd
ms.openlocfilehash: 5b22336221c7bdda3c9dd7adf23308a2b0bad450
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975232"
---
# <a name="using-double-buffering"></a>Verwenden der doppelten Pufferung
Sie können doppelt gepufferte Grafiken verwenden, um Flimmern in Ihren Anwendungen zu reduzieren, die komplexe Zeichnungsvorgänge enthalten. Der .NET Framework enthält integrierte Unterstützung für die doppelte Pufferung, oder Sie können Grafiken manuell verwalten und Renderern.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Doppelt gepufferte Grafiken](double-buffered-graphics.md)  
 Führt das Double-Puffer Konzept und die .NET Framework-Unterstützung ein.  
  
 [Vorgehensweise: Reduzieren von Grafikflimmern mit doppelter Pufferung für Formulare und Steuerelemente](how-to-reduce-graphics-flicker-with-double-buffering-for-forms-and-controls.md)  
 Veranschaulicht, wie die standardmäßige Unterstützung für die doppelte Pufferung in der .NET Framework verwendet wird.  
  
 [Vorgehensweise: Manuelles Verwalten von gepufferten Grafiken](how-to-manually-manage-buffered-graphics.md)  
 Zeigt, wie Sie die doppelte Pufferung in-Anwendungen verwalten.  
  
 [Vorgehensweise: Manuelles Rendern von gepufferten Grafiken](how-to-manually-render-buffered-graphics.md)  
 Veranschaulicht, wie Sie doppelt gepufferte Grafiken renderten.  
  
## <a name="reference"></a>Verweis  
 <xref:System.Windows.Forms.Control.SetStyle%2A> Steuerungsmethode, die die doppelte Pufferung ermöglicht.  
  
 <xref:System.Drawing.BufferedGraphicsContext> Stellt Methoden zum Erstellen von Grafik Puffern bereit.  
  
 <xref:System.Drawing.BufferedGraphicsManager>  
 Bietet Zugriff auf den gepufferten Grafik Kontext für eine Anwendungsdomäne.
