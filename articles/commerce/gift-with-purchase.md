---
title: 購入プロモーションでギフトを構成する
description: このトピックでは、Microsoft Dynamics 365 Commerce で「ギフトと購入」プロモーションを構成する方法について説明します 。
author: shalabh
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: v-chgri
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e3776ef0b746074a869fa65af486be0f33bbbbb8
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937548"
---
# <a name="configure-gift-with-purchase-promotions"></a><span data-ttu-id="5e566-103">購入プロモーションでギフトを構成する</span><span class="sxs-lookup"><span data-stu-id="5e566-103">Configure gift with purchase promotions</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="5e566-104">このトピックでは、Microsoft Dynamics 365 Commerce で「ギフトと購入」プロモーションを構成する方法について説明します 。</span><span class="sxs-lookup"><span data-stu-id="5e566-104">This topic describes how to configure "gift with purchase" promotions in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5e566-105">「ギフトと購入」のプロモーションを実行することは、小売業者の間で一般的な方法です。</span><span class="sxs-lookup"><span data-stu-id="5e566-105">It's a common practice among retailers to run "gift with purchase" promotions.</span></span> <span data-ttu-id="5e566-106">目標は、追加品目に対する無料または割引の特典を提供することにより、顧客が製品を定価で購入するように説得することです。</span><span class="sxs-lookup"><span data-stu-id="5e566-106">The goal is to persuade customers to buy a product at full price by offering a bonus of an additional item for free or at a discount.</span></span> <span data-ttu-id="5e566-107">これらのプロモーションは、移動の遅い製品の販売に役立ち、(正しく実行されている場合)、全体的なカスタマー エクスペリエンスの向上にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5e566-107">These promotions can help sell slow-moving products and (if they are run correctly) can also help improve the overall customer experience.</span></span> <span data-ttu-id="5e566-108">Dynamics 365 Commerce バージョン 10.0.19 リリース移行、小売業者「しきい値割引」機能を使用して、これらのプロモーション を構成できます。</span><span class="sxs-lookup"><span data-stu-id="5e566-108">As of the Dynamics 365 Commerce version 10.0.19 release, retailers can use the "Threshold discount" feature to configure these promotions.</span></span>

## <a name="threshold-discount-feature"></a><span data-ttu-id="5e566-109">しきい値割引機能</span><span class="sxs-lookup"><span data-stu-id="5e566-109">Threshold discount feature</span></span>

<span data-ttu-id="5e566-110">Commerce Version 10.0.19 のリリース以降、コマース本社 (**Retail と Commerce \> 価格決定と割引 \> しきい値割引**) で **しきい値割引** ページの **しきい値層** クイック タブの **割引方法** フィールドで新しい **割引明細行** 値を選択できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5e566-110">As of the Commerce version 10.0.19 release, a new **Discount lines** value is available for selection in the **Discount method** field on the **Threshold discount tiers** FastTab of the **Threshold discounts** page in Commerce headquarters (**Retail and Commerce \> Pricing and discounts \> Threshold discounts**).</span></span> <span data-ttu-id="5e566-111">**割引明細行** 割引方法が選択されている場合は、**しきい値割引明細行** という名前の新しいクイック タブがページの下部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e566-111">If the **Discount lines** discount method is selected, a new FastTab that is named **Threshold discount lines** appears at the bottom of the page.</span></span> 

<span data-ttu-id="5e566-112">**しきい値割引** ページの **明細行** クイック タブに一覧表示される品目は、プロモーションの対象品目と見なす必要がありますが、**しきい値割明細行** クイック タブに一覧表示されている品目は割引品目と見なす必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e566-112">The items that are listed on the **Lines** FastTab of the **Threshold discounts** page should be considered the qualifying items for a promotion, whereas the items that are listed on the **Threshold discount lines** FastTab should be considered the discounted items.</span></span> <span data-ttu-id="5e566-113">**明細行** クイック タブで指定されたしきい値は、しきい値に達しているかどうかを判断するために、特定の明細行と比較して確認されます。</span><span class="sxs-lookup"><span data-stu-id="5e566-113">The threshold amount that is specified on the **Lines** FastTab is checked against the qualifying lines to determine whether the threshold has been met.</span></span> <span data-ttu-id="5e566-114">しきい値に達した場合、割引は **しきい値割引明細行** クイック タブに一覧表示されている品目に適用されます。</span><span class="sxs-lookup"><span data-stu-id="5e566-114">If the threshold is met, the discount is applied to the items that are listed on the **Threshold discount lines** FastTab.</span></span> 

## <a name="promotion-configuration-examples"></a><span data-ttu-id="5e566-115">プロモーション コンフィギュレーションの例</span><span class="sxs-lookup"><span data-stu-id="5e566-115">Promotion configuration examples</span></span>

<span data-ttu-id="5e566-116">**しきい値割引明細行** クイック タブの **数量制限** のフィールドを使用して、しきい値に達したときにに割引する品目の数を指定 (したがって制限) できます。</span><span class="sxs-lookup"><span data-stu-id="5e566-116">You can use the **Quantity limit** field on the **Threshold discount lines** FastTab to specify (and therefore limit) the number of items that should be discounted when the threshold is met.</span></span> <span data-ttu-id="5e566-117">たとえば、ドレス シャツに 200 ドルを費やした顧客が、2 つのネクタイを無料で入手できるプロモーションを実行するとします。</span><span class="sxs-lookup"><span data-stu-id="5e566-117">For example, you want to run a promotion where customers who spend $200 on dress shirts get two ties for free.</span></span> <span data-ttu-id="5e566-118">**しきい値割引明細行** クイック タブで、新しいしきい値割引層を作成します。</span><span class="sxs-lookup"><span data-stu-id="5e566-118">On the **Threshold discount lines** FastTab, you create a new threshold discount tier.</span></span> <span data-ttu-id="5e566-119">**金額** フィールドに **200.00** と入力し、**割引方法** フィールドで **割引明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e566-119">You enter **200.00** in the **Amount** field and select **Discount lines** in the **Discount method** field.</span></span> <span data-ttu-id="5e566-120">次に、**明細行** クイック タブで **ドレス シャツ** カテゴリを選択して、対象品目を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e566-120">Next, on the **Lines** FastTab, you select the **Dress Shirts** category to specify the qualifying items.</span></span> <span data-ttu-id="5e566-121">**しきい値割引明細行** クイック タブで **ネクタイ** カテゴリを選択して、割引品目を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e566-121">On the **Threshold discount lines** FastTab, you select the **Ties** category to specify the discounted items.</span></span> <span data-ttu-id="5e566-122">最後に、**ネクタイ** カテゴリの場合、**契約価格/割引率** フィールドに **100.00** と入力して、価格を 100％ 引き下げます。また、**数量制限** フィールドに **2.00** と入力して、割引品目の数を最大 2 つの品目に制限します。</span><span class="sxs-lookup"><span data-stu-id="5e566-122">Finally, for the **Ties** category, you enter **100.00** in the **Deal price/Discount percent** field to take 100 percent off the price, and you enter **2.00** in the **Quantity limit** field to limit the number of discounted items to a maximum of two items.</span></span> <span data-ttu-id="5e566-123">現在、合計 $200 を超えるドレス シャツがトランザクションに追加され、一部のネクタイもトランザクションに追加されると、最大 2 つのネクタイが無料で顧客に提供されます。</span><span class="sxs-lookup"><span data-stu-id="5e566-123">Now, when dress shirts that total more than $200 are added to a transaction, and some ties are also added to the transaction, up to two ties will be provided to the customer for free.</span></span> 

<span data-ttu-id="5e566-124">次の図は、Commerce 本社での「ドレス シャツに $200 を費やし、2 つのネクタイを無料で入手する」プロモーションの例の構成を示しています。</span><span class="sxs-lookup"><span data-stu-id="5e566-124">The following illustration shows the configuration for the "spend $200 on dress shirts and get two ties for free" promotion example in Commerce headquarters.</span></span> 

![Commerce 本社での購入例の構成を含むギフト](./media/gift-with-purchase.png)

<span data-ttu-id="5e566-126">前述のように、**しきい値割引明細行** クイック タブの **数量制限** のフィールドを使用して、割引する必要のある品目の数を制限できます。</span><span class="sxs-lookup"><span data-stu-id="5e566-126">As has been mentioned, the **Quantity limit** field on the **Threshold discount lines** FastTab lets you to limit the number of items that should be discounted.</span></span> <span data-ttu-id="5e566-127">このフィールドが **0.00** に設定されている場合、割引できる品目の数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="5e566-127">If this field is set to **0.00**, there is no limit on the number of items that can be discounted.</span></span> <span data-ttu-id="5e566-128">したがって、前の例では、**ネクタイ** カテゴリの **数量制限** フィールドが **0.00** に設定されている場合、特定のしきい値を満たす顧客は、任意の数のネクタイを無料で入手できます。</span><span class="sxs-lookup"><span data-stu-id="5e566-128">Therefore, for the previous example, if the **Quantity limit** field for the **Ties** category is set to **0.00**, customers who meet the qualifying threshold can get any number of ties for free.</span></span> 

<span data-ttu-id="5e566-129">複数の品目を **しきい値割引明細行** クイック タブに追加して、割引する必要のある品目を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="5e566-129">You can add multiple items to the **Threshold discount lines** FastTab to indicate the items that should be discounted.</span></span> <span data-ttu-id="5e566-130">前の例では、2 つのネクタイに 1 つの行を追加し、2 つの蝶ネクタイに別の行を追加すると、システムはこの構成を「ドレス シャツに $200 を費やし、2 つのネクタイ *と* 2 つの蝶ネクタイを無料で入手する」と解釈します。</span><span class="sxs-lookup"><span data-stu-id="5e566-130">For the previous example, if you add one row for two ties and another row for two bow ties, the system will interpret this configuration as "spend $200 on dress shirts, and get two ties *and* two bow ties for free."</span></span> <span data-ttu-id="5e566-131">プロモーションで代わりに 2 つのネクタイ *または* 2 つの蝶ネクタイ (または 1 つのネクタイと 1 つの蝶ネクタイ) を無料で提供する必要がある場合は、ネクタイと蝶ネクタイの新しいカテゴリを作成して、ネクタイと蝶ネクタイの割引を 1 つの行に構成できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e566-131">If the promotion should instead involve giving two ties *or* two bow ties for free (or one tie and one bow tie), you must create a new category for ties and bow ties, so that the tie and bow tie discounts can be configured on a single row.</span></span>

## <a name="view-available-discounts-feature"></a><span data-ttu-id="5e566-132">使用可能な割引機能の表示</span><span class="sxs-lookup"><span data-stu-id="5e566-132">View available discounts feature</span></span>

<span data-ttu-id="5e566-133">「使用可能な割引の表示」機能は、販売担当者や顧客が、販売時点管理 (POS) で、トランザクションが無料または割引対象の品目の対象であることを知るのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5e566-133">The "View available discounts" feature helps sales associates and customers learn, at the point of sale (POS), that a transaction has qualified for free or discounted items.</span></span> <span data-ttu-id="5e566-134">この機能は、特定のトランザクションに適用できるべての割引を表示します。</span><span class="sxs-lookup"><span data-stu-id="5e566-134">This feature shows all applicable discounts for a given transaction.</span></span> <span data-ttu-id="5e566-135">「使用可能な割引の表示」機能の詳細については、 [割引を使用したクロスセルとアップセル](discounts-pos.md#cross-sell-and-upsell-by-using-discounts) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e566-135">For more information about the "View available discounts" feature, see [Cross-sell and upsell by using discounts](discounts-pos.md#cross-sell-and-upsell-by-using-discounts).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e566-136">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5e566-136">Additional resources</span></span>

[<span data-ttu-id="5e566-137">割引を使用したクロスセルとアップセル</span><span class="sxs-lookup"><span data-stu-id="5e566-137">Cross-sell and upsell by using discounts</span></span>](discounts-pos.md#cross-sell-and-upsell-by-using-discounts)

