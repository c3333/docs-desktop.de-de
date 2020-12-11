---
title: Durch geänderte Eigenschaften ausgelöste Ereignisse
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], property changes (using code)
- properties [Windows Forms], changes
ms.assetid: 268039ec-5aaa-4d76-b902-acccb036c850
ms.openlocfilehash: 939972713ad95e9302c436268f4a6288a659ca6e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976952"
---
# <a name="property-changed-events"></a>Durch geänderte Eigenschaften ausgelöste Ereignisse

Wenn Sie möchten, dass das Steuerelement Benachrichtigungen sendet, wenn eine Eigenschaft namens *propertyName* geändert wird, definieren Sie ein Ereignis namens *propertyName* `Changed` und eine Methode namens `On` *propertyName* `Changed` , mit der das Ereignis ausgelöst wird. Die Benennungs Konvention in Windows Forms besteht darin, das *geänderte* Wort an den Namen der Eigenschaft anzufügen. Der zugeordnete Ereignisdelegattyp für geänderte Ereignisse der Eigenschaft ist <xref:System.EventHandler> , und der Ereignis Datentyp ist <xref:System.EventArgs> . Die-Basisklasse <xref:System.Windows.Forms.Control> definiert viele Eigenschaften geänderte Ereignisse, wie z <xref:System.Windows.Forms.Control.BackColorChanged> <xref:System.Windows.Forms.Control.BackgroundImageChanged> . b.,, <xref:System.Windows.Forms.Control.FontChanged> , <xref:System.Windows.Forms.Control.LocationChanged> und andere. Hintergrundinformationen zu Ereignissen finden Sie unter [Ereignisse](/dotnet/standard/events/index) und [Ereignisse in Windows Forms](events-in-windows-forms-controls.md)-Steuerelementen.  
  
 Eigenschaften geänderte Ereignisse sind nützlich, da Sie Benutzern eines Steuer Elements das Anfügen von Ereignis Handlern gestatten, die auf die Änderung reagieren. Wenn das Steuerelement auf ein durch die Anwendung geändertes Ereignis reagieren muss, überschreiben Sie die entsprechende `On` *propertyName* - `Changed` Methode, anstatt einen Delegaten an das Ereignis anzufügen. Ein Steuerelement antwortet in der Regel auf ein Ereignis, das durch eine Eigenschaft geändert wurde, indem andere Eigenschaften aktualisiert werden oder ein Teil oder die gesamte Zeichen Oberfläche neu gezeichnet wird.  
  
 Das folgende Beispiel zeigt, wie das `FlashTrackBar` benutzerdefinierte Steuerelement auf einige der durch die Eigenschaften geänderten Ereignisse reagiert, von denen es erbt <xref:System.Windows.Forms.Control> . Das komplette Beispiel finden Sie unter Gewusst [wie: Erstellen eines Windows Forms Steuer Elements, das den Fortschritt anzeigt](how-to-create-a-windows-forms-control-that-shows-progress.md).  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#2)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#2)]  
  
## <a name="see-also"></a>Siehe auch

- [Ereignisse](/dotnet/standard/events/index)
- [Ereignisse in Windows Forms-Steuerelementen](events-in-windows-forms-controls.md)
- [Eigenschaften von Windows Forms-Steuerelementen](properties-in-windows-forms-controls.md)
