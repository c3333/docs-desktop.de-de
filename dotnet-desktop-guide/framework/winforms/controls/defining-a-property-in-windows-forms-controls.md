---
title: Definieren von Steuerelement Eigenschaften
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- properties [Windows Forms], defining in code
- custom controls [Windows Forms], defining properties in code
ms.assetid: c2eb8277-a842-4d99-89a9-647b901a0434
ms.openlocfilehash: ef81818123e78c50ade9f700a3acdbea1c5551b4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972152"
---
# <a name="defining-a-property-in-windows-forms-controls"></a><span data-ttu-id="bdce4-102">Definieren einer Eigenschaft in Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="bdce4-102">Defining a Property in Windows Forms Controls</span></span>

<span data-ttu-id="bdce4-103">Eine Übersicht über Eigenschaften finden Sie unter [Übersicht über Eigenschaften](/previous-versions/visualstudio/visual-studio-2013/65zdfbdt(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="bdce4-103">For an overview of properties, see [Properties Overview](/previous-versions/visualstudio/visual-studio-2013/65zdfbdt(v=vs.120)).</span></span> <span data-ttu-id="bdce4-104">Es gibt einige wichtige Überlegungen beim Definieren einer Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="bdce4-104">There are a few important considerations when defining a property:</span></span>  
  
- <span data-ttu-id="bdce4-105">Sie müssen auf die Eigenschaften, die Sie definieren, Attribute anwenden.</span><span class="sxs-lookup"><span data-stu-id="bdce4-105">You must apply attributes to the properties you define.</span></span> <span data-ttu-id="bdce4-106">Attribute geben an, wie der Designer eine Eigenschaft anzeigen sollte.</span><span class="sxs-lookup"><span data-stu-id="bdce4-106">Attributes specify how the designer should display a property.</span></span> <span data-ttu-id="bdce4-107">Einzelheiten hierzu finden Sie unter [Attribute für Komponenten in der Entwurfszeit](/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="bdce4-107">For details, see [Design-Time Attributes for Components](/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120)).</span></span>  
  
- <span data-ttu-id="bdce4-108">Wenn sich die Änderung der-Eigenschaft auf die visuelle Darstellung des Steuer Elements auswirkt, müssen Sie die- <xref:System.Windows.Forms.Control.Invalidate%2A> Methode (die von Ihrem Steuerelement erbt <xref:System.Windows.Forms.Control> ) aus der-Zugriffsmethode aufrufen `set` .</span><span class="sxs-lookup"><span data-stu-id="bdce4-108">If changing the property affects the visual display of the control, call the <xref:System.Windows.Forms.Control.Invalidate%2A> method (that your control inherits from <xref:System.Windows.Forms.Control>) from the `set` accessor.</span></span> <span data-ttu-id="bdce4-109"><xref:System.Windows.Forms.Control.Invalidate%2A> Ruft wiederum die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode auf, die das-Steuerelement neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="bdce4-109"><xref:System.Windows.Forms.Control.Invalidate%2A> in turn calls the <xref:System.Windows.Forms.Control.OnPaint%2A> method, which redraws the control.</span></span> <span data-ttu-id="bdce4-110">Mehrere Aufrufe von <xref:System.Windows.Forms.Control.Invalidate%2A> führen zu einem einzigen Aufruf <xref:System.Windows.Forms.Control.OnPaint%2A> von aus Gründen der Effizienz.</span><span class="sxs-lookup"><span data-stu-id="bdce4-110">Multiple calls to <xref:System.Windows.Forms.Control.Invalidate%2A> result in a single call to <xref:System.Windows.Forms.Control.OnPaint%2A> for efficiency.</span></span>  
  
- <span data-ttu-id="bdce4-111">Die .NET Framework-Klassenbibliothek stellt Typkonverter für häufig verwendete Datentypen wie z.B. ganze Zahlen, Dezimalzahlen, boolesche Werte und andere bereit.</span><span class="sxs-lookup"><span data-stu-id="bdce4-111">The .NET Framework class library provides type converters for common data types such as integers, decimal numbers, Boolean values, and others.</span></span> <span data-ttu-id="bdce4-112">Der Zweck eines Typkonverters ist im Allgemeinen, die Konvertierung von einer Zeichenfolge in einen Wert (von Zeichenfolgedaten in andere Datentypen) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bdce4-112">The purpose of a type converter is generally to provide string-to-value conversion (from string data to other data types).</span></span> <span data-ttu-id="bdce4-113">Allgemeine Datentypen sind Standardtypkonverter, die Werte in Zeichenfolgen und Zeichenfolgen in die entsprechenden Datentypen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="bdce4-113">Common data types are associated with default type converters that convert values into strings and strings into the appropriate data types.</span></span> <span data-ttu-id="bdce4-114">Wenn Sie eine Eigenschaft definieren (d.h. nicht dem Standard entsprechend), die einen benutzerdefinierten Datentyp aufweist, müssen Sie ein Attribut anwenden, das den dieser Eigenschaft zuzuordnenden Typkonverter angibt.</span><span class="sxs-lookup"><span data-stu-id="bdce4-114">If you define a property that is a custom (that is, nonstandard) data type, you will have to apply an attribute that specifies the type converter to associate with that property.</span></span> <span data-ttu-id="bdce4-115">Sie können ein Attribut auch verwenden, um einer Eigenschaft einen benutzerdefinierten Typeditor für die Benutzeroberfläche zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="bdce4-115">You can also use an attribute to associate a custom UI type editor with a property.</span></span> <span data-ttu-id="bdce4-116">Ein Typeditor für die Benutzeroberfläche stellt eine Benutzeroberfläche für die Bearbeitung einer Eigenschaft oder eines Datentyps bereit.</span><span class="sxs-lookup"><span data-stu-id="bdce4-116">A UI type editor provides a user interface for editing a property or data type.</span></span> <span data-ttu-id="bdce4-117">So ist beispielsweise ein Farbwähler ein Typeditor für die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="bdce4-117">A color picker is an example of a UI type editor.</span></span> <span data-ttu-id="bdce4-118">Beispiele für Attribute werden am Ende dieses Themas angegeben.</span><span class="sxs-lookup"><span data-stu-id="bdce4-118">Examples of attributes are given at the end of this topic.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="bdce4-119">Wenn für Ihre benutzerdefinierte Eigenschaft kein Typkonverter oder Typeditor für die Benutzeroberfläche verfügbar ist, können Sie einen implementieren, wie unter [Erweitern der Entwurfszeitunterstützung](/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="bdce4-119">If a type converter or a UI type editor is not available for your custom property, you can implement one as described in [Extending Design-Time Support](/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120)).</span></span>  
  
 <span data-ttu-id="bdce4-120">Das folgende Codefragment definiert eine benutzerdefinierte Eigenschaft mit dem Namen `EndColor` für das benutzerdefinierte Steuerelement `FlashTrackBar`.</span><span class="sxs-lookup"><span data-stu-id="bdce4-120">The following code fragment defines a custom property named `EndColor` for the custom control `FlashTrackBar`.</span></span>  
  
```vb  
Public Class FlashTrackBar  
   Inherits Control  
   ...  
   ' Private data member that backs the EndColor property.  
   Private _endColor As Color = Color.LimeGreen  
  
   ' The Category attribute tells the designer to display  
   ' it in the Flash grouping.
   ' The Description attribute provides a description of  
   ' the property.
   <Category("Flash"), _  
   Description("The ending color of the bar.")>  _  
   Public Property EndColor() As Color  
      ' The public property EndColor accesses _endColor.  
      Get  
         Return _endColor  
      End Get  
      Set  
         _endColor = value  
         If Not (baseBackground Is Nothing) And showGradient Then  
            baseBackground.Dispose()  
            baseBackground = Nothing  
         End If  
         ' The Invalidate method calls the OnPaint method, which redraws
         ' the control.  
         Invalidate()  
      End Set  
   End Property  
   ...  
End Class  
```  
  
```csharp  
public class FlashTrackBar : Control {  
   ...  
   // Private data member that backs the EndColor property.  
   private Color endColor = Color.LimeGreen;  
   // The Category attribute tells the designer to display  
   // it in the Flash grouping.
   // The Description attribute provides a description of  
   // the property.
   [  
   Category("Flash"),  
   Description("The ending color of the bar.")  
   ]  
   // The public property EndColor accesses endColor.  
   public Color EndColor {  
      get {  
         return endColor;  
      }  
      set {  
         endColor = value;  
         if (baseBackground != null && showGradient) {  
            baseBackground.Dispose();  
            baseBackground = null;  
         }  
         // The Invalidate method calls the OnPaint method, which redraws
         // the control.  
         Invalidate();  
      }  
   }  
   ...  
}  
```  
  
 <span data-ttu-id="bdce4-121">Das folgende Codefragment ordnet der Eigenschaft `Value` einen Typkonverter und einen Typeditor für die Benutzeroberfläche zu.</span><span class="sxs-lookup"><span data-stu-id="bdce4-121">The following code fragment associates a type converter and a UI type editor with the property `Value`.</span></span> <span data-ttu-id="bdce4-122">In diesem Fall `Value` ist eine ganze Zahl, die über einen Standardtyp Konverter verfügt, aber das- <xref:System.ComponentModel.TypeConverterAttribute> Attribut wendet einen benutzerdefinierten Typkonverter ( `FlashTrackBarValueConverter` ) an, der es dem Designer ermöglicht, ihn als Prozentsatz anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bdce4-122">In this case `Value` is an integer and has a default type converter, but the <xref:System.ComponentModel.TypeConverterAttribute> attribute applies a custom type converter (`FlashTrackBarValueConverter`) that enables the designer to display it as a percentage.</span></span> <span data-ttu-id="bdce4-123">Im Typeditor für die Benutzeroberfläche, `FlashTrackBarValueEditor`, kann der Prozentwert visuell angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bdce4-123">The UI type editor, `FlashTrackBarValueEditor`, allows the percentage to be displayed visually.</span></span> <span data-ttu-id="bdce4-124">Dieses Beispiel zeigt auch, dass der vom-oder-Attribut angegebene Typkonverter oder Editor <xref:System.ComponentModel.TypeConverterAttribute> <xref:System.ComponentModel.EditorAttribute> den Standard Konverter überschreibt.</span><span class="sxs-lookup"><span data-stu-id="bdce4-124">This example also shows that the type converter or editor specified by the <xref:System.ComponentModel.TypeConverterAttribute> or <xref:System.ComponentModel.EditorAttribute> attribute overrides the default converter.</span></span>  
  
```vb  
<Category("Flash"), _  
TypeConverter(GetType(FlashTrackBarValueConverter)), _  
Editor(GetType(FlashTrackBarValueEditor), _  
GetType(UITypeEditor)), _  
Description("The current value of the track bar.  You can enter an actual value or a percentage.")>  _  
Public ReadOnly Property Value() As Integer  
...  
End Property  
```  
  
```csharp  
[  
Category("Flash"),
TypeConverter(typeof(FlashTrackBarValueConverter)),  
Editor(typeof(FlashTrackBarValueEditor), typeof(UITypeEditor)),  
Description("The current value of the track bar.  You can enter an actual value or a percentage.")  
]  
public int Value {  
...  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="bdce4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdce4-125">See also</span></span>

- [<span data-ttu-id="bdce4-126">Eigenschaften von Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="bdce4-126">Properties in Windows Forms Controls</span></span>](properties-in-windows-forms-controls.md)
- [<span data-ttu-id="bdce4-127">Definieren von Standardwerten mit der ShouldSerialize-Methode und der Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="bdce4-127">Defining Default Values with the ShouldSerialize and Reset Methods</span></span>](defining-default-values-with-the-shouldserialize-and-reset-methods.md)
- [<span data-ttu-id="bdce4-128">Durch geänderte Eigenschaften ausgelöste Ereignisse</span><span class="sxs-lookup"><span data-stu-id="bdce4-128">Property-Changed Events</span></span>](property-changed-events.md)
- [<span data-ttu-id="bdce4-129">Attribute in Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="bdce4-129">Attributes in Windows Forms Controls</span></span>](attributes-in-windows-forms-controls.md)
