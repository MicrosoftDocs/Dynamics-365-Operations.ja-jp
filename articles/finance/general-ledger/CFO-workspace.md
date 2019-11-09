---
title: CFO ワークスペースへの財務分析コードの追加
description: このトピックでは、CFO ワークスペースに財務分析コードを追加し、それにより元帳および予算のレポートを使用できるようにする方法を説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3817c6688339735c7478e85786efe15bd2372c91
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178626"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="f7abc-103">CFO ワークスペースへの財務分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="f7abc-103">Add financial dimensions to the CFO workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7abc-104">このトピックでは、最高財務責任者 (CFO) ワークスペースに財務分析コードを追加し、それにより元帳および予算のレポートを使用できるようにする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="f7abc-105">CFO ワークスペースには、**概要**タブと**財務**タブがあります。これら 2 つのタブ上のレポートは、LedgerActivityMeasure および BudgetActivityMeasure という 2 つの措置によってサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f7abc-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="f7abc-106">これら 2 つの措置と DimensionCombinationEntity エンティティの間に関係があります。</span><span class="sxs-lookup"><span data-stu-id="f7abc-106">There is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="f7abc-107">したがって、分析コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f7abc-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="f7abc-108">Finance の**エンティティ格納**ページで、**LedgerActivityMeasure** および **BudgetActivityMeasure** 措置を更新します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-108">In Finance, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="f7abc-109">Microsoft Visual Studio で、アプリケーション エクスプローラーを開き、**LedgerCFO** を検索します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="f7abc-110">**リソース**で、**LedgerCFOWorkspacePBIX**を開きます。</span><span class="sxs-lookup"><span data-stu-id="f7abc-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="f7abc-111">Microsoft Power BI desktop でリソースを開く場合、**データの取得**を選択し、**SQL Server データベース**を選択し、**接続**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="f7abc-112">サーバー名を入力し、**AxDW** をデータベースとして入力します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="f7abc-113">**DirectQuery**を選択し **OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="f7abc-114">**LedgerActivityMeasure\_DimensionCombination**を検索して選択し、**読み込み**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="f7abc-115">**フィールド** 一覧で、**財務分析コード**の表の名前を変更し、簡単に識別できるようにします。</span><span class="sxs-lookup"><span data-stu-id="f7abc-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="f7abc-116">**関係の管理**を選択し、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="f7abc-117">最初のフィールドで、**総勘定元帳活動**を選択し、次に **LedgerDimension**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="f7abc-118">2 番目のフィールドで、**LedgerActivityMeasure\_DimensionCombination** (または表の名前を変更した場合、**財務分析コード**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="f7abc-119">**DimensionCombinationRECID** ヘッダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="f7abc-120">**基数** フィールドで、**多対一**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="f7abc-121">**クロス フィルター方向** 値を **単一**に変更します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="f7abc-122">**この関係を有効にする** および **参照整合性を仮定する**の両方を選択し、**OK**を選択し、次に **閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="f7abc-123">[![リレーションシップを作成](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="f7abc-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="f7abc-124">**フィールド** 一覧で、表および使用可能な財務分析コードが表示されるべきです。</span><span class="sxs-lookup"><span data-stu-id="f7abc-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="f7abc-125">レポート レベルのフィルターに、使用する財務分析コードをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="f7abc-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="f7abc-126">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-126">Save your changes.</span></span>
15. <span data-ttu-id="f7abc-127">アプリケーション オブジェクト ツリー (AOT) で、プロジェクトを右クリックし、**同期**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7abc-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="f7abc-128">プロジェクトを構築して、結果を表示するアプリケーションを開きます。</span><span class="sxs-lookup"><span data-stu-id="f7abc-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="f7abc-129">[![完了済ワークスペース](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="f7abc-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>