---
title: オンライン チャネル レポートの生成
description: このトピックでは、Microsoft Dynamics 365 Retail でオンライン チャネルのレポートを生成する方法について説明します。
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 77737c134df8f3ba598fe9026fa7c01ca9976733
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698053"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="73d01-103">オンライン チャネル レポートの生成</span><span class="sxs-lookup"><span data-stu-id="73d01-103">Generate online channel reports</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="73d01-104">このトピックでは、Microsoft Dynamics 365 Retail でオンライン チャネルのレポートを生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="73d01-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="73d01-105">概要</span><span class="sxs-lookup"><span data-stu-id="73d01-105">Overview</span></span>

<span data-ttu-id="73d01-106">Retail では、複数のレポートを生成および表示して、オンライン チャネルの実行状況を確認できます。</span><span class="sxs-lookup"><span data-stu-id="73d01-106">You can generate and view several reports in Retail to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="73d01-107">チャネル集計レポート</span><span class="sxs-lookup"><span data-stu-id="73d01-107">Channel summary report</span></span>

<span data-ttu-id="73d01-108">**チャネル集計**レポートには、選択したチャネルの次のトランザクションの集計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d01-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="73d01-109">販売トランザクション</span><span class="sxs-lookup"><span data-stu-id="73d01-109">Sales transactions</span></span>
- <span data-ttu-id="73d01-110">支払トランザクション</span><span class="sxs-lookup"><span data-stu-id="73d01-110">Payment transactions</span></span>
- <span data-ttu-id="73d01-111">税トランザクション</span><span class="sxs-lookup"><span data-stu-id="73d01-111">Tax transactions</span></span>
- <span data-ttu-id="73d01-112">割引トランザクション</span><span class="sxs-lookup"><span data-stu-id="73d01-112">Discounted transactions</span></span>

<span data-ttu-id="73d01-113">**チャネル集計**レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73d01-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="73d01-114">**小売\>照会とレポート\>売上レポート\>チャネル集計レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="73d01-114">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="73d01-115">**開始日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-116">**終了日**フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-117">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="73d01-118">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="73d01-119">年別チャネル売上レポート</span><span class="sxs-lookup"><span data-stu-id="73d01-119">Channel sales by year report</span></span> 

<span data-ttu-id="73d01-120">**年別チャネル売上レポート**には、特定の店舗における前年比売上の比較が表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d01-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="73d01-121">売上を比較する年度を選択すると、レポートは選択した年度の売上と前年度の売上を比較します。</span><span class="sxs-lookup"><span data-stu-id="73d01-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="73d01-122">**年別チャネル売上**レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73d01-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="73d01-123">**小売\>照会とレポート\>売上レポート\>年別チャネル売上レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="73d01-123">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="73d01-124">**開始暦年**のフィールドに、年を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="73d01-125">**終了暦年**のフィールドに、年を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="73d01-126">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="73d01-127">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="73d01-128">時間別チャネル売上レポート</span><span class="sxs-lookup"><span data-stu-id="73d01-128">Channel sales by hour report</span></span>

<span data-ttu-id="73d01-129">**時間別チャネル売上**レポートには、選択したチャネルまたは作業単位の時間あたりの販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d01-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="73d01-130">**時間別チャネル売上**レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73d01-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="73d01-131">**小売\>照会とレポート\>売上レポート\>時間別チャネル売上レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="73d01-131">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="73d01-132">**開始日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-133">**終了日**フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-134">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="73d01-135">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="73d01-136">上位の顧客レポート</span><span class="sxs-lookup"><span data-stu-id="73d01-136">Top customers report</span></span>

<span data-ttu-id="73d01-137">**上位の顧客**レポートには、選択したチャネルまたは作業単位の上位 *N* 顧客の販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d01-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="73d01-138">値 *N* は 10 ~ 100 の数値で、ユーザーが選択した集計測定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="73d01-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="73d01-139">**上位の顧客**レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73d01-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="73d01-140">**小売\>照会とレポート\>売上レポート\>上位の顧客レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="73d01-140">Go to **Retail \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="73d01-141">**開始日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-142">**終了日**フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-143">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="73d01-144">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="73d01-145">上位割引レポート</span><span class="sxs-lookup"><span data-stu-id="73d01-145">Top discounts report</span></span>

<span data-ttu-id="73d01-146">**上位割引**レポートには、選択したチャネルまたは作業単位の上位 *N* 割引の販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d01-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="73d01-147">値 *N* は 10 ~ 100 の数値で、ユーザーが選択した集計測定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="73d01-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="73d01-148">**上位割引**レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73d01-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="73d01-149">**小売\>照会とレポート\>売上レポート\>上位割引レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="73d01-149">Go to **Retail \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="73d01-150">**開始日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-151">**終了日**フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-152">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="73d01-153">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="73d01-154">上位製品レポート</span><span class="sxs-lookup"><span data-stu-id="73d01-154">Top products report</span></span>

<span data-ttu-id="73d01-155">**上位製品**レポートには、選択したチャネルまたは作業単位の上位 *N* 製品の販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d01-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="73d01-156">値 *N* は 10 ~ 100 の数値で、ユーザーが選択した集計測定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="73d01-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="73d01-157">**上位製品**レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73d01-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="73d01-158">**小売\>照会とレポート\>売上レポート\>上位製品レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="73d01-158">Go to **Retail \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="73d01-159">**開始日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-160">**終了日**フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-161">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="73d01-162">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="73d01-163">カテゴリ売上レポート</span><span class="sxs-lookup"><span data-stu-id="73d01-163">Category sales report</span></span>

<span data-ttu-id="73d01-164">**カテゴリ売上**レポートには、選択されたチャネルまたは作業単位のカテゴリ階層の各ノードについて、選択した期間における販売メトリックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d01-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="73d01-165">**カテゴリ売上**レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73d01-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="73d01-166">**小売 \> 照会およびレポート \> 販売レポート \> カテゴリ売上レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="73d01-166">Go to **Retail \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="73d01-167">**開始日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-168">**終了日**フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-169">**チャネル** フィールドで、オンライン チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="73d01-170">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="73d01-171">組織売上レポート</span><span class="sxs-lookup"><span data-stu-id="73d01-171">Organization sales report</span></span>

<span data-ttu-id="73d01-172">**組織売上**レポートには、組織単位ごとに小売店舗のパフォーマンスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d01-172">The **Organization sales** report shows the performance of your retail stores by organization unit.</span></span> <span data-ttu-id="73d01-173">このレポートには、店舗ごとの販売数量と金額、および各店舗の利益率が含まれます。</span><span class="sxs-lookup"><span data-stu-id="73d01-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="73d01-174">組織単位は、既定のレポート階層に基づいています。</span><span class="sxs-lookup"><span data-stu-id="73d01-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="73d01-175">**組織売上**レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="73d01-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="73d01-176">**小売 \> 照会およびレポート \> 販売レポート \> 組織売上レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="73d01-176">Go to **Retail \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="73d01-177">**開始日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-178">**終了日**フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73d01-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="73d01-179">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73d01-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73d01-180">追加リソース</span><span class="sxs-lookup"><span data-stu-id="73d01-180">Additional resources</span></span>

- [<span data-ttu-id="73d01-181">Dynamics 365 Retail のヘルプ リソース</span><span class="sxs-lookup"><span data-stu-id="73d01-181">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)