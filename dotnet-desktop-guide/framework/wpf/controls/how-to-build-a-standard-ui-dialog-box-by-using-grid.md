---
title: 'Gewusst wie: Erstellen eines Benutzeroberflächen-Standarddialogfelds unter Verwendung des Grid-Elements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- dialog boxes [WPF], creating
- Grid control [WPF], creating [WPF], dialog box
ms.assetid: d6ac3d51-844b-4d29-96d8-81a696a7b960
ms.openlocfilehash: 442d69f891d53365653c01ef4dca296398ae7195
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978092"
---
# <a name="how-to-build-a-standard-ui-dialog-box-by-using-grid"></a>Gewusst wie: Erstellen eines Benutzeroberflächen-Standarddialogfelds unter Verwendung des Grid-Elements
In diesem Beispiel wird gezeigt, wie ein Standard [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] Dialogfeld mit dem-Element erstellt wird <xref:System.Windows.Controls.Grid> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Dialogfeld wie das Dialogfeld **Ausführen** im Windows-Betriebssystem erstellt.  
  
 Im Beispiel wird ein erstellt <xref:System.Windows.Controls.Grid> und die <xref:System.Windows.Controls.ColumnDefinition> -Klasse und die- <xref:System.Windows.Controls.RowDefinition> Klasse verwendet, um fünf Spalten und vier Zeilen zu definieren.  
  
 Im Beispiel wird dann ein,, hinzugefügt und positioniert, <xref:System.Windows.Controls.Image> `RunIcon.png` um das Bild darzustellen, das im Dialogfeld gefunden wird. Das Bild wird in der ersten Spalte und Zeile der <xref:System.Windows.Controls.Grid> (der oberen linken Ecke) platziert.  
  
 Im folgenden Beispiel <xref:System.Windows.Controls.TextBlock> wird der ersten Spalte, die die restlichen Spalten der ersten Zeile umfasst, ein-Element hinzugefügt. Der <xref:System.Windows.Controls.TextBlock> zweiten Zeile in der ersten Spalte wird ein weiteres Element hinzugefügt, das das **geöffnete** Textfeld darstellt. Ein <xref:System.Windows.Controls.TextBlock> folgt, das den Dateneingabe Bereich darstellt.  
  
 Schließlich werden in diesem Beispiel der <xref:System.Windows.Controls.Button> letzten Zeile drei Elemente hinzugefügt, die die Ereignisse " **OK**", " **Abbrechen**" und " **Durchsuchen** " darstellen.  
  
 [!code-csharp[GridRunDialog#1](~/samples/snippets/csharp/VS_Snippets_Wpf/GridRunDialog/CSharp/window1.xaml.cs#1)]
 [!code-vb[GridRunDialog#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GridRunDialog/VisualBasic/grid_vb.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.GridUnitType>
- [Übersicht über Panel-Elemente](panels-overview.md)
- [Artikel zu Vorgehensweisen](grid-how-to-topics.md)
