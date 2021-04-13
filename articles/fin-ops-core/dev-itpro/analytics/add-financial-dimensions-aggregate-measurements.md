---
title: 集計の測定への財務分析コードの追加
description: このトピックでは、パワー ユーザーが既製の Power BI レポートに財務分析コードを組み込む方法について説明します。
author: MilindaV2
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.assetid: c04e0a7b-1747-4b88-b729-fd820f8ab600
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8 for Finance and Operations
ms.openlocfilehash: 8b34896224c47064c997ebe34ecc19be452512a0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754586"
---
# <a name="add-financial-dimensions-to-aggregate-measurements"></a><span data-ttu-id="95b1d-103">集計の測定への財務分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="95b1d-103">Add financial dimensions to aggregate measurements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95b1d-104">この機能により、パワーユーザーは 既成の Microsoft Power BI レポートに財務分析コードを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-104">This feature lets power users include financial dimensions in ready-made Microsoft Power BI reports.</span></span> <span data-ttu-id="95b1d-105">パワー ユーザーは、財務分析コードを使用する新しい Power BI レポートを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-105">Power users can also create new Power BI reports that use financial dimensions.</span></span>

<span data-ttu-id="95b1d-106">財務分析コードは、追加情報を保持する勘定科目表を有効にする、ユーザー定義されたコンフィギュレーション データです。</span><span class="sxs-lookup"><span data-stu-id="95b1d-106">Financial dimensions are user-defined configuration data that enables the ledger chart of accounts to retain additional information.</span></span> <span data-ttu-id="95b1d-107">財務分析コードを追加することにより、ユーザーは勘定科目表および財務諸表に含まれる追加のデータ フィールドを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-107">By adding financial dimensions, a user can configure additional data fields that will be included with the chart of accounts and financial reports.</span></span> <span data-ttu-id="95b1d-108">したがって、元帳勘定科目表をそれらのフィールドに基づいて詳しく分析できます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-108">Therefore, the ledger chart of accounts can be sliced and diced based on those fields.</span></span> <span data-ttu-id="95b1d-109">この機能は、強力な財務報告を提供します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-109">This feature provides powerful financial reporting.</span></span> <span data-ttu-id="95b1d-110">たとえば、追加した新しい財務分析コードを使用して元帳データを参照できます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-110">For example, you can explore ledger data by using the new financial dimensions that you've added.</span></span> <span data-ttu-id="95b1d-111">リリースされるときに既製の Power BI レポートに財務分析コードが含まれていないため、これらの追加フィールドを既製のレポートに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-111">Because no financial dimensions are included in the ready-made Power BI reports when they are released, you must include these additional fields to the ready-made reports.</span></span> 

<span data-ttu-id="95b1d-112">財務分析コード フィールドがレポートに含まれた後、他のユーザーとレポートを共有できます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-112">After financial dimension fields are included in the report, you can share the report with other users.</span></span> <span data-ttu-id="95b1d-113">これらの他のユーザーは、財務分析コード フィールドのすべてまたは一部を含むことによって、チャートなどの既存のビジュアルを変更できます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-113">Those other users can modify existing visuals, such as charts, by including all or some of the financial dimension fields.</span></span>

> [!NOTE]
> <span data-ttu-id="95b1d-114">この機能は Microsoft Dynamics 365 for Finance and Operations、Enterprise edition (2017 年 7 月) で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="95b1d-114">This feature is available in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span> <span data-ttu-id="95b1d-115">プラットフォーム アップデート 8 以降も必要です。</span><span class="sxs-lookup"><span data-stu-id="95b1d-115">Platform update 8 or later is also required.</span></span> 

## <a name="how-does-this-feature-work"></a><span data-ttu-id="95b1d-116">この機能はどのように作用しますか。</span><span class="sxs-lookup"><span data-stu-id="95b1d-116">How does this feature work?</span></span>

<span data-ttu-id="95b1d-117">エンティティ格納は、パワー ユーザーがレポートを作成できる運用データ ウェアハウスです。</span><span class="sxs-lookup"><span data-stu-id="95b1d-117">The Entity store is an operational data warehouse that lets power users create reports.</span></span> <span data-ttu-id="95b1d-118">エンティティ格納が更新されるときはいつでも、すべての使用可能な財務分析コードがそれに含まれます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-118">Whenever the Entity store is updated, all available financial dimensions are included in it.</span></span> <span data-ttu-id="95b1d-119">総勘定仕訳元帳レベルの詳細を含む **元帳活動** の集計の測定の例を検討します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-119">We will look at an example from the **Ledger Activity** aggregate measurement that contains General ledger journal-level details.</span></span>

<span data-ttu-id="95b1d-120">次のリストは、更新されたときに エンティティ格納に格納されるテーブルの一部を示しています。</span><span class="sxs-lookup"><span data-stu-id="95b1d-120">The following list shows some of the tables are filled in the Entity store when it's updated.</span></span> <span data-ttu-id="95b1d-121">変更が加えられたテーブルは太字です。</span><span class="sxs-lookup"><span data-stu-id="95b1d-121">Tables that have changed are bold.</span></span>

- <span data-ttu-id="95b1d-122">LedgerActivityMeasure\_LedgerActivityMeasureGroup</span><span class="sxs-lookup"><span data-stu-id="95b1d-122">LedgerActivityMeasure\_LedgerActivityMeasureGroup</span></span>
- <span data-ttu-id="95b1d-123">LedgerActivityMeasure\_TransactionDate</span><span class="sxs-lookup"><span data-stu-id="95b1d-123">LedgerActivityMeasure\_TransactionDate</span></span>
- <span data-ttu-id="95b1d-124">LedgerActivityMeasure\_Currency</span><span class="sxs-lookup"><span data-stu-id="95b1d-124">LedgerActivityMeasure\_Currency</span></span>
- <span data-ttu-id="95b1d-125">LedgerActivityMeasure\_FiscalPeriodDateAggregtateDimension</span><span class="sxs-lookup"><span data-stu-id="95b1d-125">LedgerActivityMeasure\_FiscalPeriodDateAggregtateDimension</span></span>
- <span data-ttu-id="95b1d-126">LedgerActivityMeasure\_LedgerFactDimension</span><span class="sxs-lookup"><span data-stu-id="95b1d-126">LedgerActivityMeasure\_LedgerFactDimension</span></span>
- <span data-ttu-id="95b1d-127">LedgerActivityMeasure\_FiscalYearOffsetDimension</span><span class="sxs-lookup"><span data-stu-id="95b1d-127">LedgerActivityMeasure\_FiscalYearOffsetDimension</span></span>
- <span data-ttu-id="95b1d-128">LedgerActivityMeasure\_MainAccount</span><span class="sxs-lookup"><span data-stu-id="95b1d-128">LedgerActivityMeasure\_MainAccount</span></span>
- <span data-ttu-id="95b1d-129">**LedgerActivityMeasure\_DimensionCombination**</span><span class="sxs-lookup"><span data-stu-id="95b1d-129">**LedgerActivityMeasure\_DimensionCombination**</span></span>
- <span data-ttu-id="95b1d-130">LedgerActivityMeasure\_Ledger</span><span class="sxs-lookup"><span data-stu-id="95b1d-130">LedgerActivityMeasure\_Ledger</span></span>
- <span data-ttu-id="95b1d-131">LedgerActivityMeasure\_MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="95b1d-131">LedgerActivityMeasure\_MainAccountCategory</span></span>
- <span data-ttu-id="95b1d-132">LedgerActivityMeasure\_Company</span><span class="sxs-lookup"><span data-stu-id="95b1d-132">LedgerActivityMeasure\_Company</span></span>
- <span data-ttu-id="95b1d-133">LedgerActivityMeasure\_MainAccountLegalEntity</span><span class="sxs-lookup"><span data-stu-id="95b1d-133">LedgerActivityMeasure\_MainAccountLegalEntity</span></span>
- <span data-ttu-id="95b1d-134">**LedgerActivityMeasure\_Agreement**</span><span class="sxs-lookup"><span data-stu-id="95b1d-134">**LedgerActivityMeasure\_Agreement**</span></span>
- <span data-ttu-id="95b1d-135">**LedgerActivityMeasure\_BankAccount**</span><span class="sxs-lookup"><span data-stu-id="95b1d-135">**LedgerActivityMeasure\_BankAccount**</span></span>
- <span data-ttu-id="95b1d-136">**LedgerActivityMeasure\_BusinessUnit**</span><span class="sxs-lookup"><span data-stu-id="95b1d-136">**LedgerActivityMeasure\_BusinessUnit**</span></span>
- <span data-ttu-id="95b1d-137">**LedgerActivityMeasure\_Campaign**</span><span class="sxs-lookup"><span data-stu-id="95b1d-137">**LedgerActivityMeasure\_Campaign**</span></span>
- <span data-ttu-id="95b1d-138">**LedgerActivityMeasure\_Cargo**</span><span class="sxs-lookup"><span data-stu-id="95b1d-138">**LedgerActivityMeasure\_Cargo**</span></span>
- <span data-ttu-id="95b1d-139">**LedgerActivityMeasure\_Cargo\_CN**</span><span class="sxs-lookup"><span data-stu-id="95b1d-139">**LedgerActivityMeasure\_Cargo\_CN**</span></span>

<span data-ttu-id="95b1d-140">システムで定義されている各財務分析コードについて、エンティティ格納で対応するテーブルを確認できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-140">Notice that, for each financial dimension that is defined in your system, you might see a corresponding table in the Entity store.</span></span>

<span data-ttu-id="95b1d-141">LedgerActivityMeasure\_DimensionCombination テーブルを調べると、フィールドの一覧が拡張され、追加フィールドが含まれていることが分かります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-141">If you examine the LedgerActivityMeasure\_DimensionCombination table, you will notice that the list of fields has been expanded and now includes additional fields.</span></span> <span data-ttu-id="95b1d-142">それぞれの新しいフィールドは、財務分析コードに対応します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-142">Each new field corresponds to a financial dimension.</span></span> <span data-ttu-id="95b1d-143">例については、以下は追加のフィールドの一部です。</span><span class="sxs-lookup"><span data-stu-id="95b1d-143">For an example, here are some of the additional fields:</span></span>

- <span data-ttu-id="95b1d-144">契約 \_FK</span><span class="sxs-lookup"><span data-stu-id="95b1d-144">Agreement\_FK</span></span>
- <span data-ttu-id="95b1d-145">契約 \_ 内容</span><span class="sxs-lookup"><span data-stu-id="95b1d-145">Agreement\_Description</span></span>
- <span data-ttu-id="95b1d-146">契約 \_ 値</span><span class="sxs-lookup"><span data-stu-id="95b1d-146">Agreement\_Value</span></span>
- <span data-ttu-id="95b1d-147">BankAccount\_FK</span><span class="sxs-lookup"><span data-stu-id="95b1d-147">BankAccount\_FK</span></span>
- <span data-ttu-id="95b1d-148">BankAccount\_説明</span><span class="sxs-lookup"><span data-stu-id="95b1d-148">BankAccount\_Description</span></span>
- <span data-ttu-id="95b1d-149">BankAccount\_値</span><span class="sxs-lookup"><span data-stu-id="95b1d-149">BankAccount\_Value</span></span>
- <span data-ttu-id="95b1d-150">BusinessUnit\_FK</span><span class="sxs-lookup"><span data-stu-id="95b1d-150">BusinessUnit\_FK</span></span>
- <span data-ttu-id="95b1d-151">BusinessUnit\_説明</span><span class="sxs-lookup"><span data-stu-id="95b1d-151">BusinessUnit\_Description</span></span>
- <span data-ttu-id="95b1d-152">BusinessUnit\_値</span><span class="sxs-lookup"><span data-stu-id="95b1d-152">BusinessUnit\_Value</span></span>

<span data-ttu-id="95b1d-153">**仕入先** という名前の新しい財務分析コードをユーザーが定義した場合、エンティティ格納が更新されると、LedgerActivityMeasure \_仕入先という新しいテーブルが追加されます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-153">If a user defines a new financial dimension that is named **vendor**, when the Entity store is updated, a new table is added that is named LedgerActivityMeasure\_Vendor.</span></span>

<span data-ttu-id="95b1d-154">LedgerActivityMeasure\_DimensionCombination テーブルには、次の新しいフィールド セットも含められます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-154">The LedgerActivityMeasure\_DimensionCombination table will also contain the following new set of fields:</span></span>

- <span data-ttu-id="95b1d-155">仕入先\_FK</span><span class="sxs-lookup"><span data-stu-id="95b1d-155">Vendor\_FK</span></span>
- <span data-ttu-id="95b1d-156">仕入先\_説明</span><span class="sxs-lookup"><span data-stu-id="95b1d-156">Vendor\_Description</span></span>
- <span data-ttu-id="95b1d-157">仕入先\_値</span><span class="sxs-lookup"><span data-stu-id="95b1d-157">Vendor\_Value</span></span>

## <a name="how-a-power-bi-report-author-can-create-reports-that-use-financial-dimensions"></a><span data-ttu-id="95b1d-158">Power BI レポート作成者が財務分析コードを使用するレポートを作成する方法</span><span class="sxs-lookup"><span data-stu-id="95b1d-158">How a Power BI report author can create reports that use financial dimensions</span></span>

<span data-ttu-id="95b1d-159">ビジネス ユーザーは、Power BI デスクトップを使用して財務分析コードを使用する新しいレポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-159">A business user can create a new report that uses financial dimensions by using Power BI desktop.</span></span> <span data-ttu-id="95b1d-160">財務分析コードを使用する既存のレポートを更新して、追加のフィールドを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-160">Existing reports that use financial dimensions can be updated so that they include additional fields.</span></span>

<span data-ttu-id="95b1d-161">この例では、元帳活動メジャー グループを使用するレポートを作成するために Power BI デスクトップを使用します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-161">In this example, we will use Power BI desktop to create a report that uses the Ledger Activity measure group.</span></span> 

1. <span data-ttu-id="95b1d-162">開発環境で、Power BI desktop を使用してエンティティ ストア データベースに接続します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-162">In a development environment, connect to the Entity store database by using Power BI desktop.</span></span> 
2. <span data-ttu-id="95b1d-163">次のテーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-163">Select the following tables:</span></span>

    - <span data-ttu-id="95b1d-164">LedgerActivityMeasure\_LedgerActivityMeasureGroup</span><span class="sxs-lookup"><span data-stu-id="95b1d-164">LedgerActivityMeasure\_LedgerActivityMeasureGroup</span></span>
    - <span data-ttu-id="95b1d-165">LedgerActivityMeasure\_FiscalPeriodDateAggregtateDimension</span><span class="sxs-lookup"><span data-stu-id="95b1d-165">LedgerActivityMeasure\_FiscalPeriodDateAggregtateDimension</span></span>
    - <span data-ttu-id="95b1d-166">LedgerActivityMeasure\_DimensionCombination</span><span class="sxs-lookup"><span data-stu-id="95b1d-166">LedgerActivityMeasure\_DimensionCombination</span></span>

3. <span data-ttu-id="95b1d-167">Power BI デスクトップの **リレーションシップの管理** オプションを使用して、テーブル フィールド間に以下のリレーションシップを定義します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-167">Use the **Manage relationships** option in Power BI desktop to define the following relationships between table fields:</span></span>

    - <span data-ttu-id="95b1d-168">**LedgerActivityMeasure\_LedgerActivityMeasureGroup.LEDGERDIMENSION** および **LedgerActivityMeasure\_DimensionCombination.DIMENTIONCOMBINATIONRECID** 間の結合を定義します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-168">Define a join between **LedgerActivityMeasure\_LedgerActivityMeasureGroup.LEDGERDIMENSION** and **LedgerActivityMeasure\_DimensionCombination.DIMENTIONCOMBINATIONRECID**.</span></span>
    - <span data-ttu-id="95b1d-169">**LedgerActivityMeasure\_LedgerActivityMeasureGroup.LEDGERGREGORIANDATEID** および **LedgerActivityMeasure\_FiscalPeriodDateAggregateDimension.LEDGERPERIODGREGORIANDATEID** 間の結合を定義します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-169">Define a join between **LedgerActivityMeasure\_LedgerActivityMeasureGroup.LEDGERGREGORIANDATEID** and **LedgerActivityMeasure\_FiscalPeriodDateAggregateDimension.LEDGERPERIODGREGORIANDATEID**.</span></span>

4. <span data-ttu-id="95b1d-170">**販売** および **YearName** フィールドを使用するマトリックス レポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-170">Create a matrix report that uses the **Sales** and **YearName** fields.</span></span> <span data-ttu-id="95b1d-171">レポートは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-171">The report should resemble the following example.</span></span>

    ![販売および YearName フィールドを使用するマトリックス レポートの例](media/d1d0e190896bec3a755b9b586a3cb657.png)

    <span data-ttu-id="95b1d-173">次に、財務分析コード値を追加します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-173">Next, we will add financial dimension values.</span></span>

5. <span data-ttu-id="95b1d-174">Power BI デスクトップのフィールドの一覧で、**LedgerActivityMeasure\_DimensionCombination** テーブルを展開します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-174">In the list of fields in Power BI desktop, expand the **LedgerActivityMeasure\_DimensionCombination** table.</span></span> <span data-ttu-id="95b1d-175">次のように、分析コード フィールドの一覧がテーブル フィールドに拡張されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-175">You will see that the list of dimension fields is expanded into table fields, as shown here.</span></span>

    ![テーブル フィールドに拡張された分析コード フィールドのリスト](media/b5099b0c03fa16f0c2ab70943c7cce8b.png)

6. <span data-ttu-id="95b1d-177">レポートに **BusinessUnit\_Description** フィールドを含めます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-177">Include the **BusinessUnit\_Description** field in the report.</span></span> <span data-ttu-id="95b1d-178">これで、レポートに、次の例のように、業務単位ごとの販売が表示されます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-178">Your report should now show sales by business unit, as shown in the following example.</span></span>

    ![事業単位ごとの販売を示すレポート](media/c39e94631896301db6675d36fc9d3886.png)

    <span data-ttu-id="95b1d-180">**BusinessUnit\_description** フィールドおよび **BusinessUnit\_Value** フィールドがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-180">Notice that you have the **BusinessUnit\_description** field and the **BusinessUnit\_Value** field.</span></span> <span data-ttu-id="95b1d-181">値フィールドを使用すると、列のソートに使用できる数値を取得できます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-181">The value field lets you to get a numerical value that can be used to sort columns.</span></span>

7. <span data-ttu-id="95b1d-182">新しい財務分析コードを定義し、エンティティ ストアを更新します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-182">Define a new financial dimension, and update the Entity store.</span></span> 
8. <span data-ttu-id="95b1d-183">更新が完了したら、**LedgerActivityMeasure\_DimensionCombination** テーブルを右クリックして、**データの更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-183">When the update is completed, right-click the **LedgerActivityMeasure\_DimensionCombination** table, and then select **Refresh data**.</span></span> <span data-ttu-id="95b1d-184">定義した新しい財務分析コードが、レポートに使用できるフィールドの一覧に反映されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-184">Notice that the new financial dimension that you defined is reflected in the list of fields that are available for reporting.</span></span>

    ![データの更新](media/6d345e2f68dfb0413daebfd5f469db2c.png)

9. <span data-ttu-id="95b1d-186">新しい財務分析コード フィールドをレポートに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-186">You can include the new financial dimension fields in the report.</span></span>

### <a name="creating-reports-that-use-expanded-financial-dimension-tables"></a><span data-ttu-id="95b1d-187">展開済の財務分析コード テーブルを使用するレポートを作成しています</span><span class="sxs-lookup"><span data-stu-id="95b1d-187">Creating reports that use expanded Financial dimension tables</span></span>

<span data-ttu-id="95b1d-188">先に説明したように、新しいテーブルはエンティティ格納で作成されました。</span><span class="sxs-lookup"><span data-stu-id="95b1d-188">As we discussed earlier, new tables were created in the Entity store.</span></span> <span data-ttu-id="95b1d-189">各財務分析コード フィールドは、新しいテーブルにも追加されます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-189">Each financial dimension field is also added to a new table.</span></span> <span data-ttu-id="95b1d-190">新しいテーブルには、名前、値、および説明の個々のフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="95b1d-190">The new tables contain individual fields for the name, value, and description.</span></span>

<span data-ttu-id="95b1d-191">新しいテーブルに、レポートの作成に使用される LedgerActivityMeasure\_DimensionCombination テーブルと結合するために使用できるキーが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-191">Notice that the new tables contain a key that can be used to join them with the LedgerActivityMeasure\_DimensionCombination table that is used to create the report.</span></span> <span data-ttu-id="95b1d-192">これらの追加テーブルのフィールドを使用する場合は、レポートにフィールドを含め、キーを使用して関連付けるだけです。</span><span class="sxs-lookup"><span data-stu-id="95b1d-192">If you want to use fields from these additional tables, just include them in the report and relate them by using the keys.</span></span>

1. <span data-ttu-id="95b1d-193">作成済みのレポートを開きます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-193">Open the report that you created earlier.</span></span>

    <span data-ttu-id="95b1d-194">ここで、レポートに財務分析コード テーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-194">We will now add a financial dimension table to the report.</span></span>

2. <span data-ttu-id="95b1d-195">Power BI desktop で、メニューの **最近のソース** をクリックしてから、**AXDW** データ接続を選択します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-195">In Power BI desktop, click **Recent Sources** on the menu, and then select the **AXDW** data connection.</span></span> <span data-ttu-id="95b1d-196">テーブル ナビゲーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-196">Table navigator is shown.</span></span>
3. <span data-ttu-id="95b1d-197">レポートの **LedgerActivityMeasure\_LegalEntity** テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-197">Select the **LedgerActivityMeasure\_LegalEntity** table for the report.</span></span>

    > [!NOTE]
    > <span data-ttu-id="95b1d-198">開発またはデモ環境を使用している場合、**LegalEntity** はデモ データで定義されている財務分析コードであるため、このテーブルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-198">If you're using a development or demo environment, you see this table because **LegalEntity** is a financial dimension that is defined in demo data.</span></span> <span data-ttu-id="95b1d-199">独自のデータで作業している場合、表示されるテーブルは定義した財務分析コードに対応します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-199">If you're working with your own data, the tables that you see will correspond to financial dimensions that you've defined.</span></span>

    <span data-ttu-id="95b1d-200">ここで、レポートにある既存のテーブルに選択したテーブルを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-200">We will now relate the selected table to existing tables in the report.</span></span> 

4. <span data-ttu-id="95b1d-201">レポートで、**リレーションシップの管理** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-201">In the report, open the **Manage relationships** dialog box.</span></span>
5. <span data-ttu-id="95b1d-202">**LedgerActivityMeasure\_DimensionCombination.LegalEntity\_FK** を **LedgerActivityMeasure\_LegalEntity.KEY\_** に結合します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-202">Join **LedgerActivityMeasure\_DimensionCombination.LegalEntity\_FK** to **LedgerActivityMeasure\_LegalEntity.KEY\_**.</span></span>

<span data-ttu-id="95b1d-203">手順 3 で別の分析コード テーブルを選択する場合は、対応する **FieldName\_FK** フィールドを組み合わせテーブルから分析コード テーブルの **KEY\_** フィールドに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-203">If you select a different dimension table in step 3, you must relate the corresponding **FieldName\_FK** field from the combination table to the **KEY\_** field in the dimension table.</span></span>

## <a name="how-a-developer-can-enable-financial-dimensions"></a><span data-ttu-id="95b1d-204">開発者が財務分析コードを有効にする方法</span><span class="sxs-lookup"><span data-stu-id="95b1d-204">How a developer can enable financial dimensions</span></span>

<span data-ttu-id="95b1d-205">エンティティ格納内の展開されている財務分析コードを表示する前に、開発者は集計測定の財務分析コードの使用を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-205">Before users can see expanded financial dimensions in the Entity store, a developer must enable the use of financial dimensions in aggregate measurements.</span></span> <span data-ttu-id="95b1d-206">ベスト プラクティスとしては、財務データが含まれている集計測定をモデル化するときに財務分析コードが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-206">As a best practice, financial dimensions should be included when you model any aggregate measurement that involves financial data.</span></span> <span data-ttu-id="95b1d-207">財務分析コードを含めるには、「財務分析コード テーブル」に基づく集計分析コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-207">To include financial dimensions, create an aggregate dimension that is based on “financial dimension tables.”</span></span> <span data-ttu-id="95b1d-208">先に見たように、財務分析コード テーブルを使用して作成する集計分析コードはランタイムに展開されます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-208">As we saw earlier, an aggregate dimension that you create by using financial dimension tables will be expanded at runtime.</span></span>

### <a name="what-are-financial-dimension-tables"></a><span data-ttu-id="95b1d-209">財務分析コード テーブルとは</span><span class="sxs-lookup"><span data-stu-id="95b1d-209">What are financial dimension tables?</span></span>

<span data-ttu-id="95b1d-210">財務分析コード テーブルは、財務分析コード データを含むベース テーブルです。</span><span class="sxs-lookup"><span data-stu-id="95b1d-210">Financial dimension tables are base tables that contain financial dimension data.</span></span> <span data-ttu-id="95b1d-211">例では、**DimensionAttributeValueCombination** および **DimensionAttributeValueSet** があります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-211">Examples include **DimensionAttributeValueCombination** and **DimensionAttributeValueSet**.</span></span>

<span data-ttu-id="95b1d-212">これらの 2 つのテーブルに基づくテーブル、ビュー、またはエンティティを使用する場合、集計分析コードのフィールドは実行時に展開されます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-212">If you use a table, a view, or an entity that is based on those two tables, the fields of the aggregate dimension will be expanded at runtime.</span></span>

<span data-ttu-id="95b1d-213">LedgerActivityMeasure 集計の測定の次の例を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="95b1d-213">Consider the following example from the LedgerActivityMeasure aggregate measurement.</span></span>

![LedgerActivityMeasure 集計の DimensionCombination 集計ディメンション](media/08437296a512478e99b3c377170edeee.png)

<span data-ttu-id="95b1d-215">DimensionCombination は、DimensionAttributeValueCombination ベース テーブルを使用してモデル化される集計分析コードです。</span><span class="sxs-lookup"><span data-stu-id="95b1d-215">DimensionCombination is an aggregate dimension that is modeled by using the DimensionAttributeValueCombination base table.</span></span> <span data-ttu-id="95b1d-216">この場合、開発者は LedgerActivityMeasureGroup メジャー グループを使用して集計分析コードを参照しました。</span><span class="sxs-lookup"><span data-stu-id="95b1d-216">In this case, the developer has referenced the aggregate dimension by using the LedgerActivityMeasureGroup measure group.</span></span>

<span data-ttu-id="95b1d-217">実行時に、システムで新しい財務分析コードが定義されると新しい分析コード フィールドが追加されます。(つまり、DimensionCombination テーブルが展開されます。)</span><span class="sxs-lookup"><span data-stu-id="95b1d-217">At runtime, new dimension fields are added (that is, the DimensionCombination table is expanded) as new financial dimensions are defined in the system.</span></span>

### <a name="creating-role-playing-financial-dimensions"></a><span data-ttu-id="95b1d-218">ロールプレイング財務分析コードを作成しています</span><span class="sxs-lookup"><span data-stu-id="95b1d-218">Creating role-playing financial dimensions</span></span>

<span data-ttu-id="95b1d-219">元帳データを使用して報告するとき、基本アカウントと相手勘定に関する報告が必要なことがあります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-219">When you report by using ledger data, you might require reporting on primary accounts and offset accounts.</span></span> <span data-ttu-id="95b1d-220">例については、元帳トランザクションが 1 つの勘定から別の勘定への金額の転送を含む場合、基本勘定は「元」勘定、相手勘定は、「先」勘定になります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-220">For an example, if a ledger transaction involves the transfer of an amount from one account to another account, the primary account is the "from" account, whereas the offset account is the "to" account.</span></span> <span data-ttu-id="95b1d-221">このパターンは、*ロールプレイング ディメンション* パターンとして知られています。</span><span class="sxs-lookup"><span data-stu-id="95b1d-221">This pattern is known as the *role-playing dimensions* pattern.</span></span>

<span data-ttu-id="95b1d-222">基本勘定と相手勘定の両方がトランザクション データに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-222">Both primary accounts and offset accounts must be associated with transaction data.</span></span> <span data-ttu-id="95b1d-223">したがって、基本勘定と相手勘定の両方の財務分析コード フィールドを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95b1d-223">Therefore, you must expand financial dimension fields of both primary accounts and offset accounts.</span></span> <span data-ttu-id="95b1d-224">ここで、この要件をどのように満たすことができるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-224">We will now see how you can meet this requirement.</span></span> <span data-ttu-id="95b1d-225">以下の例について考えます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-225">Consider the following example.</span></span>

![ロール プレイの分析コード例](media/062a0d860fe1633a6616bca6e871f95e.png)

<span data-ttu-id="95b1d-227">LedgerActivityMeaureGroup の 2 つの分析コード参照をモデル化しました。</span><span class="sxs-lookup"><span data-stu-id="95b1d-227">We have modeled two dimension references for LedgerActivityMeaureGroup.</span></span> <span data-ttu-id="95b1d-228">最初の参照、DimensionCombinationは、**LedgerDimension** フィールドを使用して結合されます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-228">The first reference, DimensionCombination, is joined by using the **LedgerDimension** field.</span></span> <span data-ttu-id="95b1d-229">このトピックの前のところでこのパターンを確認しました。</span><span class="sxs-lookup"><span data-stu-id="95b1d-229">We saw this pattern earlier in this topic.</span></span>

<span data-ttu-id="95b1d-230">2 番目の参照、OffsetDimensionCombination は、同じ分析コードへの別の参照です。</span><span class="sxs-lookup"><span data-stu-id="95b1d-230">The second reference, OffsetDimensionCombination, is another reference to the same dimension.</span></span> <span data-ttu-id="95b1d-231">DimensionCombination 集計分析コードを再使用し、それに新しい名前を付けました。</span><span class="sxs-lookup"><span data-stu-id="95b1d-231">We have reused the DimensionCombination aggregate dimension and given it a new name.</span></span> <span data-ttu-id="95b1d-232">2 番目のケースでは、**OffsetLedgerDimension** フィールドを使用して参加できます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-232">In the second case, we can join by using the **OffsetLedgerDimension** field.</span></span>

<span data-ttu-id="95b1d-233">実行時に、システムは両方の分析コードを追加のフィールドに展開します。</span><span class="sxs-lookup"><span data-stu-id="95b1d-233">At runtime, the system will expand both these dimensions with additional fields.</span></span> <span data-ttu-id="95b1d-234">したがって、主およびオフセットの分析コード フィールドについてレポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="95b1d-234">Therefore, you can report on primary and offset dimension fields.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]