---
title: Excel テンプレートに財務分析コードの値の検索を追加
description: このトピックでは、Microsoft Excel テンプレートで分析コード値を検索する機能を追加する方法について説明します。
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 261064
ms.assetid: f3ab87ab-ee8b-462c-bb6f-4d98e0030513
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bf04b4a98cfbee5527dcc7fcc0b569943847c180
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111742"
---
# <a name="add-lookup-values-for-financial-dimensions-to-excel-templates"></a><span data-ttu-id="4da03-103">Excel テンプレートに財務分析コードの値の検索を追加</span><span class="sxs-lookup"><span data-stu-id="4da03-103">Add lookup values for financial dimensions to Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4da03-104">このトピックでは、Microsoft Excel テンプレートで分析コード値を検索する機能を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4da03-104">This topic provides information about how you can add the ability to look up dimension values in Microsoft Excel templates.</span></span>

<span data-ttu-id="4da03-105">インストール後に Microsoft Excel テンプレートに存在する唯一の値は MainAccount です。</span><span class="sxs-lookup"><span data-stu-id="4da03-105">The only value that is present on Microsoft Excel templates after installation is MainAccount.</span></span> <span data-ttu-id="4da03-106">これは、すべての顧客が持つ唯一の分析コード です。</span><span class="sxs-lookup"><span data-stu-id="4da03-106">This is the only dimension that all customers will have.</span></span> <span data-ttu-id="4da03-107">Microsoft Excel テンプレートに分析コードを追加するには、 [Excel テンプレートへの分析コードの追加](dimensions-overview.md) トピックの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4da03-107">To add the dimensions to Microsoft Excel templates, you need to complete the steps in the [Add dimensions to Excel templates](dimensions-overview.md) topic.</span></span> <span data-ttu-id="4da03-108">分析コードを追加した後、分析コード値の一覧を検索する機能が必要な場合このトピックの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="4da03-108">After you have added the dimensions, if you want the ability to look up a list of dimension values, complete the steps in this topic.</span></span> 

> [!NOTE]
> <span data-ttu-id="4da03-109">この情報は、リリースごとに変更される可能性がありますので、定期的に最新の情報を確認してください。</span><span class="sxs-lookup"><span data-stu-id="4da03-109">This information is subject to change for each release, so be sure to check back frequently for the most up-to-date information.</span></span>

1.  <span data-ttu-id="4da03-110">Visual Studio で、**DimensionCombinationEntity** または **DimensionSetEntity** を変更したプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="4da03-110">In Visual Studio, open the project where you modified **DimensionCombinationEntity** or **DimensionSetEntity.**</span></span>
2.  <span data-ttu-id="4da03-111">**DimensionCombinationEntity** または **DimensionSetEntity** を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="4da03-111">Right-click **DimensionCombinationEntity** or **DimensionSetEntity**.</span></span> <span data-ttu-id="4da03-112">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4da03-112">Select **Open**.</span></span>
3.  <span data-ttu-id="4da03-113">**関係** を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="4da03-113">Right click **Relations**.</span></span> <span data-ttu-id="4da03-114">**新規** を選択して **関係** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4da03-114">Select **New** and then click **Relation.**</span></span>
4.  <span data-ttu-id="4da03-115">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4da03-115">In the **Properties** pane, set the following properties.</span></span>
    -   <span data-ttu-id="4da03-116">**検証** - 番号</span><span class="sxs-lookup"><span data-stu-id="4da03-116">**Validate** - No</span></span>
    -   <span data-ttu-id="4da03-117">**基数** - ZeroMore</span><span class="sxs-lookup"><span data-stu-id="4da03-117">**Cardinality** - ZeroMore</span></span>
    -   <span data-ttu-id="4da03-118">**名前** - 部門などの、財務分析コードの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4da03-118">**Name** - Enter the name of the financial dimension, such as Department.</span></span>
    -   <span data-ttu-id="4da03-119">**関連データ エンティティ** - **名前** フィールドで入力した財務分析コードのエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="4da03-119">**Related Data Entity** - Select the entity for the financial dimension that you entered in the **Name** field.</span></span> <span data-ttu-id="4da03-120">次のテーブルに、財務分析コードと関連するエンティティの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="4da03-120">The following table contains a list of the financial dimensions and the related entities.</span></span>

        | <span data-ttu-id="4da03-121">財務分析コード '値の使用元'</span><span class="sxs-lookup"><span data-stu-id="4da03-121">Financial dimension 'Use values from'</span></span>     | <span data-ttu-id="4da03-122">関連するエンティティ</span><span class="sxs-lookup"><span data-stu-id="4da03-122">Related entity</span></span>                            |
        |-------------------------------------------|-------------------------------------------|
        | <span data-ttu-id="4da03-123">&lt; カスタム分析コード &gt;</span><span class="sxs-lookup"><span data-stu-id="4da03-123">&lt; Custom dimension &gt;</span></span>                | <span data-ttu-id="4da03-124">DimAttributeFinancialTagEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-124">DimAttributeFinancialTagEntity</span></span>            |
        | <span data-ttu-id="4da03-125">契約</span><span class="sxs-lookup"><span data-stu-id="4da03-125">Agreements</span></span>                                | <span data-ttu-id="4da03-126">DimAttributeAgreementHeaderExt\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-126">DimAttributeAgreementHeaderExt\_RUEntity</span></span>  |
        | <span data-ttu-id="4da03-127">銀行口座</span><span class="sxs-lookup"><span data-stu-id="4da03-127">Bank accounts</span></span>                             | <span data-ttu-id="4da03-128">DimAttributeBankAccountTableEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-128">DimAttributeBankAccountTableEntity</span></span>        |
        | <span data-ttu-id="4da03-129">BusinessUnits</span><span class="sxs-lookup"><span data-stu-id="4da03-129">BusinessUnits</span></span>                             | <span data-ttu-id="4da03-130">DimAttributeOMBusinessUnitEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-130">DimAttributeOMBusinessUnitEntity</span></span>          |
        | <span data-ttu-id="4da03-131">キャンペーン</span><span class="sxs-lookup"><span data-stu-id="4da03-131">Campaigns</span></span>                                 | <span data-ttu-id="4da03-132">DimAttributeSmmCampaignTableEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-132">DimAttributeSmmCampaignTableEntity</span></span>        |
        | <span data-ttu-id="4da03-133">現金勘定</span><span class="sxs-lookup"><span data-stu-id="4da03-133">Cash accounts</span></span>                             | <span data-ttu-id="4da03-134">DimAttributeRCashTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-134">DimAttributeRCashTable\_RUEntity</span></span>          |
        | <span data-ttu-id="4da03-135">コスト センター</span><span class="sxs-lookup"><span data-stu-id="4da03-135">Cost centers</span></span>                              | <span data-ttu-id="4da03-136">DimAttributeOMCostCenterEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-136">DimAttributeOMCostCenterEntity</span></span>            |
        | <span data-ttu-id="4da03-137">顧客グループ</span><span class="sxs-lookup"><span data-stu-id="4da03-137">Customer groups</span></span>                           | <span data-ttu-id="4da03-138">DimAttributeCustGroupEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-138">DimAttributeCustGroupEntity</span></span>               |
        | <span data-ttu-id="4da03-139">顧客</span><span class="sxs-lookup"><span data-stu-id="4da03-139">Customers</span></span>                                 | <span data-ttu-id="4da03-140">DimAttributeCustTableEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-140">DimAttributeCustTableEntity</span></span>               |
        | <span data-ttu-id="4da03-141">繰延</span><span class="sxs-lookup"><span data-stu-id="4da03-141">Deferrals</span></span>                                 | <span data-ttu-id="4da03-142">DimAttributeRDeferralsTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-142">DimAttributeRDeferralsTable\_RUEntity</span></span>     |
        | <span data-ttu-id="4da03-143">部門</span><span class="sxs-lookup"><span data-stu-id="4da03-143">Departments</span></span>                               | <span data-ttu-id="4da03-144">DimAttributeOMDepartmentEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-144">DimAttributeOMDepartmentEntity</span></span>            |
        | <span data-ttu-id="4da03-145">経費および所得コード</span><span class="sxs-lookup"><span data-stu-id="4da03-145">Expense and income codes</span></span>                  | <span data-ttu-id="4da03-146">DimAttributeRTax25ProfitTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-146">DimAttributeRTax25ProfitTable\_RUEntity</span></span>   |
        | <span data-ttu-id="4da03-147">経費の目的</span><span class="sxs-lookup"><span data-stu-id="4da03-147">Expense Purposes</span></span>                          | <span data-ttu-id="4da03-148">DimAttributeTrvTravelTxtEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-148">DimAttributeTrvTravelTxtEntity</span></span>            |
        | <span data-ttu-id="4da03-149">会計施設</span><span class="sxs-lookup"><span data-stu-id="4da03-149">Fiscal establishments</span></span>                     | <span data-ttu-id="4da03-150">DimAttributeFiscalEstablishment\_BREntity</span><span class="sxs-lookup"><span data-stu-id="4da03-150">DimAttributeFiscalEstablishment\_BREntity</span></span> |
        | <span data-ttu-id="4da03-151">固定資産グループ</span><span class="sxs-lookup"><span data-stu-id="4da03-151">Fixed asset groups</span></span>                        | <span data-ttu-id="4da03-152">DimAttributeAssetGroupEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-152">DimAttributeAssetGroupEntity</span></span>              |
        | <span data-ttu-id="4da03-153">固定資産</span><span class="sxs-lookup"><span data-stu-id="4da03-153">Fixed assets</span></span>                              | <span data-ttu-id="4da03-154">DimAttributeAssetTableEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-154">DimAttributeAssetTableEntity</span></span>              |
        | <span data-ttu-id="4da03-155">固定資産 (ロシア)</span><span class="sxs-lookup"><span data-stu-id="4da03-155">Fixed assets (Russia)</span></span>                     | <span data-ttu-id="4da03-156">DimAttributeRAssetTable\_RUEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-156">DimAttributeRAssetTable\_RUEntity</span></span>         |
        | <span data-ttu-id="4da03-157">資金</span><span class="sxs-lookup"><span data-stu-id="4da03-157">Funds</span></span>                                     | <span data-ttu-id="4da03-158">DimAttributeLedgerFund\_PSN</span><span class="sxs-lookup"><span data-stu-id="4da03-158">DimAttributeLedgerFund\_PSN</span></span>               |
        | <span data-ttu-id="4da03-159">品目グループ</span><span class="sxs-lookup"><span data-stu-id="4da03-159">Item groups</span></span>                               | <span data-ttu-id="4da03-160">DimAttributeInventItemGroupEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-160">DimAttributeInventItemGroupEntity</span></span>         |
        | <span data-ttu-id="4da03-161">アイテム</span><span class="sxs-lookup"><span data-stu-id="4da03-161">Items</span></span>                                     | <span data-ttu-id="4da03-162">DimAttributeInventTableEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-162">DimAttributeInventTableEntity</span></span>             |
        | <span data-ttu-id="4da03-163">職務</span><span class="sxs-lookup"><span data-stu-id="4da03-163">Jobs</span></span>                                      | <span data-ttu-id="4da03-164">DimAttributeHcmJobEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-164">DimAttributeHcmJobEntity</span></span>                  |
        | <span data-ttu-id="4da03-165">法人</span><span class="sxs-lookup"><span data-stu-id="4da03-165">Legal entities</span></span>                            | <span data-ttu-id="4da03-166">DimAttributeCompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-166">DimAttributeCompanyInfoEntity</span></span>             |
        | <span data-ttu-id="4da03-167">POS レジスター</span><span class="sxs-lookup"><span data-stu-id="4da03-167">POS registers</span></span>                             | <span data-ttu-id="4da03-168">DimAttributeRetailTerminalEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-168">DimAttributeRetailTerminalEntity</span></span>          |
        | <span data-ttu-id="4da03-169">職位</span><span class="sxs-lookup"><span data-stu-id="4da03-169">Positions</span></span>                                 | <span data-ttu-id="4da03-170">DimAttributeHcmPositionEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-170">DimAttributeHcmPositionEntity</span></span>             |
        | <span data-ttu-id="4da03-171">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="4da03-171">Project contracts</span></span>                         | <span data-ttu-id="4da03-172">DimAttributeProjInvoiceTableEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-172">DimAttributeProjInvoiceTableEntity</span></span>        |
        | <span data-ttu-id="4da03-173">プロジェクト グループ</span><span class="sxs-lookup"><span data-stu-id="4da03-173">Project groups</span></span>                            | <span data-ttu-id="4da03-174">DimAttributeProjGroupEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-174">DimAttributeProjGroupEntity</span></span>               |
        | <span data-ttu-id="4da03-175">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="4da03-175">Projects</span></span>                                  | <span data-ttu-id="4da03-176">DimAttributeProjTableEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-176">DimAttributeProjTableEntity</span></span>               |
        | <span data-ttu-id="4da03-177">見込顧客</span><span class="sxs-lookup"><span data-stu-id="4da03-177">Prospects</span></span>                                 | <span data-ttu-id="4da03-178">DimAttributeSmmBusRelTableEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-178">DimAttributeSmmBusRelTableEntity</span></span>          |
        | <span data-ttu-id="4da03-179">リソース グループ</span><span class="sxs-lookup"><span data-stu-id="4da03-179">Resource groups</span></span>                           | <span data-ttu-id="4da03-180">DimAttributeWrkCtrResourceGroupEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-180">DimAttributeWrkCtrResourceGroupEntity</span></span>     |
        | <span data-ttu-id="4da03-181">リソース</span><span class="sxs-lookup"><span data-stu-id="4da03-181">Resources</span></span>                                 | <span data-ttu-id="4da03-182">DimAttributeWrkCtrTableEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-182">DimAttributeWrkCtrTableEntity</span></span>             |
        | <span data-ttu-id="4da03-183">店舗</span><span class="sxs-lookup"><span data-stu-id="4da03-183">Stores</span></span>                                    | <span data-ttu-id="4da03-184">DimAttributeRetailStoreEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-184">DimAttributeRetailStoreEntity</span></span>             |
        | <span data-ttu-id="4da03-185">バリュー ストリーム</span><span class="sxs-lookup"><span data-stu-id="4da03-185">Value streams</span></span>                             | <span data-ttu-id="4da03-186">DimAttributeOMValueStreamEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-186">DimAttributeOMValueStreamEntity</span></span>           |
        | <span data-ttu-id="4da03-187">仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="4da03-187">Vendor groups</span></span>                             | <span data-ttu-id="4da03-188">DimAttributeVendGroupEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-188">DimAttributeVendGroupEntity</span></span>               |
        | <span data-ttu-id="4da03-189">仕入先</span><span class="sxs-lookup"><span data-stu-id="4da03-189">Vendors</span></span>                                   | <span data-ttu-id="4da03-190">DimAttributeVendTableEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-190">DimAttributeVendTableEntity</span></span>               |
        | <span data-ttu-id="4da03-191">作業者</span><span class="sxs-lookup"><span data-stu-id="4da03-191">Workers</span></span>                                   | <span data-ttu-id="4da03-192">DimAttributeHcmWorkerEntity</span><span class="sxs-lookup"><span data-stu-id="4da03-192">DimAttributeHcmWorkerEntity</span></span>               |

    -   <span data-ttu-id="4da03-193">**関連データ エンティティ カーディナリティ** - **ZeroOne**</span><span class="sxs-lookup"><span data-stu-id="4da03-193">**Related Data Entity Cardinality** - **ZeroOne**</span></span>
    -   <span data-ttu-id="4da03-194">**関連データ エンティティ ロール** - "分析コード部門の検索" などの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4da03-194">**Related Data Entity Role** - Enter a unique name, such as "Dimension Department Lookup".</span></span>
    -   <span data-ttu-id="4da03-195">**関係タイプ** - **関連**</span><span class="sxs-lookup"><span data-stu-id="4da03-195">**Relationship Type** - **Association**</span></span>
    -   <span data-ttu-id="4da03-196">**ロール** - 分析コード部署などの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4da03-196">**Role** - Enter a unique name, such as Dimension Department.</span></span>

5.  <span data-ttu-id="4da03-197">**関係** で、**財務分析コード** の名前を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="4da03-197">Right-click the **Financial dimension** name under **Relations.**</span></span>
6.  <span data-ttu-id="4da03-198">**新規** を選択して **標準** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4da03-198">Select **New**, and then click **Normal.**</span></span>
7.  <span data-ttu-id="4da03-199">プロパティ ウィンドウで、**フィールド** で財務分析コードの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="4da03-199">In the Properties pane, choose the name of the Financial dimension in the **Field**.</span></span>
8.  <span data-ttu-id="4da03-200">関連フィールドに **Value** と入力します。</span><span class="sxs-lookup"><span data-stu-id="4da03-200">In the Related field, type **Value**.</span></span> <span data-ttu-id="4da03-201">新しいリレーションは、次の例のようになります:</span><span class="sxs-lookup"><span data-stu-id="4da03-201">The new relation is similar to the following example.</span></span>
    
    ```xpp
    DimensionCombinationEntity.DimensionIntegration.Department==DimAttributeOMDepartmentEntity.Value
    ```

    ![Visual Studio の関係プロパティ](./media/lookupwiki.png)

9.  <span data-ttu-id="4da03-203">プロジェクトを構築してデータベースと同期します。</span><span class="sxs-lookup"><span data-stu-id="4da03-203">Build the project and then synchronize it with the database.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="4da03-204">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4da03-204">Additional resources</span></span>

[<span data-ttu-id="4da03-205">Excel テンプレートに財務分析コードの値の検索を追加</span><span class="sxs-lookup"><span data-stu-id="4da03-205">Add lookup values for financial dimensions to Excel templates</span></span>](add-dimensions-excel-templates.md)

[<span data-ttu-id="4da03-206">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="4da03-206">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)

<span data-ttu-id="4da03-207">[[Excel で開く] エクスペリエンスの作成](../office-integration/office-integration-edit-excel.md)</span><span class="sxs-lookup"><span data-stu-id="4da03-207">[Create Open in Excel experiences](../office-integration/office-integration-edit-excel.md)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]