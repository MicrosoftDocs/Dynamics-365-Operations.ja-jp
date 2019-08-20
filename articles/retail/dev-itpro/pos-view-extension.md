---
title: POS ビューの拡張によるカスタム列およびアプリ バー ボタンの追加
description: このトピックでは、[顧客の追加/編集] 画面などの既存の POS ビューを拡張する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 04/26/2019
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
ms.openlocfilehash: c4951a8b556e0b7f59911277e02fa44ba4d97920
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833131"
---
# <a name="extend-pos-views-to-add-custom-columns-and-app-bar-buttons"></a><span data-ttu-id="9154b-103">POS ビューの拡張によるカスタム列およびアプリ バー ボタンの追加</span><span class="sxs-lookup"><span data-stu-id="9154b-103">Extend POS views to add custom columns and app bar buttons</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9154b-104">このトピックでは、既存の [販売時点管理 (POS)] ビューを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9154b-104">This topic explains how you can extend existing point of sale (POS) views.</span></span> <span data-ttu-id="9154b-105">**トランザクション** 画面および **ようこそ** 画面を拡張するには、画面レイアウト デザイナーを使用します。</span><span class="sxs-lookup"><span data-stu-id="9154b-105">To extend the **Transaction** screen and **Welcome** screen, you can use the screen layout designer.</span></span> <span data-ttu-id="9154b-106">**顧客の追加/編集** 画面など、他のすべての POS ビューを拡張するには、Retail ソフトウェア開発キット (SDK) を使用します。</span><span class="sxs-lookup"><span data-stu-id="9154b-106">To extend all other POS views, such as the **Customer Add/Edit** screen, you use the Retail software development kit (SDK).</span></span> <span data-ttu-id="9154b-107">このトピックでは、Retail SDK による既存の POS ビューの拡張について説明します。</span><span class="sxs-lookup"><span data-stu-id="9154b-107">This topic focuses on the extension of existing POS views via the Retail SDK.</span></span>

> [!NOTE]
> <span data-ttu-id="9154b-108">このトピックでは Microsoft Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 for Retail プラットフォーム更新 8 と Retail アプリ更新プログラム 4 修正プログラムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="9154b-108">This topic applies to Microsoft Dynamics 365 for Finance and Operations, and to Microsoft Dynamics 365 for Retail with platform update 8 and Retail App update 4 hotfix.</span></span>

<span data-ttu-id="9154b-109">POS ビューでは、次の拡張ポイントとパターンがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="9154b-109">POS views support the following extension points and patterns:</span></span>

- <span data-ttu-id="9154b-110">**カスタム アプリケーション バーのボタン** - 選択したページのアプリケーション バーにカスタム ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="9154b-110">**Custom app bar buttons** – Add custom buttons to the app bar on selected pages.</span></span>
- <span data-ttu-id="9154b-111">**カスタム列セット** - 選択したページのグリッド列をカスタム列に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="9154b-111">**Custom column sets** – Replace the grid columns with custom columns on selected pages.</span></span>
- <span data-ttu-id="9154b-112">**カスタム コントロール** - 選択したページに、新しいコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="9154b-112">**Custom controls** – Add new controls to selected pages.</span></span>

## <a name="pos-views-that-currently-support-extensions"></a><span data-ttu-id="9154b-113">現在拡張機能をサポートする POS ビュー</span><span class="sxs-lookup"><span data-stu-id="9154b-113">POS views that currently support extensions</span></span>

<span data-ttu-id="9154b-114">次のテーブルに、現在拡張機能をサポートしている POS ビューを示します。</span><span class="sxs-lookup"><span data-stu-id="9154b-114">The following table shows the POS views that currently support extensions.</span></span> <span data-ttu-id="9154b-115">また、各 POS ビューがサポートする拡張ポイントのタイプも示します。</span><span class="sxs-lookup"><span data-stu-id="9154b-115">It also indicates the types of extension points that each POS view supports.</span></span>

> [!NOTE]
> <span data-ttu-id="9154b-116">今後のリリースと修正プログラムで、他のビューの拡張ポイントをさらにサポートします。</span><span class="sxs-lookup"><span data-stu-id="9154b-116">The upcoming releases and hotfix will add support for more extension points in other views.</span></span>


| <span data-ttu-id="9154b-117">POS ビュー</span><span class="sxs-lookup"><span data-stu-id="9154b-117">POS view</span></span>                        | <span data-ttu-id="9154b-118">カスタム コントロールがサポートされています</span><span class="sxs-lookup"><span data-stu-id="9154b-118">Custom controls are supported</span></span> | <span data-ttu-id="9154b-119">カスタム列がサポートされています</span><span class="sxs-lookup"><span data-stu-id="9154b-119">Custom columns are supported</span></span> | <span data-ttu-id="9154b-120">カスタムのアプリ バーのボタンがサポートされています</span><span class="sxs-lookup"><span data-stu-id="9154b-120">Custom app bar buttons are supported</span></span> |
|---------------------------------|-------------------------------|------------------------------|--------------------------------------|
| <span data-ttu-id="9154b-121">カート ビュー (画面レイアウトに基づく)</span><span class="sxs-lookup"><span data-stu-id="9154b-121">Cart view (Screen layout based)</span></span> | <span data-ttu-id="9154b-122">有</span><span class="sxs-lookup"><span data-stu-id="9154b-122">Yes</span></span>                           | <span data-ttu-id="9154b-123">有</span><span class="sxs-lookup"><span data-stu-id="9154b-123">Yes</span></span>                          | <span data-ttu-id="9154b-124">無</span><span class="sxs-lookup"><span data-stu-id="9154b-124">No</span></span>                                   |
| <span data-ttu-id="9154b-125">CustomerAddEditView</span><span class="sxs-lookup"><span data-stu-id="9154b-125">CustomerAddEditView</span></span>             | <span data-ttu-id="9154b-126">有</span><span class="sxs-lookup"><span data-stu-id="9154b-126">Yes</span></span>                           | <span data-ttu-id="9154b-127">無</span><span class="sxs-lookup"><span data-stu-id="9154b-127">No</span></span>                           | <span data-ttu-id="9154b-128">有</span><span class="sxs-lookup"><span data-stu-id="9154b-128">Yes</span></span>                                  |
| <span data-ttu-id="9154b-129">CustomerDetailsView</span><span class="sxs-lookup"><span data-stu-id="9154b-129">CustomerDetailsView</span></span>             | <span data-ttu-id="9154b-130">有</span><span class="sxs-lookup"><span data-stu-id="9154b-130">Yes</span></span>                           | <span data-ttu-id="9154b-131">無</span><span class="sxs-lookup"><span data-stu-id="9154b-131">No</span></span>                           | <span data-ttu-id="9154b-132">有</span><span class="sxs-lookup"><span data-stu-id="9154b-132">Yes</span></span>                                  |
| <span data-ttu-id="9154b-133">SearchView</span><span class="sxs-lookup"><span data-stu-id="9154b-133">SearchView</span></span>                      | <span data-ttu-id="9154b-134">無</span><span class="sxs-lookup"><span data-stu-id="9154b-134">No</span></span>                            | <span data-ttu-id="9154b-135">有</span><span class="sxs-lookup"><span data-stu-id="9154b-135">Yes</span></span>                          | <span data-ttu-id="9154b-136">有</span><span class="sxs-lookup"><span data-stu-id="9154b-136">Yes</span></span>                                  |
| <span data-ttu-id="9154b-137">InventoryLookupView</span><span class="sxs-lookup"><span data-stu-id="9154b-137">InventoryLookupView</span></span>             | <span data-ttu-id="9154b-138">無</span><span class="sxs-lookup"><span data-stu-id="9154b-138">No</span></span>                            | <span data-ttu-id="9154b-139">有</span><span class="sxs-lookup"><span data-stu-id="9154b-139">Yes</span></span>                          | <span data-ttu-id="9154b-140">有</span><span class="sxs-lookup"><span data-stu-id="9154b-140">Yes</span></span>                                  |
| <span data-ttu-id="9154b-141">ShowJournalView</span><span class="sxs-lookup"><span data-stu-id="9154b-141">ShowJournalView</span></span>                 | <span data-ttu-id="9154b-142">無</span><span class="sxs-lookup"><span data-stu-id="9154b-142">No</span></span>                            | <span data-ttu-id="9154b-143">有</span><span class="sxs-lookup"><span data-stu-id="9154b-143">Yes</span></span>                          | <span data-ttu-id="9154b-144">有</span><span class="sxs-lookup"><span data-stu-id="9154b-144">Yes</span></span>                                  |
| <span data-ttu-id="9154b-145">SimpleProductDetailsView</span><span class="sxs-lookup"><span data-stu-id="9154b-145">SimpleProductDetailsView</span></span>        | <span data-ttu-id="9154b-146">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-146">Yes</span></span>                           | <span data-ttu-id="9154b-147">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-147">No</span></span>                           | <span data-ttu-id="9154b-148">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-148">Yes</span></span>                                  |
| <span data-ttu-id="9154b-149">AddressAddEditView</span><span class="sxs-lookup"><span data-stu-id="9154b-149">AddressAddEditView</span></span>              | <span data-ttu-id="9154b-150">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-150">Yes</span></span>                           | <span data-ttu-id="9154b-151">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-151">No</span></span>                           | <span data-ttu-id="9154b-152">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-152">Yes</span></span>                                    |
| <span data-ttu-id="9154b-153">PaymentView</span><span class="sxs-lookup"><span data-stu-id="9154b-153">PaymentView</span></span>                     | <span data-ttu-id="9154b-154">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-154">No</span></span>                            | <span data-ttu-id="9154b-155">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-155">No</span></span>                           | <span data-ttu-id="9154b-156">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-156">Yes</span></span>                                  |
| <span data-ttu-id="9154b-157">PriceCheckView</span><span class="sxs-lookup"><span data-stu-id="9154b-157">PriceCheckView</span></span>                  | <span data-ttu-id="9154b-158">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-158">Yes</span></span>                           | <span data-ttu-id="9154b-159">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-159">No</span></span>                           | <span data-ttu-id="9154b-160">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-160">No</span></span>                                   |
| <span data-ttu-id="9154b-161">SearchOrdersView</span><span class="sxs-lookup"><span data-stu-id="9154b-161">SearchOrdersView</span></span>                | <span data-ttu-id="9154b-162">無</span><span class="sxs-lookup"><span data-stu-id="9154b-162">No</span></span>                            | <span data-ttu-id="9154b-163">有</span><span class="sxs-lookup"><span data-stu-id="9154b-163">Yes</span></span>                          | <span data-ttu-id="9154b-164">無</span><span class="sxs-lookup"><span data-stu-id="9154b-164">No</span></span>                                   |
| <span data-ttu-id="9154b-165">SearchPickingAndReceivingView</span><span class="sxs-lookup"><span data-stu-id="9154b-165">SearchPickingAndReceivingView</span></span>   | <span data-ttu-id="9154b-166">無</span><span class="sxs-lookup"><span data-stu-id="9154b-166">No</span></span>                            | <span data-ttu-id="9154b-167">有</span><span class="sxs-lookup"><span data-stu-id="9154b-167">Yes</span></span>                          | <span data-ttu-id="9154b-168">有</span><span class="sxs-lookup"><span data-stu-id="9154b-168">Yes</span></span>                                   |
| <span data-ttu-id="9154b-169">CustomerOrderHistoryView</span><span class="sxs-lookup"><span data-stu-id="9154b-169">CustomerOrderHistoryView</span></span>        | <span data-ttu-id="9154b-170">無</span><span class="sxs-lookup"><span data-stu-id="9154b-170">No</span></span>                            | <span data-ttu-id="9154b-171">有</span><span class="sxs-lookup"><span data-stu-id="9154b-171">Yes</span></span>                          | <span data-ttu-id="9154b-172">無</span><span class="sxs-lookup"><span data-stu-id="9154b-172">No</span></span>                                   |
| <span data-ttu-id="9154b-173">SearchStockCountView</span><span class="sxs-lookup"><span data-stu-id="9154b-173">SearchStockCountView</span></span>            | <span data-ttu-id="9154b-174">無</span><span class="sxs-lookup"><span data-stu-id="9154b-174">No</span></span>                            | <span data-ttu-id="9154b-175">有</span><span class="sxs-lookup"><span data-stu-id="9154b-175">Yes</span></span>                          | <span data-ttu-id="9154b-176">無</span><span class="sxs-lookup"><span data-stu-id="9154b-176">No</span></span>                                   |
| <span data-ttu-id="9154b-177">StockCountDetailsView</span><span class="sxs-lookup"><span data-stu-id="9154b-177">StockCountDetailsView</span></span>           | <span data-ttu-id="9154b-178">無</span><span class="sxs-lookup"><span data-stu-id="9154b-178">No</span></span>                            | <span data-ttu-id="9154b-179">有</span><span class="sxs-lookup"><span data-stu-id="9154b-179">Yes</span></span>                          | <span data-ttu-id="9154b-180">無</span><span class="sxs-lookup"><span data-stu-id="9154b-180">No</span></span>                                   |
| <span data-ttu-id="9154b-181">ResumeCartView</span><span class="sxs-lookup"><span data-stu-id="9154b-181">ResumeCartView</span></span>                  | <span data-ttu-id="9154b-182">無</span><span class="sxs-lookup"><span data-stu-id="9154b-182">No</span></span>                            | <span data-ttu-id="9154b-183">有</span><span class="sxs-lookup"><span data-stu-id="9154b-183">Yes</span></span>                          | <span data-ttu-id="9154b-184">無</span><span class="sxs-lookup"><span data-stu-id="9154b-184">No</span></span>                                    |
| <span data-ttu-id="9154b-185">OrderFulfillmentView</span><span class="sxs-lookup"><span data-stu-id="9154b-185">OrderFulfillmentView</span></span>            | <span data-ttu-id="9154b-186">無</span><span class="sxs-lookup"><span data-stu-id="9154b-186">No</span></span>                            | <span data-ttu-id="9154b-187">無</span><span class="sxs-lookup"><span data-stu-id="9154b-187">No</span></span>                           | <span data-ttu-id="9154b-188">有</span><span class="sxs-lookup"><span data-stu-id="9154b-188">Yes</span></span>                                   |
| <span data-ttu-id="9154b-189">InventoryLookupMatrixView</span><span class="sxs-lookup"><span data-stu-id="9154b-189">InventoryLookupMatrixView</span></span>       | <span data-ttu-id="9154b-190">無</span><span class="sxs-lookup"><span data-stu-id="9154b-190">No</span></span>                            | <span data-ttu-id="9154b-191">無</span><span class="sxs-lookup"><span data-stu-id="9154b-191">No</span></span>                           | <span data-ttu-id="9154b-192">有</span><span class="sxs-lookup"><span data-stu-id="9154b-192">Yes</span></span>                                   |
| <span data-ttu-id="9154b-193">SuspendTransactionView</span><span class="sxs-lookup"><span data-stu-id="9154b-193">SuspendTransactionView</span></span>          | <span data-ttu-id="9154b-194">無</span><span class="sxs-lookup"><span data-stu-id="9154b-194">No</span></span>                            | <span data-ttu-id="9154b-195">有</span><span class="sxs-lookup"><span data-stu-id="9154b-195">Yes</span></span>                          | <span data-ttu-id="9154b-196">無</span><span class="sxs-lookup"><span data-stu-id="9154b-196">No</span></span>                               |   
| <span data-ttu-id="9154b-197">ManageShiftView</span><span class="sxs-lookup"><span data-stu-id="9154b-197">ManageShiftView</span></span>                 | <span data-ttu-id="9154b-198">無</span><span class="sxs-lookup"><span data-stu-id="9154b-198">No</span></span>                            | <span data-ttu-id="9154b-199">無</span><span class="sxs-lookup"><span data-stu-id="9154b-199">No</span></span>                           | <span data-ttu-id="9154b-200">有</span><span class="sxs-lookup"><span data-stu-id="9154b-200">Yes</span></span>                               |  
| <span data-ttu-id="9154b-201">ReportDetailsView</span><span class="sxs-lookup"><span data-stu-id="9154b-201">ReportDetailsView</span></span>               | <span data-ttu-id="9154b-202">無</span><span class="sxs-lookup"><span data-stu-id="9154b-202">No</span></span>                            | <span data-ttu-id="9154b-203">無</span><span class="sxs-lookup"><span data-stu-id="9154b-203">No</span></span>                           | <span data-ttu-id="9154b-204">有</span><span class="sxs-lookup"><span data-stu-id="9154b-204">Yes</span></span>                               |
| <span data-ttu-id="9154b-205">SearchReceiptsView</span><span class="sxs-lookup"><span data-stu-id="9154b-205">SearchReceiptsView</span></span>              | <span data-ttu-id="9154b-206">無</span><span class="sxs-lookup"><span data-stu-id="9154b-206">No</span></span>                            | <span data-ttu-id="9154b-207">無</span><span class="sxs-lookup"><span data-stu-id="9154b-207">No</span></span>                           | <span data-ttu-id="9154b-208">有</span><span class="sxs-lookup"><span data-stu-id="9154b-208">Yes</span></span>                               |
| <span data-ttu-id="9154b-209">StockCountDetailsView</span><span class="sxs-lookup"><span data-stu-id="9154b-209">StockCountDetailsView</span></span>           | <span data-ttu-id="9154b-210">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-210">No</span></span>                            | <span data-ttu-id="9154b-211">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-211">No</span></span>                           | <span data-ttu-id="9154b-212">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-212">Yes</span></span>                               |
| <span data-ttu-id="9154b-213">TransferOrderDetailsView</span><span class="sxs-lookup"><span data-stu-id="9154b-213">TransferOrderDetailsView</span></span>        | <span data-ttu-id="9154b-214">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-214">No</span></span>                            | <span data-ttu-id="9154b-215">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-215">No</span></span>                           | <span data-ttu-id="9154b-216">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-216">Yes</span></span>                               |
| <span data-ttu-id="9154b-217">FulfillmentLineView</span><span class="sxs-lookup"><span data-stu-id="9154b-217">FulfillmentLineView</span></span>             | <span data-ttu-id="9154b-218">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-218">No</span></span>                            | <span data-ttu-id="9154b-219">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-219">Yes</span></span>                          | <span data-ttu-id="9154b-220">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-220">No</span></span>                               |
| <span data-ttu-id="9154b-221">ReturnTransactionView</span><span class="sxs-lookup"><span data-stu-id="9154b-221">ReturnTransactionView</span></span>           | <span data-ttu-id="9154b-222">いいえ</span><span class="sxs-lookup"><span data-stu-id="9154b-222">No</span></span>                            | <span data-ttu-id="9154b-223">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-223">Yes</span></span>                          | <span data-ttu-id="9154b-224">はい</span><span class="sxs-lookup"><span data-stu-id="9154b-224">Yes</span></span>                               |


> [!NOTE]
> <span data-ttu-id="9154b-225">上記に表示される表は、リリースされた最新バージョンおよび修正プログラムに基づいて更新されています。</span><span class="sxs-lookup"><span data-stu-id="9154b-225">The table shown above is updated based on the latest released version and hotfix.</span></span> <span data-ttu-id="9154b-226">旧バージョンでは、これらの拡張ポイントの一部は使用できません。</span><span class="sxs-lookup"><span data-stu-id="9154b-226">In earlier versions, some of these extension points will not be available.</span></span>

> [!NOTE]
> <span data-ttu-id="9154b-227">仕訳帳の表示 (行グリッド) と 返品トランザクション ビューのカスタム列は、行サブ フィールドの使用をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9154b-227">In Show journal (lines grid) and Return transaction view custom columns are supported using the row sub fields.</span></span> <span data-ttu-id="9154b-228">これらのサブ フィールドは、情報コード メッセージ、シリアル番号、割引の値などのように、列ではなく行として表示されます。</span><span class="sxs-lookup"><span data-stu-id="9154b-228">These sub fields will be displayed as rows instead of columns, like the info code messages or serial number or discounts values.</span></span>

<span data-ttu-id="9154b-229">フィルターの拡張機能は**仕訳帳ビューを表示**および**注文ビューを検索**でもサポートされ、カスタム フィルターを追加します。</span><span class="sxs-lookup"><span data-stu-id="9154b-229">Filter extensions are also supported in **Show journal view** and **Search order views** to add custom filters.</span></span> <span data-ttu-id="9154b-230">**注文ビューを検索** は拡張機能を使用してユーザー インターフェイス (UI) に検索用の既定パラメーターを設定することもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9154b-230">**Search order views** also supports setting default parameters for search in the user interface (UI) using extension.</span></span> <span data-ttu-id="9154b-231">たとえば、既定のストア検索パラメータを追加する場合は、拡張機能を使用して UI に表示することでそれを実行できます。</span><span class="sxs-lookup"><span data-stu-id="9154b-231">For example, if you want to add default store search parameter you can do that by using extension and showing that in the UI.</span></span> 

## <a name="add-a-custom-column-and-an-app-bar-button"></a><span data-ttu-id="9154b-232">カスタム列とアプリ バー ボタンの追加</span><span class="sxs-lookup"><span data-stu-id="9154b-232">Add a custom column and an app bar button</span></span>

1. <span data-ttu-id="9154b-233">Microsoft Visual Studio 2015 を管理者として起動します。</span><span class="sxs-lookup"><span data-stu-id="9154b-233">Start Microsoft Visual Studio 2015 as an administrator.</span></span>
2. <span data-ttu-id="9154b-234">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="9154b-234">Open the **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="9154b-235">**POS.Extensions** プロジェクトで、**SearchExtension** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-235">In the **POS.Extensions** project, create a folder that is named **SearchExtension**.</span></span>
4. <span data-ttu-id="9154b-236">**SearchExtension** フォルダーで、**ViewExtensions** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-236">In the **SearchExtension** folder, create a folder that is named **ViewExtensions**.</span></span>
5. <span data-ttu-id="9154b-237">**ViewExtensions** フォルダーで、**Search** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-237">In the **ViewExtensions** folder, create a folder that is named **Search**.</span></span>
6. <span data-ttu-id="9154b-238">**Search** フォルダーで、**CustomCustomerSearchColumns.ts** という Typescript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-238">In the **Search** folder, create a Typescript file that is named **CustomCustomerSearchColumns.ts**.</span></span>
7. <span data-ttu-id="9154b-239">**CustomCustomerSearchColumns.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9154b-239">In the **CustomCustomerSearchColumns.ts** file, add the following **import** statements to import the relevant entities and context.</span></span>

    ```Typescript
    import { ICustomerSearchColumn } from "PosApi/Extend/Views/SearchView";
    import { ICustomColumnsContext } from "PosApi/Extend/Views/CustomListColumns";
    import { ProxyEntities } from "PosApi/Entities";
    ```

8. <span data-ttu-id="9154b-240">ファイルに既存の列とカスタム列を追加します。</span><span class="sxs-lookup"><span data-stu-id="9154b-240">Add the existing column and the custom column to the file.</span></span>

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

9. <span data-ttu-id="9154b-241">ここで、列の名前のローカライズのためのリソース ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="9154b-241">You will now add the resource file for localization of the column name.</span></span> <span data-ttu-id="9154b-242">**SearchExtension** フォルダーで、**Resources** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-242">In the **SearchExtension** folder, create a folder that is named **Resources**.</span></span>
10. <span data-ttu-id="9154b-243">**Resources** フォルダーで、**Strings** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-243">In the **Resources** folder, create a folder that is named **Strings**.</span></span>
11. <span data-ttu-id="9154b-244">**Strings** フォルダーで、**en-US** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-244">In the **Strings** folder, create a folder that is named **en-US**.</span></span>
12. <span data-ttu-id="9154b-245">**en-us** フォルダーで、**resources.resjson** というファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-245">In the **en-us** folder, create a file that is named **resources.resjson**.</span></span>
13. <span data-ttu-id="9154b-246">**resources.resjson** ファイルに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="9154b-246">In the **resources.resjson** file, add the following code.</span></span>

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

14. <span data-ttu-id="9154b-247">**SearchExtension** フォルダーで、**DialogSample** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-247">In the **SearchExtension** folder, create a folder that is named **DialogSample**.</span></span>
15. <span data-ttu-id="9154b-248">**DialogSample** フォルダーで、**MessageDialog.ts** という Typescript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-248">In the **DialogSample** folder, create a Typescript file that is named **MessageDialog.ts**.</span></span>
16. <span data-ttu-id="9154b-249">**MessageDialog.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9154b-249">In the **MessageDialog.ts** file, add the following **import** statements to import the relevant entities and context.</span></span>

    ```Typescript
    import { ShowMessageDialogClientRequest, ShowMessageDialogClientResponse, IMessageDialogOptions } from "PosApi/Consume/Dialogs";
    import { IExtensionContext } from "PosApi/Framework/ExtensionContext";
    import { ClientEntities } from "PosApi/Entities";
    ```

17. <span data-ttu-id="9154b-250">**MessageDialog** という名前のクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-250">Create a class that is named **MessageDialog**.</span></span>

    ```Typescript
    export default class MessageDialog {}
    ```

18. <span data-ttu-id="9154b-251">**MessageDialog** クラスで、次の **show** メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="9154b-251">In the **MessageDialog** class, add the following **show** method.</span></span>

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

19. <span data-ttu-id="9154b-252">ここで、選択した顧客に関する詳細を含むダイアログ ボックスを開くために、検索ビューにカスタムのアプリ バー ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="9154b-252">You will now add a custom app bar button in the search view to open a dialog box that contains details about the selected customer.</span></span> <span data-ttu-id="9154b-253">**ViewExtensions** フォルダーで、**ViewCustomerSummaryCommand.ts** という Typescript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-253">In the **ViewExtensions** folder, create a Typescript file that is named **ViewCustomerSummaryCommand.ts**.</span></span>
20. <span data-ttu-id="9154b-254">**ViewCustomerSummaryCommand.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9154b-254">In the **ViewCustomerSummaryCommand.ts** file, add the following **import** statements to import the relevant entities and context.</span></span>

    ```Typescript
    import { ProxyEntities } from "PosApi/Entities";
    import { ArrayExtensions, ObjectExtensions } from "PosApi/TypeExtensions";
    import { IExtensionCommandContext } from "PosApi/Extend/Views/AppBarCommands";
    import * as SearchView from "PosApi/Extend/Views/SearchView";
    import MessageDialog from "../DialogSample/MessageDialog";
    ```

21. <span data-ttu-id="9154b-255">**ViewCustomerSummaryCommand** という名前のクラスを作成し、**CustomerSearchExtensionCommandBase** からクラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9154b-255">Create a class that is named **ViewCustomerSummaryCommand**, and extend it from **CustomerSearchExtensionCommandBase**.</span></span>

    ```Typescript
    export default class ViewCustomerSummaryCommand extends SearchView.CustomerSearchExtensionCommandBase {}
    ```

22. <span data-ttu-id="9154b-256">**ViewCustomerSummaryCommand** クラスで、選択した顧客を検索するときに、結果をキャプチャするプライベート変数を宣言します。</span><span class="sxs-lookup"><span data-stu-id="9154b-256">In the **ViewCustomerSummaryCommand** class, declare a private variable to capture the results when searching for the selected customer.</span></span>

    ```Typescript
    private _customerSearchResults: ProxyEntities.GlobalCustomer[];
    ```

23. <span data-ttu-id="9154b-257">クラス **コンストラクター** メソッドを追加して、検索ハンドラーを初期化してクリアします。</span><span class="sxs-lookup"><span data-stu-id="9154b-257">Add the class **constructor** method to initialize and clear the search handler.</span></span>

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

24. <span data-ttu-id="9154b-258">**init** メソッドを追加して、**表示**プロパティを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9154b-258">Add the **init** method to initialize the **visible** property.</span></span>

    ```Typescript
    protected init(state: SearchView.ICustomerSearchExtensionCommandState): void {
        this.isVisible = true;
    }
    ```

25. <span data-ttu-id="9154b-259">アプリ ボタン クリック ハンドラーを処理する**実行**メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="9154b-259">Add the **execute** method to handle the app button click handler.</span></span> <span data-ttu-id="9154b-260">**execute** メソッドは、ハンドラーから選択した顧客のデータを読み取り、単純なダイアログ ボックスに表示します。</span><span class="sxs-lookup"><span data-stu-id="9154b-260">The **execute** method reads the data for the selected customer from the handler and shows it in a simple dialog box.</span></span>

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

    <span data-ttu-id="9154b-261">コード サンプルの全体は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9154b-261">The whole code sample should look like this.</span></span>

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

26. <span data-ttu-id="9154b-262">**SearchExtension** フォルダーで、**manifest.json** という JSON ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9154b-262">In the **SearchExtension** folder, create a JSON file that is named **manifest.json**.</span></span>
27. <span data-ttu-id="9154b-263">**manifest.json** ファイルに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="9154b-263">In the **manifest.json** file, add the following code.</span></span>

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

28. <span data-ttu-id="9154b-264">**POS.Extensions** プロジェクトで **extensions.json** ファイルを開き、**SearchExtension** サンプルで更新して、POS が実行時にこの拡張機能に含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="9154b-264">In the **POS.Extensions** project, open the **extensions.json** file, and update it with **SearchExtension** samples, so that the POS includes this extension at runtime.</span></span>

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

29. <span data-ttu-id="9154b-265">**tsconfig.json** ファイルで、除外リストに拡張パッケージ フォルダーをコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="9154b-265">In the **tsconfig.json** file, comment out the extension package folders in the exclude list.</span></span> <span data-ttu-id="9154b-266">POS は、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="9154b-266">The POS uses this file to include or exclude the extension.</span></span> <span data-ttu-id="9154b-267">既定では、リストに除外された拡張リスト全体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9154b-267">By default, the list contains the whole excluded extensions list.</span></span> <span data-ttu-id="9154b-268">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、除外リストの拡張子をコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="9154b-268">To include an extension as part of the POS, add the name of the extension folder, and comment out the extension in the exclude list, as shown here.</span></span>

    ```Typescript
    "exclude": [
    "SampleExtensions"
    //"SampleExtensions2",
    //"SearchExtension"
    ],
    ```

30. <span data-ttu-id="9154b-269">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="9154b-269">Compile and rebuild the project.</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="9154b-270">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="9154b-270">Validate the customization</span></span>

<span data-ttu-id="9154b-271">カスタマイズを検証するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9154b-271">Follow these steps to validate the customization.</span></span>

1. <span data-ttu-id="9154b-272">オペレーター ID に **000160**、パスワードに **123** を使用して Retail Modern POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="9154b-272">Sign in to Retail Modern POS by using **000160** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="9154b-273">上部の検索バーを使って顧客 **2001** を検索します。</span><span class="sxs-lookup"><span data-stu-id="9154b-273">Search for customer **2001** by using the search bar on the top.</span></span>

    <span data-ttu-id="9154b-274">追加したカスタム列が表示されました。</span><span class="sxs-lookup"><span data-stu-id="9154b-274">You should see the custom columns that you added.</span></span>

3. <span data-ttu-id="9154b-275">顧客を選択し、新しいアプリケーション バーのボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9154b-275">Select a customer, and then select the new app bar button.</span></span> <span data-ttu-id="9154b-276">選択した顧客に関する詳細を含むダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9154b-276">A dialog box should appear that contains details about the selected customer.</span></span>
