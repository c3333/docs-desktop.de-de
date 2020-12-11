---
title: Mauszeiger
ms.date: 03/30/2017
helpviewer_keywords:
- pointers [Windows Forms], setting
- mouse pointers
- mouse cursors
- mouse pointers [Windows Forms], setting
- cursors [Windows Forms], setting
- mouse [Windows Forms], cursors
ms.assetid: c3400d85-de5b-42e8-abc3-d6088d69ee53
ms.openlocfilehash: 4e8349effcd9b59045e39b763b4cb8b7d2fceb91
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976948"
---
# <a name="mouse-pointers-in-windows-forms"></a>Mauszeiger in Windows Forms
Der Maus *Zeiger*, der manchmal auch als Cursor bezeichnet wird, ist eine Bitmap, die für Benutzereingaben mit der Maus einen Fokuspunkt auf dem Bildschirm angibt. Dieses Thema enthält eine Übersicht über den Mauszeiger in Windows Forms und beschreibt einige Möglichkeiten zum Ändern und Steuern des Mauszeigers.  
  
## <a name="accessing-the-mouse-pointer"></a>Zugreifen auf den Mauszeiger  
 Der Mauszeiger wird durch die <xref:System.Windows.Forms.Cursor> -Klasse dargestellt, und jede <xref:System.Windows.Forms.Control> verfügt über eine- <xref:System.Windows.Forms.Control.Cursor%2A?displayProperty=nameWithType> Eigenschaft, die den Zeiger für dieses Steuerelement angibt. Die <xref:System.Windows.Forms.Cursor> -Klasse enthält Eigenschaften, die den-Zeiger beschreiben, z. b. die-Eigenschaft und die-Eigenschaft sowie Methoden, die <xref:System.Windows.Forms.Cursor.Position%2A> <xref:System.Windows.Forms.Cursor.HotSpot%2A> die Darstellung des Zeigers ändern können, wie z <xref:System.Windows.Forms.Cursor.Show%2A> . b. die <xref:System.Windows.Forms.Cursor.Hide%2A> Methoden, und <xref:System.Windows.Forms.Cursor.DrawStretched%2A> .  
  
## <a name="controlling-the-mouse-pointer"></a>Steuern des Mauszeigers  
 Manchmal möchten Sie möglicherweise den Bereich einschränken, in dem der Mauszeiger verwendet werden kann, oder die Position der Maus ändern. Sie können die aktuelle Position der Maus mit der-Eigenschaft des-Objekts oder des festlegen <xref:System.Windows.Forms.Cursor.Position%2A> <xref:System.Windows.Forms.Cursor> . Außerdem können Sie den Bereich einschränken, in dem der Mauszeiger zum Festlegen der-Eigenschaft verwendet werden kann <xref:System.Windows.Forms.Cursor.Clip%2A> . Standardmäßig ist der Clip-Bereich der gesamte Bildschirm.  
  
## <a name="changing-the-mouse-pointer"></a>Ändern des Mauszeigers  
 Das Ändern des Mauszeigers ist eine wichtige Möglichkeit zum Bereitstellen von Feedback für den Benutzer. Beispielsweise kann der Mauszeiger in den Handlern des-Ereignisses und des-Ereignisses geändert werden, <xref:System.Windows.Forms.Control.MouseEnter> <xref:System.Windows.Forms.Control.MouseLeave> um dem Benutzer mitzuteilen, dass Berechnungen durchlaufen werden, und die Benutzerinteraktion im-Steuerelement einzuschränken. Manchmal ändert sich der Mauszeiger aufgrund von System Ereignissen, z. b. wenn die Anwendung an einem Drag & Drop-Vorgang beteiligt ist.  
  
 Die primäre Methode zum Ändern des Mauszeigers besteht darin, die- <xref:System.Windows.Forms.Control.Cursor%2A?displayProperty=nameWithType> Eigenschaft oder die- <xref:System.Windows.Forms.Control.DefaultCursor%2A> Eigenschaft eines-Steuer Elements auf einen neuen festzulegen <xref:System.Windows.Forms.Cursor> . Beispiele zum Ändern des Mauszeigers finden Sie im Codebeispiel in der- <xref:System.Windows.Forms.Cursor> Klasse. Außerdem macht die- <xref:System.Windows.Forms.Cursors> Klasse eine Reihe von- <xref:System.Windows.Forms.Cursor> Objekten für viele verschiedene Zeiger Typen verfügbar, z. b. einen Zeiger, der einer Hand ähnelt. Um den Wait-Zeiger anzuzeigen, der einem Sanduhr ähnelt, wenn sich der Mauszeiger auf dem Steuerelement befindet, verwenden Sie die- <xref:System.Windows.Forms.Control.UseWaitCursor%2A> Eigenschaft der- <xref:System.Windows.Forms.Control> Klasse.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Cursor>
- [Mauseingabe in einer Windows Forms-Anwendung](mouse-input-in-a-windows-forms-application.md)
- [Drag &amp;amp; Drop-Funktionen in Windows Forms](drag-and-drop-functionality-in-windows-forms.md)
