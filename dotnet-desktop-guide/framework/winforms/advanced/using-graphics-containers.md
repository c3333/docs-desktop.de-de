---
title: Verwenden von Grafikcontainern
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], using containers
- graphics containers
- examples [Windows Forms], graphics containers
ms.assetid: 74632f91-cefa-4f51-ab7c-f9ac91942caf
ms.openlocfilehash: cfad7254057a31ea8268784cd4b6849850f3e2aa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975224"
---
# <a name="using-graphics-containers"></a><span data-ttu-id="6262b-102">Verwenden von Grafikcontainern</span><span class="sxs-lookup"><span data-stu-id="6262b-102">Using Graphics Containers</span></span>
<span data-ttu-id="6262b-103">Ein <xref:System.Drawing.Graphics> -Objekt stellt Methoden wie <xref:System.Drawing.Graphics.DrawLine%2A> , <xref:System.Drawing.Graphics.DrawImage%2A> und <xref:System.Drawing.Graphics.DrawString%2A> zum Anzeigen von Vektorbildern, Rasterbildern und Text bereit.</span><span class="sxs-lookup"><span data-stu-id="6262b-103">A <xref:System.Drawing.Graphics> object provides methods such as <xref:System.Drawing.Graphics.DrawLine%2A>, <xref:System.Drawing.Graphics.DrawImage%2A>, and <xref:System.Drawing.Graphics.DrawString%2A> for displaying vector images, raster images, and text.</span></span> <span data-ttu-id="6262b-104">Ein- <xref:System.Drawing.Graphics> Objekt verfügt auch über mehrere Eigenschaften, die die Qualität und Ausrichtung der Elemente beeinflussen, die gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="6262b-104">A <xref:System.Drawing.Graphics> object also has several properties that influence the quality and orientation of the items that are drawn.</span></span> <span data-ttu-id="6262b-105">Beispielsweise legt die Eigenschaft Glättungs Modus fest, ob Antialiasing auf Linien und Kurven angewendet wird, und die Welt Transformations Eigenschaft wirkt sich auf die Position und Drehung der Elemente aus, die gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="6262b-105">For example, the smoothing mode property determines whether antialiasing is applied to lines and curves, and the world transformation property influences the position and rotation of the items that are drawn.</span></span>  
  
 <span data-ttu-id="6262b-106">Ein- <xref:System.Drawing.Graphics> Objekt ist einem bestimmten Anzeigegerät zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6262b-106">A <xref:System.Drawing.Graphics> object is associated with a particular display device.</span></span> <span data-ttu-id="6262b-107">Wenn Sie ein- <xref:System.Drawing.Graphics> Objekt verwenden, um in einem-Fenster zu zeichnen, wird das- <xref:System.Drawing.Graphics> Objekt auch diesem speziellen Fenster zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6262b-107">When you use a <xref:System.Drawing.Graphics> object to draw in a window, the <xref:System.Drawing.Graphics> object is also associated with that particular window.</span></span>  
  
 <span data-ttu-id="6262b-108">Ein- <xref:System.Drawing.Graphics> Objekt kann als Container betrachtet werden, da es einen Satz von Eigenschaften enthält, die das Zeichnen beeinflussen und mit gerätespezifischen Informationen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6262b-108">A <xref:System.Drawing.Graphics> object can be thought of as a container because it holds a set of properties that influence drawing and it is linked to device-specific information.</span></span> <span data-ttu-id="6262b-109">Sie können einen sekundären Container innerhalb eines vorhandenen <xref:System.Drawing.Graphics> Objekts erstellen, indem Sie die- <xref:System.Drawing.Graphics.BeginContainer%2A> Methode dieses <xref:System.Drawing.Graphics> Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6262b-109">You can create a secondary container within an existing <xref:System.Drawing.Graphics> object by calling the <xref:System.Drawing.Graphics.BeginContainer%2A> method of that <xref:System.Drawing.Graphics> object.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="6262b-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6262b-110">In This Section</span></span>  
 [<span data-ttu-id="6262b-111">Verwalten des Zustands eines Graphics-Objekts</span><span class="sxs-lookup"><span data-stu-id="6262b-111">Managing the State of a Graphics Object</span></span>](managing-the-state-of-a-graphics-object.md)  
 <span data-ttu-id="6262b-112">Beschreibt, wie die Qualitätseinstellungen, der Clippingbereich und die Transformationen eines-Objekts verwaltet werden <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="6262b-112">Describes how manage the quality settings, clipping area and transformations of a <xref:System.Drawing.Graphics> object.</span></span>  
  
 [<span data-ttu-id="6262b-113">Verwenden geschachtelter Grafikcontainer</span><span class="sxs-lookup"><span data-stu-id="6262b-113">Using Nested Graphics Containers</span></span>](using-nested-graphics-containers.md)  
 <span data-ttu-id="6262b-114">Zeigt, wie Container verwendet werden, um den Status des <xref:System.Drawing.Graphics> Objekts zu steuern.</span><span class="sxs-lookup"><span data-stu-id="6262b-114">Shows how to use containers to control the state of the <xref:System.Drawing.Graphics> object.</span></span>
