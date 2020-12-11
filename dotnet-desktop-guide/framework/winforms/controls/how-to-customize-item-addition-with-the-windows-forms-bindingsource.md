---
title: Element Addition mit BindingSource-Komponente anpassen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [Windows Forms], creating new items
- BindingSource component [Windows Forms], customizing item addition with
- examples [Windows Forms], BindingSource component
- BindingSource component [Windows Forms], examples
ms.assetid: 1aae11fc-6fb2-4cb9-b3d0-e0638fe77ef0
ms.openlocfilehash: 7d74fe6b4bbb1ddb94b359f5ba3ae32ed398d1dd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975680"
---
# <a name="how-to-customize-item-addition-with-the-windows-forms-bindingsource"></a>Vorgehensweise: Anpassen der Hinzufügung von Elementen mithilfe der BindingSource in Windows Forms
Wenn Sie eine <xref:System.Windows.Forms.BindingSource> -Komponente zum Binden eines Windows Forms-Steuerelements an eine Datenquelle verwenden, kann es ggf. erforderlich sein, die Erstellung neuer Elemente anzupassen. Die <xref:System.Windows.Forms.BindingSource> -Komponente vereinfacht dies durch die Bereitstellung des <xref:System.Windows.Forms.BindingSource.AddingNew> -Ereignisses, das in der Regel ausgelöst wird, wenn das gebundene Steuerelement ein neues Element erstellen muss. Ihr Ereignishandler kann jedes erforderliche benutzerdefinierte Verhalten (z. B. das Aufrufen einer Methode für einen Webdienst oder das Abrufen eines neuen Objekts aus einer Klassenfactory) bereitstellen.  
  
> [!NOTE]
> Wenn ein Element durch Verarbeiten des <xref:System.Windows.Forms.BindingSource.AddingNew> -Ereignisses hinzugefügt wird, kann die Hinzufügung nicht abgebrochen werden.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt, wie ein <xref:System.Windows.Forms.DataGridView> -Steuerelement mithilfe einer <xref:System.Windows.Forms.BindingSource> -Komponente an eine Klassenfactory gebunden wird. Wenn der Benutzer auf die neue Zeile des <xref:System.Windows.Forms.DataGridView> -Steuerelements klickt, wird das <xref:System.Windows.Forms.BindingSource.AddingNew> -Ereignis ausgelöst. Der Ereignishandler erstellt ein neues `DemoCustomer` -Objekt, das der Eigenschaft <xref:System.ComponentModel.AddingNewEventArgs.NewObject%2A?displayProperty=nameWithType> zugewiesen wird. Dies bewirkt, dass das neue `DemoCustomer` -Objekt der Liste der <xref:System.Windows.Forms.BindingSource> -Komponente hinzugefügt und in der neuen Zeile des <xref:System.Windows.Forms.DataGridView> -Steuerelements angezeigt wird.  
  
 [!code-cpp[System.Windows.Forms.DataConnector.AddingNew#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.AddingNew/CPP/form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.DataConnector.AddingNew#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.AddingNew/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnector.AddingNew#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.AddingNew/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys "System", "System.Data", "System.Drawing" und "System.Windows.Forms".  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.BindingNavigator>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [BindingSource-Komponente](bindingsource-component.md)
- [Vorgehensweise: Binden eines Windows Forms-Steuerelements an einen Typ](how-to-bind-a-windows-forms-control-to-a-type.md)
