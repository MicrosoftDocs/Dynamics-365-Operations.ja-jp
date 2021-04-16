---
title: 陸揚原価に仕入先の設定が追加されました
description: このトピックでは、陸揚原価モジュールを有効にした場合に既存の仕入先ページに追加される新しいフィールドについて説明します。 これらのフィールドを使用して、陸揚原価機能と組み合わせて使用する仕入先を設定します。
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 3a288517f77d1618f94f8539506d01a108e63fa5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829765"
---
# <a name="vendor-settings-added-for-landed-cost"></a><span data-ttu-id="75f63-104">陸揚原価に仕入先の設定が追加されました</span><span class="sxs-lookup"><span data-stu-id="75f63-104">Vendor settings added for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75f63-105">**陸揚原価** モジュールを有効にすると、既存の **仕入先** ページにいくつかの新しいフィールドが追加されます。</span><span class="sxs-lookup"><span data-stu-id="75f63-105">When you enable the **Landed cost** module, several new fields are added to the existing **Vendors** page.</span></span> <span data-ttu-id="75f63-106">これらのフィールドを使用して、陸揚原価機能と組み合わせて使用する仕入先を設定します。</span><span class="sxs-lookup"><span data-stu-id="75f63-106">You use these fields to set up the vendors that you will use together with Landed cost features.</span></span>

<span data-ttu-id="75f63-107">関連するフィールドを設定するには、**調達 \> 仕入先 \> すべての仕入先** に移動します。</span><span class="sxs-lookup"><span data-stu-id="75f63-107">To set the relevant fields, go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span> <span data-ttu-id="75f63-108">既存の仕入先を開くか、新しい仕入先を作成し、**その他の詳細** クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="75f63-108">Open an existing vendor, or create a new vendor, and then select the **Miscellaneous details** FastTab.</span></span> <span data-ttu-id="75f63-109">**陸揚原価** モジュールが追加した新しいフィールドはすべて、**航海** ヘッダーの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="75f63-109">All the new fields that the **Landed cost** module adds appear under the **Voyages** heading.</span></span> <span data-ttu-id="75f63-110">次の表でこれらのフィールドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="75f63-110">The following table describes these fields.</span></span>

| <span data-ttu-id="75f63-111">フィールド</span><span class="sxs-lookup"><span data-stu-id="75f63-111">Field</span></span> | <span data-ttu-id="75f63-112">説明</span><span class="sxs-lookup"><span data-stu-id="75f63-112">Description</span></span> |
|---|---|
| <span data-ttu-id="75f63-113">出荷タイプ</span><span class="sxs-lookup"><span data-stu-id="75f63-113">Shipping type</span></span> | <p><span data-ttu-id="75f63-114">陸揚原価に関係する仕入先ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="75f63-114">Select the vendor's role in relation to Landed cost:</span></span></p><ul><li><span data-ttu-id="75f63-115">**なし** – 仕入先には、陸揚原価に関連する特定のロールはありません。</span><span class="sxs-lookup"><span data-stu-id="75f63-115">**None** – The vendor has no specific role that is related to Landed cost.</span></span> <span data-ttu-id="75f63-116">ほとんどの仕入先には特定のロールが割り当がないため、この値が既定の設定です。</span><span class="sxs-lookup"><span data-stu-id="75f63-116">This value is the default setting, because most vendors will probably have no specific role.</span></span></li><li><span data-ttu-id="75f63-117">**出荷会社** – 仕入先は出荷会社です。</span><span class="sxs-lookup"><span data-stu-id="75f63-117">**Shipping company** – The vendor is a shipping company.</span></span> <span data-ttu-id="75f63-118">この出荷タイプの仕入先は、**航海** ページの **出荷会社** フィールドで選択できます。</span><span class="sxs-lookup"><span data-stu-id="75f63-118">Vendors that have this shipping type are available for selection in the **Shipping company** field on the **Voyages** page.</span></span></li><li><span data-ttu-id="75f63-119">**関税ブローカー** – 仕入先は関税ブローカーです。</span><span class="sxs-lookup"><span data-stu-id="75f63-119">**Customs broker** – The vendor is a customs broker.</span></span> <span data-ttu-id="75f63-120">この出荷タイプの仕入先は、**フォリオ** ページの **関税ブローカー** フィールドで選択できます。</span><span class="sxs-lookup"><span data-stu-id="75f63-120">Vendors that have this shipping type are available for selection in the **Customs broker** field on the **Folios** page.</span></span></li><li><span data-ttu-id="75f63-121">**エージェント** – 仕入先はエージェントです。</span><span class="sxs-lookup"><span data-stu-id="75f63-121">**Agent** – The vendor is an agent.</span></span> <span data-ttu-id="75f63-122">この出荷タイプの仕入先は、**仕入先** および **発注書** ページの **エージェント** フィールドで選択できます。</span><span class="sxs-lookup"><span data-stu-id="75f63-122">Vendors that have this shipping type are available for selection in the **Agent** field on the **Vendors** and **Purchase orders** pages.</span></span></li></ul> |
| <span data-ttu-id="75f63-123">原価タイプ グループ</span><span class="sxs-lookup"><span data-stu-id="75f63-123">Cost type group</span></span> | <span data-ttu-id="75f63-124">[自動原価](auto-cost-setup.md) を選択するために、仕入先を原価タイプ グループに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="75f63-124">Assign the vendor to a cost type group for the purpose of selecting [auto costs](auto-cost-setup.md).</span></span> |
| <span data-ttu-id="75f63-125">出荷元港</span><span class="sxs-lookup"><span data-stu-id="75f63-125">From port</span></span> | <span data-ttu-id="75f63-126">航海の出港地を選択します。</span><span class="sxs-lookup"><span data-stu-id="75f63-126">Select the port of origin for the voyage.</span></span> |
| <span data-ttu-id="75f63-127">エージェント</span><span class="sxs-lookup"><span data-stu-id="75f63-127">Agent</span></span> | <span data-ttu-id="75f63-128">仕入先から購買を行う場合の既定のエージェント。</span><span class="sxs-lookup"><span data-stu-id="75f63-128">The default agent when purchases are made from the vendor.</span></span> |
| <span data-ttu-id="75f63-129">輸入原価仕入先</span><span class="sxs-lookup"><span data-stu-id="75f63-129">Import costing vendor</span></span> | <p><span data-ttu-id="75f63-130">仕入先が陸揚原価仕入先であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="75f63-130">Indicate whether the vendor is a Landed cost vendor.</span></span></p><p><span data-ttu-id="75f63-131">**ヒント:** このフィールドをレコード レベルのセキュリティと使用して、航海の作成時に表示される発注書を制限できます。</span><span class="sxs-lookup"><span data-stu-id="75f63-131">**Tip:** You can use this field together with record-level security to limit the purchase orders that are shown when a voyage is created.</span></span></p> |
| <span data-ttu-id="75f63-132">出荷会社</span><span class="sxs-lookup"><span data-stu-id="75f63-132">Shipping company</span></span> | <span data-ttu-id="75f63-133">仕入先に対する発注書を作成するときに使用する、既定の出荷会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="75f63-133">Select the default shipping company that is used when purchase orders are created for the vendor.</span></span> |
| <span data-ttu-id="75f63-134">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="75f63-134">Services provider</span></span> | <span data-ttu-id="75f63-135">仕入先がサービス プロバイダーかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="75f63-135">Indicate whether the vendor is services provider.</span></span> |
| <span data-ttu-id="75f63-136">超過/過少許容範囲グループ</span><span class="sxs-lookup"><span data-stu-id="75f63-136">Over/Under tolerance group</span></span> | <span data-ttu-id="75f63-137">仕入先の既定の超過/過小許容範囲グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="75f63-137">Select the default over/under tolerance group for the vendor.</span></span> |
