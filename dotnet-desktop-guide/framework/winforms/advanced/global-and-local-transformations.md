---
title: Globale und lokale Transformationen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- matrices [Windows Forms], using transformations
- transformations [Windows Forms], global
- transformations [Windows Forms], local
ms.assetid: b601d66d-d572-4f11-9d2e-92f0dc8893f3
ms.openlocfilehash: f62efb31e95b0797272997fadbc28459579a0de0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975274"
---
# <a name="global-and-local-transformations"></a>Globale und lokale Transformationen
Eine globale Transformation ist eine Transformation, die auf jedes Element angewendet wird, das von einem bestimmten Objekt gezeichnet wird <xref:System.Drawing.Graphics> . Im Gegensatz dazu ist eine lokale Transformation eine Transformation, die auf ein bestimmtes Element angewendet wird, das gezeichnet werden soll.  
  
## <a name="global-transformations"></a>Globale Transformationen  
 Um eine globale Transformation zu erstellen, erstellen Sie ein <xref:System.Drawing.Graphics> -Objekt, und bearbeiten Sie dann die zugehörige- <xref:System.Drawing.Graphics.Transform%2A> Eigenschaft. Die- <xref:System.Drawing.Graphics.Transform%2A> Eigenschaft ist ein- <xref:System.Drawing.Drawing2D.Matrix> Objekt, sodass Sie eine beliebige Sequenz von affinen Transformationen enthalten kann. Die in der-Eigenschaft gespeicherte Transformation <xref:System.Drawing.Graphics.Transform%2A> wird als weltweite Transformation bezeichnet. Die- <xref:System.Drawing.Graphics> Klasse stellt mehrere Methoden zum Aufbauen einer zusammengesetzten Welt Transformation bereit: <xref:System.Drawing.Graphics.MultiplyTransform%2A> , <xref:System.Drawing.Graphics.RotateTransform%2A> , <xref:System.Drawing.Graphics.ScaleTransform%2A> und <xref:System.Drawing.Graphics.TranslateTransform%2A> . Im folgenden Beispiel wird eine Ellipse zweimal gezeichnet: einmal vor dem Erstellen einer Welt Transformation und einmal nach. Die Transformation skaliert zuerst mit dem Faktor 0,5 in der y-Richtung, übersetzt dann 50 Einheiten in die x-Richtung und dreht dann 30 Grad.  
  
 [!code-csharp[System.Drawing.CoordinateSystems#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.CoordinateSystems#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/VB/Class1.vb#21)]  
  
 Die folgende Abbildung zeigt die Matrizen, die an der Transformation beteiligt sind.  
  
 ![Transformationen](./media/aboutgdip05-art14.gif "AboutGdip05_art14")  
  
> [!NOTE]
> Im vorherigen Beispiel wird die Ellipse um den Ursprung des Koordinatensystems gedreht, das sich in der oberen linken Ecke des Client Bereichs befindet. Dies führt zu einem anderen Ergebnis als das Drehen der Ellipse über einen eigenen Mittelpunkt.  
  
## <a name="local-transformations"></a>Lokale Transformationen  
 Eine lokale Transformation gilt für ein bestimmtes Element, das gezeichnet werden soll. Ein-Objekt verfügt beispielsweise über <xref:System.Drawing.Drawing2D.GraphicsPath> eine- <xref:System.Drawing.Drawing2D.GraphicsPath.Transform%2A> Methode, die es Ihnen ermöglicht, die Datenpunkte dieses Pfades zu transformieren. Im folgenden Beispiel wird ein Rechteck ohne Transformation und ein Pfad mit einer Rotations Transformation gezeichnet. (Angenommen, es gibt keine Welt Transformation.)  
  
 [!code-csharp[System.Drawing.CoordinateSystems#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/CS/Class1.cs#22)]
 [!code-vb[System.Drawing.CoordinateSystems#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/VB/Class1.vb#22)]  
  
 Sie können die Welt Transformation mit lokalen Transformationen kombinieren, um eine Vielzahl von Ergebnissen zu erzielen. Beispielsweise können Sie mit der Welt Transformation das Koordinatensystem überarbeiten und lokale Transformationen verwenden, um Objekte zu drehen und zu skalieren, die auf dem neuen Koordinatensystem gezeichnet werden.  
  
 Angenommen, Sie möchten ein Koordinatensystem, dessen Ursprung 200 Pixel vom linken Rand des Client Bereichs und 150 Pixel vom oberen Rand des Client Bereichs hat. Angenommen, Sie möchten, dass die Maßeinheit das Pixel ist, wobei die x-Achse nach rechts und die y-Achse nach oben zeigt. Beim Standard Koordinatensystem wird die y-Achse nach unten angezeigt, sodass Sie eine Reflektion auf der horizontalen Achse ausführen müssen. Die folgende Abbildung zeigt die Matrix einer solchen Reflektion.  
  
 ![Transformationen](./media/aboutgdip05-art15.gif "AboutGdip05_art15")  
  
 Nehmen wir als nächstes an, dass Sie eine Translation 200-Einheiten nach rechts und 150-Einheiten ausführen müssen.  
  
 Im folgenden Beispiel wird das Koordinatensystem festgelegt, das gerade durch Festlegen der Welt Transformation eines-Objekts beschrieben wird <xref:System.Drawing.Graphics> .  
  
 [!code-csharp[System.Drawing.CoordinateSystems#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/CS/Class1.cs#23)]
 [!code-vb[System.Drawing.CoordinateSystems#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/VB/Class1.vb#23)]  
  
 Der folgende Code (am Ende des vorangehenden Beispiels eingefügt) erstellt einen Pfad, der aus einem einzelnen Rechteck mit der unteren linken Ecke am Ursprung des neuen Koordinatensystems besteht. Das Rechteck wird einmal ohne lokale Transformation und einmal mit einer lokalen Transformation aufgefüllt. Die lokale Transformation besteht aus einer horizontalen Skalierung mit dem Faktor 2, gefolgt von einer 30-Grad-Drehung.  
  
 [!code-csharp[System.Drawing.CoordinateSystems#24](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/CS/Class1.cs#24)]
 [!code-vb[System.Drawing.CoordinateSystems#24](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.CoordinateSystems/VB/Class1.vb#24)]  
  
 Die folgende Abbildung zeigt das neue Koordinatensystem und die beiden Rechtecke.  
  
 ![Transformationen](./media/aboutgdip05-art16.gif "AboutGdip05_art16")  
  
## <a name="see-also"></a>Siehe auch

- [Koordinatensysteme und Transformationen](coordinate-systems-and-transformations.md)
- [Verwenden von Transformationen in Managed GDI+](using-transformations-in-managed-gdi.md)
