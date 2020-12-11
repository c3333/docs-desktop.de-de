---
title: 'Gewusst wie: Positionieren der untergeordneten Elemente eines Rasters'
description: Erfahren Sie, wie Sie die Get-und Set-Methoden verwenden, die in einem Windows Presentation Foundation Raster definiert sind, um untergeordnete Elemente zu positionieren.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Grid control [WPF], positioning child elements
ms.assetid: 27b3ba9b-ad32-44e2-bcab-a79d573a463c
ms.openlocfilehash: 926d223097dd21dd0292c9523903b4be8aba8ba9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978151"
---
# <a name="how-to-position-the-child-elements-of-a-grid"></a>Gewusst wie: Positionieren der untergeordneten Elemente eines Rasters
Dieses Beispiel zeigt, wie Sie die Get-und Set-Methoden verwenden, die für zum Positionieren von untergeordneten Elementen definiert sind <xref:System.Windows.Controls.Grid> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein <xref:System.Windows.Controls.Grid> übergeordnetes Element ( `grid1` ) mit drei Spalten und drei Zeilen definiert. Ein untergeordnetes <xref:System.Windows.Shapes.Rectangle> Element ( `rect1` ) wird der <xref:System.Windows.Controls.Grid> in der Spaltenposition 0 (null), Zeilen Position 0, hinzugefügt. <xref:System.Windows.Controls.Button> -Elemente stellen Methoden dar, die aufgerufen werden können, um das <xref:System.Windows.Shapes.Rectangle> Element in der neu zu positionieren <xref:System.Windows.Controls.Grid> . Wenn ein Benutzer auf eine Schaltfläche klickt, wird die zugehörige-Methode aktiviert.  
  
 [!code-xaml[gridGetSetMethods](~/samples/snippets/csharp/VS_Snippets_Wpf/gridGetSetMethods/CSharp/Window1.xaml)]  
  
 Im folgenden Code Behind-Beispiel werden die Methoden behandelt, die von den Schaltflächen <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignissen erhoben werden. Im Beispiel werden diese Methodenaufrufe in- <xref:System.Windows.Controls.TextBlock> Elemente geschrieben, die Verwandte Get-Methoden verwenden, um die neuen Eigenschaftswerte als Zeichen folgen auszugeben.  
  
 [!code-csharp[gridGetSetMethods#2](~/samples/snippets/csharp/VS_Snippets_Wpf/gridGetSetMethods/CSharp/Window1.xaml.cs#2)]
 [!code-vb[gridGetSetMethods#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/gridGetSetMethods/VisualBasic/Window1.xaml.vb#2)]  
 Hier ist das fertige Ergebnis!

 ![ein Screenshot stellt eine WPF-Benutzeroberfläche mit zwei Spalten dar, die Rechte Seite verfügt über ein 3 x 3-Raster und die linke Schaltfläche, um ein farbiges Rechteck zwischen den Spalten und Zeilen des Rasters zu verschieben.](././media/grid-methods-sample.png)
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Grid>
- [Übersicht über Panel-Elemente](panels-overview.md)
