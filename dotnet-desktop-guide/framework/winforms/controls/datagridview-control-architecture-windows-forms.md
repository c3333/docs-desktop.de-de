---
title: Architektur des DataGridView-Steuerelements
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], architecture
ms.assetid: 1c6cabf0-02ee-4bbc-9574-b54bb7f5b19e
ms.openlocfilehash: 2e1884383cca87f8d4ff84f486e2b29761a0c55d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972175"
---
# <a name="datagridview-control-architecture-windows-forms"></a>Architektur des DataGridView-Steuerelements (Windows Forms)
Das <xref:System.Windows.Forms.DataGridView> -Steuerelement und die zugehörigen Klassen sind als flexibles, erweiterbares System zum Anzeigen und Bearbeiten von Tabellendaten konzipiert. Diese Klassen sind alle im <xref:System.Windows.Forms?displayProperty=nameWithType> -Namespace enthalten, und alle werden mit dem Präfix "DataGridView" benannt.  
  
## <a name="architecture-elements"></a>Architekturelemente  
 Die primären <xref:System.Windows.Forms.DataGridView> Begleit Klassen werden von abgeleitet <xref:System.Windows.Forms.DataGridViewElement> . Das folgende Objektmodell veranschaulicht die <xref:System.Windows.Forms.DataGridViewElement> Vererbungs Hierarchie.  
  
 ![Diagramm, das die datagridviewelements-Objektmodell Hierarchie anzeigt.](./media/datagridview-control-architecture-windows-forms/datagridviewelement-object-model.gif)  
  
 Die <xref:System.Windows.Forms.DataGridViewElement> -Klasse stellt einen Verweis auf das übergeordnete Steuerelement bereit <xref:System.Windows.Forms.DataGridView> und verfügt über eine- <xref:System.Windows.Forms.DataGridViewElement.State%2A> Eigenschaft, die einen Wert enthält, der eine Kombination von Werten aus der- <xref:System.Windows.Forms.DataGridViewElementStates> Enumeration darstellt.  
  
 In den folgenden Abschnitten werden die <xref:System.Windows.Forms.DataGridView> Begleit Klassen ausführlicher beschrieben.  
  
### <a name="datagridviewelementstates"></a>DataGridViewElementStates  
 Die <xref:System.Windows.Forms.DataGridViewElementStates>-Enumeration verfügt über folgende Werte:  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.None>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.Frozen>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.ReadOnly>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.Resizable>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.ResizableSet>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.Selected>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.Visible>  
  
 Die Werte dieser Enumeration können mit den bitweisen logischen Operatoren kombiniert werden, sodass die- <xref:System.Windows.Forms.DataGridViewElement.State%2A> Eigenschaft mehr als einen Status gleichzeitig Ausdrücken kann. Beispielsweise kann ein <xref:System.Windows.Forms.DataGridViewElement> gleichzeitig <xref:System.Windows.Forms.DataGridViewElementStates.Frozen> , <xref:System.Windows.Forms.DataGridViewElementStates.Selected> und sein <xref:System.Windows.Forms.DataGridViewElementStates.Visible> .  
  
### <a name="cells-and-bands"></a>Zellen und Bänder  
 Das- <xref:System.Windows.Forms.DataGridView> Steuerelement besteht aus zwei grundlegenden Arten von Objekten: Zellen und Bänder. Alle Zellen werden von der <xref:System.Windows.Forms.DataGridViewCell> Basisklasse abgeleitet. Die beiden Arten von Bändern, <xref:System.Windows.Forms.DataGridViewColumn> und <xref:System.Windows.Forms.DataGridViewRow> , werden beide von der- <xref:System.Windows.Forms.DataGridViewBand> Basisklasse abgeleitet.  
  
 Das- <xref:System.Windows.Forms.DataGridView> Steuerelement interagiert mit mehreren Klassen, aber die am häufigsten gefundenen sind <xref:System.Windows.Forms.DataGridViewCell> , <xref:System.Windows.Forms.DataGridViewColumn> und <xref:System.Windows.Forms.DataGridViewRow> .  
  
### <a name="datagridviewcell"></a>DataGridViewCell  
 Die Zelle ist die grundlegende Einheit der Interaktion für das <xref:System.Windows.Forms.DataGridView> . Die Anzeige wird auf Zellen zentriert, und der Dateneintrag wird häufig durch Zellen durchgeführt. Mithilfe der-Auflistung der-Klasse können Sie auf Zellen zugreifen <xref:System.Windows.Forms.DataGridViewRow.Cells%2A> <xref:System.Windows.Forms.DataGridViewRow> , und Sie können mithilfe der-Auflistung des-Steuer Elements auf die ausgewählten Zellen zugreifen <xref:System.Windows.Forms.DataGridView.SelectedCells%2A> <xref:System.Windows.Forms.DataGridView> . Das folgende Objektmodell veranschaulicht diese Verwendung und zeigt die <xref:System.Windows.Forms.DataGridViewCell> Vererbungs Hierarchie.  
  
 ![Diagramm, das die DataGridViewCell-Objektmodell Hierarchie anzeigt.](./media/datagridview-control-architecture-windows-forms/datagridviewcell-object-model.gif)  
  
 Der <xref:System.Windows.Forms.DataGridViewCell> Typ ist eine abstrakte Basisklasse, von der alle Zelltypen abgeleitet werden. <xref:System.Windows.Forms.DataGridViewCell> und die abgeleiteten Typen sind keine Windows Forms Steuerelemente, sondern einige Host Windows Forms-Steuerelemente. Alle von einer Zelle unterstützten Bearbeitungsfunktionen werden in der Regel von einem gehosteten Steuerelement behandelt.  
  
 <xref:System.Windows.Forms.DataGridViewCell> -Objekte steuern ihre eigenen Erscheinungsbild-und Zeichnungsfunktionen nicht auf die gleiche Weise wie Windows Forms-Steuerelemente. Stattdessen ist der <xref:System.Windows.Forms.DataGridView> für das Aussehen seiner <xref:System.Windows.Forms.DataGridViewCell> Objekte verantwortlich. Sie können die Darstellung und das Verhalten von Zellen durch Interaktion mit den <xref:System.Windows.Forms.DataGridView> Eigenschaften und Ereignissen des-Steuer Elements erheblich beeinflussen. Wenn Sie besondere Anforderungen an Anpassungen haben, die über die Funktionen des Steuer Elements hinausgehen <xref:System.Windows.Forms.DataGridView> , können Sie eine eigene Klasse implementieren, die von <xref:System.Windows.Forms.DataGridViewCell> oder einer ihrer untergeordneten Klassen abgeleitet ist.  
  
 Die folgende Liste zeigt die Klassen, die von abgeleitet sind <xref:System.Windows.Forms.DataGridViewCell> :  
  
- <xref:System.Windows.Forms.DataGridViewTextBoxCell>  
  
- <xref:System.Windows.Forms.DataGridViewButtonCell>  
  
- <xref:System.Windows.Forms.DataGridViewLinkCell>  
  
- <xref:System.Windows.Forms.DataGridViewCheckBoxCell>  
  
- <xref:System.Windows.Forms.DataGridViewComboBoxCell>  
  
- <xref:System.Windows.Forms.DataGridViewImageCell>  
  
- <xref:System.Windows.Forms.DataGridViewHeaderCell>  
  
- <xref:System.Windows.Forms.DataGridViewRowHeaderCell>  
  
- <xref:System.Windows.Forms.DataGridViewColumnHeaderCell>  
  
- <xref:System.Windows.Forms.DataGridViewTopLeftHeaderCell>  
  
- Ihre benutzerdefinierten Zelltypen  
  
### <a name="datagridviewcolumn"></a>DataGridViewColumn  
 Das Schema des <xref:System.Windows.Forms.DataGridView> angefügten Datenspeicher des Steuer Elements wird in den <xref:System.Windows.Forms.DataGridView> Spalten des Steuer Elements ausgedrückt. Sie können auf die <xref:System.Windows.Forms.DataGridView> Spalten des Steuer Elements mithilfe der-Auflistung zugreifen <xref:System.Windows.Forms.DataGridView.Columns%2A> . Sie können auf die ausgewählten Spalten zugreifen, indem Sie die-Auflistung verwenden <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A> . Das folgende Objektmodell veranschaulicht diese Verwendung und zeigt die <xref:System.Windows.Forms.DataGridViewColumn> Vererbungs Hierarchie.  
  
 ![Diagramm, das die DataGridViewColumn-Objektmodell Hierarchie anzeigt.](./media/datagridview-control-architecture-windows-forms/datagridviewcolumn-object-model.gif)  
  
 Einige der Schlüssel Zelltypen weisen entsprechende Spaltentypen auf. Diese werden von der- <xref:System.Windows.Forms.DataGridViewColumn> Basisklasse abgeleitet.  
  
 Die folgende Liste zeigt die Klassen, die von abgeleitet sind <xref:System.Windows.Forms.DataGridViewColumn> :  
  
- <xref:System.Windows.Forms.DataGridViewButtonColumn>  
  
- <xref:System.Windows.Forms.DataGridViewCheckBoxColumn>  
  
- <xref:System.Windows.Forms.DataGridViewComboBoxColumn>  
  
- <xref:System.Windows.Forms.DataGridViewImageColumn>  
  
- <xref:System.Windows.Forms.DataGridViewTextBoxColumn>  
  
- <xref:System.Windows.Forms.DataGridViewLinkColumn>  
  
- Ihre benutzerdefinierten Spaltentypen  
  
### <a name="datagridview-editing-controls"></a>DataGridView-Bearbeitungs Steuerelemente  
 Zellen, die erweiterte Bearbeitungsfunktionen unterstützen, verwenden normalerweise ein gehosteter Steuerelement, das von einem Windows Forms Steuerelement abgeleitet ist. Diese Steuerelemente implementieren auch die- <xref:System.Windows.Forms.IDataGridViewEditingControl> Schnittstelle. Das folgende Objektmodell veranschaulicht die Verwendung dieser Steuerelemente.  
  
 ![Diagramm, das die DataGridView-Bearbeitungs Steuerelement-Objektmodell Hierarchie anzeigt.](./media/datagridview-control-architecture-windows-forms/datagridviewediting-object-model.gif)  
  
 Die folgenden Bearbeitungs Steuerelemente werden mit dem-Steuerelement bereitgestellt <xref:System.Windows.Forms.DataGridView> :  
  
- <xref:System.Windows.Forms.DataGridViewComboBoxEditingControl>  
  
- <xref:System.Windows.Forms.DataGridViewTextBoxEditingControl>  
  
 Weitere Informationen zum Erstellen eigener Bearbeitungs Steuerelemente finden Sie unter Gewusst [wie: Hosten von Steuerelementen in Windows Forms DataGridView-Zellen](how-to-host-controls-in-windows-forms-datagridview-cells.md).  
  
 In der folgenden Tabelle wird die Beziehung zwischen Zellen Typen, Spaltentypen und Bearbeitungs Steuerelementen veranschaulicht.  
  
|Zellentyp|Gehosteter Steuerelement|Spaltentyp|  
|---------------|--------------------|-----------------|  
|<xref:System.Windows.Forms.DataGridViewButtonCell>|–|<xref:System.Windows.Forms.DataGridViewButtonColumn>|  
|<xref:System.Windows.Forms.DataGridViewCheckBoxCell>|–|<xref:System.Windows.Forms.DataGridViewCheckBoxColumn>|  
|<xref:System.Windows.Forms.DataGridViewComboBoxCell>|<xref:System.Windows.Forms.DataGridViewComboBoxEditingControl>|<xref:System.Windows.Forms.DataGridViewComboBoxColumn>|  
|<xref:System.Windows.Forms.DataGridViewImageCell>|–|<xref:System.Windows.Forms.DataGridViewImageColumn>|  
|<xref:System.Windows.Forms.DataGridViewLinkCell>|–|<xref:System.Windows.Forms.DataGridViewLinkColumn>|  
|<xref:System.Windows.Forms.DataGridViewTextBoxCell>|<xref:System.Windows.Forms.DataGridViewTextBoxEditingControl>|<xref:System.Windows.Forms.DataGridViewTextBoxColumn>|  
  
### <a name="datagridviewrow"></a>DataGridViewRow  
 Die <xref:System.Windows.Forms.DataGridViewRow> -Klasse zeigt die Datenfelder eines Datensatzes aus dem Datenspeicher an, an den das <xref:System.Windows.Forms.DataGridView> Steuerelement angefügt ist. <xref:System.Windows.Forms.DataGridView>Mithilfe der-Auflistung können Sie auf die Zeilen des-Steuer Elements zugreifen <xref:System.Windows.Forms.DataGridView.Rows%2A> . Sie können auf die ausgewählten Zeilen zugreifen, indem Sie die-Auflistung verwenden <xref:System.Windows.Forms.DataGridView.SelectedRows%2A> . Das folgende Objektmodell veranschaulicht diese Verwendung und zeigt die <xref:System.Windows.Forms.DataGridViewRow> Vererbungs Hierarchie.  
  
 ![Diagramm, das die DataGridViewRow-Objektmodell Hierarchie anzeigt.](./media/datagridview-control-architecture-windows-forms/datagridviewrow-object-model.gif)
  
 Sie können eigene Typen aus der- <xref:System.Windows.Forms.DataGridViewRow> Klasse ableiten, obwohl dies in der Regel nicht erforderlich ist. Das <xref:System.Windows.Forms.DataGridView> -Steuerelement verfügt über mehrere Zeilen bezogene Ereignisse und Eigenschaften, mit denen das Verhalten seiner Objekte angepasst werden soll <xref:System.Windows.Forms.DataGridViewRow> .  
  
 Wenn Sie die <xref:System.Windows.Forms.DataGridView> -Eigenschaft des Steuer Elements aktivieren <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A> , wird eine spezielle Zeile zum Hinzufügen neuer Zeilen als letzte Zeile angezeigt. Diese Zeile ist Teil der Auflistung <xref:System.Windows.Forms.DataGridView.Rows%2A> , verfügt jedoch über spezielle Funktionen, die möglicherweise Ihre Aufmerksamkeit erfordern. Weitere Informationen finden Sie unter [Verwenden der Zeile für neue Datensätze im Windows Forms DataGridView-Steuer](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md)Element.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über das DataGridView-Steuerelement](datagridview-control-overview-windows-forms.md)
- [Anpassen des DataGridView-Steuerelements von Windows Forms](customizing-the-windows-forms-datagridview-control.md)
- [Verwenden der Zeile für neue Datensätze im DataGridView-Steuerelement in Windows Forms](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md)
