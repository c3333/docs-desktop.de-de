---
title: Verwenden geschachtelter Grafikcontainer
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [Windows Forms], nested containers
- graphics [Windows Forms], clipping
- graphics [Windows Forms], transformations in nested objects
ms.assetid: a0d9f178-43a4-4323-bb5a-d3e3f77ae6c1
ms.openlocfilehash: 460ebb37ee62691a1e282f756840121fd378ebd8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975837"
---
# <a name="using-nested-graphics-containers"></a>Verwenden geschachtelter Grafikcontainer
GDI+ stellt Container bereit, die Sie verwenden können, um einen Teil des Zustands in einem-Objekt temporär zu ersetzen oder zu erweitern <xref:System.Drawing.Graphics> . Sie erstellen einen Container, indem Sie die- <xref:System.Drawing.Graphics.BeginContainer%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts aufrufen. Sie können wiederholt einen aufzurufenden <xref:System.Drawing.Graphics.BeginContainer%2A> Container erstellen. Jeder-Rückruf <xref:System.Drawing.Graphics.BeginContainer%2A> muss mit einem-Befehl gekoppelt werden <xref:System.Drawing.Graphics.EndContainer%2A> .  
  
## <a name="transformations-in-nested-containers"></a>Transformationen in der Liste der Container  
 Im folgenden Beispiel werden ein <xref:System.Drawing.Graphics> -Objekt und ein Container innerhalb dieses <xref:System.Drawing.Graphics> Objekts erstellt. Die globale Transformation des- <xref:System.Drawing.Graphics> Objekts ist eine Translation 100-Einheiten in der x-Richtung und 80-Einheiten in der y-Richtung. Die Welt Transformation des Containers ist eine 30-Grad-Rotation. Der Code führt den-Rückruf `DrawRectangle(pen, -60, -30, 120, 60)` zweimal aus. Der erste Aufruf von <xref:System.Drawing.Graphics.DrawRectangle%2A> befindet sich innerhalb des Containers, d. h., der Aufruf erfolgt zwischen den Aufrufen von <xref:System.Drawing.Graphics.BeginContainer%2A> und <xref:System.Drawing.Graphics.EndContainer%2A> . Der zweite-Rückruf <xref:System.Drawing.Graphics.DrawRectangle%2A> ist nach dem-Befehl <xref:System.Drawing.Graphics.EndContainer%2A> .  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.MiscLegacyTopics#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#61)]  
  
 Im vorangehenden Code wird das aus dem Container gezogene Rechteck zuerst von der Welt Transformation des Containers (Drehung) und dann von der Welt Transformation des <xref:System.Drawing.Graphics> Objekts (Übersetzung) transformiert. Das Rechteck, das von außerhalb des Containers gezeichnet wird, wird nur durch die Welt Transformation des <xref:System.Drawing.Graphics> Objekts (Translation) transformiert. Die folgende Abbildung zeigt die beiden Rechtecke:
  
 ![Abbildung, in der die in einem Container dargestellten Container angezeigt werden](./media/using-nested-graphics-containers/nested-containers-illustration.png)  
  
## <a name="clipping-in-nested-containers"></a>Clipping in geschbten Containern  
 Im folgenden Beispiel wird veranschaulicht, wie die geschbten Container Clippingbereiche verarbeiten. Der Code erstellt ein <xref:System.Drawing.Graphics> -Objekt und einen Container innerhalb dieses <xref:System.Drawing.Graphics> Objekts. Der Clippingbereich des <xref:System.Drawing.Graphics> Objekts ist ein Rechteck, und der Clippingbereich des Containers ist eine Ellipse. Der Code führt zwei Aufrufe an die- <xref:System.Drawing.Graphics.DrawLine%2A> Methode aus. Der erste Rückruf von <xref:System.Drawing.Graphics.DrawLine%2A> befindet sich innerhalb des Containers, und der zweite-Aufrufwert <xref:System.Drawing.Graphics.DrawLine%2A> ist außerhalb des Containers (nach dem-Befehl <xref:System.Drawing.Graphics.EndContainer%2A> ). Die erste Zeile wird durch die Schnittmenge der beiden Clippingbereiche abgeschnitten. Die zweite Zeile wird nur durch den rechteckigen Clippingbereich des- <xref:System.Drawing.Graphics> Objekts abgeschnitten.  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#62](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#62)]
 [!code-vb[System.Drawing.MiscLegacyTopics#62](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#62)]  
  
 Die folgende Abbildung zeigt die beiden ausgeschnittenen Zeilen:
  
 ![Abbildung, in der ein schzisted Container mit ausgeschnittenen Zeilen angezeigt wird.](./media/using-nested-graphics-containers/nested-container-clipped-lines.png)  
  
 Wie die beiden vorherigen Beispiele zeigen, sind Transformationen und Clippingbereiche in geschposteten Containern kumulativ. Wenn Sie die globalen Transformationen des Containers und des- <xref:System.Drawing.Graphics> Objekts festlegen, gelten beide Transformationen für Elemente, die aus dem Container gezogen werden. Die Transformation des Containers wird zuerst angewendet, und die Transformation des <xref:System.Drawing.Graphics> Objekts wird als zweites angewendet. Wenn Sie die Clippingbereiche des Containers und des- <xref:System.Drawing.Graphics> Objekts festlegen, werden die Elemente, die aus dem Container gezogen werden, durch die Schnittmenge der beiden Clippingbereiche abgeschnitten.  
  
## <a name="quality-settings-in-nested-containers"></a>Qualitätseinstellungen in der Liste der Container  
 Die Qualitätseinstellungen ( <xref:System.Drawing.Graphics.SmoothingMode%2A> , <xref:System.Drawing.Graphics.TextRenderingHint%2A> und die like) in den in der Liste eingefügten Containern sind nicht kumulativ. stattdessen ersetzen die Qualitätseinstellungen des Containers vorübergehend die Qualitätseinstellungen eines- <xref:System.Drawing.Graphics> Objekts. Wenn Sie einen neuen Container erstellen, werden die Qualitätseinstellungen für diesen Container auf Standardwerte festgelegt. Nehmen Sie beispielsweise an, Sie verfügen über ein- <xref:System.Drawing.Graphics> Objekt mit einem Glättungs Modus von <xref:System.Drawing.Drawing2D.SmoothingMode.AntiAlias> . Wenn Sie einen Container erstellen, ist der Glättungs Modus innerhalb des Containers der standardmäßige Glättungs Modus. Sie können den Glättungs Modus des Containers festlegen, und alle Elemente, die aus dem Container gezogen werden, werden gemäß dem von Ihnen festgelegten Modus gezeichnet. Elemente, die nach dem-Aufrufvorgang gezeichnet werden, <xref:System.Drawing.Graphics.EndContainer%2A> werden gemäß dem Glättungs Modus ( <xref:System.Drawing.Drawing2D.SmoothingMode.AntiAlias> ) gezeichnet, der vor dem-Vorgang vor aufgerufen wurde <xref:System.Drawing.Graphics.BeginContainer%2A> .  
  
## <a name="several-layers-of-nested-containers"></a>Mehrere Ebenen von als Container  
 Sie sind nicht auf einen Container in einem- <xref:System.Drawing.Graphics> Objekt beschränkt. Sie können eine Reihe von Containern erstellen, die jeweils in der vorherigen geschpotet sind, und Sie können die Welt Transformation, den Clippingbereich und die Qualitätseinstellungen der einzelnen geschposteten Container angeben. Wenn Sie eine Zeichnungs Methode aus dem innersten Container heraus aufzurufen, werden die Transformationen in der richtigen Reihenfolge angewendet, beginnend mit dem innersten Container und enden mit dem äußersten Container. Elemente, die aus dem innersten Container gezeichnet werden, werden durch die Schnittmenge aller Clippingbereiche abgeschnitten.  
  
 Im folgenden Beispiel wird ein <xref:System.Drawing.Graphics> -Objekt erstellt, und der Text Rendering-Hinweis wird auf festgelegt <xref:System.Drawing.Drawing2D.SmoothingMode.AntiAlias> . Der Code erstellt zwei Container, von denen eine geschachtelt ist. Der Text Rendering-Hinweis des äußeren Containers ist auf festgelegt <xref:System.Drawing.Text.TextRenderingHint.SingleBitPerPixel> , und der Text Rendering-Hinweis des inneren Containers wird auf festgelegt <xref:System.Drawing.Drawing2D.SmoothingMode.AntiAlias> . Der Code zeichnet drei Zeichen folgen: eine aus dem inneren Container, eine aus dem äußeren Container und eine aus dem <xref:System.Drawing.Graphics> Objekt selbst.  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#63](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#63)]
 [!code-vb[System.Drawing.MiscLegacyTopics#63](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#63)]  
  
 Die folgende Abbildung zeigt die drei Zeichen folgen. Die Zeichen folgen, die aus dem inneren Container und aus dem- <xref:System.Drawing.Graphics> Objekt gezeichnet werden, werden durch Antialiasing geglättet. Die aus dem äußeren Container gezeichnete Zeichenfolge wird nicht durch Antialiasing geglättet, da die- <xref:System.Drawing.Graphics.TextRenderingHint%2A> Eigenschaft auf festgelegt ist <xref:System.Drawing.Text.TextRenderingHint.SingleBitPerPixel> .  
  
 ![Abbildung, die die Zeichen folgen anzeigt, die aus den in einem Container erstellten Containern](./media/using-nested-graphics-containers/nested-containers-three-strings.png)  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Graphics>
- [Verwalten des Zustands eines Graphics-Objekts](managing-the-state-of-a-graphics-object.md)
