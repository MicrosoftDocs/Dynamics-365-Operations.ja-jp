---
title: "オフライン モードの Retail Modern POS (MPOS)"
description: "この記事では、Retail サーバーが利用できない場合に、オフライン モードで Retail Modern POS デバイスを使用する方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 31441
ms.assetid: 219f93a3-6321-46e9-b989-f97072af0bb3
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: f0e5e7131bf5d6f337b2197f2aa56056870b8a95
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="retail-modern-pos-mpos-in-offline-mode"></a><span data-ttu-id="73d17-103">オフライン モードの Retail Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="73d17-103">Retail Modern POS (MPOS) in offline mode</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73d17-104">この記事では、Retail サーバーが利用できない場合に、オフライン モードで Retail Modern POS デバイスを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="73d17-104">This article explains how to use Retail Modern POS devices in offline mode if the Retail Server is unavailable.</span></span>

<span data-ttu-id="73d17-105">Retail サーバーが利用できない場合、Retail Modern POS はオフラインになります。</span><span class="sxs-lookup"><span data-stu-id="73d17-105">A Retail Modern POS device will go offline if the Retail Server is unavailable.</span></span> <span data-ttu-id="73d17-106">Retail サーバーとの接続が失われると、販売時点管理 (POS) はオフライン データベースに自動的に接続されます。</span><span class="sxs-lookup"><span data-stu-id="73d17-106">When the connection with the Retail Server is lost, the point of sale (POS) automatically switches to the offline database.</span></span> <span data-ttu-id="73d17-107">オフライン プロファイルでコンフィギュレーションされたタイムアウトの間隔内でデータの要求が成功しない場合、Retail Modern POS は自動的にオフライン データベースに切り替わり、販売トランザクションを続行します。</span><span class="sxs-lookup"><span data-stu-id="73d17-107">If a data request doesn't succeed within the time-out interval that is configured in the offline profile, Retail Modern POS automatically switches to the offline database and continues the sales transaction.</span></span> <span data-ttu-id="73d17-108">Retail Modern POS はオフライン プロファイルでコンフィギュレーションされた再接続試行間隔の後に Retail Server への再接続を試みます。</span><span class="sxs-lookup"><span data-stu-id="73d17-108">Retail Modern POS will try to reconnect to the Retail Server after the reconnect attempt interval that is configured in the offline profile.</span></span> <span data-ttu-id="73d17-109">この再接続の試みは、トランザクションの開始時にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="73d17-109">This reconnect attempt will occur only at the beginning of a transaction.</span></span>

## <a name="determine-the-connection-mode-of-retail-modern-pos"></a><span data-ttu-id="73d17-110">Retail Modern POS の接続モードを決定する</span><span class="sxs-lookup"><span data-stu-id="73d17-110">Determine the connection mode of Retail Modern POS</span></span>
<span data-ttu-id="73d17-111">Retail Modern POS のステータス ヘッダーは、現在の接続状態を示します。</span><span class="sxs-lookup"><span data-stu-id="73d17-111">The status header of Retail Modern POS indicates the current connection status.</span></span> 

<span data-ttu-id="73d17-112">[![接続](./media/connection.png)](./media/connection.png)</span><span class="sxs-lookup"><span data-stu-id="73d17-112">[![connection](./media/connection.png)](./media/connection.png)</span></span> 

<span data-ttu-id="73d17-113">Retail Modern POS の **接続ステータス** ページには、オフライン データベースと同期する前回の試みのステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d17-113">The **Connection status** page in Retail Modern POS shows the status of the last attempt to synchronize with the offline database.</span></span> 

<span data-ttu-id="73d17-114">[![接続ステータス](./media/connection-status.png)](./media/connection-status.png)</span><span class="sxs-lookup"><span data-stu-id="73d17-114">[![connection status](./media/connection-status.png)](./media/connection-status.png)</span></span>

## <a name="create-a-button-to-manually-switch-between-online-and-offline-modes"></a><span data-ttu-id="73d17-115">手動でオンラインとオフライン モードを切り替えるためのボタンを作成</span><span class="sxs-lookup"><span data-stu-id="73d17-115">Create a button to manually switch between online and offline modes</span></span>
<span data-ttu-id="73d17-116">Retail Modern POS にオンラインとオフライン モードを手動で切り替えるボタンを追加できます。</span><span class="sxs-lookup"><span data-stu-id="73d17-116">You can add a button to Retail Modern POS to manually switch between online and offline modes.</span></span> <span data-ttu-id="73d17-117">**POS 操作 917 – データベース接続ステータス**のボタンを作成します。</span><span class="sxs-lookup"><span data-stu-id="73d17-117">Create a button for **POS operation 917 – Database connection status**.</span></span> <span data-ttu-id="73d17-118">接続または切断するには、ボタンをトグルとして切り替えて使用します。</span><span class="sxs-lookup"><span data-stu-id="73d17-118">Use the button as a toggle to connect or disconnect.</span></span>

## <a name="operations-that-can-be-completed-when-the-channel-database-is-offline"></a><span data-ttu-id="73d17-119">チャネル データベースがオフラインのときに実行できる操作</span><span class="sxs-lookup"><span data-stu-id="73d17-119">Operations that can be completed when the channel database is offline</span></span>
<span data-ttu-id="73d17-120">チャネル データベースがオフラインときは、次の操作を完了することができます。</span><span class="sxs-lookup"><span data-stu-id="73d17-120">You can complete the following operations when the channel database is offline.</span></span> <span data-ttu-id="73d17-121">**注記:** Commerce Data Exchange: リアルタイム サービスが必要な機能があれば、操作がサポートされていないことを示すエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d17-121">**Note:** If any functionality requires Commerce Data Exchange: Real-time Service, you receive an error message that states that the operation isn't supported.</span></span> <span data-ttu-id="73d17-122">**ヒント:** オフライン データベースで使用できるデータにのみ、レポートおよびその他の操作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="73d17-122">**Tip:** Reports and other operations will act only on the data that is available in the offline database.</span></span>

| <span data-ttu-id="73d17-123">操作 ID</span><span class="sxs-lookup"><span data-stu-id="73d17-123">Operation ID</span></span> | <span data-ttu-id="73d17-124">説明</span><span class="sxs-lookup"><span data-stu-id="73d17-124">Description</span></span>                         |
|--------------|-------------------------------------|
| <span data-ttu-id="73d17-125">100</span><span class="sxs-lookup"><span data-stu-id="73d17-125">100</span></span>          | <span data-ttu-id="73d17-126">製品売上</span><span class="sxs-lookup"><span data-stu-id="73d17-126">Product sale</span></span>                        |
| <span data-ttu-id="73d17-127">101</span><span class="sxs-lookup"><span data-stu-id="73d17-127">101</span></span>          | <span data-ttu-id="73d17-128">価格の確認</span><span class="sxs-lookup"><span data-stu-id="73d17-128">Price check</span></span>                         |
| <span data-ttu-id="73d17-129">102</span><span class="sxs-lookup"><span data-stu-id="73d17-129">102</span></span>          | <span data-ttu-id="73d17-130">製品の無効化</span><span class="sxs-lookup"><span data-stu-id="73d17-130">Void product</span></span>                        |
| <span data-ttu-id="73d17-131">103</span><span class="sxs-lookup"><span data-stu-id="73d17-131">103</span></span>          | <span data-ttu-id="73d17-132">製品コメント</span><span class="sxs-lookup"><span data-stu-id="73d17-132">Product comment</span></span>                     |
| <span data-ttu-id="73d17-133">104</span><span class="sxs-lookup"><span data-stu-id="73d17-133">104</span></span>          | <span data-ttu-id="73d17-134">価格変更</span><span class="sxs-lookup"><span data-stu-id="73d17-134">Price override</span></span>                      |
| <span data-ttu-id="73d17-135">105</span><span class="sxs-lookup"><span data-stu-id="73d17-135">105</span></span>          | <span data-ttu-id="73d17-136">数量の設定</span><span class="sxs-lookup"><span data-stu-id="73d17-136">Set quantity</span></span>                        |
| <span data-ttu-id="73d17-137">106</span><span class="sxs-lookup"><span data-stu-id="73d17-137">106</span></span>          | <span data-ttu-id="73d17-138">数量のクリア</span><span class="sxs-lookup"><span data-stu-id="73d17-138">Clear quantity</span></span>                      |
| <span data-ttu-id="73d17-139">108</span><span class="sxs-lookup"><span data-stu-id="73d17-139">108</span></span>          | <span data-ttu-id="73d17-140">製品検索</span><span class="sxs-lookup"><span data-stu-id="73d17-140">Product search</span></span>                      |
| <span data-ttu-id="73d17-141">109</span><span class="sxs-lookup"><span data-stu-id="73d17-141">109</span></span>          | <span data-ttu-id="73d17-142">返品</span><span class="sxs-lookup"><span data-stu-id="73d17-142">Return product</span></span>                      |
| <span data-ttu-id="73d17-143">115</span><span class="sxs-lookup"><span data-stu-id="73d17-143">115</span></span>          | <span data-ttu-id="73d17-144">仕訳帳の表示</span><span class="sxs-lookup"><span data-stu-id="73d17-144">Show journal</span></span>                        |
| <span data-ttu-id="73d17-145">117</span><span class="sxs-lookup"><span data-stu-id="73d17-145">117</span></span>          | <span data-ttu-id="73d17-146">ロイヤルティ カードの追加</span><span class="sxs-lookup"><span data-stu-id="73d17-146">Add loyalty card</span></span>                    |
| <span data-ttu-id="73d17-147">123</span><span class="sxs-lookup"><span data-stu-id="73d17-147">123</span></span>          | <span data-ttu-id="73d17-148">単位の変更</span><span class="sxs-lookup"><span data-stu-id="73d17-148">Change unit of measure</span></span>              |
| <span data-ttu-id="73d17-149">128</span><span class="sxs-lookup"><span data-stu-id="73d17-149">128</span></span>          | <span data-ttu-id="73d17-150">リストから取引税を上書きする</span><span class="sxs-lookup"><span data-stu-id="73d17-150">Override transaction tax from list</span></span>  |
| <span data-ttu-id="73d17-151">130</span><span class="sxs-lookup"><span data-stu-id="73d17-151">130</span></span>          | <span data-ttu-id="73d17-152">リストから明細行の製品税を上書きする</span><span class="sxs-lookup"><span data-stu-id="73d17-152">Override line product tax from list</span></span> |
| <span data-ttu-id="73d17-153">132</span><span class="sxs-lookup"><span data-stu-id="73d17-153">132</span></span>          | <span data-ttu-id="73d17-154">預金の上書き</span><span class="sxs-lookup"><span data-stu-id="73d17-154">Deposit override</span></span>                    |
| <span data-ttu-id="73d17-155">134</span><span class="sxs-lookup"><span data-stu-id="73d17-155">134</span></span>          | <span data-ttu-id="73d17-156">所属を追加</span><span class="sxs-lookup"><span data-stu-id="73d17-156">Add affiliation</span></span>                     |
| <span data-ttu-id="73d17-157">135</span><span class="sxs-lookup"><span data-stu-id="73d17-157">135</span></span>          | <span data-ttu-id="73d17-158">リストから所属を追加</span><span class="sxs-lookup"><span data-stu-id="73d17-158">Add affiliation from list</span></span>           |
| <span data-ttu-id="73d17-159">200</span><span class="sxs-lookup"><span data-stu-id="73d17-159">200</span></span>          | <span data-ttu-id="73d17-160">現金で支払う</span><span class="sxs-lookup"><span data-stu-id="73d17-160">Pay cash</span></span>                            |
| <span data-ttu-id="73d17-161">202</span><span class="sxs-lookup"><span data-stu-id="73d17-161">202</span></span>          | <span data-ttu-id="73d17-162">顧客口座から支払う</span><span class="sxs-lookup"><span data-stu-id="73d17-162">Pay customer account</span></span>                |
| <span data-ttu-id="73d17-163">203</span><span class="sxs-lookup"><span data-stu-id="73d17-163">203</span></span>          | <span data-ttu-id="73d17-164">各種通貨で支払う</span><span class="sxs-lookup"><span data-stu-id="73d17-164">Pay currency</span></span>                        |
| <span data-ttu-id="73d17-165">206</span><span class="sxs-lookup"><span data-stu-id="73d17-165">206</span></span>          | <span data-ttu-id="73d17-166">現金で即支払う</span><span class="sxs-lookup"><span data-stu-id="73d17-166">Pay cash quick</span></span>                      |
| <span data-ttu-id="73d17-167">211</span><span class="sxs-lookup"><span data-stu-id="73d17-167">211</span></span>          | <span data-ttu-id="73d17-168">支払の無効化</span><span class="sxs-lookup"><span data-stu-id="73d17-168">Void payment</span></span>                        |
| <span data-ttu-id="73d17-169">214</span><span class="sxs-lookup"><span data-stu-id="73d17-169">214</span></span>          | <span data-ttu-id="73d17-170">ギフト カードで支払う</span><span class="sxs-lookup"><span data-stu-id="73d17-170">Pay gift card</span></span>                       |
| <span data-ttu-id="73d17-171">300</span><span class="sxs-lookup"><span data-stu-id="73d17-171">300</span></span>          | <span data-ttu-id="73d17-172">品目割引金額</span><span class="sxs-lookup"><span data-stu-id="73d17-172">Line discount amount</span></span>                |
| <span data-ttu-id="73d17-173">301</span><span class="sxs-lookup"><span data-stu-id="73d17-173">301</span></span>          | <span data-ttu-id="73d17-174">品目割引率</span><span class="sxs-lookup"><span data-stu-id="73d17-174">Line discount percent</span></span>               |
| <span data-ttu-id="73d17-175">302</span><span class="sxs-lookup"><span data-stu-id="73d17-175">302</span></span>          | <span data-ttu-id="73d17-176">合計割引金額</span><span class="sxs-lookup"><span data-stu-id="73d17-176">Total discount amount</span></span>               |
| <span data-ttu-id="73d17-177">303</span><span class="sxs-lookup"><span data-stu-id="73d17-177">303</span></span>          | <span data-ttu-id="73d17-178">合計割引率</span><span class="sxs-lookup"><span data-stu-id="73d17-178">Total discount percent</span></span>              |
| <span data-ttu-id="73d17-179">500</span><span class="sxs-lookup"><span data-stu-id="73d17-179">500</span></span>          | <span data-ttu-id="73d17-180">トランザクションの無効化</span><span class="sxs-lookup"><span data-stu-id="73d17-180">Void transaction</span></span>                    |
| <span data-ttu-id="73d17-181">501</span><span class="sxs-lookup"><span data-stu-id="73d17-181">501</span></span>          | <span data-ttu-id="73d17-182">トランザクション コメント</span><span class="sxs-lookup"><span data-stu-id="73d17-182">Transaction comment</span></span>                 |
| <span data-ttu-id="73d17-183">503</span><span class="sxs-lookup"><span data-stu-id="73d17-183">503</span></span>          | <span data-ttu-id="73d17-184">トランザクションの中断</span><span class="sxs-lookup"><span data-stu-id="73d17-184">Suspend transaction</span></span>                 |
| <span data-ttu-id="73d17-185">512</span><span class="sxs-lookup"><span data-stu-id="73d17-185">512</span></span>          | <span data-ttu-id="73d17-186">ギフト カードの発行</span><span class="sxs-lookup"><span data-stu-id="73d17-186">Issue gift card</span></span>                     |
| <span data-ttu-id="73d17-187">515</span><span class="sxs-lookup"><span data-stu-id="73d17-187">515</span></span>          | <span data-ttu-id="73d17-188">注文の取り消し</span><span class="sxs-lookup"><span data-stu-id="73d17-188">Recall order</span></span>                        |
| <span data-ttu-id="73d17-189">519</span><span class="sxs-lookup"><span data-stu-id="73d17-189">519</span></span>          | <span data-ttu-id="73d17-190">ギフト カードに追加</span><span class="sxs-lookup"><span data-stu-id="73d17-190">Add to gift card</span></span>                    |
| <span data-ttu-id="73d17-191">520</span><span class="sxs-lookup"><span data-stu-id="73d17-191">520</span></span>          | <span data-ttu-id="73d17-192">ギフト カード残高</span><span class="sxs-lookup"><span data-stu-id="73d17-192">Gift card balance</span></span>                   |
| <span data-ttu-id="73d17-193">602</span><span class="sxs-lookup"><span data-stu-id="73d17-193">602</span></span>          | <span data-ttu-id="73d17-194">顧客検索</span><span class="sxs-lookup"><span data-stu-id="73d17-194">Customer search</span></span>                     |
| <span data-ttu-id="73d17-195">603</span><span class="sxs-lookup"><span data-stu-id="73d17-195">603</span></span>          | <span data-ttu-id="73d17-196">顧客のクリア</span><span class="sxs-lookup"><span data-stu-id="73d17-196">Customer clear</span></span>                      |
| <span data-ttu-id="73d17-197">612</span><span class="sxs-lookup"><span data-stu-id="73d17-197">612</span></span>          | <span data-ttu-id="73d17-198">顧客の追加</span><span class="sxs-lookup"><span data-stu-id="73d17-198">Customer add</span></span>                        |
| <span data-ttu-id="73d17-199">622</span><span class="sxs-lookup"><span data-stu-id="73d17-199">622</span></span>          | <span data-ttu-id="73d17-200">検索</span><span class="sxs-lookup"><span data-stu-id="73d17-200">Search</span></span>                              |
| <span data-ttu-id="73d17-201">623</span><span class="sxs-lookup"><span data-stu-id="73d17-201">623</span></span>          | <span data-ttu-id="73d17-202">顧客の編集</span><span class="sxs-lookup"><span data-stu-id="73d17-202">Edit customer</span></span>                       |
| <span data-ttu-id="73d17-203">701</span><span class="sxs-lookup"><span data-stu-id="73d17-203">701</span></span>          | <span data-ttu-id="73d17-204">ログオフ</span><span class="sxs-lookup"><span data-stu-id="73d17-204">Log off</span></span>                             |
| <span data-ttu-id="73d17-205">703</span><span class="sxs-lookup"><span data-stu-id="73d17-205">703</span></span>          | <span data-ttu-id="73d17-206">レジスターのロック</span><span class="sxs-lookup"><span data-stu-id="73d17-206">Lock register</span></span>                       |
| <span data-ttu-id="73d17-207">801</span><span class="sxs-lookup"><span data-stu-id="73d17-207">801</span></span>          | <span data-ttu-id="73d17-208">在庫検索</span><span class="sxs-lookup"><span data-stu-id="73d17-208">Inventory lookup</span></span>                    |
| <span data-ttu-id="73d17-209">802</span><span class="sxs-lookup"><span data-stu-id="73d17-209">802</span></span>          | <span data-ttu-id="73d17-210">在庫数</span><span class="sxs-lookup"><span data-stu-id="73d17-210">Stock count</span></span>                         |
| <span data-ttu-id="73d17-211">917</span><span class="sxs-lookup"><span data-stu-id="73d17-211">917</span></span>          | <span data-ttu-id="73d17-212">データベース接続ステータス</span><span class="sxs-lookup"><span data-stu-id="73d17-212">Database connection status</span></span>          |
| <span data-ttu-id="73d17-213">920</span><span class="sxs-lookup"><span data-stu-id="73d17-213">920</span></span>          | <span data-ttu-id="73d17-214">タイム レコーダー</span><span class="sxs-lookup"><span data-stu-id="73d17-214">Time clock</span></span>                          |
| <span data-ttu-id="73d17-215">921</span><span class="sxs-lookup"><span data-stu-id="73d17-215">921</span></span>          | <span data-ttu-id="73d17-216">タイム レコーダー エントリの表示</span><span class="sxs-lookup"><span data-stu-id="73d17-216">View time clock entries</span></span>             |
| <span data-ttu-id="73d17-217">922</span><span class="sxs-lookup"><span data-stu-id="73d17-217">922</span></span>          | <span data-ttu-id="73d17-218">製品の詳細表示</span><span class="sxs-lookup"><span data-stu-id="73d17-218">View product details</span></span>                |
| <span data-ttu-id="73d17-219">1003</span><span class="sxs-lookup"><span data-stu-id="73d17-219">1003</span></span>         | <span data-ttu-id="73d17-220">レポートの表示</span><span class="sxs-lookup"><span data-stu-id="73d17-220">View reports</span></span>                        |
| <span data-ttu-id="73d17-221">1052</span><span class="sxs-lookup"><span data-stu-id="73d17-221">1052</span></span>         | <span data-ttu-id="73d17-222">支払/入金申告</span><span class="sxs-lookup"><span data-stu-id="73d17-222">Tender declaration</span></span>                  |
| <span data-ttu-id="73d17-223">1200</span><span class="sxs-lookup"><span data-stu-id="73d17-223">1200</span></span>         | <span data-ttu-id="73d17-224">開始金額の申告</span><span class="sxs-lookup"><span data-stu-id="73d17-224">Declare start amount</span></span>                |
| <span data-ttu-id="73d17-225">1201</span><span class="sxs-lookup"><span data-stu-id="73d17-225">1201</span></span>         | <span data-ttu-id="73d17-226">釣銭入力</span><span class="sxs-lookup"><span data-stu-id="73d17-226">Float entry</span></span>                         |
| <span data-ttu-id="73d17-227">1210</span><span class="sxs-lookup"><span data-stu-id="73d17-227">1210</span></span>         | <span data-ttu-id="73d17-228">支払/入金の削除</span><span class="sxs-lookup"><span data-stu-id="73d17-228">Tender removal</span></span>                      |
| <span data-ttu-id="73d17-229">1211</span><span class="sxs-lookup"><span data-stu-id="73d17-229">1211</span></span>         | <span data-ttu-id="73d17-230">金庫保管</span><span class="sxs-lookup"><span data-stu-id="73d17-230">Safe drop</span></span>                           |
| <span data-ttu-id="73d17-231">1212</span><span class="sxs-lookup"><span data-stu-id="73d17-231">1212</span></span>         | <span data-ttu-id="73d17-232">銀行入金</span><span class="sxs-lookup"><span data-stu-id="73d17-232">Bank drop</span></span>                           |

## <a name="operations-that-cant-be-completed-when-the-channel-database-is-offline"></a><span data-ttu-id="73d17-233">チャネル データベースがオフラインのときに実行できない操作</span><span class="sxs-lookup"><span data-stu-id="73d17-233">Operations that can’t be completed when the channel database is offline</span></span>
<span data-ttu-id="73d17-234">チャネル データベースがオフラインときは、次の操作を完了することができません。</span><span class="sxs-lookup"><span data-stu-id="73d17-234">You can’t complete the following operations when the channel database is offline.</span></span>

| <span data-ttu-id="73d17-235">操作 ID</span><span class="sxs-lookup"><span data-stu-id="73d17-235">Operation ID</span></span> | <span data-ttu-id="73d17-236">説明</span><span class="sxs-lookup"><span data-stu-id="73d17-236">Description</span></span>       |
|--------------|-------------------|
| <span data-ttu-id="73d17-237">207</span><span class="sxs-lookup"><span data-stu-id="73d17-237">207</span></span>          | <span data-ttu-id="73d17-238">ロイヤルティ カードで支払う</span><span class="sxs-lookup"><span data-stu-id="73d17-238">Pay loyalty card</span></span>  |
| <span data-ttu-id="73d17-239">707</span><span class="sxs-lookup"><span data-stu-id="73d17-239">707</span></span>          | <span data-ttu-id="73d17-240">デバイスのアクティブ化</span><span class="sxs-lookup"><span data-stu-id="73d17-240">Activate device</span></span>   |
| <span data-ttu-id="73d17-241">708</span><span class="sxs-lookup"><span data-stu-id="73d17-241">708</span></span>          | <span data-ttu-id="73d17-242">デバイスの無効化</span><span class="sxs-lookup"><span data-stu-id="73d17-242">Inactivate device</span></span> |
| <span data-ttu-id="73d17-243">1053</span><span class="sxs-lookup"><span data-stu-id="73d17-243">1053</span></span>         | <span data-ttu-id="73d17-244">シフトのブラインド クローズ</span><span class="sxs-lookup"><span data-stu-id="73d17-244">Blind close shift</span></span> |
| <span data-ttu-id="73d17-245">1054</span><span class="sxs-lookup"><span data-stu-id="73d17-245">1054</span></span>         | <span data-ttu-id="73d17-246">シフトの中断</span><span class="sxs-lookup"><span data-stu-id="73d17-246">Suspend shift</span></span>     |
| <span data-ttu-id="73d17-247">1055</span><span class="sxs-lookup"><span data-stu-id="73d17-247">1055</span></span>         | <span data-ttu-id="73d17-248">シフトのクローズ</span><span class="sxs-lookup"><span data-stu-id="73d17-248">Close shift</span></span>       |
| <span data-ttu-id="73d17-249">1056</span><span class="sxs-lookup"><span data-stu-id="73d17-249">1056</span></span>         | <span data-ttu-id="73d17-250">X の印刷</span><span class="sxs-lookup"><span data-stu-id="73d17-250">Print X</span></span>           |
| <span data-ttu-id="73d17-251">1057</span><span class="sxs-lookup"><span data-stu-id="73d17-251">1057</span></span>         | <span data-ttu-id="73d17-252">再印刷 Z</span><span class="sxs-lookup"><span data-stu-id="73d17-252">Reprint Z</span></span>         |






