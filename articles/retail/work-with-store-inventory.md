---
title: "店舗在庫の管理"
description: "この記事では、在庫の管理に使用できるドキュメントのタイプについて説明します。"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 031a2f9c27bb6223dc65c3ae6b3d4e3ce775ae21
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="manage-store-inventory"></a><span data-ttu-id="40d30-103">店舗在庫の管理</span><span class="sxs-lookup"><span data-stu-id="40d30-103">Manage store inventory</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="40d30-104">この記事では、在庫の管理に使用できるドキュメントのタイプについて説明します。</span><span class="sxs-lookup"><span data-stu-id="40d30-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="40d30-105">組織の在庫を管理するには、次のドキュメント タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="40d30-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="40d30-106">発注書</span><span class="sxs-lookup"><span data-stu-id="40d30-106">Purchase orders</span></span>
<span data-ttu-id="40d30-107">発注書は本社で作成されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="40d30-108">小売倉庫が発注書ヘッダーに含まれている場合、Modern POS (MPOS) または Microsoft Dynamics 365 for Retail のクラウド POS を使用して、店舗でこの発注書を受け入れることができます。</span><span class="sxs-lookup"><span data-stu-id="40d30-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="40d30-109">店舗で受け入れる数量が入力された後、追加変更に対してその数量をローカルに保存できます。</span><span class="sxs-lookup"><span data-stu-id="40d30-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="40d30-110">または、数量を確定して本社に送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="40d30-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="40d30-111">本社では、店舗で受け入れた数量が Dynamics 365 for Retail の発注書の [**今回受入**] フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="40d30-112">移動オーダー</span><span class="sxs-lookup"><span data-stu-id="40d30-112">Transfer orders</span></span>
<span data-ttu-id="40d30-113">移動オーダーでは、特定の店舗が品目の出荷元の場所であることを指定できます。</span><span class="sxs-lookup"><span data-stu-id="40d30-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="40d30-114">この場合、移動オーダーは MPOS またはクラウド POS のピッキング要求として店舗に表示されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="40d30-115">必要な数量をピッキングした後、その数量が確定され、本社に送信されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="40d30-116">本社では、店舗でピッキングされた数量が Dynamics 365 for Retail の移動オーダーの [**今すぐ出荷**] フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="40d30-117">移動オーダーでは、特定の店舗が品目の出荷先の場所であることを指定できます。</span><span class="sxs-lookup"><span data-stu-id="40d30-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="40d30-118">この場合、移動オーダーは MPOS またはクラウド POS の入荷要求として店舗に表示されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="40d30-119">店舗で受け入れる数量が入力された後、追加変更に対してその数量をローカルに保存できます。</span><span class="sxs-lookup"><span data-stu-id="40d30-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="40d30-120">または、数量を確定して本社に送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="40d30-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="40d30-121">本社では、店舗で受け入れた数量が Dynamics 365 for Retail の移動オーダーの [**今回受入**] フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="40d30-122">在庫数</span><span class="sxs-lookup"><span data-stu-id="40d30-122">Stock counts</span></span>
<span data-ttu-id="40d30-123">在庫棚卸は、計画済または計画外のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="40d30-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="40d30-124">計画済の在庫棚卸は、棚卸を行う必要がある品目を指定する本社で開始されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="40d30-125">本社で店舗に送信可能な棚卸ドキュメントが作成され、実際の手持在庫数量が店舗で MPOS またはクラウド POS に入力されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="40d30-126">手動在庫棚卸は店舗で開始され、MPOS またはクラウド POS で実際の手持在庫数量が更新されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="40d30-127">計画済在庫棚卸とは異なり、計画外在庫棚卸に品目の定義済リストはありません。</span><span class="sxs-lookup"><span data-stu-id="40d30-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="40d30-128">いずれかのタイプの在庫棚卸が完了すると、その在庫棚卸が確定され、本社に送信されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="40d30-129">本社でその在庫棚卸が検証され、転記されます。</span><span class="sxs-lookup"><span data-stu-id="40d30-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="40d30-130">在庫検索</span><span class="sxs-lookup"><span data-stu-id="40d30-130">Inventory lookup</span></span>
<span data-ttu-id="40d30-131">複数の店舗および倉庫の現在の手持在庫製品の数量は、在庫検索ページで表示できます。</span><span class="sxs-lookup"><span data-stu-id="40d30-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="40d30-132">手持在庫の現在の数量に加えて、将来の納期回答可能在庫 (ATP) 数量は、各店舗ごとに表示できます。</span><span class="sxs-lookup"><span data-stu-id="40d30-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="40d30-133">これを行うには、表示したい ATP の店舗を選択して、次に [**店舗の使用可能性を表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="40d30-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





