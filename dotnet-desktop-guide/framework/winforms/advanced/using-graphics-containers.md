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
# <a name="using-graphics-containers"></a>Verwenden von Grafikcontainern
Ein <xref:System.Drawing.Graphics> -Objekt stellt Methoden wie <xref:System.Drawing.Graphics.DrawLine%2A> , <xref:System.Drawing.Graphics.DrawImage%2A> und <xref:System.Drawing.Graphics.DrawString%2A> zum Anzeigen von Vektorbildern, Rasterbildern und Text bereit. Ein- <xref:System.Drawing.Graphics> Objekt verfügt auch über mehrere Eigenschaften, die die Qualität und Ausrichtung der Elemente beeinflussen, die gezeichnet werden. Beispielsweise legt die Eigenschaft Glättungs Modus fest, ob Antialiasing auf Linien und Kurven angewendet wird, und die Welt Transformations Eigenschaft wirkt sich auf die Position und Drehung der Elemente aus, die gezeichnet werden.  
  
 Ein- <xref:System.Drawing.Graphics> Objekt ist einem bestimmten Anzeigegerät zugeordnet. Wenn Sie ein- <xref:System.Drawing.Graphics> Objekt verwenden, um in einem-Fenster zu zeichnen, wird das- <xref:System.Drawing.Graphics> Objekt auch diesem speziellen Fenster zugeordnet.  
  
 Ein- <xref:System.Drawing.Graphics> Objekt kann als Container betrachtet werden, da es einen Satz von Eigenschaften enthält, die das Zeichnen beeinflussen und mit gerätespezifischen Informationen verknüpft sind. Sie können einen sekundären Container innerhalb eines vorhandenen <xref:System.Drawing.Graphics> Objekts erstellen, indem Sie die- <xref:System.Drawing.Graphics.BeginContainer%2A> Methode dieses <xref:System.Drawing.Graphics> Objekts aufrufen.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Verwalten des Zustands eines Graphics-Objekts](managing-the-state-of-a-graphics-object.md)  
 Beschreibt, wie die Qualitätseinstellungen, der Clippingbereich und die Transformationen eines-Objekts verwaltet werden <xref:System.Drawing.Graphics> .  
  
 [Verwenden geschachtelter Grafikcontainer](using-nested-graphics-containers.md)  
 Zeigt, wie Container verwendet werden, um den Status des <xref:System.Drawing.Graphics> Objekts zu steuern.
