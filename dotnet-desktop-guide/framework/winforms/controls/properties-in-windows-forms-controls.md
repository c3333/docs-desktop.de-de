---
title: Eigenschaften von Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], properties overview (using code)
- controls [Windows Forms], properties
- properties [Windows Forms]
ms.assetid: 2785279b-fb57-4937-8f6b-2050e475db6f
ms.openlocfilehash: 3f9873ff032497a9cda6de199ed9db5ee9522d81
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972340"
---
# <a name="properties-in-windows-forms-controls"></a><span data-ttu-id="8f03c-102">Eigenschaften von Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="8f03c-102">Properties in Windows Forms Controls</span></span>

<span data-ttu-id="8f03c-103">Ein Windows Forms-Steuerelement erbt viele Eigenschaften aus der Basisklasse <xref:System.Windows.Forms.Control?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="8f03c-103">A Windows Forms control inherits many properties form the base class <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="8f03c-104">Hierzu gehören Eigenschaften wie <xref:System.Windows.Forms.Control.Font%2A> , <xref:System.Windows.Forms.Control.ForeColor%2A> , <xref:System.Windows.Forms.Control.BackColor%2A> , <xref:System.Windows.Forms.Control.Bounds%2A> , <xref:System.Windows.Forms.Control.ClientRectangle%2A> , <xref:System.Windows.Forms.Control.DisplayRectangle%2A> ,,, <xref:System.Windows.Forms.Control.Enabled%2A> <xref:System.Windows.Forms.Control.Focused%2A> <xref:System.Windows.Forms.Control.Height%2A> , <xref:System.Windows.Forms.Control.Width%2A> , <xref:System.Windows.Forms.Control.Visible%2A> , <xref:System.Windows.Forms.Control.AutoSize%2A> und viele andere.</span><span class="sxs-lookup"><span data-stu-id="8f03c-104">These include properties such as <xref:System.Windows.Forms.Control.Font%2A>, <xref:System.Windows.Forms.Control.ForeColor%2A>, <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.Bounds%2A>, <xref:System.Windows.Forms.Control.ClientRectangle%2A>, <xref:System.Windows.Forms.Control.DisplayRectangle%2A>, <xref:System.Windows.Forms.Control.Enabled%2A>, <xref:System.Windows.Forms.Control.Focused%2A>, <xref:System.Windows.Forms.Control.Height%2A>, <xref:System.Windows.Forms.Control.Width%2A>, <xref:System.Windows.Forms.Control.Visible%2A>, <xref:System.Windows.Forms.Control.AutoSize%2A>, and many others.</span></span> <span data-ttu-id="8f03c-105">Ausführliche Informationen zu geerbten Eigenschaften finden Sie unter <xref:System.Windows.Forms.Control?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="8f03c-105">For details about inherited properties, see <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span>  
  
 <span data-ttu-id="8f03c-106">Sie können geerbte Eigenschaften in Ihrem Steuerelement außer Kraft setzen oder neue Eigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="8f03c-106">You can override inherited properties in your control as well as define new properties.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="8f03c-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="8f03c-107">In This Section</span></span>  

 [<span data-ttu-id="8f03c-108">Definieren einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8f03c-108">Defining a Property</span></span>](defining-a-property-in-windows-forms-controls.md)  
 <span data-ttu-id="8f03c-109">Demonstriert das Implementieren einer Eigenschaft für ein benutzerdefiniertes Steuerelement oder eine Komponente und das Integrieren der Eigenschaft in die Entwurfsumgebung.</span><span class="sxs-lookup"><span data-stu-id="8f03c-109">Shows how to implement a property for a custom control or component and shows how to integrate the property into the design environment.</span></span>  
  
 [<span data-ttu-id="8f03c-110">Definieren von Standardwerten mit der ShouldSerialize-Methode und der Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="8f03c-110">Defining Default Values with the ShouldSerialize and Reset Methods</span></span>](defining-default-values-with-the-shouldserialize-and-reset-methods.md)  
 <span data-ttu-id="8f03c-111">Demonstriert das Definieren von Standardeigenschaftswerten für ein benutzerdefiniertes Steuerelement oder eine Komponente.</span><span class="sxs-lookup"><span data-stu-id="8f03c-111">Shows how to define default property values for a custom control or component.</span></span>  
  
 [<span data-ttu-id="8f03c-112">Durch geänderte Eigenschaften ausgelöste Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8f03c-112">Property-Changed Events</span></span>](property-changed-events.md)  
 <span data-ttu-id="8f03c-113">Beschreibt das Aktivieren von Benachrichtigungen über Eigenschaftsänderungen, wenn ein Eigenschaftswert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8f03c-113">Describes how to enable property-change notifications when a property value changes.</span></span>  
  
 [<span data-ttu-id="8f03c-114">Vorgehensweise: Verfügbarmachen der Eigenschaften konstituierender Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="8f03c-114">How to: Expose Properties of Constituent Controls</span></span>](how-to-expose-properties-of-constituent-controls.md)  
 <span data-ttu-id="8f03c-115">Veranschaulicht, wie man Eigenschaften von konstituierenden Steuerelementen in einem benutzerdefinierten zusammengesetzten Steuerelement verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="8f03c-115">Shows how to expose properties of constituent controls in a custom composite control.</span></span>  
  
 [<span data-ttu-id="8f03c-116">Implementierung von Methoden in benutzerdefinierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="8f03c-116">Method Implementation in Custom Controls</span></span>](method-implementation-in-custom-controls.md)  
 <span data-ttu-id="8f03c-117">Beschreibt die Implementierung von Methoden in benutzerdefinierten Steuerelementen und Komponenten.</span><span class="sxs-lookup"><span data-stu-id="8f03c-117">Describes how to implement methods in custom controls and components.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="8f03c-118">Verweis</span><span class="sxs-lookup"><span data-stu-id="8f03c-118">Reference</span></span>  

 <xref:System.Windows.Forms.UserControl>  
 <span data-ttu-id="8f03c-119">Dokumentiert die Basisklasse für das Implementieren von zusammengesetzten Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="8f03c-119">Documents the base class for implementing composite controls.</span></span>  
  
 <xref:System.ComponentModel.TypeConverterAttribute>  
 <span data-ttu-id="8f03c-120">Dokumentiert das Attribut, das angibt, <xref:System.ComponentModel.TypeConverter> welches für einen benutzerdefinierten Eigenschaftentyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f03c-120">Documents the attribute that specifies the <xref:System.ComponentModel.TypeConverter> to use for a custom property type.</span></span>  
  
 <xref:System.ComponentModel.EditorAttribute>  
 <span data-ttu-id="8f03c-121">Dokumentiert das-Attribut, das den angibt <xref:System.Drawing.Design.UITypeEditor> , der für eine benutzerdefinierte Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f03c-121">Documents the attribute that specifies the <xref:System.Drawing.Design.UITypeEditor> to use for a custom property.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="8f03c-122">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="8f03c-122">Related Sections</span></span>  

 [<span data-ttu-id="8f03c-123">Attribute in Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="8f03c-123">Attributes in Windows Forms Controls</span></span>](attributes-in-windows-forms-controls.md)  
 <span data-ttu-id="8f03c-124">Beschreibt die Attribute, die Sie auf Eigenschaften oder andere Member der benutzerdefinierten Steuerelemente und Komponenten anwenden können.</span><span class="sxs-lookup"><span data-stu-id="8f03c-124">Describes the attributes you can apply to properties or other members of your custom controls and components.</span></span>  
  
 <span data-ttu-id="8f03c-125">[Entwurfszeitattribute für Komponenten](/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="8f03c-125">[Design-Time Attributes for Components](/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120))</span></span>  
 <span data-ttu-id="8f03c-126">Listet die Metadatenattribute für Komponenten und Steuerelemente auf, damit sie in visuellen Designern zur Entwurfszeit korrekt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8f03c-126">Lists metadata attributes to apply to components and controls so that they are displayed correctly at design time in visual designers.</span></span>  
  
 <span data-ttu-id="8f03c-127">[Erweitern der Entwurfszeitunterstützung](/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="8f03c-127">[Extending Design-Time Support](/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))</span></span>  
 <span data-ttu-id="8f03c-128">Beschreibt die Implementierung von Klassen wie Editoren und Designern, die Entwurfszeitunterstützung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8f03c-128">Describes how to implement classes such as editors and designers that provide design-time support.</span></span>
