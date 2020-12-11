---
title: 'Vorgehensweise: Kopieren und Einfügen eines ElementHost-Steuerelements zur Entwurfszeit'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, content copying and pasting
- interoperability [WPF]
- ElementHost control [Windows Forms], copying and pasting at design time
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: e570375d-2a68-44ba-b4f7-c781af2d20e8
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: bde599dd8f2f592e9cd361c37572da240f710e2f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972376"
---
# <a name="how-to-copy-and-paste-an-elementhost-control"></a>Gewusst wie: Kopieren und Einfügen eines Element Host-Steuer Elements

In diesem Verfahren wird gezeigt, wie ein Windows Presentation Foundation (WPF)-Steuerelement in ein Windows Form in Visual Studio kopiert wird.

1. Fügen Sie in Visual Studio ein neues WPF <xref:System.Windows.Controls.UserControl> zu einem Windows Forms Projekt hinzu. Verwenden Sie den Standardnamen, `UserControl1.xaml`, für den Steuerelementtyp. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Erstellen eines neuen WPF-Inhalts auf Windows Forms zur Entwurfszeit](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).

2. Legen Sie im Fenster **Eigenschaften** den Wert der-Eigenschaft <xref:System.Windows.FrameworkElement.Width%2A> und <xref:System.Windows.FrameworkElement.Height%2A> der-Eigenschaft von `UserControl1` auf **200** fest.

3. Legen Sie den Wert der- <xref:System.Windows.Controls.Control.Background%2A> Eigenschaft auf **Blue** fest.

4. Erstellen Sie das Projekt.

5. Öffnen Sie `Form1` im Windows Forms-Designer.

6. Ziehen Sie aus der **Toolbox** eine Instanz von `UserControl1` auf das Formular.

   Eine Instanz von `UserControl1` wird in einem neuen <xref:System.Windows.Forms.Integration.ElementHost>-Steuerelement namens `elementHost1` gehostet.

7. Wenn `elementHost1` Sie ausgewählt haben, drücken Sie **STRG** + **C** , um Sie in die Zwischenablage zu kopieren.

8. Drücken Sie **STRG** + **V** , um das kopierte Steuerelement in das Formular einzufügen.

   <xref:System.Windows.Forms.Integration.ElementHost>Im Formular wird ein neues Steuerelement `elementHost2` mit dem Namen erstellt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [Migration und Interoperabilität](/dotnet/framework/wpf/advanced/migration-and-interoperability)
- [Verwenden von WPF-Steuerelementen](using-wpf-controls.md)
- [Entwerfen von XAML-Code in Visual Studio](/visualstudio/xaml-tools/designing-xaml-in-visual-studio)
