---
title: Formular Vererbung
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- inherited forms [Windows Forms], creating at run-time
- inheritance [Windows Forms], forms
- Windows Forms, inheritance
ms.assetid: cb3e1c0f-3d2a-4cdc-b0d1-c92eae567ffb
ms.openlocfilehash: d016eb52802a729ef3b41a1140cae3d64022d403
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975906"
---
# <a name="how-to-inherit-windows-forms"></a><span data-ttu-id="9260b-102">Vorgehensweise: Erben von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9260b-102">How to: Inherit Windows Forms</span></span>

<span data-ttu-id="9260b-103">Das Erstellen neuer Windows Forms durch Vererbung der Eigenschaften der Basisformulare ist eine praktische Möglichkeit zum Duplizieren Ihrer Bemühungen, ohne ein Formular jedes Mal von Grund auf neu erstellen zu müssen, wenn Sie es benötigen.</span><span class="sxs-lookup"><span data-stu-id="9260b-103">Creating new Windows Forms by inheriting from base forms is a handy way to duplicate your best efforts without going through the process of entirely recreating a form every time you require it.</span></span>

<span data-ttu-id="9260b-104">Weitere Informationen zum Erben von Formularen zur Entwurfszeit mit dem Dialogfeld **Vererbungsauswahl** und zur visuellen Unterscheidung zwischen den Sicherheitsebenen der vererbten Steuerelemente finden Sie unter [Vorgehensweise: Erben von Formularen mithilfe des Dialogfelds „Vererbungsauswahl“](how-to-inherit-forms-using-the-inheritance-picker-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="9260b-104">For more information about inheriting forms at design time using the **Inheritance Picker** dialog box and how to visually distinguish between security levels of inherited controls, see [How to: Inherit Forms Using the Inheritance Picker Dialog Box](how-to-inherit-forms-using-the-inheritance-picker-dialog-box.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9260b-105">Um von einem Formular zu erben, muss die Datei oder der Namespace, die dieses Formular enthalten, in eine ausführbare Datei oder DLL integriert werden.</span><span class="sxs-lookup"><span data-stu-id="9260b-105">In order to inherit from a form, the file or namespace containing that form must have been built into an executable file or DLL.</span></span> <span data-ttu-id="9260b-106">Wählen Sie zum Erstellen des Projekts aus dem Menü **Erstellen** die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="9260b-106">To build the project, choose **Build** from the **Build** menu.</span></span> <span data-ttu-id="9260b-107">Darüber hinaus muss der Klasse, die das Formular erbt, auch ein Verweis auf den Namespace hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9260b-107">Also, a reference to the namespace must be added to the class inheriting the form.</span></span>

## <a name="inherit-a-form-programmatically"></a><span data-ttu-id="9260b-108">Programm gesteuertes Erben eines Formulars</span><span class="sxs-lookup"><span data-stu-id="9260b-108">Inherit a form programmatically</span></span>

1. <span data-ttu-id="9260b-109">Fügen Sie in der Klasse einen Verweis zu dem Namespace hinzu, der das Formular enthält, das vererbt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9260b-109">In your class, add a reference to the namespace containing the form you wish to inherit from.</span></span>

2. <span data-ttu-id="9260b-110">Fügen Sie in der Klassendefinition einen Verweis auf das Formular hinzu, das vererbt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9260b-110">In the class definition, add a reference to the form to inherit from.</span></span> <span data-ttu-id="9260b-111">Der Verweis sollte den Namespace enthalten, in dem sich das Formular befindet, gefolgt von einem Punkt und dem Namen des eigentlichen Formulars.</span><span class="sxs-lookup"><span data-stu-id="9260b-111">The reference should include the namespace that contains the form, followed by a period, then the name of the base form itself.</span></span>

    ```vb
    Public Class Form2
        Inherits Namespace1.Form1
    ```

    ```csharp
    public class Form2 : Namespace1.Form1
    ```

 <span data-ttu-id="9260b-112">Denken Sie beim Erben von Formularen daran, dass Probleme mit Ereignishandlern auftreten können, die zwei Mal aufgerufen werden, da jedes Ereignis sowohl von der Basisklasse als auch von der geerbten Klasse behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="9260b-112">When inheriting forms, keep in mind that issues may arise with regard to event handlers being called twice, because each event is being handled by both the base class and the inherited class.</span></span> <span data-ttu-id="9260b-113">Weitere Informationen dazu, wie Sie dieses Problem vermeiden können, finden Sie unter [Problembehandlung für geerbte Ereignishandler in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers).</span><span class="sxs-lookup"><span data-stu-id="9260b-113">For more information on how to avoid this problem, see [Troubleshooting Inherited Event Handlers in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers).</span></span>

## <a name="see-also"></a><span data-ttu-id="9260b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9260b-114">See also</span></span>

- [<span data-ttu-id="9260b-115">Inherits Statement</span><span class="sxs-lookup"><span data-stu-id="9260b-115">Inherits Statement</span></span>](/dotnet/visual-basic/language-reference/statements/inherits-statement)
- [<span data-ttu-id="9260b-116">Imports-Anweisung (.NET-Namespace und Typ)</span><span class="sxs-lookup"><span data-stu-id="9260b-116">Imports Statement (.NET Namespace and Type)</span></span>](/dotnet/visual-basic/language-reference/statements/imports-statement-net-namespace-and-type)
- [<span data-ttu-id="9260b-117">using</span><span class="sxs-lookup"><span data-stu-id="9260b-117">using</span></span>](/dotnet/csharp/language-reference/keywords/using)
- [<span data-ttu-id="9260b-118">Auswirkungen beim Ändern der Darstellung von Basisformularen</span><span class="sxs-lookup"><span data-stu-id="9260b-118">Effects of Modifying a Base Form's Appearance</span></span>](effects-of-modifying-base-form-appearance.md)
- [<span data-ttu-id="9260b-119">Visuelle Vererbung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9260b-119">Windows Forms Visual Inheritance</span></span>](windows-forms-visual-inheritance.md)
