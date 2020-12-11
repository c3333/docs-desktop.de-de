---
title: Binden von Steuerelementen an die BindingSource-Komponente mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], binding
- BindingSource component [Windows Forms], binding controls
- data binding [Windows Forms], BindingSource component
ms.assetid: 391ae170-de5c-40f8-8233-91cb2ee4683a
ms.openlocfilehash: ec4e556e855a2c86dc280e1c386e9dabc2319c57
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975784"
---
# <a name="how-to-bind-windows-forms-controls-with-the-bindingsource-component-using-the-designer"></a><span data-ttu-id="1c361-102">Vorgehensweise: Binden von Windows Forms-Steuerelementen an die BindingSource-Komponente mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="1c361-102">How to: Bind Windows Forms Controls with the BindingSource Component Using the Designer</span></span>

<span data-ttu-id="1c361-103">Nachdem Sie dem Formular Steuerelemente hinzugefügt und die Benutzeroberfläche für die Anwendung bestimmt haben, können Sie die Steuerelemente an eine Datenquelle binden, sodass Benutzer zur Laufzeit Daten im Zusammenhang mit der Anwendung ändern und speichern können.</span><span class="sxs-lookup"><span data-stu-id="1c361-103">After you have added controls to your form and determined the user interface for your application, you can bind the controls to a data source, so that, at run time, users can alter and save data related to the application.</span></span>

 <span data-ttu-id="1c361-104">Das Binden eines Steuer Elements oder einer Reihe von Steuerelementen in Windows Forms wird am einfachsten mit dem- <xref:System.Windows.Forms.BindingSource> Steuerelement als Brücke zwischen den Steuerelementen auf dem Formular und der Datenquelle erreicht.</span><span class="sxs-lookup"><span data-stu-id="1c361-104">Binding a control or series of controls in Windows Forms is most easily accomplished using the <xref:System.Windows.Forms.BindingSource> control as a bridge between the controls on the form and the data source.</span></span>

 <span data-ttu-id="1c361-105">Mindestens ein Steuerelement in einem Formular kann an Daten gebunden werden. in der folgenden Prozedur ist ein- <xref:System.Windows.Forms.TextBox> Steuerelement an eine Datenquelle gebunden.</span><span class="sxs-lookup"><span data-stu-id="1c361-105">One or more controls on a form can be bound to data; in the following procedure, a <xref:System.Windows.Forms.TextBox> control is bound to a data source.</span></span>

 <span data-ttu-id="1c361-106">Um das Verfahren abzuschließen, wird davon ausgegangen, dass Sie eine Bindung an eine Datenquelle herstellen, die von einer Datenbank abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="1c361-106">To complete the procedure, it is assumed that you will bind to a data source derived from a database.</span></span> <span data-ttu-id="1c361-107">Weitere Informationen zum Erstellen von Datenquellen aus anderen Daten speichern finden Sie unter [Hinzufügen neuer Datenquellen](/visualstudio/data-tools/add-new-data-sources).</span><span class="sxs-lookup"><span data-stu-id="1c361-107">For more information on creating data sources from other stores of data, see [Add new data sources](/visualstudio/data-tools/add-new-data-sources).</span></span>

## <a name="to-bind-a-control-at-design-time"></a><span data-ttu-id="1c361-108">So binden Sie ein Steuerelement zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="1c361-108">To bind a control at design time</span></span>

1. <span data-ttu-id="1c361-109">Ziehen Sie ein- <xref:System.Windows.Forms.TextBox> Steuerelement auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="1c361-109">Drag a <xref:System.Windows.Forms.TextBox> control on to the form.</span></span>

2. <span data-ttu-id="1c361-110">Im **Eigenschaften** Fenster:</span><span class="sxs-lookup"><span data-stu-id="1c361-110">In the **Properties** window:</span></span>

    1. <span data-ttu-id="1c361-111">Erweitern Sie den Knoten **(DataBindings)** .</span><span class="sxs-lookup"><span data-stu-id="1c361-111">Expand the **(DataBindings)** node.</span></span>

    2. <span data-ttu-id="1c361-112">Klicken Sie auf den Pfeil neben der- <xref:System.Windows.Forms.TextBox.Text%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1c361-112">Click the arrow next to the <xref:System.Windows.Forms.TextBox.Text%2A> property.</span></span>

         <span data-ttu-id="1c361-113">Der Benutzeroberflächen-Typ-Editor für die **Daten** Quelle wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1c361-113">The **DataSource** UI type editor opens.</span></span>

         <span data-ttu-id="1c361-114">Wenn eine Datenquelle bereits für das Projekt oder Formular konfiguriert wurde, wird Sie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c361-114">If a data source has previously been configured for the project or form, it will appear.</span></span>

3. <span data-ttu-id="1c361-115">Klicken Sie auf **Projektdatenquelle hinzufügen**, um die Daten zu verbinden und die Datenquelle zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="1c361-115">Click **Add Project Data Source** to connect to data and create a data source.</span></span>

4. <span data-ttu-id="1c361-116">Klicken Sie auf der Startseite des **Assistenten zum Konfigurieren von Datenquellen** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="1c361-116">On the **Data Source Configuration Wizard** welcome page, click **Next**.</span></span>

5. <span data-ttu-id="1c361-117">Wählen Sie auf der Seite **Daten Quellentyp auswählen** die Option **Datenbank** aus.</span><span class="sxs-lookup"><span data-stu-id="1c361-117">On the **Choose a Data Source Type** page, select **Database**.</span></span>

6. <span data-ttu-id="1c361-118">Wählen Sie auf der Seite **Wählen Sie Ihre Datenverbindung** aus eine Datenverbindung aus der Liste der verfügbaren Verbindungen aus.</span><span class="sxs-lookup"><span data-stu-id="1c361-118">On the **Choose Your Data Connection** page, select a data connection from the list of available connections.</span></span> <span data-ttu-id="1c361-119">Wenn die gewünschte Datenverbindung nicht verfügbar ist, wählen Sie **neue Verbindung** aus, um eine neue Datenverbindung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c361-119">If your desired data connection is not available select **New Connection** to create a new data connection.</span></span>

7. <span data-ttu-id="1c361-120">Wählen Sie **Ja, Verbindung speichern,** um die Verbindungs Zeichenfolge in der Anwendungs Konfigurationsdatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1c361-120">Select **Yes, save the connection** to save the connection string in the application configuration file.</span></span>

8. <span data-ttu-id="1c361-121">Wählen Sie die Datenbankobjekte, die in die Anwendung gebracht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1c361-121">Select the database objects to bring into your application.</span></span> <span data-ttu-id="1c361-122">Wählen Sie in diesem Fall ein Feld in einer Tabelle aus, das Sie <xref:System.Windows.Forms.TextBox> anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="1c361-122">In this case, select a field in a table that you would like the <xref:System.Windows.Forms.TextBox> to display.</span></span>

9. <span data-ttu-id="1c361-123">Ersetzen Sie den Standardnamen des Datasets falls gewünscht.</span><span class="sxs-lookup"><span data-stu-id="1c361-123">Replace the default dataset name if you want.</span></span>

10. <span data-ttu-id="1c361-124">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="1c361-124">Click **Finish**.</span></span>

11. <span data-ttu-id="1c361-125">Klicken Sie im **Eigenschaften** Fenster erneut auf den Pfeil neben der- <xref:System.Windows.Forms.TextBox.Text%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1c361-125">In the **Properties** window, click the arrow next to the <xref:System.Windows.Forms.TextBox.Text%2A> property again.</span></span> <span data-ttu-id="1c361-126">Wählen Sie im **DataSource** -Typ-Editor für die Benutzeroberfläche den Namen des Felds aus, an das die gebunden werden soll <xref:System.Windows.Forms.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="1c361-126">In the **DataSource** UI type editor, select the name of the field to bind the <xref:System.Windows.Forms.TextBox> to.</span></span>

     <span data-ttu-id="1c361-127">Der Editor für die Benutzeroberflächen Typen " **DataSource** " wird geschlossen, und das DataSet <xref:System.Windows.Forms.BindingSource> und der für diese Datenverbindung spezifische Tabellen Adapter werden dem Formular hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1c361-127">The **DataSource** UI type editor closes and the data set, <xref:System.Windows.Forms.BindingSource> and table adapter specific to that data connection are added to your form.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c361-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c361-128">See also</span></span>

- <xref:System.Windows.Forms.BindingSource>
- <xref:System.Windows.Forms.BindingNavigator>
- [<span data-ttu-id="1c361-129">Hinzufügen neuer Datenquellen</span><span class="sxs-lookup"><span data-stu-id="1c361-129">Add new data sources</span></span>](/visualstudio/data-tools/add-new-data-sources)
- <span data-ttu-id="1c361-130">[Datenquellenfenster](/previous-versions/visualstudio/visual-studio-2013/6ckyxa83(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="1c361-130">[Data Sources Window](/previous-versions/visualstudio/visual-studio-2013/6ckyxa83(v=vs.120))</span></span>
