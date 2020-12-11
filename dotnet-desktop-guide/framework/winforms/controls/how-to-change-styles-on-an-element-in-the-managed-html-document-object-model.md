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
# <a name="how-to-change-styles-on-an-element-in-the-managed-html-document-object-model"></a><span data-ttu-id="da38f-102">Vorgehensweise: Ändern von Formaten eines Elements im verwalteten HTML-Dokumentobjektmodell</span><span class="sxs-lookup"><span data-stu-id="da38f-102">How to: Change Styles on an Element in the Managed HTML Document Object Model</span></span>

<span data-ttu-id="da38f-103">Sie können Stile in HTML verwenden, um die Darstellung eines Dokuments und seiner Elemente zu steuern.</span><span class="sxs-lookup"><span data-stu-id="da38f-103">You can use styles in HTML to control the appearance of a document and its elements.</span></span> <span data-ttu-id="da38f-104"><xref:System.Windows.Forms.HtmlDocument> und <xref:System.Windows.Forms.HtmlElement> unterstützen <xref:System.Windows.Forms.HtmlElement.Style%2A> Eigenschaften, die Format Zeichenfolgen im folgenden Format annehmen:</span><span class="sxs-lookup"><span data-stu-id="da38f-104"><xref:System.Windows.Forms.HtmlDocument> and <xref:System.Windows.Forms.HtmlElement> support <xref:System.Windows.Forms.HtmlElement.Style%2A> properties that take style strings of the following format:</span></span>

`name1:value1;...;nameN:valueN;`

<span data-ttu-id="da38f-105">Hier sehen `DIV` Sie eine mit einer Format Zeichenfolge, die die Schriftart auf Arial und den gesamten Text auf fett formatiert:</span><span class="sxs-lookup"><span data-stu-id="da38f-105">Here is a `DIV` with a style string that sets the font to Arial and all text to bold:</span></span>

```html
<DIV style="font-face:arial;font-weight:bold;">
Hello, world!
</DIV>
```

<span data-ttu-id="da38f-106">Das Problem beim Bearbeiten von Stilen mithilfe der- <xref:System.Windows.Forms.HtmlElement.Style%2A> Eigenschaft ist, dass es sich als mühsam erweisen kann, um einzelne Stileinstellungen aus der Zeichenfolge hinzuzufügen und zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="da38f-106">The problem with manipulating styles using the <xref:System.Windows.Forms.HtmlElement.Style%2A> property is that it can prove cumbersome to add to and remove individual style settings from the string.</span></span> <span data-ttu-id="da38f-107">Beispielsweise wird es zu einem komplexen Verfahren, mit dem Sie den vorherigen Text kursiv darstellen können, wenn der Benutzer den Cursor über der positioniert `DIV` , und kursiv formatierten, wenn der Cursor die verlässt `DIV` .</span><span class="sxs-lookup"><span data-stu-id="da38f-107">For example, it would become a complex procedure for you to render the previous text in italics whenever the user positions the cursor over the `DIV`, and take italics off when the cursor leaves the `DIV`.</span></span> <span data-ttu-id="da38f-108">Die Zeit wird zu einem Problem, wenn Sie eine große Anzahl von Stilen auf diese Weise bearbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="da38f-108">Time would become an issue if you need to manipulate a large number of styles in this manner.</span></span>

<span data-ttu-id="da38f-109">Das folgende Verfahren enthält Code, mit dem Sie problemlos Stile für HTML-Dokumente und-Elemente bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="da38f-109">The following procedure contains code that you can use to easily manipulate styles on HTML documents and elements.</span></span> <span data-ttu-id="da38f-110">Die Vorgehensweise erfordert, dass Sie wissen, wie Sie grundlegende Aufgaben in Windows Forms ausführen, z. b. das Erstellen eines neuen Projekts und das Hinzufügen eines Steuer Elements zu einem Formular.</span><span class="sxs-lookup"><span data-stu-id="da38f-110">The procedure requires that you know how to perform basic tasks in Windows Forms, such as creating a new project and adding a control to a form.</span></span>

### <a name="to-process-style-changes-in-a-windows-forms-application"></a><span data-ttu-id="da38f-111">So verarbeiten Sie Stiländerungen in einer Windows Forms Anwendung</span><span class="sxs-lookup"><span data-stu-id="da38f-111">To process style changes in a Windows Forms application</span></span>

1. <span data-ttu-id="da38f-112">Erstellen Sie ein neues Windows Forms-Projekt.</span><span class="sxs-lookup"><span data-stu-id="da38f-112">Create a new Windows Forms project.</span></span>

2. <span data-ttu-id="da38f-113">Erstellen Sie eine neue Klassendatei, die in der für Ihre Programmiersprache geeigneten Erweiterung endet.</span><span class="sxs-lookup"><span data-stu-id="da38f-113">Create a new class file ending in the extension appropriate for your programming language.</span></span>

3. <span data-ttu-id="da38f-114">Kopieren Sie den `StyleGenerator` Klassen Code im Beispiel Abschnitt dieses Themas in die-Klassendatei, und speichern Sie den Code.</span><span class="sxs-lookup"><span data-stu-id="da38f-114">Copy the `StyleGenerator` class code in the Example section of this topic into the class file, and save the code.</span></span>

4. <span data-ttu-id="da38f-115">Speichern Sie den folgenden HTML-Code in einer Datei mit dem Namen Test.htm.</span><span class="sxs-lookup"><span data-stu-id="da38f-115">Save the following HTML to a file named Test.htm.</span></span>

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

5. <span data-ttu-id="da38f-116">Fügen Sie <xref:System.Windows.Forms.WebBrowser> `webBrowser1` dem Hauptformular des Projekts ein-Steuerelement mit dem Namen hinzu.</span><span class="sxs-lookup"><span data-stu-id="da38f-116">Add a <xref:System.Windows.Forms.WebBrowser> control named `webBrowser1` to the main form of your project.</span></span>

6. <span data-ttu-id="da38f-117">Fügen Sie der Codedatei Ihres Projekts den folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="da38f-117">Add the following code to your project's code file.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="da38f-118">Stellen Sie sicher, dass der `webBrowser1_DocumentCompleted` Ereignishandler als Listener für das <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> Ereignis konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="da38f-118">Ensure that the `webBrowser1_DocumentCompleted` event handler is configured as a listener for the <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> event.</span></span> <span data-ttu-id="da38f-119">Doppelklicken Sie in Visual Studio auf das Steuerelement, <xref:System.Windows.Forms.WebBrowser> und konfigurieren Sie den Listener in einem Text-Editor Programm gesteuert.</span><span class="sxs-lookup"><span data-stu-id="da38f-119">In Visual Studio, double-click on the <xref:System.Windows.Forms.WebBrowser> control; in a text editor, configure the listener programmatically.</span></span>

     [!code-csharp[ManagedDOMStyles#2](~/samples/snippets/csharp/VS_Snippets_Winforms/ManagedDOMStyles/CS/Form1.cs#2)]
     [!code-vb[ManagedDOMStyles#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ManagedDOMStyles/VB/Form1.vb#2)]

7. <span data-ttu-id="da38f-120">Führen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="da38f-120">Run the project.</span></span> <span data-ttu-id="da38f-121">Führen Sie den Cursor über den ersten `DIV` aus, um die Auswirkungen des Codes zu beobachten.</span><span class="sxs-lookup"><span data-stu-id="da38f-121">Run your cursor over the first `DIV` to observe the effects of the code.</span></span>

## <a name="example"></a><span data-ttu-id="da38f-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="da38f-122">Example</span></span>

<span data-ttu-id="da38f-123">Das folgende Codebeispiel zeigt den vollständigen Code für die- `StyleGenerator` Klasse, die einen vorhandenen Stil Wert analysiert, das Hinzufügen, ändern und Entfernen von Stilen unterstützt und einen neuen Stilwert mit den angeforderten Änderungen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="da38f-123">The following code example shows the full code for the `StyleGenerator` class, which parses an existing style value, supports adding, changing, and removing styles, and returns a new style value with the requested changes.</span></span>

[!code-csharp[ManagedDOMStyles#1](~/samples/snippets/csharp/VS_Snippets_Winforms/ManagedDOMStyles/CS/StyleGenerator.cs#1)]
[!code-vb[ManagedDOMStyles#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ManagedDOMStyles/VB/StyleGenerator.vb#1)]

## <a name="see-also"></a><span data-ttu-id="da38f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da38f-124">See also</span></span>

- <xref:System.Windows.Forms.HtmlElement>
