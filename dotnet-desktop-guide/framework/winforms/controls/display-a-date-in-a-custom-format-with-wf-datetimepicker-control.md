---
title: Anzeigen eines Datums in einem benutzerdefinierten Format mit dem DateTimePicker-Steuerelement
description: Erfahren Sie, wie Sie das Windows Forms DateTimePicker-Steuerelement verwenden, um die Anzeige von Datumsangaben und Uhrzeiten im Steuerelement zu formatieren.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- DateTimePicker control [Windows Forms], display styles
- examples [Windows Forms], DateTimePicker control
- dates [Windows Forms], displaying in DateTimePicker control
ms.assetid: 39767691-2d2b-46b6-a663-b7901e581a6e
ms.openlocfilehash: 773070136e4fd43ab1bf510ebcaf6b0aa6a7ba8a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972116"
---
# <a name="how-to-display-a-date-in-a-custom-format-with-the-windows-forms-datetimepicker-control"></a><span data-ttu-id="dd83a-103">Vorgehensweise: Anzeigen eines Datums im benutzerdefinierten Format mit dem DateTimePicker-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="dd83a-103">How to: Display a Date in a Custom Format with the Windows Forms DateTimePicker Control</span></span>
<span data-ttu-id="dd83a-104">Das Windows Forms <xref:System.Windows.Forms.DateTimePicker> Steuerelement bietet Ihnen Flexibilität beim Formatieren der Anzeige von Datums-und Uhrzeitangaben im-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="dd83a-104">The Windows Forms <xref:System.Windows.Forms.DateTimePicker> control gives you flexibility in formatting the display of dates and times in the control.</span></span> <span data-ttu-id="dd83a-105">Die- <xref:System.Windows.Forms.DateTimePicker.Format%2A> Eigenschaft ermöglicht es Ihnen, aus vordefinierten Formaten auszuwählen, die im aufgeführt sind <xref:System.Windows.Forms.DateTimePickerFormat> .</span><span class="sxs-lookup"><span data-stu-id="dd83a-105">The <xref:System.Windows.Forms.DateTimePicker.Format%2A> property allows you to select from predefined formats, listed in the <xref:System.Windows.Forms.DateTimePickerFormat>.</span></span> <span data-ttu-id="dd83a-106">Wenn keines dieser Funktionen für Ihre Zwecke geeignet ist, können Sie mithilfe der in aufgeführten Formatzeichen einen eigenen Format Stil erstellen <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A> .</span><span class="sxs-lookup"><span data-stu-id="dd83a-106">If none of these is adequate for your purposes, you can create your own format style using format characters listed in <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A>.</span></span>  
  
### <a name="to-display-a-custom-format"></a><span data-ttu-id="dd83a-107">Anzeigen eines benutzerdefinierten Formats</span><span class="sxs-lookup"><span data-stu-id="dd83a-107">To display a custom format</span></span>  
  
1. <span data-ttu-id="dd83a-108">Legen Sie die <xref:System.Windows.Forms.DateTimePicker.Format%2A> -Eigenschaft auf `DateTimePickerFormat.Custom`fest.</span><span class="sxs-lookup"><span data-stu-id="dd83a-108">Set the <xref:System.Windows.Forms.DateTimePicker.Format%2A> property to `DateTimePickerFormat.Custom`.</span></span>  
  
2. <span data-ttu-id="dd83a-109">Legen <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A> Sie die Eigenschaft auf eine Format Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="dd83a-109">Set the <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A> property to a format string.</span></span>  
  
    ```vb  
    DateTimePicker1.Format = DateTimePickerFormat.Custom  
    ' Display the date as "Mon 27 Feb 2012".  
    DateTimePicker1.CustomFormat = "ddd dd MMM yyyy"  
    ```  
  
    ```csharp  
    dateTimePicker1.Format = DateTimePickerFormat.Custom;  
    // Display the date as "Mon 27 Feb 2012".  
    dateTimePicker1.CustomFormat = "ddd dd MMM yyyy";  
    ```  
  
    ```cpp  
    dateTimePicker1->Format = DateTimePickerFormat::Custom;  
    // Display the date as "Mon 27 Feb 2012".  
    dateTimePicker1->CustomFormat = "ddd dd MMM yyyy";  
    ```  
  
### <a name="to-add-text-to-the-formatted-value"></a><span data-ttu-id="dd83a-110">So fügen Sie dem formatierten Wert Text hinzu</span><span class="sxs-lookup"><span data-stu-id="dd83a-110">To add text to the formatted value</span></span>  
  
1. <span data-ttu-id="dd83a-111">Verwenden Sie einfache Anführungszeichen, um ein beliebiges Zeichen, das kein Formatzeichen wie "M" ist, oder ein Trennzeichen wie ":" einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="dd83a-111">Use single quotation marks to enclose any character that is not a format character like "M" or a delimiter like ":".</span></span> <span data-ttu-id="dd83a-112">Die Format Zeichenfolge unten zeigt z. b. das aktuelle Datum mit dem Format "Today is: 05:30:31 Friday March 02, 2012" in der Kultur Englisch (USA) an.</span><span class="sxs-lookup"><span data-stu-id="dd83a-112">For example, the format string below displays the current date with the format "Today is: 05:30:31 Friday March 02, 2012" in the English (United States) culture.</span></span>  
  
    ```vb  
    DateTimePicker1.CustomFormat = "'Today is:' hh:mm:ss dddd MMMM dd, yyyy"  
    ```  
  
    ```csharp  
    dateTimePicker1.CustomFormat = "'Today is:' hh:mm:ss dddd MMMM dd, yyyy";  
    ```  
  
    ```cpp  
    dateTimePicker1->CustomFormat =  
       "'Today is:' hh:mm:ss dddd MMMM dd, yyyy";  
    ```  
  
     <span data-ttu-id="dd83a-113">Abhängig von der Kultur Einstellung können alle Zeichen, die nicht in einfache Anführungszeichen eingeschlossen sind, geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dd83a-113">Depending on the culture setting, any characters not enclosed in single quotation marks may be changed.</span></span> <span data-ttu-id="dd83a-114">Die obige Format Zeichenfolge zeigt z. b. das aktuelle Datum mit dem Format "Today is: 05:30:31 Friday March 02, 2012" in der Kultur Englisch (USA) an.</span><span class="sxs-lookup"><span data-stu-id="dd83a-114">For example, the format string above displays the current date with the format "Today is: 05:30:31 Friday March 02, 2012" in the English (United States) culture.</span></span> <span data-ttu-id="dd83a-115">Beachten Sie, dass der erste Doppelpunkt in einfache Anführungszeichen eingeschlossen ist, da er nicht als Trennzeichen verwendet werden soll, da er sich in "hh: mm: SS" befindet.</span><span class="sxs-lookup"><span data-stu-id="dd83a-115">Note that the first colon is enclosed in single quotation marks, because it is not intended to be a delimiting character as it is in "hh:mm:ss".</span></span> <span data-ttu-id="dd83a-116">In einer anderen Kultur wird das Format möglicherweise als "heute ist: 05.30.31 Freitag, 02, 2012" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd83a-116">In another culture, the format might appear as "Today is: 05.30.31 Friday March 02, 2012".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd83a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd83a-117">See also</span></span>

- [<span data-ttu-id="dd83a-118">DateTimePicker-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="dd83a-118">DateTimePicker Control</span></span>](datetimepicker-control-windows-forms.md)
- [<span data-ttu-id="dd83a-119">Vorgehensweise: Festlegen und Zurückgeben von Datumsangaben mit dem DateTimePicker-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="dd83a-119">How to: Set and Return Dates with the Windows Forms DateTimePicker Control</span></span>](how-to-set-and-return-dates-with-the-windows-forms-datetimepicker-control.md)
