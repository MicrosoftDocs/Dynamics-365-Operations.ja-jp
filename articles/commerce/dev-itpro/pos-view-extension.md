---
title: POS ビューの拡張によるカスタム列およびアプリ バー ボタンの追加
description: このトピックでは、[顧客の追加/編集] 画面などの既存の POS ビューを拡張する方法について説明します。
author: mugunthanm
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 24411
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-11-22
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 51017bd0b64a2c7f46da6ed6642c9fa7c5b7e4a6
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039757"
---
# <a name="extend-pos-views-to-add-custom-columns-and-app-bar-buttons"></a><span data-ttu-id="ab389-103">POS ビューの拡張によるカスタム列およびアプリ バー ボタンの追加</span><span class="sxs-lookup"><span data-stu-id="ab389-103">Extend POS views to add custom columns and app bar buttons</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab389-104">このトピックでは、既存の [販売時点管理 (POS)] ビューを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab389-104">This topic explains how you can extend existing point of sale (POS) views.</span></span> <span data-ttu-id="ab389-105">**トランザクション** 画面および **ようこそ** 画面を拡張するには、画面レイアウト デザイナーを使用します。</span><span class="sxs-lookup"><span data-stu-id="ab389-105">To extend the **Transaction** screen and **Welcome** screen, you can use the screen layout designer.</span></span> <span data-ttu-id="ab389-106">**顧客の追加/編集** 画面など、他のすべての POS ビューを拡張するには、Retail ソフトウェア開発キット (SDK) を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab389-106">To extend all other POS views, such as the **Customer Add/Edit** screen, you use the Retail software development kit (SDK).</span></span> <span data-ttu-id="ab389-107">このトピックでは、Retail SDK による既存の POS ビューの拡張について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab389-107">This topic focuses on the extension of existing POS views via the Retail SDK.</span></span>



<span data-ttu-id="ab389-108">POS ビューでは、次の拡張ポイントとパターンがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="ab389-108">POS views support the following extension points and patterns:</span></span>

- <span data-ttu-id="ab389-109">**カスタム アプリケーション バーのボタン** - 選択したページのアプリケーション バーにカスタム ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="ab389-109">**Custom app bar buttons** – Add custom buttons to the app bar on selected pages.</span></span>
- <span data-ttu-id="ab389-110">**カスタム列セット** - 選択したページのグリッド列をカスタム列に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="ab389-110">**Custom column sets** – Replace the grid columns with custom columns on selected pages.</span></span>
- <span data-ttu-id="ab389-111">**カスタム コントロール** - 選択したページに、新しいコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="ab389-111">**Custom controls** – Add new controls to selected pages.</span></span>

## <a name="pos-views-that-currently-support-extensions"></a><span data-ttu-id="ab389-112">現在拡張機能をサポートする POS ビュー</span><span class="sxs-lookup"><span data-stu-id="ab389-112">POS views that currently support extensions</span></span>

<span data-ttu-id="ab389-113">次のテーブルに、現在拡張機能をサポートしている POS ビューを示します。</span><span class="sxs-lookup"><span data-stu-id="ab389-113">The following table shows the POS views that currently support extensions.</span></span> <span data-ttu-id="ab389-114">また、各 POS ビューがサポートする拡張ポイントのタイプも示します。</span><span class="sxs-lookup"><span data-stu-id="ab389-114">It also indicates the types of extension points that each POS view supports.</span></span>

> [!NOTE]
> <span data-ttu-id="ab389-115">今後のリリースと修正プログラムで、他のビューの拡張ポイントをさらにサポートします。</span><span class="sxs-lookup"><span data-stu-id="ab389-115">The upcoming releases and hotfix will add support for more extension points in other views.</span></span>


| <span data-ttu-id="ab389-116">POS ビュー (リリース)</span><span class="sxs-lookup"><span data-stu-id="ab389-116">POS view (Release)</span></span>              | <span data-ttu-id="ab389-117">カスタム コントロールがサポートされています</span><span class="sxs-lookup"><span data-stu-id="ab389-117">Custom controls are supported</span></span> | <span data-ttu-id="ab389-118">カスタム列がサポートされています</span><span class="sxs-lookup"><span data-stu-id="ab389-118">Custom columns are supported</span></span> | <span data-ttu-id="ab389-119">カスタムのアプリ バーのボタンがサポートされています</span><span class="sxs-lookup"><span data-stu-id="ab389-119">Custom app bar buttons are supported</span></span> |
|---------------------------------|-------------------------------|------------------------------|--------------------------------------|
| <span data-ttu-id="ab389-120">カート ビュー (画面レイアウトに基づく)</span><span class="sxs-lookup"><span data-stu-id="ab389-120">Cart view (Screen layout based)</span></span> | <span data-ttu-id="ab389-121">有</span><span class="sxs-lookup"><span data-stu-id="ab389-121">Yes</span></span>                           | <span data-ttu-id="ab389-122">有</span><span class="sxs-lookup"><span data-stu-id="ab389-122">Yes</span></span>                          | <span data-ttu-id="ab389-123">無</span><span class="sxs-lookup"><span data-stu-id="ab389-123">No</span></span>                                   |
| <span data-ttu-id="ab389-124">CustomerAddEditView</span><span class="sxs-lookup"><span data-stu-id="ab389-124">CustomerAddEditView</span></span>             | <span data-ttu-id="ab389-125">有</span><span class="sxs-lookup"><span data-stu-id="ab389-125">Yes</span></span>                           | <span data-ttu-id="ab389-126">無</span><span class="sxs-lookup"><span data-stu-id="ab389-126">No</span></span>                           | <span data-ttu-id="ab389-127">有</span><span class="sxs-lookup"><span data-stu-id="ab389-127">Yes</span></span>                                  |
| <span data-ttu-id="ab389-128">CustomerDetailsView</span><span class="sxs-lookup"><span data-stu-id="ab389-128">CustomerDetailsView</span></span>             | <span data-ttu-id="ab389-129">有</span><span class="sxs-lookup"><span data-stu-id="ab389-129">Yes</span></span>                           | <span data-ttu-id="ab389-130">無</span><span class="sxs-lookup"><span data-stu-id="ab389-130">No</span></span>                           | <span data-ttu-id="ab389-131">有</span><span class="sxs-lookup"><span data-stu-id="ab389-131">Yes</span></span>                                  |
| <span data-ttu-id="ab389-132">SearchView</span><span class="sxs-lookup"><span data-stu-id="ab389-132">SearchView</span></span>                      | <span data-ttu-id="ab389-133">無</span><span class="sxs-lookup"><span data-stu-id="ab389-133">No</span></span>                            | <span data-ttu-id="ab389-134">有</span><span class="sxs-lookup"><span data-stu-id="ab389-134">Yes</span></span>                          | <span data-ttu-id="ab389-135">有</span><span class="sxs-lookup"><span data-stu-id="ab389-135">Yes</span></span>                                  |
| <span data-ttu-id="ab389-136">InventoryLookupView</span><span class="sxs-lookup"><span data-stu-id="ab389-136">InventoryLookupView</span></span>             | <span data-ttu-id="ab389-137">無</span><span class="sxs-lookup"><span data-stu-id="ab389-137">No</span></span>                            | <span data-ttu-id="ab389-138">有</span><span class="sxs-lookup"><span data-stu-id="ab389-138">Yes</span></span>                          | <span data-ttu-id="ab389-139">有</span><span class="sxs-lookup"><span data-stu-id="ab389-139">Yes</span></span>                                  |
| <span data-ttu-id="ab389-140">ShowJournalView</span><span class="sxs-lookup"><span data-stu-id="ab389-140">ShowJournalView</span></span>                 | <span data-ttu-id="ab389-141">無</span><span class="sxs-lookup"><span data-stu-id="ab389-141">No</span></span>                            | <span data-ttu-id="ab389-142">有</span><span class="sxs-lookup"><span data-stu-id="ab389-142">Yes</span></span>                          | <span data-ttu-id="ab389-143">有</span><span class="sxs-lookup"><span data-stu-id="ab389-143">Yes</span></span>                                  |
| <span data-ttu-id="ab389-144">SimpleProductDetailsView</span><span class="sxs-lookup"><span data-stu-id="ab389-144">SimpleProductDetailsView</span></span>        | <span data-ttu-id="ab389-145">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-145">Yes</span></span>                           | <span data-ttu-id="ab389-146">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-146">No</span></span>                           | <span data-ttu-id="ab389-147">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-147">Yes</span></span>                                  |
| <span data-ttu-id="ab389-148">AddressAddEditView</span><span class="sxs-lookup"><span data-stu-id="ab389-148">AddressAddEditView</span></span>              | <span data-ttu-id="ab389-149">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-149">Yes</span></span>                           | <span data-ttu-id="ab389-150">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-150">No</span></span>                           | <span data-ttu-id="ab389-151">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-151">Yes</span></span>                                    |
| <span data-ttu-id="ab389-152">PaymentView</span><span class="sxs-lookup"><span data-stu-id="ab389-152">PaymentView</span></span>                     | <span data-ttu-id="ab389-153">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-153">No</span></span>                            | <span data-ttu-id="ab389-154">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-154">No</span></span>                           | <span data-ttu-id="ab389-155">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-155">Yes</span></span>                                  |
| <span data-ttu-id="ab389-156">PriceCheckView</span><span class="sxs-lookup"><span data-stu-id="ab389-156">PriceCheckView</span></span>                  | <span data-ttu-id="ab389-157">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-157">Yes</span></span>                           | <span data-ttu-id="ab389-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-158">No</span></span>                           | <span data-ttu-id="ab389-159">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-159">Yes</span></span>                                   |
| <span data-ttu-id="ab389-160">PriceCheckViewPhone</span><span class="sxs-lookup"><span data-stu-id="ab389-160">PriceCheckViewPhone</span></span>             | <span data-ttu-id="ab389-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-161">No</span></span>                            | <span data-ttu-id="ab389-162">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-162">No</span></span>                           | <span data-ttu-id="ab389-163">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-163">Yes</span></span>                                   |
| <span data-ttu-id="ab389-164">SearchOrdersView</span><span class="sxs-lookup"><span data-stu-id="ab389-164">SearchOrdersView</span></span>                | <span data-ttu-id="ab389-165">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-165">No</span></span>                            | <span data-ttu-id="ab389-166">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-166">Yes</span></span>                          | <span data-ttu-id="ab389-167">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-167">No</span></span>                                   |
| <span data-ttu-id="ab389-168">SearchPickingAndReceivingView</span><span class="sxs-lookup"><span data-stu-id="ab389-168">SearchPickingAndReceivingView</span></span>   | <span data-ttu-id="ab389-169">無</span><span class="sxs-lookup"><span data-stu-id="ab389-169">No</span></span>                            | <span data-ttu-id="ab389-170">有</span><span class="sxs-lookup"><span data-stu-id="ab389-170">Yes</span></span>                          | <span data-ttu-id="ab389-171">有</span><span class="sxs-lookup"><span data-stu-id="ab389-171">Yes</span></span>                                   |
| <span data-ttu-id="ab389-172">CustomerOrderHistoryView</span><span class="sxs-lookup"><span data-stu-id="ab389-172">CustomerOrderHistoryView</span></span>        | <span data-ttu-id="ab389-173">無</span><span class="sxs-lookup"><span data-stu-id="ab389-173">No</span></span>                            | <span data-ttu-id="ab389-174">有</span><span class="sxs-lookup"><span data-stu-id="ab389-174">Yes</span></span>                          | <span data-ttu-id="ab389-175">無</span><span class="sxs-lookup"><span data-stu-id="ab389-175">No</span></span>                                   |
| <span data-ttu-id="ab389-176">SearchStockCountView</span><span class="sxs-lookup"><span data-stu-id="ab389-176">SearchStockCountView</span></span>            | <span data-ttu-id="ab389-177">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-177">No</span></span>                            | <span data-ttu-id="ab389-178">あり</span><span class="sxs-lookup"><span data-stu-id="ab389-178">Yes</span></span>                          | <span data-ttu-id="ab389-179">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-179">No</span></span>                                   |
| <span data-ttu-id="ab389-180">StockCountDetailsView</span><span class="sxs-lookup"><span data-stu-id="ab389-180">StockCountDetailsView</span></span>           | <span data-ttu-id="ab389-181">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-181">No</span></span>                            | <span data-ttu-id="ab389-182">あり</span><span class="sxs-lookup"><span data-stu-id="ab389-182">Yes</span></span>                          | <span data-ttu-id="ab389-183">あり</span><span class="sxs-lookup"><span data-stu-id="ab389-183">Yes</span></span>                                   |
| <span data-ttu-id="ab389-184">ResumeCartView</span><span class="sxs-lookup"><span data-stu-id="ab389-184">ResumeCartView</span></span>                  | <span data-ttu-id="ab389-185">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-185">No</span></span>                            | <span data-ttu-id="ab389-186">あり</span><span class="sxs-lookup"><span data-stu-id="ab389-186">Yes</span></span>                          | <span data-ttu-id="ab389-187">あり</span><span class="sxs-lookup"><span data-stu-id="ab389-187">Yes</span></span>                                    |
| <span data-ttu-id="ab389-188">InventoryLookupMatrixView</span><span class="sxs-lookup"><span data-stu-id="ab389-188">InventoryLookupMatrixView</span></span>       | <span data-ttu-id="ab389-189">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-189">No</span></span>                            | <span data-ttu-id="ab389-190">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-190">No</span></span>                           | <span data-ttu-id="ab389-191">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-191">Yes</span></span>                                   |
| <span data-ttu-id="ab389-192">SuspendTransactionView</span><span class="sxs-lookup"><span data-stu-id="ab389-192">SuspendTransactionView</span></span>          | <span data-ttu-id="ab389-193">無</span><span class="sxs-lookup"><span data-stu-id="ab389-193">No</span></span>                            | <span data-ttu-id="ab389-194">有</span><span class="sxs-lookup"><span data-stu-id="ab389-194">Yes</span></span>                          | <span data-ttu-id="ab389-195">無</span><span class="sxs-lookup"><span data-stu-id="ab389-195">No</span></span>                               |   
| <span data-ttu-id="ab389-196">ManageShiftView</span><span class="sxs-lookup"><span data-stu-id="ab389-196">ManageShiftView</span></span>                 | <span data-ttu-id="ab389-197">無</span><span class="sxs-lookup"><span data-stu-id="ab389-197">No</span></span>                            | <span data-ttu-id="ab389-198">無</span><span class="sxs-lookup"><span data-stu-id="ab389-198">No</span></span>                           | <span data-ttu-id="ab389-199">あり</span><span class="sxs-lookup"><span data-stu-id="ab389-199">Yes</span></span>                               |  
| <span data-ttu-id="ab389-200">ReportDetailsView</span><span class="sxs-lookup"><span data-stu-id="ab389-200">ReportDetailsView</span></span>               | <span data-ttu-id="ab389-201">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-201">No</span></span>                            | <span data-ttu-id="ab389-202">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-202">No</span></span>                           | <span data-ttu-id="ab389-203">あり</span><span class="sxs-lookup"><span data-stu-id="ab389-203">Yes</span></span>                               |
| <span data-ttu-id="ab389-204">SearchReceiptsView</span><span class="sxs-lookup"><span data-stu-id="ab389-204">SearchReceiptsView</span></span>              | <span data-ttu-id="ab389-205">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-205">No</span></span>                            | <span data-ttu-id="ab389-206">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-206">No</span></span>                           | <span data-ttu-id="ab389-207">あり</span><span class="sxs-lookup"><span data-stu-id="ab389-207">Yes</span></span>                               |
| <span data-ttu-id="ab389-208">TransferOrderDetailsView</span><span class="sxs-lookup"><span data-stu-id="ab389-208">TransferOrderDetailsView</span></span>        | <span data-ttu-id="ab389-209">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-209">No</span></span>                            | <span data-ttu-id="ab389-210">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-210">No</span></span>                           | <span data-ttu-id="ab389-211">あり</span><span class="sxs-lookup"><span data-stu-id="ab389-211">Yes</span></span>                               |
| <span data-ttu-id="ab389-212">FulfillmentLineView</span><span class="sxs-lookup"><span data-stu-id="ab389-212">FulfillmentLineView</span></span>             | <span data-ttu-id="ab389-213">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-213">No</span></span>                            | <span data-ttu-id="ab389-214">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-214">Yes</span></span>                          | <span data-ttu-id="ab389-215">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-215">Yes</span></span>                               |
| <span data-ttu-id="ab389-216">ReturnTransactionView</span><span class="sxs-lookup"><span data-stu-id="ab389-216">ReturnTransactionView</span></span>           | <span data-ttu-id="ab389-217">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-217">No</span></span>                            | <span data-ttu-id="ab389-218">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-218">Yes</span></span>                          | <span data-ttu-id="ab389-219">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-219">Yes</span></span>                               |
| <span data-ttu-id="ab389-220">PickingAndReceivingDetailsView</span><span class="sxs-lookup"><span data-stu-id="ab389-220">PickingAndReceivingDetailsView</span></span>  | <span data-ttu-id="ab389-221">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab389-221">No</span></span>                            | <span data-ttu-id="ab389-222">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-222">Yes</span></span>                          | <span data-ttu-id="ab389-223">はい</span><span class="sxs-lookup"><span data-stu-id="ab389-223">Yes</span></span>                    |
| <span data-ttu-id="ab389-224">PickingAndReceivingDetailsView (高度な倉庫)</span><span class="sxs-lookup"><span data-stu-id="ab389-224">PickingAndReceivingDetailsView (Advanced warehouse)</span></span>  | <span data-ttu-id="ab389-225">無</span><span class="sxs-lookup"><span data-stu-id="ab389-225">No</span></span>                            | <span data-ttu-id="ab389-226">有</span><span class="sxs-lookup"><span data-stu-id="ab389-226">Yes</span></span>                          | <span data-ttu-id="ab389-227">有</span><span class="sxs-lookup"><span data-stu-id="ab389-227">Yes</span></span>           |
| <span data-ttu-id="ab389-228">SalesInvoiceDetailsView (10.0.11)</span><span class="sxs-lookup"><span data-stu-id="ab389-228">SalesInvoiceDetailsView (10.0.11)</span></span> | <span data-ttu-id="ab389-229">無</span><span class="sxs-lookup"><span data-stu-id="ab389-229">No</span></span>                            | <span data-ttu-id="ab389-230">無</span><span class="sxs-lookup"><span data-stu-id="ab389-230">No</span></span>                          | <span data-ttu-id="ab389-231">有</span><span class="sxs-lookup"><span data-stu-id="ab389-231">Yes</span></span>           |
| <span data-ttu-id="ab389-232">SalesInvoicesView (10.0.11)</span><span class="sxs-lookup"><span data-stu-id="ab389-232">SalesInvoicesView (10.0.11)</span></span> | <span data-ttu-id="ab389-233">無</span><span class="sxs-lookup"><span data-stu-id="ab389-233">No</span></span>                            | <span data-ttu-id="ab389-234">有</span><span class="sxs-lookup"><span data-stu-id="ab389-234">Yes</span></span>                          | <span data-ttu-id="ab389-235">無</span><span class="sxs-lookup"><span data-stu-id="ab389-235">No</span></span>           |
| <span data-ttu-id="ab389-236">InventoryDocumentShippingAndReceivingView (10.0.13)</span><span class="sxs-lookup"><span data-stu-id="ab389-236">InventoryDocumentShippingAndReceivingView (10.0.13)</span></span> | <span data-ttu-id="ab389-237">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-237">No</span></span>                            | <span data-ttu-id="ab389-238">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-238">No</span></span>                          | <span data-ttu-id="ab389-239">あり</span><span class="sxs-lookup"><span data-stu-id="ab389-239">Yes</span></span>           |
| <span data-ttu-id="ab389-240">InventoryDocumentListView</span><span class="sxs-lookup"><span data-stu-id="ab389-240">InventoryDocumentListView</span></span>  | <span data-ttu-id="ab389-241">なし</span><span class="sxs-lookup"><span data-stu-id="ab389-241">No</span></span>                            | <span data-ttu-id="ab389-242">はい (10.0.15)</span><span class="sxs-lookup"><span data-stu-id="ab389-242">Yes (10.0.15)</span></span>                          | <span data-ttu-id="ab389-243">はい (10.0.13)</span><span class="sxs-lookup"><span data-stu-id="ab389-243">Yes (10.0.13)</span></span>          |



> [!NOTE]
> <span data-ttu-id="ab389-244">上記に表示される表は、リリースされた最新バージョンおよび修正プログラムに基づいて更新されています。</span><span class="sxs-lookup"><span data-stu-id="ab389-244">The table shown above is updated based on the latest released version and hotfix.</span></span> <span data-ttu-id="ab389-245">旧バージョンでは、これらの拡張ポイントの一部は使用できません。</span><span class="sxs-lookup"><span data-stu-id="ab389-245">In earlier versions, some of these extension points will not be available.</span></span>

> [!NOTE]
> <span data-ttu-id="ab389-246">仕訳帳の表示 (行グリッド) と 返品トランザクション ビューのカスタム列は、行サブ フィールドの使用をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ab389-246">In Show journal (lines grid) and Return transaction view custom columns are supported using the row sub fields.</span></span> <span data-ttu-id="ab389-247">これらのサブ フィールドは、情報コード メッセージ、シリアル番号、割引の値などのように、列ではなく行として表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab389-247">These sub fields will be displayed as rows instead of columns, like the info code messages or serial number or discounts values.</span></span>

## <a name="custom-filter-extension"></a><span data-ttu-id="ab389-248">カスタム フィルターの拡張機能</span><span class="sxs-lookup"><span data-stu-id="ab389-248">Custom filter extension</span></span>

<span data-ttu-id="ab389-249">カスタム フィルターの拡張機能は **仕訳帳表示ビュー**、**注文検索ビュー**、および **FulfillmentLine ビュー** でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="ab389-249">Custom filter extensions are supported in **Show journal view**, **Search order view**, and **FulfillmentLine view**.</span></span> <span data-ttu-id="ab389-250">**注文検索ビュー** は拡張機能を使用してユーザー インターフェイス (UI) に検索用の既定パラメーターを設定することもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ab389-250">**Search order views** also supports setting default parameters for search in the user interface (UI) using extensions.</span></span> <span data-ttu-id="ab389-251">たとえば、店舗検索において既定のパラメーターを追加する場合は、拡張機能を使用して UI に表示することでそれを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ab389-251">For example, if you want to add a default store search parameter you can do that by using an extension and showing that in the UI.</span></span> 

<span data-ttu-id="ab389-252">カスタム フィルターの拡張機能のサンプル コードは、Retail SDK (...\RetailSDK\Code\POS\Extensions\SampleExtensions\ViewExtensions\SearchOrders\SampleOrderSearchTextFilter.ts) で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="ab389-252">Sample code for custom filter extensions are available in the Retail SDK (...\RetailSDK\Code\POS\Extensions\SampleExtensions\ViewExtensions\SearchOrders\SampleOrderSearchTextFilter.ts).</span></span>

## <a name="add-a-custom-column-and-an-app-bar-button"></a><span data-ttu-id="ab389-253">カスタム列とアプリ バー ボタンの追加</span><span class="sxs-lookup"><span data-stu-id="ab389-253">Add a custom column and an app bar button</span></span>

1. <span data-ttu-id="ab389-254">Microsoft Visual Studio 2015 を管理者として起動します。</span><span class="sxs-lookup"><span data-stu-id="ab389-254">Start Microsoft Visual Studio 2015 as an administrator.</span></span>
2. <span data-ttu-id="ab389-255">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="ab389-255">Open the **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="ab389-256">**POS.Extensions** プロジェクトで、**SearchExtension** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-256">In the **POS.Extensions** project, create a folder that is named **SearchExtension**.</span></span>
4. <span data-ttu-id="ab389-257">**SearchExtension** フォルダーで、**ViewExtensions** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-257">In the **SearchExtension** folder, create a folder that is named **ViewExtensions**.</span></span>
5. <span data-ttu-id="ab389-258">**ViewExtensions** フォルダーで、**Search** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-258">In the **ViewExtensions** folder, create a folder that is named **Search**.</span></span>
6. <span data-ttu-id="ab389-259">**Search** フォルダーで、**CustomCustomerSearchColumns.ts** という Typescript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-259">In the **Search** folder, create a Typescript file that is named **CustomCustomerSearchColumns.ts**.</span></span>
7. <span data-ttu-id="ab389-260">**CustomCustomerSearchColumns.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="ab389-260">In the **CustomCustomerSearchColumns.ts** file, add the following **import** statements to import the relevant entities and context.</span></span>

    ```typescript
    import { ICustomerSearchColumn } from "PosApi/Extend/Views/SearchView";
    import { ICustomColumnsContext } from "PosApi/Extend/Views/CustomListColumns";
    import { ProxyEntities } from "PosApi/Entities";
    ```

8. <span data-ttu-id="ab389-261">ファイルに既存の列とカスタム列を追加します。</span><span class="sxs-lookup"><span data-stu-id="ab389-261">Add the existing column and the custom column to the file.</span></span>

    ```typescript
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

9. <span data-ttu-id="ab389-262">ここで、列の名前のローカライズのためのリソース ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="ab389-262">You will now add the resource file for localization of the column name.</span></span> <span data-ttu-id="ab389-263">**SearchExtension** フォルダーで、**Resources** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-263">In the **SearchExtension** folder, create a folder that is named **Resources**.</span></span>
10. <span data-ttu-id="ab389-264">**Resources** フォルダーで、**Strings** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-264">In the **Resources** folder, create a folder that is named **Strings**.</span></span>
11. <span data-ttu-id="ab389-265">**Strings** フォルダーで、**en-US** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-265">In the **Strings** folder, create a folder that is named **en-US**.</span></span>
12. <span data-ttu-id="ab389-266">**en-us** フォルダーで、**resources.resjson** というファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-266">In the **en-us** folder, create a file that is named **resources.resjson**.</span></span>
13. <span data-ttu-id="ab389-267">**resources.resjson** ファイルに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ab389-267">In the **resources.resjson** file, add the following code.</span></span>

    ```typescript
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

14. <span data-ttu-id="ab389-268">**SearchExtension** フォルダーで、**DialogSample** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-268">In the **SearchExtension** folder, create a folder that is named **DialogSample**.</span></span>
15. <span data-ttu-id="ab389-269">**DialogSample** フォルダーで、**MessageDialog.ts** という TypeScript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-269">In the **DialogSample** folder, create a TypeScript file that is named **MessageDialog.ts**.</span></span>
16. <span data-ttu-id="ab389-270">**MessageDialog.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="ab389-270">In the **MessageDialog.ts** file, add the following **import** statements to import the relevant entities and context.</span></span>

    ```typescript
    import { ShowMessageDialogClientRequest, ShowMessageDialogClientResponse, IMessageDialogOptions } from "PosApi/Consume/Dialogs";
    import { IExtensionContext } from "PosApi/Framework/ExtensionContext";
    import { ClientEntities } from "PosApi/Entities";
    ```

17. <span data-ttu-id="ab389-271">**MessageDialog** という名前のクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-271">Create a class that is named **MessageDialog**.</span></span>

    ```typescript
    export default class MessageDialog {}
    ```

18. <span data-ttu-id="ab389-272">**MessageDialog** クラスで、次の **show** メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ab389-272">In the **MessageDialog** class, add the following **show** method.</span></span>

    ```typescript
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

19. <span data-ttu-id="ab389-273">ここで、選択した顧客に関する詳細を含むダイアログ ボックスを開くために、検索ビューにカスタムのアプリ バー ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="ab389-273">You will now add a custom app bar button in the search view to open a dialog box that contains details about the selected customer.</span></span> <span data-ttu-id="ab389-274">**ViewExtensions** フォルダーで、**ViewCustomerSummaryCommand.ts** という Typescript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-274">In the **ViewExtensions** folder, create a Typescript file that is named **ViewCustomerSummaryCommand.ts**.</span></span>
20. <span data-ttu-id="ab389-275">**ViewCustomerSummaryCommand.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="ab389-275">In the **ViewCustomerSummaryCommand.ts** file, add the following **import** statements to import the relevant entities and context.</span></span>

    ```typescript
    import { ProxyEntities } from "PosApi/Entities";
    import { ArrayExtensions, ObjectExtensions } from "PosApi/TypeExtensions";
    import { IExtensionCommandContext } from "PosApi/Extend/Views/AppBarCommands";
    import * as SearchView from "PosApi/Extend/Views/SearchView";
    import MessageDialog from "../../Controls/DialogSample/MessageDialog";
    ```

21. <span data-ttu-id="ab389-276">**ViewCustomerSummaryCommand** という名前のクラスを作成し、**CustomerSearchExtensionCommandBase** からクラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="ab389-276">Create a class that is named **ViewCustomerSummaryCommand**, and extend it from **CustomerSearchExtensionCommandBase**.</span></span>

    ```typescript
    export default class ViewCustomerSummaryCommand extends SearchView.CustomerSearchExtensionCommandBase {}
    ```

22. <span data-ttu-id="ab389-277">**ViewCustomerSummaryCommand** クラスで、選択した顧客を検索するときに、結果をキャプチャするプライベート変数を宣言します。</span><span class="sxs-lookup"><span data-stu-id="ab389-277">In the **ViewCustomerSummaryCommand** class, declare a private variable to capture the results when searching for the selected customer.</span></span>

    ```typescript
    private _customerSearchResults: ProxyEntities.GlobalCustomer[];
    ```

23. <span data-ttu-id="ab389-278">クラス **コンストラクター** メソッドを追加して、検索ハンドラーを初期化してクリアします。</span><span class="sxs-lookup"><span data-stu-id="ab389-278">Add the class **constructor** method to initialize and clear the search handler.</span></span>

    ```typescript
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

24. <span data-ttu-id="ab389-279">**init** メソッドを追加して、**表示** プロパティを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ab389-279">Add the **init** method to initialize the **visible** property.</span></span>

    ```typescript
    protected init(state: SearchView.ICustomerSearchExtensionCommandState): void {
        this.isVisible = true;
    }
    ```

25. <span data-ttu-id="ab389-280">アプリ ボタン クリック ハンドラーを処理する **実行** メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ab389-280">Add the **execute** method to handle the app button click handler.</span></span> <span data-ttu-id="ab389-281">**execute** メソッドは、ハンドラーから選択した顧客のデータを読み取り、単純なダイアログ ボックスに表示します。</span><span class="sxs-lookup"><span data-stu-id="ab389-281">The **execute** method reads the data for the selected customer from the handler and shows it in a simple dialog box.</span></span>

    ```typescript
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

    <span data-ttu-id="ab389-282">コード サンプルの全体は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="ab389-282">The whole code sample should look like this.</span></span>

    ```typescript
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

26. <span data-ttu-id="ab389-283">**SearchExtension** フォルダーで、**manifest.json** という JSON ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab389-283">In the **SearchExtension** folder, create a JSON file that is named **manifest.json**.</span></span>
27. <span data-ttu-id="ab389-284">**manifest.json** ファイルに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ab389-284">In the **manifest.json** file, add the following code.</span></span>

    ```typescript
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

28. <span data-ttu-id="ab389-285">**POS.Extensions** プロジェクトで **extensions.json** ファイルを開き、**SearchExtension** サンプルで更新して、POS が実行時にこの拡張機能に含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="ab389-285">In the **POS.Extensions** project, open the **extensions.json** file, and update it with **SearchExtension** samples, so that the POS includes this extension at runtime.</span></span>

    ```typescript
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

29. <span data-ttu-id="ab389-286">**tsconfig.json** ファイルで、除外リストに拡張パッケージ フォルダーをコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="ab389-286">In the **tsconfig.json** file, comment out the extension package folders in the exclude list.</span></span> <span data-ttu-id="ab389-287">POS は、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="ab389-287">The POS uses this file to include or exclude the extension.</span></span> <span data-ttu-id="ab389-288">既定では、リストに除外された拡張リスト全体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab389-288">By default, the list contains the whole excluded extensions list.</span></span> <span data-ttu-id="ab389-289">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、除外リストの拡張子をコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="ab389-289">To include an extension as part of the POS, add the name of the extension folder, and comment out the extension in the exclude list, as shown here.</span></span>

    ```typescript
    "exclude": [
    "SampleExtensions"
    //"SampleExtensions2",
    //"SearchExtension"
    ],
    ```

30. <span data-ttu-id="ab389-290">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="ab389-290">Compile and rebuild the project.</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="ab389-291">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="ab389-291">Validate the customization</span></span>

<span data-ttu-id="ab389-292">カスタマイズを検証するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ab389-292">Follow these steps to validate the customization.</span></span>

1. <span data-ttu-id="ab389-293">オペレーター ID に **000160**、パスワードに **123** を使用して Modern POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="ab389-293">Sign in to Modern POS by using **000160** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="ab389-294">上部の検索バーを使って顧客 **2001** を検索します。</span><span class="sxs-lookup"><span data-stu-id="ab389-294">Search for customer **2001** by using the search bar on the top.</span></span>

    <span data-ttu-id="ab389-295">追加したカスタム列が表示されました。</span><span class="sxs-lookup"><span data-stu-id="ab389-295">You should see the custom columns that you added.</span></span>

3. <span data-ttu-id="ab389-296">顧客を選択し、新しいアプリケーション バーのボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ab389-296">Select a customer, and then select the new app bar button.</span></span> <span data-ttu-id="ab389-297">選択した顧客に関する詳細を含むダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab389-297">A dialog box should appear that contains details about the selected customer.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
