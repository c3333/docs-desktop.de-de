---
title: 'Gewusst wie: Anpassen der Größe des Ziehpunkts auf einer Bildlaufleiste'
ms.date: 03/30/2017
helpviewer_keywords:
- ScrollBar control [WPF]
- customizing thumb size [WPF]
- thumb size [WPF]
ms.assetid: fa32b866-5ca1-4e73-85e7-2ac64b80d194
ms.openlocfilehash: 60ae7c4e95801036c5deb0c485645297509b830c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977815"
---
# <a name="how-to-customize-the-thumb-size-on-a-scrollbar"></a>Gewusst wie: Anpassen der Größe des Ziehpunkts auf einer Bildlaufleiste
In diesem Thema wird erläutert, wie die <xref:System.Windows.Controls.Primitives.Thumb> eines <xref:System.Windows.Controls.Primitives.ScrollBar> auf eine festgelegte Größe festgelegt wird und wie eine minimale Größe für die eines angegeben wird <xref:System.Windows.Controls.Primitives.Thumb> <xref:System.Windows.Controls.Primitives.ScrollBar> .  
  
## <a name="example"></a>Beispiel  
  
## <a name="description"></a>BESCHREIBUNG  
 Im folgenden Beispiel wird eine erstellt <xref:System.Windows.Controls.Primitives.ScrollBar> , die eine <xref:System.Windows.Controls.Primitives.Thumb> mit fester Größe aufweist. Im Beispiel wird die <xref:System.Windows.Controls.Primitives.Track.ViewportSize%2A> -Eigenschaft des <xref:System.Windows.Controls.Primitives.Thumb> auf festgelegt, <xref:System.Double.NaN> und die Höhe des wird festgelegt <xref:System.Windows.Controls.Primitives.Thumb> .  Zum Erstellen eines horizontalen <xref:System.Windows.Controls.Primitives.ScrollBar> mit einem mit <xref:System.Windows.Controls.Primitives.Thumb> fester Breite legen Sie die Breite des fest <xref:System.Windows.Controls.Primitives.Thumb> .  
  
## <a name="code"></a>Code  
 [!code-xaml[ScrollBarCustomThumbSize#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ScrollBarCustomThumbSize/CS/Window1.xaml#1)]  
  
## <a name="description"></a>BESCHREIBUNG  
 Im folgenden Beispiel wird eine erstellt <xref:System.Windows.Controls.Primitives.ScrollBar> , die eine <xref:System.Windows.Controls.Primitives.Thumb> mit einer minimalen Größe aufweist. Im Beispiel wird der Wert von festgelegt <xref:System.Windows.SystemParameters.VerticalScrollBarButtonHeightKey%2A> . Legen Sie zum Erstellen eines horizontalen <xref:System.Windows.Controls.Primitives.ScrollBar> mit einem mit <xref:System.Windows.Controls.Primitives.Thumb> einer minimalen Breite den fest <xref:System.Windows.SystemParameters.HorizontalScrollBarButtonWidthKey%2A> .  
  
## <a name="code"></a>Code  
 [!code-xaml[ScrollBarCustomThumbSize#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ScrollBarCustomThumbSize/CS/Window1.xaml#2)]  
  
## <a name="see-also"></a>Siehe auch

- [ScrollBar-Stile und -Vorlagen](scrollbar-styles-and-templates.md)
