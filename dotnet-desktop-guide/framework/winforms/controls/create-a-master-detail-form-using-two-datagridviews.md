---
title: Erstellen eines Master-Detail Formulars mit zwei DataGridView-Steuerelementen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], master/detail form
- parent-child tables [Windows Forms], displaying on Windows Forms
- master-details lists [Windows Forms], creating
ms.assetid: 99f6e876-3f7f-4139-9063-e36587c95b02
ms.openlocfilehash: d490af6517e7e45bb2dd48ab7d41c468a7eba2aa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972215"
---
# <a name="how-to-create-a-masterdetail-form-using-two-windows-forms-datagridview-controls"></a><span data-ttu-id="04135-102">Vorgehensweise: Erstellen eines Master-/Detailformulars mit zwei DataGridView-Steuerelementen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="04135-102">How to: Create a Master/Detail Form Using Two Windows Forms DataGridView Controls</span></span>

<span data-ttu-id="04135-103">Im folgenden Codebeispiel wird ein Master-/Detailformular mit zwei <xref:System.Windows.Forms.DataGridView>-Steuerelementen erstellt, die an zwei <xref:System.Windows.Forms.BindingSource>-Komponenten gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="04135-103">The following code example creates a master/detail form using two <xref:System.Windows.Forms.DataGridView> controls bound to two <xref:System.Windows.Forms.BindingSource> components.</span></span> <span data-ttu-id="04135-104">Die Datenquelle ist ein <xref:System.Data.DataSet>, das die Tabellen `Customers` und `Orders` aus der SQL Server-Beispieldatenbank "Northwind" sowie eine <xref:System.Data.DataRelation> enthält, mit der die beiden Tabellen über die Spalte `CustomerID` in Beziehung gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="04135-104">The data source is a <xref:System.Data.DataSet> that contains the `Customers` and `Orders` tables from the Northwind SQL Server sample database along with a <xref:System.Data.DataRelation> that relates the two through the `CustomerID` column.</span></span>  
  
 <span data-ttu-id="04135-105">Eine <xref:System.Windows.Forms.BindingSource> ist an die übergeordnete `Customers`-Tabelle im DataSet gebunden.</span><span class="sxs-lookup"><span data-stu-id="04135-105">One <xref:System.Windows.Forms.BindingSource> is bound to the parent `Customers` table in the data set.</span></span> <span data-ttu-id="04135-106">Diese Daten werden im <xref:System.Windows.Forms.DataGridView>-Mastersteuerelement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="04135-106">This data is displayed in the master <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="04135-107">Die andere <xref:System.Windows.Forms.BindingSource>  ist an die erste Datenverbindung gebunden.</span><span class="sxs-lookup"><span data-stu-id="04135-107">The other <xref:System.Windows.Forms.BindingSource> is bound to the first data connector.</span></span> <span data-ttu-id="04135-108">Die <xref:System.Windows.Forms.BindingSource.DataMember%2A>-Eigenschaft der zweiten <xref:System.Windows.Forms.BindingSource> ist auf den Namen der <xref:System.Data.DataRelation> festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04135-108">The <xref:System.Windows.Forms.BindingSource.DataMember%2A> property of the second <xref:System.Windows.Forms.BindingSource> is set to the <xref:System.Data.DataRelation> name.</span></span> <span data-ttu-id="04135-109">Dadurch zeigt das zugeordnete <xref:System.Windows.Forms.DataGridView>-Detailsteuerelement die Zeilen der untergeordneten `Orders`-Tabelle an, die der aktuellen Zeile im <xref:System.Windows.Forms.DataGridView>-Mastersteuerelement entsprechen.</span><span class="sxs-lookup"><span data-stu-id="04135-109">This causes the associated detail <xref:System.Windows.Forms.DataGridView> control to display the rows of the child `Orders` table that correspond to the current row in the master <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <span data-ttu-id="04135-110">Eine ausführliche Erläuterung dieses Code Beispiels finden Sie unter Exemplarische Vorgehensweise [: Erstellen eines Master-/Detailformulars mit zwei Windows Forms DataGridView-Steuerelementen](creating-a-master-detail-form-using-two-datagridviews.md).</span><span class="sxs-lookup"><span data-stu-id="04135-110">For a complete explanation of this code example, see [Walkthrough: Creating a Master/Detail Form Using Two Windows Forms DataGridView Controls](creating-a-master-detail-form-using-two-datagridviews.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="04135-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="04135-111">Example</span></span>  

 [!code-csharp[System.Windows.Forms.DataGridViewMasterDetails#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMasterDetails/CS/masterdetails.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewMasterDetails#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMasterDetails/VB/masterdetails.vb#00)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="04135-112">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="04135-112">Compiling the Code</span></span>  

 <span data-ttu-id="04135-113">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="04135-113">This example requires:</span></span>  
  
 <span data-ttu-id="04135-114">Verweise auf die Assemblys "System", "System.Data", "System.Windows.Forms" und "System.XML".</span><span class="sxs-lookup"><span data-stu-id="04135-114">References to the System, System.Data, System.Windows.Forms, and System.XML assemblies.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="04135-115">.NET Framework-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="04135-115">.NET Framework Security</span></span>  

 <span data-ttu-id="04135-116">Das Speichern vertraulicher Informationen (z. B. eines Kennworts) innerhalb der Verbindungszeichenfolge kann die Sicherheit einer Anwendung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="04135-116">Storing sensitive information, such as a password, within the connection string can affect the security of your application.</span></span> <span data-ttu-id="04135-117">Der Zugriff auf eine Datenbank lässt sich mithilfe der Windows-Authentifizierung (wird auch als integrierte Sicherheit bezeichnet) sicherer steuern.</span><span class="sxs-lookup"><span data-stu-id="04135-117">Using Windows Authentication (also known as integrated security) is a more secure way to control access to a database.</span></span> <span data-ttu-id="04135-118">Weitere Informationen finden Sie unter [Protecting Connection Information (Schützen von Verbindungsinformationen)](/dotnet/framework/data/adonet/protecting-connection-information).</span><span class="sxs-lookup"><span data-stu-id="04135-118">For more information, see [Protecting Connection Information](/dotnet/framework/data/adonet/protecting-connection-information).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04135-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04135-119">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="04135-120">Exemplarische Vorgehensweise: Erstellen eines Master-/Detailformulars mit zwei DataGridView-Steuerelementen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="04135-120">Walkthrough: Creating a Master/Detail Form Using Two Windows Forms DataGridView Controls</span></span>](creating-a-master-detail-form-using-two-datagridviews.md)
- [<span data-ttu-id="04135-121">Anzeigen von Daten im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="04135-121">Displaying Data in the Windows Forms DataGridView Control</span></span>](displaying-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="04135-122">Schützen von Verbindungsinformationen</span><span class="sxs-lookup"><span data-stu-id="04135-122">Protecting Connection Information</span></span>](/dotnet/framework/data/adonet/protecting-connection-information)
