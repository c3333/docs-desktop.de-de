---
title: 'Vorgehensweise: Verwenden von Modifizierern und GenerateMember-Eigenschaften'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- Designer_GenerateMember
- Designer_Modifiers
helpviewer_keywords:
- base forms
- inheritance [Windows Forms], forms
- inherited forms [Windows Forms], Windows Forms
- inherited forms
- form inheritance
- Windows Forms, inheritance
ms.assetid: 3381a5e4-e1a3-44e2-a765-a0b758937b85
ms.openlocfilehash: 3fbaaae53aa60f6356c3a8daa0513de86ef2dacb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975853"
---
# <a name="how-to-use-the-modifiers-and-generatemember-properties"></a><span data-ttu-id="0c35b-102">Vorgehensweise: Verwenden von Modifizierern und GenerateMember-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c35b-102">How to: Use the Modifiers and GenerateMember Properties</span></span>

<span data-ttu-id="0c35b-103">Wenn Sie eine Komponente in einem Windows Form platzieren, werden zwei Eigenschaften von der Entwurfs Umgebung bereitgestellt: `GenerateMember` und `Modifiers` .</span><span class="sxs-lookup"><span data-stu-id="0c35b-103">When you place a component on a Windows Form, two properties are provided by the design environment: `GenerateMember` and `Modifiers`.</span></span> <span data-ttu-id="0c35b-104">Die- `GenerateMember` Eigenschaft gibt an, wann die Windows Forms-Designer eine Element Variable für eine Komponente generiert.</span><span class="sxs-lookup"><span data-stu-id="0c35b-104">The `GenerateMember` property specifies when the Windows Forms Designer generates a member variable for a component.</span></span> <span data-ttu-id="0c35b-105">Die `Modifiers` Eigenschaft ist der Zugriffsmodifizierer, der dieser Element Variablen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0c35b-105">The `Modifiers` property is the access modifier assigned to that member variable.</span></span> <span data-ttu-id="0c35b-106">Wenn der Wert der- `GenerateMember` Eigenschaft ist `false` , hat der Wert der- `Modifiers` Eigenschaft keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="0c35b-106">If the value of the `GenerateMember` property is `false`, the value of the `Modifiers` property has no effect.</span></span>

## <a name="specify-whether-a-component-is-a-member-of-the-form"></a><span data-ttu-id="0c35b-107">Geben Sie an, ob eine Komponente ein Member des Formulars ist.</span><span class="sxs-lookup"><span data-stu-id="0c35b-107">Specify whether a component is a member of the form</span></span>

1. <span data-ttu-id="0c35b-108">Öffnen Sie in Visual Studio im Windows Forms-Designer das Formular.</span><span class="sxs-lookup"><span data-stu-id="0c35b-108">In Visual Studio, in the Windows Forms Designer, open your form.</span></span>

2. <span data-ttu-id="0c35b-109">Öffnen Sie die **Toolbox**, und platzieren Sie im Formular drei-Steuer <xref:System.Windows.Forms.Button> Elemente.</span><span class="sxs-lookup"><span data-stu-id="0c35b-109">Open the **Toolbox**, and on the form, place three <xref:System.Windows.Forms.Button> controls.</span></span>

3. <span data-ttu-id="0c35b-110">Legen `GenerateMember` Sie die `Modifiers` Eigenschaften und für jedes <xref:System.Windows.Forms.Button> Steuerelement entsprechend der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="0c35b-110">Set the `GenerateMember` and `Modifiers` properties for each <xref:System.Windows.Forms.Button> control according to the following table.</span></span>

    |<span data-ttu-id="0c35b-111">Schaltflächenname</span><span class="sxs-lookup"><span data-stu-id="0c35b-111">Button name</span></span>|<span data-ttu-id="0c35b-112">GenerateMember-Wert</span><span class="sxs-lookup"><span data-stu-id="0c35b-112">GenerateMember value</span></span>|<span data-ttu-id="0c35b-113">Modifiziererwert</span><span class="sxs-lookup"><span data-stu-id="0c35b-113">Modifiers value</span></span>|
    |-----------------|--------------------------|---------------------|
    |`button1`|`true`|`private`|
    |`button2`|`true`|`protected`|
    |`button3`|`false`|<span data-ttu-id="0c35b-114">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="0c35b-114">No change</span></span>|

4. <span data-ttu-id="0c35b-115">Erstellen Sie die Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="0c35b-115">Build the solution.</span></span>

5. <span data-ttu-id="0c35b-116">Klicken Sie im **Projektmappen-Explorer** auf die Schaltfläche **Alle Dateien anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="0c35b-116">In **Solution Explorer**, click the **Show All Files** button.</span></span>

6. <span data-ttu-id="0c35b-117">Öffnen Sie den Knoten **Form1** , und öffnen Sie im **Code-Editor** die Datei **Form1. Designer. vb** oder **Form1.Designer.cs** .</span><span class="sxs-lookup"><span data-stu-id="0c35b-117">Open the **Form1** node, and in the **Code Editor**,open the **Form1.Designer.vb** or **Form1.Designer.cs** file.</span></span> <span data-ttu-id="0c35b-118">Diese Datei enthält den Code, der vom Windows Forms-Designer ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0c35b-118">This file contains the code emitted by the Windows Forms Designer.</span></span>

7. <span data-ttu-id="0c35b-119">Suchen Sie die Deklarationen für die drei Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="0c35b-119">Find the declarations for the three buttons.</span></span> <span data-ttu-id="0c35b-120">Das folgende Codebeispiel zeigt die Unterschiede, die in den `GenerateMember` Eigenschaften und angegeben sind `Modifiers` .</span><span class="sxs-lookup"><span data-stu-id="0c35b-120">The following code example shows the differences specified by the `GenerateMember` and `Modifiers` properties.</span></span>

     [!code-csharp[System.Windows.Forms.GenerateMember#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.GenerateMember#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/VB/Form1.vb#3)]

     [!code-csharp[System.Windows.Forms.GenerateMember#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.GenerateMember#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/VB/Form1.vb#2)]

> [!NOTE]
> <span data-ttu-id="0c35b-121">Standardmäßig weist das-Windows Forms-Designer `private` Container Steuer `Friend` Elementen wie den-Modifizierer (in Visual Basic) zu <xref:System.Windows.Forms.Panel> .</span><span class="sxs-lookup"><span data-stu-id="0c35b-121">By default, the Windows Forms Designer assigns the `private` (`Friend` in Visual Basic) modifier to container controls like <xref:System.Windows.Forms.Panel>.</span></span> <span data-ttu-id="0c35b-122">Wenn Ihre Basis <xref:System.Windows.Forms.UserControl> oder <xref:System.Windows.Forms.Form> ein Container Steuerelement enthält, werden keine neuen untergeordneten Elemente in geerbten Steuerelementen und Formularen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="0c35b-122">If your base <xref:System.Windows.Forms.UserControl> or <xref:System.Windows.Forms.Form> has a container control, it will not accept new children in inherited controls and forms.</span></span> <span data-ttu-id="0c35b-123">Die Lösung besteht darin, den-Modifizierer des Basis Container-Steuer Elements in oder zu ändern `protected` `public` .</span><span class="sxs-lookup"><span data-stu-id="0c35b-123">The solution is to change the modifier of the base container control to `protected` or `public`.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c35b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c35b-124">See also</span></span>

- <xref:System.Windows.Forms.Button>
- [<span data-ttu-id="0c35b-125">Visuelle Vererbung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0c35b-125">Windows Forms Visual Inheritance</span></span>](windows-forms-visual-inheritance.md)
- [<span data-ttu-id="0c35b-126">Exemplarische Vorgehensweise: Demonstrieren der visuellen Vererbung</span><span class="sxs-lookup"><span data-stu-id="0c35b-126">Walkthrough: Demonstrating Visual Inheritance</span></span>](walkthrough-demonstrating-visual-inheritance.md)
- [<span data-ttu-id="0c35b-127">Vorgehensweise: Erben von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0c35b-127">How to: Inherit Windows Forms</span></span>](how-to-inherit-windows-forms.md)
