---
title: チャンネル固有の割引の定義
description: 小売業者は、多くの場合、異なるチャンネルのさまざまな割引を設定します。 このトピックでは、特定のチャンネルの割引を作成するために知っておく必要のある概念を確認します。
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 36b2d8f96f8545f9fa792e42c639b03e1e14e8ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213749"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="538f9-104">チャネル固有の割引の定義</span><span class="sxs-lookup"><span data-stu-id="538f9-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="538f9-105">このトピックでは、特定のチャンネルの割引を作成するために知っておく必要のある概念を確認します。</span><span class="sxs-lookup"><span data-stu-id="538f9-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="538f9-106">チャンネル固有の割引</span><span class="sxs-lookup"><span data-stu-id="538f9-106">Channel-specific discounts</span></span>

<span data-ttu-id="538f9-107">小売業者は、多くの場合、異なるチャンネルでさまざまな割引を提供します。</span><span class="sxs-lookup"><span data-stu-id="538f9-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="538f9-108">それらは、国内市場の状況に合わせて行われたり、競合の小売業者に対処するために行われる場合があります。</span><span class="sxs-lookup"><span data-stu-id="538f9-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="538f9-109">Commerce は、チャネル固有の割引を定義するために価格グループを使用します。</span><span class="sxs-lookup"><span data-stu-id="538f9-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="538f9-110">価格グループは、次のエンティティーの 1 つ以上に割り当てることができます: チャンネル、カタログ、加盟者、ロイヤルティー プログラム。</span><span class="sxs-lookup"><span data-stu-id="538f9-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="538f9-111">この記事ではチャンネルについて説明しますが、カタログ割引、加盟者割引、ロイヤルティー割引に対しても同じ概念が適用できます。</span><span class="sxs-lookup"><span data-stu-id="538f9-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="538f9-112">価格グループ</span><span class="sxs-lookup"><span data-stu-id="538f9-112">Price groups</span></span>

<span data-ttu-id="538f9-113">[![価格グループ](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="538f9-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="538f9-114">上記の図は、トランザクションで扱うことができるエンティティ (チャンネル、カタログ、加盟者、顧客、ロイヤルティ カード) とさまざまな設定可能な割引との間の関係を説明しています。</span><span class="sxs-lookup"><span data-stu-id="538f9-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="538f9-115">すべてのトランザクションはチャンネルで発生するため、あるトランザクションに対してチャンネルが存在することが保証されます。</span><span class="sxs-lookup"><span data-stu-id="538f9-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="538f9-116">残りのエンティティーはオプションです。</span><span class="sxs-lookup"><span data-stu-id="538f9-116">The remaining entities are optional.</span></span> <span data-ttu-id="538f9-117">各マスター データ ページには、関連する価格グループのページへのリンクがあり、必要に応じて価格グループを表示および追加できます。</span><span class="sxs-lookup"><span data-stu-id="538f9-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="538f9-118">価格グループを使用すると、4 つの異なるエンティティ タイプを、割引、価格調整、売買契約に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="538f9-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="538f9-119">価格グループの名前の付け方を戦略的に計画し、整理しておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="538f9-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="538f9-120">1 つの案は、文字または数字の接頭語や接尾辞を使用して、タイプを区別することです。</span><span class="sxs-lookup"><span data-stu-id="538f9-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="538f9-121">たとえば、1-xxxxx をチャンネルの価格グループに、2-xxxxx をカタログの価格グループに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="538f9-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="538f9-122">4 つの照会ページが提供され、関連付いた割引がある可能性のある Commerce エンティティーをそれぞれ表示します。</span><span class="sxs-lookup"><span data-stu-id="538f9-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="538f9-123">**チャネル チャネルの価格グループ** – このページには、それぞれの価格グループにリンクされているチャンネルと割引の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="538f9-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="538f9-124">**カタログの価格グループ** ー このページには、それぞれの価格グループにリンクされているカタログと割引の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="538f9-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="538f9-125">**ロイヤルティーの価格グループ** ー このページには、それぞれの価格グループにリンクされているロイヤルティー プログラムと割引の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="538f9-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="538f9-126">**加盟者の価格グループ** ー このページには、それぞれの価格グループにリンクされている加盟者と割引の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="538f9-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="538f9-127">チャンネルの割引設定の例</span><span class="sxs-lookup"><span data-stu-id="538f9-127">Example channel discount set up</span></span>

<span data-ttu-id="538f9-128">次の例は、チャンネル割引の設定に関連するタスクについて説明したものです。</span><span class="sxs-lookup"><span data-stu-id="538f9-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="538f9-129">この例では、**ヒューストン** というチャネルがあり、新しい割引 **新学期** を作成しようとしています。</span><span class="sxs-lookup"><span data-stu-id="538f9-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="538f9-130">価格と割引の戦略にはチャンネル割引が含まれる可能性があるため、チャンネル作成時には常に特定チャンネルの価格グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="538f9-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="538f9-131">**ヒューストンPG** という価格グループがあり、チャンネル **ヒューストン** に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="538f9-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="538f9-132">新しい割引 **新学期** を作成した後、**割引** ページの上部にある **価格グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="538f9-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="538f9-133">**割引価格グループ** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="538f9-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="538f9-134">次に、**新規** をクリックして、価格グループ **ヒューストンPG** を選択します。</span><span class="sxs-lookup"><span data-stu-id="538f9-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="538f9-135">これで、割引を有効にして、チャンネルにプッシュすることができます。</span><span class="sxs-lookup"><span data-stu-id="538f9-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="538f9-136">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="538f9-136">Additional resources</span></span>

[<span data-ttu-id="538f9-137">価格調整と割引</span><span class="sxs-lookup"><span data-stu-id="538f9-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]