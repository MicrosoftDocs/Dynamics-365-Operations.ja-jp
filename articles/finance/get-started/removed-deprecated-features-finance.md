---
title: Dynamics 365 Finance の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。
author: roschlom
ms.date: 04/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: e0db5c35e58ab7a7cbf31642072d25ee5d8ba868
ms.sourcegitcommit: 04817103dc8e87a679d371575927284b8ce080b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/15/2021
ms.locfileid: "5898290"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="23f67-103">Dynamics 365 Finance の削除済みまたは推奨されない機能</span><span class="sxs-lookup"><span data-stu-id="23f67-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23f67-104">このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="23f67-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="23f67-105">*削除された* 機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="23f67-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="23f67-106">*削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="23f67-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="23f67-107">このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="23f67-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="23f67-108">Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](/dynamics/s-e/global/axtechrefrep_61)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23f67-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](/dynamics/s-e/global/axtechrefrep_61).</span></span> <span data-ttu-id="23f67-109">これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。</span><span class="sxs-lookup"><span data-stu-id="23f67-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a><span data-ttu-id="23f67-110">Finance 10.0.20 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="23f67-110">Features removed or deprecated in the Finance 10.0.20 release</span></span>

### <a name="rtir-query-invoice-data-request-hu-format-configuration"></a><span data-ttu-id="23f67-111">RTIR クエリ請求書データ要求 (HU) 形式の構成</span><span class="sxs-lookup"><span data-stu-id="23f67-111">RTIR Query Invoice Data Request (HU) format configuration</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="23f67-112">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="23f67-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="23f67-113">ハンガリーのオンライン請求システムとの相互運用の電子メッセージング処理から除外</span><span class="sxs-lookup"><span data-stu-id="23f67-113">Excluded from electronic messaging processing of interoperation with Hungarian online invoicing system</span></span> |
| <span data-ttu-id="23f67-114">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="23f67-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="23f67-115">なし</span><span class="sxs-lookup"><span data-stu-id="23f67-115">No</span></span> |
| <span data-ttu-id="23f67-116">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="23f67-116">**Product areas affected**</span></span>         | <span data-ttu-id="23f67-117">申請書</span><span class="sxs-lookup"><span data-stu-id="23f67-117">Application</span></span> |
| <span data-ttu-id="23f67-118">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="23f67-118">**Deployment option**</span></span>              | <span data-ttu-id="23f67-119">All</span><span class="sxs-lookup"><span data-stu-id="23f67-119">All</span></span> |
| <span data-ttu-id="23f67-120">**状態**</span><span class="sxs-lookup"><span data-stu-id="23f67-120">**Status**</span></span>                         | <span data-ttu-id="23f67-121">非推奨: 2022 年 4 月 15 日までに、「RTIR クエリ請求書データ要求 (HU)」形式の構成をサポートしなくなります。</span><span class="sxs-lookup"><span data-stu-id="23f67-121">Deprecated: By April 15, 2022, we plan to no longer support "RTIR Query Invoice Data Request (HU)" format configuration.</span></span> |


## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a><span data-ttu-id="23f67-122">Finance 10.0.17 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="23f67-122">Features removed or deprecated in the Finance 10.0.17 release</span></span>

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a><span data-ttu-id="23f67-123">電子申告コンフィギュレーションのストレージ オプションとしての LCS リポジトリ</span><span class="sxs-lookup"><span data-stu-id="23f67-123">LCS repository as a storage option for Electronic reporting configurations</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="23f67-124">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="23f67-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="23f67-125">新しい Regulatory Configuration Service (RCS) のグローバル リポジトリに置き換えられます</span><span class="sxs-lookup"><span data-stu-id="23f67-125">Replaced with the new Regulatory Configuration Service (RCS) Global repository</span></span> |
| <span data-ttu-id="23f67-126">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="23f67-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="23f67-127">あり</span><span class="sxs-lookup"><span data-stu-id="23f67-127">Yes</span></span> |
| <span data-ttu-id="23f67-128">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="23f67-128">**Product areas affected**</span></span>         | <span data-ttu-id="23f67-129">Dynamics 365 Finance、Supply Chain Management、Project Operations 製品</span><span class="sxs-lookup"><span data-stu-id="23f67-129">Dynamics 365 Finance, Supply Chain Management, and Project Operations products</span></span>|
| <span data-ttu-id="23f67-130">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="23f67-130">**Deployment option**</span></span>              | <span data-ttu-id="23f67-131">All</span><span class="sxs-lookup"><span data-stu-id="23f67-131">All</span></span> |
| <span data-ttu-id="23f67-132">**状態**</span><span class="sxs-lookup"><span data-stu-id="23f67-132">**Status**</span></span>                         | <span data-ttu-id="23f67-133">非推奨: 2022 年 4 月 1 日より、電子申告 (ER) コンフィギュレーションのストレージ オプションとして Microsoft Dynamics Lifecycle Services (LCS) リポジトリのサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="23f67-133">Deprecated: By April 01, 2022, we plan to no longer support the Microsoft Dynamics Lifecycle Services (LCS) repository as a storage option for Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="23f67-134">新しい Microsoft ER コンフィギュレーションは、グローバル リポジトリからのみダウンロードできるように公開されます。</span><span class="sxs-lookup"><span data-stu-id="23f67-134">New Microsoft ER configurations will be published for download exclusively from the Global repository.</span></span> <span data-ttu-id="23f67-135">グローバル リポジトリは、Dynamics 365 製品と RCS からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="23f67-135">The Global repository can be accessed from the Dynamics 365 products and RCS.</span></span> <span data-ttu-id="23f67-136">詳細については、[RCS から ER コンフィグレーションをインポートする](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23f67-136">For more information, see [Import ER configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a><span data-ttu-id="23f67-137">Finance 10.0.16 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="23f67-137">Features removed or deprecated in the Finance 10.0.16 release</span></span>

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a><span data-ttu-id="23f67-138">チェコ共和国向け「VAT申告 (CZ)」、および 「管理ステートメントのエクスポート ( CZ)」 電子レポート形式</span><span class="sxs-lookup"><span data-stu-id="23f67-138">"VAT declaration (CZ)" and "Control statement export (CZ)" Electronic reporting formats for Czech Republic</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="23f67-139">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="23f67-139">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="23f67-140">新しい形式に置き換えられます</span><span class="sxs-lookup"><span data-stu-id="23f67-140">Replaced with new formats</span></span> |
| <span data-ttu-id="23f67-141">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="23f67-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="23f67-142">あり</span><span class="sxs-lookup"><span data-stu-id="23f67-142">Yes</span></span> |
| <span data-ttu-id="23f67-143">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="23f67-143">**Product areas affected**</span></span>         | <span data-ttu-id="23f67-144">申請書</span><span class="sxs-lookup"><span data-stu-id="23f67-144">Application</span></span> |
| <span data-ttu-id="23f67-145">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="23f67-145">**Deployment option**</span></span>              | <span data-ttu-id="23f67-146">All</span><span class="sxs-lookup"><span data-stu-id="23f67-146">All</span></span> |
| <span data-ttu-id="23f67-147">**状態**</span><span class="sxs-lookup"><span data-stu-id="23f67-147">**Status**</span></span>                         | <span data-ttu-id="23f67-148">非推奨 : 2022年1月22日より、「VAT申告 (CZ)」、「管理ステートメントのエクスポート (CZ)」の電子申告の形式はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="23f67-148">Deprecated: By January 22, 2022, we plan to no longer support "VAT declaration (CZ)", "Control statement export (CZ)" Electronic reporting (ER) formats.</span></span> <span data-ttu-id="23f67-149">代わりに、新しい VAT申告 XML (CZ)、VAT申告 Excel (CZ)、VAT 管理ステートメント XML (CZ) 形式が「税申告」モデル配下で導入されます。</span><span class="sxs-lookup"><span data-stu-id="23f67-149">New VAT declaration XML (CZ), VAT declaration Excel (CZ), VAT control statement XML (CZ) formats are introduced instead under the "Tax declaration" model.</span></span> |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a><span data-ttu-id="23f67-150">"元帳トランザクションのエクスポート形式 (BE)" 電子レポート形式と、個別の "元帳トランザクション エクスポート (BE)" モデル (ベルギー)</span><span class="sxs-lookup"><span data-stu-id="23f67-150">"Ledger transaction export format (BE)" Electronic reporting format and respective "Ledger transaction export (BE)" model for Belgium</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="23f67-151">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="23f67-151">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="23f67-152">"標準監査ファイル (SAF)" モデルの下にある新しい ER 形式で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="23f67-152">Replaced with new ER format under "Standard Audit File (SAF-T)" model.</span></span>  |
| <span data-ttu-id="23f67-153">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="23f67-153">**Replaced by another feature?**</span></span>   | <span data-ttu-id="23f67-154">あり</span><span class="sxs-lookup"><span data-stu-id="23f67-154">Yes</span></span> |
| <span data-ttu-id="23f67-155">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="23f67-155">**Product areas affected**</span></span>         | <span data-ttu-id="23f67-156">申請書</span><span class="sxs-lookup"><span data-stu-id="23f67-156">Application</span></span> |
| <span data-ttu-id="23f67-157">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="23f67-157">**Deployment option**</span></span>              | <span data-ttu-id="23f67-158">All</span><span class="sxs-lookup"><span data-stu-id="23f67-158">All</span></span> |
| <span data-ttu-id="23f67-159">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="23f67-159">**Status**</span></span>                         | <span data-ttu-id="23f67-160">非推奨: 2021 年 12 月 1 日までに、"元帳トランザクションのエクスポート形式 (BE)" 電子レポート (ER) 形式と、個別の "元帳トランザクション エクスポート (BE)" モデルのサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="23f67-160">Deprecated: By December 1, 2021, we plan to no longer support the "Ledger transaction export format (BE)" Electronic reporting (ER) format and respective "Ledger transaction export (BE)" model.</span></span> <span data-ttu-id="23f67-161">"標準監査ファイル (SAF)" モデルの代わりに、新しい "一般会計のデータ エクスポート (BE)" 形式と "一般会計のデータ モデル マッピング" が導入されます。</span><span class="sxs-lookup"><span data-stu-id="23f67-161">A new "General ledger data export (BE)" format together with "General ledger data model mapping" are introduced instead under the "Standard Audit File (SAF-T)" model.</span></span> |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a><span data-ttu-id="23f67-162">SSRS 形式の英国用 "VAT 100" レポート</span><span class="sxs-lookup"><span data-stu-id="23f67-162">"VAT 100" report for the United Kingdom in SSRS format</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="23f67-163">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="23f67-163">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="23f67-164">"税申告モデル" で、新しい ER 形式である "VAT 申告 Excel (UK)" 形式と置き換えました。</span><span class="sxs-lookup"><span data-stu-id="23f67-164">Replaced with new ER format - "VAT Declaration Excel (UK)" format under "Tax declaration model".</span></span>  |
| <span data-ttu-id="23f67-165">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="23f67-165">**Replaced by another feature?**</span></span>   | <span data-ttu-id="23f67-166">あり</span><span class="sxs-lookup"><span data-stu-id="23f67-166">Yes</span></span> |
| <span data-ttu-id="23f67-167">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="23f67-167">**Product areas affected**</span></span>         | <span data-ttu-id="23f67-168">申請書</span><span class="sxs-lookup"><span data-stu-id="23f67-168">Application</span></span> |
| <span data-ttu-id="23f67-169">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="23f67-169">**Deployment option**</span></span>              | <span data-ttu-id="23f67-170">All</span><span class="sxs-lookup"><span data-stu-id="23f67-170">All</span></span> |
| <span data-ttu-id="23f67-171">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="23f67-171">**Status**</span></span>                         | <span data-ttu-id="23f67-172">非推奨: 2021 年 12 月 1 日までに、SSRS 形式の "VAT 100 レポート" のサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="23f67-172">Deprecated: By December 1, 2021, we plan to no longer support the "VAT 100 report" in SSRS format.</span></span> <span data-ttu-id="23f67-173">"税申告モデル" の新しい "VAT 申告の Excel (UK)" 形式は、[MTD VAT 機能](../localizations/emea-gbr-mtd-vat-integration.md) に導入されました。</span><span class="sxs-lookup"><span data-stu-id="23f67-173">A new "VAT Declaration Excel (UK)" format under "Tax declaration model" was introduced in the [MTD VAT feature](../localizations/emea-gbr-mtd-vat-integration.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a><span data-ttu-id="23f67-174">Finance 10.0.15 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="23f67-174">Features removed or deprecated in the Finance 10.0.15 release</span></span>

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a><span data-ttu-id="23f67-175">Dynamics 365 における Internet Explorer 11 のサポートの非推奨</span><span class="sxs-lookup"><span data-stu-id="23f67-175">Internet Explorer 11 support for Dynamics 365 is deprecated</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="23f67-176">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="23f67-176">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="23f67-177">2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月以降、Internet Explorer 11 はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="23f67-177">Effective December 2020, Microsoft Internet Explorer 11 support for all Dynamics 365 products is deprecated, and Internet Explorer 11 won’t be supported after August 2021.</span></span><br><br><span data-ttu-id="23f67-178">これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。</span><span class="sxs-lookup"><span data-stu-id="23f67-178">This will impact customers who use Dynamics 365 products that are designed to be used through an Internet Explorer 11 interface.</span></span> <span data-ttu-id="23f67-179">2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="23f67-179">After August 2021, Internet Explorer 11 won't be supported for such Dynamics 365 products.</span></span> |
| <span data-ttu-id="23f67-180">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="23f67-180">**Replaced by another feature?**</span></span>   | <span data-ttu-id="23f67-181">Microsoft Edge に移行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="23f67-181">We recommend that customers transition to Microsoft Edge.</span></span>|
| <span data-ttu-id="23f67-182">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="23f67-182">**Product areas affected**</span></span>         | <span data-ttu-id="23f67-183">すべての Dynamics 365 製品</span><span class="sxs-lookup"><span data-stu-id="23f67-183">All Dynamics 365 products</span></span> |
| <span data-ttu-id="23f67-184">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="23f67-184">**Deployment option**</span></span>              | <span data-ttu-id="23f67-185">All</span><span class="sxs-lookup"><span data-stu-id="23f67-185">All</span></span>|
| <span data-ttu-id="23f67-186">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="23f67-186">**Status**</span></span>                         | <span data-ttu-id="23f67-187">非推奨。</span><span class="sxs-lookup"><span data-stu-id="23f67-187">Deprecated.</span></span> <span data-ttu-id="23f67-188">2021 年 8 月以降は、Internet Explorer 11 はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="23f67-188">Internet Explorer 11 won’t be supported after August 2021.</span></span>|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="23f67-189">Finance 10.0.12 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="23f67-189">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="23f67-190">ポーランド SSRS レポート: 仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014</span><span class="sxs-lookup"><span data-stu-id="23f67-190">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="23f67-191">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="23f67-191">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="23f67-192">法的に必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="23f67-192">Not legally required.</span></span>  |
| <span data-ttu-id="23f67-193">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="23f67-193">**Replaced by another feature?**</span></span>   | <span data-ttu-id="23f67-194">はい (VAT 申告を含む標準監査ファイル用の Excel 形式 - JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="23f67-194">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="23f67-195">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="23f67-195">**Product areas affected**</span></span>         | <span data-ttu-id="23f67-196">応募</span><span class="sxs-lookup"><span data-stu-id="23f67-196">Application</span></span> |
| <span data-ttu-id="23f67-197">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="23f67-197">**Deployment option**</span></span>              | <span data-ttu-id="23f67-198">すべて</span><span class="sxs-lookup"><span data-stu-id="23f67-198">All</span></span> |
| <span data-ttu-id="23f67-199">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="23f67-199">**Status**</span></span>                         | <span data-ttu-id="23f67-200">非推奨: 2021 年 7 月 1 日には、SSRS レポートのサポートはなくなります: **仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014**。</span><span class="sxs-lookup"><span data-stu-id="23f67-200">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="23f67-201">代わりに、VAT 申告を含む標準監査ファイルの Excel 形式 (JPK_VDEK) の例が導入されます。</span><span class="sxs-lookup"><span data-stu-id="23f67-201">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="23f67-202">Finance 10.0.11 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="23f67-202">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="23f67-203">ノルウェー標準主勘定</span><span class="sxs-lookup"><span data-stu-id="23f67-203">Norwegian Standard main accounts</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="23f67-204">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="23f67-204">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="23f67-205">再設計</span><span class="sxs-lookup"><span data-stu-id="23f67-205">Redesign</span></span>  |
| <span data-ttu-id="23f67-206">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="23f67-206">**Replaced by another feature?**</span></span>   | <span data-ttu-id="23f67-207">はい (ER 形式のアプリケーション固有パラメータに置き換えられます)</span><span class="sxs-lookup"><span data-stu-id="23f67-207">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="23f67-208">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="23f67-208">**Product areas affected**</span></span>         | <span data-ttu-id="23f67-209">応募</span><span class="sxs-lookup"><span data-stu-id="23f67-209">Application</span></span> |
| <span data-ttu-id="23f67-210">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="23f67-210">**Deployment option**</span></span>              | <span data-ttu-id="23f67-211">すべて</span><span class="sxs-lookup"><span data-stu-id="23f67-211">All</span></span> |
| <span data-ttu-id="23f67-212">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="23f67-212">**Status**</span></span>                         | <span data-ttu-id="23f67-213">非推奨: 2021 年 4 月 1 日までに、標準主勘定に関連する機能: 参照フィールド、関連テーブル、データ エンティティ はサポートされなくなる予定です。</span><span class="sxs-lookup"><span data-stu-id="23f67-213">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="23f67-214">Finance 10.0.7 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="23f67-214">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="23f67-215">ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります</span><span class="sxs-lookup"><span data-stu-id="23f67-215">Workflow request change dialog box no longer includes user selection drop-down list</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="23f67-216">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="23f67-216">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="23f67-217">勘定グループを選択する機能に変更されました。</span><span class="sxs-lookup"><span data-stu-id="23f67-217">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="23f67-218">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="23f67-218">**Replaced by another feature?**</span></span>   | <span data-ttu-id="23f67-219">有</span><span class="sxs-lookup"><span data-stu-id="23f67-219">Yes</span></span> |
| <span data-ttu-id="23f67-220">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="23f67-220">**Product areas affected**</span></span>         | <span data-ttu-id="23f67-221">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="23f67-221">Workflow</span></span> |
| <span data-ttu-id="23f67-222">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="23f67-222">**Deployment option**</span></span>              | <span data-ttu-id="23f67-223">すべて</span><span class="sxs-lookup"><span data-stu-id="23f67-223">All</span></span> |
| <span data-ttu-id="23f67-224">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="23f67-224">**Status**</span></span>                         | <span data-ttu-id="23f67-225">非推奨: 2020 年 12 月 1 日までに、勘定グループを選択せずに中国の伝票タイプ設定をサポートしなくなります。</span><span class="sxs-lookup"><span data-stu-id="23f67-225">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="23f67-226">新しいデザインの詳細については、[10.0.7 の新機能](whats-new-changed-10-0-7.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23f67-226">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="23f67-227">削除済みまたは非推奨の機能に関する以前の発表</span><span class="sxs-lookup"><span data-stu-id="23f67-227">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="23f67-228">以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23f67-228">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
