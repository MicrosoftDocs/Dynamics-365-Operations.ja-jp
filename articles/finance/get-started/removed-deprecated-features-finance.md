---
title: Dynamics 365 Finance の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
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
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175111"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="596a7-103">Dynamics 365 Finance の削除済みまたは推奨されない機能</span><span class="sxs-lookup"><span data-stu-id="596a7-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="596a7-104">このトピックでは、Dynamics 365 Finance から削除された、または削除される予定の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="596a7-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="596a7-105">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="596a7-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="596a7-106">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="596a7-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="596a7-107">このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="596a7-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="596a7-108">Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="596a7-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="596a7-109">これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。</span><span class="sxs-lookup"><span data-stu-id="596a7-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="596a7-110">Finance 10.0.12 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="596a7-110">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="596a7-111">ポーランド SSRS レポート: 仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014</span><span class="sxs-lookup"><span data-stu-id="596a7-111">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="596a7-112">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="596a7-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="596a7-113">法的に必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="596a7-113">Not legally required.</span></span>  |
| <span data-ttu-id="596a7-114">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="596a7-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="596a7-115">はい (VAT 申告を含む標準監査ファイル用の Excel 形式 - JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="596a7-115">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="596a7-116">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="596a7-116">**Product areas affected**</span></span>         | <span data-ttu-id="596a7-117">応募</span><span class="sxs-lookup"><span data-stu-id="596a7-117">Application</span></span> |
| <span data-ttu-id="596a7-118">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="596a7-118">**Deployment option**</span></span>              | <span data-ttu-id="596a7-119">すべて</span><span class="sxs-lookup"><span data-stu-id="596a7-119">All</span></span> |
| <span data-ttu-id="596a7-120">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="596a7-120">**Status**</span></span>                         | <span data-ttu-id="596a7-121">非推奨: 2021 年 7 月 1 日には、SSRS レポートのサポートはなくなります: **仮受 VAT 登録、購買 VAT 登録、EU 集計 VAT 登録 – 機能参照 PL-00014**。</span><span class="sxs-lookup"><span data-stu-id="596a7-121">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="596a7-122">代わりに、VAT 申告を含む標準監査ファイルの Excel 形式 (JPK_VDEK) の例が導入されます。</span><span class="sxs-lookup"><span data-stu-id="596a7-122">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="596a7-123">Finance 10.0.11 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="596a7-123">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="596a7-124">ノルウェー標準主勘定</span><span class="sxs-lookup"><span data-stu-id="596a7-124">Norwegian Standard main accounts</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="596a7-125">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="596a7-125">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="596a7-126">再設計</span><span class="sxs-lookup"><span data-stu-id="596a7-126">Redesign</span></span>  |
| <span data-ttu-id="596a7-127">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="596a7-127">**Replaced by another feature?**</span></span>   | <span data-ttu-id="596a7-128">はい (ER 形式のアプリケーション固有パラメータに置き換えられます)</span><span class="sxs-lookup"><span data-stu-id="596a7-128">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="596a7-129">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="596a7-129">**Product areas affected**</span></span>         | <span data-ttu-id="596a7-130">応募</span><span class="sxs-lookup"><span data-stu-id="596a7-130">Application</span></span> |
| <span data-ttu-id="596a7-131">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="596a7-131">**Deployment option**</span></span>              | <span data-ttu-id="596a7-132">すべて</span><span class="sxs-lookup"><span data-stu-id="596a7-132">All</span></span> |
| <span data-ttu-id="596a7-133">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="596a7-133">**Status**</span></span>                         | <span data-ttu-id="596a7-134">非推奨: 2021 年 4 月 1 日までに、標準主勘定に関連する機能: 参照フィールド、関連テーブル、データ エンティティ はサポートされなくなる予定です。</span><span class="sxs-lookup"><span data-stu-id="596a7-134">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="596a7-135">Finance 10.0.7 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="596a7-135">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="596a7-136">ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります</span><span class="sxs-lookup"><span data-stu-id="596a7-136">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="596a7-137">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="596a7-137">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="596a7-138">勘定グループを選択する機能に変更されました。</span><span class="sxs-lookup"><span data-stu-id="596a7-138">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="596a7-139">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="596a7-139">**Replaced by another feature?**</span></span>   | <span data-ttu-id="596a7-140">有</span><span class="sxs-lookup"><span data-stu-id="596a7-140">Yes</span></span> |
| <span data-ttu-id="596a7-141">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="596a7-141">**Product areas affected**</span></span>         | <span data-ttu-id="596a7-142">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="596a7-142">Workflow</span></span> |
| <span data-ttu-id="596a7-143">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="596a7-143">**Deployment option**</span></span>              | <span data-ttu-id="596a7-144">すべて</span><span class="sxs-lookup"><span data-stu-id="596a7-144">All</span></span> |
| <span data-ttu-id="596a7-145">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="596a7-145">**Status**</span></span>                         | <span data-ttu-id="596a7-146">非推奨: 2020 年 12 月 1 日までに、勘定グループを選択せずに中国の伝票タイプ設定をサポートしなくなります。</span><span class="sxs-lookup"><span data-stu-id="596a7-146">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="596a7-147">新しいデザインの詳細については、[10.0.7 の新機能](whats-new-changed-10-0-7.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="596a7-147">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="596a7-148">削除済みまたは非推奨の機能に関する以前の発表</span><span class="sxs-lookup"><span data-stu-id="596a7-148">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="596a7-149">以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="596a7-149">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
