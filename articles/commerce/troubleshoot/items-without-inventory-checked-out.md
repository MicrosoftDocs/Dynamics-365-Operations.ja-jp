---
title: 在庫のない品目はチェックアウトできる
description: このトピックでは、顧客が在庫切れ品目を買い物カゴに追加してチェックアウトに進む際に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018461"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="ce30d-103">在庫のない品目はチェックアウトできる</span><span class="sxs-lookup"><span data-stu-id="ce30d-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce30d-104">このトピックでは、顧客が在庫切れ品目を買い物カゴに追加してチェックアウトに進む際に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="ce30d-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="ce30d-105">説明</span><span class="sxs-lookup"><span data-stu-id="ce30d-105">Description</span></span>

<span data-ttu-id="ce30d-106">ユーザーは、店舗に在庫がない場合でも品目をカートに追加し、チェックアウト ページに進みます。</span><span class="sxs-lookup"><span data-stu-id="ce30d-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="ce30d-107">解像度</span><span class="sxs-lookup"><span data-stu-id="ce30d-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="ce30d-108">Commerce サイト ビルダーの在庫切れエラーを表示するプロパティの有効化</span><span class="sxs-lookup"><span data-stu-id="ce30d-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="ce30d-109">Commerce サイト ビルダーの **在庫切れエラーを表示する** プロパティを有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ce30d-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ce30d-110">作業しているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce30d-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="ce30d-111">左のナビゲーション ウィンドウで、**ページ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce30d-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="ce30d-112">**CartPage** を選択してして開きます。</span><span class="sxs-lookup"><span data-stu-id="ce30d-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="ce30d-113">**買い物かご 1** スロットを選択してから **編集** を選択し、プロパティ ウィンドウで **在庫切れエラーを表示する** チェック ボックス を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce30d-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="ce30d-114">ページを保存してプ公開します。</span><span class="sxs-lookup"><span data-stu-id="ce30d-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce30d-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ce30d-115">Additional resources</span></span>

[<span data-ttu-id="ce30d-116">在庫設定の適用</span><span class="sxs-lookup"><span data-stu-id="ce30d-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="ce30d-117">小売チャンネルの引当可能在庫数量の計算</span><span class="sxs-lookup"><span data-stu-id="ce30d-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="ce30d-118">在庫バッファーと在庫レベルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ce30d-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
