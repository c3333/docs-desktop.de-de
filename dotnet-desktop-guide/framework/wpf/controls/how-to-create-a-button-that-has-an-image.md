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
# <a name="how-to-create-a-button-that-has-an-image"></a><span data-ttu-id="713a6-102">Gewusst wie: Erstellen einer Schaltfläche mit einem Bild</span><span class="sxs-lookup"><span data-stu-id="713a6-102">How to: Create a Button That Has an Image</span></span>
<span data-ttu-id="713a6-103">Dieses Beispiel zeigt, wie Sie ein Bild in einen einschließen <xref:System.Windows.Controls.Button> .</span><span class="sxs-lookup"><span data-stu-id="713a6-103">This example shows how to include an image on a <xref:System.Windows.Controls.Button>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="713a6-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="713a6-104">Example</span></span>  
 <span data-ttu-id="713a6-105">Im folgenden Beispiel werden zwei-Steuer <xref:System.Windows.Controls.Button> Elemente erstellt.</span><span class="sxs-lookup"><span data-stu-id="713a6-105">The following example creates two <xref:System.Windows.Controls.Button> controls.</span></span> <span data-ttu-id="713a6-106">Eine <xref:System.Windows.Controls.Button> enthält Text, und die andere enthält ein Bild.</span><span class="sxs-lookup"><span data-stu-id="713a6-106">One <xref:System.Windows.Controls.Button> contains text and the other contains an image.</span></span> <span data-ttu-id="713a6-107">Das Image befindet sich in einem Ordner namens "Data", bei dem es sich um einen Unterordner des Projekt Ordners des Beispiels handelt.</span><span class="sxs-lookup"><span data-stu-id="713a6-107">The image is in a folder called data, which is a subfolder of the example’s project folder.</span></span> <span data-ttu-id="713a6-108">Wenn ein Benutzer auf das <xref:System.Windows.Controls.Button> -Bild klickt, das das Bild enthält, wird der Hintergrund und der Text der anderen <xref:System.Windows.Controls.Button> geändert.</span><span class="sxs-lookup"><span data-stu-id="713a6-108">When a user clicks the <xref:System.Windows.Controls.Button> that has the image, the background and the text of the other <xref:System.Windows.Controls.Button> change.</span></span>  
  
 <span data-ttu-id="713a6-109">In diesem Beispiel <xref:System.Windows.Controls.Button> werden Steuerelemente mithilfe von Markup erstellt, aber es wird Code verwendet, um die <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignishandler zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="713a6-109">This example creates <xref:System.Windows.Controls.Button> controls by using markup but uses code to write the <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event handlers.</span></span>  
  
 [!code-xaml[BtnColor#4](~/samples/snippets/csharp/VS_Snippets_Wpf/BtnColor/CSharp/Pane1.xaml#4)]  
  
 [!code-csharp[BtnColor#6](~/samples/snippets/csharp/VS_Snippets_Wpf/BtnColor/CSharp/Pane1.xaml.cs#6)]
 [!code-vb[BtnColor#6](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BtnColor/VisualBasic/Pane1.xaml.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="713a6-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="713a6-110">See also</span></span>

- [<span data-ttu-id="713a6-111">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="713a6-111">Controls</span></span>](index.md)
- [<span data-ttu-id="713a6-112">Steuerelementbibliothek</span><span class="sxs-lookup"><span data-stu-id="713a6-112">Control Library</span></span>](control-library.md)
