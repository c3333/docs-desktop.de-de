---
title: 'Gewusst wie: Auflisten von Systemschriftarten'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- typography [WPF], enumerating system fonts
- fonts [WPF], enumerating
- system fonts [WPF], enumerating
- enumerating [WPF], system fonts
ms.assetid: 36e37791-55b9-4f01-a496-5cc10335e6a6
ms.openlocfilehash: 7ea16afa12233ad5f8268ec048bed187f6081299
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977136"
---
# <a name="how-to-enumerate-system-fonts"></a>Gewusst wie: Auflisten von Systemschriftarten
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie die Schriftarten in der System Schriftart Auflistung aufgelistet werden. Der Schrift Familienname jedes <xref:System.Windows.Media.FontFamily> in <xref:System.Windows.Media.Fonts.SystemFontFamilies%2A> wird einem Kombinations Feld als Element hinzugefügt.  
  
 [!code-csharp[TextOverview#100](~/samples/snippets/csharp/VS_Snippets_Wpf/TextOverview/CSharp/Window1.xaml.cs#100)]
 [!code-vb[TextOverview#100](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextOverview/visualbasic/window1.xaml.vb#100)]  
  
 Wenn sich mehrere Versionen der gleichen Schriftfamilie im gleichen Verzeichnis befinden, gibt die [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Schriftart Enumeration die aktuellste Version der Schriftart zurück. Wenn die Versionsinformationen keine Auflösung bereitstellen, wird die Schriftart mit dem neuesten Zeitstempel zurückgegeben. Wenn die Zeitstempel-Informationen gleichwertig sind, wird die Schriftart Datei zurückgegeben, die zuerst in alphabetischer Reihenfolge angezeigt wird.
