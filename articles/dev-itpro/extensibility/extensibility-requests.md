---
title: "拡張機能の要求"
description: "このトピックでは、Dynamics 365 for Finance and Operations で追加の拡張ポイントを要求する方法について説明します。"
author: FrankDahl
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 86e3808c04b93370cd3cecdfb0d76a976aa7ee8c
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="extensibility-requests"></a><span data-ttu-id="543f3-103">拡張機能の要求</span><span class="sxs-lookup"><span data-stu-id="543f3-103">Extensibility requests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="543f3-104">Microsoft Dynamics 365 for Finance and Operations は拡張機能を排他的に使用して、製品をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="543f3-104">Microsoft Dynamics 365 for Finance and Operations exclusively uses extensions to customize the product.</span></span> <span data-ttu-id="543f3-105">この変更はパートナーのエコシステム全体に影響することを知っています。</span><span class="sxs-lookup"><span data-stu-id="543f3-105">We're aware that this change impacts our entire partner ecosystem.</span></span> <span data-ttu-id="543f3-106">[拡張性のホーム ページ](extensibility-home-page.md)に記載されているリソースを読むことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="543f3-106">We recommend that you read the resources listed on the [Extensibility home page](extensibility-home-page.md).</span></span> <span data-ttu-id="543f3-107">これらのリソースは多くの質問に答え、拡張機能を使用してソリューションを構築するための準備を整えます。</span><span class="sxs-lookup"><span data-stu-id="543f3-107">These resources answer many questions and prepare you for building solutions using extensions.</span></span>

<span data-ttu-id="543f3-108">拡張機能では、オーバーレイによって可能であったいくつかのカスタマイズが実行できないことが見つかります。</span><span class="sxs-lookup"><span data-stu-id="543f3-108">You will discover that some customizations, which were possible with overlayering, cannot be done through extensions.</span></span> <span data-ttu-id="543f3-109">オーバーレイすることなく同じビジネス要件を可能にするために、多くの拡張機能を追加しており、今後さらに追加する予定です。</span><span class="sxs-lookup"><span data-stu-id="543f3-109">To enable the same business requirements without overlayering, we have added many extension capabilities and expect to add more going forward.</span></span> <span data-ttu-id="543f3-110">オーバーレイにより実行された一部のカスタマイズについては、ログ要求をして、顧客の必要に気付けるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="543f3-110">For some customizations that were done with overlayering, you will need to log requests, to make us aware of what you need.</span></span>

## <a name="what-we-are-doing"></a><span data-ttu-id="543f3-111">実行する内容</span><span class="sxs-lookup"><span data-stu-id="543f3-111">What we are doing</span></span>
<span data-ttu-id="543f3-112">しばらくの間、拡張ベースのカスタマイズ モデルに向けて取り組みます。</span><span class="sxs-lookup"><span data-stu-id="543f3-112">We've been working toward an extension-based customization model for some time.</span></span> <span data-ttu-id="543f3-113">過去のいくつかのリリースにわたって、段階的にモデルが封印されてきました。</span><span class="sxs-lookup"><span data-stu-id="543f3-113">Over the past several releases we have been gradually sealing models.</span></span> <span data-ttu-id="543f3-114">Dynamics 365 for Finance and Operations リリース 8.0 以降、これでシールが完了しました。</span><span class="sxs-lookup"><span data-stu-id="543f3-114">As of Dynamics 365 for Finance and Operations release 8.0, this completes the sealing.</span></span> <span data-ttu-id="543f3-115">このリリースより後は、拡張ベースのカスタマイズのみが許可されます。</span><span class="sxs-lookup"><span data-stu-id="543f3-115">From this release forward, only extension-based customizations are allowed.</span></span> 

<span data-ttu-id="543f3-116">今後のリリースでは、より多くの拡張機能を追加して、独立系ソフトウェア ベンダー (ISV) と付加価値再販業者 (VAR) が包括的なビジネス ソリューションを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="543f3-116">In future releases, we will be adding even more extensibility capabilities to enable independent software vendors (ISVs) and value-added resellers (VARs) to deliver complete business solutions.</span></span> <span data-ttu-id="543f3-117">顧客ごとに公開の頻度に応じてこれらに優先順位を付けます。</span><span class="sxs-lookup"><span data-stu-id="543f3-117">We will prioritize these on a customer-by-customer basis with frequent releases.</span></span>

## <a name="how-do-i-log-extensibility-requests"></a><span data-ttu-id="543f3-118">拡張機能の要求を記録するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="543f3-118">How do I log extensibility requests?</span></span>
<span data-ttu-id="543f3-119">拡張子として実装することができないカスタマイズが見つかった場合は、シナリオに対して適切な拡張子サポートが製品に追加されるように Microsoft にリクエストを記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="543f3-119">If you discover a customization that you cannot implement as an extension, you must log a request to Microsoft to ensure appropriate extension support is added to the product for your scenario.</span></span>

<span data-ttu-id="543f3-120">要求を記録する前に、考慮すべき点がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="543f3-120">Before logging the request, there are a few things to consider:</span></span>  
- <span data-ttu-id="543f3-121">既存の拡張性機能を満たす必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="543f3-121">Could the requirement be met with existing extensibility features?</span></span> <span data-ttu-id="543f3-122">拡張機能を備えたソリューションを構築するには、異なる設計および実装パターンが必要です。</span><span class="sxs-lookup"><span data-stu-id="543f3-122">Building solutions with extensions requires different design and implementation patterns.</span></span>
- <span data-ttu-id="543f3-123">顧客またはビジネス アナリストへの要求はどれほど重要ですか。</span><span class="sxs-lookup"><span data-stu-id="543f3-123">How important is the requirement to the customer and/or business analyst?</span></span>  
- <span data-ttu-id="543f3-124">実装のアップグレードは長期間利用しやすいですか。</span><span class="sxs-lookup"><span data-stu-id="543f3-124">Will the implementation be upgrade friendly for the long term?</span></span>

<span data-ttu-id="543f3-125">高度なロードマップ情報を本質的に共有しているため、秘密保持契約の下にある組織はフィードバック コミュニティに登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="543f3-125">Because we are essentially sharing deep roadmap information, we require that organizations be under NDA to be enrolled in our feedback community.</span></span>

<span data-ttu-id="543f3-126">パートナーは、従業員ごとにではなく一度だけフィードバック コミュニティに参加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="543f3-126">Partners only need to join the feedback community once and not for each of their employees.</span></span> <span data-ttu-id="543f3-127">フィードバック コミュニティに登録するには。</span><span class="sxs-lookup"><span data-stu-id="543f3-127">To enroll in the feedback community:</span></span>

1. [<span data-ttu-id="543f3-128">組織のプロファイル情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="543f3-128">Provide organization profile information.</span></span>](http://aka.ms/feedbackcommunitynomination)
2. [<span data-ttu-id="543f3-129">NDA に署名し、契約書、コード、およびデータ共有ポリシーを入力します。</span><span class="sxs-lookup"><span data-stu-id="543f3-129">Sign the NDA, input agreement, code and data sharing policies.</span></span>](http://aka.ms/feedbackcommunityagreement)

<span data-ttu-id="543f3-130">パートナーとして、契約書に署名した後、組織内のユーザーは Yammer グループのフィードバックにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="543f3-130">As a partner, after you have signed the agreements, people from your organization will be able to access the feedback Yammer groups.</span></span> <span data-ttu-id="543f3-131">さまざまな拡張性のテーマについて検討している「オペレーションの拡張性」の Yammer グループに参加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="543f3-131">We recommend that you join the Yammer group 'Operations extensibility' where a broad range of extensibility topics are discussed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="543f3-132">今後のリリースで、拡張機能の要求が Lifecycle Services (LCS) 経由で送信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="543f3-132">In a future release, extensibility requests will be able to be submitted via Lifecycle Services (LCS).</span></span> <span data-ttu-id="543f3-133">しばらくは、daxcf@microsoft.com まで要求を送信してください。</span><span class="sxs-lookup"><span data-stu-id="543f3-133">In the meantime, please submit your request to daxcf@microsoft.com.</span></span>

<span data-ttu-id="543f3-134">拡張機能の要求を記録するときは、拡張機能を有効にする必要がある対象に関する詳細情報を入力し、拡張を必要とする内容に関する情報を含めます。</span><span class="sxs-lookup"><span data-stu-id="543f3-134">When you log extensibility requests, please enter detailed information about what you need to become enabled for extensibility, and include information on what it is you need to extend.</span></span> <span data-ttu-id="543f3-135">これはマイクロソフトがお客様の要求に効率的に対処するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="543f3-135">This will help Microsoft to be efficient in addressing your requests.</span></span> <span data-ttu-id="543f3-136">ニーズに効果的に取り組み、ユーザーが必要とする機能を標準アプリケーションで有効にする仕方を Microsoft に提案してください。</span><span class="sxs-lookup"><span data-stu-id="543f3-136">You are  welcome to propose how Microsoft could enable the functionality that you need in the standard application in a way that effectively addresses your needs.</span></span>

> [!NOTE]
> <span data-ttu-id="543f3-137">拡張性の要求を修正プログラムとしてリリースしません。</span><span class="sxs-lookup"><span data-stu-id="543f3-137">We will not release extensibility requests as hotfixes.</span></span>  

<span data-ttu-id="543f3-138">拡張性要求は、Dynamics 365 for Finance and Operations のみために排他的です。</span><span class="sxs-lookup"><span data-stu-id="543f3-138">Extensibility requests are exclusive for Dynamics 365 for Finance and Operations only.</span></span> <span data-ttu-id="543f3-139">Dynamics AX 2012 またはそれ以前のリリースの拡張機能の要求に対応する計画はありません。</span><span class="sxs-lookup"><span data-stu-id="543f3-139">We are not planning to accommodate extensibility requests for Dynamics AX 2012 or earlier releases.</span></span>

## <a name="when-will-my-extensibility-requests-be-enabled"></a><span data-ttu-id="543f3-140">個人の拡張機能の要求はいつ有効になりますか。</span><span class="sxs-lookup"><span data-stu-id="543f3-140">When will my extensibility requests be enabled?</span></span>

<span data-ttu-id="543f3-141">拡張性要求は、バックログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="543f3-141">Extensibility requests are logged to a backlog.</span></span> <span data-ttu-id="543f3-142">Microsoft エンジニアは、すべての要求に優先度付けを行ってから、優先順位で作業します。</span><span class="sxs-lookup"><span data-stu-id="543f3-142">Microsoft engineers prioritize all requests, and then work on them in priority order.</span></span> <span data-ttu-id="543f3-143">Microsoft はすべての要求が処理されることを確証できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="543f3-143">Please note that Microsoft is not ensuring that all requests will be fulfilled.</span></span> <span data-ttu-id="543f3-144">特に、本質的に煩雑な要求はシームレスなアップグレードを妨げるためサポートされません。</span><span class="sxs-lookup"><span data-stu-id="543f3-144">In particular, requests that are intrusive by nature will not be supported, as they will prevent seamless upgrade.</span></span>

## <a name="how-will-extensibility-requests-be-made-available-to-deploy"></a><span data-ttu-id="543f3-145">拡張機能の要求を展開するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="543f3-145">How will extensibility requests be made available to deploy?</span></span>
<span data-ttu-id="543f3-146">Dynamics 365 for Finance and Operations リリース 8.0 の後、新しい機能拡張の要求で頻繁にアプリケーション更新をリリースする予定です。</span><span class="sxs-lookup"><span data-stu-id="543f3-146">After Dynamics 365 for Finance and Operations release 8.0, we plan to release frequent application updates with new extensibility requests.</span></span> <span data-ttu-id="543f3-147">これは、プラットフォームの更新プログラムと同じリリース ケイデンスに従います。</span><span class="sxs-lookup"><span data-stu-id="543f3-147">This will follow the same release cadence as platform updates.</span></span> 

## <a name="still-have-questions"></a><span data-ttu-id="543f3-148">疑問が解決されない場合</span><span class="sxs-lookup"><span data-stu-id="543f3-148">Still have questions?</span></span>

<span data-ttu-id="543f3-149">[拡張性についてよく寄せられる質問](app-sealing-faq.md)と[拡張機能のホーム ページ](extensibility-home-page.md)にリストされた他のリソースをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="543f3-149">Read the [Extensibility FAQ](app-sealing-faq.md) and the other resources listed on the [Extensibility home page](extensibility-home-page.md).</span></span>

