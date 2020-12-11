---
title: Grundlagen zum Entwickeln von Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], derivation types
- programming concepts [Windows Forms], Windows Forms controls
- controls [Windows Forms], creating
ms.assetid: 6277bb81-90f7-4c5b-9f4b-b02bb42dd316
ms.openlocfilehash: fab0a76e2f9fdb7e2f89e9d6a10dd9c522a6d8e1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977141"
---
# <a name="windows-forms-control-development-basics"></a>Grundlagen für das Entwickeln von Windows Forms-Steuerelementen
Ein Windows Forms-Steuerelement ist eine Klasse, die direkt oder indirekt von abgeleitet wird <xref:System.Windows.Forms.Control?displayProperty=nameWithType> . In der folgenden Liste werden gängige Szenarien zum Entwickeln von Windows Forms-Steuerelementen beschrieben:  
  
- Kombinieren vorhandener Steuerelemente zum Erstellen eines zusammengesetzten Steuer Elements.  
  
     Zusammengesetzte Steuerelemente Kapseln eine Benutzeroberfläche, die als Steuerelement wieder verwendet werden kann. Ein Beispiel für ein zusammengesetztes Steuerelement ist ein Steuerelement, das aus einem Textfeld und einer Schaltfläche Zurücksetzen besteht. Visuelle Designer bieten umfassende Unterstützung für das Erstellen von zusammengesetzten Steuerelementen. Zum Erstellen eines zusammengesetzten Steuer Elements leiten Sie von ab <xref:System.Windows.Forms.UserControl?displayProperty=nameWithType> . Die-Basisklasse <xref:System.Windows.Forms.UserControl> stellt Tastatur Routing für untergeordnete Steuerelemente bereit und ermöglicht, dass untergeordnete Steuerelemente als Gruppe funktionieren. Weitere Informationen finden Sie unter [Entwickeln eines zusammengesetzten Windows Forms-Steuerelements](developing-a-composite-windows-forms-control.md).  
  
- Erweitern eines vorhandenen Steuer Elements, um es anzupassen oder seiner Funktionalität hinzuzufügen.  
  
     Eine Schaltfläche, deren Farbe nicht geändert werden kann, und eine Schaltfläche mit einer zusätzlichen Eigenschaft, die nachverfolgt, wie oft auf Sie geklickt wurde, sind Beispiele für erweiterte Steuerelemente. Sie können jedes Windows Forms Steuerelement anpassen, indem Sie es ableiten und Eigenschaften, Methoden und Ereignisse überschreiben oder hinzufügen.  
  
- Erstellen eines Steuer Elements, das vorhandene Steuerelemente weder kombiniert noch erweitert.  
  
     Leiten Sie in diesem Szenario das Steuerelement von der-Basisklasse ab <xref:System.Windows.Forms.Control> . Sie können Eigenschaften, Methoden und Ereignisse der Basisklasse hinzufügen und überschreiben. Informationen zu den ersten Schritten finden Sie unter Gewusst [wie: Entwickeln eines einfachen Windows Forms Steuer](how-to-develop-a-simple-windows-forms-control.md)Elements.  
  
 Die Basisklasse für Windows Forms Steuerelemente, <xref:System.Windows.Forms.Control> , stellt die erforderliche Komponente für die visuelle Darstellung in Client seitigen Windows-basierten Anwendungen bereit. <xref:System.Windows.Forms.Control> stellt ein Fenster Handle bereit, verarbeitet das Nachrichten Routing und bietet Maus-und Tastatur Ereignisse sowie viele weitere Ereignisse der Benutzeroberfläche. Sie bietet erweiterte Layouts und verfügt über Eigenschaften, die für die visuelle Anzeige spezifisch sind, z <xref:System.Windows.Forms.Control.ForeColor%2A> <xref:System.Windows.Forms.Control.BackColor%2A> . b.,, <xref:System.Windows.Forms.Control.Height%2A> , <xref:System.Windows.Forms.Control.Width%2A> und viele andere. Außerdem bietet Sie Sicherheit, Threading Unterstützung und Interoperabilität mit ActiveX-Steuerelementen. Da der Großteil der Infrastruktur von der Basisklasse bereitgestellt wird, ist es relativ einfach, Ihre eigenen Windows Forms-Steuerelemente zu entwickeln.  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Entwickeln eines einfachen Windows Forms-Steuerelements](how-to-develop-a-simple-windows-forms-control.md)
- [Entwickeln eines zusammengesetzten Windows Forms-Steuerelements](developing-a-composite-windows-forms-control.md)
- [Vorgehensweise: Erstellen eines Windows Forms-Steuerelements, das den Fortschritt anzeigt](how-to-create-a-windows-forms-control-that-shows-progress.md)
- [Arten von benutzerdefinierten Steuerelementen](varieties-of-custom-controls.md)
