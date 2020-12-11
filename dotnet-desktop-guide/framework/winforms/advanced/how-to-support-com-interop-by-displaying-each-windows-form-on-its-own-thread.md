---
title: 'Vorgehensweise: Unterstützen von COM-Interop durch das Anzeigen einzelner Windows Forms in einem eigenen Thread'
ms.date: 03/30/2017
dev_langs:
- vb
helpviewer_keywords:
- COM interop [Windows Forms], Windows Forms
- COM [Windows Forms]
- Windows Forms, unmanaged
- ActiveX controls [Windows Forms], COM interop
- Windows Forms, interop
ms.assetid: a9e04765-d2de-4389-a494-a9a6d07aa6ee
ms.openlocfilehash: 074fc2d3fcfe1bf02bc6f6af65a3d9aed39fe786
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976115"
---
# <a name="how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread"></a><span data-ttu-id="5017c-102">Gewusst wie: unterstützen von COM-Interop durch Anzeigen jedes Windows Forms in einem eigenen Thread</span><span class="sxs-lookup"><span data-stu-id="5017c-102">How to: Support COM interop by displaying each Windows Form on its own thread</span></span>

<span data-ttu-id="5017c-103">Sie können Probleme mit der COM-Interoperabilität beheben, indem Sie das Formular in einer .NET Framework-Nachrichten Schleife anzeigen, die Sie mit der-Methode erstellen können <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="5017c-103">You can resolve COM interoperability problems by displaying your form on a .NET Framework message loop, which you can create by using the <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> method.</span></span>

<span data-ttu-id="5017c-104">Damit ein Windows Form aus einer COM-Clientanwendung heraus ordnungsgemäß funktioniert, müssen Sie das Formular in einer Windows Forms-Nachrichtenschleife ausführen.</span><span class="sxs-lookup"><span data-stu-id="5017c-104">To make a Windows Form work correctly from a COM client application, you must run the form on a Windows Forms message loop.</span></span> <span data-ttu-id="5017c-105">Hierzu können Sie einen der folgenden Ansätze verwenden:</span><span class="sxs-lookup"><span data-stu-id="5017c-105">To do this, use one of the following approaches:</span></span>

- <span data-ttu-id="5017c-106">Verwenden Sie die <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> -Methode, um das Windows Form anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5017c-106">Use the <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> method to display the Windows Form.</span></span> <span data-ttu-id="5017c-107">Weitere Informationen finden Sie unter [Vorgehensweise: Unterstützen von COM-Interop durch Anzeigen eines Windows Forms mit der ShowDialog-Methode](com-interop-by-displaying-a-windows-form-shadow.md).</span><span class="sxs-lookup"><span data-stu-id="5017c-107">For more information, see [How to: Support COM Interop by Displaying a Windows Form with the ShowDialog Method](com-interop-by-displaying-a-windows-form-shadow.md).</span></span>

- <span data-ttu-id="5017c-108">Zeigen Sie jedes Windows Form in einem separaten Thread an.</span><span class="sxs-lookup"><span data-stu-id="5017c-108">Display each Windows Form on a separate thread.</span></span>

<span data-ttu-id="5017c-109">In Visual Studio wird dieses Feature umfassend unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5017c-109">There is extensive support for this feature in Visual Studio.</span></span>

<span data-ttu-id="5017c-110">Siehe auch [Exemplarische Vorgehensweise: Unterstützen von COM-Interop durch das Anzeigen jedes Windows Forms in einem eigenen Thread](/previous-versions/visualstudio/visual-studio-2010/ms233639(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="5017c-110">Also see [Walkthrough: Supporting COM Interop by Displaying Each Windows Form on Its Own Thread](/previous-versions/visualstudio/visual-studio-2010/ms233639(v=vs.100)).</span></span>

## <a name="example"></a><span data-ttu-id="5017c-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5017c-111">Example</span></span>

<span data-ttu-id="5017c-112">Im folgenden Codebeispiel wird veranschaulicht, wie Sie das Formular über einen separaten Thread anzeigen und die <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> -Methode aufrufen, um ein Windows Forms-Nachrichtensystem über diesen Thread zu starten</span><span class="sxs-lookup"><span data-stu-id="5017c-112">The following code example demonstrates how to display the form on a separate thread and call the <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> method to start a Windows Forms message pump on that thread.</span></span> <span data-ttu-id="5017c-113">Um diesen Ansatz zu verwenden, müssen Sie jeden Aufruf des Formulars aus der nicht verwalteten Anwendung marshallen, indem Sie die <xref:System.Windows.Forms.Control.Invoke%2A> Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="5017c-113">To use this approach, you must marshal any calls to the form from the unmanaged application by using the <xref:System.Windows.Forms.Control.Invoke%2A> method.</span></span>

<span data-ttu-id="5017c-114">Dieser Ansatz erfordert, dass jede Instanz eines Formulars über ihren eigenen Thread ausgeführt wird, indem sie ihre eigene Nachrichtenschleife verwendet.</span><span class="sxs-lookup"><span data-stu-id="5017c-114">This approach requires that each instance of a form runs on its own thread by using its own message loop.</span></span> <span data-ttu-id="5017c-115">Es ist nicht möglich, mehrere Nachrichtenschleifen pro Thread auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5017c-115">You cannot have more than one message loop running per thread.</span></span> <span data-ttu-id="5017c-116">Daher können Sie die Nachrichtenschleife der Clientanwendung nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="5017c-116">Therefore, you cannot change the client application's message loop.</span></span> <span data-ttu-id="5017c-117">Sie können jedoch die .NET Framework Komponente ändern, um einen neuen Thread zu starten, der seine eigene Nachrichten Schleife verwendet.</span><span class="sxs-lookup"><span data-stu-id="5017c-117">However, you can modify the .NET Framework component to start a new thread that uses its own message loop.</span></span>

[!code-vb[System.Windows.Forms.ComInterop#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ComInterop/VB/COMForm.vb#1)]

[!code-vb[System.Windows.Forms.ComInterop#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ComInterop/VB/FormManager.vb#10)]

[!code-vb[System.Windows.Forms.ComInterop#100](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ComInterop/VB/Form1.vb#100)]

## <a name="compile-the-code"></a><span data-ttu-id="5017c-118">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="5017c-118">Compile the code</span></span>

<span data-ttu-id="5017c-119">Kompilieren Sie die Typen `COMForm`, `Form1`und `FormManager` in eine Assembly namens `COMWinform.dll`.</span><span class="sxs-lookup"><span data-stu-id="5017c-119">Compile the `COMForm`, `Form1`, and `FormManager` types into an assembly called `COMWinform.dll`.</span></span> <span data-ttu-id="5017c-120">Registrieren Sie die Assembly für COM-Interop, indem Sie eine der Methoden verwenden, die unter [Packaging an Assembly for COM](/dotnet/framework/interop/packaging-an-assembly-for-co)beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="5017c-120">Register the assembly for COM interop by using one of the methods described in [Packaging an Assembly for COM](/dotnet/framework/interop/packaging-an-assembly-for-co).</span></span> <span data-ttu-id="5017c-121">Sie können die Assembly und deren entsprechende Typbibliotheksdatei (.tlb) in nicht verwalteten Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5017c-121">You can now use the assembly and its corresponding type library (.tlb) file in unmanaged applications.</span></span> <span data-ttu-id="5017c-122">Beispielsweise können Sie die Typbibliothek als Verweis in einem ausführbaren Visual Basic 6.0-Projekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="5017c-122">For example, you can use the type library as a reference in a Visual Basic 6.0 executable project.</span></span>

## <a name="see-also"></a><span data-ttu-id="5017c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5017c-123">See also</span></span>

- [<span data-ttu-id="5017c-124">Verfügbarmachen von .NET Framework-Komponenten in COM</span><span class="sxs-lookup"><span data-stu-id="5017c-124">Exposing .NET Framework Components to COM</span></span>](/dotnet/framework/interop/exposing-dotnet-components-to-co)
- [<span data-ttu-id="5017c-125">Verpacken einer Assembly für COM</span><span class="sxs-lookup"><span data-stu-id="5017c-125">Packaging an Assembly for COM</span></span>](/dotnet/framework/interop/packaging-an-assembly-for-co)
- [<span data-ttu-id="5017c-126">Registrieren von Assemblys bei COM</span><span class="sxs-lookup"><span data-stu-id="5017c-126">Registering Assemblies with COM</span></span>](/dotnet/framework/interop/registering-assemblies-with-co)
- [<span data-ttu-id="5017c-127">Vorgehensweise: Unterstützen von COM-Interop durch Anzeigen eines Windows Forms mit der ShowDialog-Methode</span><span class="sxs-lookup"><span data-stu-id="5017c-127">How to: Support COM Interop by Displaying a Windows Form with the ShowDialog Method</span></span>](com-interop-by-displaying-a-windows-form-shadow.md)
- [<span data-ttu-id="5017c-128">Übersicht über Windows Forms und nicht verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="5017c-128">Windows Forms and Unmanaged Applications Overview</span></span>](windows-forms-and-unmanaged-applications-overview.md)
