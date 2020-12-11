---
title: 'Vorgehensweise: Erben von der Control-Klasse'
ms.date: 03/30/2017
helpviewer_keywords:
- inheritance [Windows Forms], Windows Forms custom controls
- Control class [Windows Forms], inheriting from
- custom controls [Windows Forms], inheritance
- OnPaint method [Windows Forms]
- custom controls [Windows Forms], creating
ms.assetid: 46ba0df3-5cf7-443c-a3b4-a72660172476
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: a00c4deb795800931f5dbf61b545b62acf971ff0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975622"
---
# <a name="how-to-inherit-from-the-control-class"></a>Vorgehensweise: Erben von der Control-Klasse

Wenn Sie ein vollständig benutzerdefiniertes Steuerelement erstellen möchten, das in einem Windows Form verwendet werden soll, sollten Sie von der- <xref:System.Windows.Forms.Control> Klasse erben. Obwohl die Vererbung von der- <xref:System.Windows.Forms.Control> Klasse erfordert, dass Sie mehr Planung und Implementierung durchführen, bietet Sie Ihnen auch die größte Palette von Optionen. Wenn Sie von Erben <xref:System.Windows.Forms.Control> , erben Sie die grundlegende Funktionalität, mit der Steuerelemente funktionieren. Die Funktionalität, die in der <xref:System.Windows.Forms.Control> -Klasse enthalten ist, verarbeitet Benutzereingaben über Tastatur und Maus, definiert die Begrenzungen und die Größe des Steuer Elements, stellt ein Windows-Handle bereit und bietet Nachrichten Behandlung und Sicherheit. Sie enthält keine Zeichnungen, bei denen es sich in diesem Fall um das eigentliche Rendering der grafischen Benutzeroberfläche des Steuerelements handelt, und keine spezifische Funktionalität für Benutzerinteraktion. Sie müssen alle diese Aspekte über benutzerdefinierten Code bereitstellen.

## <a name="to-create-a-custom-control"></a>So erstellen Sie ein benutzerdefiniertes Steuerelement

1. Erstellen Sie in Visual Studio eine neue **Windows-Anwendung** oder ein **Windows-Steuerelement Bibliothek** -Projekt.

2. Wählen Sie im Menü **Projekt** den Eintrag **Klasse hinzufügen** aus.

3. Klicken Sie im Dialogfeld **Neues Element hinzufügen** auf **Benutzerdefiniertes Steuerelement**.

   Ein neues benutzerdefiniertes Steuerelement wird zu Ihrem Projekt hinzugefügt.

4. Drücken Sie **F7** , um den **Code-Editor** für das benutzerdefinierte Steuerelement zu öffnen.

5. Suchen Sie die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode, die mit Ausnahme eines Aufrufes der- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode der-Basisklasse leer ist.

6. Ändern Sie den Code so, dass er die gewünschte benutzerdefinierte Darstellung Ihres Steuerelements enthält.

   Informationen zum Schreiben von Code zum Rendern von Grafiken für Steuerelemente finden Sie unter [Zeichnen und Ausgeben von benutzerdefinierten Steuerelementen](custom-control-painting-and-rendering.md).

7. Implementieren Sie alle benutzerdefinierten Methoden, Eigenschaften oder Ereignisse, die in das Steuerelement eingebunden werden sollen.

8. Speichern und testen Sie das Steuerelement.

## <a name="see-also"></a>Siehe auch

- [Arten von benutzerdefinierten Steuerelementen](varieties-of-custom-controls.md)
- [How to: Erben von der UserControl-Klasse](how-to-inherit-from-the-usercontrol-class.md)
- [Vorgehensweise: Erben von vorhandenen Windows Forms-Steuerelementen](how-to-inherit-from-existing-windows-forms-controls.md)
- [Vorgehensweise: Erstellen von Steuerelementen für Windows Forms](how-to-author-controls-for-windows-forms.md)
- [Problembehandlung für geerbte Ereignishandler in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers)
- [Entwickeln von Windows Forms-Steuerelementen zur Entwurfszeit](developing-windows-forms-controls-at-design-time.md)
