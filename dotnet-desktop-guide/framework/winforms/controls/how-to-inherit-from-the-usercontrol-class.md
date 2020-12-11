---
title: 'Vorgehensweise: Erben von der UserControl-Klasse'
ms.date: 03/30/2017
helpviewer_keywords:
- inheritance [Windows Forms], Windows Forms custom controls
- UserControl class [Windows Forms], inheriting from
- user controls [Windows Forms], creating
- composite controls [Windows Forms], creating
ms.assetid: 67713625-e2e4-4f6a-bce7-0855ee5043d9
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 5c278cfadd1bb0c9720718c08791a37f90d964d7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976617"
---
# <a name="how-to-inherit-from-the-usercontrol-class"></a>Vorgehensweise: Erben von der UserControl-Klasse

Sie können ein *Benutzersteuerelement* erstellen, um die Funktionalität einer oder mehrerer Windows Forms-Steuerelemente mit benutzerdefiniertem Code zu kombinieren. Benutzersteuerelemente kombinieren die schnelle Entwicklung von Steuerelementen, die standardmäßige Funktionalität von Windows Forms-Steuerelementen und die Vielseitigkeit von benutzerdefinierten Eigenschaften und Methoden. Wenn Sie mit dem Erstellen eines Benutzersteuerelements beginnen, wird ein Designer angezeigt, auf dem Sie die standardmäßigen Windows Forms-Steuerelemente platzieren können. Diese Steuerelemente behalten ihre implementierte Funktionalität sowie das Aussehen und Verhalten der Standardsteuerelemente. Sobald diese Steuerelemente in das Benutzersteuerelement integriert sind, stehen sie jedoch nicht mehr über Code zur Verfügung. Das Benutzersteuerelement führt seine eigene Grafikausgabe aus und behandelt auch die gesamte grundlegende Funktionalität von Steuerelementen.

## <a name="to-create-a-user-control"></a>So erstellen Sie ein benutzerdefiniertes Steuerelement

1. Erstellen Sie in Visual Studio ein neues **Windows-Steuerelement Bibliothek** -Projekt.

   Ein neues Projekt mit einem leeren Benutzersteuerelement wird erstellt.

2. Ziehen Sie Steuerelemente von der Registerkarte **Windows Forms** der **Toolbox** auf den Designer.

3. Diese Steuerelemente sollten so positioniert und entworfen werden, wie Sie im fertig gestellten Steuerelement angezeigt werden sollen. Wenn Sie möchten, dass Entwickler auf die konstituierenden Steuerelemente zugreifen können, müssen Sie diese als öffentlich deklarieren oder Eigenschaften des konstituierenden Steuerelements einzeln verfügbar machen. Einzelheiten finden Sie unter [Vorgehensweise: Verfügbarmachen der Eigenschaften konstituierender Steuerelemente](how-to-expose-properties-of-constituent-controls.md).

4. Implementieren Sie alle benutzerdefinierten Methoden oder Eigenschaften, die in das Steuerelement eingebunden werden sollen.

5. Drücken Sie **F5** , um das Projekt zu erstellen, und führen Sie das Steuerelement im **UserControl-Test Container** aus. Weitere Informationen finden Sie unter Gewusst [wie: Testen des Run-Time Verhaltens eines UserControl-Steuer](how-to-test-the-run-time-behavior-of-a-usercontrol.md)Elements.

## <a name="see-also"></a>Siehe auch

- [Arten von benutzerdefinierten Steuerelementen](varieties-of-custom-controls.md)
- [Vorgehensweise: Erben von der Control-Klasse](how-to-inherit-from-the-control-class.md)
- [Vorgehensweise: Erben von vorhandenen Windows Forms-Steuerelementen](how-to-inherit-from-existing-windows-forms-controls.md)
- [Vorgehensweise: Erstellen von Steuerelementen für Windows Forms](how-to-author-controls-for-windows-forms.md)
- [Problembehandlung bei vererbten Ereignis Handlern in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers)
- [Vorgehensweise: Testen des Laufzeitverhaltens eines UserControl](how-to-test-the-run-time-behavior-of-a-usercontrol.md)
