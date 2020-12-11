---
title: Hinzufügen von Anwendungssymbolen zur Taskleiste mit der NotifyIcon-Komponente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- TrayIcon
helpviewer_keywords:
- status area icons
- icons [Windows Forms], adding to taskbar
- NotifyIcon component
- taskbar [Windows Forms], adding icons
ms.assetid: d28c0fe6-aaf2-4df7-ad74-928d861a8510
ms.openlocfilehash: 46b50ecaabe75dba08fea922d7b5639031692269
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975790"
---
# <a name="how-to-add-application-icons-to-the-taskbar-with-the-windows-forms-notifyicon-component"></a>Vorgehensweise: Hinzufügen von Anwendungssymbolen zur Taskleiste mit der NotifyIcon-Komponente in Windows Forms

Die Windows Forms <xref:System.Windows.Forms.NotifyIcon> Komponente zeigt ein einzelnes Symbol im Status Benachrichtigungsbereich der Taskleiste an. Um mehrere Symbole im Statusbereich anzuzeigen, müssen Sie <xref:System.Windows.Forms.NotifyIcon> über mehrere Komponenten im Formular verfügen. Um das für ein Steuerelement angezeigte Symbol festzulegen, verwenden Sie die- <xref:System.Windows.Forms.NotifyIcon.Icon%2A> Eigenschaft. Sie können auch Code im- <xref:System.Windows.Forms.NotifyIcon.DoubleClick> Ereignishandler schreiben, sodass etwas passiert, wenn der Benutzer auf das Symbol doppelklickt. Beispielsweise können Sie festlegen, dass ein Dialogfeld angezeigt wird, in dem der Benutzer den durch das Symbol dargestellten Hintergrundprozess konfigurieren kann.

> [!NOTE]
> Die <xref:System.Windows.Forms.NotifyIcon> Komponente wird nur zu Benachrichtigungs Zwecken verwendet, um Benutzer darauf aufmerksam zu machen, dass eine Aktion oder ein Ereignis aufgetreten ist oder eine Änderung des Status einer bestimmten Art vorliegt. Sie sollten Menüs, Symbolleisten und andere Elemente der Benutzeroberfläche für die Standard Interaktion mit-Anwendungen verwenden.

### <a name="to-set-the-icon"></a>So legen Sie das Symbol fest

1. Weisen Sie der-Eigenschaft einen Wert zu <xref:System.Windows.Forms.NotifyIcon.Icon%2A> . Der Wert muss vom Typ sein `System.Drawing.Icon` und kann aus einer ICO-Datei geladen werden. Sie können die Symbol Datei im Code oder durch Klicken auf die Schaltfläche mit den Auslassungs Zeichen ( ![ ...) im Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ) neben der <xref:System.Windows.Forms.NotifyIcon.Icon%2A> -Eigenschaft im **Eigenschaften** Fenster angeben und dann die Datei im **geöffneten** Dialogfeld öffnen.

2. Legen Sie die <xref:System.Windows.Forms.NotifyIcon.Visible%2A> -Eigenschaft auf `true`fest.

3. Legen <xref:System.Windows.Forms.NotifyIcon.Text%2A> Sie die Eigenschaft auf eine entsprechende QuickInfo-Zeichenfolge fest.

     Im folgenden Codebeispiel ist der Pfad, der für den Speicherort des Symbols festgelegt wurde, der Ordner " **eigene** Dateien". Dieser Speicherort wird verwendet, da Sie davon ausgehen können, dass die meisten Computer unter dem Windows-Betriebssystem diesen Ordner enthalten. Wenn Sie diesen Speicherort auswählen, können Benutzer mit minimalen System Zugriffsebenen die Anwendung sicher ausführen. Das folgende Beispiel erfordert ein Formular mit einem <xref:System.Windows.Forms.NotifyIcon> bereits hinzugefügten-Steuerelement. Außerdem ist eine Symbol Datei mit dem Namen erforderlich `Icon.ico` .

    ```vb
    ' You should replace the bold icon in the sample below
    ' with an icon of your own choosing.
    NotifyIcon1.Icon = New _
       System.Drawing.Icon(System.Environment.GetFolderPath _
       (System.Environment.SpecialFolder.Personal) _
       & "\Icon.ico")
    NotifyIcon1.Visible = True
    NotifyIcon1.Text = "Antivirus program"
    ```

    ```csharp
    // You should replace the bold icon in the sample below
    // with an icon of your own choosing.
    // Note the escape character used (@) when specifying the path.
    notifyIcon1.Icon =
       new System.Drawing.Icon (System.Environment.GetFolderPath
       (System.Environment.SpecialFolder.Personal)
       + @"\Icon.ico");
    notifyIcon1.Visible = true;
    notifyIcon1.Text = "Antivirus program";
    ```

    ```cpp
    // You should replace the bold icon in the sample below
    // with an icon of your own choosing.
    notifyIcon1->Icon = gcnew
       System::Drawing::Icon(String::Concat
       (System::Environment::GetFolderPath
       (System::Environment::SpecialFolder::Personal),
       "\\Icon.ico"));
    notifyIcon1->Visible = true;
    notifyIcon1->Text = "Antivirus program";
    ```

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.NotifyIcon>
- <xref:System.Windows.Forms.NotifyIcon.Icon%2A>
- [Vorgehensweise: Zuordnen eines Kontextmenüs zu einer NotifyIcon-Komponente in Windows Forms](how-to-associate-a-shortcut-menu-with-a-windows-forms-notifyicon-component.md)
- [NotifyIcon-Komponente](notifyicon-component-windows-forms.md)
- [Übersicht über die NotifyIcon-Komponente](notifyicon-component-overview-windows-forms.md)
