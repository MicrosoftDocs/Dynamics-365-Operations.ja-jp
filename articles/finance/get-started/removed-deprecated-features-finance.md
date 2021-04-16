---
title: Dynamics 365 Finance の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。
author: roschlom
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 5a8f5dbc52eab78697de0d3a48d8cceb42c36540
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836916"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="0007a-103">Dynamics 365 Finance の削除済みまたは推奨されない機能</span><span class="sxs-lookup"><span data-stu-id="0007a-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0007a-104">このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="0007a-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="0007a-105">*削除された* 機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="0007a-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="0007a-106">*削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0007a-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="0007a-107">このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0007a-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="0007a-108">Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://docs.microsoft.com/dynamics/s-e/global/axtechrefrep_61)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0007a-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://docs.microsoft.com/dynamics/s-e/global/axtechrefrep_61).</span></span> <span data-ttu-id="0007a-109">これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。</span><span class="sxs-lookup"><span data-stu-id="0007a-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a><span data-ttu-id="0007a-110">Finance 10.0.17 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="0007a-110">Features removed or deprecated in the Finance 10.0.17 release</span></span>

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a><span data-ttu-id="0007a-111">電子申告コンフィギュレーションのストレージ オプションとしての LCS リポジトリ</span><span class="sxs-lookup"><span data-stu-id="0007a-111">LCS repository as a storage option for Electronic reporting configurations</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="0007a-112">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="0007a-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="0007a-113">新しい Regulatory Configuration Service (RCS) のグローバル リポジトリに置き換えられます</span><span class="sxs-lookup"><span data-stu-id="0007a-113">Replaced with the new Regulatory Configuration Service (RCS) Global repository</span></span> |
| <span data-ttu-id="0007a-114">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="0007a-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="0007a-115">あり</span><span class="sxs-lookup"><span data-stu-id="0007a-115">Yes</span></span> |
| <span data-ttu-id="0007a-116">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="0007a-116">**Product areas affected**</span></span>         | <span data-ttu-id="0007a-117">Dynamics 365 Finance、Supply Chain Management、Project Operations 製品</span><span class="sxs-lookup"><span data-stu-id="0007a-117">Dynamics 365 Finance, Supply Chain Management, and Project Operations products</span></span>|
| <span data-ttu-id="0007a-118">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="0007a-118">**Deployment option**</span></span>              | <span data-ttu-id="0007a-119">All</span><span class="sxs-lookup"><span data-stu-id="0007a-119">All</span></span> |
| <span data-ttu-id="0007a-120">**状態**</span><span class="sxs-lookup"><span data-stu-id="0007a-120">**Status**</span></span>                         | <span data-ttu-id="0007a-121">非推奨: 2022 年 4 月 1 日より、電子申告 (ER) コンフィギュレーションのストレージ オプションとして Microsoft Dynamics Lifecycle Services (LCS) リポジトリのサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="0007a-121">Deprecated: By April 01, 2022, we plan to no longer support the Microsoft Dynamics Lifecycle Services (LCS) repository as a storage option for Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="0007a-122">新しい Microsoft ER コンフィギュレーションは、グローバル リポジトリからのみダウンロードできるように公開されます。</span><span class="sxs-lookup"><span data-stu-id="0007a-122">New Microsoft ER configurations will be published for download exclusively from the Global repository.</span></span> <span data-ttu-id="0007a-123">グローバル リポジトリは、Dynamics 365 製品と RCS からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="0007a-123">The Global repository can be accessed from the Dynamics 365 products and RCS.</span></span> <span data-ttu-id="0007a-124">詳細については、[RCS から ER コンフィグレーションをインポートする](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0007a-124">For more information, see [Import ER configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a><span data-ttu-id="0007a-125">Finance 10.0.16 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="0007a-125">Features removed or deprecated in the Finance 10.0.16 release</span></span>

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a><span data-ttu-id="0007a-126">チェコ共和国向け「VAT申告 (CZ)」、および 「管理ステートメントのエクスポート ( CZ)」 電子レポート形式</span><span class="sxs-lookup"><span data-stu-id="0007a-126">"VAT declaration (CZ)" and "Control statement export (CZ)" Electronic reporting formats for Czech Republic</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="0007a-127">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="0007a-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="0007a-128">新しい形式に置き換えられます</span><span class="sxs-lookup"><span data-stu-id="0007a-128">Replaced with new formats</span></span> |
| <span data-ttu-id="0007a-129">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="0007a-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="0007a-130">あり</span><span class="sxs-lookup"><span data-stu-id="0007a-130">Yes</span></span> |
| <span data-ttu-id="0007a-131">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="0007a-131">**Product areas affected**</span></span>         | <span data-ttu-id="0007a-132">申請書</span><span class="sxs-lookup"><span data-stu-id="0007a-132">Application</span></span> |
| <span data-ttu-id="0007a-133">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="0007a-133">**Deployment option**</span></span>              | <span data-ttu-id="0007a-134">All</span><span class="sxs-lookup"><span data-stu-id="0007a-134">All</span></span> |
| <span data-ttu-id="0007a-135">**状態**</span><span class="sxs-lookup"><span data-stu-id="0007a-135">**Status**</span></span>                         | <span data-ttu-id="0007a-136">非推奨 : 2022年1月22日より、「VAT申告 (CZ)」、「管理ステートメントのエクスポート (CZ)」の電子申告の形式はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="0007a-136">Deprecated: By January 22, 2022, we plan to no longer support "VAT declaration (CZ)", "Control statement export (CZ)" Electronic reporting (ER) formats.</span></span> <span data-ttu-id="0007a-137">代わりに、新しい VAT申告 XML (CZ)、VAT申告 Excel (CZ)、VAT 管理ステートメント XML (CZ) 形式が「税申告」モデル配下で導入されます。</span><span class="sxs-lookup"><span data-stu-id="0007a-137">New VAT declaration XML (CZ), VAT declaration Excel (CZ), VAT control statement XML (CZ) formats are introduced instead under the "Tax declaration" model.</span></span> |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a><span data-ttu-id="0007a-138">"元帳トランザクションのエクスポート形式 (BE)" 電子レポート形式と、個別の "元帳トランザクション エクスポート (BE)" モデル (ベルギー)</span><span class="sxs-lookup"><span data-stu-id="0007a-138">"Ledger transaction export format (BE)" Electronic reporting format and respective "Ledger transaction export (BE)" model for Belgium</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="0007a-139">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="0007a-139">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="0007a-140">"標準監査ファイル (SAF)" モデルの下にある新しい ER 形式で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="0007a-140">Replaced with new ER format under "Standard Audit File (SAF-T)" model.</span></span>  |
| <span data-ttu-id="0007a-141">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="0007a-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="0007a-142">あり</span><span class="sxs-lookup"><span data-stu-id="0007a-142">Yes</span></span> |
| <span data-ttu-id="0007a-143">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="0007a-143">**Product areas affected**</span></span>         | <span data-ttu-id="0007a-144">申請書</span><span class="sxs-lookup"><span data-stu-id="0007a-144">Application</span></span> |
| <span data-ttu-id="0007a-145">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="0007a-145">**Deployment option**</span></span>              | <span data-ttu-id="0007a-146">All</span><span class="sxs-lookup"><span data-stu-id="0007a-146">All</span></span> |
| <span data-ttu-id="0007a-147">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="0007a-147">**Status**</span></span>                         | <span data-ttu-id="0007a-148">非推奨: 2021 年 12 月 1 日までに、"元帳トランザクションのエクスポート形式 (BE)" 電子レポート (ER) 形式と、個別の "元帳トランザクション エクスポート (BE)" モデルのサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="0007a-148">Deprecated: By December 1, 2021, we plan to no longer support the "Ledger transaction export format (BE)" Electronic reporting (ER) format and respective "Ledger transaction export (BE)" model.</span></span> <span data-ttu-id="0007a-149">"標準監査ファイル (SAF)" モデルの代わりに、新しい "一般会計のデータ エクスポート (BE)" 形式と "一般会計のデータ モデル マッピング" が導入されます。</span><span class="sxs-lookup"><span data-stu-id="0007a-149">A new "General ledger data export (BE)" format together with "General ledger data model mapping" are introduced instead under the "Standard Audit File (SAF-T)" model.</span></span> |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a><span data-ttu-id="0007a-150">SSRS 形式の英国用 "VAT 100" レポート</span><span class="sxs-lookup"><span data-stu-id="0007a-150">"VAT 100" report for the United Kingdom in SSRS format</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="0007a-151">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="0007a-151">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="0007a-152">"税申告モデル" で、新しい ER 形式である "VAT 申告 Excel (UK)" 形式と置き換えました。</span><span class="sxs-lookup"><span data-stu-id="0007a-152">Replaced with new ER format - "VAT Declaration Excel (UK)" format under "Tax declaration model".</span></span>  |
| <span data-ttu-id="0007a-153">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="0007a-153">**Replaced by another feature?**</span></span>   | <span data-ttu-id="0007a-154">あり</span><span class="sxs-lookup"><span data-stu-id="0007a-154">Yes</span></span> |
| <span data-ttu-id="0007a-155">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="0007a-155">**Product areas affected**</span></span>         | <span data-ttu-id="0007a-156">申請書</span><span class="sxs-lookup"><span data-stu-id="0007a-156">Application</span></span> |
| <span data-ttu-id="0007a-157">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="0007a-157">**Deployment option**</span></span>              | <span data-ttu-id="0007a-158">All</span><span class="sxs-lookup"><span data-stu-id="0007a-158">All</span></span> |
| <span data-ttu-id="0007a-159">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="0007a-159">**Status**</span></span>                         | <span data-ttu-id="0007a-160">非推奨: 2021 年 12 月 1 日までに、SSRS 形式の "VAT 100 レポート" のサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="0007a-160">Deprecated: By December 1, 2021, we plan to no longer support the "VAT 100 report" in SSRS format.</span></span> <span data-ttu-id="0007a-161">"税申告モデル" の新しい "VAT 申告の Excel (UK)" 形式は、[MTD VAT 機能](../localizations/emea-gbr-mtd-vat-integration.md) に導入されました。</span><span class="sxs-lookup"><span data-stu-id="0007a-161">A new "VAT Declaration Excel (UK)" format under "Tax declaration model" was introduced in the [MTD VAT feature](../localizations/emea-gbr-mtd-vat-integration.md).</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a><span data-ttu-id="0007a-162">Finance 10.0.15 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="0007a-162">Features removed or deprecated in the Finance 10.0.15 release</span></span>

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a><span data-ttu-id="0007a-163">Dynamics 365 における Internet Explorer 11 のサポートの非推奨</span><span class="sxs-lookup"><span data-stu-id="0007a-163">Internet Explorer 11 support for Dynamics 365 is deprecated</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="0007a-164">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="0007a-164">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="0007a-165">2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月以降、Internet Explorer 11 はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="0007a-165">Effective December 2020, Microsoft Internet Explorer 11 support for all Dynamics 365 products is deprecated, and Internet Explorer 11 won’t be supported after August 2021.</span></span><br><br><span data-ttu-id="0007a-166">これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。</span><span class="sxs-lookup"><span data-stu-id="0007a-166">This will impact customers who use Dynamics 365 products that are designed to be used through an Internet Explorer 11 interface.</span></span> <span data-ttu-id="0007a-167">2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="0007a-167">After August 2021, Internet Explorer 11 won't be supported for such Dynamics 365 products.</span></span> |
| <span data-ttu-id="0007a-168">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="0007a-168">**Replaced by another feature?**</span></span>   | <span data-ttu-id="0007a-169">Microsoft Edge に移行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0007a-169">We recommend that customers transition to Microsoft Edge.</span></span>|
| <span data-ttu-id="0007a-170">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="0007a-170">**Product areas affected**</span></span>         | <span data-ttu-id="0007a-171">すべての Dynamics 365 製品</span><span class="sxs-lookup"><span data-stu-id="0007a-171">All Dynamics 365 products</span></span> |
| <span data-ttu-id="0007a-172">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="0007a-172">**Deployment option**</span></span>              | <span data-ttu-id="0007a-173">All</span><span class="sxs-lookup"><span data-stu-id="0007a-173">All</span></span>|
| <span data-ttu-id="0007a-174">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="0007a-174">**Status**</span></span>                         | <span data-ttu-id="0007a-175">非推奨。</span><span class="sxs-lookup"><span data-stu-id="0007a-175">Deprecated.</span></span> <span data-ttu-id="0007a-176">2021 年 8 月以降は、Internet Explorer 11 はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="0007a-176">Internet Explorer 11 won’t be supported after August 2021.</span></span>|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="0007a-177">Finance 10.0.12 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="0007a-177">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="0007a-178">ポーランド SSRS レポート: 仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014</span><span class="sxs-lookup"><span data-stu-id="0007a-178">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="0007a-179">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="0007a-179">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="0007a-180">法的に必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="0007a-180">Not legally required.</span></span>  |
| <span data-ttu-id="0007a-181">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="0007a-181">**Replaced by another feature?**</span></span>   | <span data-ttu-id="0007a-182">はい (VAT 申告を含む標準監査ファイル用の Excel 形式 - JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="0007a-182">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="0007a-183">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="0007a-183">**Product areas affected**</span></span>         | <span data-ttu-id="0007a-184">応募</span><span class="sxs-lookup"><span data-stu-id="0007a-184">Application</span></span> |
| <span data-ttu-id="0007a-185">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="0007a-185">**Deployment option**</span></span>              | <span data-ttu-id="0007a-186">すべて</span><span class="sxs-lookup"><span data-stu-id="0007a-186">All</span></span> |
| <span data-ttu-id="0007a-187">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="0007a-187">**Status**</span></span>                         | <span data-ttu-id="0007a-188">非推奨: 2021 年 7 月 1 日には、SSRS レポートのサポートはなくなります: **仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014**。</span><span class="sxs-lookup"><span data-stu-id="0007a-188">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="0007a-189">代わりに、VAT 申告を含む標準監査ファイルの Excel 形式 (JPK_VDEK) の例が導入されます。</span><span class="sxs-lookup"><span data-stu-id="0007a-189">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="0007a-190">Finance 10.0.11 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="0007a-190">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="0007a-191">ノルウェー標準主勘定</span><span class="sxs-lookup"><span data-stu-id="0007a-191">Norwegian Standard main accounts</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="0007a-192">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="0007a-192">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="0007a-193">再設計</span><span class="sxs-lookup"><span data-stu-id="0007a-193">Redesign</span></span>  |
| <span data-ttu-id="0007a-194">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="0007a-194">**Replaced by another feature?**</span></span>   | <span data-ttu-id="0007a-195">はい (ER 形式のアプリケーション固有パラメータに置き換えられます)</span><span class="sxs-lookup"><span data-stu-id="0007a-195">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="0007a-196">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="0007a-196">**Product areas affected**</span></span>         | <span data-ttu-id="0007a-197">応募</span><span class="sxs-lookup"><span data-stu-id="0007a-197">Application</span></span> |
| <span data-ttu-id="0007a-198">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="0007a-198">**Deployment option**</span></span>              | <span data-ttu-id="0007a-199">すべて</span><span class="sxs-lookup"><span data-stu-id="0007a-199">All</span></span> |
| <span data-ttu-id="0007a-200">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="0007a-200">**Status**</span></span>                         | <span data-ttu-id="0007a-201">非推奨: 2021 年 4 月 1 日までに、標準主勘定に関連する機能: 参照フィールド、関連テーブル、データ エンティティ はサポートされなくなる予定です。</span><span class="sxs-lookup"><span data-stu-id="0007a-201">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="0007a-202">Finance 10.0.7 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="0007a-202">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="0007a-203">ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります</span><span class="sxs-lookup"><span data-stu-id="0007a-203">Workflow request change dialog box no longer includes user selection drop-down list</span></span>

| &nbsp; | &nbsp; |
|------------|--------------------|
| <span data-ttu-id="0007a-204">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="0007a-204">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="0007a-205">勘定グループを選択する機能に変更されました。</span><span class="sxs-lookup"><span data-stu-id="0007a-205">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="0007a-206">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="0007a-206">**Replaced by another feature?**</span></span>   | <span data-ttu-id="0007a-207">有</span><span class="sxs-lookup"><span data-stu-id="0007a-207">Yes</span></span> |
| <span data-ttu-id="0007a-208">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="0007a-208">**Product areas affected**</span></span>         | <span data-ttu-id="0007a-209">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="0007a-209">Workflow</span></span> |
| <span data-ttu-id="0007a-210">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="0007a-210">**Deployment option**</span></span>              | <span data-ttu-id="0007a-211">すべて</span><span class="sxs-lookup"><span data-stu-id="0007a-211">All</span></span> |
| <span data-ttu-id="0007a-212">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="0007a-212">**Status**</span></span>                         | <span data-ttu-id="0007a-213">非推奨: 2020 年 12 月 1 日までに、勘定グループを選択せずに中国の伝票タイプ設定をサポートしなくなります。</span><span class="sxs-lookup"><span data-stu-id="0007a-213">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="0007a-214">新しいデザインの詳細については、[10.0.7 の新機能](whats-new-changed-10-0-7.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0007a-214">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="0007a-215">削除済みまたは非推奨の機能に関する以前の発表</span><span class="sxs-lookup"><span data-stu-id="0007a-215">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="0007a-216">以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0007a-216">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
