---
title: リリース 10.0.15 (2020 年 12 月) の Dynamics 365 Supply Chain Management プレビューの新機能
description: このトピックでは、Dynamics 365 Supply Chain Management 10.0.15 の新機能または変更された機能について説明します。
author: kamaybac
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7c7ac0e795ec085584be9cfdef65333969255ed6
ms.sourcegitcommit: c55fecae96b4bb27bc313ba10a97eddb9c91350a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989314"
---
# <a name="whats-new-in-the-dynamics-365-supply-chain-management-preview-of-release-10015-december-2020"></a><span data-ttu-id="a2f10-103">リリース 10.0.15 (2020 年 12 月) の Dynamics 365 Supply Chain Management プレビューの新機能</span><span class="sxs-lookup"><span data-stu-id="a2f10-103">What's new in the Dynamics 365 Supply Chain Management preview of release 10.0.15 (December 2020)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a2f10-104">このトピックでは、バージョン 10.0.15 の Microsoft Dynamics 365 Supply Chain Management プレビューの新機能または変更された機能について一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="a2f10-104">This topic lists features that are either new or changed in the Microsoft Dynamics 365 Supply Chain Management preview of version 10.0.15.</span></span> <span data-ttu-id="a2f10-105">このバージョンには 10.0.644 のビルド番号が含まれており、次のように使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2f10-105">This version has a build number of 10.0.644 and is available as follows:</span></span>

- <span data-ttu-id="a2f10-106">**リリース 10.0.15 のプレビュー:** 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="a2f10-106">**Preview of release 10.0.15:** October 2020</span></span>
- <span data-ttu-id="a2f10-107">**リリース 10.0.15 の一般提供 (手動更新):** 2020 年 11 月</span><span class="sxs-lookup"><span data-stu-id="a2f10-107">**General availability of release 10.0.15 (manual update):** November 2020</span></span>
- <span data-ttu-id="a2f10-108">**リリース 10.0.15 の一般提供 (自動更新):** 2020 年 12 月</span><span class="sxs-lookup"><span data-stu-id="a2f10-108">**General availability of release 10.0.15 (auto update):** December 2020</span></span>

## <a name="features-included-in-this-release"></a><span data-ttu-id="a2f10-109">このリリースに含まれる機能</span><span class="sxs-lookup"><span data-stu-id="a2f10-109">Features included in this release</span></span>

<span data-ttu-id="a2f10-110">このリリースでは次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2f10-110">The following features are included in this release.</span></span> <span data-ttu-id="a2f10-111">機能タイトルは、[リリース計画](https://docs.microsoft.com/dynamics365/release-plans/)のサイトに関する追加情報にリンクします。</span><span class="sxs-lookup"><span data-stu-id="a2f10-111">The feature titles link to additional information on the [Release plans](https://docs.microsoft.com/dynamics365/release-plans/) site.</span></span> <span data-ttu-id="a2f10-112">追加のリンクは、その機能に対して現在使用可能な追加のドキュメントを指します。</span><span class="sxs-lookup"><span data-stu-id="a2f10-112">Additional links point to additional documentation that is currently available for that feature.</span></span> <span data-ttu-id="a2f10-113">一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a2f10-113">Some of the listed features are still in preview, while others may already be generally available.</span></span> <span data-ttu-id="a2f10-114">リリース計画へのリンクを使用してリリース日を確認するか、または現在のリリース ウェーブに対してリリースおよび計画されているすべての機能の日付の概要については、[Dynamics 365 Supply Chain Management の新機能および計画](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/planned-features) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2f10-114">Follow the links to the release plan to see the release dates, or go to [What's new and planned for Dynamics 365 Supply Chain Management](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/planned-features) for an overview of dates for all features released and planned for the current release wave.</span></span> <span data-ttu-id="a2f10-115">これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2f10-115">Most of these features must be enabled using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) before you can use them.</span></span>

- <span data-ttu-id="a2f10-116">製造と倉庫の実行ワークロードを使用したクラウドおよびエッジ スケールのユニット管理</span><span class="sxs-lookup"><span data-stu-id="a2f10-116">Cloud and edge scale unit management with manufacturing and warehouse execution workloads</span></span>
- [<span data-ttu-id="a2f10-117">倉庫アプリからの移動オーダーを作成および処理します</span><span class="sxs-lookup"><span data-stu-id="a2f10-117">Create and process transfer orders from the warehouse app</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/ad-hoc-transfer-order-creation-warehousing-mobile-app)<br> <span data-ttu-id="a2f10-118">- 詳細については、[倉庫アプリからの移動オーダーの作成](../warehousing/create-transfer-order-from-warehouse-app.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2f10-118">- For more information, see [Create transfer orders from the warehouse app](../warehousing/create-transfer-order-from-warehouse-app.md).</span></span>
- [<span data-ttu-id="a2f10-119">仕入先入札の既定の RFQ 返信フィールド</span><span class="sxs-lookup"><span data-stu-id="a2f10-119">Default RFQ reply fields for vendor bidding</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/default-rfq-reply-fields-for-vendor-bidding)<br> <span data-ttu-id="a2f10-120">- 詳細については、[見積依頼 (RFQ) の概要](../procurement/request-quotations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2f10-120">- For more information, see [Requests for quotation (RFQs) overview](../procurement/request-quotations.md).</span></span>
- [<span data-ttu-id="a2f10-121">Dynamics 365 Supply Chain Management のエンジニアリング変更管理アドイン</span><span class="sxs-lookup"><span data-stu-id="a2f10-121">Engineering Change Management Add-in for Dynamics 365 Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/engineering-change-management)<!-- <br> - For more information, see [Engineering change management overview](../engineering-change-management/product-engineering-overview.md).-->
- [<span data-ttu-id="a2f10-122">製造のための Mixed-reality ガイド</span><span class="sxs-lookup"><span data-stu-id="a2f10-122">Mixed-reality Guides for manufacturing</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/mixed-reality-guides-manufacturing)<br> <span data-ttu-id="a2f10-123">- 詳細については、[生産での作業者への Mixed reality ガイドの提供](../production-control/instruction-guides-in-production-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2f10-123">- For more information, see [Provide mixed-reality Guides for workers in production](../production-control/instruction-guides-in-production-overview.md).</span></span>
- [<span data-ttu-id="a2f10-124">生産フロアの実行における新しいユーザー エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="a2f10-124">New user experience for production floor execution</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/mes-terminal-enhancements-discrete-manufacturing)<!-- <br> - For more information, see [How workers use the production floor execution interface](../production-control/production-floor-execution-use.md).-->
- [<span data-ttu-id="a2f10-125">倉庫アプリ イベントの処理</span><span class="sxs-lookup"><span data-stu-id="a2f10-125">Process warehouse app events</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/process-warehouse-app-events)<br> <span data-ttu-id="a2f10-126">- 詳細については、[倉庫アプリのイベント処理](../warehousing/warehouse-app-events.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2f10-126">- For more information, see [Warehouse app event processing](../warehousing/warehouse-app-events.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2f10-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a2f10-127">Additional resources</span></span>

### <a name="platform-updates-for-finance-and-operations-apps"></a><span data-ttu-id="a2f10-128">Finance and Operations アプリのプラットフォーム更新プログラム</span><span class="sxs-lookup"><span data-stu-id="a2f10-128">Platform updates for Finance and Operations apps</span></span>

<span data-ttu-id="a2f10-129">Microsoft Dynamics 365 Supply Chain Management 10.0.15 には、Platform updates が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2f10-129">Microsoft Dynamics 365 Supply Chain Management 10.0.15 includes platform updates.</span></span> <span data-ttu-id="a2f10-130">詳細については、[Finance and Operations アプリのバージョン 10.0.15 (2020 年 10 月) のプラットフォーム アップデート](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-15.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2f10-130">To learn more, see [Platform updates for version 10.0.15 of Finance and Operations apps (October 2020)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-15.md).</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a2f10-131">バグ修正</span><span class="sxs-lookup"><span data-stu-id="a2f10-131">Bug fixes</span></span>

<span data-ttu-id="a2f10-132">10.0.15 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=514518&dbType=3&qc=8fbe12733a7e1aa197e91fb11530f69fa89b9b39c08d89a19873f755c9430988) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2f10-132">For information about the bug fixes included in each of the updates that are part of 10.0.15, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=514518&dbType=3&qc=8fbe12733a7e1aa197e91fb11530f69fa89b9b39c08d89a19873f755c9430988).</span></span>

### <a name="dynamics-365-2020-release-wave-2-plan"></a><span data-ttu-id="a2f10-133">Dynamics 365: 2020 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="a2f10-133">Dynamics 365: 2020 release wave 2 plan</span></span>

<span data-ttu-id="a2f10-134">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="a2f10-134">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="a2f10-135">[Dynamics 365: 2020 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/index) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="a2f10-135">Check out the [Dynamics 365: 2020 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/index).</span></span> <span data-ttu-id="a2f10-136">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="a2f10-136">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="a2f10-137">削除済みおよび非推奨の Supply Chain Management 機能</span><span class="sxs-lookup"><span data-stu-id="a2f10-137">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="a2f10-138">[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)トピックは、Supply Chain Management で削除または非推奨となる予定の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="a2f10-138">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="a2f10-139">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="a2f10-139">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="a2f10-140">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a2f10-140">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="a2f10-141">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="a2f10-141">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="a2f10-142">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="a2f10-142">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="a2f10-143">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="a2f10-143">Typically, these are functional updates that need to be made to the compiler.</span></span>
