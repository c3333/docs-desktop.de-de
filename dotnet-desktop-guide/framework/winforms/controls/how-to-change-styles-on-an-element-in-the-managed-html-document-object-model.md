---
title: 'Vorgehensweise: Ändern von Formaten eines Elements im verwalteten HTML-Dokumentobjektmodell'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- managed HTML DOM [Windows Forms], changing styles on elements
ms.assetid: 154e8d9f-3e2d-4e8b-a6f3-c85a070e9cc1
ms.openlocfilehash: 728bc77db959e25fe31d2ff37288b2359dca852e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975707"
---
# <a name="how-to-change-styles-on-an-element-in-the-managed-html-document-object-model"></a>Vorgehensweise: Ändern von Formaten eines Elements im verwalteten HTML-Dokumentobjektmodell

Sie können Stile in HTML verwenden, um die Darstellung eines Dokuments und seiner Elemente zu steuern. <xref:System.Windows.Forms.HtmlDocument> und <xref:System.Windows.Forms.HtmlElement> unterstützen <xref:System.Windows.Forms.HtmlElement.Style%2A> Eigenschaften, die Format Zeichenfolgen im folgenden Format annehmen:

`name1:value1;...;nameN:valueN;`

Hier sehen `DIV` Sie eine mit einer Format Zeichenfolge, die die Schriftart auf Arial und den gesamten Text auf fett formatiert:

```html
<DIV style="font-face:arial;font-weight:bold;">
Hello, world!
</DIV>
```

Das Problem beim Bearbeiten von Stilen mithilfe der- <xref:System.Windows.Forms.HtmlElement.Style%2A> Eigenschaft ist, dass es sich als mühsam erweisen kann, um einzelne Stileinstellungen aus der Zeichenfolge hinzuzufügen und zu entfernen. Beispielsweise wird es zu einem komplexen Verfahren, mit dem Sie den vorherigen Text kursiv darstellen können, wenn der Benutzer den Cursor über der positioniert `DIV` , und kursiv formatierten, wenn der Cursor die verlässt `DIV` . Die Zeit wird zu einem Problem, wenn Sie eine große Anzahl von Stilen auf diese Weise bearbeiten müssen.

Das folgende Verfahren enthält Code, mit dem Sie problemlos Stile für HTML-Dokumente und-Elemente bearbeiten können. Die Vorgehensweise erfordert, dass Sie wissen, wie Sie grundlegende Aufgaben in Windows Forms ausführen, z. b. das Erstellen eines neuen Projekts und das Hinzufügen eines Steuer Elements zu einem Formular.

### <a name="to-process-style-changes-in-a-windows-forms-application"></a>So verarbeiten Sie Stiländerungen in einer Windows Forms Anwendung

1. Erstellen Sie ein neues Windows Forms-Projekt.

2. Erstellen Sie eine neue Klassendatei, die in der für Ihre Programmiersprache geeigneten Erweiterung endet.

3. Kopieren Sie den `StyleGenerator` Klassen Code im Beispiel Abschnitt dieses Themas in die-Klassendatei, und speichern Sie den Code.

4. Speichern Sie den folgenden HTML-Code in einer Datei mit dem Namen Test.htm.

    ```html
    <HTML>
        <BODY>

            <DIV style="font-face:arial;font-weight:bold;">
                Hello, world!
            </DIV><P>

            <DIV>
                Hello again, world!
            </DIV><P>

        </BODY>
    </HTML>
    ```

5. Fügen Sie <xref:System.Windows.Forms.WebBrowser> `webBrowser1` dem Hauptformular des Projekts ein-Steuerelement mit dem Namen hinzu.

6. Fügen Sie der Codedatei Ihres Projekts den folgenden Code hinzu.

    > [!IMPORTANT]
    > Stellen Sie sicher, dass der `webBrowser1_DocumentCompleted` Ereignishandler als Listener für das <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> Ereignis konfiguriert ist. Doppelklicken Sie in Visual Studio auf das Steuerelement, <xref:System.Windows.Forms.WebBrowser> und konfigurieren Sie den Listener in einem Text-Editor Programm gesteuert.

     [!code-csharp[ManagedDOMStyles#2](~/samples/snippets/csharp/VS_Snippets_Winforms/ManagedDOMStyles/CS/Form1.cs#2)]
     [!code-vb[ManagedDOMStyles#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ManagedDOMStyles/VB/Form1.vb#2)]

7. Führen Sie das Projekt aus. Führen Sie den Cursor über den ersten `DIV` aus, um die Auswirkungen des Codes zu beobachten.

## <a name="example"></a>Beispiel

Das folgende Codebeispiel zeigt den vollständigen Code für die- `StyleGenerator` Klasse, die einen vorhandenen Stil Wert analysiert, das Hinzufügen, ändern und Entfernen von Stilen unterstützt und einen neuen Stilwert mit den angeforderten Änderungen zurückgibt.

[!code-csharp[ManagedDOMStyles#1](~/samples/snippets/csharp/VS_Snippets_Winforms/ManagedDOMStyles/CS/StyleGenerator.cs#1)]
[!code-vb[ManagedDOMStyles#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ManagedDOMStyles/VB/StyleGenerator.vb#1)]

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.HtmlElement>
