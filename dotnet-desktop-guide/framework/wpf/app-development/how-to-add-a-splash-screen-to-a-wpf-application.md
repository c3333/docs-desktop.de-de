---
title: Vorgehensweise beim Hinzufügen eines Begrüßungs Bildschirms
description: Erfahren Sie, wie Sie einer Windows Presentation Foundation (WPF)-Anwendung ein Startfenster oder einen Begrüßungsbildschirm hinzufügen.
ms.date: 08/18/2018
helpviewer_keywords:
- WPF [WPF], splash screen
- startup window [WPF]
- SplashScreen class [WPF]
- splash screen [WPF]
ms.assetid: d70a25c4-5fb9-4c27-b01d-b1b8ef39b3fd
ms.openlocfilehash: 99a20dca755b7fd066ed6068ed2efa4cca8acaa9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977129"
---
# <a name="how-to-add-a-splash-screen-to-a-wpf-application"></a>Gewusst wie: Hinzufügen eines Begrüßungsbildschirms zu einer WPF-Anwendung

In diesem Thema wird gezeigt, wie Sie einer Windows Presentation Foundation (WPF)-Anwendung ein Startfenster oder einen Begrüßungs *Bildschirm* hinzufügen.

## <a name="to-add-an-existing-image-as-a-splash-screen"></a>So fügen Sie ein vorhandenes Bild als Begrüßungsbildschirm hinzu

1. Erstellen oder suchen Sie ein Bild, das Sie für den Begrüßungsbildschirm verwenden möchten. Sie können jedes beliebige Bildformat verwenden, das von der Windows Imaging Component (WIC) unterstützt wird. Beispielsweise können Sie das Format BMP, GIF, JPEG, PNG oder TIFF verwenden.

2. Fügen Sie die Bilddatei zum WPF-Anwendungsprojekt hinzu.

3. Wählen Sie in **Projektmappen-Explorer** das Abbild aus.

4. Klicken Sie im Eigenschaftenfenster auf den Dropdown Pfeil für die Eigenschaft **Buildaktion** .

5. Wählen Sie in der Dropdown Liste die Option **SplashScreen** aus.

6. Drücken Sie **F5**, um die Anwendung zu erstellen und auszuführen.

     Das Bild mit dem Begrüßungsbildschirm wird in der Mitte des Bildschirms angezeigt und wird dann ausgeblendet, wenn das Hauptanwendungsfenster angezeigt wird.

## <a name="to-exclude-the-splash-screen-from-build"></a>So schließen Sie den Begrüßungsbildschirm vom Build aus

1. Wählen Sie in **Projektmappen-Explorer** das Bild mit dem Begrüßungsbildschirm aus.

2. Legen Sie im Fenster **Eigenschaften** die **Buildaktion** auf **None** fest.

## <a name="to-remove-the-splash-screen-from-an-application"></a>So entfernen Sie den Begrüßungsbildschirm aus einer Anwendung

Löschen Sie in **Projektmappen-Explorer** das Bild des Begrüßungs Bildschirms.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.SplashScreen>
- [Vorgehensweise: Hinzufügen vorhandener Elemente zu einem Projekt](/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))
