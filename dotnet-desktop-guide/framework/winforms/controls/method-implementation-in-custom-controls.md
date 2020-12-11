---
title: Implementierung von Methoden in benutzerdefinierten Steuerelementen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- user controls [Windows Forms], method implementation
- custom controls [Windows Forms], overloading methods
- custom controls [Windows Forms], method implementation
- methods [Windows Forms]
- methods [Windows Forms], custom controls
ms.assetid: 35d14fca-4bb4-4a27-8211-1f7a98ea27de
ms.openlocfilehash: 8541e38f3ccdf45a41c806e2d3d69ff1e8210daf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975545"
---
# <a name="method-implementation-in-custom-controls"></a><span data-ttu-id="113f3-102">Implementierung von Methoden in benutzerdefinierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="113f3-102">Method Implementation in Custom Controls</span></span>

<span data-ttu-id="113f3-103">Eine Methode wird genauso in ein Steuerelement implementiert, wie sie in eine beliebige andere Komponente implementiert würde.</span><span class="sxs-lookup"><span data-stu-id="113f3-103">A method is implemented in a control in the same manner a method would be implemented in any other component.</span></span>  
  
 <span data-ttu-id="113f3-104">Wenn es in Visual Basic erforderlich ist, dass eine Methode einen Wert zurückgibt, wird sie als `Public Function` implementiert.</span><span class="sxs-lookup"><span data-stu-id="113f3-104">In Visual Basic, if a method is required to return a value, it is implemented as a `Public Function`.</span></span> <span data-ttu-id="113f3-105">Wenn kein Wert zurückgegeben wird, wird sie als `Public Sub` implementiert.</span><span class="sxs-lookup"><span data-stu-id="113f3-105">If no value is returned, it is implemented as a `Public Sub`.</span></span> <span data-ttu-id="113f3-106">Methoden können mithilfe der folgenden Syntax deklariert werden:</span><span class="sxs-lookup"><span data-stu-id="113f3-106">Methods are declared using the following syntax:</span></span>  
  
```vb  
Public Function ConvertMatterToEnergy(Matter as Integer) As Integer  
   ' Conversion code goes here.  
End Function  
```  
  
 <span data-ttu-id="113f3-107">Da Funktionen einen Wert zurückgeben, müssen sie einen Rückgabetyp angeben, beispielsweise ganze Zahl, Zeichenfolge, Objekt usw.</span><span class="sxs-lookup"><span data-stu-id="113f3-107">Because functions return a value, they must specify a return type, such as integer, string, object, and so on.</span></span> <span data-ttu-id="113f3-108">Wenn `Function`-Prozeduren oder `Sub`-Prozeduren Argumente übernehmen, müssen diese ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="113f3-108">The arguments `Function` or `Sub` procedures take, if any, must also be specified.</span></span>  
  
 <span data-ttu-id="113f3-109">In C# wird nicht wie in Visual Basic zwischen Funktionen und Prozeduren unterschieden.</span><span class="sxs-lookup"><span data-stu-id="113f3-109">C# makes no distinction between functions and procedures, as Visual Basic does.</span></span> <span data-ttu-id="113f3-110">Von einer Methode wird entweder ein Wert oder `void` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="113f3-110">A method either returns a value or returns `void`.</span></span> <span data-ttu-id="113f3-111">Die Syntax zum Deklarieren einer öffentlichen C#-Methode lautet:</span><span class="sxs-lookup"><span data-stu-id="113f3-111">The syntax for declaring a C# public method is:</span></span>  
  
```csharp  
public int ConvertMatterToEnergy(int matter)  
{  
   // Conversion code goes here.  
}  
```  
  
 <span data-ttu-id="113f3-112">Wenn eine Methode deklariert wird, sollten, wenn möglich, alle ihre Argumente als explizite Datentypen deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="113f3-112">When you declare a method, declare all of its arguments as explicit data types whenever possible.</span></span> <span data-ttu-id="113f3-113">Argumente, die Objektverweise verwenden, sollten als spezielle Klassentypen deklariert werden, z. B. `As Widget` statt `As Object`.</span><span class="sxs-lookup"><span data-stu-id="113f3-113">Arguments that take object references should be declared as specific class types — for example, `As Widget` instead of `As Object`.</span></span> <span data-ttu-id="113f3-114">In Visual Basic wird die Einhaltung dieser Regel mit der Standardeinstellung `Option Strict` automatisch erzwungen.</span><span class="sxs-lookup"><span data-stu-id="113f3-114">In Visual Basic, the default setting `Option Strict` automatically enforces this rule.</span></span>  
  
 <span data-ttu-id="113f3-115">Mit typisierten Argumenten ist es möglich, dass viele Entwicklerfehler bereits vom Compiler und nicht erst zur Laufzeit aufgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="113f3-115">Typed arguments allow many developer errors to be caught by the compiler, rather than at run time.</span></span> <span data-ttu-id="113f3-116">Fehler werden vom Compiler grundsätzlich aufgefangen, während die Qualität des Laufzeittests von der Art der Testreihe bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="113f3-116">The compiler always catches errors, whereas run-time testing is only as good as the test suite.</span></span>  
  
## <a name="overloaded-methods"></a><span data-ttu-id="113f3-117">Überladene Methoden</span><span class="sxs-lookup"><span data-stu-id="113f3-117">Overloaded Methods</span></span>  

 <span data-ttu-id="113f3-118">Wenn Benutzer des Steuerelements in der Lage sein sollen, verschiedene Kombinationen von Parametern für Methoden anzugeben, müssen mehrere Überladungen der Methode unter Verwendung expliziter Datentypen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="113f3-118">If you want to allow users of your control to supply different combinations of parameters to a method, provide multiple overloads of the method, using explicit data types.</span></span> <span data-ttu-id="113f3-119">Vermeiden Sie das Erstellen von Parametern, die als `As Object` deklariert sind und beliebige Datentypen enthalten können. Dies könnte zu Fehlern führen, die möglicherweise während des Testens nicht aufgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="113f3-119">Avoid creating parameters declared `As Object` that can contain any data type, as this can lead to errors that might not be caught in testing.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="113f3-120">Bei dem universellen Datentyp in der Common Language Runtime handelt es sich um `Object` und nicht um `Variant`.</span><span class="sxs-lookup"><span data-stu-id="113f3-120">The universal data type in the common language runtime is `Object` rather than `Variant`.</span></span> <span data-ttu-id="113f3-121">`Variant` wurde aus der Sprache entfernt.</span><span class="sxs-lookup"><span data-stu-id="113f3-121">`Variant` has been removed from the language.</span></span>  
  
 <span data-ttu-id="113f3-122">Mit der `Spin`-Methode eines hypothetischen `Widget`-Steuerelements könnte beispielsweise entweder die direkte Angabe der Richtung und Geschwindigkeit des Drehfelds oder die Angabe eines anderen `Widget`-Objekts ermöglicht werden, von dem das Drehmoment übernommen wird:</span><span class="sxs-lookup"><span data-stu-id="113f3-122">For example, the `Spin` method of a hypothetical `Widget` control might allow either direct specification of spin direction and speed, or specification of another `Widget` object from which angular momentum is to be absorbed:</span></span>  
  
```vb  
Overloads Public Sub Spin( _  
   ByVal SpinDirection As SpinDirectionsEnum, _  
   ByVal RevolutionsPerSecond As Double)  
   ' Implementation code here.  
End Sub  
Overloads Public Sub Spin(ByVal Driver As Widget) _  
   ' Implementation code here.  
End Sub  
```  
  
```csharp  
public void Spin(SpinDirectionsEnum spinDirection, double revolutionsPerSecond)  
{  
   // Implementation code here.  
}  
  
public void Spin(Widget driver)  
{  
   // Implementation code here.  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="113f3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="113f3-123">See also</span></span>

- [<span data-ttu-id="113f3-124">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="113f3-124">Events</span></span>](/dotnet/standard/events/index)
- [<span data-ttu-id="113f3-125">Eigenschaften von Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="113f3-125">Properties in Windows Forms Controls</span></span>](properties-in-windows-forms-controls.md)
