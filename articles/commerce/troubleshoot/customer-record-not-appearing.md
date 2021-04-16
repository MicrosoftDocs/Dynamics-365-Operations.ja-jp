---
title: 顧客レコードが Commerce 本社に表示されない
description: このトピックでは、顧客レコードがすぐに Commerce 本社に表示されない場合に役立つトラブルシューティング ガイドを提供します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5499e3c059c9e735df87ef8b462d446e0710d90c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801798"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="6929b-103">顧客レコードが Commerce 本社に表示されない</span><span class="sxs-lookup"><span data-stu-id="6929b-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6929b-104">このトピックでは、顧客レコードがすぐに Commerce 本社に表示されない場合に役立つトラブルシューティング ガイドを提供します。</span><span class="sxs-lookup"><span data-stu-id="6929b-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="6929b-105">説明</span><span class="sxs-lookup"><span data-stu-id="6929b-105">Description</span></span>

<span data-ttu-id="6929b-106">電子商取引店舗のサインアップ フローを使用して新しい顧客レコードを作成する場合、対応する顧客レコードが Commerce 本社にすぐに表示されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="6929b-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="6929b-107">解像度</span><span class="sxs-lookup"><span data-stu-id="6929b-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="6929b-108">非同期モードでの顧客作成の無効化</span><span class="sxs-lookup"><span data-stu-id="6929b-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6929b-109">非同期の顧客作成を無効にすると、各レコードの作成によって Commerce 本社へのリアルタイムの要求が生成されるため、システム パフォーマンスに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6929b-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="6929b-110">さらに、Commerce 本社がダウンしている場合 (たとえばサービス フロー中)、新しい顧客作成フローではエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6929b-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="6929b-111">Commerce 本社で非同期モードでの顧客作成を無効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6929b-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6929b-112">**Retail と Commerce \> チャネル設定 \> オンライン ストアの設定 \> 機能プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6929b-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="6929b-113">オンライン チャネルの機能プロファイルをまだ使用していない場合は、それを作成します。</span><span class="sxs-lookup"><span data-stu-id="6929b-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="6929b-114">**非同期モードで顧客を作成** オプションが **いいえ** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6929b-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="6929b-115">**Retail と Commerce \> チャネル \> オンライン ストア** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6929b-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="6929b-116">非同期顧客作成を無効にするオンライン ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="6929b-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="6929b-117">**一般** タブで、**機能プロファイル** フィールドがオンライン チャネルに使用している機能プロファイルに設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6929b-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6929b-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6929b-118">Additional resources</span></span>

[<span data-ttu-id="6929b-119">Commerce での B2C テナントの設定</span><span class="sxs-lookup"><span data-stu-id="6929b-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
