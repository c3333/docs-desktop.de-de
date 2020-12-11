---
title: Das AutoSize-Verhalten im TableLayoutPanel-Steuerelement
ms.date: 03/30/2017
ms.topic: overview
helpviewer_keywords:
- AutoSize property [Windows Forms], tableLayoutPanel control
- controls [Windows Forms], sizing
- localizing forms
- layout [Windows Forms], AutoSize
- sizing [Windows Forms], automatic
- TableLayoutPanel control [Windows Forms], AutoSize behavior
- automatic sizing
- AutoSizeMode property
ms.assetid: 9233e0c3-2fa6-405e-8701-959479b1250e
ms.openlocfilehash: daeca48c4fcfaf83d6506ba07d60ec2dcfdcace7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975788"
---
# <a name="autosize-behavior-in-the-tablelayoutpanel-control"></a>Das AutoSize-Verhalten im TableLayoutPanel-Steuerelement
## <a name="distinct-autosize-behaviors"></a>Eindeutige automatische Größen Verhalten  
 Das- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement unterstützt das automatische Größen Anpassungs Verhalten auf folgende Weise:  
  
- Durch die- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft.  
  
- Durch die <xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A> -Eigenschaft der <xref:System.Windows.Forms.TableLayoutPanel> Spalten-und Zeilen Stile des Steuer Elements.  
  
### <a name="the-autosize-property-with-row-and-column-styles"></a>Die AutoSize-Eigenschaft mit Zeilen-und Spalten Formaten.  
 In der folgenden Tabelle wird die Interaktion zwischen der <xref:System.Windows.Forms.Control.AutoSize%2A> -Eigenschaft und den <xref:System.Windows.Forms.TableLayoutPanel> Spalten-und Zeilen Stilen des-Steuer Elements beschrieben.  
  
|AutoSize-Einstellung|Stil Interaktion|  
|----------------------|-----------------------|  
|`false`|Das <xref:System.Windows.Forms.TableLayoutPanel> -Steuerelement wird von links nach rechts fortgesetzt, und es wird Speicherplatz für die Spalte oder Zeile oder in der folgenden Reihenfolge zugewiesen.<br /><br /> 1. wenn die- <xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A> Eigenschaft auf festgelegt ist <xref:System.Windows.Forms.SizeType.Absolute> , wird die Anzahl der Pixel zugeordnet, die von oder angegeben werden <xref:System.Windows.Forms.ColumnStyle.Width%2A> <xref:System.Windows.Forms.RowStyle.Height%2A> .<br />2. wenn die <xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A> -Eigenschaft auf festgelegt ist <xref:System.Windows.Forms.SizeType.AutoSize> , wird die Anzahl der Pixel zugewiesen, die von der-Methode des untergeordneten Steuer Elements zurückgegeben wird <xref:System.Windows.Forms.Control.GetPreferredSize%2A> .<br />3. nach dem Zuordnen von Speicherplatz für alle <xref:System.Windows.Forms.SizeType.Absolute> -und- <xref:System.Windows.Forms.SizeType.AutoSize> Spalten oder-Zeilen werden alle Spalten oder Zeilen mit <xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A> fest geleggelegten Wert <xref:System.Windows.Forms.SizeType.Percent> verwendet, um proportional den verbleibenden freien Speicherplatz zuzuordnen.|  
|`true`|Ähnlich wie bei der vorherigen Interaktion, mit der Ausnahme, dass <xref:System.Windows.Forms.SizeType.Percent> Spalten oder Zeilen einen automatischen Größen Anpassungs Aspekt erhalten.<br /><br /> Mit dem- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement wird die Spalte oder Zeile erweitert, um ausreichenden freien Speicherplatz zu schaffen, sodass keine Spalte oder Zeile mit Formatvorlagen für <xref:System.Windows.Forms.SizeType.Percent> den Inhalt angezeigt wird. Das- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement ordnet den neuen Platz proportional entsprechend der- <xref:System.Windows.Forms.ColumnStyle.Width%2A> Eigenschaft oder der-Eigenschaft zu <xref:System.Windows.Forms.RowStyle.Height%2A> .|  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.TableLayoutPanel>
- [Übersicht über das TableLayoutPanel-Steuerelement](tablelayoutpanel-control-overview.md)
