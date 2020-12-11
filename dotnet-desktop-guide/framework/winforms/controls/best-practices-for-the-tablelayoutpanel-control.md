---
title: Empfohlene Vorgehensweisen für das TableLayoutPanel-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- layout [Windows Forms]
- TableLayoutPanel control [Windows Forms], best practices
- forms [Windows Forms], best practices
- AutoSize property [Windows Forms], tableLayoutPanel control
- controls [Windows Forms], sizing
- TableLayoutPanel control [Windows Forms], AutoSize behavior
- layout [Windows Forms], AutoSize
- layout [Windows Forms], best practices
- best practices [Windows Forms], tableLayoutPanel control
- sizing [Windows Forms], automatic
- automatic sizing
ms.assetid: b6706efb-d7a4-45ec-8cf4-08fa993e3afb
ms.openlocfilehash: e46d0fe6913bec61bd56199b7cb56a9b24d15bd0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975787"
---
# <a name="best-practices-for-the-tablelayoutpanel-control"></a><span data-ttu-id="35691-102">Empfohlene Vorgehensweisen für das TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="35691-102">Best Practices for the TableLayoutPanel Control</span></span>
<span data-ttu-id="35691-103">Das- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement bietet leistungsstarke Layoutfeatures, die Sie sorgfältig berücksichtigen sollten, bevor Sie Ihre Windows Forms verwenden.</span><span class="sxs-lookup"><span data-stu-id="35691-103">The <xref:System.Windows.Forms.TableLayoutPanel> control provides powerful layout features that you should consider carefully before using on your Windows Forms.</span></span>

## <a name="recommendations"></a><span data-ttu-id="35691-104">Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="35691-104">Recommendations</span></span>
 <span data-ttu-id="35691-105">Anhand der folgenden Empfehlungen können Sie das- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement optimal nutzen.</span><span class="sxs-lookup"><span data-stu-id="35691-105">The following recommendations will help you use the <xref:System.Windows.Forms.TableLayoutPanel> control to its best advantage.</span></span>

### <a name="targeted-use"></a><span data-ttu-id="35691-106">Gezielte Verwendung</span><span class="sxs-lookup"><span data-stu-id="35691-106">Targeted Use</span></span>
 <span data-ttu-id="35691-107">Verwenden Sie das <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement sparsam.</span><span class="sxs-lookup"><span data-stu-id="35691-107">Use the <xref:System.Windows.Forms.TableLayoutPanel> control sparingly.</span></span> <span data-ttu-id="35691-108">Diese sollten nicht in allen Situationen verwendet werden, in denen ein Layout in der Größe geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="35691-108">You should not use it in all situations that require a resizable layout.</span></span> <span data-ttu-id="35691-109">In der folgenden Liste werden Layouts beschrieben, die am meisten von der Verwendung des-Steuer Elements profitieren <xref:System.Windows.Forms.TableLayoutPanel> :</span><span class="sxs-lookup"><span data-stu-id="35691-109">The following list describes layouts that benefit most from the use of the <xref:System.Windows.Forms.TableLayoutPanel> control:</span></span>

- <span data-ttu-id="35691-110">Layouts, bei denen mehrere Teile des Formulars proportional zueinander angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="35691-110">Layouts in which there are multiple parts of the form that resize proportionally to each other.</span></span>

- <span data-ttu-id="35691-111">Layouts, die zur Laufzeit dynamisch geändert oder generiert werden, z. b. Dateneingabeformulare, die auf der Grundlage von Einstellungen Benutzer anpassbare Felder hinzugefügt oder subtrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="35691-111">Layouts that will be modified or generated dynamically at run time, such as data entry forms that have user-customizable fields added or subtracted based on preferences.</span></span>

- <span data-ttu-id="35691-112">Layouts, die in einer Gesamtgröße bleiben sollen.</span><span class="sxs-lookup"><span data-stu-id="35691-112">Layouts that should remain at an overall fixed size.</span></span> <span data-ttu-id="35691-113">Beispielsweise können Sie über ein Dialogfeld verfügen, das kleiner als 800 x 600 sein sollte, aber Sie müssen lokalisierte Zeichen folgen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="35691-113">For example, you may have a dialog box that should remain smaller than 800 x 600, but you need to support localized strings.</span></span>

 <span data-ttu-id="35691-114">In der folgenden Liste werden Layouts beschrieben, die von der Verwendung des Steuer Elements nicht stark profitieren <xref:System.Windows.Forms.TableLayoutPanel> :</span><span class="sxs-lookup"><span data-stu-id="35691-114">The following list describes layouts that do not benefit greatly from using the <xref:System.Windows.Forms.TableLayoutPanel> control:</span></span>

- <span data-ttu-id="35691-115">Einfache Dateneingabeformulare mit einer einzelnen Spalte von Bezeichnungen und einer einzelnen Spalte mit Texteingabe Bereichen.</span><span class="sxs-lookup"><span data-stu-id="35691-115">Simple data entry forms with a single column of labels and a single column of text-entry areas.</span></span>

- <span data-ttu-id="35691-116">Formulare mit einem einzelnen großen Anzeigebereich, der den gesamten verfügbaren Platz ausfüllen soll, wenn eine Größenänderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="35691-116">Forms with a single large display area that should fill all the available space when a resize occurs.</span></span> <span data-ttu-id="35691-117">Ein Beispiel hierfür ist ein Formular, das ein einzelnes Steuerelement anzeigt <xref:System.Windows.Forms.PropertyGrid> .</span><span class="sxs-lookup"><span data-stu-id="35691-117">An example of this is a form that displays a single <xref:System.Windows.Forms.PropertyGrid> control.</span></span> <span data-ttu-id="35691-118">Verwenden Sie in diesem Fall das verankern, da nichts anderes bei der Größenänderung des Formulars erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="35691-118">In this case, use anchoring, because nothing else should expand when the form is resized.</span></span>

 <span data-ttu-id="35691-119">Wählen Sie sorgfältig aus, welche Steuerelemente sich in einem Steuerelement befinden müssen <xref:System.Windows.Forms.TableLayoutPanel> .</span><span class="sxs-lookup"><span data-stu-id="35691-119">Choose carefully which controls need to be in a <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span> <span data-ttu-id="35691-120">Wenn Sie mit dem verankern Platz für Ihren Text um 30% vergrößern können, sollten Sie die- <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaft nur verwenden.</span><span class="sxs-lookup"><span data-stu-id="35691-120">If you have room for your text to grow by 30% using anchoring, consider using the <xref:System.Windows.Forms.Control.Anchor%2A> property only.</span></span> <span data-ttu-id="35691-121">Wenn Sie den für das Layout benötigten Speicherplatz einschätzen können, <xref:System.Windows.Forms.Control.Dock%2A> ist die Verwendung von und <xref:System.Windows.Forms.Control.Anchor%2A> einfacher als das Schätzen der Details des verbleibenden Speicherplatzes und des verbleibenden <xref:System.Windows.Forms.Control.AutoSize%2A> Verhaltens.</span><span class="sxs-lookup"><span data-stu-id="35691-121">If you can estimate the space required by your layout, use of <xref:System.Windows.Forms.Control.Dock%2A> and <xref:System.Windows.Forms.Control.Anchor%2A> is easier than estimating the details of remaining space and <xref:System.Windows.Forms.Control.AutoSize%2A> behavior.</span></span>

 <span data-ttu-id="35691-122">Im Allgemeinen sollten Sie beim Entwerfen des Layouts mit dem <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement den Entwurf so einfach wie möglich halten.</span><span class="sxs-lookup"><span data-stu-id="35691-122">In general, when designing your layout with the <xref:System.Windows.Forms.TableLayoutPanel> control, keep the design as simple as possible.</span></span>

### <a name="use-the-document-outline-window"></a><span data-ttu-id="35691-123">Verwenden des Dokument Gliederungs Fensters</span><span class="sxs-lookup"><span data-stu-id="35691-123">Use the Document Outline Window</span></span>
 <span data-ttu-id="35691-124">Das Dokument Gliederungs Fenster bietet eine Strukturansicht Ihres Layouts, mit der Sie die z-Reihenfolge und die Beziehungen zwischen übergeordneten und untergeordneten Elementen der Steuerelemente bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="35691-124">The Document Outline window gives you a tree view of your layout, which you can use to manipulate the z-order and parent-child relationships of your controls.</span></span> <span data-ttu-id="35691-125">Wählen Sie im **Menü Ansicht** die Option **Weitere Fenster**, und klicken Sie dann auf **Dokument** Gliederung.</span><span class="sxs-lookup"><span data-stu-id="35691-125">From the **View menu**, select **Other Windows**, then select **Document Outline**.</span></span>

### <a name="avoid-nesting"></a><span data-ttu-id="35691-126">Schachteln vermeiden</span><span class="sxs-lookup"><span data-stu-id="35691-126">Avoid Nesting</span></span>
 <span data-ttu-id="35691-127">Vermeiden Sie das Schachteln anderer <xref:System.Windows.Forms.TableLayoutPanel> Steuerelemente in einem <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="35691-127">Avoid nesting other <xref:System.Windows.Forms.TableLayoutPanel> controls within a <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span> <span data-ttu-id="35691-128">Das Debuggen von schsted Layouts kann schwierig sein.</span><span class="sxs-lookup"><span data-stu-id="35691-128">Debugging nested layouts can be difficult.</span></span>

### <a name="avoid-visual-inheritance"></a><span data-ttu-id="35691-129">Vermeiden der visuellen Vererbung</span><span class="sxs-lookup"><span data-stu-id="35691-129">Avoid Visual Inheritance</span></span>
 <span data-ttu-id="35691-130">Das- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement unterstützt keine visuelle Vererbung in der Windows Forms-Designer in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="35691-130">The <xref:System.Windows.Forms.TableLayoutPanel> control does not support visual inheritance in the Windows Forms Designer in Visual Studio.</span></span> <span data-ttu-id="35691-131">Ein <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement in einer abgeleiteten Klasse wird zur Entwurfszeit als "gesperrt" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35691-131">A <xref:System.Windows.Forms.TableLayoutPanel> control in a derived class appears as "locked" at design time.</span></span>

## <a name="see-also"></a><span data-ttu-id="35691-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35691-132">See also</span></span>

- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
