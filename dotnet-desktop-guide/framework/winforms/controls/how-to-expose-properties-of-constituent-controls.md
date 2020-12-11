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
# <a name="how-to-expose-properties-of-constituent-controls"></a><span data-ttu-id="62d72-102">Vorgehensweise: Verfügbarmachen der Eigenschaften konstituierender Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="62d72-102">How to: Expose Properties of Constituent Controls</span></span>
<span data-ttu-id="62d72-103">Die Steuerelemente, die ein zusammengesetztes Steuerelement bilden, sind *konstituierende Steuerelemente*.</span><span class="sxs-lookup"><span data-stu-id="62d72-103">The controls that make up a composite control are called *constituent controls*.</span></span> <span data-ttu-id="62d72-104">Diese Steuerelemente werden normalerweise als privat deklariert und können daher nicht vom Entwickler aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="62d72-104">These controls are normally declared private, and thus cannot be accessed by the developer.</span></span> <span data-ttu-id="62d72-105">Wenn Sie für zukünftige Benutzereigenschaften dieser Steuerelemente verfügbar machen möchten, müssen Sie Sie für den Benutzer verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="62d72-105">If you want to make properties of these controls available to future users, you must expose them to the user.</span></span> <span data-ttu-id="62d72-106">Eine Eigenschaft eines konstituierenden Steuer Elements wird verfügbar gemacht, indem eine Eigenschaft im Benutzer Steuerelement erstellt und der-Accessor und der-Accessor dieser Eigenschaft verwendet werden, `get` `set` um die Änderung in der private-Eigenschaft des konstituierenden Steuer Elements zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="62d72-106">A property of a constituent control is exposed by creating a property in the user control, and using the `get` and `set` accessors of that property to effect the change in the private property of the constituent control.</span></span>

 <span data-ttu-id="62d72-107">Stellen Sie sich ein hypothetisches Benutzer Steuerelement mit einer konstituierenden Schalt `MyButton` Fläche namens vor</span><span class="sxs-lookup"><span data-stu-id="62d72-107">Consider a hypothetical user control with a constituent button named `MyButton`.</span></span> <span data-ttu-id="62d72-108">In diesem Beispiel wird der Wert, der `ConstituentButtonBackColor` in der- <xref:System.Windows.Forms.Control.BackColor%2A> Eigenschaft von gespeichert ist, übermittelt `MyButton` , wenn der Benutzer die-Eigenschaft anfordert.</span><span class="sxs-lookup"><span data-stu-id="62d72-108">In this example, when the user requests the `ConstituentButtonBackColor` property, the value stored in the <xref:System.Windows.Forms.Control.BackColor%2A> property of `MyButton` is delivered.</span></span> <span data-ttu-id="62d72-109">Wenn der Benutzer dieser Eigenschaft einen Wert zuweist, wird dieser Wert automatisch an die <xref:System.Windows.Forms.Control.BackColor%2A> -Eigenschaft von übermittelt, `MyButton` und der `set` Code wird ausgeführt, und die Farbe von wird geändert `MyButton` .</span><span class="sxs-lookup"><span data-stu-id="62d72-109">When the user assigns a value to this property, that value is automatically passed to the <xref:System.Windows.Forms.Control.BackColor%2A> property of `MyButton` and the `set` code will execute, changing the color of `MyButton`.</span></span>

 <span data-ttu-id="62d72-110">Im folgenden Beispiel wird gezeigt, wie die- <xref:System.Windows.Forms.Control.BackColor%2A> Eigenschaft der konstituierenden Schaltfläche verfügbar gemacht wird:</span><span class="sxs-lookup"><span data-stu-id="62d72-110">The following example shows how to expose the <xref:System.Windows.Forms.Control.BackColor%2A> property of the constituent button:</span></span>

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

### <a name="to-expose-a-property-of-a-constituent-control"></a><span data-ttu-id="62d72-111">So machen Sie eine Eigenschaft eines konstituierenden Steuer Elements verfügbar</span><span class="sxs-lookup"><span data-stu-id="62d72-111">To expose a property of a constituent control</span></span>

1. <span data-ttu-id="62d72-112">Erstellen Sie eine öffentliche Eigenschaft für das Benutzer Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="62d72-112">Create a public property for your user control.</span></span>

2. <span data-ttu-id="62d72-113">`get`Schreiben Sie im-Abschnitt der-Eigenschaft Code, der den Wert der Eigenschaft abruft, die Sie verfügbar machen möchten.</span><span class="sxs-lookup"><span data-stu-id="62d72-113">In the `get` section of the property, write code that retrieves the value of the property you want to expose.</span></span>

3. <span data-ttu-id="62d72-114">`set`Schreiben Sie im-Abschnitt der-Eigenschaft Code, der den Wert der-Eigenschaft an die verfügbar gemachte-Eigenschaft des konstituierenden Steuer Elements übergibt.</span><span class="sxs-lookup"><span data-stu-id="62d72-114">In the `set` section of the property, write code that passes the value of the property to the exposed property of the constituent control.</span></span>

## <a name="see-also"></a><span data-ttu-id="62d72-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62d72-115">See also</span></span>

- <xref:System.Windows.Forms.UserControl>
- [<span data-ttu-id="62d72-116">Eigenschaften von Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="62d72-116">Properties in Windows Forms Controls</span></span>](properties-in-windows-forms-controls.md)
- [<span data-ttu-id="62d72-117">Arten von benutzerdefinierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="62d72-117">Varieties of Custom Controls</span></span>](varieties-of-custom-controls.md)
