---
title: オンライン チャネル レポートの生成
description: このトピックでは、Microsoft Dynamics 365 Commerce でオンライン チャネルのレポートを生成する方法について説明します。
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58342f07233e3c6a6e6a1af87ab23513ad63caf5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970045"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="c6a0c-103">オンライン チャネル レポートの生成</span><span class="sxs-lookup"><span data-stu-id="c6a0c-103">Generate online channel reports</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c6a0c-104">このトピックでは、Microsoft Dynamics 365 Commerce でオンライン チャネルのレポートを生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c6a0c-105">概要</span><span class="sxs-lookup"><span data-stu-id="c6a0c-105">Overview</span></span>

<span data-ttu-id="c6a0c-106">Commerce では、複数のレポートを生成および表示して、オンライン チャネルの実行状況を確認できます。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-106">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="c6a0c-107">チャネル集計レポート</span><span class="sxs-lookup"><span data-stu-id="c6a0c-107">Channel summary report</span></span>

<span data-ttu-id="c6a0c-108">**チャネル集計** レポートには、選択したチャネルの次のトランザクションの集計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="c6a0c-109">販売トランザクション</span><span class="sxs-lookup"><span data-stu-id="c6a0c-109">Sales transactions</span></span>
- <span data-ttu-id="c6a0c-110">支払トランザクション</span><span class="sxs-lookup"><span data-stu-id="c6a0c-110">Payment transactions</span></span>
- <span data-ttu-id="c6a0c-111">税トランザクション</span><span class="sxs-lookup"><span data-stu-id="c6a0c-111">Tax transactions</span></span>
- <span data-ttu-id="c6a0c-112">割引トランザクション</span><span class="sxs-lookup"><span data-stu-id="c6a0c-112">Discounted transactions</span></span>

<span data-ttu-id="c6a0c-113">**チャネル集計** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="c6a0c-114">**Retail と Commerce\> 照会とレポート\>売上レポート\>チャネル集計レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-114">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="c6a0c-115">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-116">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-117">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="c6a0c-118">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="c6a0c-119">年別チャネル売上レポート</span><span class="sxs-lookup"><span data-stu-id="c6a0c-119">Channel sales by year report</span></span> 

<span data-ttu-id="c6a0c-120">**年別チャネル売上レポート** には、特定の店舗における前年比売上の比較が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="c6a0c-121">売上を比較する年度を選択すると、レポートは選択した年度の売上と前年度の売上を比較します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="c6a0c-122">**年別チャネル売上** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="c6a0c-123">**Retail と Commerce\> 照会とレポート\>売上レポート\>年別チャネル売上レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-123">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="c6a0c-124">**開始暦年** のフィールドに、年を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="c6a0c-125">**終了暦年** のフィールドに、年を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="c6a0c-126">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="c6a0c-127">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="c6a0c-128">時間別チャネル売上レポート</span><span class="sxs-lookup"><span data-stu-id="c6a0c-128">Channel sales by hour report</span></span>

<span data-ttu-id="c6a0c-129">**時間別チャネル売上** レポートには、選択したチャネルまたは作業単位の時間あたりの販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="c6a0c-130">**時間別チャネル売上** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="c6a0c-131">**Retail と Commerce\> 照会とレポート\>売上レポート\>時間別チャネル売上レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-131">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="c6a0c-132">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-133">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-134">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="c6a0c-135">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="c6a0c-136">上位の顧客レポート</span><span class="sxs-lookup"><span data-stu-id="c6a0c-136">Top customers report</span></span>

<span data-ttu-id="c6a0c-137">**上位の顧客** レポートには、選択したチャネルまたは作業単位の上位 *N* 顧客の販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="c6a0c-138">値 *N* は 10 ~ 100 の数値で、ユーザーが選択した集計測定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="c6a0c-139">**上位の顧客** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="c6a0c-140">**Retail と Commerce\> 照会とレポート\>売上レポート\>上位の顧客レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-140">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="c6a0c-141">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-142">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-143">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="c6a0c-144">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="c6a0c-145">上位割引レポート</span><span class="sxs-lookup"><span data-stu-id="c6a0c-145">Top discounts report</span></span>

<span data-ttu-id="c6a0c-146">**上位割引** レポートには、選択したチャネルまたは作業単位の上位 *N* 割引の販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="c6a0c-147">値 *N* は 10 ~ 100 の数値で、ユーザーが選択した集計測定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="c6a0c-148">**上位割引** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="c6a0c-149">**Retail と Commerce\> 照会とレポート\>売上レポート\>上位割引レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-149">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="c6a0c-150">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-151">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-152">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="c6a0c-153">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="c6a0c-154">上位製品レポート</span><span class="sxs-lookup"><span data-stu-id="c6a0c-154">Top products report</span></span>

<span data-ttu-id="c6a0c-155">**上位製品** レポートには、選択したチャネルまたは作業単位の上位 *N* 製品の販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="c6a0c-156">値 *N* は 10 ~ 100 の数値で、ユーザーが選択した集計測定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="c6a0c-157">**上位製品** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="c6a0c-158">**Retail と Commerce\> 照会とレポート\>売上レポート\>上位製品レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-158">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="c6a0c-159">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-160">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-161">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="c6a0c-162">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="c6a0c-163">カテゴリ売上レポート</span><span class="sxs-lookup"><span data-stu-id="c6a0c-163">Category sales report</span></span>

<span data-ttu-id="c6a0c-164">**カテゴリ売上** レポートには、選択されたチャネルまたは作業単位のカテゴリ階層の各ノードについて、選択した期間における販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="c6a0c-165">**カテゴリ売上** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="c6a0c-166">**Retail と Commerce\> 照会およびレポート\>売上レポート\>カテゴリ売上レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-166">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="c6a0c-167">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-168">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-169">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="c6a0c-170">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="c6a0c-171">組織売上レポート</span><span class="sxs-lookup"><span data-stu-id="c6a0c-171">Organization sales report</span></span>

<span data-ttu-id="c6a0c-172">**組織売上** レポートには、組織単位ごとに店舗のパフォーマンスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-172">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="c6a0c-173">このレポートには、店舗ごとの販売数量と金額、および各店舗の利益率が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="c6a0c-174">組織単位は、既定のレポート階層に基づいています。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="c6a0c-175">**組織売上** レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="c6a0c-176">**Retail と Commerce\> 照会およびレポート\>売上レポート\>組織売上レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-176">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="c6a0c-177">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-178">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="c6a0c-179">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6a0c-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6a0c-180">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c6a0c-180">Additional resources</span></span>

- [<span data-ttu-id="c6a0c-181">Commerce のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="c6a0c-181">Commerce home page</span></span>](../retail/index.md)
