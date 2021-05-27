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
ms.openlocfilehash: 8cacf2fbef8873288493f71b43d22dc186e6d18e
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980900"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="d64ac-103">Dynamics 365 Finance の削除済みまたは推奨されない機能</span><span class="sxs-lookup"><span data-stu-id="d64ac-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d64ac-104">このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d64ac-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="d64ac-105">*削除された* 機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="d64ac-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="d64ac-106">*削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d64ac-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="d64ac-107">このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d64ac-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="d64ac-108">Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](/dynamics/s-e/global/axtechrefrep_61)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d64ac-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](/dynamics/s-e/global/axtechrefrep_61).</span></span> <span data-ttu-id="d64ac-109">これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。</span><span class="sxs-lookup"><span data-stu-id="d64ac-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a><span data-ttu-id="d64ac-110">Finance 10.0.20 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="d64ac-110">Features removed or deprecated in the Finance 10.0.20 release</span></span>

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a><span data-ttu-id="d64ac-111">"RTIR クエリ請求書データ要求 (HU)" 電子レポート (ER) 形式のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d64ac-111">"RTIR Query Invoice Data Request (HU)" Electronic reporting (ER) format configuration</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="d64ac-112">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="d64ac-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d64ac-113">ハンガリーのオンライン請求システムとの相互運用の電子メッセージング処理から除外</span><span class="sxs-lookup"><span data-stu-id="d64ac-113">Excluded from electronic messaging processing of interoperation with Hungarian online invoicing system</span></span> |
| <span data-ttu-id="d64ac-114">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="d64ac-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d64ac-115">なし</span><span class="sxs-lookup"><span data-stu-id="d64ac-115">No</span></span> |
| <span data-ttu-id="d64ac-116">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="d64ac-116">**Product areas affected**</span></span>         | <span data-ttu-id="d64ac-117">申請書</span><span class="sxs-lookup"><span data-stu-id="d64ac-117">Application</span></span> |
| <span data-ttu-id="d64ac-118">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="d64ac-118">**Deployment option**</span></span>              | <span data-ttu-id="d64ac-119">All</span><span class="sxs-lookup"><span data-stu-id="d64ac-119">All</span></span> |
| <span data-ttu-id="d64ac-120">**状態**</span><span class="sxs-lookup"><span data-stu-id="d64ac-120">**Status**</span></span>                         | <span data-ttu-id="d64ac-121">非推奨: 2022 年 4 月 15 日までに、「RTIR クエリ請求書データ要求 (HU)」形式の構成をサポートしなくなります。</span><span class="sxs-lookup"><span data-stu-id="d64ac-121">Deprecated: By April 15, 2022, we plan to no longer support "RTIR Query Invoice Data Request (HU)" format configuration.</span></span> |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a><span data-ttu-id="d64ac-122">"ドイツ監査ファイル出力" 形式によるフランスの "フランス監査ファイル" 電子レポート (ER) 形式</span><span class="sxs-lookup"><span data-stu-id="d64ac-122">"French FEC audit file" Electronic reporting (ER) format for France under "German audit file output" format</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="d64ac-123">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="d64ac-123">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d64ac-124">新しい "FEC 監査ファイル (FR)" 形式に置き換えられた</span><span class="sxs-lookup"><span data-stu-id="d64ac-124">Replaced with new "FEC audit file (FR)" format</span></span> |
| <span data-ttu-id="d64ac-125">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="d64ac-125">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d64ac-126">あり</span><span class="sxs-lookup"><span data-stu-id="d64ac-126">Yes</span></span> |
| <span data-ttu-id="d64ac-127">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="d64ac-127">**Product areas affected**</span></span>         | <span data-ttu-id="d64ac-128">申請書</span><span class="sxs-lookup"><span data-stu-id="d64ac-128">Application</span></span> |
| <span data-ttu-id="d64ac-129">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="d64ac-129">**Deployment option**</span></span>              | <span data-ttu-id="d64ac-130">All</span><span class="sxs-lookup"><span data-stu-id="d64ac-130">All</span></span> |
| <span data-ttu-id="d64ac-131">**状態**</span><span class="sxs-lookup"><span data-stu-id="d64ac-131">**Status**</span></span>                         | <span data-ttu-id="d64ac-132">非推奨: 2022年5月1日より、"ドイツ監査ファイル出力" 形式による、フランスの "フランス監査ファイル" 電子レポート (ER) 形式はサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="d64ac-132">Deprecated: by May 1, 2022, we plan to no longer support "French FEC audit file" Electronic reporting (ER) format for France under "German audit file output" format.</span></span> <span data-ttu-id="d64ac-133">新しい FEC 監査ファイル (FR) 形式が "データ エクスポート モデル" の下に導入されます。</span><span class="sxs-lookup"><span data-stu-id="d64ac-133">New FEC audit file (FR) format is introduced instead under the "Data export model".</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a><span data-ttu-id="d64ac-134">Finance 10.0.17 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="d64ac-134">Features removed or deprecated in the Finance 10.0.17 release</span></span>

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a><span data-ttu-id="d64ac-135">電子申告コンフィギュレーションのストレージ オプションとしての LCS リポジトリ</span><span class="sxs-lookup"><span data-stu-id="d64ac-135">LCS repository as a storage option for Electronic reporting configurations</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="d64ac-136">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="d64ac-136">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d64ac-137">新しい Regulatory Configuration Service (RCS) のグローバル リポジトリに置き換えられます</span><span class="sxs-lookup"><span data-stu-id="d64ac-137">Replaced with the new Regulatory Configuration Service (RCS) Global repository</span></span> |
| <span data-ttu-id="d64ac-138">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="d64ac-138">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d64ac-139">あり</span><span class="sxs-lookup"><span data-stu-id="d64ac-139">Yes</span></span> |
| <span data-ttu-id="d64ac-140">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="d64ac-140">**Product areas affected**</span></span>         | <span data-ttu-id="d64ac-141">Dynamics 365 Finance、Supply Chain Management、Project Operations 製品</span><span class="sxs-lookup"><span data-stu-id="d64ac-141">Dynamics 365 Finance, Supply Chain Management, and Project Operations products</span></span>|
| <span data-ttu-id="d64ac-142">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="d64ac-142">**Deployment option**</span></span>              | <span data-ttu-id="d64ac-143">All</span><span class="sxs-lookup"><span data-stu-id="d64ac-143">All</span></span> |
| <span data-ttu-id="d64ac-144">**状態**</span><span class="sxs-lookup"><span data-stu-id="d64ac-144">**Status**</span></span>                         | <span data-ttu-id="d64ac-145">非推奨: 2022 年 4 月 1 日より、電子申告 (ER) コンフィギュレーションのストレージ オプションとして Microsoft Dynamics Lifecycle Services (LCS) リポジトリのサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="d64ac-145">Deprecated: By April 01, 2022, we plan to no longer support the Microsoft Dynamics Lifecycle Services (LCS) repository as a storage option for Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="d64ac-146">新しい Microsoft ER コンフィギュレーションは、グローバル リポジトリからのみダウンロードできるように公開されます。</span><span class="sxs-lookup"><span data-stu-id="d64ac-146">New Microsoft ER configurations will be published for download exclusively from the Global repository.</span></span> <span data-ttu-id="d64ac-147">グローバル リポジトリは、Dynamics 365 製品と RCS からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d64ac-147">The Global repository can be accessed from the Dynamics 365 products and RCS.</span></span> <span data-ttu-id="d64ac-148">詳細については、[RCS から ER コンフィグレーションをインポートする](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d64ac-148">For more information, see [Import ER configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a><span data-ttu-id="d64ac-149">Finance 10.0.16 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="d64ac-149">Features removed or deprecated in the Finance 10.0.16 release</span></span>

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a><span data-ttu-id="d64ac-150">チェコ共和国向け「VAT申告 (CZ)」、および 「管理ステートメントのエクスポート ( CZ)」 電子レポート形式</span><span class="sxs-lookup"><span data-stu-id="d64ac-150">"VAT declaration (CZ)" and "Control statement export (CZ)" Electronic reporting formats for Czech Republic</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="d64ac-151">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="d64ac-151">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d64ac-152">新しい形式に置き換えられます</span><span class="sxs-lookup"><span data-stu-id="d64ac-152">Replaced with new formats</span></span> |
| <span data-ttu-id="d64ac-153">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="d64ac-153">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d64ac-154">あり</span><span class="sxs-lookup"><span data-stu-id="d64ac-154">Yes</span></span> |
| <span data-ttu-id="d64ac-155">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="d64ac-155">**Product areas affected**</span></span>         | <span data-ttu-id="d64ac-156">申請書</span><span class="sxs-lookup"><span data-stu-id="d64ac-156">Application</span></span> |
| <span data-ttu-id="d64ac-157">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="d64ac-157">**Deployment option**</span></span>              | <span data-ttu-id="d64ac-158">All</span><span class="sxs-lookup"><span data-stu-id="d64ac-158">All</span></span> |
| <span data-ttu-id="d64ac-159">**状態**</span><span class="sxs-lookup"><span data-stu-id="d64ac-159">**Status**</span></span>                         | <span data-ttu-id="d64ac-160">非推奨 : 2022年1月22日より、「VAT申告 (CZ)」、「管理ステートメントのエクスポート (CZ)」の電子申告の形式はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="d64ac-160">Deprecated: By January 22, 2022, we plan to no longer support "VAT declaration (CZ)", "Control statement export (CZ)" Electronic reporting (ER) formats.</span></span> <span data-ttu-id="d64ac-161">代わりに、新しい VAT申告 XML (CZ)、VAT申告 Excel (CZ)、VAT 管理ステートメント XML (CZ) 形式が「税申告」モデル配下で導入されます。</span><span class="sxs-lookup"><span data-stu-id="d64ac-161">New VAT declaration XML (CZ), VAT declaration Excel (CZ), VAT control statement XML (CZ) formats are introduced instead under the "Tax declaration" model.</span></span> |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a><span data-ttu-id="d64ac-162">"元帳トランザクションのエクスポート形式 (BE)" 電子レポート形式と、個別の "元帳トランザクション エクスポート (BE)" モデル (ベルギー)</span><span class="sxs-lookup"><span data-stu-id="d64ac-162">"Ledger transaction export format (BE)" Electronic reporting format and respective "Ledger transaction export (BE)" model for Belgium</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="d64ac-163">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="d64ac-163">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d64ac-164">"標準監査ファイル (SAF)" モデルの下にある新しい ER 形式で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="d64ac-164">Replaced with new ER format under "Standard Audit File (SAF-T)" model.</span></span>  |
| <span data-ttu-id="d64ac-165">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="d64ac-165">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d64ac-166">あり</span><span class="sxs-lookup"><span data-stu-id="d64ac-166">Yes</span></span> |
| <span data-ttu-id="d64ac-167">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="d64ac-167">**Product areas affected**</span></span>         | <span data-ttu-id="d64ac-168">申請書</span><span class="sxs-lookup"><span data-stu-id="d64ac-168">Application</span></span> |
| <span data-ttu-id="d64ac-169">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="d64ac-169">**Deployment option**</span></span>              | <span data-ttu-id="d64ac-170">All</span><span class="sxs-lookup"><span data-stu-id="d64ac-170">All</span></span> |
| <span data-ttu-id="d64ac-171">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="d64ac-171">**Status**</span></span>                         | <span data-ttu-id="d64ac-172">非推奨: 2021 年 12 月 1 日までに、"元帳トランザクションのエクスポート形式 (BE)" 電子レポート (ER) 形式と、個別の "元帳トランザクション エクスポート (BE)" モデルのサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="d64ac-172">Deprecated: By December 1, 2021, we plan to no longer support the "Ledger transaction export format (BE)" Electronic reporting (ER) format and respective "Ledger transaction export (BE)" model.</span></span> <span data-ttu-id="d64ac-173">"標準監査ファイル (SAF)" モデルの代わりに、新しい "一般会計のデータ エクスポート (BE)" 形式と "一般会計のデータ モデル マッピング" が導入されます。</span><span class="sxs-lookup"><span data-stu-id="d64ac-173">A new "General ledger data export (BE)" format together with "General ledger data model mapping" are introduced instead under the "Standard Audit File (SAF-T)" model.</span></span> |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a><span data-ttu-id="d64ac-174">SSRS 形式の英国用 "VAT 100" レポート</span><span class="sxs-lookup"><span data-stu-id="d64ac-174">"VAT 100" report for the United Kingdom in SSRS format</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="d64ac-175">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="d64ac-175">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d64ac-176">"税申告モデル" で、新しい ER 形式である "VAT 申告 Excel (UK)" 形式と置き換えました。</span><span class="sxs-lookup"><span data-stu-id="d64ac-176">Replaced with new ER format - "VAT Declaration Excel (UK)" format under "Tax declaration model".</span></span>  |
| <span data-ttu-id="d64ac-177">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="d64ac-177">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d64ac-178">あり</span><span class="sxs-lookup"><span data-stu-id="d64ac-178">Yes</span></span> |
| <span data-ttu-id="d64ac-179">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="d64ac-179">**Product areas affected**</span></span>         | <span data-ttu-id="d64ac-180">申請書</span><span class="sxs-lookup"><span data-stu-id="d64ac-180">Application</span></span> |
| <span data-ttu-id="d64ac-181">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="d64ac-181">**Deployment option**</span></span>              | <span data-ttu-id="d64ac-182">All</span><span class="sxs-lookup"><span data-stu-id="d64ac-182">All</span></span> |
| <span data-ttu-id="d64ac-183">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="d64ac-183">**Status**</span></span>                         | <span data-ttu-id="d64ac-184">非推奨: 2021 年 12 月 1 日までに、SSRS 形式の "VAT 100 レポート" のサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="d64ac-184">Deprecated: By December 1, 2021, we plan to no longer support the "VAT 100 report" in SSRS format.</span></span> <span data-ttu-id="d64ac-185">"税申告モデル" の新しい "VAT 申告の Excel (UK)" 形式は、[MTD VAT 機能](../localizations/emea-gbr-mtd-vat-integration.md) に導入されました。</span><span class="sxs-lookup"><span data-stu-id="d64ac-185">A new "VAT Declaration Excel (UK)" format under "Tax declaration model" was introduced in the [MTD VAT feature](../localizations/emea-gbr-mtd-vat-integration.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a><span data-ttu-id="d64ac-186">Finance 10.0.15 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="d64ac-186">Features removed or deprecated in the Finance 10.0.15 release</span></span>

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a><span data-ttu-id="d64ac-187">Dynamics 365 における Internet Explorer 11 のサポートの非推奨</span><span class="sxs-lookup"><span data-stu-id="d64ac-187">Internet Explorer 11 support for Dynamics 365 is deprecated</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="d64ac-188">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="d64ac-188">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d64ac-189">2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月以降、Internet Explorer 11 はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="d64ac-189">Effective December 2020, Microsoft Internet Explorer 11 support for all Dynamics 365 products is deprecated, and Internet Explorer 11 won’t be supported after August 2021.</span></span><br><br><span data-ttu-id="d64ac-190">これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。</span><span class="sxs-lookup"><span data-stu-id="d64ac-190">This will impact customers who use Dynamics 365 products that are designed to be used through an Internet Explorer 11 interface.</span></span> <span data-ttu-id="d64ac-191">2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="d64ac-191">After August 2021, Internet Explorer 11 won't be supported for such Dynamics 365 products.</span></span> |
| <span data-ttu-id="d64ac-192">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="d64ac-192">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d64ac-193">Microsoft Edge に移行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d64ac-193">We recommend that customers transition to Microsoft Edge.</span></span>|
| <span data-ttu-id="d64ac-194">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="d64ac-194">**Product areas affected**</span></span>         | <span data-ttu-id="d64ac-195">すべての Dynamics 365 製品</span><span class="sxs-lookup"><span data-stu-id="d64ac-195">All Dynamics 365 products</span></span> |
| <span data-ttu-id="d64ac-196">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="d64ac-196">**Deployment option**</span></span>              | <span data-ttu-id="d64ac-197">All</span><span class="sxs-lookup"><span data-stu-id="d64ac-197">All</span></span>|
| <span data-ttu-id="d64ac-198">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="d64ac-198">**Status**</span></span>                         | <span data-ttu-id="d64ac-199">非推奨。</span><span class="sxs-lookup"><span data-stu-id="d64ac-199">Deprecated.</span></span> <span data-ttu-id="d64ac-200">2021 年 8 月以降は、Internet Explorer 11 はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="d64ac-200">Internet Explorer 11 won’t be supported after August 2021.</span></span>|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="d64ac-201">Finance 10.0.12 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="d64ac-201">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="d64ac-202">廃止されていない: ポーランド SSRS レポート: 仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014</span><span class="sxs-lookup"><span data-stu-id="d64ac-202">Not deprecated: Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="d64ac-203">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="d64ac-203">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d64ac-204">法的に必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="d64ac-204">Not legally required.</span></span>  |
| <span data-ttu-id="d64ac-205">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="d64ac-205">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d64ac-206">はい (VAT 申告を含む標準監査ファイル用の Excel 形式 - JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="d64ac-206">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="d64ac-207">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="d64ac-207">**Product areas affected**</span></span>         | <span data-ttu-id="d64ac-208">申請書</span><span class="sxs-lookup"><span data-stu-id="d64ac-208">Application</span></span> |
| <span data-ttu-id="d64ac-209">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="d64ac-209">**Deployment option**</span></span>              | <span data-ttu-id="d64ac-210">All</span><span class="sxs-lookup"><span data-stu-id="d64ac-210">All</span></span> |
| <span data-ttu-id="d64ac-211">**状態**</span><span class="sxs-lookup"><span data-stu-id="d64ac-211">**Status**</span></span>                         | <span data-ttu-id="d64ac-212">非推奨ではない: 2021 年 4 月 27 日現在、SSRS レポートのサポートを継続する予定です: **仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014**。</span><span class="sxs-lookup"><span data-stu-id="d64ac-212">Not deprecated: As of April 27, 2021, we plan to continue to support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="d64ac-213">VAT 申告を含む標準監査ファイルの Excel 形式 (JPK_VDEK) の例も導入されました。</span><span class="sxs-lookup"><span data-stu-id="d64ac-213">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) has also been introduced.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="d64ac-214">Finance 10.0.11 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="d64ac-214">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="d64ac-215">ノルウェー標準主勘定</span><span class="sxs-lookup"><span data-stu-id="d64ac-215">Norwegian Standard main accounts</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="d64ac-216">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="d64ac-216">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d64ac-217">再設計</span><span class="sxs-lookup"><span data-stu-id="d64ac-217">Redesign</span></span>  |
| <span data-ttu-id="d64ac-218">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="d64ac-218">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d64ac-219">はい (ER 形式のアプリケーション固有パラメータに置き換えられます)</span><span class="sxs-lookup"><span data-stu-id="d64ac-219">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="d64ac-220">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="d64ac-220">**Product areas affected**</span></span>         | <span data-ttu-id="d64ac-221">応募</span><span class="sxs-lookup"><span data-stu-id="d64ac-221">Application</span></span> |
| <span data-ttu-id="d64ac-222">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="d64ac-222">**Deployment option**</span></span>              | <span data-ttu-id="d64ac-223">すべて</span><span class="sxs-lookup"><span data-stu-id="d64ac-223">All</span></span> |
| <span data-ttu-id="d64ac-224">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="d64ac-224">**Status**</span></span>                         | <span data-ttu-id="d64ac-225">非推奨: 2021 年 4 月 1 日までに、標準主勘定に関連する機能: 参照フィールド、関連テーブル、データ エンティティ はサポートされなくなる予定です。</span><span class="sxs-lookup"><span data-stu-id="d64ac-225">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="d64ac-226">Finance 10.0.7 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="d64ac-226">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="d64ac-227">ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります</span><span class="sxs-lookup"><span data-stu-id="d64ac-227">Workflow request change dialog box no longer includes user selection drop-down list</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="d64ac-228">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="d64ac-228">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="d64ac-229">勘定グループを選択する機能に変更されました。</span><span class="sxs-lookup"><span data-stu-id="d64ac-229">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="d64ac-230">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="d64ac-230">**Replaced by another feature?**</span></span>   | <span data-ttu-id="d64ac-231">有</span><span class="sxs-lookup"><span data-stu-id="d64ac-231">Yes</span></span> |
| <span data-ttu-id="d64ac-232">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="d64ac-232">**Product areas affected**</span></span>         | <span data-ttu-id="d64ac-233">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="d64ac-233">Workflow</span></span> |
| <span data-ttu-id="d64ac-234">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="d64ac-234">**Deployment option**</span></span>              | <span data-ttu-id="d64ac-235">すべて</span><span class="sxs-lookup"><span data-stu-id="d64ac-235">All</span></span> |
| <span data-ttu-id="d64ac-236">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="d64ac-236">**Status**</span></span>                         | <span data-ttu-id="d64ac-237">非推奨: 2020 年 12 月 1 日までに、勘定グループを選択せずに中国の伝票タイプ設定をサポートしなくなります。</span><span class="sxs-lookup"><span data-stu-id="d64ac-237">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="d64ac-238">新しいデザインの詳細については、[10.0.7 の新機能](whats-new-changed-10-0-7.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d64ac-238">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="d64ac-239">削除済みまたは非推奨の機能に関する以前の発表</span><span class="sxs-lookup"><span data-stu-id="d64ac-239">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="d64ac-240">以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d64ac-240">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
