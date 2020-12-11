---
title: L2DBForm.xaml.cs-Quellcode
ms.date: 10/22/2019
ms.topic: sample
ms.openlocfilehash: 882699a76eab3c291cd92c298287bc5d28fb08e1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976545"
---
# <a name="l2dbformxamlcs-source-code"></a>L2DBForm.xaml.cs-Quellcode

Diese Seite enthält den Inhalt und die Beschreibung des c#-Quellcodes in der Datei *L2DBForm.XAML.cs*. Die in dieser Datei enthaltene L2XDBForm-Teilklasse kann in die folgenden drei logischen Abschnitte unterteilt werden: Datenmember und die Ereignishandler `OnRemove` und `OnAddBook` für das Klicken auf Schaltflächen.

## <a name="data-members"></a>Datenmember

Zwei private Datenmember werden verwendet, um diese Klasse den Fenster Ressourcen zuzuordnen, die in *L2DBForm. XAML* verwendet werden.

- Die `myBooks`-Namespacevariable wird mit `"http://www.mybooks.com"` initialisiert.

- Der `bookList`-Member wird im Konstruktor mit der folgenden Zeile in die CDATA-Zeichenfolge in *L2DBForm.xaml* initialisiert:

    ```csharp
    bookList = (XElement)((ObjectDataProvider)Resources["LoadedBooks"]).Data;
    ```

## <a name="onaddbook-event-handler"></a>Ereignishandler „OnAddBook“

Diese Methode enthält die folgenden drei Anweisungen:

- Die erste Bedingungsanweisung wird zur Eingabevalidierung verwendet.

- Die zweite Anweisung erstellt aus den Zeichenfolgenwerten, die der Benutzer im Benutzeroberflächenabschnitt **Add New Book** eingegeben hat, ein neues <xref:System.Xml.Linq.XElement>.

- Die letzte Anweisung fügt dem Datenanbieter in *L2DBForm.xaml* dieses neue Buchelement hinzu. Daraufhin aktualisiert die dynamische Datenbindung automatisch die Benutzeroberfläche mit diesem neuen Element. Zusätzlicher, vom Benutzer bereitgestellter Code ist nicht erforderlich.

## <a name="onremove-event-handler"></a>Ereignishandler „OnRemove“

Der `OnRemove`-Handler ist aus zwei Gründen komplizierter als der `OnAddBook`-Handler. Erstens: Das unformatierte XML enthält beibehaltenen Leerraum, sodass zusammen mit dem Bucheintrag auch  passende neue Zeilen entfernt werden müssen. Zweitens: Im Sinne der Bequemlichkeit wird die Auswahl, die auf dem gelöschten Element lag, auf das vorherige Element in der Liste zurückgesetzt.

Die Hauptarbeit wird aber mit dem Entfernen des ausgewählten Buchelements von lediglich zwei Anweisungen ausgeführt:

- Zunächst wird das dem aktuell ausgewählten Element im Listenfeld zugeordnete Buchelement abgerufen:

    ```csharp
    XElement selBook = (XElement)lbBooks.SelectedItem;
    ```

- Anschließend wird dieses Element aus dem Datenanbieter gelöscht:

    ```csharp
    selBook.Remove();
    ```

Auch hier stellt die dynamische Datenbindung sicher, dass die Benutzeroberfläche des Programms automatisch aktualisiert wird.

## <a name="example"></a>Beispiel

### <a name="code"></a>Code

```csharp
using System;
using System.Linq;
using System.Collections;
using System.Collections.Generic;
using System.Diagnostics;
using System.Text;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Input;
using System.Xml;
using System.Xml.Linq;

namespace LinqToXmlDataBinding {
    /// <summary>
    /// Interaction logic for L2XDBForm.xaml
    /// </summary>

    public partial class L2XDBForm : System.Windows.Window
    {
        XNamespace mybooks = "http://www.mybooks.com";
        XElement bookList;

        public L2XDBForm()
        {
            InitializeComponent();
            bookList = (XElement)((ObjectDataProvider)Resources["LoadedBooks"]).Data;
        }

        void OnRemoveBook(object sender, EventArgs e)
        {
            int index = lbBooks.SelectedIndex;
            if (index < 0) return;

            XElement selBook = (XElement)lbBooks.SelectedItem;
            //Get next node before removing element.
            XNode nextNode = selBook.NextNode;
            selBook.Remove();

            //Remove any matching newline node.
            if (nextNode != null && nextNode.ToString().Trim().Equals(""))
            { nextNode.Remove(); }

            //Set selected item.
            if (lbBooks.Items.Count > 0)
            {  lbBooks.SelectedItem = lbBooks.Items[index > 0 ? index - 1 : 0]; }
        }

        void OnAddBook(object sender, EventArgs e)
        {
            if (String.IsNullOrEmpty(tbAddID.Text) ||
                String.IsNullOrEmpty(tbAddValue.Text))
            {
                MessageBox.Show("Please supply both a Book ID and a Value!", "Entry Error!");
                return;
            }
            XElement newBook = new XElement(
                                mybooks + "book",
                                new XAttribute("id", tbAddID.Text),
                                tbAddValue.Text);
            bookList.Add("  ", newBook, "\r\n");
        }
    }
}
```

### <a name="comments"></a>Kommentare

Informationen zur zugeordneten XAML-Quelle für diese Handler finden Sie unter [L2DBForm.xaml.cs-Quellcode](l2dbform-xaml-source-code.md).

## <a name="see-also"></a>Siehe auch

- [Exemplarische Vorgehensweise: LinqToXmlDataBinding-Beispiel](linq-to-xml-data-binding-sample.md)
- [L2DBForm.xaml-Quellcode](l2dbform-xaml-source-code.md)
