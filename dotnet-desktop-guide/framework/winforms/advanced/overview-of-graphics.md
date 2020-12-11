---
title: Übersicht über Grafiken
ms.date: 03/30/2017
ms.topic: overview
helpviewer_keywords:
- graphics [Windows Forms], using managed interface
- graphics [Windows Forms], about graphics
ms.assetid: a602aef8-a8c8-4c36-9816-74e7bad96a68
ms.openlocfilehash: e2cc534c32c24f3ac13248bd16b177205e480820
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975264"
---
# <a name="overview-of-graphics"></a>Übersicht über Grafiken
GDI+ ist eine Anwendungsprogrammierschnittstelle (Application Programming Interface, API), die das Subsystem des Microsoft Windows-Betriebssystems bildet. GDI+ ist dafür verantwortlich, Informationen auf Bildschirmen und Druckern anzuzeigen. Wie der Name schon sagt, ist GDI+ der Nachfolger für GDI, der in früheren Versionen von Windows enthaltene Graphics Device Interface.  
  
## <a name="managed-class-interface"></a>Schnittstelle für verwaltete Klassen  
 Die GDI+-API wird durch einen Satz von Klassen verfügbar gemacht, die als verwalteter Code bereitgestellt werden. Dieser Satz von Klassen wird als *Schnittstelle der verwalteten Klasse* zu GDI+ bezeichnet. Die Schnittstelle für verwaltete Klassen besteht aus den folgenden Namespaces:  
  
- <xref:System.Drawing>  
  
- <xref:System.Drawing.Drawing2D>  
  
- <xref:System.Drawing.Imaging>  
  
- <xref:System.Drawing.Text>  
  
- <xref:System.Drawing.Printing>  
  
 Bei einer Graphics Device Interface, z. b. GDI+, können Sie Informationen auf einem Bildschirm oder Drucker anzeigen, ohne sich Gedanken über die Details eines bestimmten Anzeige Geräts machen zu müssen. Der Programmierer führt Aufrufe an Methoden aus, die von GDI+-Klassen bereitgestellt werden. In diesen Methoden wiederum werden die speziellen Gerätetreiber aufgerufen. GDI+ isoliert die Anwendung von der Grafikhardware. Diese Isolierung versetzt den Programmierer in die Lage, geräteunabhängige Anwendungen erstellen zu können.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Grafiken](graphics-overview-windows-forms.md)
