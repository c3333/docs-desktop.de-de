---
title: Attribute in Steuerelementen
ms.date: 03/30/2017
ms.topic: overview
helpviewer_keywords:
- attributes [Windows Forms]
- attributes [Windows Forms], data binding properties
- attributes [Windows Forms], control properties
- attributes [Windows Forms], classes
ms.assetid: 2c5640e9-6c6c-49d7-a5e4-a768f6be7853
ms.openlocfilehash: 8f60b30021e6418f2ebf53965b62043e46e202b4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975151"
---
# <a name="attributes-in-windows-forms-controls"></a><span data-ttu-id="9d844-102">Attribute in Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="9d844-102">Attributes in Windows Forms Controls</span></span>

<span data-ttu-id="9d844-103">Das .NET Framework bietet eine Vielzahl von Attributen, die Sie auf die Member der benutzerdefinierten Steuerelemente und Komponenten anwenden können.</span><span class="sxs-lookup"><span data-stu-id="9d844-103">The .NET Framework provides a variety of attributes you can apply to the members of your custom controls and components.</span></span> <span data-ttu-id="9d844-104">Einige dieser Attribute haben Auswirkungen auf das Laufzeitverhalten einer Klasse, während andere Auswirkungen auf das Entwurfszeitverhalten haben.</span><span class="sxs-lookup"><span data-stu-id="9d844-104">Some of these attributes affect the run-time behavior of a class, and others affect the design-time behavior.</span></span>  
  
## <a name="attributes-for-control-and-component-properties"></a><span data-ttu-id="9d844-105">Attribute für Steuerelement- und Komponenteneigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d844-105">Attributes for Control and Component Properties</span></span>  

 <span data-ttu-id="9d844-106">Die folgende Tabelle enthält die Attribute, die Sie auf Eigenschaften oder andere Member der benutzerdefinierten Steuerelemente und Komponenten anwenden können.</span><span class="sxs-lookup"><span data-stu-id="9d844-106">The following table shows the attributes you can apply to properties or other members of your custom controls and components.</span></span> <span data-ttu-id="9d844-107">Ein Beispiel, in dem viele dieser Attribute verwendet werden, finden Sie unter [Vorgehensweise: Anwenden von Attributen auf Windows Forms-Steuerelemente](how-to-apply-attributes-in-windows-forms-controls.md).</span><span class="sxs-lookup"><span data-stu-id="9d844-107">For an example that uses many of these attributes, see [How to: Apply Attributes in Windows Forms Controls](how-to-apply-attributes-in-windows-forms-controls.md).</span></span>  
  
|<span data-ttu-id="9d844-108">attribute</span><span class="sxs-lookup"><span data-stu-id="9d844-108">Attribute</span></span>|<span data-ttu-id="9d844-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d844-109">Description</span></span>|  
|---------------|-----------------|  
|<xref:System.ComponentModel.AmbientValueAttribute>|<span data-ttu-id="9d844-110">Gibt den Wert an, der an eine Eigenschaft übergeben werden soll, damit die Eigenschaft den zugehörigen Wert von einer anderen Quelle abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="9d844-110">Specifies the value to pass to a property to cause the property to get its value from another source.</span></span> <span data-ttu-id="9d844-111">Dies wird als *Umgebung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9d844-111">This is known as *ambience*.</span></span>|  
|<xref:System.ComponentModel.BrowsableAttribute>|<span data-ttu-id="9d844-112">Gibt an, ob eine Eigenschaft oder ein Ereignis in einem **Eigenschaften** Fenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d844-112">Specifies whether a property or event should be displayed in a **Properties** window.</span></span>|  
|<xref:System.ComponentModel.CategoryAttribute>|<span data-ttu-id="9d844-113">Gibt den Namen der Kategorie an, in der die Eigenschaft oder das Ereignis gruppiert werden soll, wenn Sie in einem- <xref:System.Windows.Forms.PropertyGrid> Steuerelement festgelegt ist <xref:System.Windows.Forms.PropertySort.Categorized> .</span><span class="sxs-lookup"><span data-stu-id="9d844-113">Specifies the name of the category in which to group the property or event when displayed in a <xref:System.Windows.Forms.PropertyGrid> control set to <xref:System.Windows.Forms.PropertySort.Categorized> mode.</span></span>|  
|<xref:System.ComponentModel.DefaultValueAttribute>|<span data-ttu-id="9d844-114">Gibt den Standardwert für eine Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="9d844-114">Specifies the default value for a property.</span></span>|  
|<xref:System.ComponentModel.DescriptionAttribute>|<span data-ttu-id="9d844-115">Gibt die Beschreibung einer Eigenschaft oder eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="9d844-115">Specifies a description for a property or event.</span></span>|  
|<xref:System.ComponentModel.DisplayNameAttribute>|<span data-ttu-id="9d844-116">Gibt den Anzeigenamen für eine Eigenschaft, ein Ereignis oder eine `public void`-Methode an, die keine Argumente akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="9d844-116">Specifies the display name for a property, event, or `public void` method that takes no arguments.</span></span>|  
|<xref:System.ComponentModel.EditorAttribute>|<span data-ttu-id="9d844-117">Gibt den Editor an, der zum Ändern einer Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d844-117">Specifies the editor to use to change a property.</span></span>|  
|<xref:System.ComponentModel.EditorBrowsableAttribute>|<span data-ttu-id="9d844-118">Gibt an, dass eine Eigenschaft oder Methode in einem Editor angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9d844-118">Specifies that a property or method is viewable in an editor.</span></span>|  
|<xref:System.ComponentModel.Design.HelpKeywordAttribute>|<span data-ttu-id="9d844-119">Gibt das Kontextschlüsselwort für eine Klasse oder ein Element an.</span><span class="sxs-lookup"><span data-stu-id="9d844-119">Specifies the context keyword for a class or member.</span></span>|  
|<xref:System.ComponentModel.LocalizableAttribute>|<span data-ttu-id="9d844-120">Gibt an, ob eine Eigenschaft lokalisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d844-120">Specifies whether a property should be localized.</span></span>|  
|<xref:System.ComponentModel.PasswordPropertyTextAttribute>|<span data-ttu-id="9d844-121">Gibt an, dass die Textdarstellung eines Objekts von Zeichen wie Sternchen verdeckt wird.</span><span class="sxs-lookup"><span data-stu-id="9d844-121">Indicates that an object's text representation is obscured by characters such as asterisks.</span></span>|  
|<xref:System.ComponentModel.ReadOnlyAttribute>|<span data-ttu-id="9d844-122">Gibt an, ob die Eigenschaft, an die dieses Attribut gebunden ist, schreibgeschützt ist oder ob zur Entwurfszeit Lese-/Schreibzugriff gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="9d844-122">Specifies whether the property this attribute is bound to is read-only or read/write at design time.</span></span>|  
|<xref:System.ComponentModel.RefreshPropertiesAttribute>|<span data-ttu-id="9d844-123">Gibt an, dass das Eigenschaftenraster aktualisiert werden sollte, wenn sich der zugehörige Eigenschaftswert ändert.</span><span class="sxs-lookup"><span data-stu-id="9d844-123">Indicates that the property grid should refresh when the associated property value changes.</span></span>|  
|<xref:System.ComponentModel.TypeConverterAttribute>|<span data-ttu-id="9d844-124">Gibt an, welcher Typ als Konverter für das Objekt verwendet werden sollte, an das dieses Attribut gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="9d844-124">Specifies what type to use as a converter for the object this attribute is bound to.</span></span>|  
  
## <a name="attributes-for-data-binding-properties"></a><span data-ttu-id="9d844-125">Attribute für Datenbindungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d844-125">Attributes for Data Binding Properties</span></span>  

 <span data-ttu-id="9d844-126">In der folgenden Tabelle werden die Attribute angezeigt, die Sie für die Angabe anwenden können, wie Ihre benutzerdefinierten Steuerelemente und Komponenten mit der Datenbindung interagieren.</span><span class="sxs-lookup"><span data-stu-id="9d844-126">The following table shows the attributes you can apply to specify how your custom controls and components interact with data binding.</span></span>  
  
|<span data-ttu-id="9d844-127">attribute</span><span class="sxs-lookup"><span data-stu-id="9d844-127">Attribute</span></span>|<span data-ttu-id="9d844-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d844-128">Description</span></span>|  
|---------------|-----------------|  
|<xref:System.ComponentModel.BindableAttribute>|<span data-ttu-id="9d844-129">Gibt an, ob eine Eigenschaft in der Regel für die Bindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d844-129">Specifies whether a property is typically used for binding.</span></span>|  
|<xref:System.ComponentModel.ComplexBindingPropertiesAttribute>|<span data-ttu-id="9d844-130">Gibt die Eigenschaften der Datenquelle und des Datenmembers für eine Komponente an.</span><span class="sxs-lookup"><span data-stu-id="9d844-130">Specifies the data source and data member properties for a component.</span></span>|  
|<xref:System.ComponentModel.DefaultBindingPropertyAttribute>|<span data-ttu-id="9d844-131">Gibt die Standardbindungseigenschaft für eine Komponente an.</span><span class="sxs-lookup"><span data-stu-id="9d844-131">Specifies the default binding property for a component.</span></span>|  
|<xref:System.ComponentModel.LookupBindingPropertiesAttribute>|<span data-ttu-id="9d844-132">Gibt die Eigenschaften der Datenquelle und des Datenmembers für eine Komponente an.</span><span class="sxs-lookup"><span data-stu-id="9d844-132">Specifies the data source and data member properties for a component.</span></span>|  
|<xref:System.ComponentModel.AttributeProviderAttribute>|<span data-ttu-id="9d844-133">Ermöglicht die Umleitung von Attributen.</span><span class="sxs-lookup"><span data-stu-id="9d844-133">Enables attribute redirection.</span></span>|  
  
## <a name="attributes-for-classes"></a><span data-ttu-id="9d844-134">Attribute für Klassen</span><span class="sxs-lookup"><span data-stu-id="9d844-134">Attributes for Classes</span></span>  

 <span data-ttu-id="9d844-135">In der folgenden Tabelle werden die Attribute angezeigt, die Sie anwenden können, um das Verhalten Ihrer benutzerdefinierten Steuerelemente und Komponenten zur Entwurfszeit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9d844-135">The following table shows the attributes you can apply to specify the behavior of your custom controls and components at design time.</span></span>  
  
|<span data-ttu-id="9d844-136">attribute</span><span class="sxs-lookup"><span data-stu-id="9d844-136">Attribute</span></span>|<span data-ttu-id="9d844-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d844-137">Description</span></span>|  
|---------------|-----------------|  
|<xref:System.ComponentModel.DefaultEventAttribute>|<span data-ttu-id="9d844-138">Gibt das Standardereignis für eine Komponente an.</span><span class="sxs-lookup"><span data-stu-id="9d844-138">Specifies the default event for a component.</span></span>|  
|<xref:System.ComponentModel.DefaultPropertyAttribute>|<span data-ttu-id="9d844-139">Gibt die Standardeigenschaft für eine Komponente an.</span><span class="sxs-lookup"><span data-stu-id="9d844-139">Specifies the default property for a component.</span></span>|  
|<xref:System.ComponentModel.DesignerAttribute>|<span data-ttu-id="9d844-140">Gibt die Klasse an, die zum Implementieren von Entwurfszeitdiensten für eine Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d844-140">Specifies the class used to implement design-time services for a component.</span></span>|  
|<xref:System.ComponentModel.DesignerCategoryAttribute>|<span data-ttu-id="9d844-141">Gibt an, dass der Designer für eine Klasse zu einer bestimmten Kategorie gehört.</span><span class="sxs-lookup"><span data-stu-id="9d844-141">Specifies that the designer for a class belongs to a certain category.</span></span>|  
|<xref:System.ComponentModel.ToolboxItemAttribute>|<span data-ttu-id="9d844-142">Stellt ein Attribut eines Werkzeugkastenelements dar.</span><span class="sxs-lookup"><span data-stu-id="9d844-142">Represents an attribute of a toolbox item.</span></span>|  
|<xref:System.ComponentModel.ToolboxItemFilterAttribute>|<span data-ttu-id="9d844-143">Gibt die Filterzeichenfolge und den Filtertyp an, die für ein Werkzeugkastenelement verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9d844-143">Specifies the filter string and filter type to use for a Toolbox item.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9d844-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d844-144">See also</span></span>

- <xref:System.Attribute>
- [<span data-ttu-id="9d844-145">Vorgehensweise: Anwenden von Attributen auf Windows Forms-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9d844-145">How to: Apply Attributes in Windows Forms Controls</span></span>](how-to-apply-attributes-in-windows-forms-controls.md)
- <span data-ttu-id="9d844-146">[Erweitern der Entwurfszeitunterstützung](/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="9d844-146">[Extending Design-Time Support](/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))</span></span>
- [<span data-ttu-id="9d844-147">Entwickeln benutzerdefinierter Windows Forms-Steuerelemente mit .NET Framework</span><span class="sxs-lookup"><span data-stu-id="9d844-147">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](developing-custom-windows-forms-controls.md)
