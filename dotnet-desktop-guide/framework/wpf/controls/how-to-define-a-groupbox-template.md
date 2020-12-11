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
# <a name="how-to-define-a-groupbox-template"></a><span data-ttu-id="30521-102">Gewusst wie: Definieren einer GroupBox-Vorlage</span><span class="sxs-lookup"><span data-stu-id="30521-102">How to: Define a GroupBox Template</span></span>

<span data-ttu-id="30521-103">In diesem Beispiel wird gezeigt, wie eine Vorlage für ein-Steuerelement erstellt wird <xref:System.Windows.Controls.GroupBox> .</span><span class="sxs-lookup"><span data-stu-id="30521-103">This example shows how to create a template for a <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="30521-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="30521-104">Example</span></span>  

 <span data-ttu-id="30521-105">Im folgenden Beispiel wird eine <xref:System.Windows.Controls.GroupBox> Steuerelement Vorlage mithilfe eines- <xref:System.Windows.Controls.Grid> Steuer Elements für das Layout definiert.</span><span class="sxs-lookup"><span data-stu-id="30521-105">The following example defines a <xref:System.Windows.Controls.GroupBox> control template by using a <xref:System.Windows.Controls.Grid> control for layout.</span></span> <span data-ttu-id="30521-106">Die Vorlage verwendet einen <xref:System.Windows.Controls.BorderGapMaskConverter> , um den Rahmen der zu definieren <xref:System.Windows.Controls.GroupBox> , sodass der Inhalt nicht durch den Rahmen verdeckt wird <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> .</span><span class="sxs-lookup"><span data-stu-id="30521-106">The template uses a <xref:System.Windows.Controls.BorderGapMaskConverter> to define the border of the <xref:System.Windows.Controls.GroupBox> so that the border does not obscure the <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> content.</span></span>  
  
 [!code-xaml[GroupBoxSnippet#GroupBoxTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/GroupBoxSnippet/CS/Window1.xaml#groupboxtemplate)]  
  
## <a name="see-also"></a><span data-ttu-id="30521-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30521-107">See also</span></span>

- <xref:System.Windows.Controls.GroupBox>
- <span data-ttu-id="30521-108">[Vorgehensweise: Erstellen einer GroupBox](/previous-versions/dotnet/netframework-3.5/ms748321(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="30521-108">[How to: Create a GroupBox](/previous-versions/dotnet/netframework-3.5/ms748321(v=vs.90))</span></span>
