---
title: 'Gewusst wie: Erstellen einer Schaltfläche mit einem Bild'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Button controls [WPF], creating
ms.assetid: 607a193c-4098-4dd8-8dc0-51256cec2020
ms.openlocfilehash: 5be928ac75ad727feabcde07ac0c6dc76ed130e6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978078"
---
# <a name="how-to-create-a-button-that-has-an-image"></a>Gewusst wie: Erstellen einer Schaltfläche mit einem Bild
Dieses Beispiel zeigt, wie Sie ein Bild in einen einschließen <xref:System.Windows.Controls.Button> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden zwei-Steuer <xref:System.Windows.Controls.Button> Elemente erstellt. Eine <xref:System.Windows.Controls.Button> enthält Text, und die andere enthält ein Bild. Das Image befindet sich in einem Ordner namens "Data", bei dem es sich um einen Unterordner des Projekt Ordners des Beispiels handelt. Wenn ein Benutzer auf das <xref:System.Windows.Controls.Button> -Bild klickt, das das Bild enthält, wird der Hintergrund und der Text der anderen <xref:System.Windows.Controls.Button> geändert.  
  
 In diesem Beispiel <xref:System.Windows.Controls.Button> werden Steuerelemente mithilfe von Markup erstellt, aber es wird Code verwendet, um die <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignishandler zu schreiben.  
  
 [!code-xaml[BtnColor#4](~/samples/snippets/csharp/VS_Snippets_Wpf/BtnColor/CSharp/Pane1.xaml#4)]  
  
 [!code-csharp[BtnColor#6](~/samples/snippets/csharp/VS_Snippets_Wpf/BtnColor/CSharp/Pane1.xaml.cs#6)]
 [!code-vb[BtnColor#6](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BtnColor/VisualBasic/Pane1.xaml.vb#6)]  
  
## <a name="see-also"></a>Siehe auch

- [Steuerelemente](index.md)
- [Steuerelementbibliothek](control-library.md)
