---
title: Hinzufügen von Steuerelementen ohne Benutzeroberfläche
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- NonVisualSelection
helpviewer_keywords:
- invisible controls [Windows Forms]
- Windows Forms controls, adding to form
- controls [Windows Forms], nonvisual
- Windows Forms controls, nonvisual
- nonvisual controls [Windows Forms]
ms.assetid: 52134d9c-cff6-4eed-8e2b-3d5eb3bd494e
ms.openlocfilehash: c1ab1ec848b4c7a19ed9a65b67e17679bac215cd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976251"
---
# <a name="how-to-add-controls-without-a-user-interface-to-windows-forms"></a>Gewusst wie: Hinzufügen von Steuerelementen ohne Benutzeroberfläche zu Windows Forms

Ein nicht visuelles Steuerelement (oder eine Komponente) stellt Funktionen für Ihre Anwendung bereit. Im Gegensatz zu anderen Steuerelementen bieten Komponenten keine Benutzeroberfläche für den Benutzer und müssen daher nicht auf der Windows Forms-Designer Oberfläche angezeigt werden. Wenn eine Komponente zu einem Formular hinzugefügt wird, zeigt der Windows Forms-Designer am unteren Rand des Formulars, in dem alle Komponenten angezeigt werden, eine Größe an, die geändert werden kann. Nachdem ein Steuerelement der Komponenten Leiste hinzugefügt wurde, können Sie die Komponente auswählen und deren Eigenschaften wie jedes andere Steuerelement im Formular festlegen.

## <a name="add-a-component-to-a-windows-form"></a>Hinzufügen einer Komponente zu einem Windows Form

1. Öffnen Sie das Formular in Visual Studio. Weitere Informationen finden Sie unter Gewusst [wie: Anzeigen von Windows Forms im Designer](/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).

2. Klicken Sie in der **Toolbox** auf eine Komponente, und ziehen Sie Sie in das Formular.

     Die Komponente wird in der Komponenten Leiste angezeigt.

Darüber hinaus können Komponenten zur Laufzeit einem Formular hinzugefügt werden. Dies ist ein häufiges Szenario, insbesondere, da Komponenten keinen visuellen Ausdruck aufweisen, anders als Steuerelemente mit einer Benutzeroberfläche. Im folgenden Beispiel <xref:System.Windows.Forms.Timer> wird eine Komponente zur Laufzeit hinzugefügt. (Beachten Sie, dass Visual Studio eine Reihe von unterschiedlichen Timern enthält. verwenden Sie in diesem Fall eine Windows Forms <xref:System.Windows.Forms.Timer> Komponente. Weitere Informationen zu den verschiedenen Timern in Visual Studio finden [Sie unter Einführung in Server-Based Timer](/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).)

> [!CAUTION]
> Komponenten verfügen häufig über Steuerungs spezifische Eigenschaften, die für eine effektive Funktionsweise der Komponente festgelegt werden müssen. Im Fall der nachfolgenden <xref:System.Windows.Forms.Timer> Komponente legen Sie die- `Interval` Eigenschaft fest. Stellen Sie sicher, dass Sie beim Hinzufügen von Komponenten zu Ihrem Projekt die Eigenschaften festlegen, die für diese Komponente erforderlich sind.

## <a name="add-a-component-to-a-windows-form-programmatically"></a>Programm gesteuertes Hinzufügen einer Komponente zu einem Windows Form

1. Erstellen Sie im Code eine Instanz der- <xref:System.Windows.Forms.Timer> Klasse.

2. Legen Sie die- `Interval` Eigenschaft fest, um die Zeit zwischen Ticks des Timers zu bestimmen.

3. Konfigurieren Sie alle anderen erforderlichen Eigenschaften für die Komponente.

     Der folgende Code zeigt die Erstellung eines- <xref:System.Windows.Forms.Timer> Objekts, dessen- `Interval` Eigenschaft auf festgelegt ist.

    ```vb
    Public Sub CreateTimer()
       Dim timerKeepTrack As New System.Windows.Forms.Timer
       timerKeepTrack.Interval = 1000
    End Sub
    ```

    ```csharp
    public void createTimer()
    {
       System.Windows.Forms.Timer timerKeepTrack = new
           System.Windows.Forms.Timer();
       timerKeepTrack.Interval = 1000;
    }
    ```

    ```cpp
    public:
       void createTimer()
       {
          System::Windows::Forms::Timer^ timerKeepTrack = gcnew
             System::Windows::Forms::Timer();
          timerKeepTrack->Interval = 1000;
       }
    ```

    > [!IMPORTANT]
    > Sie können den lokalen Computer mit einem Sicherheitsrisiko über das Netzwerk verfügbar machen, indem Sie auf ein schädliches UserControl-Steuerelement verweisen. Dies wäre nur ein Problem, wenn eine böswillige Person ein schädliches benutzerdefiniertes Steuerelement erstellt, gefolgt von dem, das Sie versehentlich dem Projekt hinzufügen.

## <a name="see-also"></a>Siehe auch

- [Windows Forms Steuerelemente](index.md)
- [How to: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md)
- [Gewusst wie: Hinzufügen von ActiveX-Steuerelementen zu Windows Forms](how-to-add-activex-controls-to-windows-forms.md)
- [Einfügen von Steuerelementen in Windows Forms](putting-controls-on-windows-forms.md)
- [Beschriften einzelner Steuerelemente für Windows Forms und Konfigurieren von Shortcuts für diese Elemente](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Steuerelemente für Windows Forms](controls-to-use-on-windows-forms.md)
- [Windows Forms-Steuerelemente nach Funktion](windows-forms-controls-by-function.md)
