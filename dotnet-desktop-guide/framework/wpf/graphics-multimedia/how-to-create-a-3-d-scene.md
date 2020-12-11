---
title: 'Gewusst wie: Erstellen einer 3D-Szene'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- scenes [WPF], 3D
- 3D scenes
ms.assetid: adb4a598-71a2-4dd5-b677-ea3fc11b78b2
ms.openlocfilehash: 36453894e06e7b59f339c21713449140c17f6851
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977622"
---
# <a name="how-to-create-a-3d-scene"></a>Gewusst wie: Erstellen einer 3D-Szene
Dieses Beispiel zeigt, wie ein 3D-Objekt erstellt wird, das wie ein Papierblatt aussieht, das gedreht wurde. Eine <xref:System.Windows.Controls.Viewport3D> zusammen mit den folgenden Komponenten wird verwendet, um diese einfache 3D-Szene zu erstellen:  
  
- Eine Kamera wird mit einem erstellt <xref:System.Windows.Media.Media3D.PerspectiveCamera> . Die Kamera gibt an, welcher Teil der 3D-Szene angezeigt werden kann.  
  
- Ein Mesh wird erstellt, um die Form des 3D-Objekts (Blatt des Papiers) mithilfe der- <xref:System.Windows.Media.Media3D.GeometryModel3D.Geometry%2A> Eigenschaft von anzugeben <xref:System.Windows.Media.Media3D.GeometryModel3D> .  
  
- Mithilfe der-Eigenschaft von wird ein Material angegeben, das auf der Oberfläche des-Objekts (linearer Farbverlauf in diesem Beispiel) angezeigt werden soll <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> <xref:System.Windows.Media.Media3D.GeometryModel3D> .  
  
- Ein Licht wird erstellt, um für das-Objekt zu glänzen, das verwendet <xref:System.Windows.Media.Media3D.DirectionalLight> .  
  
## <a name="example"></a>Beispiel  
 Der folgende Code zeigt, wie Sie eine 3D-Szene in XAML erstellen.  
  
 [!code-xaml[3DGallery_snip#Basic3DShapeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/Basic3DShapeExample.xaml#basic3dshapeexamplewholepage)]  
  
## <a name="example"></a>Beispiel  
 Der folgende Code zeigt, wie die gleiche 3D-Szene in prozeduralem Code erstellt wird.  
  
 [!code-csharp[3DGallery_procedural_snip#Basic3DShapeCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/Basic3DShapeExample.cs#basic3dshapecodeexamplewholepage)]
 [!code-vb[3DGallery_procedural_snip#Basic3DShapeCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/3DGallery_procedural_snip/visualbasic/basic3dshapeexample.vb#basic3dshapecodeexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über 3D-Grafiken](3-d-graphics-overview.md)
