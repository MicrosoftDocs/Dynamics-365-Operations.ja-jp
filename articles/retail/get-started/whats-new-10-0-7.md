---
title: Dynamics 365 Retail バージョン 10.0.7 の機能をプレビューする
description: このトピックでは Dynamics 365 Retail のプレビュー中の機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 8f2142745d0f04831f22b3f146d4072bb6d60bc2
ms.sourcegitcommit: 381ea71cf22898587ca6af4700b51ad1b4d1a397
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2019
ms.locfileid: "2660823"
---
# <a name="preview-features-in-dynamics-365-retail-version-1007"></a><span data-ttu-id="58cfd-103">Dynamics 365 Retail バージョン 10.0.7 の機能をプレビューする</span><span class="sxs-lookup"><span data-stu-id="58cfd-103">Preview features in Dynamics 365 Retail version 10.0.7</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="58cfd-104">このトピックでは、Microsoft Dynamics 365 Retail 10.0.7 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="58cfd-104">This topic describes features that are new or changed in Microsoft Dynamics 365 Retail in 10.0.7.</span></span> <span data-ttu-id="58cfd-105">このバージョンのビルド番号は 10.0.283 です。</span><span class="sxs-lookup"><span data-stu-id="58cfd-105">This version has a build number of 10.0.283.</span></span> <span data-ttu-id="58cfd-106">一般提供開始日は 2020 年 1 月ですが、新機能は 10 月の初期リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-106">While the general availability date is in January 2020, the new features are available for early release in October.</span></span> <span data-ttu-id="58cfd-107">バージョン 10.0.7 の詳細については [追加リソース](whats-new-10-0-7.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58cfd-107">For more information about version 10.0.7, see [Additional resources](whats-new-10-0-7.md#additional-resources).</span></span>

## <a name="clienteling"></a><span data-ttu-id="58cfd-108">クライアンテリング</span><span class="sxs-lookup"><span data-stu-id="58cfd-108">Clienteling</span></span>
<span data-ttu-id="58cfd-109">多くの小売業者、特にハイエンドの専門小売業者は、店員に主な顧客との長期的な関係を形成させます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-109">Many retailers, especially high-end specialty retailers, want their sales associates to form long term relationships with their key customers.</span></span> <span data-ttu-id="58cfd-110">店員は、顧客の好き嫌い、購買履歴、製品の好み、記念日や誕生日などの重要な日について知っていることが期待されています。店員はそのような情報をキャプチャし、必要な時に簡単に情報を見つけられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="58cfd-110">The sales associates are expected to know about their customer's likes and dislikes, purchase history, product preferences, important dates such as anniversary, birthday etc. The associates need a place to capture such information and easily find the information when needed.</span></span> <span data-ttu-id="58cfd-111">この情報が 1 つのビューで使用可能になると、店員は、ハンドバッグを購入したい顧客や、誕生日、記念日、卒業式などの生活の重要なイベントが近づいている顧客など、特定の基準に一致する顧客を簡単にターゲットにすることができます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-111">Once this information is available in a single view, then the associates can easily target the customers that meet certain criteria for e.g. find all the customers that prefer to shop for Handbags, find customers for whom an important live event such as birthday, anniversary, graduation etc. is approaching.</span></span> <span data-ttu-id="58cfd-112">Dynamics 365 Retail の新しいクライアンテリング機能により、そのような関係の構築および管理を簡単に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-112">The new clienteling capabilities in in Dynamics 365 Retail can help your associates easily build and maintain such relationships.</span></span>

## <a name="tender-based-discounts"></a><span data-ttu-id="58cfd-113">支払/入金ベースの割引</span><span class="sxs-lookup"><span data-stu-id="58cfd-113">Tender based discounts</span></span>
<span data-ttu-id="58cfd-114">小売業者がプライベート ブランドのクレジット カードをリリースすることが一般的になりました。</span><span class="sxs-lookup"><span data-stu-id="58cfd-114">It has now become a common practice for retailers to release private branded credit cards.</span></span> <span data-ttu-id="58cfd-115">小売業者は銀行から優先レートを取得することから利益を得ており、研究によると、そのようなクレジット カードは店舗訪問の頻度の増加につながり、小売業者の収益を直接改善します。</span><span class="sxs-lookup"><span data-stu-id="58cfd-115">Retailers benefit from getting preferred rates from the banks, and according to a study, such credits cards result in an increase in the store visit frequency, thus directly improving the bottom line of the retailer.</span></span> <span data-ttu-id="58cfd-116">このため、小売業者はそのようなクレジット カードの使用頻度を増加させたいと思っています。</span><span class="sxs-lookup"><span data-stu-id="58cfd-116">So, retailers are motivated to increase the usage frequency of such credit cards.</span></span> <span data-ttu-id="58cfd-117">この目標を達成するために、小売業者は多くの場合、これらのカードの使用のために追加の割引を提供します。この機能により、小売業者は、ユーザーが優先支払/入金を使用して支払う場合に適格なラインに適用される割引率を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-117">To achieve this goal, retailers often provide additional discounts for using these cards.With this feature, the retailers can configure a discount percentage that would be applied on the qualified lines if the user pays using the preferred tender.</span></span>  

## <a name="hardware-station-mass-deployment"></a><span data-ttu-id="58cfd-118">ハードウェア ステーションの一括配置</span><span class="sxs-lookup"><span data-stu-id="58cfd-118">Hardware station mass deployment</span></span>
<span data-ttu-id="58cfd-119">企業の規模が拡大するにつれて、ハードウェア ステーションなどのコンポーネントの一括配置およびインストールは、比較的管理不能になってきています。</span><span class="sxs-lookup"><span data-stu-id="58cfd-119">As companies increase in size, massive deployment and installation of components, such as hardware station, has become relatively unmanageable.</span></span> <span data-ttu-id="58cfd-120">この機能により、初期および長期的な配置および管理の難しさを大幅に削減するだけでなく、信頼性と弾力性を増加させるハードウェア ステーションのフローを強化することができます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-120">This feature will not only dramatically reduce the difficulty of initial and long-term deployment and maintenance, it will enhance the flow of hardware station which increases reliability and resiliency.</span></span>  <span data-ttu-id="58cfd-121">この新しい機能により、ユーザーはハードウェア ステーションの一括配置をサイレントで実行することができます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-121">This new feature allows users to silently perform a mass deployment of the hardware station.</span></span> <span data-ttu-id="58cfd-122">小売業者は、このコンポーネントの配置およびサービスのために、配置ツール (System Center など) を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-122">Retailers can choose the deployment tool of their choice (such as System Center) to deploy and service this component.</span></span> <span data-ttu-id="58cfd-123">これにより、ハードウェア ステーションの時間の経過と共に、速度の強化および容易な配置に加え、ハードウェアステーションの信頼性と弾力性が改善されます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-123">This will provide improvements to reliability and resiliency over time for the hardware station on top of the enhanced speed and ease with which deployment occurs.</span></span>



## <a name="additional-resources"></a><span data-ttu-id="58cfd-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="58cfd-124">Additional resources</span></span>

### <a name="platform-update-31"></a><span data-ttu-id="58cfd-125">プラットフォーム update 31</span><span class="sxs-lookup"><span data-stu-id="58cfd-125">Platform update 31</span></span>

<span data-ttu-id="58cfd-126">Microsoft Dynamics 365 Supply Chain Management 10.0.7 には、プラットフォーム更新プログラム 31 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="58cfd-126">Microsoft Dynamics 365 Supply Chain Management 10.0.7 includes Platform update 31.</span></span> <span data-ttu-id="58cfd-127">プラットフォーム更新プログラム 31 に関する詳細については、[プラットフォーム更新プログラム 31 のプレビュー機能](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58cfd-127">To learn more about Platform update 31, see [Preview features in Platform update 31](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31.md).</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="58cfd-128">バグ修正</span><span class="sxs-lookup"><span data-stu-id="58cfd-128">Bug fixes</span></span> 
<span data-ttu-id="58cfd-129">10.0.7 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://https://fix.lcs.dynamics.com/Issue/Details?bugId=386529&dbType=3&qc=e03ced97fa18dc4439f36de17b00da7257dc15869a72e5b2435fec0acec0c493) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58cfd-129">For information about the bug fixes included in each of the updates that are part of 10.0.7, sign in to Lifecycle Services (LCS) and view the [KB article](https://https://fix.lcs.dynamics.com/Issue/Details?bugId=386529&dbType=3&qc=e03ced97fa18dc4439f36de17b00da7257dc15869a72e5b2435fec0acec0c493).</span></span>


### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="58cfd-130">Dynamics 365: 2019 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="58cfd-130">Dynamics 365: 2019 release wave 2 plan</span></span>

<span data-ttu-id="58cfd-131">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="58cfd-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="58cfd-132">[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/index) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="58cfd-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/index).</span></span> <span data-ttu-id="58cfd-133">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="58cfd-134">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="58cfd-134">Removed and deprecated features</span></span>

<span data-ttu-id="58cfd-135">[削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="58cfd-135">The [Removed or deprecated features](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="58cfd-136">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="58cfd-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="58cfd-137">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="58cfd-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="58cfd-138">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="58cfd-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="58cfd-139">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="58cfd-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="58cfd-140">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="58cfd-140">Typically, these are functional updates that need to be made to the compiler.</span></span>