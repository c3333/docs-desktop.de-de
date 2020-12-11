---
title: 'Gewusst wie: Synchrones Suchen in einem Storyboard'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- seeking Storyboards synchronously [WPF]
- Storyboards [WPF], seeking synchronously
ms.assetid: 03e06271-a946-4810-88ea-3fb4cfa9e0f1
ms.openlocfilehash: 8ac55346ac83ee94318de90655bde6053ef20687
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977311"
---
# <a name="how-to-seek-a-storyboard-synchronously"></a><span data-ttu-id="cfed6-102">Gewusst wie: Synchrones Suchen in einem Storyboard</span><span class="sxs-lookup"><span data-stu-id="cfed6-102">How to: Seek a Storyboard Synchronously</span></span>
<span data-ttu-id="cfed6-103">Im folgenden Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.Animation.Storyboard.SeekAlignedToLastTick%2A> Methode eines verwendet wird <xref:System.Windows.Media.Animation.Storyboard> , um eine beliebige Position in einer Storyboard-Animation synchron zu suchen.</span><span class="sxs-lookup"><span data-stu-id="cfed6-103">The following example shows how to use the <xref:System.Windows.Media.Animation.Storyboard.SeekAlignedToLastTick%2A> method of a <xref:System.Windows.Media.Animation.Storyboard> to seek to any position in a storyboard animation synchronously.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cfed6-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cfed6-104">Example</span></span>  
 <span data-ttu-id="cfed6-105">Im Folgenden wird das XAML-Markup für das Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cfed6-105">The following is the XAML markup for the sample.</span></span>  
  
 [!code-xaml[SeekStoryboard_snip#SeekStoryboardSynchronouslyExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/SeekStoryboard_snip/CSharp/SeekStoryboardSynchronouslyExample.xaml#seekstoryboardsynchronouslyexamplewholepage)]  
  
## <a name="example"></a><span data-ttu-id="cfed6-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cfed6-106">Example</span></span>  
 <span data-ttu-id="cfed6-107">Im Folgenden wird der Code dargestellt, der zusammen mit dem obigen XAML-Code verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfed6-107">The following is the code used with the XAML code above.</span></span>  
  
 [!code-csharp[SeekStoryboard_snip#SeekStoryboardSynchronouslyCodeBehindExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/SeekStoryboard_snip/CSharp/SeekStoryboardSynchronouslyExample.xaml.cs#seekstoryboardsynchronouslycodebehindexamplewholepage)]
 [!code-vb[SeekStoryboard_snip#SeekStoryboardSynchronouslyCodeBehindExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/SeekStoryboard_snip/VisualBasic/SeekStoryboardSynchronouslyExample.xaml.vb#seekstoryboardsynchronouslycodebehindexamplewholepage)]
