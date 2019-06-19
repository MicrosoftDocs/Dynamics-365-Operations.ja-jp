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
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 261064
ms.assetid: f3ab87ab-ee8b-462c-bb6f-4d98e0030513
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 571fa8b12ead1e59a06524aad9f36b201f81d43b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554537"
---
# <a name="add-lookup-values-for-financial-dimensions-to-excel-templates"></a><span data-ttu-id="8aefb-103">Excel テンプレートに財務分析コードの値の検索を追加</span><span class="sxs-lookup"><span data-stu-id="8aefb-103">Add lookup values for financial dimensions to Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8aefb-104">このトピックでは、Microsoft Excel テンプレートで分析コード値を検索する機能を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-104">This topic provides information about how you can add the ability to look up dimension values in Microsoft Excel templates.</span></span>

<span data-ttu-id="8aefb-105">インストール後に Microsoft Excel テンプレートに存在する唯一の値は MainAccount です。</span><span class="sxs-lookup"><span data-stu-id="8aefb-105">The only value that is present on Microsoft Excel templates after installation is MainAccount.</span></span> <span data-ttu-id="8aefb-106">これは、すべての顧客が持つ唯一の分析コード です。</span><span class="sxs-lookup"><span data-stu-id="8aefb-106">This is the only dimension that all customers will have.</span></span> <span data-ttu-id="8aefb-107">Microsoft Excel テンプレートに分析コードを追加するには、[Microsoft Excel テンプレートに分析コードを追加](dimensions-overview.md) トピックの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8aefb-107">To add the dimensions to Microsoft Excel templates, you need to complete the steps in the [Add dimensions to the Microsoft Excel templates](dimensions-overview.md) topic.</span></span> <span data-ttu-id="8aefb-108">分析コードを追加した後、分析コード値の一覧を検索する機能が必要な場合このトピックの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-108">After you have added the dimensions, if you want the ability to look up a list of dimension values, complete the steps in this topic.</span></span> <span data-ttu-id="8aefb-109">**注記:** この情報は、リリースごとに変更される可能性がありますので、定期的に最新の情報を確認してください。</span><span class="sxs-lookup"><span data-stu-id="8aefb-109">**Note:**  This information is subject to change for each release, so be sure to check back frequently for the most up-to-date information.</span></span>

1.  <span data-ttu-id="8aefb-110">Visual Studio で、**DimensionCombinationEntity** または **DimensionSetEntity** を変更したプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="8aefb-110">In Visual Studio, open the project where you modified **DimensionCombinationEntity** or **DimensionSetEntity.**</span></span>
2.  <span data-ttu-id="8aefb-111">**DimensionCombinationEntity** または **DimensionSetEntity** を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="8aefb-111">Right-click **DimensionCombinationEntity** or **DimensionSetEntity**.</span></span> <span data-ttu-id="8aefb-112">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-112">Select **Open**.</span></span>
3.  <span data-ttu-id="8aefb-113">**関係** を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="8aefb-113">Right click **Relations**.</span></span> <span data-ttu-id="8aefb-114">**新規** を選択して **関係** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8aefb-114">Select **New** and then click **Relation.**</span></span>
4.  <span data-ttu-id="8aefb-115">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-115">In the **Properties** pane, set the following properties.</span></span>
    -   <span data-ttu-id="8aefb-116">**検証** - 番号</span><span class="sxs-lookup"><span data-stu-id="8aefb-116">**Validate** - No</span></span>
    -   <span data-ttu-id="8aefb-117">**基数** - ZeroMore</span><span class="sxs-lookup"><span data-stu-id="8aefb-117">**Cardinality** - ZeroMore</span></span>
    -   <span data-ttu-id="8aefb-118">**名前** - 部門などの、財務分析コードの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-118">**Name** - Enter the name of the financial dimension, such as Department.</span></span>
    -   <span data-ttu-id="8aefb-119">**関連データ エンティティ** - **名前**フィールドで入力した財務分析コードのエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-119">**Related Data Entity** - Select the entity for the financial dimension that you entered in the **Name** field.</span></span> <span data-ttu-id="8aefb-120">次のテーブルに、財務分析コードと関連するエンティティの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-120">The following table contains a list of the financial dimensions and the related entities.</span></span>

        | <span data-ttu-id="8aefb-121">**財務分析コード '値の使用元'**</span><span class="sxs-lookup"><span data-stu-id="8aefb-121">**Financial dimension 'Use values from'**</span></span> | <span data-ttu-id="8aefb-122">**関連するエンティティ**</span><span class="sxs-lookup"><span data-stu-id="8aefb-122">**Related entity**</span></span>                        |
        |-------------------------------------------|-------------------------------------------|
        | <span data-ttu-id="8aefb-123">&lt; カスタム分析コード &gt;</span><span class="sxs-lookup"><span data-stu-id="8aefb-123">&lt; Custom dimension &gt;</span></span>                | <span data-ttu-id="8aefb-124">DimAttributeFinancialTagEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-124">DimAttributeFinancialTagEntity</span></span>            |
        | <span data-ttu-id="8aefb-125">契約</span><span class="sxs-lookup"><span data-stu-id="8aefb-125">Agreements</span></span>                                | <span data-ttu-id="8aefb-126">DimAttributeAgreementHeaderExt\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-126">DimAttributeAgreementHeaderExt\_RUEntity</span></span>  |
        | <span data-ttu-id="8aefb-127">銀行口座</span><span class="sxs-lookup"><span data-stu-id="8aefb-127">Bank accounts</span></span>                             | <span data-ttu-id="8aefb-128">DimAttributeBankAccountTableEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-128">DimAttributeBankAccountTableEntity</span></span>        |
        | <span data-ttu-id="8aefb-129">BusinessUnits</span><span class="sxs-lookup"><span data-stu-id="8aefb-129">BusinessUnits</span></span>                             | <span data-ttu-id="8aefb-130">DimAttributeOMBusinessUnitEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-130">DimAttributeOMBusinessUnitEntity</span></span>          |
        | <span data-ttu-id="8aefb-131">キャンペーン</span><span class="sxs-lookup"><span data-stu-id="8aefb-131">Campaigns</span></span>                                 | <span data-ttu-id="8aefb-132">DimAttributeSmmCampaignTableEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-132">DimAttributeSmmCampaignTableEntity</span></span>        |
        | <span data-ttu-id="8aefb-133">現金勘定</span><span class="sxs-lookup"><span data-stu-id="8aefb-133">Cash accounts</span></span>                             | <span data-ttu-id="8aefb-134">DimAttributeRCashTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-134">DimAttributeRCashTable\_RUEntity</span></span>          |
        | <span data-ttu-id="8aefb-135">コスト センター</span><span class="sxs-lookup"><span data-stu-id="8aefb-135">Cost centers</span></span>                              | <span data-ttu-id="8aefb-136">DimAttributeOMCostCenterEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-136">DimAttributeOMCostCenterEntity</span></span>            |
        | <span data-ttu-id="8aefb-137">顧客グループ</span><span class="sxs-lookup"><span data-stu-id="8aefb-137">Customer groups</span></span>                           | <span data-ttu-id="8aefb-138">DimAttributeCustGroupEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-138">DimAttributeCustGroupEntity</span></span>               |
        | <span data-ttu-id="8aefb-139">顧客</span><span class="sxs-lookup"><span data-stu-id="8aefb-139">Customers</span></span>                                 | <span data-ttu-id="8aefb-140">DimAttributeCustTableEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-140">DimAttributeCustTableEntity</span></span>               |
        | <span data-ttu-id="8aefb-141">繰延</span><span class="sxs-lookup"><span data-stu-id="8aefb-141">Deferrals</span></span>                                 | <span data-ttu-id="8aefb-142">DimAttributeRDeferralsTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-142">DimAttributeRDeferralsTable\_RUEntity</span></span>     |
        | <span data-ttu-id="8aefb-143">部門</span><span class="sxs-lookup"><span data-stu-id="8aefb-143">Departments</span></span>                               | <span data-ttu-id="8aefb-144">DimAttributeOMDepartmentEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-144">DimAttributeOMDepartmentEntity</span></span>            |
        | <span data-ttu-id="8aefb-145">経費および所得コード</span><span class="sxs-lookup"><span data-stu-id="8aefb-145">Expense and income codes</span></span>                  | <span data-ttu-id="8aefb-146">DimAttributeRTax25ProfitTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-146">DimAttributeRTax25ProfitTable\_RUEntity</span></span>   |
        | <span data-ttu-id="8aefb-147">経費の目的</span><span class="sxs-lookup"><span data-stu-id="8aefb-147">Expense Purposes</span></span>                          | <span data-ttu-id="8aefb-148">DimAttributeTrvTravelTxtEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-148">DimAttributeTrvTravelTxtEntity</span></span>            |
        | <span data-ttu-id="8aefb-149">会計施設</span><span class="sxs-lookup"><span data-stu-id="8aefb-149">Fiscal establishments</span></span>                     | <span data-ttu-id="8aefb-150">DimAttributeFiscalEstablishment\_BREntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-150">DimAttributeFiscalEstablishment\_BREntity</span></span> |
        | <span data-ttu-id="8aefb-151">固定資産グループ</span><span class="sxs-lookup"><span data-stu-id="8aefb-151">Fixed asset groups</span></span>                        | <span data-ttu-id="8aefb-152">DimAttributeAssetGroupEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-152">DimAttributeAssetGroupEntity</span></span>              |
        | <span data-ttu-id="8aefb-153">固定資産</span><span class="sxs-lookup"><span data-stu-id="8aefb-153">Fixed assets</span></span>                              | <span data-ttu-id="8aefb-154">DimAttributeAssetTableEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-154">DimAttributeAssetTableEntity</span></span>              |
        | <span data-ttu-id="8aefb-155">固定資産 (ロシア)</span><span class="sxs-lookup"><span data-stu-id="8aefb-155">Fixed assets (Russia)</span></span>                     | <span data-ttu-id="8aefb-156">DimAttributeRAssetTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-156">DimAttributeRAssetTable\_RUEntity</span></span>         |
        | <span data-ttu-id="8aefb-157">資金</span><span class="sxs-lookup"><span data-stu-id="8aefb-157">Funds</span></span>                                     | <span data-ttu-id="8aefb-158">DimAttributeLedgerFund\_PSN</span><span class="sxs-lookup"><span data-stu-id="8aefb-158">DimAttributeLedgerFund\_PSN</span></span>               |
        | <span data-ttu-id="8aefb-159">品目グループ</span><span class="sxs-lookup"><span data-stu-id="8aefb-159">Item groups</span></span>                               | <span data-ttu-id="8aefb-160">DimAttributeInventItemGroupEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-160">DimAttributeInventItemGroupEntity</span></span>         |
        | <span data-ttu-id="8aefb-161">アイテム</span><span class="sxs-lookup"><span data-stu-id="8aefb-161">Items</span></span>                                     | <span data-ttu-id="8aefb-162">DimAttributeInventTableEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-162">DimAttributeInventTableEntity</span></span>             |
        | <span data-ttu-id="8aefb-163">職務</span><span class="sxs-lookup"><span data-stu-id="8aefb-163">Jobs</span></span>                                      | <span data-ttu-id="8aefb-164">DimAttributeHcmJobEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-164">DimAttributeHcmJobEntity</span></span>                  |
        | <span data-ttu-id="8aefb-165">法人</span><span class="sxs-lookup"><span data-stu-id="8aefb-165">Legal entities</span></span>                            | <span data-ttu-id="8aefb-166">DimAttributeCompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-166">DimAttributeCompanyInfoEntity</span></span>             |
        | <span data-ttu-id="8aefb-167">POS レジスター</span><span class="sxs-lookup"><span data-stu-id="8aefb-167">POS registers</span></span>                             | <span data-ttu-id="8aefb-168">DimAttributeRetailTerminalEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-168">DimAttributeRetailTerminalEntity</span></span>          |
        | <span data-ttu-id="8aefb-169">職位</span><span class="sxs-lookup"><span data-stu-id="8aefb-169">Positions</span></span>                                 | <span data-ttu-id="8aefb-170">DimAttributeHcmPositionEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-170">DimAttributeHcmPositionEntity</span></span>             |
        | <span data-ttu-id="8aefb-171">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="8aefb-171">Project contracts</span></span>                         | <span data-ttu-id="8aefb-172">DimAttributeProjInvoiceTableEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-172">DimAttributeProjInvoiceTableEntity</span></span>        |
        | <span data-ttu-id="8aefb-173">プロジェクト グループ</span><span class="sxs-lookup"><span data-stu-id="8aefb-173">Project groups</span></span>                            | <span data-ttu-id="8aefb-174">DimAttributeProjGroupEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-174">DimAttributeProjGroupEntity</span></span>               |
        | <span data-ttu-id="8aefb-175">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="8aefb-175">Projects</span></span>                                  | <span data-ttu-id="8aefb-176">DimAttributeProjTableEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-176">DimAttributeProjTableEntity</span></span>               |
        | <span data-ttu-id="8aefb-177">見込顧客</span><span class="sxs-lookup"><span data-stu-id="8aefb-177">Prospects</span></span>                                 | <span data-ttu-id="8aefb-178">DimAttributeSmmBusRelTableEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-178">DimAttributeSmmBusRelTableEntity</span></span>          |
        | <span data-ttu-id="8aefb-179">リソース グループ</span><span class="sxs-lookup"><span data-stu-id="8aefb-179">Resource groups</span></span>                           | <span data-ttu-id="8aefb-180">DimAttributeWrkCtrResourceGroupEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-180">DimAttributeWrkCtrResourceGroupEntity</span></span>     |
        | <span data-ttu-id="8aefb-181">リソース</span><span class="sxs-lookup"><span data-stu-id="8aefb-181">Resources</span></span>                                 | <span data-ttu-id="8aefb-182">DimAttributeWrkCtrTableEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-182">DimAttributeWrkCtrTableEntity</span></span>             |
        | <span data-ttu-id="8aefb-183">店舗</span><span class="sxs-lookup"><span data-stu-id="8aefb-183">Stores</span></span>                                    | <span data-ttu-id="8aefb-184">DimAttributeRetailStoreEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-184">DimAttributeRetailStoreEntity</span></span>             |
        | <span data-ttu-id="8aefb-185">バリュー ストリーム</span><span class="sxs-lookup"><span data-stu-id="8aefb-185">Value streams</span></span>                             | <span data-ttu-id="8aefb-186">DimAttributeOMValueStreamEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-186">DimAttributeOMValueStreamEntity</span></span>           |
        | <span data-ttu-id="8aefb-187">仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="8aefb-187">Vendor groups</span></span>                             | <span data-ttu-id="8aefb-188">DimAttributeVendGroupEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-188">DimAttributeVendGroupEntity</span></span>               |
        | <span data-ttu-id="8aefb-189">仕入先</span><span class="sxs-lookup"><span data-stu-id="8aefb-189">Vendors</span></span>                                   | <span data-ttu-id="8aefb-190">DimAttributeVendTableEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-190">DimAttributeVendTableEntity</span></span>               |
        | <span data-ttu-id="8aefb-191">作業者</span><span class="sxs-lookup"><span data-stu-id="8aefb-191">Workers</span></span>                                   | <span data-ttu-id="8aefb-192">DimAttributeHcmWorkerEntity</span><span class="sxs-lookup"><span data-stu-id="8aefb-192">DimAttributeHcmWorkerEntity</span></span>               |

    -   <span data-ttu-id="8aefb-193">**関連データ エンティティ カーディナリティ** - **ZeroOne**</span><span class="sxs-lookup"><span data-stu-id="8aefb-193">**Related Data Entity Cardinality** - **ZeroOne**</span></span>
    -   <span data-ttu-id="8aefb-194">**関連データ エンティティ ロール** - 分析コード部署などの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-194">**Related Data Entity Role** - Enter a unique name, such as Dimension Department.</span></span>
    -   <span data-ttu-id="8aefb-195">**関係タイプ** - **関連**</span><span class="sxs-lookup"><span data-stu-id="8aefb-195">**Relationship Type** - **Association**</span></span>
    -   <span data-ttu-id="8aefb-196">**ロール** - 分析コード部署などの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-196">**Role** - Enter a unique name, such as Dimension Department.</span></span>

5.  <span data-ttu-id="8aefb-197">**関係** で、**財務分析コード** の名前を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="8aefb-197">Right-click the **Financial dimension** name under **Relations.**</span></span>
6.  <span data-ttu-id="8aefb-198">**新規** を選択して **標準** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8aefb-198">Select **New**, and then click **Normal.**</span></span>
7.  <span data-ttu-id="8aefb-199">プロパティ ウィンドウで、**フィールド**で財務分析コードの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-199">In the Properties pane, choose the name of the Financial dimension in the **Field**.</span></span>
8.  <span data-ttu-id="8aefb-200">関連フィールドに **Value** と入力します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-200">In the Related field, type **Value**.</span></span> <span data-ttu-id="8aefb-201">新しいリレーションは、次の例のようになります:</span><span class="sxs-lookup"><span data-stu-id="8aefb-201">The new relation is similar to the following example.</span></span>

        DimensionCombinationEntity.DimensionIntegration.Department==DimAttributeOMDepartmentEntity.Value

    ![lookupwiki](./media/lookupwiki.png)

9.  <span data-ttu-id="8aefb-203">プロジェクトを構築してデータベースと同期します。</span><span class="sxs-lookup"><span data-stu-id="8aefb-203">Build the project and then synchronize it with the database.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="8aefb-204">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8aefb-204">Additional resources</span></span>

[<span data-ttu-id="8aefb-205">Microsoft Excel テンプレートへの分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="8aefb-205">Add dimensions to Microsoft Excel templates</span></span>](add-dimensions-excel-templates.md)

[<span data-ttu-id="8aefb-206">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="8aefb-206">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)



