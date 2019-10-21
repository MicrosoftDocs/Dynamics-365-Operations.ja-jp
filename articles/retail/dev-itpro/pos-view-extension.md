---
title: POS ビューの拡張によるカスタム列およびアプリ バー ボタンの追加
description: このトピックでは、[顧客の追加/編集] 画面などの既存の POS ビューを拡張する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 08/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 24411
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-11-22
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 796b2c2aeddc333ac7b594db25fd88fc467c22e3
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023456"
---
# <a name="extend-pos-views-to-add-custom-columns-and-app-bar-buttons"></a><span data-ttu-id="1ade2-103">POS ビューの拡張によるカスタム列およびアプリ バー ボタンの追加</span><span class="sxs-lookup"><span data-stu-id="1ade2-103">Extend POS views to add custom columns and app bar buttons</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ade2-104">このトピックでは、既存の [販売時点管理 (POS)] ビューを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-104">This topic explains how you can extend existing point of sale (POS) views.</span></span> <span data-ttu-id="1ade2-105">**トランザクション** 画面および **ようこそ** 画面を拡張するには、画面レイアウト デザイナーを使用します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-105">To extend the **Transaction** screen and **Welcome** screen, you can use the screen layout designer.</span></span> <span data-ttu-id="1ade2-106">**顧客の追加/編集** 画面など、他のすべての POS ビューを拡張するには、Retail ソフトウェア開発キット (SDK) を使用します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-106">To extend all other POS views, such as the **Customer Add/Edit** screen, you use the Retail software development kit (SDK).</span></span> <span data-ttu-id="1ade2-107">このトピックでは、Retail SDK による既存の POS ビューの拡張について説明します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-107">This topic focuses on the extension of existing POS views via the Retail SDK.</span></span>



<span data-ttu-id="1ade2-108">POS ビューでは、次の拡張ポイントとパターンがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="1ade2-108">POS views support the following extension points and patterns:</span></span>

- <span data-ttu-id="1ade2-109">**カスタム アプリケーション バーのボタン** - 選択したページのアプリケーション バーにカスタム ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-109">**Custom app bar buttons** – Add custom buttons to the app bar on selected pages.</span></span>
- <span data-ttu-id="1ade2-110">**カスタム列セット** - 選択したページのグリッド列をカスタム列に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="1ade2-110">**Custom column sets** – Replace the grid columns with custom columns on selected pages.</span></span>
- <span data-ttu-id="1ade2-111">**カスタム コントロール** - 選択したページに、新しいコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-111">**Custom controls** – Add new controls to selected pages.</span></span>

## <a name="pos-views-that-currently-support-extensions"></a><span data-ttu-id="1ade2-112">現在拡張機能をサポートする POS ビュー</span><span class="sxs-lookup"><span data-stu-id="1ade2-112">POS views that currently support extensions</span></span>

<span data-ttu-id="1ade2-113">次のテーブルに、現在拡張機能をサポートしている POS ビューを示します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-113">The following table shows the POS views that currently support extensions.</span></span> <span data-ttu-id="1ade2-114">また、各 POS ビューがサポートする拡張ポイントのタイプも示します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-114">It also indicates the types of extension points that each POS view supports.</span></span>

> [!NOTE]
> <span data-ttu-id="1ade2-115">今後のリリースと修正プログラムで、他のビューの拡張ポイントをさらにサポートします。</span><span class="sxs-lookup"><span data-stu-id="1ade2-115">The upcoming releases and hotfix will add support for more extension points in other views.</span></span>


| <span data-ttu-id="1ade2-116">POS ビュー</span><span class="sxs-lookup"><span data-stu-id="1ade2-116">POS view</span></span>                        | <span data-ttu-id="1ade2-117">カスタム コントロールがサポートされています</span><span class="sxs-lookup"><span data-stu-id="1ade2-117">Custom controls are supported</span></span> | <span data-ttu-id="1ade2-118">カスタム列がサポートされています</span><span class="sxs-lookup"><span data-stu-id="1ade2-118">Custom columns are supported</span></span> | <span data-ttu-id="1ade2-119">カスタムのアプリ バーのボタンがサポートされています</span><span class="sxs-lookup"><span data-stu-id="1ade2-119">Custom app bar buttons are supported</span></span> |
|---------------------------------|-------------------------------|------------------------------|--------------------------------------|
| <span data-ttu-id="1ade2-120">カート ビュー (画面レイアウトに基づく)</span><span class="sxs-lookup"><span data-stu-id="1ade2-120">Cart view (Screen layout based)</span></span> | <span data-ttu-id="1ade2-121">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-121">Yes</span></span>                           | <span data-ttu-id="1ade2-122">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-122">Yes</span></span>                          | <span data-ttu-id="1ade2-123">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-123">No</span></span>                                   |
| <span data-ttu-id="1ade2-124">CustomerAddEditView</span><span class="sxs-lookup"><span data-stu-id="1ade2-124">CustomerAddEditView</span></span>             | <span data-ttu-id="1ade2-125">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-125">Yes</span></span>                           | <span data-ttu-id="1ade2-126">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-126">No</span></span>                           | <span data-ttu-id="1ade2-127">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-127">Yes</span></span>                                  |
| <span data-ttu-id="1ade2-128">CustomerDetailsView</span><span class="sxs-lookup"><span data-stu-id="1ade2-128">CustomerDetailsView</span></span>             | <span data-ttu-id="1ade2-129">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-129">Yes</span></span>                           | <span data-ttu-id="1ade2-130">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-130">No</span></span>                           | <span data-ttu-id="1ade2-131">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-131">Yes</span></span>                                  |
| <span data-ttu-id="1ade2-132">SearchView</span><span class="sxs-lookup"><span data-stu-id="1ade2-132">SearchView</span></span>                      | <span data-ttu-id="1ade2-133">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-133">No</span></span>                            | <span data-ttu-id="1ade2-134">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-134">Yes</span></span>                          | <span data-ttu-id="1ade2-135">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-135">Yes</span></span>                                  |
| <span data-ttu-id="1ade2-136">InventoryLookupView</span><span class="sxs-lookup"><span data-stu-id="1ade2-136">InventoryLookupView</span></span>             | <span data-ttu-id="1ade2-137">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-137">No</span></span>                            | <span data-ttu-id="1ade2-138">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-138">Yes</span></span>                          | <span data-ttu-id="1ade2-139">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-139">Yes</span></span>                                  |
| <span data-ttu-id="1ade2-140">ShowJournalView</span><span class="sxs-lookup"><span data-stu-id="1ade2-140">ShowJournalView</span></span>                 | <span data-ttu-id="1ade2-141">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-141">No</span></span>                            | <span data-ttu-id="1ade2-142">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-142">Yes</span></span>                          | <span data-ttu-id="1ade2-143">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-143">Yes</span></span>                                  |
| <span data-ttu-id="1ade2-144">SimpleProductDetailsView</span><span class="sxs-lookup"><span data-stu-id="1ade2-144">SimpleProductDetailsView</span></span>        | <span data-ttu-id="1ade2-145">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-145">Yes</span></span>                           | <span data-ttu-id="1ade2-146">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-146">No</span></span>                           | <span data-ttu-id="1ade2-147">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-147">Yes</span></span>                                  |
| <span data-ttu-id="1ade2-148">AddressAddEditView</span><span class="sxs-lookup"><span data-stu-id="1ade2-148">AddressAddEditView</span></span>              | <span data-ttu-id="1ade2-149">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-149">Yes</span></span>                           | <span data-ttu-id="1ade2-150">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-150">No</span></span>                           | <span data-ttu-id="1ade2-151">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-151">Yes</span></span>                                    |
| <span data-ttu-id="1ade2-152">PaymentView</span><span class="sxs-lookup"><span data-stu-id="1ade2-152">PaymentView</span></span>                     | <span data-ttu-id="1ade2-153">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-153">No</span></span>                            | <span data-ttu-id="1ade2-154">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-154">No</span></span>                           | <span data-ttu-id="1ade2-155">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-155">Yes</span></span>                                  |
| <span data-ttu-id="1ade2-156">PriceCheckView</span><span class="sxs-lookup"><span data-stu-id="1ade2-156">PriceCheckView</span></span>                  | <span data-ttu-id="1ade2-157">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-157">Yes</span></span>                           | <span data-ttu-id="1ade2-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-158">No</span></span>                           | <span data-ttu-id="1ade2-159">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-159">Yes</span></span>                                   |
| <span data-ttu-id="1ade2-160">PriceCheckViewPhone</span><span class="sxs-lookup"><span data-stu-id="1ade2-160">PriceCheckViewPhone</span></span>             | <span data-ttu-id="1ade2-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-161">No</span></span>                            | <span data-ttu-id="1ade2-162">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-162">No</span></span>                           | <span data-ttu-id="1ade2-163">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-163">Yes</span></span>                                   |
| <span data-ttu-id="1ade2-164">SearchOrdersView</span><span class="sxs-lookup"><span data-stu-id="1ade2-164">SearchOrdersView</span></span>                | <span data-ttu-id="1ade2-165">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-165">No</span></span>                            | <span data-ttu-id="1ade2-166">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-166">Yes</span></span>                          | <span data-ttu-id="1ade2-167">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-167">No</span></span>                                   |
| <span data-ttu-id="1ade2-168">SearchPickingAndReceivingView</span><span class="sxs-lookup"><span data-stu-id="1ade2-168">SearchPickingAndReceivingView</span></span>   | <span data-ttu-id="1ade2-169">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-169">No</span></span>                            | <span data-ttu-id="1ade2-170">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-170">Yes</span></span>                          | <span data-ttu-id="1ade2-171">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-171">Yes</span></span>                                   |
| <span data-ttu-id="1ade2-172">CustomerOrderHistoryView</span><span class="sxs-lookup"><span data-stu-id="1ade2-172">CustomerOrderHistoryView</span></span>        | <span data-ttu-id="1ade2-173">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-173">No</span></span>                            | <span data-ttu-id="1ade2-174">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-174">Yes</span></span>                          | <span data-ttu-id="1ade2-175">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-175">No</span></span>                                   |
| <span data-ttu-id="1ade2-176">SearchStockCountView</span><span class="sxs-lookup"><span data-stu-id="1ade2-176">SearchStockCountView</span></span>            | <span data-ttu-id="1ade2-177">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-177">No</span></span>                            | <span data-ttu-id="1ade2-178">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-178">Yes</span></span>                          | <span data-ttu-id="1ade2-179">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-179">No</span></span>                                   |
| <span data-ttu-id="1ade2-180">StockCountDetailsView</span><span class="sxs-lookup"><span data-stu-id="1ade2-180">StockCountDetailsView</span></span>           | <span data-ttu-id="1ade2-181">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-181">No</span></span>                            | <span data-ttu-id="1ade2-182">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-182">Yes</span></span>                          | <span data-ttu-id="1ade2-183">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-183">No</span></span>                                   |
| <span data-ttu-id="1ade2-184">ResumeCartView</span><span class="sxs-lookup"><span data-stu-id="1ade2-184">ResumeCartView</span></span>                  | <span data-ttu-id="1ade2-185">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-185">No</span></span>                            | <span data-ttu-id="1ade2-186">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-186">Yes</span></span>                          | <span data-ttu-id="1ade2-187">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-187">No</span></span>                                    |
| <span data-ttu-id="1ade2-188">OrderFulfillmentView</span><span class="sxs-lookup"><span data-stu-id="1ade2-188">OrderFulfillmentView</span></span>            | <span data-ttu-id="1ade2-189">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-189">No</span></span>                            | <span data-ttu-id="1ade2-190">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-190">No</span></span>                           | <span data-ttu-id="1ade2-191">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-191">Yes</span></span>                                   |
| <span data-ttu-id="1ade2-192">InventoryLookupMatrixView</span><span class="sxs-lookup"><span data-stu-id="1ade2-192">InventoryLookupMatrixView</span></span>       | <span data-ttu-id="1ade2-193">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-193">No</span></span>                            | <span data-ttu-id="1ade2-194">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-194">No</span></span>                           | <span data-ttu-id="1ade2-195">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-195">Yes</span></span>                                   |
| <span data-ttu-id="1ade2-196">SuspendTransactionView</span><span class="sxs-lookup"><span data-stu-id="1ade2-196">SuspendTransactionView</span></span>          | <span data-ttu-id="1ade2-197">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-197">No</span></span>                            | <span data-ttu-id="1ade2-198">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-198">Yes</span></span>                          | <span data-ttu-id="1ade2-199">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-199">No</span></span>                               |   
| <span data-ttu-id="1ade2-200">ManageShiftView</span><span class="sxs-lookup"><span data-stu-id="1ade2-200">ManageShiftView</span></span>                 | <span data-ttu-id="1ade2-201">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-201">No</span></span>                            | <span data-ttu-id="1ade2-202">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-202">No</span></span>                           | <span data-ttu-id="1ade2-203">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-203">Yes</span></span>                               |  
| <span data-ttu-id="1ade2-204">ReportDetailsView</span><span class="sxs-lookup"><span data-stu-id="1ade2-204">ReportDetailsView</span></span>               | <span data-ttu-id="1ade2-205">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-205">No</span></span>                            | <span data-ttu-id="1ade2-206">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-206">No</span></span>                           | <span data-ttu-id="1ade2-207">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-207">Yes</span></span>                               |
| <span data-ttu-id="1ade2-208">SearchReceiptsView</span><span class="sxs-lookup"><span data-stu-id="1ade2-208">SearchReceiptsView</span></span>              | <span data-ttu-id="1ade2-209">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-209">No</span></span>                            | <span data-ttu-id="1ade2-210">無</span><span class="sxs-lookup"><span data-stu-id="1ade2-210">No</span></span>                           | <span data-ttu-id="1ade2-211">有</span><span class="sxs-lookup"><span data-stu-id="1ade2-211">Yes</span></span>                               |
| <span data-ttu-id="1ade2-212">StockCountDetailsView</span><span class="sxs-lookup"><span data-stu-id="1ade2-212">StockCountDetailsView</span></span>           | <span data-ttu-id="1ade2-213">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-213">No</span></span>                            | <span data-ttu-id="1ade2-214">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-214">No</span></span>                           | <span data-ttu-id="1ade2-215">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-215">Yes</span></span>                               |
| <span data-ttu-id="1ade2-216">TransferOrderDetailsView</span><span class="sxs-lookup"><span data-stu-id="1ade2-216">TransferOrderDetailsView</span></span>        | <span data-ttu-id="1ade2-217">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-217">No</span></span>                            | <span data-ttu-id="1ade2-218">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-218">No</span></span>                           | <span data-ttu-id="1ade2-219">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-219">Yes</span></span>                               |
| <span data-ttu-id="1ade2-220">FulfillmentLineView</span><span class="sxs-lookup"><span data-stu-id="1ade2-220">FulfillmentLineView</span></span>             | <span data-ttu-id="1ade2-221">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-221">No</span></span>                            | <span data-ttu-id="1ade2-222">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-222">Yes</span></span>                          | <span data-ttu-id="1ade2-223">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-223">No</span></span>                               |
| <span data-ttu-id="1ade2-224">ReturnTransactionView</span><span class="sxs-lookup"><span data-stu-id="1ade2-224">ReturnTransactionView</span></span>           | <span data-ttu-id="1ade2-225">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ade2-225">No</span></span>                            | <span data-ttu-id="1ade2-226">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-226">Yes</span></span>                          | <span data-ttu-id="1ade2-227">はい</span><span class="sxs-lookup"><span data-stu-id="1ade2-227">Yes</span></span>                               |


> [!NOTE]
> <span data-ttu-id="1ade2-228">上記に表示される表は、リリースされた最新バージョンおよび修正プログラムに基づいて更新されています。</span><span class="sxs-lookup"><span data-stu-id="1ade2-228">The table shown above is updated based on the latest released version and hotfix.</span></span> <span data-ttu-id="1ade2-229">旧バージョンでは、これらの拡張ポイントの一部は使用できません。</span><span class="sxs-lookup"><span data-stu-id="1ade2-229">In earlier versions, some of these extension points will not be available.</span></span>

> [!NOTE]
> <span data-ttu-id="1ade2-230">仕訳帳の表示 (行グリッド) と 返品トランザクション ビューのカスタム列は、行サブ フィールドの使用をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="1ade2-230">In Show journal (lines grid) and Return transaction view custom columns are supported using the row sub fields.</span></span> <span data-ttu-id="1ade2-231">これらのサブ フィールドは、情報コード メッセージ、シリアル番号、割引の値などのように、列ではなく行として表示されます。</span><span class="sxs-lookup"><span data-stu-id="1ade2-231">These sub fields will be displayed as rows instead of columns, like the info code messages or serial number or discounts values.</span></span>

<span data-ttu-id="1ade2-232">フィルターの拡張機能は**仕訳帳ビューを表示**および**注文ビューを検索**でもサポートされ、カスタム フィルターを追加します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-232">Filter extensions are also supported in **Show journal view** and **Search order views** to add custom filters.</span></span> <span data-ttu-id="1ade2-233">**注文ビューを検索** は拡張機能を使用してユーザー インターフェイス (UI) に検索用の既定パラメーターを設定することもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="1ade2-233">**Search order views** also supports setting default parameters for search in the user interface (UI) using extension.</span></span> <span data-ttu-id="1ade2-234">たとえば、既定のストア検索パラメータを追加する場合は、拡張機能を使用して UI に表示することでそれを実行できます。</span><span class="sxs-lookup"><span data-stu-id="1ade2-234">For example, if you want to add default store search parameter you can do that by using extension and showing that in the UI.</span></span> 

## <a name="add-a-custom-column-and-an-app-bar-button"></a><span data-ttu-id="1ade2-235">カスタム列とアプリ バー ボタンの追加</span><span class="sxs-lookup"><span data-stu-id="1ade2-235">Add a custom column and an app bar button</span></span>

1. <span data-ttu-id="1ade2-236">Microsoft Visual Studio 2015 を管理者として起動します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-236">Start Microsoft Visual Studio 2015 as an administrator.</span></span>
2. <span data-ttu-id="1ade2-237">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="1ade2-237">Open the **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="1ade2-238">**POS.Extensions** プロジェクトで、**SearchExtension** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-238">In the **POS.Extensions** project, create a folder that is named **SearchExtension**.</span></span>
4. <span data-ttu-id="1ade2-239">**SearchExtension** フォルダーで、**ViewExtensions** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-239">In the **SearchExtension** folder, create a folder that is named **ViewExtensions**.</span></span>
5. <span data-ttu-id="1ade2-240">**ViewExtensions** フォルダーで、**Search** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-240">In the **ViewExtensions** folder, create a folder that is named **Search**.</span></span>
6. <span data-ttu-id="1ade2-241">**Search** フォルダーで、**CustomCustomerSearchColumns.ts** という Typescript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-241">In the **Search** folder, create a Typescript file that is named **CustomCustomerSearchColumns.ts**.</span></span>
7. <span data-ttu-id="1ade2-242">**CustomCustomerSearchColumns.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="1ade2-242">In the **CustomCustomerSearchColumns.ts** file, add the following **import** statements to import the relevant entities and context.</span></span>

    ```Typescript
    import { ICustomerSearchColumn } from "PosApi/Extend/Views/SearchView";
    import { ICustomColumnsContext } from "PosApi/Extend/Views/CustomListColumns";
    import { ProxyEntities } from "PosApi/Entities";
    ```

8. <span data-ttu-id="1ade2-243">ファイルに既存の列とカスタム列を追加します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-243">Add the existing column and the custom column to the file.</span></span>

    ```Typescript
    export default (context: ICustomColumnsContext): ICustomerSearchColumn[] => {
        return [
            {
                title: context.resources.getString("string_2"),
                computeValue: (row: ProxyEntities.GlobalCustomer): string => { return row.AccountNumber; },
                ratio: 15,
                collapseOrder: 5,
                minWidth: 120
             }, {
                title: context.resources.getString("string_3"),
                computeValue: (row: ProxyEntities.GlobalCustomer): string => { return row.FullName; },
                ratio: 20,
                collapseOrder: 4,
                minWidth: 200
            }, {
                title: context.resources.getString("string_4"),
                computeValue: (row: ProxyEntities.GlobalCustomer): string => { return row.FullAddress; },
                ratio: 25,
                collapseOrder: 1,
                minWidth: 200
            }, {
                title: context.resources.getString("string_5"),
                computeValue: (row: ProxyEntities.GlobalCustomer): string => { return row.Email; },
                ratio: 20,
                collapseOrder: 2,
                minWidth: 200
            }, {
                title: context.resources.getString("string_7"),
                computeValue: (row: ProxyEntities.GlobalCustomer): string => { return row.Phone; },
                ratio: 20,
                collapseOrder: 3,
                minWidth: 120
            }
        ];
    };
    ```

9. <span data-ttu-id="1ade2-244">ここで、列の名前のローカライズのためのリソース ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-244">You will now add the resource file for localization of the column name.</span></span> <span data-ttu-id="1ade2-245">**SearchExtension** フォルダーで、**Resources** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-245">In the **SearchExtension** folder, create a folder that is named **Resources**.</span></span>
10. <span data-ttu-id="1ade2-246">**Resources** フォルダーで、**Strings** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-246">In the **Resources** folder, create a folder that is named **Strings**.</span></span>
11. <span data-ttu-id="1ade2-247">**Strings** フォルダーで、**en-US** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-247">In the **Strings** folder, create a folder that is named **en-US**.</span></span>
12. <span data-ttu-id="1ade2-248">**en-us** フォルダーで、**resources.resjson** というファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-248">In the **en-us** folder, create a file that is named **resources.resjson**.</span></span>
13. <span data-ttu-id="1ade2-249">**resources.resjson** ファイルに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-249">In the **resources.resjson** file, add the following code.</span></span>

    ```Typescript
    {
        //======================== Sample View extensions strings. ========================
        "string_0" : "Quick compare products",
        "_string_0.comment" : "Product search page app bar command label.",
        "string_1" : "View customer summary",
        "_string_1.comment" : "Customer search page app bar command label.",
        //======================== Column names. ========================
        "string_2" : "ACCOUNT NUMBER_CUSTOMIZED",
        "_string_2.comment" : "Customer search column name.",
        "string_3" : "NAME",
        "_string_3.comment" : "Customer search column name.",
        "string_4" : "ADDRESS",
        "_string_4.comment" : "Customer search column name.",
        "string_5" : "CONTACT EMAIL",
        "_string_5.comment" : "Customer search column name.",
        "string_7" : "PHONE NUMBER",
        "_string_7.comment" : "Customer search column name."
    }
    ```

14. <span data-ttu-id="1ade2-250">**SearchExtension** フォルダーで、**DialogSample** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-250">In the **SearchExtension** folder, create a folder that is named **DialogSample**.</span></span>
15. <span data-ttu-id="1ade2-251">**DialogSample** フォルダーで、**MessageDialog.ts** という Typescript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-251">In the **DialogSample** folder, create a Typescript file that is named **MessageDialog.ts**.</span></span>
16. <span data-ttu-id="1ade2-252">**MessageDialog.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="1ade2-252">In the **MessageDialog.ts** file, add the following **import** statements to import the relevant entities and context.</span></span>

    ```Typescript
    import { ShowMessageDialogClientRequest, ShowMessageDialogClientResponse, IMessageDialogOptions } from "PosApi/Consume/Dialogs";
    import { IExtensionContext } from "PosApi/Framework/ExtensionContext";
    import { ClientEntities } from "PosApi/Entities";
    ```

17. <span data-ttu-id="1ade2-253">**MessageDialog** という名前のクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-253">Create a class that is named **MessageDialog**.</span></span>

    ```Typescript
    export default class MessageDialog {}
    ```

18. <span data-ttu-id="1ade2-254">**MessageDialog** クラスで、次の **show** メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-254">In the **MessageDialog** class, add the following **show** method.</span></span>

    ```Typescript
    public static show(context: IExtensionContext, message: string): Promise<void> {
        let promise: Promise<void> = new Promise<void>((resolve: () => void, reject: (reason?: any) => void) => 
        {
            let messageDialogOptions: IMessageDialogOptions = {
                title: "Extension Message Dialog",
                message: message,
                showCloseX: true, // this property will return "Close" as result when "X" is clicked to close dialog.
                button1: {
                    id: "Button1Close",
                    label: "OK",
                    result: "OKResult"
                },
                button2: {
                    id: "Button2Cancel",
                    label: "Cancel",
                    result: "CancelResult"
                }
            };
            let dialogRequest: ShowMessageDialogClientRequest<ShowMessageDialogClientResponse> =
                new ShowMessageDialogClientRequest<ShowMessageDialogClientResponse>(messageDialogOptions);
                context.runtime.executeAsync(dialogRequest).then((
                    result: ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>) => {
                if (!result.canceled) {
                    context.logger.logInformational("MessageDialog result: " + result.data.result.dialogResult);
                    resolve();
                }
            }).catch((reason: any) => {
            context.logger.logError(JSON.stringify(reason));
            reject(reason);
            });
        });
        return promise;
    }
    ```

19. <span data-ttu-id="1ade2-255">ここで、選択した顧客に関する詳細を含むダイアログ ボックスを開くために、検索ビューにカスタムのアプリ バー ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-255">You will now add a custom app bar button in the search view to open a dialog box that contains details about the selected customer.</span></span> <span data-ttu-id="1ade2-256">**ViewExtensions** フォルダーで、**ViewCustomerSummaryCommand.ts** という Typescript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-256">In the **ViewExtensions** folder, create a Typescript file that is named **ViewCustomerSummaryCommand.ts**.</span></span>
20. <span data-ttu-id="1ade2-257">**ViewCustomerSummaryCommand.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="1ade2-257">In the **ViewCustomerSummaryCommand.ts** file, add the following **import** statements to import the relevant entities and context.</span></span>

    ```Typescript
    import { ProxyEntities } from "PosApi/Entities";
    import { ArrayExtensions, ObjectExtensions } from "PosApi/TypeExtensions";
    import { IExtensionCommandContext } from "PosApi/Extend/Views/AppBarCommands";
    import * as SearchView from "PosApi/Extend/Views/SearchView";
    import MessageDialog from "../DialogSample/MessageDialog";
    ```

21. <span data-ttu-id="1ade2-258">**ViewCustomerSummaryCommand** という名前のクラスを作成し、**CustomerSearchExtensionCommandBase** からクラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-258">Create a class that is named **ViewCustomerSummaryCommand**, and extend it from **CustomerSearchExtensionCommandBase**.</span></span>

    ```Typescript
    export default class ViewCustomerSummaryCommand extends SearchView.CustomerSearchExtensionCommandBase {}
    ```

22. <span data-ttu-id="1ade2-259">**ViewCustomerSummaryCommand** クラスで、選択した顧客を検索するときに、結果をキャプチャするプライベート変数を宣言します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-259">In the **ViewCustomerSummaryCommand** class, declare a private variable to capture the results when searching for the selected customer.</span></span>

    ```Typescript
    private _customerSearchResults: ProxyEntities.GlobalCustomer[];
    ```

23. <span data-ttu-id="1ade2-260">クラス **コンストラクター** メソッドを追加して、検索ハンドラーを初期化してクリアします。</span><span class="sxs-lookup"><span data-stu-id="1ade2-260">Add the class **constructor** method to initialize and clear the search handler.</span></span>

    ```Typescript
    constructor(context: IExtensionCommandContext<SearchView.ICustomerSearchToExtensionCommandMessageTypeMap>) {
        super(context);
        this.id = "viewCustomerSummaryCommand";
        this.label = context.resources.getString("string_1");
        this.extraClass = "iconLightningBolt";
        this._customerSearchResults = [];
        this.searchResultsSelectedHandler = (data: SearchView.CustomerSearchSearchResultSelectedData): void => {
            this._customerSearchResults = data.customers;
            this.canExecute = true;
        };
        this.searchResultSelectionClearedHandler = (): void => {
            this._customerSearchResults = [];
            this.canExecute = false;
        };
    }
    ```

24. <span data-ttu-id="1ade2-261">**init** メソッドを追加して、**表示**プロパティを初期化します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-261">Add the **init** method to initialize the **visible** property.</span></span>

    ```Typescript
    protected init(state: SearchView.ICustomerSearchExtensionCommandState): void {
        this.isVisible = true;
    }
    ```

25. <span data-ttu-id="1ade2-262">アプリ ボタン クリック ハンドラーを処理する**実行**メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-262">Add the **execute** method to handle the app button click handler.</span></span> <span data-ttu-id="1ade2-263">**execute** メソッドは、ハンドラーから選択した顧客のデータを読み取り、単純なダイアログ ボックスに表示します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-263">The **execute** method reads the data for the selected customer from the handler and shows it in a simple dialog box.</span></span>

    ```Typescript
    protected execute(): void {
        let customer: ProxyEntities.GlobalCustomer = ArrayExtensions.firstOrUndefined(this._customerSearchResults);
        if (!ObjectExtensions.isNullOrUndefined(customer)) {
            let message: string = "Customer Account: " + (customer.AccountNumber || "") + " | ";
            message += "Name: " + customer.FullName + " | ";
            message += "Phone Number: " + customer.Phone + " | ";
            message += "Email Address: " + customer.Email;
            MessageDialog.show(this.context, message);
        } 
    }
    ```

    <span data-ttu-id="1ade2-264">コード サンプルの全体は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="1ade2-264">The whole code sample should look like this.</span></span>

    ```Typescript
    import { ProxyEntities } from "PosApi/Entities";
    import { ArrayExtensions, ObjectExtensions } from "PosApi/TypeExtensions";
    import { IExtensionCommandContext } from "PosApi/Extend/Views/AppBarCommands";
    import * as SearchView from "PosApi/Extend/Views/SearchView";
    import MessageDialog from "../../DialogSample/MessageDialog";
    export default class ViewCustomerSummaryCommand extends SearchView.CustomerSearchExtensionCommandBase {
        private _customerSearchResults: ProxyEntities.GlobalCustomer[];

        /**
        * Creates a new instance of the ViewCustomerSummaryCommand class.
        * @param {IExtensionCommandContext<CustomerDetailsView.ICustomerSearchToExtensionCommandMessageTypeMap>} context The command context.
        * @remarks The command context contains APIs through which a command can communicate with POS.
        */
        constructor(context: IExtensionCommandContext<SearchView.ICustomerSearchToExtensionCommandMessageTypeMap>) {
            super(context);
            this.id = "viewCustomerSummaryCommand";
            this.label = context.resources.getString("string_1");
            this.extraClass = "iconLightningBolt";
            this._customerSearchResults = [];

            this.searchResultsSelectedHandler = (data: SearchView.CustomerSearchSearchResultSelectedData): void => {
                this._customerSearchResults = data.customers;
                this.canExecute = true;
            };

            this.searchResultSelectionClearedHandler = (): void => {
                this._customerSearchResults = [];
                this.canExecute = false;
            };
        }

        /**
        * Initializes the command.
        * @param {CustomerDetailsView.ICustomerDetailsExtensionCommandState} state The state used to initialize the command.
        */
        protected init(state: SearchView.ICustomerSearchExtensionCommandState): void {
            this.isVisible = true;
        }

        /**
        * Executes the command.
        */
        protected execute(): void {
            let customer: ProxyEntities.GlobalCustomer = ArrayExtensions.firstOrUndefined(this._customerSearchResults);
            if (!ObjectExtensions.isNullOrUndefined(customer)) {
                let message: string = "Customer Account: " + (customer.AccountNumber || "") + " | ";
                message += "Name: " + customer.FullName + " | ";
                message += "Phone Number: " + customer.Phone + " | ";
                message += "Email Address: " + customer.Email;
                MessageDialog.show(this.context, message);
            }
        }
    }
    ```

26. <span data-ttu-id="1ade2-265">**SearchExtension** フォルダーで、**manifest.json** という JSON ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-265">In the **SearchExtension** folder, create a JSON file that is named **manifest.json**.</span></span>
27. <span data-ttu-id="1ade2-266">**manifest.json** ファイルに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-266">In the **manifest.json** file, add the following code.</span></span>

    ```Typescript
    {
        "$schema": "../manifestSchema.json",
        "name": "Pos_Extensibility_Samples",
        "publisher": "Microsoft",
        "version": "7.2.0",
        "minimumPosVersion": "7.2.0.0",
        "components": {
            "resources": {
                "supportedUICultures": [ "en-US" ],
                "fallbackUICulture": "en-US",
                "culturesDirectoryPath": "Resources/Strings ",
                "stringResourcesFileName": "resources.resjson",
                "cultureInfoOverridesFilePath": "Resources/cultureInfoOverrides.json"
            },
            "extend": {
                "views": {
                    "SearchView": {
                        "customerAppBarCommands": [ { "modulePath": "ViewExtensions/Search/ViewCustomerSummaryCommand" } ],
                        "customerListConfiguration": { "modulePath": "ViewExtensions/Search/CustomCustomerSearchColumns" }
                    }
                }
            }
        }
    }
    ```

28. <span data-ttu-id="1ade2-267">**POS.Extensions** プロジェクトで **extensions.json** ファイルを開き、**SearchExtension** サンプルで更新して、POS が実行時にこの拡張機能に含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="1ade2-267">In the **POS.Extensions** project, open the **extensions.json** file, and update it with **SearchExtension** samples, so that the POS includes this extension at runtime.</span></span>

    ```Typescript
    {
        "extensionPackages": [
        {
            "baseUrl": "SampleExtensions2"
        },
        {
            "baseUrl": "SearchExtension"
        }
        ]
    }
    ```

29. <span data-ttu-id="1ade2-268">**tsconfig.json** ファイルで、除外リストに拡張パッケージ フォルダーをコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="1ade2-268">In the **tsconfig.json** file, comment out the extension package folders in the exclude list.</span></span> <span data-ttu-id="1ade2-269">POS は、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-269">The POS uses this file to include or exclude the extension.</span></span> <span data-ttu-id="1ade2-270">既定では、リストに除外された拡張リスト全体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1ade2-270">By default, the list contains the whole excluded extensions list.</span></span> <span data-ttu-id="1ade2-271">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、除外リストの拡張子をコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="1ade2-271">To include an extension as part of the POS, add the name of the extension folder, and comment out the extension in the exclude list, as shown here.</span></span>

    ```Typescript
    "exclude": [
    "SampleExtensions"
    //"SampleExtensions2",
    //"SearchExtension"
    ],
    ```

30. <span data-ttu-id="1ade2-272">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="1ade2-272">Compile and rebuild the project.</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="1ade2-273">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="1ade2-273">Validate the customization</span></span>

<span data-ttu-id="1ade2-274">カスタマイズを検証するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1ade2-274">Follow these steps to validate the customization.</span></span>

1. <span data-ttu-id="1ade2-275">オペレーター ID に **000160**、パスワードに **123** を使用して Retail Modern POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="1ade2-275">Sign in to Retail Modern POS by using **000160** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="1ade2-276">上部の検索バーを使って顧客 **2001** を検索します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-276">Search for customer **2001** by using the search bar on the top.</span></span>

    <span data-ttu-id="1ade2-277">追加したカスタム列が表示されました。</span><span class="sxs-lookup"><span data-stu-id="1ade2-277">You should see the custom columns that you added.</span></span>

3. <span data-ttu-id="1ade2-278">顧客を選択し、新しいアプリケーション バーのボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="1ade2-278">Select a customer, and then select the new app bar button.</span></span> <span data-ttu-id="1ade2-279">選択した顧客に関する詳細を含むダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1ade2-279">A dialog box should appear that contains details about the selected customer.</span></span>
