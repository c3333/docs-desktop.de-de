---
title: Validieren von Daten im DataGridView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data [Windows Forms], validation
- DataGridView control [Windows Forms], data validation
- data grids [Windows Forms], validating data
- data validation [Windows Forms], Windows Forms
ms.assetid: d10aef35-701e-4a3c-a684-2a2ed1aeaca6
ms.openlocfilehash: 120a228910a4e6f45d45eaf0001c6cba33fdb733
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975580"
---
# <a name="how-to-validate-data-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="7aa49-102">Vorgehensweise: Überprüfen von Daten im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7aa49-102">How to: Validate Data in the Windows Forms DataGridView Control</span></span>

<span data-ttu-id="7aa49-103">Im folgenden Codebeispiel wird gezeigt, wie Daten validiert werden, die von einem Benutzer in ein <xref:System.Windows.Forms.DataGridView>-Steuerelement eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="7aa49-103">The following code example demonstrates how to validate data entered by a user into a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="7aa49-104">In diesem Beispiel wird die <xref:System.Windows.Forms.DataGridView> mit Zeilen aus der Tabelle `Customers` der Northwind-Beispieldatenbank gefüllt.</span><span class="sxs-lookup"><span data-stu-id="7aa49-104">In this example, the <xref:System.Windows.Forms.DataGridView> is populated with rows from the `Customers` table of the Northwind sample database.</span></span> <span data-ttu-id="7aa49-105">Wenn der Benutzer eine Zelle in der Spalte `CompanyName` bearbeitet, wird der Wert auf Gültigkeit überprüft, indem geprüft wird, dass die Zelle nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="7aa49-105">When the user edits a cell in the `CompanyName` column, its value is tested for validity by checking that it is not empty.</span></span> <span data-ttu-id="7aa49-106">Wenn der Ereignishandler für das <xref:System.Windows.Forms.DataGridView.CellValidating>-Ereignis feststellt, dass es sich bei dem Wert um eine leere Zeichenfolge handelt, sorgt die <xref:System.Windows.Forms.DataGridView> dafür, dass der Benutzer die Zelle erst verlassen kann, nachdem er eine nicht leere Zeichenfolge eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7aa49-106">If the event handler for the <xref:System.Windows.Forms.DataGridView.CellValidating> event finds that the value is an empty string, the <xref:System.Windows.Forms.DataGridView> prevents the user from exiting the cell until a non-empty string is entered.</span></span>  
  
 <span data-ttu-id="7aa49-107">Eine vollständige Erläuterung dieses Codebeispiels finden Sie unter [Exemplarische Vorgehensweise: Validieren von Daten im DataGridView-Steuerelement in Windows Forms](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="7aa49-107">For a complete explanation of this code example, see [Walkthrough: Validating Data in the Windows Forms DataGridView Control](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="7aa49-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7aa49-108">Example</span></span>  

 [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewDataValidation#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#00)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="7aa49-109">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="7aa49-109">Compiling the Code</span></span>  

 <span data-ttu-id="7aa49-110">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7aa49-110">This example requires:</span></span>  
  
- <span data-ttu-id="7aa49-111">Verweise auf die Assemblys "System", "System.Data", "System.Windows.Forms" und "System.XML".</span><span class="sxs-lookup"><span data-stu-id="7aa49-111">References to the System, System.Data, System.Windows.Forms and System.XML assemblies.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="7aa49-112">.NET Framework-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="7aa49-112">.NET Framework Security</span></span>  

 <span data-ttu-id="7aa49-113">Das Speichern vertraulicher Informationen (z. B. eines Kennworts) innerhalb der Verbindungszeichenfolge kann die Sicherheit einer Anwendung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="7aa49-113">Storing sensitive information, such as a password, within the connection string can affect the security of your application.</span></span> <span data-ttu-id="7aa49-114">Der Zugriff auf eine Datenbank lässt sich mithilfe der Windows-Authentifizierung (wird auch als integrierte Sicherheit bezeichnet) sicherer steuern.</span><span class="sxs-lookup"><span data-stu-id="7aa49-114">Using Windows Authentication (also known as integrated security) is a more secure way to control access to a database.</span></span> <span data-ttu-id="7aa49-115">Weitere Informationen finden Sie unter [Protecting Connection Information (Schützen von Verbindungsinformationen)](/dotnet/framework/data/adonet/protecting-connection-information).</span><span class="sxs-lookup"><span data-stu-id="7aa49-115">For more information, see [Protecting Connection Information](/dotnet/framework/data/adonet/protecting-connection-information).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7aa49-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7aa49-116">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="7aa49-117">Exemplarische Vorgehensweise: Validieren von Daten im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7aa49-117">Walkthrough: Validating Data in the Windows Forms DataGridView Control</span></span>](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="7aa49-118">Dateneingabe im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7aa49-118">Data Entry in the Windows Forms DataGridView Control</span></span>](data-entry-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="7aa49-119">Exemplarische Vorgehensweise: Behandeln von Fehlern, die während der Dateneingabe im DataGridView-Steuerelement in Windows Forms auftreten</span><span class="sxs-lookup"><span data-stu-id="7aa49-119">Walkthrough: Handling Errors that Occur During Data Entry in the Windows Forms DataGridView Control</span></span>](handling-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [<span data-ttu-id="7aa49-120">Schützen von Verbindungsinformationen</span><span class="sxs-lookup"><span data-stu-id="7aa49-120">Protecting Connection Information</span></span>](/dotnet/framework/data/adonet/protecting-connection-information)
