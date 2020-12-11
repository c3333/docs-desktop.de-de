---
title: Übersicht über das PrintPreviewDialog-Steuerelement
ms.date: 01/08/2018
f1_keywords:
- PrintPreviewDialog
helpviewer_keywords:
- PrintPreviewDialog control (using designer), about PrintPreviewDialog
ms.assetid: efd4ee8d-6edd-47ec-88e4-4a4759bd2384
ms.openlocfilehash: c7576beb56cd10a691a850969c132a2d33ad8870
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972347"
---
# <a name="printpreviewdialog-control-overview-windows-forms"></a>Übersicht über das PrintPreviewDialog-Steuerelement (Windows Forms)

Das Windows Forms- <xref:System.Windows.Forms.PrintPreviewDialog> Steuerelement ist ein vorkonfiguriertes Dialogfeld, mit dem angezeigt wird, wie ein [PrintDocument](printdocument-component-windows-forms.md) angezeigt wird, wenn es gedruckt wird. Verwenden Sie es in Ihrer Windows-basierten Anwendung als einfache Lösung, anstatt ein eigenes Dialogfeld zu konfigurieren. Das Steuerelement enthält Schaltflächen zum Drucken, Vergrößern, Anzeigen mindestens einer Seite und Schließen des Dialogfelds.

## <a name="key-properties-and-methods"></a>Schlüsseleigenschaften und-Methoden

Die Schlüsseleigenschaft des Steuer Elements ist <xref:System.Windows.Forms.PrintPreviewDialog.Document%2A> , wodurch das Dokument in der Vorschau angezeigt wird. Das Dokument muss ein- <xref:System.Drawing.Printing.PrintDocument> Objekt sein. Um das Dialogfeld anzuzeigen, müssen Sie die zugehörige- <xref:System.Windows.Forms.Form.ShowDialog%2A> Methode aufrufen. Antialiasing kann dazu führen, dass der Text glatter erscheint, aber auch die Anzeige langsamer wird. um es zu verwenden, legen Sie die- <xref:System.Windows.Forms.PrintPreviewDialog.UseAntiAlias%2A> Eigenschaft auf fest `true` .

Bestimmte Eigenschaften sind über die verfügbar <xref:System.Windows.Forms.PrintPreviewControl> , die in <xref:System.Windows.Forms.PrintPreviewDialog> enthalten ist. (Sie müssen das <xref:System.Windows.Forms.PrintPreviewControl> Formular nicht dem Formular hinzufügen. es wird automatisch in der enthalten, <xref:System.Windows.Forms.PrintPreviewDialog> Wenn Sie das Dialogfeld zum Formular hinzufügen.) Beispiele für Eigenschaften, die über den verfügbar <xref:System.Windows.Forms.PrintPreviewControl> sind, sind die <xref:System.Windows.Forms.PrintPreviewControl.Columns%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.PrintPreviewControl.Rows%2A> , die die Anzahl der horizontal und vertikal angezeigten Seiten auf dem Steuerelement bestimmen. Sie können <xref:System.Windows.Forms.PrintPreviewControl.Columns%2A> wie `PrintPreviewDialog1.PrintPreviewControl.Columns` in Visual Basic, `printPreviewDialog1.PrintPreviewControl.Columns` in Visual c# oder `printPreviewDialog1->PrintPreviewControl->Columns` Visual C++ auf die-Eigenschaft zugreifen.

## <a name="printpreviewdialog-performance"></a>PrintPreviewDialog-Leistung

Unter den folgenden Bedingungen wird das- <xref:System.Windows.Forms.PrintPreviewDialog> Steuerelement sehr langsam initialisiert:

- Ein Netzwerkdrucker wird verwendet.
- Die Benutzereinstellungen für diesen Drucker (z. b. Duplex Einstellungen) werden geändert.

Für apps, die auf dem .NET Framework 4.5.2 ausgeführt werden, können Sie den folgenden Schlüssel zum- \<appSettings> Abschnitt der Konfigurationsdatei hinzufügen, um die Leistung der <xref:System.Windows.Forms.PrintPreviewDialog> Steuerungs Initialisierung zu verbessern:

```xml
<appSettings>
   <add key="EnablePrintPreviewOptimization" value="true" />
</appSettings>
```

Wenn der `EnablePrintPreviewOptimization` Schlüssel auf einen anderen Wert festgelegt ist, oder wenn der Schlüssel nicht vorhanden ist, wird die Optimierung nicht angewendet.

Für apps, die unter .NET Framework 4,6 oder höheren Versionen ausgeführt werden, können Sie den folgenden Schalter dem- [\<AppContextSwitchOverrides>](/dotnet/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element) Element im- [\<runtime>](/dotnet/framework/configure-apps/file-schema/runtime/index) Abschnitt Ihrer APP-Konfigurationsdatei hinzufügen:

```xml
<runtime >
   <!-- AppContextSwitchOverrides values are in the form of 'key1=true|false;key2=true|false -->
   <AppContextSwitchOverrides value = "Switch.System.Drawing.Printing.OptimizePrintPreview=true" />
</runtime >
```

Wenn der Schalter nicht vorhanden ist oder auf einen anderen Wert festgelegt ist, wird die Optimierung nicht angewendet.

Wenn Sie das- <xref:System.Drawing.Printing.PrintDocument.QueryPageSettings> Ereignis verwenden, um Druckereinstellungen zu ändern, wird die Leistung des <xref:System.Windows.Forms.PrintPreviewDialog> Steuer Elements nicht verbessert, auch wenn ein Optimierungs Konfigurationsschalter festgelegt ist.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.PrintPreviewDialog>
- [Übersicht über das PrintPreviewControl-Steuerelement](printpreviewcontrol-control-overview-windows-forms.md)
- [PrintPreviewDialog-Steuerelement](printpreviewdialog-control-windows-forms.md)
- [Dialogfeld-Steuerelemente und -Komponenten](dialog-box-controls-and-components-windows-forms.md)
