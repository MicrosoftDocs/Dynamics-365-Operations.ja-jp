---
title: "オフライン モードの Retail Modern POS"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 07ba24614ce7a69b58f28b29f599bac030f1d767
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="retail-modern-pos-in-offline-mode"></a><span data-ttu-id="5a8da-103">オフライン モードの Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="5a8da-103">Retail Modern POS in offline mode</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a8da-104">この記事では、Retail サーバーが利用できない場合に、オフライン モードで Retail Modern POS デバイスを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5a8da-104">This article explains how to use Retail Modern POS devices in offline mode if the Retail Server is unavailable.</span></span>

<span data-ttu-id="5a8da-105">Retail サーバーが利用できない場合、Retail Modern POS はオフラインになります。</span><span class="sxs-lookup"><span data-stu-id="5a8da-105">A Retail Modern POS device will go offline if the Retail Server is unavailable.</span></span> <span data-ttu-id="5a8da-106">Retail サーバーとの接続が失われると、販売時点管理 (POS) はオフライン データベースに自動的に接続されます。</span><span class="sxs-lookup"><span data-stu-id="5a8da-106">When the connection with the Retail Server is lost, the point of sale (POS) automatically switches to the offline database.</span></span> <span data-ttu-id="5a8da-107">オフライン プロファイルでコンフィギュレーションされたタイムアウトの間隔内でデータの要求が成功しない場合、Retail Modern POS は自動的にオフライン データベースに切り替わり、販売トランザクションを続行します。</span><span class="sxs-lookup"><span data-stu-id="5a8da-107">If a data request doesn't succeed within the time-out interval that is configured in the offline profile, Retail Modern POS automatically switches to the offline database and continues the sales transaction.</span></span> <span data-ttu-id="5a8da-108">Retail Modern POS はオフライン プロファイルでコンフィギュレーションされた再接続試行間隔の後に Retail Server への再接続を試みます。</span><span class="sxs-lookup"><span data-stu-id="5a8da-108">Retail Modern POS will try to reconnect to the Retail Server after the reconnect attempt interval that is configured in the offline profile.</span></span> <span data-ttu-id="5a8da-109">この再接続の試みは、トランザクションの開始時にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="5a8da-109">This reconnect attempt will occur only at the beginning of a transaction.</span></span>

## <a name="determine-the-connection-mode-of-retail-modern-pos"></a><span data-ttu-id="5a8da-110">Retail Modern POS の接続モードを決定する</span><span class="sxs-lookup"><span data-stu-id="5a8da-110">Determine the connection mode of Retail Modern POS</span></span>
<span data-ttu-id="5a8da-111">Retail Modern POS のステータス ヘッダーは、現在の接続状態を示します。</span><span class="sxs-lookup"><span data-stu-id="5a8da-111">The status header of Retail Modern POS indicates the current connection status.</span></span> 

<span data-ttu-id="5a8da-112">[![接続](./media/connection.png)](./media/connection.png)</span><span class="sxs-lookup"><span data-stu-id="5a8da-112">[![connection](./media/connection.png)](./media/connection.png)</span></span> 

<span data-ttu-id="5a8da-113">Retail Modern POS の **接続ステータス** ページには、オフライン データベースと同期する前回の試みのステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a8da-113">The **Connection status** page in Retail Modern POS shows the status of the last attempt to synchronize with the offline database.</span></span> 

<span data-ttu-id="5a8da-114">[![接続ステータス](./media/connection-status.png)](./media/connection-status.png)</span><span class="sxs-lookup"><span data-stu-id="5a8da-114">[![connection status](./media/connection-status.png)](./media/connection-status.png)</span></span>

## <a name="create-a-button-to-manually-switch-between-online-and-offline-modes"></a><span data-ttu-id="5a8da-115">手動でオンラインとオフライン モードを切り替えるためのボタンを作成</span><span class="sxs-lookup"><span data-stu-id="5a8da-115">Create a button to manually switch between online and offline modes</span></span>
<span data-ttu-id="5a8da-116">Retail Modern POS にオンラインとオフライン モードを手動で切り替えるボタンを追加できます。</span><span class="sxs-lookup"><span data-stu-id="5a8da-116">You can add a button to Retail Modern POS to manually switch between online and offline modes.</span></span> <span data-ttu-id="5a8da-117">**POS 操作 917 – データベース接続ステータス**のボタンを作成します。</span><span class="sxs-lookup"><span data-stu-id="5a8da-117">Create a button for **POS operation 917 – Database connection status**.</span></span> <span data-ttu-id="5a8da-118">接続または切断するには、ボタンをトグルとして切り替えて使用します。</span><span class="sxs-lookup"><span data-stu-id="5a8da-118">Use the button as a toggle to connect or disconnect.</span></span>

## <a name="operations-that-can-be-completed-when-the-channel-database-is-offline"></a><span data-ttu-id="5a8da-119">チャネル データベースがオフラインのときに実行できる操作</span><span class="sxs-lookup"><span data-stu-id="5a8da-119">Operations that can be completed when the channel database is offline</span></span>
<span data-ttu-id="5a8da-120">チャネル データベースがオフラインときは、次の操作を完了することができます。</span><span class="sxs-lookup"><span data-stu-id="5a8da-120">You can complete the following operations when the channel database is offline.</span></span> <span data-ttu-id="5a8da-121">**注記:** Commerce Data Exchange: リアルタイム サービスが必要な機能があれば、操作がサポートされていないことを示すエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a8da-121">**Note:** If any functionality requires Commerce Data Exchange: Real-time Service, you receive an error message that states that the operation isn't supported.</span></span> <span data-ttu-id="5a8da-122">**ヒント:** オフライン データベースで使用できるデータにのみ、レポートおよびその他の操作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="5a8da-122">**Tip:** Reports and other operations will act only on the data that is available in the offline database.</span></span>

| <span data-ttu-id="5a8da-123">操作 ID</span><span class="sxs-lookup"><span data-stu-id="5a8da-123">Operation ID</span></span> | <span data-ttu-id="5a8da-124">説明</span><span class="sxs-lookup"><span data-stu-id="5a8da-124">Description</span></span>                         |
|--------------|-------------------------------------|
| <span data-ttu-id="5a8da-125">100</span><span class="sxs-lookup"><span data-stu-id="5a8da-125">100</span></span>          | <span data-ttu-id="5a8da-126">製品売上</span><span class="sxs-lookup"><span data-stu-id="5a8da-126">Product sale</span></span>                        |
| <span data-ttu-id="5a8da-127">101</span><span class="sxs-lookup"><span data-stu-id="5a8da-127">101</span></span>          | <span data-ttu-id="5a8da-128">価格の確認</span><span class="sxs-lookup"><span data-stu-id="5a8da-128">Price check</span></span>                         |
| <span data-ttu-id="5a8da-129">102</span><span class="sxs-lookup"><span data-stu-id="5a8da-129">102</span></span>          | <span data-ttu-id="5a8da-130">製品の無効化</span><span class="sxs-lookup"><span data-stu-id="5a8da-130">Void product</span></span>                        |
| <span data-ttu-id="5a8da-131">103</span><span class="sxs-lookup"><span data-stu-id="5a8da-131">103</span></span>          | <span data-ttu-id="5a8da-132">製品コメント</span><span class="sxs-lookup"><span data-stu-id="5a8da-132">Product comment</span></span>                     |
| <span data-ttu-id="5a8da-133">104</span><span class="sxs-lookup"><span data-stu-id="5a8da-133">104</span></span>          | <span data-ttu-id="5a8da-134">価格変更</span><span class="sxs-lookup"><span data-stu-id="5a8da-134">Price override</span></span>                      |
| <span data-ttu-id="5a8da-135">105</span><span class="sxs-lookup"><span data-stu-id="5a8da-135">105</span></span>          | <span data-ttu-id="5a8da-136">数量の設定</span><span class="sxs-lookup"><span data-stu-id="5a8da-136">Set quantity</span></span>                        |
| <span data-ttu-id="5a8da-137">106</span><span class="sxs-lookup"><span data-stu-id="5a8da-137">106</span></span>          | <span data-ttu-id="5a8da-138">数量のクリア</span><span class="sxs-lookup"><span data-stu-id="5a8da-138">Clear quantity</span></span>                      |
| <span data-ttu-id="5a8da-139">108</span><span class="sxs-lookup"><span data-stu-id="5a8da-139">108</span></span>          | <span data-ttu-id="5a8da-140">製品検索</span><span class="sxs-lookup"><span data-stu-id="5a8da-140">Product search</span></span>                      |
| <span data-ttu-id="5a8da-141">109</span><span class="sxs-lookup"><span data-stu-id="5a8da-141">109</span></span>          | <span data-ttu-id="5a8da-142">返品</span><span class="sxs-lookup"><span data-stu-id="5a8da-142">Return product</span></span>                      |
| <span data-ttu-id="5a8da-143">115</span><span class="sxs-lookup"><span data-stu-id="5a8da-143">115</span></span>          | <span data-ttu-id="5a8da-144">仕訳帳の表示</span><span class="sxs-lookup"><span data-stu-id="5a8da-144">Show journal</span></span>                        |
| <span data-ttu-id="5a8da-145">117</span><span class="sxs-lookup"><span data-stu-id="5a8da-145">117</span></span>          | <span data-ttu-id="5a8da-146">ロイヤルティ カードの追加</span><span class="sxs-lookup"><span data-stu-id="5a8da-146">Add loyalty card</span></span>                    |
| <span data-ttu-id="5a8da-147">123</span><span class="sxs-lookup"><span data-stu-id="5a8da-147">123</span></span>          | <span data-ttu-id="5a8da-148">単位の変更</span><span class="sxs-lookup"><span data-stu-id="5a8da-148">Change unit of measure</span></span>              |
| <span data-ttu-id="5a8da-149">128</span><span class="sxs-lookup"><span data-stu-id="5a8da-149">128</span></span>          | <span data-ttu-id="5a8da-150">リストから取引税を上書きする</span><span class="sxs-lookup"><span data-stu-id="5a8da-150">Override transaction tax from list</span></span>  |
| <span data-ttu-id="5a8da-151">130</span><span class="sxs-lookup"><span data-stu-id="5a8da-151">130</span></span>          | <span data-ttu-id="5a8da-152">リストから明細行の製品税を上書きする</span><span class="sxs-lookup"><span data-stu-id="5a8da-152">Override line product tax from list</span></span> |
| <span data-ttu-id="5a8da-153">132</span><span class="sxs-lookup"><span data-stu-id="5a8da-153">132</span></span>          | <span data-ttu-id="5a8da-154">預金の上書き</span><span class="sxs-lookup"><span data-stu-id="5a8da-154">Deposit override</span></span>                    |
| <span data-ttu-id="5a8da-155">134</span><span class="sxs-lookup"><span data-stu-id="5a8da-155">134</span></span>          | <span data-ttu-id="5a8da-156">所属を追加</span><span class="sxs-lookup"><span data-stu-id="5a8da-156">Add affiliation</span></span>                     |
| <span data-ttu-id="5a8da-157">135</span><span class="sxs-lookup"><span data-stu-id="5a8da-157">135</span></span>          | <span data-ttu-id="5a8da-158">リストから所属を追加</span><span class="sxs-lookup"><span data-stu-id="5a8da-158">Add affiliation from list</span></span>           |
| <span data-ttu-id="5a8da-159">200</span><span class="sxs-lookup"><span data-stu-id="5a8da-159">200</span></span>          | <span data-ttu-id="5a8da-160">現金で支払う</span><span class="sxs-lookup"><span data-stu-id="5a8da-160">Pay cash</span></span>                            |
| <span data-ttu-id="5a8da-161">202</span><span class="sxs-lookup"><span data-stu-id="5a8da-161">202</span></span>          | <span data-ttu-id="5a8da-162">顧客口座から支払う</span><span class="sxs-lookup"><span data-stu-id="5a8da-162">Pay customer account</span></span>                |
| <span data-ttu-id="5a8da-163">203</span><span class="sxs-lookup"><span data-stu-id="5a8da-163">203</span></span>          | <span data-ttu-id="5a8da-164">各種通貨で支払う</span><span class="sxs-lookup"><span data-stu-id="5a8da-164">Pay currency</span></span>                        |
| <span data-ttu-id="5a8da-165">206</span><span class="sxs-lookup"><span data-stu-id="5a8da-165">206</span></span>          | <span data-ttu-id="5a8da-166">現金で即支払う</span><span class="sxs-lookup"><span data-stu-id="5a8da-166">Pay cash quick</span></span>                      |
| <span data-ttu-id="5a8da-167">211</span><span class="sxs-lookup"><span data-stu-id="5a8da-167">211</span></span>          | <span data-ttu-id="5a8da-168">支払の無効化</span><span class="sxs-lookup"><span data-stu-id="5a8da-168">Void payment</span></span>                        |
| <span data-ttu-id="5a8da-169">214</span><span class="sxs-lookup"><span data-stu-id="5a8da-169">214</span></span>          | <span data-ttu-id="5a8da-170">ギフト カードで支払う</span><span class="sxs-lookup"><span data-stu-id="5a8da-170">Pay gift card</span></span>                       |
| <span data-ttu-id="5a8da-171">300</span><span class="sxs-lookup"><span data-stu-id="5a8da-171">300</span></span>          | <span data-ttu-id="5a8da-172">品目割引金額</span><span class="sxs-lookup"><span data-stu-id="5a8da-172">Line discount amount</span></span>                |
| <span data-ttu-id="5a8da-173">301</span><span class="sxs-lookup"><span data-stu-id="5a8da-173">301</span></span>          | <span data-ttu-id="5a8da-174">品目割引率</span><span class="sxs-lookup"><span data-stu-id="5a8da-174">Line discount percent</span></span>               |
| <span data-ttu-id="5a8da-175">302</span><span class="sxs-lookup"><span data-stu-id="5a8da-175">302</span></span>          | <span data-ttu-id="5a8da-176">合計割引金額</span><span class="sxs-lookup"><span data-stu-id="5a8da-176">Total discount amount</span></span>               |
| <span data-ttu-id="5a8da-177">303</span><span class="sxs-lookup"><span data-stu-id="5a8da-177">303</span></span>          | <span data-ttu-id="5a8da-178">合計割引率</span><span class="sxs-lookup"><span data-stu-id="5a8da-178">Total discount percent</span></span>              |
| <span data-ttu-id="5a8da-179">500</span><span class="sxs-lookup"><span data-stu-id="5a8da-179">500</span></span>          | <span data-ttu-id="5a8da-180">トランザクションの無効化</span><span class="sxs-lookup"><span data-stu-id="5a8da-180">Void transaction</span></span>                    |
| <span data-ttu-id="5a8da-181">501</span><span class="sxs-lookup"><span data-stu-id="5a8da-181">501</span></span>          | <span data-ttu-id="5a8da-182">トランザクション コメント</span><span class="sxs-lookup"><span data-stu-id="5a8da-182">Transaction comment</span></span>                 |
| <span data-ttu-id="5a8da-183">503</span><span class="sxs-lookup"><span data-stu-id="5a8da-183">503</span></span>          | <span data-ttu-id="5a8da-184">トランザクションの中断</span><span class="sxs-lookup"><span data-stu-id="5a8da-184">Suspend transaction</span></span>                 |
| <span data-ttu-id="5a8da-185">512</span><span class="sxs-lookup"><span data-stu-id="5a8da-185">512</span></span>          | <span data-ttu-id="5a8da-186">ギフト カードの発行</span><span class="sxs-lookup"><span data-stu-id="5a8da-186">Issue gift card</span></span>                     |
| <span data-ttu-id="5a8da-187">515</span><span class="sxs-lookup"><span data-stu-id="5a8da-187">515</span></span>          | <span data-ttu-id="5a8da-188">注文の取り消し</span><span class="sxs-lookup"><span data-stu-id="5a8da-188">Recall order</span></span>                        |
| <span data-ttu-id="5a8da-189">519</span><span class="sxs-lookup"><span data-stu-id="5a8da-189">519</span></span>          | <span data-ttu-id="5a8da-190">ギフト カードに追加</span><span class="sxs-lookup"><span data-stu-id="5a8da-190">Add to gift card</span></span>                    |
| <span data-ttu-id="5a8da-191">520</span><span class="sxs-lookup"><span data-stu-id="5a8da-191">520</span></span>          | <span data-ttu-id="5a8da-192">ギフト カード残高</span><span class="sxs-lookup"><span data-stu-id="5a8da-192">Gift card balance</span></span>                   |
| <span data-ttu-id="5a8da-193">602</span><span class="sxs-lookup"><span data-stu-id="5a8da-193">602</span></span>          | <span data-ttu-id="5a8da-194">顧客検索</span><span class="sxs-lookup"><span data-stu-id="5a8da-194">Customer search</span></span>                     |
| <span data-ttu-id="5a8da-195">603</span><span class="sxs-lookup"><span data-stu-id="5a8da-195">603</span></span>          | <span data-ttu-id="5a8da-196">顧客のクリア</span><span class="sxs-lookup"><span data-stu-id="5a8da-196">Customer clear</span></span>                      |
| <span data-ttu-id="5a8da-197">612</span><span class="sxs-lookup"><span data-stu-id="5a8da-197">612</span></span>          | <span data-ttu-id="5a8da-198">顧客の追加</span><span class="sxs-lookup"><span data-stu-id="5a8da-198">Customer add</span></span>                        |
| <span data-ttu-id="5a8da-199">622</span><span class="sxs-lookup"><span data-stu-id="5a8da-199">622</span></span>          | <span data-ttu-id="5a8da-200">検索</span><span class="sxs-lookup"><span data-stu-id="5a8da-200">Search</span></span>                              |
| <span data-ttu-id="5a8da-201">623</span><span class="sxs-lookup"><span data-stu-id="5a8da-201">623</span></span>          | <span data-ttu-id="5a8da-202">顧客の編集</span><span class="sxs-lookup"><span data-stu-id="5a8da-202">Edit customer</span></span>                       |
| <span data-ttu-id="5a8da-203">701</span><span class="sxs-lookup"><span data-stu-id="5a8da-203">701</span></span>          | <span data-ttu-id="5a8da-204">ログオフ</span><span class="sxs-lookup"><span data-stu-id="5a8da-204">Log off</span></span>                             |
| <span data-ttu-id="5a8da-205">703</span><span class="sxs-lookup"><span data-stu-id="5a8da-205">703</span></span>          | <span data-ttu-id="5a8da-206">レジスターのロック</span><span class="sxs-lookup"><span data-stu-id="5a8da-206">Lock register</span></span>                       |
| <span data-ttu-id="5a8da-207">801</span><span class="sxs-lookup"><span data-stu-id="5a8da-207">801</span></span>          | <span data-ttu-id="5a8da-208">在庫検索</span><span class="sxs-lookup"><span data-stu-id="5a8da-208">Inventory lookup</span></span>                    |
| <span data-ttu-id="5a8da-209">802</span><span class="sxs-lookup"><span data-stu-id="5a8da-209">802</span></span>          | <span data-ttu-id="5a8da-210">在庫数</span><span class="sxs-lookup"><span data-stu-id="5a8da-210">Stock count</span></span>                         |
| <span data-ttu-id="5a8da-211">917</span><span class="sxs-lookup"><span data-stu-id="5a8da-211">917</span></span>          | <span data-ttu-id="5a8da-212">データベース接続ステータス</span><span class="sxs-lookup"><span data-stu-id="5a8da-212">Database connection status</span></span>          |
| <span data-ttu-id="5a8da-213">920</span><span class="sxs-lookup"><span data-stu-id="5a8da-213">920</span></span>          | <span data-ttu-id="5a8da-214">タイム レコーダー</span><span class="sxs-lookup"><span data-stu-id="5a8da-214">Time clock</span></span>                          |
| <span data-ttu-id="5a8da-215">921</span><span class="sxs-lookup"><span data-stu-id="5a8da-215">921</span></span>          | <span data-ttu-id="5a8da-216">タイム レコーダー エントリの表示</span><span class="sxs-lookup"><span data-stu-id="5a8da-216">View time clock entries</span></span>             |
| <span data-ttu-id="5a8da-217">922</span><span class="sxs-lookup"><span data-stu-id="5a8da-217">922</span></span>          | <span data-ttu-id="5a8da-218">製品の詳細表示</span><span class="sxs-lookup"><span data-stu-id="5a8da-218">View product details</span></span>                |
| <span data-ttu-id="5a8da-219">1003</span><span class="sxs-lookup"><span data-stu-id="5a8da-219">1003</span></span>         | <span data-ttu-id="5a8da-220">レポートの表示</span><span class="sxs-lookup"><span data-stu-id="5a8da-220">View reports</span></span>                        |
| <span data-ttu-id="5a8da-221">1052</span><span class="sxs-lookup"><span data-stu-id="5a8da-221">1052</span></span>         | <span data-ttu-id="5a8da-222">支払/入金申告</span><span class="sxs-lookup"><span data-stu-id="5a8da-222">Tender declaration</span></span>                  |
| <span data-ttu-id="5a8da-223">1200</span><span class="sxs-lookup"><span data-stu-id="5a8da-223">1200</span></span>         | <span data-ttu-id="5a8da-224">開始金額の申告</span><span class="sxs-lookup"><span data-stu-id="5a8da-224">Declare start amount</span></span>                |
| <span data-ttu-id="5a8da-225">1201</span><span class="sxs-lookup"><span data-stu-id="5a8da-225">1201</span></span>         | <span data-ttu-id="5a8da-226">釣銭入力</span><span class="sxs-lookup"><span data-stu-id="5a8da-226">Float entry</span></span>                         |
| <span data-ttu-id="5a8da-227">1210</span><span class="sxs-lookup"><span data-stu-id="5a8da-227">1210</span></span>         | <span data-ttu-id="5a8da-228">支払/入金の削除</span><span class="sxs-lookup"><span data-stu-id="5a8da-228">Tender removal</span></span>                      |
| <span data-ttu-id="5a8da-229">1211</span><span class="sxs-lookup"><span data-stu-id="5a8da-229">1211</span></span>         | <span data-ttu-id="5a8da-230">金庫保管</span><span class="sxs-lookup"><span data-stu-id="5a8da-230">Safe drop</span></span>                           |
| <span data-ttu-id="5a8da-231">1212</span><span class="sxs-lookup"><span data-stu-id="5a8da-231">1212</span></span>         | <span data-ttu-id="5a8da-232">銀行入金</span><span class="sxs-lookup"><span data-stu-id="5a8da-232">Bank drop</span></span>                           |

## <a name="operations-that-cant-be-completed-when-the-channel-database-is-offline"></a><span data-ttu-id="5a8da-233">チャネル データベースがオフラインのときに実行できない操作</span><span class="sxs-lookup"><span data-stu-id="5a8da-233">Operations that can’t be completed when the channel database is offline</span></span>
<span data-ttu-id="5a8da-234">チャネル データベースがオフラインときは、次の操作を完了することができません。</span><span class="sxs-lookup"><span data-stu-id="5a8da-234">You can’t complete the following operations when the channel database is offline.</span></span>

| <span data-ttu-id="5a8da-235">操作 ID</span><span class="sxs-lookup"><span data-stu-id="5a8da-235">Operation ID</span></span> | <span data-ttu-id="5a8da-236">説明</span><span class="sxs-lookup"><span data-stu-id="5a8da-236">Description</span></span>       |
|--------------|-------------------|
| <span data-ttu-id="5a8da-237">207</span><span class="sxs-lookup"><span data-stu-id="5a8da-237">207</span></span>          | <span data-ttu-id="5a8da-238">ロイヤルティ カードで支払う</span><span class="sxs-lookup"><span data-stu-id="5a8da-238">Pay loyalty card</span></span>  |
| <span data-ttu-id="5a8da-239">707</span><span class="sxs-lookup"><span data-stu-id="5a8da-239">707</span></span>          | <span data-ttu-id="5a8da-240">デバイスのアクティブ化</span><span class="sxs-lookup"><span data-stu-id="5a8da-240">Activate device</span></span>   |
| <span data-ttu-id="5a8da-241">708</span><span class="sxs-lookup"><span data-stu-id="5a8da-241">708</span></span>          | <span data-ttu-id="5a8da-242">デバイスの無効化</span><span class="sxs-lookup"><span data-stu-id="5a8da-242">Inactivate device</span></span> |
| <span data-ttu-id="5a8da-243">1053</span><span class="sxs-lookup"><span data-stu-id="5a8da-243">1053</span></span>         | <span data-ttu-id="5a8da-244">シフトのブラインド クローズ</span><span class="sxs-lookup"><span data-stu-id="5a8da-244">Blind close shift</span></span> |
| <span data-ttu-id="5a8da-245">1054</span><span class="sxs-lookup"><span data-stu-id="5a8da-245">1054</span></span>         | <span data-ttu-id="5a8da-246">シフトの中断</span><span class="sxs-lookup"><span data-stu-id="5a8da-246">Suspend shift</span></span>     |
| <span data-ttu-id="5a8da-247">1055</span><span class="sxs-lookup"><span data-stu-id="5a8da-247">1055</span></span>         | <span data-ttu-id="5a8da-248">シフトのクローズ</span><span class="sxs-lookup"><span data-stu-id="5a8da-248">Close shift</span></span>       |
| <span data-ttu-id="5a8da-249">1056</span><span class="sxs-lookup"><span data-stu-id="5a8da-249">1056</span></span>         | <span data-ttu-id="5a8da-250">X の印刷</span><span class="sxs-lookup"><span data-stu-id="5a8da-250">Print X</span></span>           |
| <span data-ttu-id="5a8da-251">1057</span><span class="sxs-lookup"><span data-stu-id="5a8da-251">1057</span></span>         | <span data-ttu-id="5a8da-252">再印刷 Z</span><span class="sxs-lookup"><span data-stu-id="5a8da-252">Reprint Z</span></span>         |






