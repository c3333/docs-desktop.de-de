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
# <a name="how-to-implement-validation-logic-on-custom-objects"></a>Gewusst wie: Implementieren von Validierungslogik für benutzerdefinierte Objekte
In diesem Beispiel wird gezeigt, wie Validierungs Logik für ein benutzerdefiniertes Objekt implementiert und anschließend gebunden wird.  
  
## <a name="example"></a>Beispiel  
 Sie können eine Validierungs Logik für die Geschäfts Schicht bereitstellen, wenn das Quell Objekt implementiert <xref:System.ComponentModel.IDataErrorInfo> , wie im folgenden Beispiel gezeigt, das ein-Objekt definiert, `Person` das implementiert <xref:System.ComponentModel.IDataErrorInfo> :  
  
 [!code-csharp[BusinessLayerValidation#IDataErrorInfo](~/samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Data.cs#idataerrorinfo)]
 [!code-vb[BusinessLayerValidation#IDataErrorInfo](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BusinessLayerValidation/VisualBasic/Data.vb#idataerrorinfo)]  
  
 Im folgenden Beispiel wird die Text-Eigenschaft des Textfelds an die- `Person.Age` Eigenschaft gebunden, die für die Bindung über eine Ressourcen Deklaration zur Verfügung gestellt wurde, der zugewiesen ist `x:Key` `data` . Der <xref:System.Windows.Controls.DataErrorValidationRule> überprüft die Validierungs Fehler, die von der-Implementierung ausgelöst wurden <xref:System.ComponentModel.IDataErrorInfo> .  
  
 [!code-xaml[BusinessLayerValidation#BoundTextBox](~/samples/snippets/csharp/VS_Snippets_Wpf/BusinessLayerValidation/CSharp/Window1.xaml?highlight=8,11-19,25-42)]  
  
 Anstatt das <xref:System.Windows.Controls.DataErrorValidationRule> zu verwenden, können Sie alternativ die- <xref:System.Windows.Data.Binding.ValidatesOnDataErrors%2A> Eigenschaft auf festlegen `true` .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ExceptionValidationRule>
- [Implementieren der Bindungs Validierung](how-to-implement-binding-validation.md)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
