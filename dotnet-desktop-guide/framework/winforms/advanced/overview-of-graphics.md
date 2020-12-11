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
# <a name="overview-of-graphics"></a><span data-ttu-id="a5778-102">Übersicht über Grafiken</span><span class="sxs-lookup"><span data-stu-id="a5778-102">Overview of Graphics</span></span>
<span data-ttu-id="a5778-103">GDI+ ist eine Anwendungsprogrammierschnittstelle (Application Programming Interface, API), die das Subsystem des Microsoft Windows-Betriebssystems bildet.</span><span class="sxs-lookup"><span data-stu-id="a5778-103">GDI+ is an application programming interface (API) that forms the subsystem of the Microsoft Windows operating system.</span></span> <span data-ttu-id="a5778-104">GDI+ ist dafür verantwortlich, Informationen auf Bildschirmen und Druckern anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a5778-104">GDI+ is responsible for displaying information on screens and printers.</span></span> <span data-ttu-id="a5778-105">Wie der Name schon sagt, ist GDI+ der Nachfolger für GDI, der in früheren Versionen von Windows enthaltene Graphics Device Interface.</span><span class="sxs-lookup"><span data-stu-id="a5778-105">As its name suggests, GDI+ is the successor to GDI, the Graphics Device Interface included with earlier versions of Windows.</span></span>  
  
## <a name="managed-class-interface"></a><span data-ttu-id="a5778-106">Schnittstelle für verwaltete Klassen</span><span class="sxs-lookup"><span data-stu-id="a5778-106">Managed Class Interface</span></span>  
 <span data-ttu-id="a5778-107">Die GDI+-API wird durch einen Satz von Klassen verfügbar gemacht, die als verwalteter Code bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a5778-107">The GDI+ API is exposed through a set of classes deployed as managed code.</span></span> <span data-ttu-id="a5778-108">Dieser Satz von Klassen wird als *Schnittstelle der verwalteten Klasse* zu GDI+ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a5778-108">This set of classes is called the *managed class interface* to GDI+.</span></span> <span data-ttu-id="a5778-109">Die Schnittstelle für verwaltete Klassen besteht aus den folgenden Namespaces:</span><span class="sxs-lookup"><span data-stu-id="a5778-109">The following namespaces make up the managed class interface:</span></span>  
  
- <xref:System.Drawing>  
  
- <xref:System.Drawing.Drawing2D>  
  
- <xref:System.Drawing.Imaging>  
  
- <xref:System.Drawing.Text>  
  
- <xref:System.Drawing.Printing>  
  
 <span data-ttu-id="a5778-110">Bei einer Graphics Device Interface, z. b. GDI+, können Sie Informationen auf einem Bildschirm oder Drucker anzeigen, ohne sich Gedanken über die Details eines bestimmten Anzeige Geräts machen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="a5778-110">With a Graphics Device Interface, such as GDI+, you can display information on a screen or printer without having to be concerned about the details of a particular display device.</span></span> <span data-ttu-id="a5778-111">Der Programmierer führt Aufrufe an Methoden aus, die von GDI+-Klassen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a5778-111">The programmer makes calls to methods provided by GDI+ classes.</span></span> <span data-ttu-id="a5778-112">In diesen Methoden wiederum werden die speziellen Gerätetreiber aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a5778-112">Those methods, in turn, make the appropriate calls to specific device drivers.</span></span> <span data-ttu-id="a5778-113">GDI+ isoliert die Anwendung von der Grafikhardware.</span><span class="sxs-lookup"><span data-stu-id="a5778-113">GDI+ insulates the application from the graphics hardware.</span></span> <span data-ttu-id="a5778-114">Diese Isolierung versetzt den Programmierer in die Lage, geräteunabhängige Anwendungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="a5778-114">It is this insulation that enables a programmer to create device-independent applications.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5778-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5778-115">See also</span></span>

- [<span data-ttu-id="a5778-116">Übersicht über Grafiken</span><span class="sxs-lookup"><span data-stu-id="a5778-116">Graphics Overview</span></span>](graphics-overview-windows-forms.md)
