---
title: オフライン モードの Retail Modern POS (MPOS)
description: この記事では、Retail サーバーが利用できない場合に、オフライン モードで Retail Modern POS デバイスを使用する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 08/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 31441
ms.assetid: 219f93a3-6321-46e9-b989-f97072af0bb3
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8e3b2fd2e6780570e3480c25df2e7bff42b4d4da
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564383"
---
# <a name="retail-modern-pos-mpos-in-offline-mode"></a><span data-ttu-id="1dc99-103">オフライン モードの Retail Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="1dc99-103">Retail Modern POS (MPOS) in offline mode</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dc99-104">このトピックでは、Retail サーバーが利用できない場合に、オフライン モードで Retail Modern POS デバイスを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1dc99-104">This topic explains how to use Retail Modern POS devices in offline mode if the Retail Server is unavailable.</span></span>

<span data-ttu-id="1dc99-105">Retail サーバーが利用できない場合、Retail Modern POS はオフラインになります。</span><span class="sxs-lookup"><span data-stu-id="1dc99-105">A Retail Modern POS device will go offline if the Retail Server is unavailable.</span></span> <span data-ttu-id="1dc99-106">Retail サーバーとの接続が失われると、販売時点管理 (POS) はオフライン データベースに自動的に接続されます。</span><span class="sxs-lookup"><span data-stu-id="1dc99-106">When the connection with the Retail Server is lost, the point of sale (POS) automatically switches to the offline database.</span></span> <span data-ttu-id="1dc99-107">オフライン プロファイルでコンフィギュレーションされたタイムアウトの間隔内でデータの要求が成功しない場合、Retail Modern POS は自動的にオフライン データベースに切り替わり、販売トランザクションを続行します。</span><span class="sxs-lookup"><span data-stu-id="1dc99-107">If a data request doesn't succeed within the time-out interval that is configured in the offline profile, Retail Modern POS automatically switches to the offline database and continues the sales transaction.</span></span> <span data-ttu-id="1dc99-108">Retail Modern POS はオフライン プロファイルでコンフィギュレーションされた再接続試行間隔の後に Retail Server への再接続を試みます。</span><span class="sxs-lookup"><span data-stu-id="1dc99-108">Retail Modern POS will try to reconnect to the Retail Server after the reconnect attempt interval that is configured in the offline profile.</span></span> <span data-ttu-id="1dc99-109">この再接続の試みは、トランザクションの開始時にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="1dc99-109">This reconnect attempt will occur only at the beginning of a transaction.</span></span>

## <a name="determine-the-connection-mode-of-retail-modern-pos"></a><span data-ttu-id="1dc99-110">Retail Modern POS の接続モードを決定する</span><span class="sxs-lookup"><span data-stu-id="1dc99-110">Determine the connection mode of Retail Modern POS</span></span>
<span data-ttu-id="1dc99-111">Retail Modern POS のステータス ヘッダーは、現在の接続状態を示します。</span><span class="sxs-lookup"><span data-stu-id="1dc99-111">The status header of Retail Modern POS indicates the current connection status.</span></span> 

<span data-ttu-id="1dc99-112">[![接続](./media/connection.png)](./media/connection.png)</span><span class="sxs-lookup"><span data-stu-id="1dc99-112">[![connection](./media/connection.png)](./media/connection.png)</span></span> 

<span data-ttu-id="1dc99-113">Retail Modern POS の**接続ステータス**ページには、オフライン データベースと同期する前回の試みのステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1dc99-113">The **Connection status** page in Retail Modern POS shows the status of the last attempt to synchronize with the offline database.</span></span> 

<span data-ttu-id="1dc99-114">[![接続ステータス](./media/connection-status.png)](./media/connection-status.png)</span><span class="sxs-lookup"><span data-stu-id="1dc99-114">[![connection status](./media/connection-status.png)](./media/connection-status.png)</span></span>

## <a name="create-a-button-to-manually-switch-between-online-and-offline-modes"></a><span data-ttu-id="1dc99-115">手動でオンラインとオフライン モードを切り替えるためのボタンを作成</span><span class="sxs-lookup"><span data-stu-id="1dc99-115">Create a button to manually switch between online and offline modes</span></span>
<span data-ttu-id="1dc99-116">Retail Modern POS にオンラインとオフライン モードを手動で切り替えるボタンを追加できます。</span><span class="sxs-lookup"><span data-stu-id="1dc99-116">You can add a button to Retail Modern POS to manually switch between online and offline modes.</span></span> <span data-ttu-id="1dc99-117">**POS 操作 917 – データベース接続ステータス**のボタンを作成します。</span><span class="sxs-lookup"><span data-stu-id="1dc99-117">Create a button for **POS operation 917 – Database connection status**.</span></span> <span data-ttu-id="1dc99-118">接続または切断するには、ボタンをトグルとして切り替えて使用します。</span><span class="sxs-lookup"><span data-stu-id="1dc99-118">Use the button as a toggle to connect or disconnect.</span></span>

## <a name="operations-that-can-be-completed-when-the-channel-database-is-offline"></a><span data-ttu-id="1dc99-119">チャネル データベースがオフラインのときに実行できる操作</span><span class="sxs-lookup"><span data-stu-id="1dc99-119">Operations that can be completed when the channel database is offline</span></span>
<span data-ttu-id="1dc99-120">チャネル データベースがオフラインときは、次の操作を完了することができます。</span><span class="sxs-lookup"><span data-stu-id="1dc99-120">You can complete the following operations when the channel database is offline.</span></span> 

> [!NOTE]
> <span data-ttu-id="1dc99-121">Commerce Data Exchange: リアルタイム サービスが必要な機能があれば、操作がサポートされていないことを示すエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1dc99-121">If any functionality requires Commerce Data Exchange: Real-time Service, you receive an error message that states that the operation isn't supported.</span></span> <span data-ttu-id="1dc99-122">この例は、在庫検索操作です。</span><span class="sxs-lookup"><span data-stu-id="1dc99-122">An example of this is the Inventory Lookup operation.</span></span> <span data-ttu-id="1dc99-123">工程では品目の検索が許可されますが、HQ への接続がない場合、店舗の調達グループで定義された店舗の倉庫と関連する店舗の倉庫から入手可能な在庫データに必要なリアルタイム サービス コールは失敗します。</span><span class="sxs-lookup"><span data-stu-id="1dc99-123">While the operation will allow you to look up an item, the Real-time Service call necessary to get available inventory data from the store's warehouse and the related store's warehouses as defined in the store's Fulfillment Group will fail if there is no connectivity to HQ.</span></span>   

<span data-ttu-id="1dc99-124">**ヒント:** オフライン データベースで使用できるデータにのみ、レポートおよびその他の操作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="1dc99-124">**Tip:** Reports and other operations will act only on the data that is available in the offline database.</span></span>

| <span data-ttu-id="1dc99-125">操作 ID</span><span class="sxs-lookup"><span data-stu-id="1dc99-125">Operation ID</span></span> | <span data-ttu-id="1dc99-126">説明</span><span class="sxs-lookup"><span data-stu-id="1dc99-126">Description</span></span>                         |
|--------------|-------------------------------------|
| <span data-ttu-id="1dc99-127">100</span><span class="sxs-lookup"><span data-stu-id="1dc99-127">100</span></span>          | <span data-ttu-id="1dc99-128">製品売上</span><span class="sxs-lookup"><span data-stu-id="1dc99-128">Product sale</span></span>                        |
| <span data-ttu-id="1dc99-129">101</span><span class="sxs-lookup"><span data-stu-id="1dc99-129">101</span></span>          | <span data-ttu-id="1dc99-130">価格の確認</span><span class="sxs-lookup"><span data-stu-id="1dc99-130">Price check</span></span>                         |
| <span data-ttu-id="1dc99-131">102</span><span class="sxs-lookup"><span data-stu-id="1dc99-131">102</span></span>          | <span data-ttu-id="1dc99-132">製品の無効化</span><span class="sxs-lookup"><span data-stu-id="1dc99-132">Void product</span></span>                        |
| <span data-ttu-id="1dc99-133">103</span><span class="sxs-lookup"><span data-stu-id="1dc99-133">103</span></span>          | <span data-ttu-id="1dc99-134">製品コメント</span><span class="sxs-lookup"><span data-stu-id="1dc99-134">Product comment</span></span>                     |
| <span data-ttu-id="1dc99-135">104</span><span class="sxs-lookup"><span data-stu-id="1dc99-135">104</span></span>          | <span data-ttu-id="1dc99-136">価格変更</span><span class="sxs-lookup"><span data-stu-id="1dc99-136">Price override</span></span>                      |
| <span data-ttu-id="1dc99-137">105</span><span class="sxs-lookup"><span data-stu-id="1dc99-137">105</span></span>          | <span data-ttu-id="1dc99-138">数量の設定</span><span class="sxs-lookup"><span data-stu-id="1dc99-138">Set quantity</span></span>                        |
| <span data-ttu-id="1dc99-139">106</span><span class="sxs-lookup"><span data-stu-id="1dc99-139">106</span></span>          | <span data-ttu-id="1dc99-140">数量のクリア</span><span class="sxs-lookup"><span data-stu-id="1dc99-140">Clear quantity</span></span>                      |
| <span data-ttu-id="1dc99-141">108</span><span class="sxs-lookup"><span data-stu-id="1dc99-141">108</span></span>          | <span data-ttu-id="1dc99-142">製品検索</span><span class="sxs-lookup"><span data-stu-id="1dc99-142">Product search</span></span>                      |
| <span data-ttu-id="1dc99-143">109</span><span class="sxs-lookup"><span data-stu-id="1dc99-143">109</span></span>          | <span data-ttu-id="1dc99-144">返品</span><span class="sxs-lookup"><span data-stu-id="1dc99-144">Return product</span></span>                      |
| <span data-ttu-id="1dc99-145">115</span><span class="sxs-lookup"><span data-stu-id="1dc99-145">115</span></span>          | <span data-ttu-id="1dc99-146">仕訳帳の表示</span><span class="sxs-lookup"><span data-stu-id="1dc99-146">Show journal</span></span>                        |
| <span data-ttu-id="1dc99-147">117</span><span class="sxs-lookup"><span data-stu-id="1dc99-147">117</span></span>          | <span data-ttu-id="1dc99-148">ロイヤルティ カードの追加</span><span class="sxs-lookup"><span data-stu-id="1dc99-148">Add loyalty card</span></span>                    |
| <span data-ttu-id="1dc99-149">123</span><span class="sxs-lookup"><span data-stu-id="1dc99-149">123</span></span>          | <span data-ttu-id="1dc99-150">単位の変更</span><span class="sxs-lookup"><span data-stu-id="1dc99-150">Change unit of measure</span></span>              |
| <span data-ttu-id="1dc99-151">128</span><span class="sxs-lookup"><span data-stu-id="1dc99-151">128</span></span>          | <span data-ttu-id="1dc99-152">リストから取引税を上書きする</span><span class="sxs-lookup"><span data-stu-id="1dc99-152">Override transaction tax from list</span></span>  |
| <span data-ttu-id="1dc99-153">130</span><span class="sxs-lookup"><span data-stu-id="1dc99-153">130</span></span>          | <span data-ttu-id="1dc99-154">リストから明細行の製品税を上書きする</span><span class="sxs-lookup"><span data-stu-id="1dc99-154">Override line product tax from list</span></span> |
| <span data-ttu-id="1dc99-155">132</span><span class="sxs-lookup"><span data-stu-id="1dc99-155">132</span></span>          | <span data-ttu-id="1dc99-156">預金の上書き</span><span class="sxs-lookup"><span data-stu-id="1dc99-156">Deposit override</span></span>                    |
| <span data-ttu-id="1dc99-157">134</span><span class="sxs-lookup"><span data-stu-id="1dc99-157">134</span></span>          | <span data-ttu-id="1dc99-158">所属を追加</span><span class="sxs-lookup"><span data-stu-id="1dc99-158">Add affiliation</span></span>                     |
| <span data-ttu-id="1dc99-159">135</span><span class="sxs-lookup"><span data-stu-id="1dc99-159">135</span></span>          | <span data-ttu-id="1dc99-160">リストから所属を追加</span><span class="sxs-lookup"><span data-stu-id="1dc99-160">Add affiliation from list</span></span>           |
| <span data-ttu-id="1dc99-161">200</span><span class="sxs-lookup"><span data-stu-id="1dc99-161">200</span></span>          | <span data-ttu-id="1dc99-162">現金で支払う</span><span class="sxs-lookup"><span data-stu-id="1dc99-162">Pay cash</span></span>                            |
| <span data-ttu-id="1dc99-163">202</span><span class="sxs-lookup"><span data-stu-id="1dc99-163">202</span></span>          | <span data-ttu-id="1dc99-164">顧客口座から支払う</span><span class="sxs-lookup"><span data-stu-id="1dc99-164">Pay customer account</span></span>                |
| <span data-ttu-id="1dc99-165">203</span><span class="sxs-lookup"><span data-stu-id="1dc99-165">203</span></span>          | <span data-ttu-id="1dc99-166">各種通貨で支払う</span><span class="sxs-lookup"><span data-stu-id="1dc99-166">Pay currency</span></span>                        |
| <span data-ttu-id="1dc99-167">206</span><span class="sxs-lookup"><span data-stu-id="1dc99-167">206</span></span>          | <span data-ttu-id="1dc99-168">現金で即支払う</span><span class="sxs-lookup"><span data-stu-id="1dc99-168">Pay cash quick</span></span>                      |
| <span data-ttu-id="1dc99-169">211</span><span class="sxs-lookup"><span data-stu-id="1dc99-169">211</span></span>          | <span data-ttu-id="1dc99-170">支払の無効化</span><span class="sxs-lookup"><span data-stu-id="1dc99-170">Void payment</span></span>                        |
| <span data-ttu-id="1dc99-171">214</span><span class="sxs-lookup"><span data-stu-id="1dc99-171">214</span></span>          | <span data-ttu-id="1dc99-172">ギフト カードで支払う</span><span class="sxs-lookup"><span data-stu-id="1dc99-172">Pay gift card</span></span>                       |
| <span data-ttu-id="1dc99-173">300</span><span class="sxs-lookup"><span data-stu-id="1dc99-173">300</span></span>          | <span data-ttu-id="1dc99-174">品目割引金額</span><span class="sxs-lookup"><span data-stu-id="1dc99-174">Line discount amount</span></span>                |
| <span data-ttu-id="1dc99-175">301</span><span class="sxs-lookup"><span data-stu-id="1dc99-175">301</span></span>          | <span data-ttu-id="1dc99-176">品目割引率</span><span class="sxs-lookup"><span data-stu-id="1dc99-176">Line discount percent</span></span>               |
| <span data-ttu-id="1dc99-177">302</span><span class="sxs-lookup"><span data-stu-id="1dc99-177">302</span></span>          | <span data-ttu-id="1dc99-178">合計割引金額</span><span class="sxs-lookup"><span data-stu-id="1dc99-178">Total discount amount</span></span>               |
| <span data-ttu-id="1dc99-179">303</span><span class="sxs-lookup"><span data-stu-id="1dc99-179">303</span></span>          | <span data-ttu-id="1dc99-180">合計割引率</span><span class="sxs-lookup"><span data-stu-id="1dc99-180">Total discount percent</span></span>              |
| <span data-ttu-id="1dc99-181">500</span><span class="sxs-lookup"><span data-stu-id="1dc99-181">500</span></span>          | <span data-ttu-id="1dc99-182">トランザクションの無効化</span><span class="sxs-lookup"><span data-stu-id="1dc99-182">Void transaction</span></span>                    |
| <span data-ttu-id="1dc99-183">501</span><span class="sxs-lookup"><span data-stu-id="1dc99-183">501</span></span>          | <span data-ttu-id="1dc99-184">トランザクション コメント</span><span class="sxs-lookup"><span data-stu-id="1dc99-184">Transaction comment</span></span>                 |
| <span data-ttu-id="1dc99-185">503</span><span class="sxs-lookup"><span data-stu-id="1dc99-185">503</span></span>          | <span data-ttu-id="1dc99-186">トランザクションの中断</span><span class="sxs-lookup"><span data-stu-id="1dc99-186">Suspend transaction</span></span>                 |
| <span data-ttu-id="1dc99-187">512</span><span class="sxs-lookup"><span data-stu-id="1dc99-187">512</span></span>          | <span data-ttu-id="1dc99-188">ギフト カードの発行</span><span class="sxs-lookup"><span data-stu-id="1dc99-188">Issue gift card</span></span>                     |
| <span data-ttu-id="1dc99-189">515</span><span class="sxs-lookup"><span data-stu-id="1dc99-189">515</span></span>          | <span data-ttu-id="1dc99-190">注文の取り消し</span><span class="sxs-lookup"><span data-stu-id="1dc99-190">Recall order</span></span>                        |
| <span data-ttu-id="1dc99-191">519</span><span class="sxs-lookup"><span data-stu-id="1dc99-191">519</span></span>          | <span data-ttu-id="1dc99-192">ギフト カードに追加</span><span class="sxs-lookup"><span data-stu-id="1dc99-192">Add to gift card</span></span>                    |
| <span data-ttu-id="1dc99-193">520</span><span class="sxs-lookup"><span data-stu-id="1dc99-193">520</span></span>          | <span data-ttu-id="1dc99-194">ギフト カード残高</span><span class="sxs-lookup"><span data-stu-id="1dc99-194">Gift card balance</span></span>                   |
| <span data-ttu-id="1dc99-195">602</span><span class="sxs-lookup"><span data-stu-id="1dc99-195">602</span></span>          | <span data-ttu-id="1dc99-196">顧客検索</span><span class="sxs-lookup"><span data-stu-id="1dc99-196">Customer search</span></span>                     |
| <span data-ttu-id="1dc99-197">603</span><span class="sxs-lookup"><span data-stu-id="1dc99-197">603</span></span>          | <span data-ttu-id="1dc99-198">顧客のクリア</span><span class="sxs-lookup"><span data-stu-id="1dc99-198">Customer clear</span></span>                      |
| <span data-ttu-id="1dc99-199">612</span><span class="sxs-lookup"><span data-stu-id="1dc99-199">612</span></span>          | <span data-ttu-id="1dc99-200">顧客の追加</span><span class="sxs-lookup"><span data-stu-id="1dc99-200">Customer add</span></span>                        |
| <span data-ttu-id="1dc99-201">622</span><span class="sxs-lookup"><span data-stu-id="1dc99-201">622</span></span>          | <span data-ttu-id="1dc99-202">検索</span><span class="sxs-lookup"><span data-stu-id="1dc99-202">Search</span></span>                              |
| <span data-ttu-id="1dc99-203">623</span><span class="sxs-lookup"><span data-stu-id="1dc99-203">623</span></span>          | <span data-ttu-id="1dc99-204">顧客の編集</span><span class="sxs-lookup"><span data-stu-id="1dc99-204">Edit customer</span></span>                       |
| <span data-ttu-id="1dc99-205">701</span><span class="sxs-lookup"><span data-stu-id="1dc99-205">701</span></span>          | <span data-ttu-id="1dc99-206">ログオフ</span><span class="sxs-lookup"><span data-stu-id="1dc99-206">Log off</span></span>                             |
| <span data-ttu-id="1dc99-207">703</span><span class="sxs-lookup"><span data-stu-id="1dc99-207">703</span></span>          | <span data-ttu-id="1dc99-208">レジスターのロック</span><span class="sxs-lookup"><span data-stu-id="1dc99-208">Lock register</span></span>                       |
| <span data-ttu-id="1dc99-209">801</span><span class="sxs-lookup"><span data-stu-id="1dc99-209">801</span></span>          | <span data-ttu-id="1dc99-210">在庫検索</span><span class="sxs-lookup"><span data-stu-id="1dc99-210">Inventory lookup</span></span>                    |
| <span data-ttu-id="1dc99-211">802</span><span class="sxs-lookup"><span data-stu-id="1dc99-211">802</span></span>          | <span data-ttu-id="1dc99-212">在庫数</span><span class="sxs-lookup"><span data-stu-id="1dc99-212">Stock count</span></span>                         |
| <span data-ttu-id="1dc99-213">917</span><span class="sxs-lookup"><span data-stu-id="1dc99-213">917</span></span>          | <span data-ttu-id="1dc99-214">データベース接続ステータス</span><span class="sxs-lookup"><span data-stu-id="1dc99-214">Database connection status</span></span>          |
| <span data-ttu-id="1dc99-215">920</span><span class="sxs-lookup"><span data-stu-id="1dc99-215">920</span></span>          | <span data-ttu-id="1dc99-216">タイム レコーダー</span><span class="sxs-lookup"><span data-stu-id="1dc99-216">Time clock</span></span>                          |
| <span data-ttu-id="1dc99-217">921</span><span class="sxs-lookup"><span data-stu-id="1dc99-217">921</span></span>          | <span data-ttu-id="1dc99-218">タイム レコーダー エントリの表示</span><span class="sxs-lookup"><span data-stu-id="1dc99-218">View time clock entries</span></span>             |
| <span data-ttu-id="1dc99-219">922</span><span class="sxs-lookup"><span data-stu-id="1dc99-219">922</span></span>          | <span data-ttu-id="1dc99-220">製品の詳細表示</span><span class="sxs-lookup"><span data-stu-id="1dc99-220">View product details</span></span>                |
| <span data-ttu-id="1dc99-221">1003</span><span class="sxs-lookup"><span data-stu-id="1dc99-221">1003</span></span>         | <span data-ttu-id="1dc99-222">レポートの表示</span><span class="sxs-lookup"><span data-stu-id="1dc99-222">View reports</span></span>                        |
| <span data-ttu-id="1dc99-223">1052</span><span class="sxs-lookup"><span data-stu-id="1dc99-223">1052</span></span>         | <span data-ttu-id="1dc99-224">支払/入金申告</span><span class="sxs-lookup"><span data-stu-id="1dc99-224">Tender declaration</span></span>                  |
| <span data-ttu-id="1dc99-225">1200</span><span class="sxs-lookup"><span data-stu-id="1dc99-225">1200</span></span>         | <span data-ttu-id="1dc99-226">開始金額の申告</span><span class="sxs-lookup"><span data-stu-id="1dc99-226">Declare start amount</span></span>                |
| <span data-ttu-id="1dc99-227">1201</span><span class="sxs-lookup"><span data-stu-id="1dc99-227">1201</span></span>         | <span data-ttu-id="1dc99-228">釣銭入力</span><span class="sxs-lookup"><span data-stu-id="1dc99-228">Float entry</span></span>                         |
| <span data-ttu-id="1dc99-229">1210</span><span class="sxs-lookup"><span data-stu-id="1dc99-229">1210</span></span>         | <span data-ttu-id="1dc99-230">支払/入金の削除</span><span class="sxs-lookup"><span data-stu-id="1dc99-230">Tender removal</span></span>                      |
| <span data-ttu-id="1dc99-231">1211</span><span class="sxs-lookup"><span data-stu-id="1dc99-231">1211</span></span>         | <span data-ttu-id="1dc99-232">金庫保管</span><span class="sxs-lookup"><span data-stu-id="1dc99-232">Safe drop</span></span>                           |
| <span data-ttu-id="1dc99-233">1212</span><span class="sxs-lookup"><span data-stu-id="1dc99-233">1212</span></span>         | <span data-ttu-id="1dc99-234">銀行入金</span><span class="sxs-lookup"><span data-stu-id="1dc99-234">Bank drop</span></span>                           |

## <a name="operations-that-cant-be-completed-when-the-channel-database-is-offline"></a><span data-ttu-id="1dc99-235">チャネル データベースがオフラインのときに実行できない操作</span><span class="sxs-lookup"><span data-stu-id="1dc99-235">Operations that can’t be completed when the channel database is offline</span></span>
<span data-ttu-id="1dc99-236">チャネル データベースがオフラインときは、次の操作を完了することができません。</span><span class="sxs-lookup"><span data-stu-id="1dc99-236">You can’t complete the following operations when the channel database is offline.</span></span>

| <span data-ttu-id="1dc99-237">操作 ID</span><span class="sxs-lookup"><span data-stu-id="1dc99-237">Operation ID</span></span> | <span data-ttu-id="1dc99-238">説明</span><span class="sxs-lookup"><span data-stu-id="1dc99-238">Description</span></span>       |
|--------------|-------------------|
| <span data-ttu-id="1dc99-239">207</span><span class="sxs-lookup"><span data-stu-id="1dc99-239">207</span></span>          | <span data-ttu-id="1dc99-240">ロイヤルティ カードで支払う</span><span class="sxs-lookup"><span data-stu-id="1dc99-240">Pay loyalty card</span></span>  |
| <span data-ttu-id="1dc99-241">707</span><span class="sxs-lookup"><span data-stu-id="1dc99-241">707</span></span>          | <span data-ttu-id="1dc99-242">デバイスのアクティブ化</span><span class="sxs-lookup"><span data-stu-id="1dc99-242">Activate device</span></span>   |
| <span data-ttu-id="1dc99-243">708</span><span class="sxs-lookup"><span data-stu-id="1dc99-243">708</span></span>          | <span data-ttu-id="1dc99-244">デバイスの無効化</span><span class="sxs-lookup"><span data-stu-id="1dc99-244">Inactivate device</span></span> |
| <span data-ttu-id="1dc99-245">1053</span><span class="sxs-lookup"><span data-stu-id="1dc99-245">1053</span></span>         | <span data-ttu-id="1dc99-246">シフトのブラインド クローズ</span><span class="sxs-lookup"><span data-stu-id="1dc99-246">Blind close shift</span></span> |
| <span data-ttu-id="1dc99-247">1054</span><span class="sxs-lookup"><span data-stu-id="1dc99-247">1054</span></span>         | <span data-ttu-id="1dc99-248">シフトの中断</span><span class="sxs-lookup"><span data-stu-id="1dc99-248">Suspend shift</span></span>     |
| <span data-ttu-id="1dc99-249">1055</span><span class="sxs-lookup"><span data-stu-id="1dc99-249">1055</span></span>         | <span data-ttu-id="1dc99-250">シフトのクローズ</span><span class="sxs-lookup"><span data-stu-id="1dc99-250">Close shift</span></span>       |
| <span data-ttu-id="1dc99-251">1056</span><span class="sxs-lookup"><span data-stu-id="1dc99-251">1056</span></span>         | <span data-ttu-id="1dc99-252">X の印刷</span><span class="sxs-lookup"><span data-stu-id="1dc99-252">Print X</span></span>           |
| <span data-ttu-id="1dc99-253">1057</span><span class="sxs-lookup"><span data-stu-id="1dc99-253">1057</span></span>         | <span data-ttu-id="1dc99-254">再印刷 Z</span><span class="sxs-lookup"><span data-stu-id="1dc99-254">Reprint Z</span></span>         |





