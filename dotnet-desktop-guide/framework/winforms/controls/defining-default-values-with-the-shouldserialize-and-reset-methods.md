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
# <a name="defining-default-values-with-the-shouldserialize-and-reset-methods"></a><span data-ttu-id="2f4b1-103">Definieren von Standardwerten mit der ShouldSerialize-Methode und der Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="2f4b1-103">Defining Default Values with the ShouldSerialize and Reset Methods</span></span>
<span data-ttu-id="2f4b1-104">`ShouldSerialize` und `Reset` sind optionale Methoden, die Sie für eine Eigenschaft bereitstellen können, wenn die Eigenschaft nicht über einen einfachen Standardwert verfügt.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-104">`ShouldSerialize` and `Reset` are optional methods that you can provide for a property, if the property does not have a simple default value.</span></span> <span data-ttu-id="2f4b1-105">Wenn die Eigenschaft über einen einfachen Standardwert verfügt, sollten Sie den anwenden <xref:System.ComponentModel.DefaultValueAttribute> und stattdessen den Standardwert für den attributklassenkonstruktor angeben.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-105">If the property has a simple default value, you should apply the <xref:System.ComponentModel.DefaultValueAttribute> and supply the default value to the attribute class constructor instead.</span></span> <span data-ttu-id="2f4b1-106">Beide Mechanismen ermöglichen die folgenden Funktionen im Designer:</span><span class="sxs-lookup"><span data-stu-id="2f4b1-106">Either of these mechanisms enables the following features in the designer:</span></span>

- <span data-ttu-id="2f4b1-107">Die-Eigenschaft stellt im Eigenschaften Browser eine visuelle Anzeige dar, wenn Sie von ihrem Standardwert geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-107">The property provides visual indication in the property browser if it has been modified from its default value.</span></span>

- <span data-ttu-id="2f4b1-108">Der Benutzer kann mit der rechten Maustaste auf die Eigenschaft klicken und **Zurücksetzen** auswählen, um die Eigenschaft auf den Standardwert wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-108">The user can right-click on the property and choose **Reset** to restore the property to its default value.</span></span>

- <span data-ttu-id="2f4b1-109">Der Designer generiert effizienteren Code.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-109">The designer generates more efficient code.</span></span>

> [!NOTE]
> <span data-ttu-id="2f4b1-110">Wenden Sie entweder an, <xref:System.ComponentModel.DefaultValueAttribute> oder stellen Sie die `Reset` Methoden *propertyName* und `ShouldSerialize` *propertyName* bereit.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-110">Either apply the <xref:System.ComponentModel.DefaultValueAttribute> or provide `Reset`*PropertyName* and `ShouldSerialize`*PropertyName* methods.</span></span> <span data-ttu-id="2f4b1-111">Verwenden Sie nicht beides.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-111">Do not use both.</span></span>

<span data-ttu-id="2f4b1-112">Verwenden Sie beim Deklarieren einer- `ShouldSerialize` oder- `Reset` Methode den `private` Zugriffsmodifizierer</span><span class="sxs-lookup"><span data-stu-id="2f4b1-112">When declaring a `ShouldSerialize` or `Reset` method, use the `private` access modifier.</span></span> <span data-ttu-id="2f4b1-113">Diese Methoden werden in der Regel vom Designer und nicht von Benutzercode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-113">These methods are usually invoked by the designer and not by user code.</span></span>

 <span data-ttu-id="2f4b1-114">Mit der `Reset` *propertyName* -Methode wird eine Eigenschaft auf ihren Standardwert festgelegt, wie im folgenden Code Fragment dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-114">The `Reset`*PropertyName* method sets a property to its default value, as shown in the following code fragment.</span></span>

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
> <span data-ttu-id="2f4b1-115">Wenn eine Eigenschaft nicht über eine- `Reset` Methode verfügt, nicht mit markiert ist <xref:System.ComponentModel.DefaultValueAttribute> und in der Deklaration kein Standardwert angegeben ist, `Reset` wird die Option für diese Eigenschaft im Kontextmenü des **Eigenschaften** Fensters der Windows Forms-Designer in Visual Studio deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-115">If a property does not have a `Reset` method, is not marked with a <xref:System.ComponentModel.DefaultValueAttribute>, and does not have a default value supplied in its declaration, the `Reset` option for that property is disabled in the shortcut menu of the **Properties** window of the Windows Forms Designer in Visual Studio.</span></span>

 <span data-ttu-id="2f4b1-116">Designer wie Visual Studio verwenden die `ShouldSerialize` *propertyName* -Methode, um zu überprüfen, ob sich eine Eigenschaft von ihrem Standardwert geändert hat, und schreiben Code nur in das Formular, wenn eine Eigenschaft geändert wird, was eine effizientere Codegenerierung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-116">Designers such as Visual Studio use the `ShouldSerialize`*PropertyName* method to check whether a property has changed from its default value and write code into the form only if a property is changed, thus allowing for more efficient code generation.</span></span> <span data-ttu-id="2f4b1-117">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2f4b1-117">For example:</span></span>

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
> <span data-ttu-id="2f4b1-118">Wenn Sie die Serialisierung einer Eigenschaft durch den Designer dauerhaft verhindern möchten, fügen Sie das [DesignerSerializationVisibility](xref:System.ComponentModel.DesignerSerializationVisibilityAttribute) -Attribut mit dem Wert von hinzu `Hidden` .</span><span class="sxs-lookup"><span data-stu-id="2f4b1-118">If you want to permanently prevent a property from being serialized by the designer, add the [DesignerSerializationVisibility](xref:System.ComponentModel.DesignerSerializationVisibilityAttribute) attribute with the value of `Hidden`.</span></span>

 <span data-ttu-id="2f4b1-119">Ein umfassendes Codebeispiel folgt.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-119">A complete code example follows.</span></span>

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

 <span data-ttu-id="2f4b1-120">In diesem Fall wird der Eigenschaften Browser nicht angezeigt, auch wenn der Wert der privaten Variablen, auf die von der- `MyFont` Eigenschaft zugegriffen wird `null` , nicht angezeigt wird `null` . stattdessen wird die- <xref:System.Windows.Forms.Control.Font%2A> Eigenschaft des übergeordneten Elements angezeigt, wenn dies nicht der Fall ist `null` , oder der <xref:System.Windows.Forms.Control.Font%2A> in definierte Standardwert <xref:System.Windows.Forms.Control> .</span><span class="sxs-lookup"><span data-stu-id="2f4b1-120">In this case, even when the value of the private variable accessed by the `MyFont` property is `null`, the property browser does not display `null`; instead, it displays the <xref:System.Windows.Forms.Control.Font%2A> property of the parent, if it is not `null`, or the default <xref:System.Windows.Forms.Control.Font%2A> value defined in <xref:System.Windows.Forms.Control>.</span></span> <span data-ttu-id="2f4b1-121">Daher kann der Standardwert für `MyFont` nicht einfach festgelegt werden, und ein <xref:System.ComponentModel.DefaultValueAttribute> kann nicht auf diese Eigenschaft angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f4b1-121">Thus the default value for `MyFont` cannot be simply set, and a <xref:System.ComponentModel.DefaultValueAttribute> cannot be applied to this property.</span></span> <span data-ttu-id="2f4b1-122">Stattdessen müssen die `ShouldSerialize` -Methode und die- `Reset` Methode für die-Eigenschaft implementiert werden `MyFont` .</span><span class="sxs-lookup"><span data-stu-id="2f4b1-122">Instead, the `ShouldSerialize` and `Reset` methods must be implemented for the `MyFont` property.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f4b1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f4b1-123">See also</span></span>

- [<span data-ttu-id="2f4b1-124">Eigenschaften von Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="2f4b1-124">Properties in Windows Forms Controls</span></span>](properties-in-windows-forms-controls.md)
- [<span data-ttu-id="2f4b1-125">Definieren einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2f4b1-125">Defining a Property</span></span>](defining-a-property-in-windows-forms-controls.md)
- [<span data-ttu-id="2f4b1-126">Durch geänderte Eigenschaften ausgelöste Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2f4b1-126">Property-Changed Events</span></span>](property-changed-events.md)
- <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute?displayProperty=fullName>
