---
title: 'Vorgehensweise: Bereitstellen einer Toolboxbitmap für ein Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Toolbox [Windows Forms], adding bitmaps for custom controls
- custom controls [Windows Forms], Toolbox bitmaps
- bitmaps [Windows Forms], custom controls
ms.assetid: 0ed0840a-616d-41ba-a27d-3573241932ad
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: bb4ccc3b95dc69606a33074f21ee66aa5efda55b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974780"
---
# <a name="how-to-provide-a-toolbox-bitmap-for-a-control"></a><span data-ttu-id="593a2-102">Vorgehensweise: Bereitstellen einer Toolboxbitmap für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="593a2-102">How to: Provide a Toolbox Bitmap for a Control</span></span>

<span data-ttu-id="593a2-103">Wenn Sie ein spezielles Symbol für das Steuerelement in der **Toolbox** von Visual Studio anzeigen möchten, können Sie ein bestimmtes Bild mithilfe von angeben <xref:System.Drawing.ToolboxBitmapAttribute> .</span><span class="sxs-lookup"><span data-stu-id="593a2-103">If you want to have a special icon for your control appear in the **Toolbox** of Visual Studio, you can specify a particular image by using the <xref:System.Drawing.ToolboxBitmapAttribute>.</span></span> <span data-ttu-id="593a2-104">Diese Klasse ist ein *Attribut*, eine besondere Klassenform, die Sie an andere Klassen anfügen können.</span><span class="sxs-lookup"><span data-stu-id="593a2-104">This class is an *attribute*, a special kind of class you can attach to other classes.</span></span> <span data-ttu-id="593a2-105">Weitere Informationen zu Attributen finden Sie unter [Übersicht über Attribute (Visual Basic)](/dotnet/visual-basic/programming-guide/concepts/attributes/index) für Visual Basic oder [Attribute (c#)](/dotnet/csharp/programming-guide/concepts/attributes/index) für c#.</span><span class="sxs-lookup"><span data-stu-id="593a2-105">For more information about attributes, see [Attributes overview (Visual Basic)](/dotnet/visual-basic/programming-guide/concepts/attributes/index) for Visual Basic or [Attributes (C#)](/dotnet/csharp/programming-guide/concepts/attributes/index) for C#.</span></span>

<span data-ttu-id="593a2-106">Mithilfe des <xref:System.Drawing.ToolboxBitmapAttribute> können Sie eine Zeichenfolge angeben, die den Pfad und den Dateinamen für eine 16 x 16 Pixel-Bitmap angibt.</span><span class="sxs-lookup"><span data-stu-id="593a2-106">Using the <xref:System.Drawing.ToolboxBitmapAttribute>, you can specify a string that indicates the path and file name for a 16 by 16 pixel bitmap.</span></span> <span data-ttu-id="593a2-107">Diese Bitmap wird dann neben dem Steuerelement angezeigt, wenn sie zur **Toolbox** hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="593a2-107">This bitmap then appears next to your control when added to the **Toolbox**.</span></span> <span data-ttu-id="593a2-108">Sie können auch einen angeben <xref:System.Type> . in diesem Fall wird die Bitmap geladen, die diesem Typ zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="593a2-108">You can also specify a <xref:System.Type>, in which case the bitmap associated with that type is loaded.</span></span> <span data-ttu-id="593a2-109">Wenn Sie sowohl eine <xref:System.Type> als auch eine Zeichenfolge angeben, sucht das Steuerelement nach einer Bildressource mit dem Namen, der durch den Zeichen folgen Parameter in der Assembly angegeben ist, die den vom-Parameter angegebenen Typ enthält <xref:System.Type> .</span><span class="sxs-lookup"><span data-stu-id="593a2-109">If you specify both a <xref:System.Type> and a string, the control searches for an image resource with the name specified by the string parameter in the assembly containing the type specified by the <xref:System.Type> parameter.</span></span>

## <a name="to-specify-a-toolbox-bitmap-for-your-control"></a><span data-ttu-id="593a2-110">So geben sie eine Toolboxbitmap für Ihr Steuerelement an</span><span class="sxs-lookup"><span data-stu-id="593a2-110">To specify a Toolbox bitmap for your control</span></span>

1. <span data-ttu-id="593a2-111">Fügen Sie der <xref:System.Drawing.ToolboxBitmapAttribute> Klassen Deklaration Ihres Steuer Elements vor dem `Class` -Schlüsselwort für Visual Basic und oberhalb der Klassen Deklaration für Visual c# hinzu.</span><span class="sxs-lookup"><span data-stu-id="593a2-111">Add the <xref:System.Drawing.ToolboxBitmapAttribute> to the class declaration of your control before the `Class` keyword for visual Basic, and above the class declaration for Visual C#.</span></span>

    ```vb
    ' Specifies the bitmap associated with the Button type.
    <ToolboxBitmap(GetType(Button))> Class MyControl1
    ' Specifies a bitmap file.
    End Class
    <ToolboxBitmap("C:\Documents and Settings\Joe\MyPics\myImage.bmp")> _
       Class MyControl2
    End Class
    ' Specifies a type that indicates the assembly to search, and the name
    ' of an image resource to look for.
    <ToolboxBitmap(GetType(MyControl), "MyControlBitmap")> Class MyControl
    End Class
    ```

    ```csharp
    // Specifies the bitmap associated with the Button type.
    [ToolboxBitmap(typeof(Button))]
    class MyControl1 : UserControl
    {
    }
    // Specifies a bitmap file.
    [ToolboxBitmap(@"C:\Documents and Settings\Joe\MyPics\myImage.bmp")]
    class MyControl2 : UserControl
    {
    }
    // Specifies a type that indicates the assembly to search, and the name
    // of an image resource to look for.
    [ToolboxBitmap(typeof(MyControl), "MyControlBitmap")]
    class MyControl : UserControl
    {
    }
    ```

2. <span data-ttu-id="593a2-112">Erstellen Sie das Projekt neu.</span><span class="sxs-lookup"><span data-stu-id="593a2-112">Rebuild the project.</span></span>

    > [!NOTE]
    > <span data-ttu-id="593a2-113">Die Bitmap wird nicht in der Toolbox für automatisch generierte Steuerelemente und Komponenten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="593a2-113">The bitmap does not appear in the Toolbox for autogenerated controls and components.</span></span> <span data-ttu-id="593a2-114">Laden Sie das Steuerelement mithilfe des Dialogfelds **Toolboxelemente auswählen** neu, um die Bitmap anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="593a2-114">To see the bitmap, reload the control by using the **Choose Toolbox Items** dialog box.</span></span> <span data-ttu-id="593a2-115">Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise: Automatisches Füllen der Toolbox mit benutzerdefinierten Komponenten](walkthrough-automatically-populating-the-toolbox-with-custom-components.md).</span><span class="sxs-lookup"><span data-stu-id="593a2-115">For more information, see [Walkthrough: Automatically Populating the Toolbox with Custom Components](walkthrough-automatically-populating-the-toolbox-with-custom-components.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="593a2-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="593a2-116">See also</span></span>

- <xref:System.Drawing.ToolboxBitmapAttribute>
- [<span data-ttu-id="593a2-117">Exemplarische Vorgehensweise: Automatisches Füllen der Toolbox mit benutzerdefinierten Komponenten</span><span class="sxs-lookup"><span data-stu-id="593a2-117">Walkthrough: Automatically Populating the Toolbox with Custom Components</span></span>](walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
- [<span data-ttu-id="593a2-118">Entwickeln von Windows Forms-Steuerelementen zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="593a2-118">Developing Windows Forms Controls at Design Time</span></span>](developing-windows-forms-controls-at-design-time.md)
- [<span data-ttu-id="593a2-119">Übersicht über Attribute (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="593a2-119">Attributes overview (Visual Basic)</span></span>](/dotnet/visual-basic/programming-guide/concepts/attributes/index)
- [<span data-ttu-id="593a2-120">Attribute (C#)</span><span class="sxs-lookup"><span data-stu-id="593a2-120">Attributes (C#)</span></span>](/dotnet/csharp/programming-guide/concepts/attributes/index)
