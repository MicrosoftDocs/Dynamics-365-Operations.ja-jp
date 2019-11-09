---
title: 自動化エンティティ格納更新
description: このトピックでは自動化エンティティ格納更新を有効にする方法について説明します。
author: MilindaV2
manager: AnnBe
ms.date: 01/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: AutomatedEntityStoreRefresh
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27661
ms.assetid: 861cfa94-c6f3-4c84-89ac-22c78bf6b7a4
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca7584ce242bbc4c4545b230c3d6cc3483aff065
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174579"
---
# <a name="automated-entity-store-refresh"></a><span data-ttu-id="febfa-103">自動化エンティティ格納更新</span><span class="sxs-lookup"><span data-stu-id="febfa-103">Automated Entity store refresh</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="febfa-104">概要</span><span class="sxs-lookup"><span data-stu-id="febfa-104">Overview</span></span>

<span data-ttu-id="febfa-105">エンティティ格納が自動化され、システムにより管理されます。</span><span class="sxs-lookup"><span data-stu-id="febfa-105">Entity store refresh is automated and managed by the system.</span></span> <span data-ttu-id="febfa-106">管理者はシステム バッチ スケジュールを使用してエンティティ格納更新をスケジュールまたは監視する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="febfa-106">Administrators do not need to schedule or monitor the Entity store refresh with the system batch schedules.</span></span> <span data-ttu-id="febfa-107">更新操作は予想待機時間に基づいています。</span><span class="sxs-lookup"><span data-stu-id="febfa-107">The refresh operation is based on anticipated latency.</span></span> <span data-ttu-id="febfa-108">この機能は、Platform update 23 で有効化されます。</span><span class="sxs-lookup"><span data-stu-id="febfa-108">This functionality is enabled in Platform update 23.</span></span> <span data-ttu-id="febfa-109">管理者として、この機能を使用するためにオプトインを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="febfa-109">As an administrator you do need to opt-in to use this feature.</span></span>

## <a name="enable-automated-refresh"></a><span data-ttu-id="febfa-110">自動化更新を有効にする</span><span class="sxs-lookup"><span data-stu-id="febfa-110">Enable automated refresh</span></span>
<span data-ttu-id="febfa-111">以下の手順を完了して自動化エンティティ格納更新を有効にします。</span><span class="sxs-lookup"><span data-stu-id="febfa-111">Complete the following steps to enable automated Entity store refresh.</span></span>

1. <span data-ttu-id="febfa-112">**システム管理** > **セットアップ** > **エンティティ格納** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="febfa-112">Go to **System administration** > **Set up** > **Entity store**.</span></span> <span data-ttu-id="febfa-113">**エンティティ店舗** ページで、メッセージに、**自動エンティティ格納更新** オプションに切り替えることができることが示されます。</span><span class="sxs-lookup"><span data-stu-id="febfa-113">On the **Entity store** page, a message indicates that you can switch to the **Automated Entity store refresh** option.</span></span> <span data-ttu-id="febfa-114">このオプションは、システムによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="febfa-114">This option is managed by the system.</span></span> <span data-ttu-id="febfa-115">管理者はエンティティ格納更新をスケジュールまたは監視する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="febfa-115">An admin does not have to schedule or monitor the Entity store refresh.</span></span>

2. <span data-ttu-id="febfa-116">**今すぐ切り替える** を選択します。</span><span class="sxs-lookup"><span data-stu-id="febfa-116">Select **Switch now**.</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="febfa-117">このアクションは、元に戻すことはできません。</span><span class="sxs-lookup"><span data-stu-id="febfa-117">This action isn't reversible.</span></span> <span data-ttu-id="febfa-118">**自動エンティティ格納更新** オプションに切り替えた後、古いユーザー インターフェイス (UI) エクスペリエンスに戻すことはできません。</span><span class="sxs-lookup"><span data-stu-id="febfa-118">After you switch to the **Automated Entity store refresh** option, you can't revert to the old user interface (UI) experience.</span></span>

3. <span data-ttu-id="febfa-119">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="febfa-119">Select **Yes** to continue.</span></span>

<span data-ttu-id="febfa-120">新しいエクスペリエンスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="febfa-120">You will now see the new experience.</span></span>

![新しい UI エクスペリエンス](./media/entity-store-data-lake-3.JPG)

<span data-ttu-id="febfa-122">新しいエクスペリエンスをオンにすると、それぞれの集計の測定で更新を定義できます。</span><span class="sxs-lookup"><span data-stu-id="febfa-122">After the new experience is turned on, you can define the refresh for each aggregate measurement.</span></span> <span data-ttu-id="febfa-123">次の更新オプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="febfa-123">The following refresh options are available:</span></span>

- <span data-ttu-id="febfa-124">1 時間ごと</span><span class="sxs-lookup"><span data-stu-id="febfa-124">Every hour</span></span>
- <span data-ttu-id="febfa-125">1 日に 2 回</span><span class="sxs-lookup"><span data-stu-id="febfa-125">Twice a day</span></span>
- <span data-ttu-id="febfa-126">1 日に 1 回</span><span class="sxs-lookup"><span data-stu-id="febfa-126">Once a day</span></span>
- <span data-ttu-id="febfa-127">1 週間に 1 回</span><span class="sxs-lookup"><span data-stu-id="febfa-127">Once a week</span></span>

<span data-ttu-id="febfa-128">**更新** ボタンをクリックすることにより、管理者が必要に応じて任意の集計測定を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="febfa-128">An admin can also refresh any aggregate measurement on demand by clicking the **Refresh** button.</span></span> <span data-ttu-id="febfa-129">追加のオプションは、将来のプラットフォーム更新プログラムで追加されます。</span><span class="sxs-lookup"><span data-stu-id="febfa-129">Additional options will be added in future platform updates.</span></span> <span data-ttu-id="febfa-130">これらのオプションには、リアルタイム更新のオプションが含められます。</span><span class="sxs-lookup"><span data-stu-id="febfa-130">These options will include options for real-time refresh.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="febfa-131">自動化更新を有効にすると、システムは集計測定の更新を無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="febfa-131">When automated refresh is enabled, the system can disable the refresh of aggregate measurements.</span></span> <span data-ttu-id="febfa-132">集計測定に戻って、適切な更新間隔が適用されていることを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="febfa-132">You must revisit aggregate measurements and validate that appropriate refresh intervals have been applied.</span></span>