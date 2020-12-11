---
title: Behandeln von Fehlern, die während der Dateneingabe im DataGridView-Steuerelement auftreten
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- error handling [Windows Forms], dataGridView control
- data grids [Windows Forms], error handling
- DataGridView control [Windows Forms], error handling
- data entry [Windows Forms], error handling
- error handling [Windows Forms], data entry
ms.assetid: 9004e72f-fdec-4264-a37d-2c99764efc13
ms.openlocfilehash: 3753bc750c9988b586e3d1c9cabf6672ff44bff7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975764"
---
# <a name="how-to-handle-errors-that-occur-during-data-entry-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="516e7-102">Vorgehensweise: Behandeln von Fehlern, die während der Dateneingabe im DataGridView-Steuerelement in Windows Forms auftreten</span><span class="sxs-lookup"><span data-stu-id="516e7-102">How to: Handle Errors That Occur During Data Entry in the Windows Forms DataGridView Control</span></span>

<span data-ttu-id="516e7-103">Im folgenden Codebeispiel wird veranschaulicht, wie das <xref:System.Windows.Forms.DataGridView>-Steuerelement verwendet wird, um dem Benutzer Dateneingabefehler zu melden.</span><span class="sxs-lookup"><span data-stu-id="516e7-103">The following code example demonstrates how to use the <xref:System.Windows.Forms.DataGridView> control to report data entry errors to the user.</span></span>  
  
 <span data-ttu-id="516e7-104">Eine ausführliche Erläuterung dieses Code Beispiels finden Sie unter Exemplarische Vorgehensweise [: Behandeln von Fehlern, die während der Dateneingabe im Windows Forms DataGridView-Steuerelement auftreten](handling-errors-that-occur-during-data-entry-in-the-datagrid.md).</span><span class="sxs-lookup"><span data-stu-id="516e7-104">For a complete explanation of this code example, see [Walkthrough: Handling Errors that Occur During Data Entry in the Windows Forms DataGridView Control](handling-errors-that-occur-during-data-entry-in-the-datagrid.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="516e7-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="516e7-105">Example</span></span>  

 [!code-csharp[System.Windows.Forms.DataGridView.DataError#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridView.DataError#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#00)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="516e7-106">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="516e7-106">Compiling the Code</span></span>  

 <span data-ttu-id="516e7-107">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="516e7-107">This example requires:</span></span>  
  
- <span data-ttu-id="516e7-108">Verweise auf die Assemblys "System", "System.Data", "System.Windows.Forms" und "System.XML".</span><span class="sxs-lookup"><span data-stu-id="516e7-108">References to the System, System.Data, System.Windows.Forms, and System.XML assemblies.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="516e7-109">.NET Framework-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="516e7-109">.NET Framework Security</span></span>  

 <span data-ttu-id="516e7-110">Das Speichern vertraulicher Informationen (z. B. eines Kennworts) innerhalb der Verbindungszeichenfolge kann die Sicherheit einer Anwendung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="516e7-110">Storing sensitive information, such as a password, within the connection string can affect the security of your application.</span></span> <span data-ttu-id="516e7-111">Der Zugriff auf eine Datenbank lässt sich mithilfe der Windows-Authentifizierung (wird auch als integrierte Sicherheit bezeichnet) sicherer steuern.</span><span class="sxs-lookup"><span data-stu-id="516e7-111">Using Windows Authentication (also known as integrated security) is a more secure way to control access to a database.</span></span> <span data-ttu-id="516e7-112">Weitere Informationen finden Sie unter [Protecting Connection Information (Schützen von Verbindungsinformationen)](/dotnet/framework/data/adonet/protecting-connection-information).</span><span class="sxs-lookup"><span data-stu-id="516e7-112">For more information, see [Protecting Connection Information](/dotnet/framework/data/adonet/protecting-connection-information).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="516e7-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="516e7-113">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="516e7-114">Exemplarische Vorgehensweise: Behandeln von Fehlern, die während der Dateneingabe im DataGridView-Steuerelement in Windows Forms auftreten</span><span class="sxs-lookup"><span data-stu-id="516e7-114">Walkthrough: Handling Errors that Occur During Data Entry in the Windows Forms DataGridView Control</span></span>](handling-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [<span data-ttu-id="516e7-115">Dateneingabe im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="516e7-115">Data Entry in the Windows Forms DataGridView Control</span></span>](data-entry-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="516e7-116">Exemplarische Vorgehensweise: Validieren von Daten im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="516e7-116">Walkthrough: Validating Data in the Windows Forms DataGridView Control</span></span>](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="516e7-117">Schützen von Verbindungsinformationen</span><span class="sxs-lookup"><span data-stu-id="516e7-117">Protecting Connection Information</span></span>](/dotnet/framework/data/adonet/protecting-connection-information)
