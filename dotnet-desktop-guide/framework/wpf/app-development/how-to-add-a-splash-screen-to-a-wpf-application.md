---
title: Vorgehensweise beim Hinzufügen eines Begrüßungs Bildschirms
description: Erfahren Sie, wie Sie einer Windows Presentation Foundation (WPF)-Anwendung ein Startfenster oder einen Begrüßungsbildschirm hinzufügen.
ms.date: 08/18/2018
helpviewer_keywords:
- WPF [WPF], splash screen
- startup window [WPF]
- SplashScreen class [WPF]
- splash screen [WPF]
ms.assetid: d70a25c4-5fb9-4c27-b01d-b1b8ef39b3fd
ms.openlocfilehash: 99a20dca755b7fd066ed6068ed2efa4cca8acaa9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977129"
---
# <a name="how-to-add-a-splash-screen-to-a-wpf-application"></a><span data-ttu-id="b1733-103">Gewusst wie: Hinzufügen eines Begrüßungsbildschirms zu einer WPF-Anwendung</span><span class="sxs-lookup"><span data-stu-id="b1733-103">How to: Add a Splash Screen to a WPF Application</span></span>

<span data-ttu-id="b1733-104">In diesem Thema wird gezeigt, wie Sie einer Windows Presentation Foundation (WPF)-Anwendung ein Startfenster oder einen Begrüßungs *Bildschirm* hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b1733-104">This topic shows how to add a startup window, or *splash screen*, to a Windows Presentation Foundation (WPF) application.</span></span>

## <a name="to-add-an-existing-image-as-a-splash-screen"></a><span data-ttu-id="b1733-105">So fügen Sie ein vorhandenes Bild als Begrüßungsbildschirm hinzu</span><span class="sxs-lookup"><span data-stu-id="b1733-105">To add an existing image as a splash screen</span></span>

1. <span data-ttu-id="b1733-106">Erstellen oder suchen Sie ein Bild, das Sie für den Begrüßungsbildschirm verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b1733-106">Create or find an image that you want to use for the splash screen.</span></span> <span data-ttu-id="b1733-107">Sie können jedes beliebige Bildformat verwenden, das von der Windows Imaging Component (WIC) unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b1733-107">You can use any image format that is supported by the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="b1733-108">Beispielsweise können Sie das Format BMP, GIF, JPEG, PNG oder TIFF verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1733-108">For example, you can use the BMP, GIF, JPEG, PNG, or TIFF format.</span></span>

2. <span data-ttu-id="b1733-109">Fügen Sie die Bilddatei zum WPF-Anwendungsprojekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="b1733-109">Add the image file to the WPF Application project.</span></span>

3. <span data-ttu-id="b1733-110">Wählen Sie in **Projektmappen-Explorer** das Abbild aus.</span><span class="sxs-lookup"><span data-stu-id="b1733-110">In **Solution Explorer**, select the image.</span></span>

4. <span data-ttu-id="b1733-111">Klicken Sie im Eigenschaftenfenster auf den Dropdown Pfeil für die Eigenschaft **Buildaktion** .</span><span class="sxs-lookup"><span data-stu-id="b1733-111">In the Properties window, click the drop-down arrow for the **Build Action** property.</span></span>

5. <span data-ttu-id="b1733-112">Wählen Sie in der Dropdown Liste die Option **SplashScreen** aus.</span><span class="sxs-lookup"><span data-stu-id="b1733-112">Select **SplashScreen** from the drop-down list.</span></span>

6. <span data-ttu-id="b1733-113">Drücken Sie **F5**, um die Anwendung zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b1733-113">Press **F5** to build and run the application.</span></span>

     <span data-ttu-id="b1733-114">Das Bild mit dem Begrüßungsbildschirm wird in der Mitte des Bildschirms angezeigt und wird dann ausgeblendet, wenn das Hauptanwendungsfenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b1733-114">The splash screen image appears in the center of the screen, and then fades when the main application window appears.</span></span>

## <a name="to-exclude-the-splash-screen-from-build"></a><span data-ttu-id="b1733-115">So schließen Sie den Begrüßungsbildschirm vom Build aus</span><span class="sxs-lookup"><span data-stu-id="b1733-115">To exclude the splash screen from build</span></span>

1. <span data-ttu-id="b1733-116">Wählen Sie in **Projektmappen-Explorer** das Bild mit dem Begrüßungsbildschirm aus.</span><span class="sxs-lookup"><span data-stu-id="b1733-116">In **Solution Explorer**, select the splash screen image.</span></span>

2. <span data-ttu-id="b1733-117">Legen Sie im Fenster **Eigenschaften** die **Buildaktion** auf **None** fest.</span><span class="sxs-lookup"><span data-stu-id="b1733-117">In the **Properties** window, set the **Build Action** to **None**.</span></span>

## <a name="to-remove-the-splash-screen-from-an-application"></a><span data-ttu-id="b1733-118">So entfernen Sie den Begrüßungsbildschirm aus einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="b1733-118">To remove the splash screen from an application</span></span>

<span data-ttu-id="b1733-119">Löschen Sie in **Projektmappen-Explorer** das Bild des Begrüßungs Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="b1733-119">In **Solution Explorer**, delete the splash screen image.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1733-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1733-120">See also</span></span>

- <xref:System.Windows.SplashScreen>
- <span data-ttu-id="b1733-121">[Vorgehensweise: Hinzufügen vorhandener Elemente zu einem Projekt](/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="b1733-121">[How to: Add Existing Items to a Project](/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))</span></span>
