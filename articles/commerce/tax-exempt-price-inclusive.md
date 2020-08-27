---
title: 非課税の計算
description: このトピックでは、販売時点管理 (POS) およびコール センターでの非課税計算の機能について説明します。
author: rubendel
manager: annbe
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 936609fbc19a9bbd52bf100d2737bf37e53e5233
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621426"
---
# <a name="calculation-of-tax-exemption"></a><span data-ttu-id="b735c-103">非課税の計算</span><span class="sxs-lookup"><span data-stu-id="b735c-103">Calculation of tax exemption</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b735c-104">このトピックでは、販売時点管理 (POS) およびコール センターでの非課税計算の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="b735c-104">This topic describes functionality for tax exemption calculations in the point of sale (POS) and call center.</span></span>

## <a name="key-terms"></a><span data-ttu-id="b735c-105">重要な用語</span><span class="sxs-lookup"><span data-stu-id="b735c-105">Key terms</span></span>

| <span data-ttu-id="b735c-106">期間</span><span class="sxs-lookup"><span data-stu-id="b735c-106">Term</span></span> | <span data-ttu-id="b735c-107">説明</span><span class="sxs-lookup"><span data-stu-id="b735c-107">Description</span></span> |
|---|---|
| <span data-ttu-id="b735c-108">B2B</span><span class="sxs-lookup"><span data-stu-id="b735c-108">B2B</span></span> | <span data-ttu-id="b735c-109">"企業間" の略称。</span><span class="sxs-lookup"><span data-stu-id="b735c-109">An abbreviation for "business to business."</span></span> <span data-ttu-id="b735c-110">小売業者と個人間の売上ではなく、企業間の売上を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b735c-110">It's used to indicate sales between businesses, as opposed to sales between a retailer and an individual.</span></span> |
| <span data-ttu-id="b735c-111">VAT</span><span class="sxs-lookup"><span data-stu-id="b735c-111">VAT</span></span> | <span data-ttu-id="b735c-112">製品の価格に含まれる付加価値税。</span><span class="sxs-lookup"><span data-stu-id="b735c-112">Value-added tax that is included in the price of a product.</span></span> |

## <a name="adjust-prices-for-tax-exemptions-when-the-price-includes-tax"></a><span data-ttu-id="b735c-113">税込み価格の場合に非課税の価格を調整する</span><span class="sxs-lookup"><span data-stu-id="b735c-113">Adjust prices for tax exemptions when the price includes tax</span></span>

<span data-ttu-id="b735c-114">Microsoft Dynamics 365 Commerce バージョン 10.0.13 以降には、**非課税を含む価格の計算**オプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b735c-114">Microsoft Dynamics 365 Commerce version 10.0.13 and later include a **Calculate price inclusive tax exempt** option.</span></span> <span data-ttu-id="b735c-115">このオプションを**はい**に設定すると、トランザクション内のトランザクションまたは特定の税を控除する必要がある場合に、内税シナリオの価格が調整されます。</span><span class="sxs-lookup"><span data-stu-id="b735c-115">If this option is set to **Yes**, prices in tax-inclusive scenarios are adjusted when the transaction or specific taxes in the transaction should be exempted.</span></span> <span data-ttu-id="b735c-116">店舗ベースの税を使用する場合は、税の上書きを使用してこれらの控除を適用できます。</span><span class="sxs-lookup"><span data-stu-id="b735c-116">When store-based taxes are used, you can apply these exemptions by using tax overrides.</span></span> <span data-ttu-id="b735c-117">店舗で顧客ベースの税が使用されている場合、顧客の税設定に基づいて自動的に控除が適用されます。</span><span class="sxs-lookup"><span data-stu-id="b735c-117">When customer-based taxes are used at the store, the exemptions are automatically applied based on the customer's tax settings.</span></span>

<span data-ttu-id="b735c-118">この設定は、コール センターまたは店舗で作成された注文でもサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b735c-118">This setting is also supported for orders that are created in the call center and stores.</span></span>

![非課税シナリオで価格を調整するための、非課税を含む価格の計算オプションの設定](media/CalcPriceInc.png)

## <a name="set-up-price-reductions-for-tax-exemptions"></a><span data-ttu-id="b735c-120">非課税の価格下方修正を設定する</span><span class="sxs-lookup"><span data-stu-id="b735c-120">Set up price reductions for tax exemptions</span></span>

<span data-ttu-id="b735c-121">次の手順は、デモ データ シナリオでこの機能をテストする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b735c-121">The following steps show how to test this capability in demo data scenarios.</span></span> <span data-ttu-id="b735c-122">他のデータ セットの設定手順も同様です。</span><span class="sxs-lookup"><span data-stu-id="b735c-122">The setup steps for other data sets are similar.</span></span>

1. <span data-ttu-id="b735c-123">**小売とコマース** \> **チャネル** \> **店舗** \> **すべての店舗**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b735c-123">Go to **Retail and Commerce** \> **Channels** \> **Stores** \> **All stores**.</span></span>
2. <span data-ttu-id="b735c-124">**サンフランシスコ**の店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-124">Select the **San Francisco** store.</span></span> <span data-ttu-id="b735c-125">店舗の詳細を開くには、店舗用**小売チャネル ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-125">To open the store details, select the **Retail Channel Id** value for the store.</span></span>
3. <span data-ttu-id="b735c-126">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-126">Select **Edit**.</span></span>
4. <span data-ttu-id="b735c-127">**全般**クイック タブで、**非課税を含む価格の計算**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b735c-127">On the **General** FastTab, set the **Calculate price inclusive tax exempt** option to **Yes**.</span></span>
5. <span data-ttu-id="b735c-128">**税込価格**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b735c-128">Set the **Price includes tax** option to **Yes**.</span></span>
6. <span data-ttu-id="b735c-129">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-129">Select **Save**.</span></span>
7. <span data-ttu-id="b735c-130">検索フィールドに**売上税グループ**を入力して、**売上税グループ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b735c-130">Enter **Sales tax groups** in the search field to open the **Sales tax groups** page.</span></span>
8. <span data-ttu-id="b735c-131">**新規**を選択し、売上税グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b735c-131">Select **New**, and enter a name for the sales tax group.</span></span>
9. <span data-ttu-id="b735c-132">**設定**クイック タブで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-132">On the **Setup** FastTab, select **Add**.</span></span>
10. <span data-ttu-id="b735c-133">**売上税コード**列のドロップダウン リストで、**RP\_CAST** を選択してから、**控除**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-133">On the drop-down list in the **Sales tax code** column, select **RP\_CAST**, and then select the **Exempt** check box.</span></span>
11. <span data-ttu-id="b735c-134">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-134">Select **Save**.</span></span>
12. <span data-ttu-id="b735c-135">検索フィールドに**売上税の上書き**を入力して、**売上税の上書き**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b735c-135">Enter **Sales tax overrides** in the search field to open the **Sales tax overrides** page.</span></span>
13. <span data-ttu-id="b735c-136">**新規**を選択し、売上税の上書きの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b735c-136">Select **New**, and enter a name for the sales tax override.</span></span>
14. <span data-ttu-id="b735c-137">ステータスを**有効にする**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b735c-137">Set the status to **Enable**.</span></span>
15. <span data-ttu-id="b735c-138">**上書きタイプ** フィールドで、**売上税グループ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-138">In the **Override type** field, select **Sales tax group**.</span></span>
16. <span data-ttu-id="b735c-139">**上書き元**フィールドで、**すべての税グループ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-139">In the **From** field, select **Any tax group**.</span></span>
17. <span data-ttu-id="b735c-140">**ターゲット** フィールドで、**指定した税グループ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-140">In the **To** field, select **Specified tax group**.</span></span>
18. <span data-ttu-id="b735c-141">**上書き元税グループ** フィールドで、**CA** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-141">In the **From tax group** field, select **CA**.</span></span>
19. <span data-ttu-id="b735c-142">**上書き先税グループ** フィールドで、前に作成した売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-142">In the **To tax group** field, select the sales tax group that created earlier.</span></span>
20. <span data-ttu-id="b735c-143">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-143">Select **Save**.</span></span>
21. <span data-ttu-id="b735c-144">検索フィールドに**売上税の上書きグループ**を入力して、**売上税の上書きグループ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b735c-144">Enter **Sales tax override groups** in the search field to open the **Sales tax override groups** page.</span></span>
22. <span data-ttu-id="b735c-145">**既定**のグループを選択してから、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-145">Select the **Default** group, and then select **Edit**.</span></span>
23. <span data-ttu-id="b735c-146">**追加**を選択してから、前に作成した売上税の上書きを選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-146">Select **Add**, and then select the sales tax override that you created earlier.</span></span>
24. <span data-ttu-id="b735c-147">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-147">Select **Save**.</span></span>
25. <span data-ttu-id="b735c-148">検索ボックスに**配送スケジュール**を入力して、**配送スケジュール** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b735c-148">Enter **Distribution schedules** in the search box to open the **Distribution schedules** page.</span></span>
26. <span data-ttu-id="b735c-149">スケジュール ジョブ **9999** を選択してから、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-149">Select schedule job **9999**, and then select **Run now**.</span></span>
27. <span data-ttu-id="b735c-150">ジョブの同期が完了したら、POS を開きます。</span><span class="sxs-lookup"><span data-stu-id="b735c-150">When the jobs have completed synchronization, open the POS.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b735c-151">チャネルの税の詳細がキャッシュされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b735c-151">Tax details for the channel might be cached.</span></span> <span data-ttu-id="b735c-152">次に、販売時点管理アプリケーションを閉じて再起動し、チャネル データベースとの同期が完了した後の変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="b735c-152">Then close the point of sale application and relaunch it to to observe the changes after they have synchronized to the channel database.</span></span>

28. <span data-ttu-id="b735c-153">品目 **91050** をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="b735c-153">Add item **91050** to a transaction.</span></span>
29. <span data-ttu-id="b735c-154">**税の上書き**を選択してから、**取引税の上書き**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-154">Select **Tax overrides**, and then select **Override transaction tax**.</span></span>
30. <span data-ttu-id="b735c-155">前に作成した売上税の上書きを選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-155">Select the sales tax override that you created earlier.</span></span> <span data-ttu-id="b735c-156">税額は 0 (ゼロ) に引き下げられ、明細行品目の価格は非課税を反映して引き下げられます。</span><span class="sxs-lookup"><span data-stu-id="b735c-156">The tax is reduced to 0 (zero), and the price for the line items is reduced to reflect the tax exemption.</span></span>

<span data-ttu-id="b735c-157">または、**顧客ベースの税を使用する**オプションを**はい**に設定してから、顧客に直接作成する売上税グループを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="b735c-157">Alternatively, you can set the **Use customer based tax** option for the store to **Yes** and then assign the sales tax group that you create directly to the customer.</span></span> <span data-ttu-id="b735c-158">その後、顧客がトランザクションに追加されるときに、顧客の非課税ステータスを反映するように価格が引き下げられます。</span><span class="sxs-lookup"><span data-stu-id="b735c-158">Then, when the customer is added to a transaction, the prices are reduced to reflect that customer's tax-exempt status.</span></span>

### <a name="check-customers-for-exemptions-when-tax-is-exclusive-of-price"></a><span data-ttu-id="b735c-159">外税価格の場合に、控除がある顧客を確認する</span><span class="sxs-lookup"><span data-stu-id="b735c-159">Check customers for exemptions when tax is exclusive of price</span></span>

<span data-ttu-id="b735c-160">酒屋などの一部の小売業種では、商品を現金売りトランザクションで個人およびその他の企業に販売します。</span><span class="sxs-lookup"><span data-stu-id="b735c-160">Some retail verticals, such as liquor stores, sell goods to individuals and other businesses in cash-and-carry transactions.</span></span> <span data-ttu-id="b735c-161">ただし、多くの場合、異なる顧客区分を含むトランザクションには課税目的の異なる要件があります。</span><span class="sxs-lookup"><span data-stu-id="b735c-161">However, in many cases, transactions that involve different customer segments have different requirements for taxation purposes.</span></span> <span data-ttu-id="b735c-162">たとえば、酒屋が一部の企業に商品を販売する場合、販売される品目に通常関連付けられている売上税は、これらの特定の企業に対して控除される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b735c-162">For example, when a liquor store sells goods to some businesses, sales taxes that are usually associated with the items that are sold might be exempt for those specific businesses.</span></span> <span data-ttu-id="b735c-163">ただし、それ以外の場合は、通常の売上税が適用されます。</span><span class="sxs-lookup"><span data-stu-id="b735c-163">However, in all other cases, regular sales tax should apply.</span></span>

<span data-ttu-id="b735c-164">このシナリオをサポートするには、店舗の**顧客の非課税計算**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b735c-164">To support this scenario, set the **Calculate customer tax exempt** option for the store to **Yes**.</span></span> <span data-ttu-id="b735c-165">その後、トランザクションに顧客を追加すると、POS はその顧客に適用できる税額をチェックします。</span><span class="sxs-lookup"><span data-stu-id="b735c-165">Then, when a customer is added to a transaction, the POS checks the taxes that are applicable to that customer.</span></span> <span data-ttu-id="b735c-166">顧客の税設定に**非課税**としてマークされている税コードが含まれているが、税額がトランザクションに適用される場合、税額はトランザクションの非課税と見なされ、トランザクションに追加されません。</span><span class="sxs-lookup"><span data-stu-id="b735c-166">If the customer's tax settings have a tax code that is marked as **Exempt**, but tax is applicable to the transaction, the tax is treated as exempt for the transaction and isn't added to the transaction.</span></span>

<span data-ttu-id="b735c-167">**顧客の非課税計算**オプションは、価格に税が含まれない店舗に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b735c-167">The **Calculate customer tax exempt** option applies to stores where the price doesn't include tax.</span></span> <span data-ttu-id="b735c-168">店舗の**宛先に基づく税を使用**オプションが**はい**に設定されている場合にも、非課税計算がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b735c-168">The exemption calculation is also supported if the **Use destination based tax** option for the store is set to **Yes**.</span></span>

### <a name="set-up-tax-exemption-calculations-for-customers"></a><span data-ttu-id="b735c-169">顧客の非課税計算を設定する</span><span class="sxs-lookup"><span data-stu-id="b735c-169">Set up tax exemption calculations for customers</span></span>

<span data-ttu-id="b735c-170">次の手順は、デモ データ シナリオでこの機能をテストする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b735c-170">The following steps show how to test this capability in demo data scenarios.</span></span> <span data-ttu-id="b735c-171">他のデータ セットの設定手順も同様です。</span><span class="sxs-lookup"><span data-stu-id="b735c-171">The setup steps for other data sets are similar.</span></span>

1. <span data-ttu-id="b735c-172">**小売とコマース** \> **チャネル** \> **店舗** \> **すべての店舗**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b735c-172">Go to **Retail and Commerce** \> **Channels** \> **Stores** \> **All stores**.</span></span>
2. <span data-ttu-id="b735c-173">**サンフランシスコ**の店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-173">Select the **San Francisco** store.</span></span> <span data-ttu-id="b735c-174">店舗の詳細を開くには、店舗用**小売チャネル ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-174">To open the store details, select the **Retail Channel Id** value for the store.</span></span>
3. <span data-ttu-id="b735c-175">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-175">Select **Edit**.</span></span>
4. <span data-ttu-id="b735c-176">**全般**クイック タブで、**顧客の非課税計算**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b735c-176">On the **General** FastTab, set the **Calculate customer tax exempt** option to **Yes**.</span></span>
5. <span data-ttu-id="b735c-177">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-177">Select **Save**.</span></span>
6. <span data-ttu-id="b735c-178">検索フィールドに**売上税グループ**を入力して、**売上税グループ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b735c-178">Enter **Sales tax groups** in the search field to open the **Sales tax groups** page.</span></span>
7. <span data-ttu-id="b735c-179">**新規**を選択し、売上税グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b735c-179">Select **New**, and enter a name for the sales tax group.</span></span>
8. <span data-ttu-id="b735c-180">**設定**クイック タブで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-180">On the **Setup** FastTab, select **Add**.</span></span>
9. <span data-ttu-id="b735c-181">**売上税コード**列のドロップダウン リストで、**RP\_CAST** を選択してから、**控除**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-181">On the drop-down list in the **Sales tax code** column, select **RP\_CAST**, and then select the **Exempt** check box.</span></span>
10. <span data-ttu-id="b735c-182">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-182">Select **Save**.</span></span>
11. <span data-ttu-id="b735c-183">**小売とコマース** \> **すべての顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b735c-183">Go to **Retail and Commerce** \> **All customers**.</span></span>
12. <span data-ttu-id="b735c-184">**Matthew Tolley** のアカウント ID **004009** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-184">Select account ID **004009** for **Matthew Tolley**.</span></span>
13. <span data-ttu-id="b735c-185">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-185">Select **Edit**.</span></span>
14. <span data-ttu-id="b735c-186">**請求書と出荷**クイック タブの、**売上税グループ** フィールドで、先に作成した売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-186">On the **Invoice and delivery** FastTab, in the **Sales tax group** field, select the sales tax group that you created earlier.</span></span>
15. <span data-ttu-id="b735c-187">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-187">Select **Save**.</span></span>
16. <span data-ttu-id="b735c-188">検索フィールドに**配送スケジュール**を入力して、**配送スケジュール** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b735c-188">Enter **Distribution schedules** in the search field to open the **Distribution schedules** page.</span></span>
17. <span data-ttu-id="b735c-189">スケジュール ジョブ **9999** を選択してから、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b735c-189">Select schedule job **9999**, and then select **Run now**.</span></span>
18. <span data-ttu-id="b735c-190">ジョブの同期が完了したら、POS を開きます。</span><span class="sxs-lookup"><span data-stu-id="b735c-190">When the jobs have completed synchronization, open the POS.</span></span>
19. <span data-ttu-id="b735c-191">品目 **91050** をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="b735c-191">Add item **91050** to a transaction.</span></span> <span data-ttu-id="b735c-192">予定されている合計金額は **$75.06** です。</span><span class="sxs-lookup"><span data-stu-id="b735c-192">The total that is due is **$75.06**.</span></span>
20. <span data-ttu-id="b735c-193">**Matthew Tolley** をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="b735c-193">Add **Matthew Tolley** to the transaction.</span></span> <span data-ttu-id="b735c-194">この顧客の控除を反映するように税額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="b735c-194">Taxes are recalculated to reflect this customer's exemption.</span></span>
