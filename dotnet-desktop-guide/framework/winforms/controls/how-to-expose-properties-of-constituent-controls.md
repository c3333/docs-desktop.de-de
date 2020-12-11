---
title: 'Vorgehensweise: Verfügbarmachen der Eigenschaften konstituierender Steuerelemente'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- user controls [Windows Forms], exposing constituent controls
- controls [Windows Forms], constituent
- custom controls [Windows Forms], exposing properties
- constituent controls
ms.assetid: 5c1ec98b-aa48-4823-986e-4712551cfdf1
ms.openlocfilehash: f006e42771a5ecc71f6a508fd78d0e2dd8f2d2f2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975640"
---
# <a name="how-to-expose-properties-of-constituent-controls"></a>Vorgehensweise: Verfügbarmachen der Eigenschaften konstituierender Steuerelemente
Die Steuerelemente, die ein zusammengesetztes Steuerelement bilden, sind *konstituierende Steuerelemente*. Diese Steuerelemente werden normalerweise als privat deklariert und können daher nicht vom Entwickler aufgerufen werden. Wenn Sie für zukünftige Benutzereigenschaften dieser Steuerelemente verfügbar machen möchten, müssen Sie Sie für den Benutzer verfügbar machen. Eine Eigenschaft eines konstituierenden Steuer Elements wird verfügbar gemacht, indem eine Eigenschaft im Benutzer Steuerelement erstellt und der-Accessor und der-Accessor dieser Eigenschaft verwendet werden, `get` `set` um die Änderung in der private-Eigenschaft des konstituierenden Steuer Elements zu beeinflussen.

 Stellen Sie sich ein hypothetisches Benutzer Steuerelement mit einer konstituierenden Schalt `MyButton` Fläche namens vor In diesem Beispiel wird der Wert, der `ConstituentButtonBackColor` in der- <xref:System.Windows.Forms.Control.BackColor%2A> Eigenschaft von gespeichert ist, übermittelt `MyButton` , wenn der Benutzer die-Eigenschaft anfordert. Wenn der Benutzer dieser Eigenschaft einen Wert zuweist, wird dieser Wert automatisch an die <xref:System.Windows.Forms.Control.BackColor%2A> -Eigenschaft von übermittelt, `MyButton` und der `set` Code wird ausgeführt, und die Farbe von wird geändert `MyButton` .

 Im folgenden Beispiel wird gezeigt, wie die- <xref:System.Windows.Forms.Control.BackColor%2A> Eigenschaft der konstituierenden Schaltfläche verfügbar gemacht wird:

```vb
Public Property ButtonColor() as System.Drawing.Color
   Get
      Return MyButton.BackColor
   End Get
   Set(Value as System.Drawing.Color)
      MyButton.BackColor = Value
   End Set
End Property
```

```csharp
public Color ButtonColor
{
   get
   {
      return(myButton.BackColor);
   }
   set
   {
      myButton.BackColor = value;
   }
}
```

### <a name="to-expose-a-property-of-a-constituent-control"></a>So machen Sie eine Eigenschaft eines konstituierenden Steuer Elements verfügbar

1. Erstellen Sie eine öffentliche Eigenschaft für das Benutzer Steuerelement.

2. `get`Schreiben Sie im-Abschnitt der-Eigenschaft Code, der den Wert der Eigenschaft abruft, die Sie verfügbar machen möchten.

3. `set`Schreiben Sie im-Abschnitt der-Eigenschaft Code, der den Wert der-Eigenschaft an die verfügbar gemachte-Eigenschaft des konstituierenden Steuer Elements übergibt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.UserControl>
- [Eigenschaften von Windows Forms-Steuerelementen](properties-in-windows-forms-controls.md)
- [Arten von benutzerdefinierten Steuerelementen](varieties-of-custom-controls.md)
