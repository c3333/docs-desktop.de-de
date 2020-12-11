---
title: 'Gewusst wie: Definieren einer GroupBox-Vorlage'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], GroupBox
- GroupBox control [WPF], creating templates
ms.assetid: 85a4d1a7-4753-4f4a-b26d-14fa10c1ddb5
ms.openlocfilehash: f04e4a7e3feb4bd7c5dac1b4127d48923fb7ea62
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977814"
---
# <a name="how-to-define-a-groupbox-template"></a>Gewusst wie: Definieren einer GroupBox-Vorlage

In diesem Beispiel wird gezeigt, wie eine Vorlage für ein-Steuerelement erstellt wird <xref:System.Windows.Controls.GroupBox> .  
  
## <a name="example"></a>Beispiel  

 Im folgenden Beispiel wird eine <xref:System.Windows.Controls.GroupBox> Steuerelement Vorlage mithilfe eines- <xref:System.Windows.Controls.Grid> Steuer Elements für das Layout definiert. Die Vorlage verwendet einen <xref:System.Windows.Controls.BorderGapMaskConverter> , um den Rahmen der zu definieren <xref:System.Windows.Controls.GroupBox> , sodass der Inhalt nicht durch den Rahmen verdeckt wird <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> .  
  
 [!code-xaml[GroupBoxSnippet#GroupBoxTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/GroupBoxSnippet/CS/Window1.xaml#groupboxtemplate)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.GroupBox>
- [Vorgehensweise: Erstellen einer GroupBox](/previous-versions/dotnet/netframework-3.5/ms748321(v=vs.90))
