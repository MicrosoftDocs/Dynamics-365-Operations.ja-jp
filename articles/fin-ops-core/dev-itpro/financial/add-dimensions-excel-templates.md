---
title: Excel テンプレートに財務分析コードの値の検索を追加
description: このトピックでは、Microsoft Excel テンプレートで分析コード値を検索する機能を追加する方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 261064
ms.assetid: f3ab87ab-ee8b-462c-bb6f-4d98e0030513
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 99c41833fb2cb479bb230a7653e220904cc1a673
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191574"
---
# <a name="add-lookup-values-for-financial-dimensions-to-excel-templates"></a><span data-ttu-id="f9a64-103">Excel テンプレートに財務分析コードの値の検索を追加</span><span class="sxs-lookup"><span data-stu-id="f9a64-103">Add lookup values for financial dimensions to Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9a64-104">このトピックでは、Microsoft Excel テンプレートで分析コード値を検索する機能を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-104">This topic provides information about how you can add the ability to look up dimension values in Microsoft Excel templates.</span></span>

<span data-ttu-id="f9a64-105">インストール後に Microsoft Excel テンプレートに存在する唯一の値は MainAccount です。</span><span class="sxs-lookup"><span data-stu-id="f9a64-105">The only value that is present on Microsoft Excel templates after installation is MainAccount.</span></span> <span data-ttu-id="f9a64-106">これは、すべての顧客が持つ唯一の分析コード です。</span><span class="sxs-lookup"><span data-stu-id="f9a64-106">This is the only dimension that all customers will have.</span></span> <span data-ttu-id="f9a64-107">Microsoft Excel テンプレートに分析コードを追加するには、[Microsoft Excel テンプレートに分析コードを追加](dimensions-overview.md) トピックの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9a64-107">To add the dimensions to Microsoft Excel templates, you need to complete the steps in the [Add dimensions to the Microsoft Excel templates](dimensions-overview.md) topic.</span></span> <span data-ttu-id="f9a64-108">分析コードを追加した後、分析コード値の一覧を検索する機能が必要な場合このトピックの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-108">After you have added the dimensions, if you want the ability to look up a list of dimension values, complete the steps in this topic.</span></span> <span data-ttu-id="f9a64-109">**注記:** この情報は、リリースごとに変更される可能性がありますので、定期的に最新の情報を確認してください。</span><span class="sxs-lookup"><span data-stu-id="f9a64-109">**Note:**  This information is subject to change for each release, so be sure to check back frequently for the most up-to-date information.</span></span>

1.  <span data-ttu-id="f9a64-110">Visual Studio で、**DimensionCombinationEntity** または **DimensionSetEntity** を変更したプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9a64-110">In Visual Studio, open the project where you modified **DimensionCombinationEntity** or **DimensionSetEntity.**</span></span>
2.  <span data-ttu-id="f9a64-111">**DimensionCombinationEntity** または **DimensionSetEntity** を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="f9a64-111">Right-click **DimensionCombinationEntity** or **DimensionSetEntity**.</span></span> <span data-ttu-id="f9a64-112">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-112">Select **Open**.</span></span>
3.  <span data-ttu-id="f9a64-113">**関係** を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="f9a64-113">Right click **Relations**.</span></span> <span data-ttu-id="f9a64-114">**新規** を選択して **関係** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9a64-114">Select **New** and then click **Relation.**</span></span>
4.  <span data-ttu-id="f9a64-115">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-115">In the **Properties** pane, set the following properties.</span></span>
    -   <span data-ttu-id="f9a64-116">**検証** - 番号</span><span class="sxs-lookup"><span data-stu-id="f9a64-116">**Validate** - No</span></span>
    -   <span data-ttu-id="f9a64-117">**基数** - ZeroMore</span><span class="sxs-lookup"><span data-stu-id="f9a64-117">**Cardinality** - ZeroMore</span></span>
    -   <span data-ttu-id="f9a64-118">**名前** - 部門などの、財務分析コードの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-118">**Name** - Enter the name of the financial dimension, such as Department.</span></span>
    -   <span data-ttu-id="f9a64-119">**関連データ エンティティ** - **名前**フィールドで入力した財務分析コードのエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-119">**Related Data Entity** - Select the entity for the financial dimension that you entered in the **Name** field.</span></span> <span data-ttu-id="f9a64-120">次のテーブルに、財務分析コードと関連するエンティティの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-120">The following table contains a list of the financial dimensions and the related entities.</span></span>

        | <span data-ttu-id="f9a64-121">**財務分析コード '値の使用元'**</span><span class="sxs-lookup"><span data-stu-id="f9a64-121">**Financial dimension 'Use values from'**</span></span> | <span data-ttu-id="f9a64-122">**関連するエンティティ**</span><span class="sxs-lookup"><span data-stu-id="f9a64-122">**Related entity**</span></span>                        |
        |-------------------------------------------|-------------------------------------------|
        | <span data-ttu-id="f9a64-123">&lt; カスタム分析コード &gt;</span><span class="sxs-lookup"><span data-stu-id="f9a64-123">&lt; Custom dimension &gt;</span></span>                | <span data-ttu-id="f9a64-124">DimAttributeFinancialTagEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-124">DimAttributeFinancialTagEntity</span></span>            |
        | <span data-ttu-id="f9a64-125">契約</span><span class="sxs-lookup"><span data-stu-id="f9a64-125">Agreements</span></span>                                | <span data-ttu-id="f9a64-126">DimAttributeAgreementHeaderExt\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-126">DimAttributeAgreementHeaderExt\_RUEntity</span></span>  |
        | <span data-ttu-id="f9a64-127">銀行口座</span><span class="sxs-lookup"><span data-stu-id="f9a64-127">Bank accounts</span></span>                             | <span data-ttu-id="f9a64-128">DimAttributeBankAccountTableEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-128">DimAttributeBankAccountTableEntity</span></span>        |
        | <span data-ttu-id="f9a64-129">BusinessUnits</span><span class="sxs-lookup"><span data-stu-id="f9a64-129">BusinessUnits</span></span>                             | <span data-ttu-id="f9a64-130">DimAttributeOMBusinessUnitEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-130">DimAttributeOMBusinessUnitEntity</span></span>          |
        | <span data-ttu-id="f9a64-131">キャンペーン</span><span class="sxs-lookup"><span data-stu-id="f9a64-131">Campaigns</span></span>                                 | <span data-ttu-id="f9a64-132">DimAttributeSmmCampaignTableEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-132">DimAttributeSmmCampaignTableEntity</span></span>        |
        | <span data-ttu-id="f9a64-133">現金勘定</span><span class="sxs-lookup"><span data-stu-id="f9a64-133">Cash accounts</span></span>                             | <span data-ttu-id="f9a64-134">DimAttributeRCashTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-134">DimAttributeRCashTable\_RUEntity</span></span>          |
        | <span data-ttu-id="f9a64-135">コスト センター</span><span class="sxs-lookup"><span data-stu-id="f9a64-135">Cost centers</span></span>                              | <span data-ttu-id="f9a64-136">DimAttributeOMCostCenterEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-136">DimAttributeOMCostCenterEntity</span></span>            |
        | <span data-ttu-id="f9a64-137">顧客グループ</span><span class="sxs-lookup"><span data-stu-id="f9a64-137">Customer groups</span></span>                           | <span data-ttu-id="f9a64-138">DimAttributeCustGroupEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-138">DimAttributeCustGroupEntity</span></span>               |
        | <span data-ttu-id="f9a64-139">顧客</span><span class="sxs-lookup"><span data-stu-id="f9a64-139">Customers</span></span>                                 | <span data-ttu-id="f9a64-140">DimAttributeCustTableEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-140">DimAttributeCustTableEntity</span></span>               |
        | <span data-ttu-id="f9a64-141">繰延</span><span class="sxs-lookup"><span data-stu-id="f9a64-141">Deferrals</span></span>                                 | <span data-ttu-id="f9a64-142">DimAttributeRDeferralsTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-142">DimAttributeRDeferralsTable\_RUEntity</span></span>     |
        | <span data-ttu-id="f9a64-143">部門</span><span class="sxs-lookup"><span data-stu-id="f9a64-143">Departments</span></span>                               | <span data-ttu-id="f9a64-144">DimAttributeOMDepartmentEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-144">DimAttributeOMDepartmentEntity</span></span>            |
        | <span data-ttu-id="f9a64-145">経費および所得コード</span><span class="sxs-lookup"><span data-stu-id="f9a64-145">Expense and income codes</span></span>                  | <span data-ttu-id="f9a64-146">DimAttributeRTax25ProfitTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-146">DimAttributeRTax25ProfitTable\_RUEntity</span></span>   |
        | <span data-ttu-id="f9a64-147">経費の目的</span><span class="sxs-lookup"><span data-stu-id="f9a64-147">Expense Purposes</span></span>                          | <span data-ttu-id="f9a64-148">DimAttributeTrvTravelTxtEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-148">DimAttributeTrvTravelTxtEntity</span></span>            |
        | <span data-ttu-id="f9a64-149">会計施設</span><span class="sxs-lookup"><span data-stu-id="f9a64-149">Fiscal establishments</span></span>                     | <span data-ttu-id="f9a64-150">DimAttributeFiscalEstablishment\_BREntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-150">DimAttributeFiscalEstablishment\_BREntity</span></span> |
        | <span data-ttu-id="f9a64-151">固定資産グループ</span><span class="sxs-lookup"><span data-stu-id="f9a64-151">Fixed asset groups</span></span>                        | <span data-ttu-id="f9a64-152">DimAttributeAssetGroupEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-152">DimAttributeAssetGroupEntity</span></span>              |
        | <span data-ttu-id="f9a64-153">固定資産</span><span class="sxs-lookup"><span data-stu-id="f9a64-153">Fixed assets</span></span>                              | <span data-ttu-id="f9a64-154">DimAttributeAssetTableEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-154">DimAttributeAssetTableEntity</span></span>              |
        | <span data-ttu-id="f9a64-155">固定資産 (ロシア)</span><span class="sxs-lookup"><span data-stu-id="f9a64-155">Fixed assets (Russia)</span></span>                     | <span data-ttu-id="f9a64-156">DimAttributeRAssetTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-156">DimAttributeRAssetTable\_RUEntity</span></span>         |
        | <span data-ttu-id="f9a64-157">資金</span><span class="sxs-lookup"><span data-stu-id="f9a64-157">Funds</span></span>                                     | <span data-ttu-id="f9a64-158">DimAttributeLedgerFund\_PSN</span><span class="sxs-lookup"><span data-stu-id="f9a64-158">DimAttributeLedgerFund\_PSN</span></span>               |
        | <span data-ttu-id="f9a64-159">品目グループ</span><span class="sxs-lookup"><span data-stu-id="f9a64-159">Item groups</span></span>                               | <span data-ttu-id="f9a64-160">DimAttributeInventItemGroupEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-160">DimAttributeInventItemGroupEntity</span></span>         |
        | <span data-ttu-id="f9a64-161">アイテム</span><span class="sxs-lookup"><span data-stu-id="f9a64-161">Items</span></span>                                     | <span data-ttu-id="f9a64-162">DimAttributeInventTableEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-162">DimAttributeInventTableEntity</span></span>             |
        | <span data-ttu-id="f9a64-163">職務</span><span class="sxs-lookup"><span data-stu-id="f9a64-163">Jobs</span></span>                                      | <span data-ttu-id="f9a64-164">DimAttributeHcmJobEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-164">DimAttributeHcmJobEntity</span></span>                  |
        | <span data-ttu-id="f9a64-165">法人</span><span class="sxs-lookup"><span data-stu-id="f9a64-165">Legal entities</span></span>                            | <span data-ttu-id="f9a64-166">DimAttributeCompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-166">DimAttributeCompanyInfoEntity</span></span>             |
        | <span data-ttu-id="f9a64-167">POS レジスター</span><span class="sxs-lookup"><span data-stu-id="f9a64-167">POS registers</span></span>                             | <span data-ttu-id="f9a64-168">DimAttributeRetailTerminalEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-168">DimAttributeRetailTerminalEntity</span></span>          |
        | <span data-ttu-id="f9a64-169">職位</span><span class="sxs-lookup"><span data-stu-id="f9a64-169">Positions</span></span>                                 | <span data-ttu-id="f9a64-170">DimAttributeHcmPositionEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-170">DimAttributeHcmPositionEntity</span></span>             |
        | <span data-ttu-id="f9a64-171">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="f9a64-171">Project contracts</span></span>                         | <span data-ttu-id="f9a64-172">DimAttributeProjInvoiceTableEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-172">DimAttributeProjInvoiceTableEntity</span></span>        |
        | <span data-ttu-id="f9a64-173">プロジェクト グループ</span><span class="sxs-lookup"><span data-stu-id="f9a64-173">Project groups</span></span>                            | <span data-ttu-id="f9a64-174">DimAttributeProjGroupEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-174">DimAttributeProjGroupEntity</span></span>               |
        | <span data-ttu-id="f9a64-175">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="f9a64-175">Projects</span></span>                                  | <span data-ttu-id="f9a64-176">DimAttributeProjTableEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-176">DimAttributeProjTableEntity</span></span>               |
        | <span data-ttu-id="f9a64-177">見込顧客</span><span class="sxs-lookup"><span data-stu-id="f9a64-177">Prospects</span></span>                                 | <span data-ttu-id="f9a64-178">DimAttributeSmmBusRelTableEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-178">DimAttributeSmmBusRelTableEntity</span></span>          |
        | <span data-ttu-id="f9a64-179">リソース グループ</span><span class="sxs-lookup"><span data-stu-id="f9a64-179">Resource groups</span></span>                           | <span data-ttu-id="f9a64-180">DimAttributeWrkCtrResourceGroupEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-180">DimAttributeWrkCtrResourceGroupEntity</span></span>     |
        | <span data-ttu-id="f9a64-181">リソース</span><span class="sxs-lookup"><span data-stu-id="f9a64-181">Resources</span></span>                                 | <span data-ttu-id="f9a64-182">DimAttributeWrkCtrTableEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-182">DimAttributeWrkCtrTableEntity</span></span>             |
        | <span data-ttu-id="f9a64-183">店舗</span><span class="sxs-lookup"><span data-stu-id="f9a64-183">Stores</span></span>                                    | <span data-ttu-id="f9a64-184">DimAttributeRetailStoreEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-184">DimAttributeRetailStoreEntity</span></span>             |
        | <span data-ttu-id="f9a64-185">バリュー ストリーム</span><span class="sxs-lookup"><span data-stu-id="f9a64-185">Value streams</span></span>                             | <span data-ttu-id="f9a64-186">DimAttributeOMValueStreamEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-186">DimAttributeOMValueStreamEntity</span></span>           |
        | <span data-ttu-id="f9a64-187">仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="f9a64-187">Vendor groups</span></span>                             | <span data-ttu-id="f9a64-188">DimAttributeVendGroupEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-188">DimAttributeVendGroupEntity</span></span>               |
        | <span data-ttu-id="f9a64-189">仕入先</span><span class="sxs-lookup"><span data-stu-id="f9a64-189">Vendors</span></span>                                   | <span data-ttu-id="f9a64-190">DimAttributeVendTableEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-190">DimAttributeVendTableEntity</span></span>               |
        | <span data-ttu-id="f9a64-191">作業者</span><span class="sxs-lookup"><span data-stu-id="f9a64-191">Workers</span></span>                                   | <span data-ttu-id="f9a64-192">DimAttributeHcmWorkerEntity</span><span class="sxs-lookup"><span data-stu-id="f9a64-192">DimAttributeHcmWorkerEntity</span></span>               |

    -   <span data-ttu-id="f9a64-193">**関連データ エンティティ カーディナリティ** - **ZeroOne**</span><span class="sxs-lookup"><span data-stu-id="f9a64-193">**Related Data Entity Cardinality** - **ZeroOne**</span></span>
    -   <span data-ttu-id="f9a64-194">**関連データ エンティティ ロール** - "分析コード部門の検索" などの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-194">**Related Data Entity Role** - Enter a unique name, such as "Dimension Department Lookup".</span></span>
    -   <span data-ttu-id="f9a64-195">**関係タイプ** - **関連**</span><span class="sxs-lookup"><span data-stu-id="f9a64-195">**Relationship Type** - **Association**</span></span>
    -   <span data-ttu-id="f9a64-196">**ロール** - 分析コード部署などの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-196">**Role** - Enter a unique name, such as Dimension Department.</span></span>

5.  <span data-ttu-id="f9a64-197">**関係** で、**財務分析コード** の名前を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="f9a64-197">Right-click the **Financial dimension** name under **Relations.**</span></span>
6.  <span data-ttu-id="f9a64-198">**新規** を選択して **標準** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9a64-198">Select **New**, and then click **Normal.**</span></span>
7.  <span data-ttu-id="f9a64-199">プロパティ ウィンドウで、**フィールド**で財務分析コードの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-199">In the Properties pane, choose the name of the Financial dimension in the **Field**.</span></span>
8.  <span data-ttu-id="f9a64-200">関連フィールドに **Value** と入力します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-200">In the Related field, type **Value**.</span></span> <span data-ttu-id="f9a64-201">新しいリレーションは、次の例のようになります:</span><span class="sxs-lookup"><span data-stu-id="f9a64-201">The new relation is similar to the following example.</span></span>

        DimensionCombinationEntity.DimensionIntegration.Department==DimAttributeOMDepartmentEntity.Value

    ![lookupwiki](./media/lookupwiki.png)

9.  <span data-ttu-id="f9a64-203">プロジェクトを構築してデータベースと同期します。</span><span class="sxs-lookup"><span data-stu-id="f9a64-203">Build the project and then synchronize it with the database.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="f9a64-204">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f9a64-204">Additional resources</span></span>

[<span data-ttu-id="f9a64-205">Microsoft Excel テンプレートへの分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="f9a64-205">Add dimensions to Microsoft Excel templates</span></span>](add-dimensions-excel-templates.md)

[<span data-ttu-id="f9a64-206">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="f9a64-206">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)



