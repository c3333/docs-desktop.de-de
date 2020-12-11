---
title: 'Vorgehensweise: Testen des Laufzeitverhaltens eines UserControl'
ms.date: 03/30/2017
helpviewer_keywords:
- UserControl class [Windows Forms], testing
- user controls [Windows Forms], testing
- composite controls [Windows Forms], testing
- UserControl Test Container
- UserControl class [Windows Forms], run-time behavior
ms.assetid: 4e4d5c49-1346-40ac-9d96-40211b573583
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: c619900ea0b7f1b50976fec8d26dd3145dc07693
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976743"
---
# <a name="how-to-test-the-run-time-behavior-of-a-usercontrol"></a>Gewusst wie: Testen des Lauf Zeit Verhaltens eines UserControl-Steuer Elements

Beim Entwickeln eines <xref:System.Windows.Forms.UserControl> muss das Laufzeitverhalten getestet werden. Sie können ein separates Windows-basiertes Anwendungsprojekt erstellen und das Steuerelement in einem Testformular platzieren, aber dieses Verfahren ist nicht praktisch. Ein schnelleres und einfacheres Verfahren besteht darin, den von Visual Studio bereitgestellten **UserControl-Test Container** zu verwenden. Dieser Test Container startet direkt aus dem Windows-Steuerelement Bibliothek-Projekt.

> [!IMPORTANT]
> Damit der Test Container das Laden <xref:System.Windows.Forms.UserControl> kann, muss das Steuerelement über mindestens einen öffentlichen Konstruktor verfügen.
> [!NOTE]
> Ein Visual C++-Steuerelement kann nicht mit dem **UserControl-Test Container** getestet werden.

## <a name="test-the-run-time-behavior-of-a-usercontrol"></a>Testen des Lauf Zeit Verhaltens eines UserControl-Steuer Elements

1. Erstellen Sie in Visual Studio ein Windows-Steuerelement Bibliothek-Projekt, und nennen Sie es **TestContainerExample**.

2. Ziehen Sie in der **Windows Forms-Designer** ein- <xref:System.Windows.Forms.Label> Steuerelement aus der **Toolbox** auf die Entwurfs Oberfläche des Steuer Elements.

3. Drücken Sie <kbd>F5</kbd> , um das Projekt zu erstellen und den **UserControl-Test Container** auszuführen. Der Test Container wird mit Ihrem <xref:System.Windows.Forms.UserControl> im **Vorschau** Bereich angezeigt.

4. Wählen Sie die <xref:System.Windows.Forms.Control.BackColor%2A> Eigenschaft aus, die im Steuerelement <xref:System.Windows.Forms.PropertyGrid> rechts neben dem **Vorschaufenster** angezeigt wird. Ändern Sie den Wert in **ControlDark**. Beachten Sie, dass sich das Steuerelement in eine dunklere Farbe ändert. Ändern Sie andere Eigenschaftswerte, und beobachten Sie die Auswirkung auf das Steuerelement.

5. Aktivieren Sie das Kontrollkästchen **Benutzer Steuerelement andocken** unter dem **Vorschau** Bereich. Beachten Sie, dass die Größe des Steuer Elements geändert wird, um den Bereich auszufüllen. Ändern Sie die Größe des Test Containers, und beobachten Sie, dass die Größe des Steuer Elements mit dem Bereich angepasst wird.

6. Schließen Sie den Test Container.

7. Fügen Sie dem Projekt **TestContainerExample** ein weiteres Benutzer Steuerelement hinzu.

8. Ziehen Sie in der **Windows Forms-Designer** ein- <xref:System.Windows.Forms.Button> Steuerelement aus der **Toolbox** auf die Entwurfs Oberfläche des Steuer Elements.

9. Drücken Sie <kbd>F5</kbd> , um das Projekt zu erstellen und den Test Container auszuführen.

10. Klicken Sie auf das **Benutzer Steuerelement auswählen** <xref:System.Windows.Forms.ComboBox> , um zwischen den beiden Benutzer Steuerelementen zu wechseln.

## <a name="test-user-controls-from-another-project"></a>Testen von Benutzer Steuerelementen aus einem anderen Projekt

Sie können Benutzer Steuerelemente aus anderen Projekten im Test Container Ihres aktuellen Projekts testen.

1. Erstellen Sie in Visual Studio ein Windows-Steuerelement Bibliothek-Projekt, und nennen Sie es **TestContainerExample2**.

2. Ziehen Sie in der **Windows Forms-Designer** ein- <xref:System.Windows.Forms.RadioButton> Steuerelement aus der **Toolbox** auf die Entwurfs Oberfläche des Steuer Elements.

3. Drücken Sie <kbd>F5</kbd> , um das Projekt zu erstellen und den Test Container auszuführen. Der Test Container wird mit Ihrem <xref:System.Windows.Forms.UserControl> im **Vorschau** Bereich angezeigt.

4. Klicken Sie auf die Schaltfläche **Laden** .

5. Navigieren Sie im Dialogfeld **Öffnen** zu *TestContainerExample.dll*, das Sie im vorherigen Verfahren erstellt haben. Wählen Sie *TestContainerExample.dll* aus, und klicken Sie auf **Öffnen** , um die Benutzer Steuerelemente zu laden.

6. Verwenden **Sie das Benutzer Steuerelement auswählen** <xref:System.Windows.Forms.ComboBox> , um zwischen den beiden Benutzer Steuerelementen aus dem Projekt **TestContainerExample** zu wechseln.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.UserControl>
- [Vorgehensweise: Erstellen von zusammengesetzten Steuerelementen](how-to-author-composite-controls.md)
- [Exemplarische Vorgehensweise: Erstellen eines zusammengesetzten Steuer Elements](walkthrough-authoring-a-composite-control-with-visual-csharp.md)
- [Benutzersteuerelement-Designer](/previous-versions/visualstudio/visual-studio-2010/183c3hth(v=vs.100))
