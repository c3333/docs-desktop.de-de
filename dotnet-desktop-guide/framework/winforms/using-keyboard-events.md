---
title: Verwenden von Tastaturereignissen
ms.date: 03/30/2017
helpviewer_keywords:
- KeyPress event [Windows Forms]
- keyboards [Windows Forms], keyboard events
- KeyUp event
- KeyDown event
- keyboard events
- events [Windows Forms], keyboard
ms.assetid: d3f3e14b-a459-4ee6-9875-8957e34f8ee9
ms.openlocfilehash: dc404a73d5de96c69e4241b818965fe2bef22a50
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974711"
---
# <a name="using-keyboard-events"></a>Verwenden von Tastaturereignissen
Die meisten Windows Forms-Programme verarbeiten Tastatureingaben, indem sie Tastaturereignisse behandeln. Dieses Thema enthält eine Übersicht über die Tastaturereignisse, einschließlich Details dazu, wann jedes Ereignis verwendet wird sowie zu den Daten, die für jedes Ereignis übergeben werden.  Weitere Informationen finden Sie auch unter [Übersicht über Ereignishandler (Windows Forms)](event-handlers-overview-windows-forms.md) und [Übersicht über Ereignisse (Windows Forms)](events-overview-windows-forms.md).  
  
## <a name="keyboard-events"></a>Tastaturereignisse  
 Windows Forms stellen zwei Ereignisse bereit, die auftreten, wenn ein Benutzer eine Taste auf der Tastatur drückt, und ein Ereignis, wenn der Benutzer die Taste loslässt:  
  
- Das <xref:System.Windows.Forms.Control.KeyDown>-Ereignis tritt einmal auf.  
  
- Das <xref:System.Windows.Forms.Control.KeyPress>-Ereignis, das mehrfach auftreten kann, wenn der Benutzer die gleiche Taste gedrückt hält.  
  
- Das <xref:System.Windows.Forms.Control.KeyUp>-Ereignis tritt einmal auf, wenn der Benutzer eine Taste loslässt.  
  
 Wenn der Benutzer eine Taste drückt, ermittelt Windows Forms , welches Ereignis ausgelöst werden soll, und zwar basierend darauf, ob die Tastatureingabe eine Zeichentaste oder eine Steuer- bzw. Funktionstaste ist. Weitere Informationen zu Zeichen und physischen Schlüsseln finden Sie unter [Funktionsweise von Tastatureingaben](how-keyboard-input-works.md).  
  
 In der folgenden Tabelle werden diese drei Tastaturereignisse beschrieben.  
  
|Tastaturereignis|BESCHREIBUNG|Ergebnisse|  
|--------------------|-----------------|-------------|  
|<xref:System.Windows.Forms.Control.KeyDown>|Dieses Ereignis wird ausgelöst, wenn der Benutzer eine Steuer- bzw. Funktionstaste drückt.|Der Handler für <xref:System.Windows.Forms.Control.KeyDown> erhält Folgendes:<br /><br /> <ul><li>Einen <xref:System.Windows.Forms.KeyEventArgs>-Parameter, der die <xref:System.Windows.Forms.KeyEventArgs.KeyCode%2A>-Eigenschaft bereitstellt (womit eine Steuer- oder Funktionstaste angegeben wird).</li><li>Die <xref:System.Windows.Forms.KeyEventArgs.Modifiers%2A>-Eigenschaft (UMSCHALT, STRG oder ALT).</li><li>Die <xref:System.Windows.Forms.KeyEventArgs.KeyData%2A>-Eigenschaft (wodurch der Tastencode und der Modifizierer kombiniert werden). Der <xref:System.Windows.Forms.KeyEventArgs>-Parameter stellt zudem Folgendes bereit:<br /><br /> <ul><li>Die <xref:System.Windows.Forms.KeyEventArgs.Handled%2A>-Eigenschaft, die festgelegt werden kann, um zu verhindert, dass das zugrunde liegende Steuerelement auf den Tastendruck reagiert.</li><li>Die <xref:System.Windows.Forms.KeyEventArgs.SuppressKeyPress%2A>-Eigenschaft, die verwendet werden kann, um <xref:System.Windows.Forms.Control.KeyPress>- und <xref:System.Windows.Forms.Control.KeyUp>-Eigenschaften für diesen Tastendruck zu unterdrücken.</li></ul></li></ul>|  
|<xref:System.Windows.Forms.Control.KeyPress>|Dieses Ereignis wird ausgelöst, wenn der oder die Tastendrücke ein Zeichen bewirken. Wenn der Benutzer beispielsweise die Tasten UMSCHALT und kleines "a" drückt, wird das Zeichen "A" in Großbuchstaben angezeigt.|<xref:System.Windows.Forms.Control.KeyPress> wird nach <xref:System.Windows.Forms.Control.KeyDown> ausgelöst.<br /><br /> <ul><li>Der Handler für <xref:System.Windows.Forms.Control.KeyPress> erhält Folgendes:</li><li>Einen <xref:System.Windows.Forms.KeyPressEventArgs>-Parameter, der den Zeichencode der gedrückten Taste enthält. Dieser Zeichencode ist für jede Kombination aus Zeichentaste und Modifizierertaste eindeutig.<br /><br />     So generiert die Taste "A" beispielsweise:<br /><br /> <ul><li>Den Zeichencode 65 in Verbindung mit der UMSCHALT-TASTE, oder</li><li>97 in Verbindung mit der FESTSTELLTASTE, wenn diese allein gedrückt wird,</li><li>und 1, wenn sie zusammen mit der STRG-TASTE gedrückt wird.</li></ul></li></ul>|  
|<xref:System.Windows.Forms.Control.KeyUp>|Dieses Ereignis wird ausgelöst, wenn der Benutzer eine Steuer- bzw. Funktionstaste loslässt.|Der Handler für <xref:System.Windows.Forms.Control.KeyUp> erhält Folgendes:<br /><br /> <ul><li>Einen <xref:System.Windows.Forms.KeyEventArgs>-Parameter.<br /><br /> <ul><li>Dieser stellt die <xref:System.Windows.Forms.KeyEventArgs.KeyCode%2A>-Eigenschaft bereit (womit eine Steuer- oder Funktionstaste angegeben wird).</li><li>Die <xref:System.Windows.Forms.KeyEventArgs.Modifiers%2A>-Eigenschaft (UMSCHALT, STRG oder ALT).</li><li>Die <xref:System.Globalization.SortKey.KeyData%2A>-Eigenschaft (wodurch der Tastencode und der Modifizierer kombiniert werden).</li></ul></li></ul>|  
  
## <a name="see-also"></a>Siehe auch

- [Tastatureingaben in einer Windows Forms-Anwendung](keyboard-input-in-a-windows-forms-application.md)
- [Funktionsweise von Tastatureingaben](how-keyboard-input-works.md)
- [Mauseingabe in einer Windows Forms-Anwendung](mouse-input-in-a-windows-forms-application.md)
