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
# <a name="using-double-buffering"></a><span data-ttu-id="38536-102">Verwenden der doppelten Pufferung</span><span class="sxs-lookup"><span data-stu-id="38536-102">Using Double Buffering</span></span>
<span data-ttu-id="38536-103">Sie können doppelt gepufferte Grafiken verwenden, um Flimmern in Ihren Anwendungen zu reduzieren, die komplexe Zeichnungsvorgänge enthalten.</span><span class="sxs-lookup"><span data-stu-id="38536-103">You can use double-buffered graphics to reduce flicker in your applications that contain complex painting operations.</span></span> <span data-ttu-id="38536-104">Der .NET Framework enthält integrierte Unterstützung für die doppelte Pufferung, oder Sie können Grafiken manuell verwalten und Renderern.</span><span class="sxs-lookup"><span data-stu-id="38536-104">The .NET Framework contains built-in support for double-buffering or you can manage and render graphics manually.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="38536-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="38536-105">In This Section</span></span>  
 [<span data-ttu-id="38536-106">Doppelt gepufferte Grafiken</span><span class="sxs-lookup"><span data-stu-id="38536-106">Double Buffered Graphics</span></span>](double-buffered-graphics.md)  
 <span data-ttu-id="38536-107">Führt das Double-Puffer Konzept und die .NET Framework-Unterstützung ein.</span><span class="sxs-lookup"><span data-stu-id="38536-107">Introduces double buffering concept and outlines .NET Framework support.</span></span>  
  
 [<span data-ttu-id="38536-108">Vorgehensweise: Reduzieren von Grafikflimmern mit doppelter Pufferung für Formulare und Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="38536-108">How to: Reduce Graphics Flicker with Double Buffering for Forms and Controls</span></span>](how-to-reduce-graphics-flicker-with-double-buffering-for-forms-and-controls.md)  
 <span data-ttu-id="38536-109">Veranschaulicht, wie die standardmäßige Unterstützung für die doppelte Pufferung in der .NET Framework verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38536-109">Demonstrates how to use the default double buffering support in the .NET Framework.</span></span>  
  
 [<span data-ttu-id="38536-110">Vorgehensweise: Manuelles Verwalten von gepufferten Grafiken</span><span class="sxs-lookup"><span data-stu-id="38536-110">How to: Manually Manage Buffered Graphics</span></span>](how-to-manually-manage-buffered-graphics.md)  
 <span data-ttu-id="38536-111">Zeigt, wie Sie die doppelte Pufferung in-Anwendungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="38536-111">Shows how to manage double buffering in applications.</span></span>  
  
 [<span data-ttu-id="38536-112">Vorgehensweise: Manuelles Rendern von gepufferten Grafiken</span><span class="sxs-lookup"><span data-stu-id="38536-112">How to: Manually Render Buffered Graphics</span></span>](how-to-manually-render-buffered-graphics.md)  
 <span data-ttu-id="38536-113">Veranschaulicht, wie Sie doppelt gepufferte Grafiken renderten.</span><span class="sxs-lookup"><span data-stu-id="38536-113">Demonstrates how to render double-buffered graphics.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="38536-114">Verweis</span><span class="sxs-lookup"><span data-stu-id="38536-114">Reference</span></span>  
 <span data-ttu-id="38536-115"><xref:System.Windows.Forms.Control.SetStyle%2A> Steuerungsmethode, die die doppelte Pufferung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="38536-115"><xref:System.Windows.Forms.Control.SetStyle%2A> Control method that enables double buffering.</span></span>  
  
 <span data-ttu-id="38536-116"><xref:System.Drawing.BufferedGraphicsContext> Stellt Methoden zum Erstellen von Grafik Puffern bereit.</span><span class="sxs-lookup"><span data-stu-id="38536-116"><xref:System.Drawing.BufferedGraphicsContext> Provides methods for creating graphics buffers.</span></span>  
  
 <xref:System.Drawing.BufferedGraphicsManager>  
 <span data-ttu-id="38536-117">Bietet Zugriff auf den gepufferten Grafik Kontext für eine Anwendungsdomäne.</span><span class="sxs-lookup"><span data-stu-id="38536-117">Provides access to the buffered graphics context for a application domain.</span></span>
