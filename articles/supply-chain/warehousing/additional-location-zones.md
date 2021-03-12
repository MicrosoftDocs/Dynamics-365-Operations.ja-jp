---
title: 追加の場所ゾーン
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management に追加された新しい場所ゾーンの概要を示します。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 662725edf5bf8d95be038f7c989b73d8d05fa0df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996429"
---
# <a name="additional-location-zones"></a><span data-ttu-id="c9394-103">追加の場所ゾーン</span><span class="sxs-lookup"><span data-stu-id="c9394-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9394-104">Microsoft Dynamics 365 Supply Chain Management では、3 つの新しいゾーン フィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c9394-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c9394-105">倉庫管理者は、これらを使用して追加の倉庫組織またはレイアウトを定義できます。</span><span class="sxs-lookup"><span data-stu-id="c9394-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="c9394-106">新しいゾーン フィールドは、手動で設定するか、または **場所設定** ウィザードを使用して設定できます。</span><span class="sxs-lookup"><span data-stu-id="c9394-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="c9394-107">これらは、場所テーブルを使用する任意のクエリまたはフィルター処理で使用できます。</span><span class="sxs-lookup"><span data-stu-id="c9394-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="c9394-108">ゾーン フィールドを使用するための追加の設定は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="c9394-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="c9394-109">追加の場所ゾーン機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="c9394-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="c9394-110">*追加の場所ゾーン* 機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9394-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="c9394-111">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c9394-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c9394-112">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="c9394-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c9394-113">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="c9394-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c9394-114">**機能名:** *追加の場所ゾーン*</span><span class="sxs-lookup"><span data-stu-id="c9394-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="c9394-115">場所ゾーンの使用</span><span class="sxs-lookup"><span data-stu-id="c9394-115">Use location zones</span></span>

1. <span data-ttu-id="c9394-116">**倉庫管理 \> 設定 \> 倉庫 \> 場所設定ウィザード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9394-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="c9394-117">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="c9394-117">Set the following values:</span></span>

    - <span data-ttu-id="c9394-118">**倉庫** フィールドで、_62_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9394-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="c9394-119">**ゾーン ID** フィールドで、_FLOOR_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9394-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="c9394-120">**追加ゾーン 1** フィールドで、_PICKZONE1_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9394-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="c9394-121">**追加ゾーン 2** フィールドで、_WEBSHOP1_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9394-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="c9394-122">**場所プロファイル ID** フィールドで、_FLOOR_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9394-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="c9394-123">**フロア** 明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9394-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="c9394-124">**開始番号** フィールドに _1_ を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9394-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="c9394-125">**終了番号** フィールドに _3_ を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9394-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="c9394-126">**通路** 明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9394-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="c9394-127">**開始番号** フィールドに _1_ を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9394-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="c9394-128">**終了番号** フィールドに _5_ を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9394-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="c9394-129">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9394-129">Select **Create**.</span></span>
8. <span data-ttu-id="c9394-130">新しい場所が追加されたことを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9394-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="c9394-131">メッセージを表示するには、**メッセージを表示する** のボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9394-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="c9394-132">**倉庫管理 \> 設定 \> 倉庫 \> 場所** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9394-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="c9394-133">新しい場所が一覧に表示され、すべてのゾーン フィールド (既存のゾーン フィールドと新しい追加ゾーン フィールド) が使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="c9394-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
