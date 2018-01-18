--- 
title: "ロイヤルティ スキーマの定義"
description: "この手順は、ロイヤルティ スキームの定義方法を説明します。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 3c3efa665f99c80c79543ea880359db814f92bff
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="define-loyalty-schemes"></a><span data-ttu-id="9cb16-103">ロイヤルティ スキーマの定義</span><span class="sxs-lookup"><span data-stu-id="9cb16-103">Define loyalty schemes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9cb16-104">この手順は、ロイヤルティ スキームの定義方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-104">This procedure walks through how to define a loyalty scheme.</span></span> <span data-ttu-id="9cb16-105">ロイヤルティ スキームは、ロイヤルティ プログラムの報酬取得および報酬償還ルールです。</span><span class="sxs-lookup"><span data-stu-id="9cb16-105">Loyalty schemes are reward earning and redeeming rules for a loyalty program.</span></span> <span data-ttu-id="9cb16-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="9cb16-107">[小売りとコマース] > [顧客] > [ロイヤルティ] > [ロイヤルティ スキーム] に移動します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-107">Go to Retail and commerce > Customers > Loyalty > Loyalty schemes.</span></span>
2. <span data-ttu-id="9cb16-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-108">Click New.</span></span>
3. <span data-ttu-id="9cb16-109">[スキーム ID] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-109">In the Scheme ID field, type a value.</span></span>
4. <span data-ttu-id="9cb16-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9cb16-111">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9cb16-111">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9cb16-112">ロイヤルティ プログラムの複数のロイヤルティ スキームを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9cb16-112">You can have multiple loyalty schemes for a loyalty program.</span></span> <span data-ttu-id="9cb16-113">ロイヤルティ スキームは、すべてのチャンネルまたはチャンネルのサブセットだけでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="9cb16-113">Loyalty schemes can be for all channels or only a sub-set of channels.</span></span>  
6. <span data-ttu-id="9cb16-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9cb16-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9cb16-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-116">Click Save.</span></span>
9. <span data-ttu-id="9cb16-117">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-117">Click Add line.</span></span>
10. <span data-ttu-id="9cb16-118">[活動タイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-118">In the Activity type field, select an option.</span></span>
    * <span data-ttu-id="9cb16-119">消費金額に基づいて顧客が報酬を取得する場合は、[金額別の製品購買] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-119">Select Purchase products by amount if you want customers to earn rewards based on how much they spend.</span></span> <span data-ttu-id="9cb16-120">購買数量に基づいて顧客が報酬を取得する場合は、[数量別の製品購買] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-120">Select Purchase products by quantity if you want customers to earn rewards based on how many products they buy.</span></span>  <span data-ttu-id="9cb16-121">何をどれだけ購入したかに関係なく、顧客が各販売トランザクションに対して報酬を取得する場合、[販売トランザクション カウント] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-121">Select Sales transaction count if you want customers to earn rewards for each sales transaction, regardless of what or how much is purchased.</span></span>  
    * <span data-ttu-id="9cb16-122">カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-122">Select a category.</span></span> <span data-ttu-id="9cb16-123">カテゴリはこの所得ルールが適用される製品を制限します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-123">The category will limit which products this earning rule applies to.</span></span>  
    * <span data-ttu-id="9cb16-124">所得ルールをすべての製品に適用する場合は、このフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-124">If you want the earning rule to apply to all products, leave this field blank.</span></span>  
11. <span data-ttu-id="9cb16-125">[活動金額 / 数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-125">In the Activity amount/quantity field, enter a number.</span></span>
    *  <span data-ttu-id="9cb16-126">[販売トランザクション カウント] の活動タイプに、「1.0」という値を常に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cb16-126">For activity type Sales transaction count, you should always use a value of '1.0'.</span></span> <span data-ttu-id="9cb16-127">[金額別の購入] または [数量別の購入] の活動タイプでは、トランザクションがその入力値より小さい場合、取得ルールが発生しません。</span><span class="sxs-lookup"><span data-stu-id="9cb16-127">For activity types of Purchase by amount or Purchase by quantity, any transaction that is less than the value entered will not trigger the earning rule.</span></span> <span data-ttu-id="9cb16-128">たとえば、活動タイプが [金額別の購入] で「10.00」と入力した場合、「9.00」の販売トランザクションでは、この取得ルールの報酬を取得できません。</span><span class="sxs-lookup"><span data-stu-id="9cb16-128">For example, if the activity type is Purchase by amount, and you enter '10.00', then a sales transaction for '9.00' will not earn rewards for this earning rule.</span></span>  
12. <span data-ttu-id="9cb16-129">[活動の通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-129">In the Activity currency field, type a value.</span></span>
13. <span data-ttu-id="9cb16-130">[報酬ポイント ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9cb16-130">In the Reward point ID field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="9cb16-131">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-131">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="9cb16-132">[報酬ポイント] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-132">In the Reward points field, enter a number.</span></span>
    * <span data-ttu-id="9cb16-133">金額タイプの報酬ポイントは、小数点以下を含む取得した金額を記録します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-133">Amount type reward points will record earned amounts with decimals.</span></span> <span data-ttu-id="9cb16-134">たとえば、取得ルールが 1 カナダ ドルの支払いごとに 1 報酬ポイントの取得と規定する場合、顧客が 1.25 カナダ ドルを支払うと、顧客は 1.25 報酬ポイントを取得することになります。</span><span class="sxs-lookup"><span data-stu-id="9cb16-134">For example, if the earning rule states 1 reward point earned for every 1 Canadian Dollar spent, and the customer spends 1.25 Canadian Dollars, then the customer will earn 1.25 reward points.</span></span> <span data-ttu-id="9cb16-135">数量タイプの報酬ポイントは、取得した金額を整数で記録します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-135">Quantity type reward points will record earned amounts in integers.</span></span> <span data-ttu-id="9cb16-136">この例では、取得ルールが 1 カナダ ドルの支払いごとに 1 報酬ポイントの取得と規定する場合、顧客が 1.25 カナダ ドルを支払うと、顧客は 1.0 報酬ポイントを取得することになります。</span><span class="sxs-lookup"><span data-stu-id="9cb16-136">Using the example where the earning rule states 1 reward point earned for every 1 Canadian Dollar spent, and the customer spends 1.25 Canadian Dollars, then the customer will earn 1.0 reward points.</span></span>  
16. <span data-ttu-id="9cb16-137">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-137">Click Save.</span></span>
17. <span data-ttu-id="9cb16-138">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-138">Click Add line.</span></span>
    * <span data-ttu-id="9cb16-139">償還ルールは、ロイヤルティ支払方法を使うときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="9cb16-139">Redemption rules are used when the loyalty payment method is used.</span></span>  
18. <span data-ttu-id="9cb16-140">[報酬ポイント ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9cb16-140">In the Reward point ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9cb16-141">引換可能な報酬ポイントのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9cb16-141">Only redeemable reward points are shown.</span></span>  
19. <span data-ttu-id="9cb16-142">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-142">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="9cb16-143">[報酬ポイント] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-143">In the Reward points field, enter a number.</span></span>
21. <span data-ttu-id="9cb16-144">[償還タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-144">In the Redemption type field, select an option.</span></span>
    * <span data-ttu-id="9cb16-145">金額別支払を選択すると、通貨の値として扱われる金額または数量フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9cb16-145">Selecting Payment by amount causes the Amount or quantity field to be treated as a currency value.</span></span> <span data-ttu-id="9cb16-146">この場合、支払通貨単位ごとに使用される報酬ポイントの金額は、固定比率です。</span><span class="sxs-lookup"><span data-stu-id="9cb16-146">In this case, the amount of reward points used per currency unit of payment is a fixed ratio.</span></span> <span data-ttu-id="9cb16-147">[数量別支払] を選択すると、数量の値として扱われる [金額または数量] フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9cb16-147">Selecting Payment by quantity causes the Amount or quantity field to be treated as a quantity value.</span></span> <span data-ttu-id="9cb16-148">この場合、品目数量ごとの報酬ポイントの金額は固定比率ですが、ロイヤルティ報酬ポイントによって支払われる品目の価格が同じ数量に対して変わるならば、通貨金額も異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9cb16-148">In this case, the amount of reward points used per item quantity is a fixed ratio, however, the amount in currency can vary if the price of items paid for with loyalty reward points varies for the same quantity.</span></span> <span data-ttu-id="9cb16-149">ロイヤルティ ポイント割引の償還タイプは、「ロシア」などの国 / 地域の固有機能であるコンフィギュレーション キーが有効で、POS 機能プロファイルに「RU」などの ISO コードがある場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="9cb16-149">Redemption type of Loyalty points discount is only valid when the 'Russia' Country/Regional specific features configuration key is enabled, and the POS functionality profiles has an ISO code of 'RU'.</span></span>  
    * <span data-ttu-id="9cb16-150">カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-150">Select a category.</span></span> <span data-ttu-id="9cb16-151">カテゴリはこの償還ルールが適用される製品を制限します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-151">The category will limit which products this redemption rule applies to.</span></span>  
    * <span data-ttu-id="9cb16-152">償還ルールをすべての製品に適用する場合は、このフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-152">If you want the redemption rule to apply to all products, leave this field blank.</span></span>  
22. <span data-ttu-id="9cb16-153">[金額または数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-153">In the Amount or quantity field, enter a number.</span></span>
23. <span data-ttu-id="9cb16-154">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cb16-154">In the Currency field, type a value.</span></span>
24. <span data-ttu-id="9cb16-155">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-155">Click Save.</span></span>
25. <span data-ttu-id="9cb16-156">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-156">Click Add line.</span></span>
    * <span data-ttu-id="9cb16-157">利用可能な組織ノード リストから一つ以上のノードを選択して、選択した組織ノード リストへ移動させるには、2 つのリスト間で矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-157">Select one or more nodes from the Available organization nodes list and move them to the Selected organization nodes list by clicking the arrow between the two lists.</span></span>  
26. <span data-ttu-id="9cb16-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-158">Click OK.</span></span>
27. <span data-ttu-id="9cb16-159">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cb16-159">Click Save.</span></span>
    * <span data-ttu-id="9cb16-160">ロイヤルティ スキームのチャンネルを変更する場合は、ロイヤルティ スキーム プロセスを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cb16-160">Anytime you change the channels for a loyalty scheme, you must run Process loyalty schemes.</span></span> <span data-ttu-id="9cb16-161">この方法で、チャンネルは更新されたロイヤルティ スキームを取得できます。</span><span class="sxs-lookup"><span data-stu-id="9cb16-161">That way, the channels will get updated loyalty schemes.</span></span>  


