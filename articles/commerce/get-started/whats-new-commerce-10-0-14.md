---
title: Dynamics 365 Commerce 10.0.14 (2020 年 11 月) の新機能と変更された機能
description: このトピックでは、Dynamics 365 Commerce 10.0.14 の新機能または変更された機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-08-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 280eba948f598e279e9bc00a778c4d4ad3ab91fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965064"
---
# <a name="whats-new-and-changed-in-dynamics-365-commerce-10014-november-2020"></a><span data-ttu-id="db2f3-103">Dynamics 365 Commerce 10.0.14 (2020 年 11 月) の新機能と変更された機能</span><span class="sxs-lookup"><span data-stu-id="db2f3-103">What's new and changed in Dynamics 365 Commerce 10.0.14 (November 2020)</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="db2f3-104">このトピックでは、Microsoft Dynamics 365 Commerce 10.0.14 の新機能または変更された機能について列挙します。</span><span class="sxs-lookup"><span data-stu-id="db2f3-104">This topic lists features that are either new or changed in Microsoft Dynamics 365 Commerce 10.0.14.</span></span> <span data-ttu-id="db2f3-105">このバージョンのビルド番号は 10.0.605 で、次のスケジュールで使用できます。</span><span class="sxs-lookup"><span data-stu-id="db2f3-105">This version has a build number of 10.0.605 and is available on the following schedule:</span></span>

- <span data-ttu-id="db2f3-106">**プレビュー リリース:** 2020 年 9 月</span><span class="sxs-lookup"><span data-stu-id="db2f3-106">**Preview release:** September 2020</span></span>
- <span data-ttu-id="db2f3-107">**一般提供 (自己更新):** 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="db2f3-107">**General availability (self-update):** October 2020</span></span>
- <span data-ttu-id="db2f3-108">**自動更新:** 2020 年 11 月</span><span class="sxs-lookup"><span data-stu-id="db2f3-108">**Auto-update:** November 2020</span></span>

## <a name="features-included-in-this-release"></a><span data-ttu-id="db2f3-109">このリリースに含まれる機能</span><span class="sxs-lookup"><span data-stu-id="db2f3-109">Features included in this release</span></span>

<span data-ttu-id="db2f3-110">このリリースでは次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="db2f3-110">The following features are included in this release.</span></span> <span data-ttu-id="db2f3-111">機能タイトルは、[リリース計画](https://docs.microsoft.com/dynamics365/release-plans/)のサイトに関する追加情報にリンクします。</span><span class="sxs-lookup"><span data-stu-id="db2f3-111">The feature titles link to additional information on the [Release plans](https://docs.microsoft.com/dynamics365/release-plans/) site.</span></span> <span data-ttu-id="db2f3-112">追加のリンクは、その機能に対して現在使用可能な追加のドキュメントを指します。</span><span class="sxs-lookup"><span data-stu-id="db2f3-112">Additional links point to additional documentation that is currently available for that feature.</span></span> <span data-ttu-id="db2f3-113">これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="db2f3-113">Most of these features must be enabled using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) before you can use them.</span></span>

- [<span data-ttu-id="db2f3-114">E コマース用の放棄されたカート機能</span><span class="sxs-lookup"><span data-stu-id="db2f3-114">Abandoned cart capabilities for e-commerce</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/commerce/dynamics365-commerce/abandoned-cart-capabilities-e-commerce)
- [<span data-ttu-id="db2f3-115">Dynamics 365 Commerce での実験</span><span class="sxs-lookup"><span data-stu-id="db2f3-115">Experimentation in Dynamics 365 Commerce</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/commerce/dynamics365-commerce/experimentation-dynamics-365-commerce)
- [<span data-ttu-id="db2f3-116">POS での入荷中に、発注書への品目の追加がサポートされます</span><span class="sxs-lookup"><span data-stu-id="db2f3-116">Support for adding items to purchase orders during receiving in POS</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/commerce/dynamics365-commerce/support-adding-items-purchase-orders-during-receiving-pos)<br> <span data-ttu-id="db2f3-117">- 詳細については、[POS での入庫在庫操作](../pos-inbound-inventory-operation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db2f3-117">- For more information, see [Inbound inventory operation in POS](../pos-inbound-inventory-operation.md).</span></span>
- [<span data-ttu-id="db2f3-118">POS から出荷する移動オーダーの出荷時のシリアル番号登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="db2f3-118">Support serial number registration on outbound transfer order shipments from POS</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/commerce/dynamics365-commerce/support-serial-number-registration-outbound-transfer-order-shipments-pos)<br> <span data-ttu-id="db2f3-119">- 詳細については、[POS でシリアル化された品目を使って作業する](../pos-serialized-items.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db2f3-119">- For more information, see [Work with serialized items in the POS](../pos-serialized-items.md).</span></span>
- <span data-ttu-id="db2f3-120">ソーシャル共有モジュール</span><span class="sxs-lookup"><span data-stu-id="db2f3-120">Social share module</span></span><br> <span data-ttu-id="db2f3-121">- 詳細については、[ソーシャル シェア モジュール](../social-share-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db2f3-121">- For more information, see [Social share module](../social-share-module.md).</span></span>
- <span data-ttu-id="db2f3-122">ハードウェア ステーションを使用しないクレジットカードの処理</span><span class="sxs-lookup"><span data-stu-id="db2f3-122">Process credit cards without a hardware station</span></span><br> <span data-ttu-id="db2f3-123">- 詳細については、[ハードウェア ステーションのないクレジットカードの処理](../dev-itpro/cnp-pos.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db2f3-123">- For more information, see [Process credit cards without a hardware station](../dev-itpro/cnp-pos.md).</span></span>
- [<span data-ttu-id="db2f3-124">ギフト カードの残高の確認モジュール</span><span class="sxs-lookup"><span data-stu-id="db2f3-124">Gift card balance check module</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/commerce/dynamics365-commerce/gift-card-purchase-e-commerce)<br> <span data-ttu-id="db2f3-125">- 詳細については、[ギフト カード モジュール](../add-giftcard.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db2f3-125">- For more information, see [Gift card module](../add-giftcard.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db2f3-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="db2f3-126">Additional resources</span></span>

### <a name="platform-updates-for-finance-and-operations-apps"></a><span data-ttu-id="db2f3-127">Finance and Operations アプリのプラットフォーム更新プログラム</span><span class="sxs-lookup"><span data-stu-id="db2f3-127">Platform updates for Finance and Operations apps</span></span>

<span data-ttu-id="db2f3-128">Dynamics 365 Commerce 10.0.14 には、プラットフォーム更新プログラムが含まれています。</span><span class="sxs-lookup"><span data-stu-id="db2f3-128">Dynamics 365 Commerce 10.0.14 includes platform updates.</span></span> <span data-ttu-id="db2f3-129">詳細については、[Finance and Operations アプリのバージョン 10.0.14 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db2f3-129">To learn more, see [Platform updates for version 10.0.14 of Finance and Operations apps](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14.md).</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="db2f3-130">バグ修正</span><span class="sxs-lookup"><span data-stu-id="db2f3-130">Bug fixes</span></span> 
<span data-ttu-id="db2f3-131">この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=488609&dbType=3&qc=8251e8e1d5e2386de850599926c1adc3fec8e2ba25308036d22cdfe0a1c28fc7) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db2f3-131">For information about the bug fixes that are included in this update, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=488609&dbType=3&qc=8251e8e1d5e2386de850599926c1adc3fec8e2ba25308036d22cdfe0a1c28fc7).</span></span>

### <a name="dynamics-365-2020-release-wave-2-plan"></a><span data-ttu-id="db2f3-132">Dynamics 365: 2020 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="db2f3-132">Dynamics 365: 2020 release wave 2 plan</span></span>

<span data-ttu-id="db2f3-133">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="db2f3-133">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="db2f3-134">[Dynamics 365: 2020 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="db2f3-134">Check out the [Dynamics 365: 2020 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/).</span></span> <span data-ttu-id="db2f3-135">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="db2f3-135">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="db2f3-136">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="db2f3-136">Removed and deprecated features</span></span>

<span data-ttu-id="db2f3-137">[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)トピックでは、Commerce で削除または廃止された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="db2f3-137">The [Removed or deprecated features in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) topic describes features that have been removed or deprecated for Commerce.</span></span>

- <span data-ttu-id="db2f3-138">*削除された* 機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="db2f3-138">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="db2f3-139">*削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="db2f3-139">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="db2f3-140">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="db2f3-140">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="db2f3-141">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="db2f3-141">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="db2f3-142">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="db2f3-142">Typically, these are functional updates that need to be made to the compiler.</span></span>
