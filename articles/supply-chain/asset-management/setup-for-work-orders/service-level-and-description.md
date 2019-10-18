---
title: サービス レベルと説明
description: このトピックでは、資産管理のサービス レベルと説明について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e645c25208f55b1032bc7f7c181c72db7a2f265
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874650"
---
# <a name="service-level-and-description"></a><span data-ttu-id="a2951-103">サービス レベルと説明</span><span class="sxs-lookup"><span data-stu-id="a2951-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a2951-104">ワーク オーダーを作成するときに、そのサービス レベルを定義し、そのサービス レベルに一般的な説明を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="a2951-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="a2951-105">**ワーク オーダー サービス レベル**のページでワーク オーダー サービス レベルを作成し、**ワーク オーダーの説明**のページで説明を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="a2951-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="a2951-106">サービス レベルの作成</span><span class="sxs-lookup"><span data-stu-id="a2951-106">Create a service level</span></span>

1. <span data-ttu-id="a2951-107">**資産管理** \> **設定** \> **ワーク オーダー** \> **サービス レベル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2951-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="a2951-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2951-108">Select **New**.</span></span>
3. <span data-ttu-id="a2951-109">**サービス レベル** フィールドに、サービス レベル (番号など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2951-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="a2951-110">**名前**フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2951-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="a2951-111">**ワーク オーダー** クイック タブでは、開始予定日時と終了予定日時を定義できます。</span><span class="sxs-lookup"><span data-stu-id="a2951-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="a2951-112">このファスト タブのフィールドは、ワーク オーダーを開始および終了する期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="a2951-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="a2951-113">これらは、手動で作成されたワーク オーダーや、メンテナンス要求に基づいて作成されたワーク オーダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2951-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="a2951-114">**開始日**のフィールドに日数を入力して、ワーク オーダーを開始する期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="a2951-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="a2951-115">日数は、ワーク オーダーの作成日から計算されます。</span><span class="sxs-lookup"><span data-stu-id="a2951-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="a2951-116">たとえば、作成時にワーク オーダーを開始する場合は、**0** を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2951-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="a2951-117">ワーク オーダーが作成されてから 1 週間以内に開始する場合は、**7** を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2951-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="a2951-118">開始日に加えてワーク オーダーに開始時刻を設定するには、**開始時刻の設定**オプションを **はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a2951-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="a2951-119">次に、**開始時刻**フィールドに開始時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2951-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="a2951-120">このオプションを**いいえ**に設定した場合は、現在の時刻が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2951-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="a2951-121">**終了日**のフィールドに日数を入力して、ワーク オーダーを終了する期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="a2951-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="a2951-122">日数は、ワーク オーダーの開始日から計算されます。</span><span class="sxs-lookup"><span data-stu-id="a2951-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="a2951-123">たとえば、開始日から 1 週間以内にワーク オーダーを終了する場合は **7** と入力します。</span><span class="sxs-lookup"><span data-stu-id="a2951-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="a2951-124">終了日に加えてワーク オーダーに終了時刻を設定するには、**終了時刻の設定**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a2951-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="a2951-125">次に、**終了時刻**フィールドに終了時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2951-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="a2951-126">このオプションを**いいえ**に設定した場合は、現在の時刻が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2951-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="a2951-127">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2951-127">Select **Save**.</span></span>

![図 1](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="a2951-129">説明の作成</span><span class="sxs-lookup"><span data-stu-id="a2951-129">Create a description</span></span>

1. <span data-ttu-id="a2951-130">**資産管理** \> **設定** \> **ワーク オーダー** \> **説明**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2951-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="a2951-131">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2951-131">Select **New**.</span></span>
3. <span data-ttu-id="a2951-132">**説明**フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2951-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="a2951-133">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2951-133">Select **Save**.</span></span>