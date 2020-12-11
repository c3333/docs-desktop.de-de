---
title: 'Vorgehensweise: Anzeigen der kontextbezogenen Hilfe'
ms.date: 03/30/2017
helpviewer_keywords:
- pop-up Help
- Help [Windows Forms], pop-up Help
- Windows Forms, displaying Help
- forms [Windows Forms], displaying Help
- modal dialog boxes [Windows Forms], pop-up Help
- F1 Help [Windows Forms], in dialog boxes
- HelpProvider component [Windows Forms]
- Help [Windows Forms], adding to dialog boxes
ms.assetid: 218aa81e-e87e-4d67-af05-11627bbdce3b
ms.openlocfilehash: a3b40f49119fcf7900f1f0c8b77c5d83fe81144c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972358"
---
# <a name="how-to-display-pop-up-help"></a>Gewusst wie: Anzeigen der Popup Hilfe

Eine Möglichkeit zum Anzeigen der Hilfe Windows Forms finden Sie über die Schaltfläche " **Hilfe** ", die sich auf der rechten Seite der Titelleiste befindet, auf die über die-Eigenschaft zugegriffen werden kann <xref:System.Windows.Forms.Form.HelpButton%2A> . Diese Art, die Hilfe aufzurufen, eignet sich besonders für Dialogfelder. In modal (mit der <xref:System.Windows.Forms.Form.ShowDialog%2A>-Methode) angezeigten Dialogfeldern ist das Aufrufen externer Hilfesysteme problematisch, da modale Dialogfelder zuerst geschlossen werden müssen, ehe der Fokus auf ein anderes Fenster gerichtet werden kann. Außerdem erfordert die Verwendung der Schaltfläche **Hilfe** , dass in der Titelleiste keine Schaltfläche **minimieren** oder **maximieren** angezeigt wird. Dabei handelt es sich um eine standardmäßige Dialogfeld Konvention, während Formulare normalerweise die Schaltflächen **minimieren** und **maximieren** .

Sie können die-Komponente auch verwenden, <xref:System.Windows.Forms.HelpProvider> um Steuerelemente mit Dateien in einem Hilfesystem zu verknüpfen, auch wenn Sie die Popup Hilfe implementiert haben. Weitere Informationen finden Sie unter [Bereitstellen von Hilfe in einer Windows-Anwendung](how-to-provide-help-in-a-windows-application.md).

## <a name="display-pop-up-help"></a>Popup Hilfe anzeigen

1. Ziehen Sie in Visual Studio eine [HelpProvider](../controls/helpprovider-component-windows-forms.md) -Komponente aus der Toolbox auf das Formular.

   Sie befindet sich in der Komponentenleiste im unteren Bereich des Windows Forms Designer.

2. Legen Sie im Fenster "Eigenschaften" die Eigenschaft <xref:System.Windows.Forms.Form.HelpButton%2A> auf `true` fest. Dadurch wird in der Titelleiste des Formulars auf der rechten Seite eine Schaltfläche mit einem Fragezeichen angezeigt.

3. Damit die Hilfeschaltfläche <xref:System.Windows.Forms.Form.HelpButton%2A> angezeigt werden kann, müssen Sie die Eigenschaften <xref:System.Windows.Forms.Form.MinimizeBox%2A> und <xref:System.Windows.Forms.Form.MaximizeBox%2A> des Formulars auf `false`, die Eigenschaft <xref:System.Windows.Forms.Form.ControlBox%2A> auf `true` und die Eigenschaft <xref:System.Windows.Forms.Form.FormBorderStyle%2A> auf einen der folgenden Werte festlegen: <xref:System.Windows.Forms.FormBorderStyle.FixedSingle>, <xref:System.Windows.Forms.FormBorderStyle.Fixed3D>, <xref:System.Windows.Forms.FormBorderStyle.FixedDialog> oder <xref:System.Windows.Forms.FormBorderStyle.Sizable>.

4. Wählen Sie das Steuerelement aus, für das Sie Hilfeinformationen in Ihrem Formular anzeigen möchten, und legen Sie im Fenster "Eigenschaften" den Hilfetext fest. Dies ist die Text Zeichenfolge, die [in einem Fenster](../controls/tooltip-component-windows-forms.md)angezeigt wird, das einer QuickInfo ähnelt.

5. Drücken Sie **F5**.

6. Klicken Sie in der Titelleiste auf die Schaltfläche **Hilfe** , und klicken Sie auf das Steuerelement, für das Sie die Hilfe Zeichenfolge

## <a name="see-also"></a>Siehe auch

- [Benutzerführung mithilfe von QuickInfos](control-help-using-tooltips.md)
- [Integrieren von Benutzerhilfe in Windows Forms](integrating-user-help-in-windows-forms.md)
- [Windows Forms](../index.yml)
