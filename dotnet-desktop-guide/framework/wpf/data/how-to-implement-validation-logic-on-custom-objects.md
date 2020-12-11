---
title: 'Gewusst wie: Implementieren von Validierungslogik für benutzerdefinierte Objekte'
ms.date: 08/02/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- checking for validation errors [WPF]
- validation errors [WPF], checking for
- implementing validation logic on custom objects [WPF]
- custom objects [WPF], implementing validation logic on
ms.assetid: 751fda9b-44f9-4d63-b4f2-1df07ac41e0f
ms.openlocfilehash: 8520504757e9e9ec9557b84ca2608b4cb99daf62
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977797"
---
# <a name="how-to-implement-validation-logic-on-custom-objects"></a><span data-ttu-id="b0f8c-102">Gewusst wie: Implementieren von Validierungslogik für benutzerdefinierte Objekte</span><span class="sxs-lookup"><span data-stu-id="b0f8c-102">How to: Implement Validation Logic on Custom Objects</span></span>
<span data-ttu-id="b0f8c-103">In diesem Beispiel wird gezeigt, wie Validierungs Logik für ein benutzerdefiniertes Objekt implementiert und anschließend gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-103">This example shows how to implement validation logic on a custom object and then bind to it.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b0f8c-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0f8c-104">Example</span></span>  
 <span data-ttu-id="b0f8c-105">Sie können eine Validierungs Logik für die Geschäfts Schicht bereitstellen, wenn das Quell Objekt implementiert <xref:System.ComponentModel.IDataErrorInfo> , wie im folgenden Beispiel gezeigt, das ein-Objekt definiert, `Person` das implementiert <xref:System.ComponentModel.IDataErrorInfo> :</span><span class="sxs-lookup"><span data-stu-id="b0f8c-105">You can provide validation logic on the business layer if your source object implements <xref:System.ComponentModel.IDataErrorInfo>, as in the following example, which defines a `Person` object that implements <xref:System.ComponentModel.IDataErrorInfo>:</span></span>  
  
 [!code-csharp[BusinessLayerValidation#IDataErrorInfo](~/samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Data.cs#idataerrorinfo)]
 [!code-vb[BusinessLayerValidation#IDataErrorInfo](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BusinessLayerValidation/VisualBasic/Data.vb#idataerrorinfo)]  
  
 <span data-ttu-id="b0f8c-106">Im folgenden Beispiel wird die Text-Eigenschaft des Textfelds an die- `Person.Age` Eigenschaft gebunden, die für die Bindung über eine Ressourcen Deklaration zur Verfügung gestellt wurde, der zugewiesen ist `x:Key` `data` .</span><span class="sxs-lookup"><span data-stu-id="b0f8c-106">In the following example, the text property of the text box binds to the `Person.Age` property, which has been made available for binding through a resource declaration that is given the `x:Key` `data`.</span></span> <span data-ttu-id="b0f8c-107">Der <xref:System.Windows.Controls.DataErrorValidationRule> überprüft die Validierungs Fehler, die von der-Implementierung ausgelöst wurden <xref:System.ComponentModel.IDataErrorInfo> .</span><span class="sxs-lookup"><span data-stu-id="b0f8c-107">The <xref:System.Windows.Controls.DataErrorValidationRule> checks for the validation errors raised by the <xref:System.ComponentModel.IDataErrorInfo> implementation.</span></span>  
  
 [!code-xaml[BusinessLayerValidation#BoundTextBox](~/samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Window1.xaml?highlight=8,11-19,25-42)]  
  
 <span data-ttu-id="b0f8c-108">Anstatt das <xref:System.Windows.Controls.DataErrorValidationRule> zu verwenden, können Sie alternativ die- <xref:System.Windows.Data.Binding.ValidatesOnDataErrors%2A> Eigenschaft auf festlegen `true` .</span><span class="sxs-lookup"><span data-stu-id="b0f8c-108">Alternatively, instead of using the <xref:System.Windows.Controls.DataErrorValidationRule>, you can set the <xref:System.Windows.Data.Binding.ValidatesOnDataErrors%2A> property to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0f8c-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0f8c-109">See also</span></span>

- <xref:System.Windows.Controls.ExceptionValidationRule>
- [<span data-ttu-id="b0f8c-110">Implementieren der Bindungs Validierung</span><span class="sxs-lookup"><span data-stu-id="b0f8c-110">Implement Binding Validation</span></span>](how-to-implement-binding-validation.md)
- [<span data-ttu-id="b0f8c-111">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="b0f8c-111">How-to Topics</span></span>](data-binding-how-to-topics.md)
