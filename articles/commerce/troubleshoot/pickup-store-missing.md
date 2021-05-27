---
title: 選択した店舗の一覧に小売店舗が表示されません
description: このトピックでは、店舗の一覧に小売店舗が表示されない場合に役立つトラブルシューティングガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020829"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="5b1e9-103">選択した店舗の一覧に小売店舗が表示されません</span><span class="sxs-lookup"><span data-stu-id="5b1e9-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b1e9-104">このトピックでは、店舗の一覧に小売店舗が表示されない場合に役立つトラブルシューティングガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="5b1e9-105">説明</span><span class="sxs-lookup"><span data-stu-id="5b1e9-105">Description</span></span>

<span data-ttu-id="5b1e9-106">店舗の一覧に商品を受け取ることができる小売店舗は、表示されません。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="5b1e9-107">解像度</span><span class="sxs-lookup"><span data-stu-id="5b1e9-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="5b1e9-108">Commerce 本社の店舗住所の経度と緯度を構成します</span><span class="sxs-lookup"><span data-stu-id="5b1e9-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="5b1e9-109">Commerce 本社の店舗住所の経度と緯度を構成するには次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5b1e9-110">**Retail と Commerce \> チャンネル \> 店舗 \> すべての店舗** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="5b1e9-111">eコマース サイトの集荷オプションの中から表示する店舗を検索します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="5b1e9-112">**作業単位数** 値をメモします。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="5b1e9-113">**組織管理 \> 組織 \> 作業単位** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="5b1e9-114">以前にメモした作業単位番号を検索し、検索結果の作業単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="5b1e9-115">**住所** クイック タブで、**その他のオプション** を選択し、**詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="5b1e9-116">**一般** クイック タブで、**経度** フィールドと **緯度** フィールドが正しく設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="5b1e9-117">この手順の一環として、値が正または負の数として正しく指定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="5b1e9-118">Commerce 本社でのフルフィルメント グループを構成します</span><span class="sxs-lookup"><span data-stu-id="5b1e9-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="5b1e9-119">Commerce 本社でフルフィルメント グループを構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5b1e9-120">**Retail と Commerce \> チャネル \> オンライン ストア** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="5b1e9-121">構成するオンライン ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="5b1e9-122">アクション ペインで、**設定** を選択し、**フルフィルメント グループの割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="5b1e9-123">**フルフィルメント グループの割り当て** ページで、オンラインストアのフルフィルメント グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="5b1e9-124">**設定** で、フルフィルメント グループに対して小売店舗が正しく構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b1e9-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b1e9-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5b1e9-125">Additional resources</span></span> 

[<span data-ttu-id="5b1e9-126">作業単位の作成</span><span class="sxs-lookup"><span data-stu-id="5b1e9-126">Create an operating unit</span></span>](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[<span data-ttu-id="5b1e9-127">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="5b1e9-127">Set up an online channel</span></span>](../channel-setup-online.md)