---
title: "チャンネル固有の割引の定義"
description: "小売業者は、多くの場合、異なるチャンネルのさまざまな割引を設定します。 このトピックでは、特定のチャンネルの割引を作成するために知っておく必要のある概念を確認します。"
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0300ed4a10f6979fb673447323f7fdf61041529f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="define-channel-specific-discounts"></a><span data-ttu-id="b0dc0-104">チャンネル固有の割引の定義</span><span class="sxs-lookup"><span data-stu-id="b0dc0-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0dc0-105">小売業者は、多くの場合、異なるチャンネルのさまざまな割引を設定します。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-105">Retailers often set different discounts in different channels.</span></span> <span data-ttu-id="b0dc0-106">このトピックでは、特定のチャンネルの割引を作成するために知っておく必要のある概念を確認します。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-106">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span> 

<a name="channel-specific-discounts"></a><span data-ttu-id="b0dc0-107">チャンネル固有の割引</span><span class="sxs-lookup"><span data-stu-id="b0dc0-107">Channel-specific discounts</span></span>
--------------------------

<span data-ttu-id="b0dc0-108">小売業者は、多くの場合、異なるチャンネルでさまざまな割引を提供します。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-108">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="b0dc0-109">それらは、国内市場の状況に合わせて行われたり、競合の小売業者に対処するために行われる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-109">This is may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="b0dc0-110">Microsoft Dynamics 365 for Retail は、価格グループを使用して、チャンネル固有の割引を定義します。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-110">Microsoft Dynamics 365 for Retail uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="b0dc0-111">価格グループは、次のエンティティーの 1 つ以上に割り当てることができます: チャンネル、カタログ、加盟者、ロイヤルティー プログラム。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-111">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="b0dc0-112">この記事ではチャンネルについて説明しますが、カタログ割引、加盟者割引、ロイヤルティー割引に対しても同じ概念が適用できます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-112">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="b0dc0-113">価格グループ</span><span class="sxs-lookup"><span data-stu-id="b0dc0-113">Price groups</span></span>

<span data-ttu-id="b0dc0-114">[![価格グループ](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="b0dc0-114">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="b0dc0-115">上記の図は、トランザクションで扱うことができるエンティティ (チャンネル、カタログ、加盟者、顧客、ロイヤルティ カード) とさまざまな設定可能な割引との間の関係を説明しています。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-115">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="b0dc0-116">すべてのトランザクションはチャンネルで発生するため、あるトランザクションに対してチャンネルが存在することが保証されます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-116">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="b0dc0-117">残りのエンティティーはオプションです。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-117">The remaining entities are optional.</span></span> <span data-ttu-id="b0dc0-118">各マスター データ ページには、関連する価格グループのページへのリンクがあり、必要に応じて価格グループを表示および追加できます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-118">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="b0dc0-119">価格グループを使用すると、4 つの異なるエンティティ タイプを、割引、価格調整、売買契約に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-119">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="b0dc0-120">価格グループの名前の付け方を戦略的に計画し、整理しておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-120">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="b0dc0-121">1 つの案は、文字または数字の接頭語や接尾辞を使用して、タイプを区別することです。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-121">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="b0dc0-122">たとえば、1-xxxxx をチャンネルの価格グループに、2-xxxxx をカタログの価格グループに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-122">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="b0dc0-123">4 つの照会ページが提供され、関連付いた割引がある可能性のある小売エンティティーをそれぞれ表示します。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-123">There are four inquiry pages that focus on each of the retail entities that can have discounts associated to them.</span></span>

-   <span data-ttu-id="b0dc0-124">**小売チャンネルの価格グループ** - このページには、それぞれの価格グループにリンクされているチャンネルと割引の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-124">**Retail channel price groups** - This page shows a list of channels and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="b0dc0-125">**カタログの価格グループ** - このページには、それぞれの価格グループにリンクされているカタログと割引の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-125">**Catalog price groups** - This page shows a list of catalogs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="b0dc0-126">**ロイヤルティーの価格グループ** - このページには、それぞれの価格グループにリンクされているロイヤルティー プログラムと割引の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-126">**Loyalty price groups** - This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="b0dc0-127">**加盟者の価格グループ** - このページには、それぞれの価格グループにリンクされている加盟者と割引の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-127">**Affiliation price groups** - This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="b0dc0-128">チャンネルの割引設定の例</span><span class="sxs-lookup"><span data-stu-id="b0dc0-128">Example channel discount set up</span></span>
<span data-ttu-id="b0dc0-129">次の例は、チャンネル割引の設定に関連するタスクについて説明したものです。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-129">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1.  <span data-ttu-id="b0dc0-130">この例では、**ヒューストン**というチャンネルがあり、新しい割引**新学期**を作成しようとしています。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-130">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School.**</span></span>
2.  <span data-ttu-id="b0dc0-131">価格と割引の戦略にはチャンネル割引が含まれる可能性があるため、チャンネル作成時には常に特定チャンネルの価格グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-131">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3.  <span data-ttu-id="b0dc0-132">**ヒューストンPG**という価格グループがあり、チャンネル**ヒューストン**に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-132">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4.  <span data-ttu-id="b0dc0-133">新しい割引**新学期**を作成した後、**割引**ページの上部にある**価格グループ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-133">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="b0dc0-134">**割引価格グループ**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-134">The **Discount price groups** page will open.</span></span> <span data-ttu-id="b0dc0-135">次に、**新規**をクリックして、価格グループ**ヒューストンPG**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-135">Next, click **New** and select the **Houston-PG** price group.</span></span>
5.  <span data-ttu-id="b0dc0-136">これで、割引を有効にして、チャンネルにプッシュすることができます。</span><span class="sxs-lookup"><span data-stu-id="b0dc0-136">Now you can enable the discount and push it to the channel.</span></span>



<a name="additional-resources"></a><span data-ttu-id="b0dc0-137">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="b0dc0-137">Additional resources</span></span>
--------

[<span data-ttu-id="b0dc0-138">価格調整と割引</span><span class="sxs-lookup"><span data-stu-id="b0dc0-138">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)




