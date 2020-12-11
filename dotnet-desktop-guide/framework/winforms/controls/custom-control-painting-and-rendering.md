---
title: Zeichnen und Ausgeben von benutzerdefinierten Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], rendering
- custom controls [Windows Forms], painting
- user controls [Windows Forms], painting
ms.assetid: a09dbf76-0966-4cbf-a66a-2083ba98e068
ms.openlocfilehash: 14abac5678bfffa3cdb61307fd3cb54681c82a99
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972198"
---
# <a name="custom-control-painting-and-rendering"></a><span data-ttu-id="2a9ff-102">Zeichnen und Ausgeben von benutzerdefinierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="2a9ff-102">Custom Control Painting and Rendering</span></span>
<span data-ttu-id="2a9ff-103">Das benutzerdefinierte Zeichnen von Steuerelementen ist eine der vielen komplizierten Aufgaben, die durch die .NET Framework einfach gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-103">Custom painting of controls is one of the many complicated tasks made easy by the .NET Framework.</span></span> <span data-ttu-id="2a9ff-104">Wenn Sie ein benutzerdefiniertes Steuerelement erstellen, stehen Ihnen viele Optionen hinsichtlich der grafischen Darstellung des Steuer Elements zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-104">When authoring a custom control, you have many options regarding your control's graphical appearance.</span></span> <span data-ttu-id="2a9ff-105">Wenn Sie ein Steuerelement erstellen, das von erbt `Control` , müssen Sie Code bereitstellen, der es dem Steuerelement ermöglicht, seine grafische Darstellung zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-105">If you are authoring a control that inherits from the `Control`, you must provide code that allows your control to render its graphical representation.</span></span> <span data-ttu-id="2a9ff-106">Wenn Sie ein Benutzer Steuerelement erstellen, indem Sie von Erben `UserControl` , oder von einem der Windows Forms Steuerelemente erben, können Sie die grafische Standarddarstellung überschreiben und ihren eigenen Grafik Code bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-106">If you are creating a user control by inheriting from the `UserControl`, or are inheriting from one of the Windows Forms controls, you may override the standard graphical representation and provide your own graphics code.</span></span> <span data-ttu-id="2a9ff-107">Wenn Sie ein benutzerdefiniertes Rendering für die konstituierenden Steuerelemente einer erstellen möchten `UserControl` , die Sie erstellen, werden die Optionen eingeschränkt, aber Sie können dennoch eine große Bandbreite grafischer Möglichkeiten für Ihre Steuerelemente und Anwendungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-107">If you want to provide custom rendering for the constituent controls of a `UserControl` you are authoring, your options become more limited, but still allow a wide range of graphical possibilities for your controls and applications.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2a9ff-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2a9ff-108">In This Section</span></span>  
 [<span data-ttu-id="2a9ff-109">Wiedergeben eines Windows Forms-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="2a9ff-109">Rendering a Windows Forms Control</span></span>](rendering-a-windows-forms-control.md)  
 <span data-ttu-id="2a9ff-110">Zeigt, wie die Logik programmiert wird, die ein-Steuerelement anzeigt.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-110">Shows how to program the logic that displays a control.</span></span>  
  
 [<span data-ttu-id="2a9ff-111">Benutzerdefinierte Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="2a9ff-111">User-Drawn Controls</span></span>](user-drawn-controls.md)  
 <span data-ttu-id="2a9ff-112">Bietet einen Überblick über die Schritte zum Schreiben und Überschreiben von Renderingcode für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-112">Gives an overview of the steps involved in writing and overriding rendering code for your control.</span></span>  
  
 [<span data-ttu-id="2a9ff-113">Konstituierende Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="2a9ff-113">Constituent Controls</span></span>](constituent-controls.md)  
 <span data-ttu-id="2a9ff-114">Beschreibt, wie benutzerdefinierter Renderingcode für konstituierende Steuerelemente in den Benutzer Steuerelementen und Formularen implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-114">Describes how to implement custom rendering code for constituent controls in your user controls and forms.</span></span>  
  
 [<span data-ttu-id="2a9ff-115">Vorgehensweise: Ausblenden des Steuerelements zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="2a9ff-115">How to: Make Your Control Invisible at Run Time</span></span>](how-to-make-your-control-invisible-at-run-time.md)  
 <span data-ttu-id="2a9ff-116">Zeigt, wie die <xref:System.Windows.Forms.Control.Visible%2A> -Eigenschaft verwendet wird, um ein Steuerelement auszublenden und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-116">Shows how to use the <xref:System.Windows.Forms.Control.Visible%2A> property to hide and show a control.</span></span>  
  
 [<span data-ttu-id="2a9ff-117">Vorgehensweise: Verwenden eines transparenten Hintergrunds für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="2a9ff-117">How to: Give Your Control a Transparent Background</span></span>](how-to-give-your-control-a-transparent-background.md)  
 <span data-ttu-id="2a9ff-118">Zeigt, wie die- <xref:System.Windows.Forms.Control.SetStyle%2A> Methode verwendet wird, um eine nicht transparente, transparente oder teilweise transparente Hintergrundfarbe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-118">Shows how to use the <xref:System.Windows.Forms.Control.SetStyle%2A> method to create a background color that is opaque, transparent, or partially transparent.</span></span>  
  
 [<span data-ttu-id="2a9ff-119">Rendering von Steuerelementen mit visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="2a9ff-119">Rendering Controls with Visual Styles</span></span>](rendering-controls-with-visual-styles.md)  
 <span data-ttu-id="2a9ff-120">Veranschaulicht das Rendering von Steuerelementen mit visuellen Stilen in Betriebssystemen, die diese unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-120">Shows how to render controls using visual styles in operating systems that support them.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="2a9ff-121">Verweis</span><span class="sxs-lookup"><span data-stu-id="2a9ff-121">Reference</span></span>  
 <xref:System.Windows.Forms.Control>  
 <span data-ttu-id="2a9ff-122">Beschreibt diese Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-122">Describes this class and has links to all of its members.</span></span>  
  
 <xref:System.Windows.Forms.UserControl>  
 <span data-ttu-id="2a9ff-123">Beschreibt diese Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-123">Describes this class and has links to all of its members.</span></span>  
  
 <xref:System.Windows.Forms.Control.OnPaint%2A>  
 <span data-ttu-id="2a9ff-124">Beschreibt diese Methode.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-124">Describes this method.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="2a9ff-125">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="2a9ff-125">Related Sections</span></span>  
 [<span data-ttu-id="2a9ff-126">Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen</span><span class="sxs-lookup"><span data-stu-id="2a9ff-126">How to: Create Graphics Objects for Drawing</span></span>](../advanced/how-to-create-graphics-objects-for-drawing.md)  
 <span data-ttu-id="2a9ff-127">Stellt die GDI+-Grafik Funktionalität aus einer Visual Studio-Perspektive vor und enthält Links zu weiteren Informationen.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-127">Introduces GDI+ graphics functionality from a Visual Studio perspective and gives links to more information.</span></span>  
  
 [<span data-ttu-id="2a9ff-128">Arten von benutzerdefinierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="2a9ff-128">Varieties of Custom Controls</span></span>](varieties-of-custom-controls.md)  
 <span data-ttu-id="2a9ff-129">Beschreibt die Arten von benutzerdefinierten Steuerelementen, die Sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="2a9ff-129">Describes the kinds of custom controls you can author.</span></span>
