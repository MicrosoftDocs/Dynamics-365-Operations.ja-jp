---
title: "販売注文に対する同一バッチの引当"
description: "この記事では、在庫の単一のバッチに対して在庫引当を許可する製品の設定方法を説明します。"
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2df93fd40be28cadbf5cc518bf2de0f26a5942b5
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="20ba3-103">販売注文に対する同一バッチの引当</span><span class="sxs-lookup"><span data-stu-id="20ba3-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20ba3-104">この記事では、在庫の単一のバッチに対して在庫引当を許可する製品の設定方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="20ba3-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="20ba3-105">同じバッチの引当により、販売注文明細行の在庫を単一の在庫バッチに対して引当できます。</span><span class="sxs-lookup"><span data-stu-id="20ba3-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="20ba3-106">たとえば、壁紙を注文する顧客が、壁紙のロール間で不整合が生じないように、同じバッチまたはロットで注文全体に対応することを要求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="20ba3-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="20ba3-107">同じバッチの引当を使用する製品を設定するには、次の設定で、製品に割り当てる品目モデル グループ、追跡用分析コード グループ、および保管分析コード グループを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ba3-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="20ba3-108">**品目モデル グループ** – 品目モデル グループは、在庫ポリシーの**引当**フィールド グループで、**同じバッチの選択**と**要求の連結**が選択されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ba3-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="20ba3-109">**追跡用の分析コード グループ** – 追跡用分析コード グループでは、バッチ番号に対して**分析コード別補充計画**フィールドが選択されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20ba3-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="20ba3-110">**保管分析コード グループ** – 保管分析コード グループには**サイト**および**倉庫**に対して選択された**分析コード別補充計画**フィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="20ba3-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="20ba3-111">同じバッチの選択に対して設定された販売注文明細行の製品の在庫引当を行う場合、Microsoft Dynamics 365 for Finance and Operations は、単一の在庫バッチから注文数量を引当しようとします。</span><span class="sxs-lookup"><span data-stu-id="20ba3-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="20ba3-112">すべての特定のバッチ属性要件を考慮します。</span><span class="sxs-lookup"><span data-stu-id="20ba3-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="20ba3-113">数量が単一のバッチで対応できない場合は**同じバッチの引当の競合**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20ba3-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="20ba3-114">このページでは、引当を続行する際の問題と、実行できるアクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="20ba3-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="20ba3-115">次の条件は、バッチの引当を防ぐ場合があります。</span><span class="sxs-lookup"><span data-stu-id="20ba3-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="20ba3-116">バッチの廃棄コードに、販売の [**引当のブロック**] が [**ブロック**] とフラグ設定されている。</span><span class="sxs-lookup"><span data-stu-id="20ba3-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="20ba3-117">有効期限と該当する顧客の販売可能日数に基づくと、バッチが期限切れになっている。</span><span class="sxs-lookup"><span data-stu-id="20ba3-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="20ba3-118">品目モデル グループが先入れ先出し (FEFO) 日付管理対象で、品質保持期限日がピック基準として選択されている場合、品目には引き続き引当が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="20ba3-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="20ba3-119">有効期限、出庫期限、および顧客の販売可能日数に基づくと、バッチの在庫有効期間が十分に残っていない。</span><span class="sxs-lookup"><span data-stu-id="20ba3-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>





