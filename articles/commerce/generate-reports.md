---
title: オンライン チャネル レポートの生成
description: このトピックでは、Microsoft Dynamics 365 Commerce でオンライン チャネルのレポートを生成する方法について説明します。
author: psimolin
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 80d62b29fcc95a3153c604512e1ee6b3e55ba840
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019790"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="b7454-103">オンライン チャネル レポートの生成</span><span class="sxs-lookup"><span data-stu-id="b7454-103">Generate online channel reports</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b7454-104">このトピックでは、Microsoft Dynamics 365 Commerce でオンライン チャネルのレポートを生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b7454-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b7454-105">Commerce では、複数のレポートを生成および表示して、オンライン チャネルの実行状況を確認できます。</span><span class="sxs-lookup"><span data-stu-id="b7454-105">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="b7454-106">チャネル集計レポート</span><span class="sxs-lookup"><span data-stu-id="b7454-106">Channel summary report</span></span>

<span data-ttu-id="b7454-107">**チャネル集計** レポートには、選択したチャネルの次のトランザクションの集計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7454-107">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="b7454-108">販売トランザクション</span><span class="sxs-lookup"><span data-stu-id="b7454-108">Sales transactions</span></span>
- <span data-ttu-id="b7454-109">支払トランザクション</span><span class="sxs-lookup"><span data-stu-id="b7454-109">Payment transactions</span></span>
- <span data-ttu-id="b7454-110">税トランザクション</span><span class="sxs-lookup"><span data-stu-id="b7454-110">Tax transactions</span></span>
- <span data-ttu-id="b7454-111">割引トランザクション</span><span class="sxs-lookup"><span data-stu-id="b7454-111">Discounted transactions</span></span>

<span data-ttu-id="b7454-112">**チャネル集計** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b7454-112">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="b7454-113">**Retail と Commerce\> 照会とレポート\>売上レポート\>チャネル集計レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7454-113">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="b7454-114">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-114">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-115">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-115">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-116">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-116">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b7454-117">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-117">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="b7454-118">年別チャネル売上レポート</span><span class="sxs-lookup"><span data-stu-id="b7454-118">Channel sales by year report</span></span> 

<span data-ttu-id="b7454-119">**年別チャネル売上レポート** には、特定の店舗における前年比売上の比較が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7454-119">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="b7454-120">売上を比較する年度を選択すると、レポートは選択した年度の売上と前年度の売上を比較します。</span><span class="sxs-lookup"><span data-stu-id="b7454-120">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="b7454-121">**年別チャネル売上** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b7454-121">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="b7454-122">**Retail と Commerce\> 照会とレポート\>売上レポート\>年別チャネル売上レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7454-122">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="b7454-123">**開始暦年** のフィールドに、年を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-123">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="b7454-124">**終了暦年** のフィールドに、年を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-124">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="b7454-125">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-125">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b7454-126">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-126">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="b7454-127">時間別チャネル売上レポート</span><span class="sxs-lookup"><span data-stu-id="b7454-127">Channel sales by hour report</span></span>

<span data-ttu-id="b7454-128">**時間別チャネル売上** レポートには、選択したチャネルまたは作業単位の時間あたりの販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7454-128">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="b7454-129">**時間別チャネル売上** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b7454-129">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="b7454-130">**Retail と Commerce\> 照会とレポート\>売上レポート\>時間別チャネル売上レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7454-130">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="b7454-131">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-131">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-132">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-132">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-133">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-133">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b7454-134">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-134">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="b7454-135">上位の顧客レポート</span><span class="sxs-lookup"><span data-stu-id="b7454-135">Top customers report</span></span>

<span data-ttu-id="b7454-136">**上位の顧客** レポートには、選択したチャネルまたは作業単位の上位 *N* 顧客の販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7454-136">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="b7454-137">値 *N* は 10 ~ 100 の数値で、ユーザーが選択した集計測定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b7454-137">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="b7454-138">**上位の顧客** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b7454-138">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="b7454-139">**Retail と Commerce\> 照会とレポート\>売上レポート\>上位の顧客レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7454-139">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="b7454-140">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-140">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-141">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-141">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-142">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-142">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b7454-143">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-143">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="b7454-144">上位割引レポート</span><span class="sxs-lookup"><span data-stu-id="b7454-144">Top discounts report</span></span>

<span data-ttu-id="b7454-145">**上位割引** レポートには、選択したチャネルまたは作業単位の上位 *N* 割引の販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7454-145">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="b7454-146">値 *N* は 10 ~ 100 の数値で、ユーザーが選択した集計測定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b7454-146">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="b7454-147">**上位割引** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b7454-147">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="b7454-148">**Retail と Commerce\> 照会とレポート\>売上レポート\>上位割引レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7454-148">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="b7454-149">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-149">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-150">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-150">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-151">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-151">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b7454-152">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-152">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="b7454-153">上位製品レポート</span><span class="sxs-lookup"><span data-stu-id="b7454-153">Top products report</span></span>

<span data-ttu-id="b7454-154">**上位製品** レポートには、選択したチャネルまたは作業単位の上位 *N* 製品の販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7454-154">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="b7454-155">値 *N* は 10 ~ 100 の数値で、ユーザーが選択した集計測定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b7454-155">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="b7454-156">**上位製品** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b7454-156">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="b7454-157">**Retail と Commerce\> 照会とレポート\>売上レポート\>上位製品レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7454-157">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="b7454-158">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-158">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-159">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-159">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-160">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-160">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b7454-161">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-161">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="b7454-162">カテゴリ売上レポート</span><span class="sxs-lookup"><span data-stu-id="b7454-162">Category sales report</span></span>

<span data-ttu-id="b7454-163">**カテゴリ売上** レポートには、選択されたチャネルまたは作業単位のカテゴリ階層の各ノードについて、選択した期間における販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7454-163">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="b7454-164">**カテゴリ売上** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b7454-164">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="b7454-165">**Retail と Commerce\> 照会およびレポート\>売上レポート\>カテゴリ売上レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7454-165">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="b7454-166">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-166">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-167">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-167">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-168">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-168">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="b7454-169">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-169">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="b7454-170">組織売上レポート</span><span class="sxs-lookup"><span data-stu-id="b7454-170">Organization sales report</span></span>

<span data-ttu-id="b7454-171">**組織売上** レポートには、組織単位ごとに店舗のパフォーマンスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7454-171">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="b7454-172">このレポートには、店舗ごとの販売数量と金額、および各店舗の利益率が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b7454-172">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="b7454-173">組織単位は、既定のレポート階層に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b7454-173">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="b7454-174">**組織売上** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b7454-174">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="b7454-175">**Retail と Commerce\> 照会およびレポート\>売上レポート\>組織売上レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7454-175">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="b7454-176">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-176">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-177">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7454-177">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="b7454-178">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7454-178">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7454-179">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b7454-179">Additional resources</span></span>

- [<span data-ttu-id="b7454-180">Commerce のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="b7454-180">Commerce home page</span></span>](./index.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]