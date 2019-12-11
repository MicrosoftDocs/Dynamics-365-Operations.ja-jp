---
title: 評価とレビューの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価とレビューについて説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 45a6710a10fe3d33457c1327c8fc339c9ad0082a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698191"
---
# <a name="ratings-and-reviews-overview"></a><span data-ttu-id="5162b-103">評価とレビューの概要</span><span class="sxs-lookup"><span data-stu-id="5162b-103">Ratings and reviews overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5162b-104">このトピックでは、Microsoft Dynamics 365 Commerce の評価とレビューについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5162b-104">This topic covers ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5162b-105">概要</span><span class="sxs-lookup"><span data-stu-id="5162b-105">Overview</span></span>

<span data-ttu-id="5162b-106">評価とレビューは、他の顧客が製品をどのように認識しているかを知りたい E コマースの顧客にとって非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="5162b-106">Ratings and reviews are crucial for e-Commerce customers who want to know how other customers perceive a product.</span></span> <span data-ttu-id="5162b-107">また、消費者が購買決定を行うのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5162b-107">They can also help consumers make purchase decisions.</span></span> <span data-ttu-id="5162b-108">Dynamics 365 Commerce において、評価とレビューのソリューションにより、小売業者は製品に対する顧客からのレビューと評価を把握できます。</span><span class="sxs-lookup"><span data-stu-id="5162b-108">In Dynamics 365 Commerce, the ratings and reviews solution lets retailers capture product reviews and ratings from customers.</span></span> <span data-ttu-id="5162b-109">小売業者は、E コマース Web サイト間での平均評価とレビュー情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="5162b-109">Retailers can then show average ratings and review information across their e-Commerce website.</span></span>

<span data-ttu-id="5162b-110">平均評価情報は、販売時点管理 (POS) およびコール センター チャネルで表示されます。</span><span class="sxs-lookup"><span data-stu-id="5162b-110">Average rating information is shown in point of sale (POS) and call center channels.</span></span> <span data-ttu-id="5162b-111">したがって、販売担当者はユーザーが決定するためにそれを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5162b-111">Therefore, sales associates can use it to help users make decisions.</span></span> <span data-ttu-id="5162b-112">評価とレビューは、小売業者が製品の品質を向上させるために使用するフィードバック メカニズムとしても機能するので、売上が増加します。</span><span class="sxs-lookup"><span data-stu-id="5162b-112">Ratings and reviews can also serve as a feedback mechanism that retailers can use to improve the quality of a product and therefore increase sales.</span></span>

<span data-ttu-id="5162b-113">Dynamics 365 Commerce の評価とレビュー機能は、オムニチャネル ソリューションであり、プラットフォームの一部としてネイティブで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="5162b-113">Ratings and reviews functionality in Dynamics 365 Commerce is an omnichannel solution and is natively available as part of the platform.</span></span> <span data-ttu-id="5162b-114">評価とレビュー ソリューションは、Microsoft Azure の上位にビルドされ、高いスケーラビリティと信頼性を提供します。</span><span class="sxs-lookup"><span data-stu-id="5162b-114">The ratings and reviews solution is built on top of Microsoft Azure, which provides high scalability and reliability.</span></span>

<span data-ttu-id="5162b-115">次の図で、評価とレビュー ソリューションが Dynamics 365 Commerce でどのように機能するかを示します。</span><span class="sxs-lookup"><span data-stu-id="5162b-115">The following illustration shows how the ratings and reviews solution works in Dynamics 365 Commerce.</span></span>

![Dynamics 365 for Commerce の評価とレビュー](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

<span data-ttu-id="5162b-117">Dynamics 365 Commerce の評価とレビュー ソリューションは、Azure Cognitive Services を使用し、自動的に 40 の言語で俗語をモデレーションします。</span><span class="sxs-lookup"><span data-stu-id="5162b-117">The ratings and reviews solution in Dynamics 365 Commerce uses Azure Cognitive Services to offer automatic moderation of profane words in 40 languages.</span></span> <span data-ttu-id="5162b-118">人間による承認は必要ではないので、モデレーション費を減少できます。</span><span class="sxs-lookup"><span data-stu-id="5162b-118">Because human approval isn't required, moderation costs are reduced.</span></span> <span data-ttu-id="5162b-119">また、システムは、顧客の懸念事項、フィードバック、および要求の取り下げに応答し、ユーザーからのデータ要求処理を行うために使用できるモデレーター ツールも提供します。</span><span class="sxs-lookup"><span data-stu-id="5162b-119">The system also offers moderator tools that can be used to respond to customer concerns, feedback, and take-down requests, and to address data requests from users.</span></span>

<span data-ttu-id="5162b-120">評価とレビュー ソリューションは、製品リスト、検索結果、製品の詳細ページ、およびその他の場所に評価の概要を表示するウィジェットを提供します。</span><span class="sxs-lookup"><span data-stu-id="5162b-120">The ratings and reviews solution provides widgets that show rating summaries in product lists, in search results, on product details page, and in other places.</span></span> <span data-ttu-id="5162b-121">ウィジェットは完全なレビュー リストを表示し、また並べ替えやフィルタ処理のオプションも提供します。</span><span class="sxs-lookup"><span data-stu-id="5162b-121">The widgets show complete review lists, and they also provide sorting and filtering options.</span></span>

<span data-ttu-id="5162b-122">また、評価とレビュー ソリューションは、評価とレビュにインサイトを与えるためのメトリックス セットを含む、ビジネス インテリジェンス (BI) テンプレートも提供します。</span><span class="sxs-lookup"><span data-stu-id="5162b-122">The ratings and reviews solution also provides a business intelligence (BI) template that includes a set of metrics to provide insights into ratings and reviews.</span></span> <span data-ttu-id="5162b-123">さらなる分析のために、評価とレビュー データをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="5162b-123">Ratings and reviews data can be exported for further analysis.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5162b-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5162b-124">Additional resources</span></span>

[<span data-ttu-id="5162b-125">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="5162b-125">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="5162b-126">評価とレビューの管理</span><span class="sxs-lookup"><span data-stu-id="5162b-126">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="5162b-127">評価とレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5162b-127">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="5162b-128">Dynamics 365 Retail の商品評価の同期</span><span class="sxs-lookup"><span data-stu-id="5162b-128">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
