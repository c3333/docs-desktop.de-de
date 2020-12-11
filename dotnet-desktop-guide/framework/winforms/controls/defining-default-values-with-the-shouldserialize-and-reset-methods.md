---
title: Definieren von Standardwerten mit der ShouldSerialize-Methode und der Reset-Methode
description: Erfahren Sie, wie Sie die Methoden zum Windows Forms-Designer verwenden, um das Verhalten der-Designer zu steuern.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], property methods
- ShouldPersist method
ms.assetid: 7b6c5e00-3771-46b4-9142-5a80d5864a5e
ms.openlocfilehash: b425b301a1c07030ad4cefa70e41198d08598631
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972143"
---
# <a name="defining-default-values-with-the-shouldserialize-and-reset-methods"></a>Definieren von Standardwerten mit der ShouldSerialize-Methode und der Reset-Methode
`ShouldSerialize` und `Reset` sind optionale Methoden, die Sie für eine Eigenschaft bereitstellen können, wenn die Eigenschaft nicht über einen einfachen Standardwert verfügt. Wenn die Eigenschaft über einen einfachen Standardwert verfügt, sollten Sie den anwenden <xref:System.ComponentModel.DefaultValueAttribute> und stattdessen den Standardwert für den attributklassenkonstruktor angeben. Beide Mechanismen ermöglichen die folgenden Funktionen im Designer:

- Die-Eigenschaft stellt im Eigenschaften Browser eine visuelle Anzeige dar, wenn Sie von ihrem Standardwert geändert wurde.

- Der Benutzer kann mit der rechten Maustaste auf die Eigenschaft klicken und **Zurücksetzen** auswählen, um die Eigenschaft auf den Standardwert wiederherzustellen.

- Der Designer generiert effizienteren Code.

> [!NOTE]
> Wenden Sie entweder an, <xref:System.ComponentModel.DefaultValueAttribute> oder stellen Sie die `Reset` Methoden *propertyName* und `ShouldSerialize` *propertyName* bereit. Verwenden Sie nicht beides.

Verwenden Sie beim Deklarieren einer- `ShouldSerialize` oder- `Reset` Methode den `private` Zugriffsmodifizierer Diese Methoden werden in der Regel vom Designer und nicht von Benutzercode aufgerufen.

 Mit der `Reset` *propertyName* -Methode wird eine Eigenschaft auf ihren Standardwert festgelegt, wie im folgenden Code Fragment dargestellt.

```vb
Private Sub ResetMyFont()
   MyFont = Nothing
End Sub
```

```csharp
private void ResetMyFont()
{
   MyFont = null;
}
```

> [!NOTE]
> Wenn eine Eigenschaft nicht über eine- `Reset` Methode verfügt, nicht mit markiert ist <xref:System.ComponentModel.DefaultValueAttribute> und in der Deklaration kein Standardwert angegeben ist, `Reset` wird die Option für diese Eigenschaft im Kontextmenü des **Eigenschaften** Fensters der Windows Forms-Designer in Visual Studio deaktiviert.

 Designer wie Visual Studio verwenden die `ShouldSerialize` *propertyName* -Methode, um zu überprüfen, ob sich eine Eigenschaft von ihrem Standardwert geändert hat, und schreiben Code nur in das Formular, wenn eine Eigenschaft geändert wird, was eine effizientere Codegenerierung ermöglicht. Beispiel:

```vb
'Returns true if the font has changed; otherwise, returns false.
' The designer writes code to the form only if true is returned.
Private Function ShouldSerializeMyFont() As Boolean
   Return thefont IsNot Nothing
End Function
```

```csharp
// Returns true if the font has changed; otherwise, returns false.
// The designer writes code to the form only if true is returned.
private bool ShouldSerializeMyFont()
{
   return thefont != null;
}
```

> [!TIP]
> Wenn Sie die Serialisierung einer Eigenschaft durch den Designer dauerhaft verhindern möchten, fügen Sie das [DesignerSerializationVisibility](xref:System.ComponentModel.DesignerSerializationVisibilityAttribute) -Attribut mit dem Wert von hinzu `Hidden` .

 Ein umfassendes Codebeispiel folgt.

```vb
Option Explicit
Option Strict

Imports System.Drawing
Imports System.Windows.Forms

Public Class MyControl
   Inherits Control

   ' Declare an instance of the Font class
   ' and set its default value to Nothing.
   Private thefont As Font = Nothing

   ' The MyFont property.
   Public Property MyFont() As Font
      ' Note that the Font property never
      ' returns null.
      Get
         If Not (thefont Is Nothing) Then
            Return thefont
         End If
         If Not (Parent Is Nothing) Then
            Return Parent.Font
         End If
         Return Control.DefaultFont
      End Get
      Set
         thefont = value
      End Set
   End Property

   Private Function ShouldSerializeMyFont() As Boolean
      Return thefont IsNot Nothing
   End Function

   Private Sub ResetMyFont()
      MyFont = Nothing
   End Sub
End Class
```

```csharp
using System;
using System.Drawing;
using System.Windows.Forms;

public class MyControl : Control {
   // Declare an instance of the Font class
   // and set its default value to null.
   private Font thefont = null;

   // The MyFont property.
   public Font MyFont {
      // Note that the MyFont property never
      // returns null.
      get {
         if (thefont != null) return thefont;
         if (Parent != null) return Parent.Font;
         return Control.DefaultFont;
      }
      set {
         thefont = value;
      }
   }

   private bool ShouldSerializeMyFont()
   {
      return thefont != null;
   }

   private void ResetMyFont()
   {
      MyFont = null;
   }
}
```

 In diesem Fall wird der Eigenschaften Browser nicht angezeigt, auch wenn der Wert der privaten Variablen, auf die von der- `MyFont` Eigenschaft zugegriffen wird `null` , nicht angezeigt wird `null` . stattdessen wird die- <xref:System.Windows.Forms.Control.Font%2A> Eigenschaft des übergeordneten Elements angezeigt, wenn dies nicht der Fall ist `null` , oder der <xref:System.Windows.Forms.Control.Font%2A> in definierte Standardwert <xref:System.Windows.Forms.Control> . Daher kann der Standardwert für `MyFont` nicht einfach festgelegt werden, und ein <xref:System.ComponentModel.DefaultValueAttribute> kann nicht auf diese Eigenschaft angewendet werden. Stattdessen müssen die `ShouldSerialize` -Methode und die- `Reset` Methode für die-Eigenschaft implementiert werden `MyFont` .

## <a name="see-also"></a>Siehe auch

- [Eigenschaften von Windows Forms-Steuerelementen](properties-in-windows-forms-controls.md)
- [Definieren einer Eigenschaft](defining-a-property-in-windows-forms-controls.md)
- [Durch geänderte Eigenschaften ausgelöste Ereignisse](property-changed-events.md)
- <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute?displayProperty=fullName>
