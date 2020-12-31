---
title: Dynamics 365 Finance の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。
author: roschlom
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a406db6d78302fa05596a58fffb7464222d4bfea
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689497"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="82de8-103">Dynamics 365 Finance の削除済みまたは推奨されない機能</span><span class="sxs-lookup"><span data-stu-id="82de8-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82de8-104">このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="82de8-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="82de8-105">*削除された* 機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="82de8-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="82de8-106">*削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="82de8-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="82de8-107">このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="82de8-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="82de8-108">Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82de8-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="82de8-109">これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。</span><span class="sxs-lookup"><span data-stu-id="82de8-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a><span data-ttu-id="82de8-110">Finance 10.0.16 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="82de8-110">Features removed or deprecated in the Finance 10.0.16 release</span></span>

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a><span data-ttu-id="82de8-111">"元帳トランザクションのエクスポート形式 (BE)" 電子レポート形式と、個別の "元帳トランザクション エクスポート (BE)" モデル (ベルギー)</span><span class="sxs-lookup"><span data-stu-id="82de8-111">"Ledger transaction export format (BE)" Electronic reporting format and respective "Ledger transaction export (BE)" model for Belgium</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="82de8-112">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="82de8-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="82de8-113">"標準監査ファイル (SAF)" モデルの下にある新しい ER 形式で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="82de8-113">Replaced with new ER format under "Standard Audit File (SAF-T)" model.</span></span>  |
| <span data-ttu-id="82de8-114">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="82de8-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="82de8-115">あり</span><span class="sxs-lookup"><span data-stu-id="82de8-115">Yes</span></span> |
| <span data-ttu-id="82de8-116">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="82de8-116">**Product areas affected**</span></span>         | <span data-ttu-id="82de8-117">申請書</span><span class="sxs-lookup"><span data-stu-id="82de8-117">Application</span></span> |
| <span data-ttu-id="82de8-118">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="82de8-118">**Deployment option**</span></span>              | <span data-ttu-id="82de8-119">All</span><span class="sxs-lookup"><span data-stu-id="82de8-119">All</span></span> |
| <span data-ttu-id="82de8-120">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="82de8-120">**Status**</span></span>                         | <span data-ttu-id="82de8-121">非推奨: 2021 年 12 月 1 日までに、"元帳トランザクションのエクスポート形式 (BE)" 電子レポート (ER) 形式と、個別の "元帳トランザクション エクスポート (BE)" モデルのサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="82de8-121">Deprecated: By December 1, 2021, we plan to no longer support the "Ledger transaction export format (BE)" Electronic reporting (ER) format and respective "Ledger transaction export (BE)" model.</span></span> <span data-ttu-id="82de8-122">"標準監査ファイル (SAF)" モデルの代わりに、新しい "一般会計のデータ エクスポート (BE)" 形式と "一般会計のデータ モデル マッピング" が導入されます。</span><span class="sxs-lookup"><span data-stu-id="82de8-122">A new "General ledger data export (BE)" format together with "General ledger data model mapping" are introduced instead under the "Standard Audit File (SAF-T)" model.</span></span> |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a><span data-ttu-id="82de8-123">SSRS 形式の英国用 "VAT 100" レポート</span><span class="sxs-lookup"><span data-stu-id="82de8-123">"VAT 100" report for the United Kingdom in SSRS format</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="82de8-124">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="82de8-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="82de8-125">"税申告モデル" で、新しい ER 形式である "VAT 申告 Excel (UK)" 形式と置き換えました。</span><span class="sxs-lookup"><span data-stu-id="82de8-125">Replaced with new ER format - "VAT Declaration Excel (UK)" format under "Tax declaration model".</span></span>  |
| <span data-ttu-id="82de8-126">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="82de8-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="82de8-127">あり</span><span class="sxs-lookup"><span data-stu-id="82de8-127">Yes</span></span> |
| <span data-ttu-id="82de8-128">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="82de8-128">**Product areas affected**</span></span>         | <span data-ttu-id="82de8-129">申請書</span><span class="sxs-lookup"><span data-stu-id="82de8-129">Application</span></span> |
| <span data-ttu-id="82de8-130">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="82de8-130">**Deployment option**</span></span>              | <span data-ttu-id="82de8-131">All</span><span class="sxs-lookup"><span data-stu-id="82de8-131">All</span></span> |
| <span data-ttu-id="82de8-132">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="82de8-132">**Status**</span></span>                         | <span data-ttu-id="82de8-133">非推奨: 2021 年 12 月 1 日までに、SSRS 形式の "VAT 100 レポート" のサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="82de8-133">Deprecated: By December 1, 2021, we plan to no longer support the "VAT 100 report" in SSRS format.</span></span> <span data-ttu-id="82de8-134">"税申告モデル" の新しい "VAT 申告の Excel (UK)" 形式は、[MTD VAT 機能](../localizations/emea-gbr-mtd-vat-integration.md) に導入されました。</span><span class="sxs-lookup"><span data-stu-id="82de8-134">A new "VAT Declaration Excel (UK)" format under "Tax declaration model" was introduced in the [MTD VAT feature](../localizations/emea-gbr-mtd-vat-integration.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a><span data-ttu-id="82de8-135">Finance 10.0.15 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="82de8-135">Features removed or deprecated in the Finance 10.0.15 release</span></span>

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a><span data-ttu-id="82de8-136">Dynamics 365 における Internet Explorer 11 のサポートの非推奨</span><span class="sxs-lookup"><span data-stu-id="82de8-136">Internet Explorer 11 support for Dynamics 365 is deprecated</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="82de8-137">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="82de8-137">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="82de8-138">2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月以降、Internet Explorer 11 はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="82de8-138">Effective December 2020, Microsoft Internet Explorer 11 support for all Dynamics 365 products is deprecated, and Internet Explorer 11 won’t be supported after August 2021.</span></span><br><br><span data-ttu-id="82de8-139">これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。</span><span class="sxs-lookup"><span data-stu-id="82de8-139">This will impact customers who use Dynamics 365 products that are designed to be used through an Internet Explorer 11 interface.</span></span> <span data-ttu-id="82de8-140">2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="82de8-140">After August 2021, Internet Explorer 11 won't be supported for such Dynamics 365 products.</span></span> |
| <span data-ttu-id="82de8-141">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="82de8-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="82de8-142">Microsoft Edge に移行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="82de8-142">We recommend that customers transition to Microsoft Edge.</span></span>|
| <span data-ttu-id="82de8-143">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="82de8-143">**Product areas affected**</span></span>         | <span data-ttu-id="82de8-144">すべての Dynamics 365 製品</span><span class="sxs-lookup"><span data-stu-id="82de8-144">All Dynamics 365 products</span></span> |
| <span data-ttu-id="82de8-145">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="82de8-145">**Deployment option**</span></span>              | <span data-ttu-id="82de8-146">All</span><span class="sxs-lookup"><span data-stu-id="82de8-146">All</span></span>|
| <span data-ttu-id="82de8-147">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="82de8-147">**Status**</span></span>                         | <span data-ttu-id="82de8-148">非推奨。</span><span class="sxs-lookup"><span data-stu-id="82de8-148">Deprecated.</span></span> <span data-ttu-id="82de8-149">2021 年 8 月以降は、Internet Explorer 11 はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="82de8-149">Internet Explorer 11 won’t be supported after August 2021.</span></span>|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="82de8-150">Finance 10.0.12 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="82de8-150">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="82de8-151">ポーランド SSRS レポート: 仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014</span><span class="sxs-lookup"><span data-stu-id="82de8-151">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="82de8-152">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="82de8-152">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="82de8-153">法的に必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="82de8-153">Not legally required.</span></span>  |
| <span data-ttu-id="82de8-154">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="82de8-154">**Replaced by another feature?**</span></span>   | <span data-ttu-id="82de8-155">はい (VAT 申告を含む標準監査ファイル用の Excel 形式 - JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="82de8-155">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="82de8-156">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="82de8-156">**Product areas affected**</span></span>         | <span data-ttu-id="82de8-157">応募</span><span class="sxs-lookup"><span data-stu-id="82de8-157">Application</span></span> |
| <span data-ttu-id="82de8-158">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="82de8-158">**Deployment option**</span></span>              | <span data-ttu-id="82de8-159">すべて</span><span class="sxs-lookup"><span data-stu-id="82de8-159">All</span></span> |
| <span data-ttu-id="82de8-160">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="82de8-160">**Status**</span></span>                         | <span data-ttu-id="82de8-161">非推奨: 2021 年 7 月 1 日には、SSRS レポートのサポートはなくなります: **仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014**。</span><span class="sxs-lookup"><span data-stu-id="82de8-161">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="82de8-162">代わりに、VAT 申告を含む標準監査ファイルの Excel 形式 (JPK_VDEK) の例が導入されます。</span><span class="sxs-lookup"><span data-stu-id="82de8-162">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="82de8-163">Finance 10.0.11 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="82de8-163">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="82de8-164">ノルウェー標準主勘定</span><span class="sxs-lookup"><span data-stu-id="82de8-164">Norwegian Standard main accounts</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="82de8-165">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="82de8-165">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="82de8-166">再設計</span><span class="sxs-lookup"><span data-stu-id="82de8-166">Redesign</span></span>  |
| <span data-ttu-id="82de8-167">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="82de8-167">**Replaced by another feature?**</span></span>   | <span data-ttu-id="82de8-168">はい (ER 形式のアプリケーション固有パラメータに置き換えられます)</span><span class="sxs-lookup"><span data-stu-id="82de8-168">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="82de8-169">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="82de8-169">**Product areas affected**</span></span>         | <span data-ttu-id="82de8-170">応募</span><span class="sxs-lookup"><span data-stu-id="82de8-170">Application</span></span> |
| <span data-ttu-id="82de8-171">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="82de8-171">**Deployment option**</span></span>              | <span data-ttu-id="82de8-172">すべて</span><span class="sxs-lookup"><span data-stu-id="82de8-172">All</span></span> |
| <span data-ttu-id="82de8-173">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="82de8-173">**Status**</span></span>                         | <span data-ttu-id="82de8-174">非推奨: 2021 年 4 月 1 日までに、標準主勘定に関連する機能: 参照フィールド、関連テーブル、データ エンティティ はサポートされなくなる予定です。</span><span class="sxs-lookup"><span data-stu-id="82de8-174">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="82de8-175">Finance 10.0.7 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="82de8-175">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="82de8-176">ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります</span><span class="sxs-lookup"><span data-stu-id="82de8-176">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="82de8-177">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="82de8-177">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="82de8-178">勘定グループを選択する機能に変更されました。</span><span class="sxs-lookup"><span data-stu-id="82de8-178">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="82de8-179">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="82de8-179">**Replaced by another feature?**</span></span>   | <span data-ttu-id="82de8-180">有</span><span class="sxs-lookup"><span data-stu-id="82de8-180">Yes</span></span> |
| <span data-ttu-id="82de8-181">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="82de8-181">**Product areas affected**</span></span>         | <span data-ttu-id="82de8-182">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="82de8-182">Workflow</span></span> |
| <span data-ttu-id="82de8-183">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="82de8-183">**Deployment option**</span></span>              | <span data-ttu-id="82de8-184">すべて</span><span class="sxs-lookup"><span data-stu-id="82de8-184">All</span></span> |
| <span data-ttu-id="82de8-185">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="82de8-185">**Status**</span></span>                         | <span data-ttu-id="82de8-186">非推奨: 2020 年 12 月 1 日までに、勘定グループを選択せずに中国の伝票タイプ設定をサポートしなくなります。</span><span class="sxs-lookup"><span data-stu-id="82de8-186">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="82de8-187">新しいデザインの詳細については、[10.0.7 の新機能](whats-new-changed-10-0-7.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82de8-187">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="82de8-188">削除済みまたは非推奨の機能に関する以前の発表</span><span class="sxs-lookup"><span data-stu-id="82de8-188">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="82de8-189">以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82de8-189">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
