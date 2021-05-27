---
title: オンライン注文の税金が間違って計算される
description: このトピックでは、オンライン注文の税金が間違って計算された場合、または販売明細行の税グループが正しく設定されていない場合に役立つトラブルシューティング ガイドを示します。
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
ms.openlocfilehash: f7cef533d76bdddfbad2e8c5f84f81ef62bccc38
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021106"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="b0936-103">オンライン注文の税金が間違って計算される</span><span class="sxs-lookup"><span data-stu-id="b0936-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0936-104">このトピックでは、オンライン注文の税金が間違って計算された場合、または販売明細行の税グループが正しく設定されていない場合に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="b0936-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="b0936-105">説明</span><span class="sxs-lookup"><span data-stu-id="b0936-105">Description</span></span>

<span data-ttu-id="b0936-106">eコマース注文が行われると、税金が正しく計算されていないか、販売明細行の税グループが正しく設定されていません。</span><span class="sxs-lookup"><span data-stu-id="b0936-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="b0936-107">解像度</span><span class="sxs-lookup"><span data-stu-id="b0936-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="b0936-108">Commerce 本社で小売店舗の消費税を構成する</span><span class="sxs-lookup"><span data-stu-id="b0936-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="b0936-109">Commerce 本社で小売店舗の消費税を構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b0936-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b0936-110">**Retail と Commerce \> チャネル \> すべての店舗** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0936-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="b0936-111">消費税を構成する店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0936-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="b0936-112">**一般** クイックタブの **消費税** セクションで、店舗の消費税情報を構成します。</span><span class="sxs-lookup"><span data-stu-id="b0936-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="b0936-113">店舗からの製品集荷の場合、税グループは、集荷用に選択された店舗から取得されます。</span><span class="sxs-lookup"><span data-stu-id="b0936-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="b0936-114">詳細については、[店舗のほかの税オプションの設定](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0936-114">For more information, see [Set other tax options for stores](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="b0936-115">Commerce 本社で顧客の住所の消費税を構成する</span><span class="sxs-lookup"><span data-stu-id="b0936-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="b0936-116">Commerce 本社で顧客の住所の消費税を構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b0936-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b0936-117">**売掛金勘定 \> 顧客 \> すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0936-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="b0936-118">消費税を構成する対象の顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0936-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="b0936-119">**住所** クイックタブで、消費税を構成する対象の住所を選択し、**詳細オプション** を選択して、**詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0936-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="b0936-120">**一般** クイックタブで、**税グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0936-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="b0936-121">**消費税** フィールドで、適切な値を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0936-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="b0936-122">顧客の住所で消費税がかかる出荷の場合、その明細行の配送先住所により、その明細行の税グループが決まります。</span><span class="sxs-lookup"><span data-stu-id="b0936-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="b0936-123">顧客が既に構成されている税グループがある既存の住所に出荷する場合は、既存の税グループが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0936-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="b0936-124">既定では、住所には作成時に税グループがありません。</span><span class="sxs-lookup"><span data-stu-id="b0936-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="b0936-125">Commerce 本社の一般的な消費税グループの構成</span><span class="sxs-lookup"><span data-stu-id="b0936-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="b0936-126">Commerce 本社で一般的な消費税グループを構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b0936-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b0936-127">**税 \> 間接税 \> 売上税 \> 消費税グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0936-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="b0936-128">左のナビゲーションで、構成する税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b0936-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="b0936-129">**小売の宛先に基づく税** クイックタブで、消費税グループの税金を構成します。</span><span class="sxs-lookup"><span data-stu-id="b0936-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="b0936-130">顧客の住所で消費税がかからない出荷の場合、税グループに対して構成されている明細行の配送先住所と宛先に基づく税によって、税グループが決まります。</span><span class="sxs-lookup"><span data-stu-id="b0936-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="b0936-131">詳細については、[宛先に基づくオンライン ストアのための税の設定](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0936-131">For more information, see [Set up taxes for online stores based on destination](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0936-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b0936-132">Additional resources</span></span>

[<span data-ttu-id="b0936-133">オンライン注文用の消費税のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b0936-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)